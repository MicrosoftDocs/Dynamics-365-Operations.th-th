---
title: รีเซ็ตชุดงานที่ติดค้าง
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาที่มีชุดงานที่ติดขัด
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053526"
---
# <a name="reset-stuck-batch-jobs"></a>รีเซ็ตชุดงานที่ติดค้าง

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>ออก

Microsoft Dynamics 365 Human Resources สามารถพบปัญหาเกี่ยวกับชุดงานที่ติดขัดในสถานะ **กำลังดำเนินการ** หรือ **กำลังยกเลิก** และไม่เสร็จสมบูรณ์

## <a name="resolution"></a>ความละเอียด

เมื่อชุดงานติดค้างอยู่ในสถานะ **กำลังดำเนินการ** หรือ **กำลังยกเลิก** คุณสามารถรีเซ็ตสถานะโดยการบังคับการยกเลิกงาน หลังจากที่คุณยกเลิกชุดงานแล้ว คุณสามารถรีเซ็ตชุดงานได้โดยการตั้งค่าเป็นสถานะ **กำลังรอ** จากนั้น จะถูกเลือกอีกครั้งสำหรับการดำเนินการในการรันชุดงานที่จัดกำหนดการไว้ถัดไป

1. ในพื้นที่ทำงาน **การจัดการระบบ** ให้เลือกหน้า **ลิงค์** และเลือก **ชุดงาน**

2. ในหน้ารายการ **ชุดงาน** ให้เลือกงานที่ต้องถูกรีเซ็ต

3. บน Ribbon การดำเนินการ เลือก **บังคับให้ยกเลิก** และยืนยันการดำเนินการ

   > [!NOTE]
   > การดำเนินการ **บังคับให้ยกเลิก** จะพร้อมใช้งานเฉพาะเมื่อชุดงานที่เลือกมีสถานะเป็น **กำลังดำเนินการ** หรือ **กำลังยกเลิก** และไม่มีการรันการดำเนินการชุดงานหรือกระบวนการยกเลิกสำหรับงาน

4. บน Ribbon การดำเนินการ เลือก **เปลี่ยนสถานะ**

5. บนหน้า **เลือกสถานะใหม่** ให้เลือก **กำลังรอ** แล้วจากนั้น เลือก **ตกลง**

   ![เลือกสถานะชุดงานใหม่](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ปรับปรุงประสิทธิภาพการทำงานโดยการจัดกำหนดการชุดงานหลังเวลาทำการ](hr-admin-troubleshooting-batch-jobs.md)<br>
[ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
