---
title: ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท '
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184381"
---
# <a name="configure-financial-cross-company-data-sharing"></a>ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท  ใช้บริษัท USMF และข้อมูลทางการเงินซึ่งใช้เท็มเพลตร่วมกัน 

คำแนะนำงานนี้ต้องการแพลตฟอร์ม Dynamics AX 7.1 หรือใหม่กว่า

1. ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > พื้นที่ทำงาน > การจัดการข้อมูล**
2. คลิก **นำเข้า**
3. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ **รูปแบบข้อมูลต้นทาง** ให้เลือกชนิด 'แพคเกจ' คลิก **อัพโหลด** นำทางไปยังสถานที่ของข้อมูลทางการเงินที่ใช้ไฟล์แพคเกจเท็มเพลตร่วมกัน และเลือกไฟล์นั้น
5. คลิก **บันทึก**
6. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก เลือกข้อมูลที่ใช้นโยบายร่วมกัน ที่เพิ่งถูกสร้างขึ้น  
7. คลิก **นำเข้า**
8. คลิก **ปิด**
9. รีเฟรชหน้า
10. ปิดหน้า
11. ปิดหน้า
12. ปิดหน้า
13. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการระบบ > ตั้งค่า > ตั้งค่าคอนฟิกการใช้ข้อมูลร่วมกันข้ามบริษัท**
14. ในรายการนี้ ให้ค้นหาและเลือก **จำนวนวันการชำระเงิน**
15. คลิก **เพิ่ม**
16. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
17. ในฟิลด์ **บริษัท** ให้ป้อน 'USSI'
18. คลิก **เพิ่ม**
19. ในฟิลด์ **บริษัท** ให้ป้อน 'USMF'
20. คลิก **บันทึก**
21. คลิก **เปิดใช้งาน**
22. คลิก **ใช่** 
23. คลิก **ค้นหาปัญหาที่มีร่วมกัน**
24. คลิก **ใช่** 
25. คลิก **อัพเดตค่าฟิลด์**
26. คลิก **ใช้ค่าจากบริษัท 1**
27. รีเฟรชหน้า
28. ปิดหน้า

