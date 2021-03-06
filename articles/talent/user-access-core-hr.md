---
title: ผู้ใช้สามารถเข้าถึงทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 Talent - ทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึง Attract หรือ Onboard ได้
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462692"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>ผู้ใช้สามารถเข้าถึงทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้

[!include [banner](includes/banner.md)]

**รายละเอียดสภาพแวดล้อม**

- การปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS) ถูกดำเนินการโดยผู้ใช้ A
- ผู้ใช้ A เพิ่มผู้ใช้ B เป็นผู้ใช้ไปยัง Microsoft Dynamics 365 Human Resources

**ออกใช้**

ผู้ใช้ B สามารถเข้าถึงทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึงแอป Talent: Attract หรือ Talent: Onboard ได้ เมื่อผู้ใช้พยายามไปยัง **แอปประสบการณ์** เขาหรือเธอจะถูกนำไปยังสภาพแวดล้อมการทดลองแทน

**โซลูชัน**

ผู้ใช้ B ต้องได้รับมอบหมายสิทธิ์เพื่อดูสภาพแวดล้อม Microsoft Power Apps ที่ผู้ใช้ A สร้างในระหว่างกระบวนการการจัดเตรียม

สำหรับข้อมูล ให้ดูส่วน "การอนุญาตให้เข้าถึงสภาพแวดล้อม" ใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)

**วิธีแก้ปัญหาระยะยาว**

Microsoft กำลังพิจารณาการกำหนดสิทธิ์ที่เหมาะสมให้กับ Onboard และ Attract โดยอัตโนมัติ เมื่อผู้ใช้ถูกเพิ่มลงในทรัพยากรบุคคล


[!INCLUDE[footer-include](../includes/footer-banner.md)]