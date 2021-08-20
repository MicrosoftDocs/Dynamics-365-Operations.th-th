---
title: ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps
description: บทความนี้อธิบายสิ่งที่ต้องทำ หากผู้ดูแลไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ca9e3db374c46dd00f0bb2f1f655e9acaf87fcfd2699f94c6703905d544cd84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745729"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ออกใช้**

- ผู้เช่า/ผู้ดูแลสภาพแวดล้อมไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
- ผู้ใช้ไม่มีลิขสิทธิ์ที่มีสิทธิสร้างสภาพแวดล้อม

**โซลูชัน**

ตรวจสอบให้แน่ใจว่าผู้ดูแลระบบผู้เช่าได้มอบหมายลิขสิทธิ์ Power Apps P2 ที่ถูกต้องให้กับผู้ใช้ที่สร้างสภาพแวดล้อม แผนบริการ Microsoft Dynamics ต่อไปนี้จะให้สิทธิ์ในการสร้างสภาพแวดล้อม

| หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)       | Power Apps แผนบริการ P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps สำหรับ Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps สำหรับ Dynamics 365 |

โปรดทราบว่า Microsoft Office SKU ที่หลากหลายยังให้สิทธิ์ พร้อมกับ Power Apps Plan 2 SKUs แบบสแตนด์อโลนอีกด้วย จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่

1. ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)
2. สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [การเตรียมใช้งานทรัพยากรบุคคล](/dynamics365/unified-operations/talent/provisioning-talent)


[!INCLUDE[footer-include](../includes/footer-banner.md)]