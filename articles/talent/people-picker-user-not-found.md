---
title: ไม่พบผู้ใช้ในตัวเลือกบุคคลใน Attract หรือ Onboard
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำเมื่อผู้ใช้ในผู้เช่าบริษัทไม่แสดงขึ้นในตัวเลือกบุคคลในแอพลิเคชัน Attract และ Onboard Dynamics 365 for Talent
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519206"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>ไม่พบผู้ใช้ Azure Active Directory ในตัวเลือกบุคคล

[!include [banner](includes/banner.md)]

## <a name="issue"></a>ออกใช้

ผู้ใช้ที่ถูกต้องบางอย่างใน Microsoft Azure Active Directory (Azure AD) สำหรับผู้เช่าไม่ปรากฏเมื่อค้นหาชื่อในตัวเลือกบุคคลในแอพลิเคชัน Attract และ Onboard Dynamics 365 for Talent

## <a name="cause"></a>สาเหตุ

ชนิดผู้ใช้บางอย่างยังไม่ได้รับการสนับสนุนในแอพลิเคชัน Attract และ Onboard ในขณะนี้ ตรวจสอบว่าผู้ใช้ไม่ใช่ผู้ใช้ที่เป็นแขกของ Azure AD Business to Business (B2B) ข้อมูล "ชนิดของผู้ใช้" มีอยู่ในเบลด Azure Active Directory บนพอร์ทัล Azure

ดูข้อมูลเพิ่มเติมเกี่ยวกับ Azure B2B ดูที่ [อะไรคือการเข้าถึงของผู้ใช้ที่เป็นแขกใน Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b)

สำหรับผู้ใช้ที่ไม่ใช่ B2B มีผู้ใช้บางชนิดที่อาจมีคุณสมบัติ "ชนิดของผู้ใช้" ที่ไม่เสร็จสมบูรณ์ในออบเจ็กต์ **ผู้ใช้** สิ่งนี้สามารถตรวจสอบและแก้ไขได้โดยใช้โมดูล Azure AD Powershell สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0)

## <a name="resolution"></a>ความละเอียด

เมื่อต้องการทำขั้นตอนต่อไปนี้ให้เสร็จเพื่อแก้ปัญหา คุณจะต้องมีสิทธิ์ "ผู้ดูแลระบบส่วนกลาง" บนผู้เช่า Azure Active Directory หรือสิทธิ์สำหรับ **User.ReadWrite.All**

เมื่อต้องการตรวจสอบ "ชนิดของผู้ใช้" สำหรับผู้ใช้ที่ได้รับผลกระทบ

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
คำสั่งจะส่งกลับข้อมูลต่อไปนี้
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
โปรดจดจำลักษณะ **UserType** ของผู้ใช้ ถ้า **UserType** ว่างเปล่า เช่น ไม่ใช่ "สมาชิก" หรือ "แขก" ให้อัพเดต **UserType** โดยใช้คำสั่งต่อไปนี้

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
