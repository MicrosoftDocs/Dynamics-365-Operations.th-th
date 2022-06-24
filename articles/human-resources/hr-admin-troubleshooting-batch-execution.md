---
title: รีเซ็ตชุดงานที่ติดค้าง
description: บทความนี้อธิบายวิธีการแก้ไขปัญหาที่มีชุดงานที่ติดขัด
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896031"
---
# <a name="reset-stuck-batch-jobs"></a>รีเซ็ตชุดงานที่ติดค้าง


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>ออก

Microsoft Dynamics 365 Human Resources สามารถพบปัญหาเกี่ยวกับชุดงานที่ติดขัดในสถานะ **กำลังดำเนินการ** หรือ **กำลังยกเลิก** และไม่เสร็จสมบูรณ์

## <a name="resolution"></a>ความละเอียด

เมื่อชุดงานติดค้างอยู่ในสถานะ **กำลังดำเนินการ** หรือ **กำลังยกเลิก** คุณสามารถรีเซ็ตสถานะโดยการบังคับการยกเลิกงาน หลังจากที่คุณยกเลิกชุดงานแล้ว คุณสามารถรีเซ็ตชุดงานได้โดยการตั้งค่าเป็นสถานะ **กำลังรอ** จากนั้น จะถูกเลือกอีกครั้งสำหรับการดำเนินการในการเรียกใช้ชุดงานที่จัดกำหนดการไว้ถัดไป

1. ในพื้นที่ทำงาน **การจัดการระบบ** ให้เลือกหน้า **ลิงค์** และเลือก **ชุดงาน**

2. ในหน้ารายการ **ชุดงาน** ให้เลือกงานที่ต้องถูกรีเซ็ต

3. บน Ribbon การดำเนินการ เลือก **บังคับให้ยกเลิก** และยืนยันการดำเนินการ

   > [!NOTE]
   > การดำเนินการ **บังคับให้ยกเลิก** จะพร้อมใช้งานเฉพาะเมื่อชุดงานที่เลือกมีสถานะเป็น **กำลังดำเนินการ** หรือ **กำลังยกเลิก** และไม่มีการเรียกใช้การดำเนินการชุดงานหรือกระบวนการยกเลิกสำหรับงาน

4. บน Ribbon การดำเนินการ เลือก **เปลี่ยนสถานะ**

5. บนหน้า **เลือกสถานะใหม่** ให้เลือก **กำลังรอ** แล้วจากนั้น เลือก **ตกลง**

   ![เลือกสถานะชุดงานใหม่](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ปรับปรุงประสิทธิภาพการทำงานโดยการจัดกำหนดการชุดงานหลังเวลาทำการ](hr-admin-troubleshooting-batch-jobs.md)<br>
[ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
