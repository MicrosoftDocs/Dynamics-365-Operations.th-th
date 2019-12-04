---
title: ผู้ใช้สามารถเข้าถึง Core HR ได้แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 Talent - Core HR แต่ไม่สามารถเข้าถึง Attract หรือ Onboard ได้
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772930"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>ผู้ใช้สามารถเข้าถึง Core HR ได้แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้

[!include [banner](includes/banner.md)]

**รายละเอียดสภาพแวดล้อม**

- การปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS) ถูกดำเนินการโดยผู้ใช้ A
- ผู้ใช้ A เพิ่มผู้ใช้ B เป็นผู้ใช้ไปยัง Microsoft Dynamics 365 Talent: Core HR

**ออกใช้**

ผู้ใช้ B สามารถเข้าถึง Core HR ได้ แต่ไม่สามารถเข้าถึง Talent: Attract หรือ Talent: แอป Onboard ได้ เมื่อผู้ใช้พยายามไปยัง **แอปประสบการณ์** เขาหรือเธอจะถูกนำไปยังสภาพแวดล้อมการทดลองแทน

**โซลูชัน**

ผู้ใช้ B ต้องได้รับมอบหมายสิทธิ์เพื่อดูสภาพแวดล้อม Microsoft Power Apps ที่ผู้ใช้ A สร้างในระหว่างกระบวนการการจัดเตรียม

สำหรับข้อมูล ให้ดูส่วน "การอนุญาตให้เข้าถึงสภาพแวดล้อม" ใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)

**วิธีแก้ปัญหาระยะยาว**

Microsoft กำลังพิจารณาการกำหนดสิทธิ์ที่เหมาะสมให้กับ Onboard และ Attract โดยอัตโนมัติ เมื่อผู้ใช้ถูกเพิ่มลงใน Core HR
