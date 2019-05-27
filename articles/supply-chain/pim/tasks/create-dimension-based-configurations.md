---
title: สร้างการจัดโครงแบบตามมิติ
description: 'กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9190d6dfd4b3f6cf0634e86845e7de028631bdd4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568500"
---
# <a name="create-dimension-based-configurations"></a>สร้างการจัดโครงแบบตามมิติ

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ  นี่คือกระบวนงานสุดท้ายในชุดที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ การดำเนินการกระบวนงานนี้จะขึ้นอยู่กับข้อมูลที่สร้างขึ้นในการบันทึกเจ็ดรายการก่อนหน้านี้ ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF


## <a name="find-the-dimension-based-product-master"></a>หาผลิตภัณฑ์หลักตามมิติ
1. คลิก การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้
2. คลิกผลิตภัณฑ์ต่างๆที่นำออกใช้
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * เลือกผลิตภัณฑ์หลักตามมิติ ที่คุณสร้างขึ้นในการบันทึกแรกในลำดับงานของการบันทึก 8 รายการนี้  

## <a name="create-configurations"></a>สร้างการตั้งค่าคอนฟิก
1. ในหน้าต่างการดำเนินการด้านวิศวกรรม คลิกรักษาโครงแบบ
2. คลิกตั้งค่าคอนฟิก
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
    * เลือกสินค้าใดๆของกลุ่มการปรับเปลี่ยนแรก  
5. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
6. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
    * เลือกสินค้าใดๆจากกลุ่มการปรับเปลี่ยนที่สอง  
7. คลิก ตกลง
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. ในฟิลด์การตั้งค่าคอนฟิก ให้พิมพ์ค่าใดค่าหนึ่ง
    * ป้อนชื่อของกลุ่มการปรับเปลี่ยนที่จะทำให้ง่ายต่อการระบุการปรับเปลี่ยน  
10. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
    * ป้อนคำอธิบายของการปรับเปลี่ยนเพื่ออธิบายส่วนประกอบ  
11. คลิก ตกลง

