---
title: แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง
description: 'กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd884362393674a4f55ea0410548edbb72786fff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465401"
---
# <a name="modify-reporting-relationships-for-a-position"></a>แก้ไขความสัมพันธ์การรายงานสำหรับตำแหน่ง

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



กระบวนงานนี้แสดงวิธีการเปลี่ยนแปลงความสัมพันธ์การรายงานสำหรับพนักงาน  ความสัมพันธ์การรายงานที่สามารถใช้สำหรับเอกสารการกำหนดเส้นทางโดยใช้ลำดับงาน  กระบวนงานยังแสดงวิธีการกำหนดพนักงานให้กับลำดับชั้นเพิ่มเติมอีกด้วย  ตัวอย่างเช่น พนักงานอาจจะเป็นส่วนหนึ่งของทีมโครงการที่มีความสัมพันธ์การรายงานแบบไม่เป็นทางการกับหัวหน้างานโครงการ  คุณสามารถกำหนดความสัมพันธ์การรายงานเพิ่มเติมในตำแหน่งเพื่อรองรับโครงการหรือเมตริกซ์สถานการณ์ต่างๆ  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF

1. ไปที่ทรัพยากรบุคคล > ตำแหน่ง > ตำแหน่ง
2. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด  ตัวอย่างเช่น กรองข้อมูลในฟิลด์ตำแหน่งด้วยค่า '000091'
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ขยายส่วนรายงานไปยังตำแหน่ง
5. คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง
6. ในฟิลด์รายงานไปยัง ให้ป้อนหรือเลือกค่า
7. คลิก สร้าง
8. ขยายส่วนความสัมพันธ์
9. คลิก เพิ่ม
10. เลือกกล่องกาเครื่องหมายทางซ้ายมือของกริด
11. ในฟิลด์ชื่อลำดับชั้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ตัวอย่าง: โครงการ  
12. ในฟิลด์รายงานไปยังตำแหน่ง ให้ป้อนหรือเลือกค่า   ตัวอย่าง:  000437
13. คลิก บันทึก



[!INCLUDE[footer-include](../includes/footer-banner.md)]