---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679851"
---
# <a name="create-new-users"></a>การสร้างผู้ใช้ใหม่

[!include [banner](../../includes/banner.md)]

ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>เชื่อมโยงผู้ใช้ที่มีสิทธิ์การใช้งาน (ชนิดใบอนุญาตใหม่เท่านั้น)
สำหรับลูกค้าที่ใช้ใบอนุญาตชนิดใหม่ที่เพิ่งมีการเพิ่มเมื่อเดือนตุลาคม 2019 ผู้ใช้ต้องเชื่อมโยงกับสิทธิ์การใช้งาน ในครั้งแรกที่ลงชื่อเข้าใช้ ผู้ใช้ที่ได้เชื่อมโยงสิทธิ์การใช้งานแล้ว จะถูกเพิ่มเป็นผู้ใช้ของระบบที่ไม่มีบทบาทโดยอัตโนมัติ

ผู้ดูแลระบบสามารถ [กำหนดสิทธิ์การใช้งานให้กับผู้ใช้](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) ใน [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>เชื่อมโยงผู้ใช้ภายนอกกับสิทธิ์การใช้งาน (ชนิดของสิทธิ์การใช้งานใหม่เท่านั้น)
ผู้ใช้ที่อยู่ภายนอกผู้เช่าที่มีการปรับใช้สภาพแวดล้อมจำเป็นต้องแสดงในไดเรกทอรีผู้เช่าโฮสต์ (Azure Active Directory (Azure AD)) เพื่อให้สามารถมอบสิทธิ์การใช้งานให้ได้ ควรเพิ่มผู้ใช้ภายนอกเหล่านั้นในผู้เช่าใน Azure AD ให้เป็นผู้ใช้ที่เป็นผู้เยี่ยมชม แล้วจึงมอบสิทธิ์การใช้งานที่เหมาะสม สำหรับข้อมูลเพิ่มเติม ดู [เพิ่ม Azure Active Directory ผู้ใช้ที่ทำงานร่วมกันแบบ B2B ในพอร์ทัล Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)

## <a name="add-a-new-user"></a>เพิ่มผู้ใช้ใหม่
1. ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**
2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
3. ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนรหัสเฉพาะสำหรับผู้ใช้ ต้องมีรหัสผู้ใช้  
4. ในฟิลด์ **ชื่อผู้ใช้** ให้ป้อนชื่อของผู้ใช้  
5. ในฟิลด์  **โดเมน** ให้ป้อนโดเมนของผู้ใช้  
6. ในฟิลด์ **นามแฝง** ให้ป้อนนามแฝงของผู้ใช้  
7. ในฟิลด์ **บริษัท** เลือกบริษัทที่ต้องการ 
8. ใน FastTab **บทบาทผู้ใช้** เลือก **มอบหมายบทบาท** เพื่อมอบหมายผู้ใช้ไปยัง Security role  สำหรับข้อมูลเพิ่มเติม ดู [มอบหมาย Security role ให้กับผู้ใช้](assign-users-security-roles.md)
9. เลือก **ตกลง**
10. เลือก **บันทึก**

## <a name="import-users"></a>นำเข้าผู้ใช้
1. ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**
2. ในบานหน้าต่างการดำเนินการ ให้เลือก **นำเข้าผู้ใช้**
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. เลือก **นำเข้าผู้ใช้**
5. เลือก **ปิด**

