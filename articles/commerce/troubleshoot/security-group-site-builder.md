---
title: ไม่สามารถตั้งค่าคอนฟิกกลุ่มความปลอดภัยของโปรแกรมสร้างไซต์ Commerce ในระหว่างการปรับใช้ครั้งแรก
description: บทความนี้จะแนะนําการแก้ไขปัญหาที่สามารถช่วยได้เมื่อกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) สําหรับโปรแกรมสร้างไซต์ Commerce ไม่ปรากฏเป็นตัวเลือกเมื่อคุณสร้างส่วนประกอบอีคอมเมิร์ซใน Microsoft Dynamics Lifecycle Services (LCS) ในระหว่างการปรับใช้ผู้เช่าอีเมลใหม่
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 797df828df16547eb3aef1f9865a663281fb9224
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899026"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>ไม่สามารถตั้งค่าคอนฟิกกลุ่มความปลอดภัยของโปรแกรมสร้างไซต์ Commerce ในระหว่างการปรับใช้ครั้งแรก

[!include [banner](../../includes/banner.md)]

บทความนี้จะแนะนําการแก้ไขปัญหาที่สามารถช่วยได้เมื่อกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) สําหรับโปรแกรมสร้างไซต์ Commerce ไม่ปรากฏเป็นตัวเลือกเมื่อคุณสร้างส่วนประกอบอีคอมเมิร์ซใน Microsoft Dynamics Lifecycle Services (LCS) ในระหว่างการปรับใช้ผู้เช่าอีเมลใหม่

## <a name="description"></a>คำอธิบาย

เมื่อคุณสร้างส่วนประกอบของอีคอมเมิร์ซเป็นส่วนหนึ่งของกระบวนการปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่ที่มีส่วนประกอบของโปรแกรมสร้างไซต์ Commerce กลุ่มรักษาความปลอดภัย Azure AD จะไม่ปรากฎขึ้นเป็นตัวเลือกในกล่องโต้ตอบ

## <a name="resolution"></a>ความละเอียด

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>เตรียมใช้งานไซต์อีคอมเมิร์ซให้กับผู้ใช้ในผู้เช่าที่ถูกต้อง

1. ไปที่ [พอร์ทัล Azure](https://portal.azure.com/)
1. ภายใต้ผู้เช่าที่เตรียมใช้งานโครงการ LCS สำหรับไซต์อีคอมเมิร์ซของคุณ ให้ปฏิบัติตามคําแนะนํา [การสร้างกลุ่มพื้นฐานและเพิ่มสมาชิกโดยใช้ Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
1. ไปที่ [LCS ](https://lcs.dynamics.com/) และลงชื่อเข้าใช้งานโดยใช้บัญชีที่ใช้ผู้เช่าเดียวกันกับกลุ่มรักษาความปลอดภัย Azure AD ที่คุณเพิ่งสร้างขึ้นร่วมกัน บัญชีต้องมีสิทธิ์เข้าดูกลุ่มรักษาความปลอดภัย Azure AD
1. ทำขั้นตอนการตั้งค่าเพื่อตั้งค่าคอนฟิกไซต์อีคอมเมิร์ซให้เสร็จ เมื่อคุณเตรียมใช้งานส่วนประกอบของอีคอมเมิร์ซ ขณะนี้กลุ่มรักษาความปลอดภัยควรปรากฏเป็นตัวเลือกในกล่องโต้ตอบ

> [!NOTE]
> เพื่อให้แน่ใจว่าฟิลด์ในกล่องโต้ตอบจะเติมด้วยรายการกลุ่มความปลอดภัย คุณต้องเลือก **ป้อน** หลังจากที่คุณป้อนชื่อของกลุ่มรักษาความปลอดภัย Azure AD ที่คุณสร้างขึ้น ผลการค้นหาจะแสดงรายการกลุ่มความปลอดภัย Azure AD ทั้งหมดที่ขึ้นต้นด้วยข้อความการค้นหา และที่ผู้ใช้มีสิทธิ์เข้าถึง คุณสามารถใช้เงื่อนไขการค้นหาสั้นๆ เพื่ออนุญาตให้ใช้ผลการค้นหาที่กว้างขึ้น

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การสร้างกลุ่มพื้นฐานและเพิ่มสมาชิกโดยใช้ Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่](../deploy-ecommerce-site.md)