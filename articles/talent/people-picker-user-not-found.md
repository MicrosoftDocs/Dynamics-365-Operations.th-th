---
title: ไม่พบผู้ใช้ในตัวเลือกบุคคลใน Attract หรือ Onboard
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำเมื่อผู้ใช้ในผู้เช่าบริษัทไม่แสดงขึ้นในตัวเลือกบุคคลในแอพลิเคชัน Dynamics 365 Talent - Attract และ Onboard
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
ms.openlocfilehash: a6d916f87ca30aa7405a51841e56ab31bbe31ac8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462754"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>ไม่พบผู้ใช้ในตัวเลือกบุคคลใน Attract หรือ Onboard

[!include [banner](includes/banner.md)]

## <a name="issue"></a>ออกใช้

ผู้ใช้ที่มีผลบังคับใช้บางคนใน Microsoft Azure Active Directory (Azure AD) สำหรับผู้เช่าไม่ปรากฏเมื่อค้นหาชื่อในตัวเลือกบุคคลในแอพลิเคชัน Dynamics 365 Talent: Attract หรือ Dynamics 365 Talent: Onboard

## <a name="cause"></a>สาเหตุ

ชนิดผู้ใช้บางชนิดยังไม่ได้รับการสนับสนุนในแอพลิเคชัน Attract and Onboard ในขณะนี้ ตรวจสอบว่าผู้ใช้ไม่ใช่ผู้ใช้ที่เป็นแขกของ Azure AD Business to Business (B2B) ข้อมูล "ชนิดของผู้ใช้" มีอยู่ในเบลด Azure Active Directory บนพอร์ทัล Azure

ดูข้อมูลเพิ่มเติมเกี่ยวกับ Azure B2B ดูที่ [อะไรคือการเข้าถึงของผู้ใช้ที่เป็นแขกใน Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b)

สำหรับผู้ใช้ที่ไม่ใช่ B2B มีผู้ใช้บางชนิดที่อาจมีคุณสมบัติ "ชนิดของผู้ใช้" ที่ไม่เสร็จสมบูรณ์ในออบเจ็กต์ **ผู้ใช้** สิ่งนี้สามารถตรวจสอบและแก้ไขได้โดยใช้โมดูล Azure AD Powershell สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0)

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
