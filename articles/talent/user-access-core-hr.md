---
title: "ผู้ใช้สามารถเข้าถึง Core HR ได้ แต่ไม่ใช่แอป Onboard หรือ Attract"
description: "หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาที่ซึ่งผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 for Talent Core HR แต่ไม่สามารถเข้าถึงแอป Attract หรือ Onboard ได้"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>ผู้ใช้สามารถเข้าถึง Core HR ได้ แต่ไม่ใช่แอป Onboard หรือ Attract

[!include [banner](includes/banner.md)]

**รายละเอียดสภาพแวดล้อม**

- มีการทำการปรับใช้ Microsoft Dynamics Lifecycle Services (LCS) โดยผู้ใช้ A
- ผู้ใช้ A เพิ่มผู้ใช้ B เป็นผู้ใช้ไปยัง Microsoft Dynamics 365 for Talent Core HR

**ออก**

ผู้ใช้ B สามารถเข้าถึง Core HR ได้ แต่ไม่สามารถเข้าถึง Talent: Attract หรือ Talent: แอป Onboard ได้ เมื่อผู้ใช้พยายามไปยัง **แอปประสบการณ์** เขาหรือเธอจะถูกนำไปยังสภาพแวดล้อมการทดลองแทน

**โซลูชัน**

ผู้ใช้ B ต้องได้รับมอบสิทธิ์ในการดูสภาพแวดล้อม Microsoft PowerApps ที่ผู้ใช้ A สร้างขึ้นในระหว่างกระบวนการเตรียมใช้งาน

สำหรับข้อมูล ให้ดูส่วน "การอนุญาตให้เข้าถึงสภาพแวดล้อม" ใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)

**วิธีแก้ปัญหาระยะยาว**

Microsoft กำลังพิจารณาการกำหนดสิทธิ์ที่เหมาะสมให้กับ Onboard และ Attract โดยอัตโนมัติ เมื่อผู้ใช้ถูกเพิ่มลงใน Core HR

