---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570532"
---
# <a name="create-new-users"></a>การสร้างผู้ใช้ใหม่

[!include [task guide banner](../../includes/task-guide-banner.md)]

ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>เชื่อมโยงผู้ใช้ที่มีสิทธิ์การใช้งาน (ชนิดใบอนุญาตใหม่เท่านั้น)
สำหรับลูกค้าที่ใช้ใบอนุญาตชนิดใหม่ที่เพิ่งมีการเพิ่มเมื่อเดือนตุลาคม 2019 ผู้ใช้ต้องเชื่อมโยงกับสิทธิ์การใช้งาน ในครั้งแรกที่ลงชื่อเข้าใช้ ผู้ใช้ที่ได้เชื่อมโยงสิทธิ์การใช้งานแล้ว จะถูกเพิ่มเป็นผู้ใช้ของระบบที่ไม่มีบทบาทโดยอัตโนมัติ ผู้ใช้ที่ไม่ได้เชื่อมโยงสิทธิ์การใช้งาน จะได้รับข้อความแจ้งเตือน

ผู้ดูแลระบบสามารถ [กำหนดสิทธิ์การใช้งานให้กับผู้ใช้](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) ใน [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)

## <a name="add-a-new-user"></a>เพิ่มผู้ใช้ใหม่
1. ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**
2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
3. ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนรหัสเฉพาะสำหรับผู้ใช้ ต้องมีรหัสผู้ใช้  
4. ในฟิลด์ **ชื่อผู้ใช้** ให้ป้อนชื่อของผู้ใช้  
5. ในฟิลด์  **โดเมน** ให้ป้อนโดเมนของผู้ใช้  
6. ในฟิลด์ **นามแฝง** ให้ป้อนนามแฝงของผู้ใช้  
7. ในฟิลด์ **บริษัท** เลือกบริษัทที่ต้องการ 
8. บนแท็บด่วน **บทบาทของผู้ใช้** ให้เลือก **กำหนดบทบาท** ที่ [จะกำหนดบทบาทความปลอดภัยให้ผู้ใช้](assign-users-security-roles.md)
9. เลือก **ตกลง**
10. เลือก **บันทึก**

## <a name="import-users"></a>นำเข้าผู้ใช้
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **นำเข้าผู้ใช้**
2. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
3. เลือก **นำเข้าผู้ใช้**
4. เลือก **ปิด**

