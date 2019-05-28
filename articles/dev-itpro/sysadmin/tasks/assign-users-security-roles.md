---
title: กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย
description: เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations Enterprise edition ผู้ใช้ต้องได้รับมอบหมายไปยัง Security role
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556720"
---
# <a name="assign-users-to-security-roles"></a>กำหนดผู้ใช้ให้กับบทบาทความปลอดภัย

[!include [task guide banner](../../includes/task-guide-banner.md)]

เพื่อเข้าถึง Microsoft Dynamics 365 for Finance and Operations Enterprise edition ผู้ใช้ต้องได้รับมอบหมายไปยัง Security role กระบวนงานนี้อธิบายวิธีที่ผู้ดูแลระบบสามารถมอบหมายผู้ใช้ให้กับบทบาทโดยอัตโนมัติ ตามข้อมูลทางธุรกิจ  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF


## <a name="automatically-assign-users-to-roles"></a>กำหนดผู้ใช้ให้กับบทบาทโดยอัตโนมัติ
1. ไปที่ การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท
2. ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'
    * เลือกบทบาทที่คุณต้องการตั้งค่าคอนฟิกกฎ  ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี  
3. คลิกเพิ่มบทบาทเพื่อเปิดกล่องโต้ตอบการวาง
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกการสอบถามที่จะใช้สำหรับกฎนี้  
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
6. (คลิกแก้ไขการสอบถาม)
    * แก้ไขการสอบถาม เมื่อจำเป็น  
7. คลิก ตกลง

## <a name="exclude-users-from-automatic-role-assignment"></a>ชแยกผู้ใช้ออกจากการกำหนดบทบาทโดยอัตโนมัติ
1. ปิดหน้า
2. ไปที่ การจัดการระบบ > ความปลอดภัย > กำหนดผู้ใช้ให้กับบทบาท
3. ในแผนภูมิ ให้เลือก 'หัวหน้างานฝ่ายบัญชี'
    * เลือกบทบาท ในตัวอย่างนี้ เลือกหัวหน้างานฝ่ายบัญชี  
4. คลิกกำหนด / แยกผู้ใช้ ด้วยตนเอง
5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * เลือกผู้ใช้  
6. คลิกแยกออกจากบทบาท
    * คลิกการแยกออกจากบทบาท เพื่อแยกผู้ใช้ที่เลือกออกจากบทบาท  เพื่อลบการแยก ให้เลือกผู้ใช้ที่คุณต้องการลบการแยก แล้วคลิกสถานะรีเซ็ต  เมื่อคุณลบการแยกโดยการรีเซ็ตสถานะของผู้ใช้ บทบาทของผู้ใช้จะถูกมอบหมายโดยอัตโนมัติอีกครั้ง  อย่างไรก็ตาม ผู้ใช้จะไม่ถูกมอบหมายในทันทีให้กับบทบาท หรือถูกแยกจากบทบาทเมื่อคุณรีเซ็ตสถานะ  ผู้ใช้จะถูกมอบหมายให้กับบทบาทหรือถูกลบออกจากบทบาทในครั้งต่อไป อย่างใดอย่างหนึ่งแทน ซึ่งกฎสำหรับการมอบหมายบทบาทโดยอัตโนมัติจะถูกรัน  

