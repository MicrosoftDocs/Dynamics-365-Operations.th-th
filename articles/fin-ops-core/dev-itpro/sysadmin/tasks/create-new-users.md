---
title: การสร้างผู้ใช้ใหม่
description: ผู้ใช้คือพนักงานภายในขององค์กรหรือลูกค้าและผู้จัดจำหน่ายภายนอก ซึ่งมีความจำเป็นต้องเข้าถึงระบบเพื่อดำเนินงานของตน
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00da7c69ff18abd02ca0cd7984e9b2de5e453a0c
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103339"
---
# <a name="create-new-users"></a>สร้างผู้ใช้ใหม่

[!include [banner](../../includes/banner.md)]

ก่อนที่คุณจะสามารถเข้าถึงแอปการเงินและการดำเนินงานได้ คุณต้องถูกเพิ่มลงในหน้า **ผู้ใช้** ก่อน (**การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**) ผู้ใช้รวมพนักงานภายในขององค์กร หรือลูกค้าและผู้จัดจำหน่ายภายนอก คุณสามารถนําเข้าหรือเพิ่มผู้ใช้ด้วยตนเอง ผู้ใช้ทั้งหมดต้องมีสิทธิ์ถูกต้องสำหรับการใช้งานตามกฎระเบียบ

สำหรับข้อมูลเกี่ยวกับวิธีการการซื้อและมอบสิทธิ์สำหรับแอปการเงินและการดำเนินงาน โปรดดูที่ [คู่มือการให้สิทธิ์การใช้งาน Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409)

## <a name="assign-a-license-to-a-user"></a>กำหนดสิทธิ์ให้กับผู้ใช้
ผู้ดูแลระบบสามารถ [กำหนดสิทธิ์การใช้งานให้กับผู้ใช้](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) ใน [Microsoft 365 admin center](/office365/admin/admin-overview/about-the-admin-center)

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>เพิ่มผู้ใช้ภายนอกใน Azure AD และกําหนดสิทธิ์ 
ผู้ใช้ภายนอกต้องถูกแสดงในไดเรกทอรีผู้เช่าของคุณ (Azure Active Directory (Azure AD)) เพื่อให้มีการกำหนดสิทธิ์ ควรเพิ่มผู้ใช้ภายนอกเหล่านั้นในผู้เช่าใน Azure AD ให้เป็นผู้ใช้ที่เป็นผู้เยี่ยมชม แล้วจึงมอบสิทธิ์การใช้งานที่เหมาะสม ความต้องการสำหรับแอปการเงินและการดำเนินงาน คือบริษัทของผู้ใช้ที่เป็นแขกจะต้องใช้ Azure AD สำหรับข้อมูลเพิ่มเติม ดู [เพิ่ม Azure Active Directory ผู้ใช้ที่ทำงานร่วมกันแบบ B2B ในพอร์ทัล Azure](/azure/active-directory/b2b/add-users-administrator)

## <a name="import-new-users-from-azure-ad"></a>นำเข้าผู้ใช้ใหม่จาก Azure AD 
1. ไปที่ **การจัดการระบบ** \> **ผู้ใช้** \> **ผู้ใช้**
2. ในบานหน้าต่างการดำเนินการ ให้เลือก **นำเข้าผู้ใช้**
3. เลือกผู้ใช้ที่จะถูกนำเข้า รายการประกอบด้วยผู้ใช้ Azure AD ที่ในขณะนี้ไม่ใช่ผู้ใช้ในสภาพแวดล้อมนี้
4. เลือก **นำเข้าผู้ใช้**
5. เลือก **ปิด**

> [!NOTE]
> ค่าของฟิลด์ **บริษัท** จะถูกตั้งค่าตามบริษัทในรอบเวลาปัจจุบันของผู้ดูแลระบบ หลังจากการนําเข้า คุณต้องกําหนดบทบาทและองค์กรตามที่เกี่ยวข้อง สำหรับข้อมูลเพิ่มเติม ดู [มอบหมาย Security role ให้กับผู้ใช้](assign-users-security-roles.md) นอกจากนี้ ยังอาจต้องเชื่อมโยงผู้ใช้กับ **บุคคล** และอัพเดตตัวเลือกผู้ใช้ เช่น ภาษา แบบมีเงื่อนไข

