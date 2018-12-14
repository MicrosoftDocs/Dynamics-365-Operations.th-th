---
title: "ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ PowerApps ได้"
description: "หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าผู้ดูแลระบบไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Microsoft PowerApps ได้"
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
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ PowerApps ได้

[!include [banner](includes/banner.md)]

**ออก**

- ผู้ดูแลระบบผู้เช่า/สภาพแวดล้อม ไม่สามารถสร้างได้ในศูนย์การจัดการ Microsoft PowerApps ได้
- ยังไม่มีการกำหนดลิขสิทธิ์ที่ให้ผู้ใช้มีสิทธิ์ในการดำเนินการขั้นตอนการสร้างสภาพแวดล้อมให้ผู้ใช้ที่กำลังดำเนินการขั้นตอนนั้นโดยตรง

**โซลูชัน**

ตรวจสอบให้แน่ใจว่า ผู้ดูแลระบบผู้เช่าได้กำหนดให้ลิขสิทธิ์ PowerApps P2 ที่ถูกต้องโดยตรงให้กับผู้ใช้ที่จะดำเนินการขั้นตอนการสร้างสภาพแวดล้อม นี่คือแผนการบริการ Microsoft Dynamics ที่ให้สิทธิ์นั้น

| หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)       | แผนการบริการ PowerApps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps สำหรับ Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps สำหรับ Dynamics 365 |

โปรดทราบว่า Microsoft Office SKUs ต่างๆ ยังให้สิทธิ์ ร่วมกับ PowerApps Plan 2 SKUs แบบสแตนด์อโลน จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่

1. ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)
2. สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)

