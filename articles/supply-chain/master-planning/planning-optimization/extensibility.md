---
title: ความสามารถในการเพิ่มประสิทธิภาพการวางแผน
description: บทความนี้จะอธิบายสถาณการณ์ความสามารถในการเพิ่มฟังก์ชันที่ได้รับการสนับสนุนในการเพิ่มประสิทธิภาพการวางแผน
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857557"
---
# <a name="planning-optimization-extensibility"></a>ความสามารถในการเพิ่มประสิทธิภาพการวางแผน

[!include [banner](../../includes/banner.md)]

บทความนี้จะอธิบายสถาณการณ์ความสามารถในการเพิ่มฟังก์ชันที่เกี่ยวข้องกับการวางแผนหลักและได้รับการสนับสนุนในการเพิ่มประสิทธิภาพการวางแผน ความสามารถเหล่านี้จะพร้อมใช้งานเมื่อเริ่มต้นใน Microsoft Dynamics 365 Supply Chain Management เวอร์ชัน10.0.13

## <a name="custom-processing-when-master-planning-is-completed"></a>การประมวลผลแบบกำหนดเองเมื่อการวางแผนหลักเสร็จสมบูรณ์

ในสถานการณ์ความสามารถในการเพิ่มฟังก์ชันในการเพิ่มประสิทธิภาพการวางแผน การประมวลแบบกำหนดเองจะเสร็จสิ้นหลังจากอัปเดตแผนแล้ว ตัวอย่างเช่น คุณอาจเพิ่มคอลัมน์ในตารางแผนการใบสั่ง (`ReqPO`) หรือคุณอาจต้องการได้รับข้อมูลสถิติบางอย่างจากแผนที่สร้าง ความสามารถในการเพิ่มฟังก์ชันที่เปิดใช้งานสถานการณ์เหล่านี้คือวิธีการ `jobCompletedSuccessfully` ในคลาส `MpsMasterPlanningEvents`

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

ต่อไปนี้เป็นตัวอย่างของความสามารถในการเพิ่มฟังก์ชันที่ตั้งค่าฟิลด์ `CstmOrderPriority` แบบกำหนดเองบนแผนการใบสั่ง

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

เมื่อคุณเพิ่มตรรกะแบบกำหนดเอง ให้พิจารณาข้อจำกัดและแนวทางที่พึงปฏิบัติต่อไปนี้

- วิธีการ `jobCompletedSuccessfully` เรียกนอกขอบเขตธุรกรรม ดังนั้น แผนจึงมองเห็นได้โดยผู้ใช้เมื่อตรรกะที่กำหนดเองเริ่มรัน ถ้าการเลือกเองของคุณตั้งค่าฟิลด์เพิ่มเติมในแผนการใบสั่ง คุณควรแจ้งให้ผู้ใช้ทราบว่าค่าของฟิลด์เหล่านั้นจะสอดคล้องกันในที่สุด (กล่าวอีกอย่างคือ ฟิลด์อาจไม่มีวันที่ในทันทีหลังจากที่งานการวางแผนเสร็จสมบูรณ์)
- งานการวางแผนหลักอื่นสามารถเริ่มต้นได้เมื่อวิธีการ `jobCompletedSuccessfully` ถูกเรียกใช้ งานใหม่อาจส่งผลกระทบต่อแผนเต็มหรือบางส่วนของแผน งานใหม่อาจอัปเดตหรือลบธุรกรรมแผนการใบสั่งหรือความต้องการเดียวกันที่สร้างขึ้นหรืออัปเดตเป็นส่วนหนึ่งของงานการวางแผนที่มีการจัดการ `jobCompletedSuccessfully` อยู่ ต้องจัดการข้อยกเว้นความขัดแย้งของการอัปเดตเมื่อขยายเหตุการณ์นี้
- หลีกเลี่ยงการใช้ขอบเขตธุรกรรมเดียว เมื่อคุณขยายวิธีการนี้ การรันการวางแผนหลักหนึ่งๆ สามารถผลิตธุรกรรมความต้องการได้มากมาย และแผนการใบสั่งนับร้อยพัน หากธุรกรรมและแผนการใบสั่งทั้งหมดเหล่านี้ได้รับการประมวลผลในขอบเขตของธุรกรรมเดียว ล็อค SQL หลายตัวจะเกิดขึ้นและบล็อคกระบวนการวางแผนอื่นๆ นอกจากนี้ ถ้ามีการระงับธุรกรรมไว้เป็นเวลานาน "โกสต์เรกคอร์ด" จะถูกสร้างในฐานข้อมูล SQL โกสต์เรกคอร์ดจะมีผลกระทบในทางลบต่อทุกกระบวนการในระบบ


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]