## <a name="manually-add-a-new-user"></a>เพิ่มผู้ใช้ใหม่ด้วยตนเอง
1. ไปที่ **การจัดการระบบ** \> **ผู้ใช้** \> **ผู้ใช้**
2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
3. ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนรหัสเฉพาะสำหรับผู้ใช้   
4. ในฟิลด์ **ชื่อผู้ใช้** ให้ป้อนชื่อของผู้ใช้  
5. ในฟิลด์ **ผู้ให้บริการ**:
 - สำหรับผู้ใช้ภายใน ให้ใช้ค่าเริ่มต้น ตัวอย่างเช่น ผู้เช่า Azure AD ของคุณที่นําหน้าด้วย https://sts.windows.net/  
 - สำหรับผู้ใช้ที่ไม่ใช่ Azure AD เช่น บัญชี Service-2-Service ให้ป้อนค่าข้อความพื้นฐาน ตัวอย่างเช่น NA ค่านี้จะช่วยหลีกเลี่ยงการเรียกการรับรองความถูกต้องที่ไม่ถูกต้อง ซึ่งอาจส่งผลให้เกิดข้อผิดพลาด ถ้ามีการใช้ค่าผู้ให้บริการข้อมูลประจำตัวที่ถูกต้อง  
 - สำหรับผู้ใช้ภายนอกหรือผู้ใช้ที่เป็นแขก ให้เพิ่มชื่อผู้เช่า Azure AD หลังจาก https://sts.windows.net/
6. ในฟิลด์ **อีเมล** ป้อนอยู่อีเมลแบบเต็มของผู้ใช้/ชื่อหลักการของผู้ใช้  
7. ในฟิลด์ **บริษัท** ให้เลือกบริษัทเริ่มต้นสำหรับผู้ใช้ 
8. เลือก **บันทึก**

ค่าต่างๆ สำหรับผู้ให้บริการข้อมูลประจำตัวและรหัสการวัดและส่งข้อมูลทางไกล จะได้รับการอัพเดตตามการเรียก [กราฟ Microsoft](/graph/overview) เมื่อมีการบันทึกเรกคอร์ดผู้ใช้ รหัสการวัดและส่งข้อมูลทางไกลจะขึ้นอยู่กับรหัสออบเจ็กต์/รหัสความปลอดภัย (SID) ของผู้ใช้ใน Azure AD

> [!NOTE]
> หลังจากที่คุณเพิ่มผู้ใช้แล้ว คุณต้องกําหนดบทบาทและองค์กรตามที่เกี่ยวข้อง สำหรับข้อมูลเพิ่มเติม ดู [มอบหมาย Security role ให้กับผู้ใช้](assign-users-security-roles.md) นอกจากนี้ ยังอาจต้องเชื่อมโยงผู้ใช้กับ **บุคคล** และอัพเดต **ตัวเลือกผู้ใช้** เช่น ภาษา แบบมีเงื่อนไข

## <a name="change-a-user-id"></a>เปลี่ยนรหัสผู้ใช้
เมื่อต้องการเปลี่ยนแปลงรหัสผู้ใช้ คุณต้องเปลี่ยนชื่อคีย์ในฐานข้อมูล เมื่อคุณเปลี่ยนรหัสผู้ใช้โดยใช้กระบวนงานนี้ การตั้งค่าของผู้ใช้ที่เกี่ยวข้องทั้งหมดจะถูกแก้ไขเพื่อใช้รหัสผู้ใช้ใหม่ ตัวอย่างเช่น ข้อมูลการใช้ในตาราง **SysLastValuy** จะถูกอัพเดตเพื่ออ้างอิงรหัสผู้ใช้ใหม่

> [!NOTE]
> รหัสผู้ใช้เป็นคีย์หลักของตารางข้อมูลผู้ใช้ การเปลี่ยนชื่อคีย์หลักอาจใช้เวลาสักพักสำหรับผู้ใช้ที่มีอยู่ เนื่องจากมีการอัพเดตการอ้างอิงทั้งหมดไปยังคีย์ในฐานข้อมูลด้วย 

1. ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**
2. เลือกผู้ใช้ในรายการ และเลือก **ตัวเลือก\> ข้อมูลเรกคอร์ด**
3. เลือก **เปลี่ยนชื่อ**
4. ป้อนค่าใหม่และค่าที่ไม่ซ้ำกันสำหรับรหัสผู้ใช้ และจากนั้น เลือก **ตกลง** 
5. เลือก **ใช่** เพื่อยืนยัน

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

สำหรับตัวเลือกเพิ่มเติมเพื่อปรับใช้ผู้ใช้ B2B โปรดดูที่ [ส่งออกผู้ใช้ B2B ไปยัง Azure AD](../implement-b2b.md)

สำหรับข้อมูลเกี่ยวกับบัญชีของระบบที่ตั้งค่าคอนฟิกไว้ล่วงหน้า โปรดดูที่ [บัญชีของระบบที่ตั้งค่าคอนฟิกไว้ล่วงหน้า](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
