---
title: ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps
description: บทความนี้อธิบายสิ่งที่ต้องทำ หากผู้ดูแลไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420741"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>ไม่สามารถสร้างสภาพแวดล้อมในศูนย์การจัดการ Power Apps

**ออกใช้**

- ผู้เช่า/ผู้ดูแลสภาพแวดล้อมไม่สามารถสร้างสภาพแวดล้อมได้ในศูนย์การจัดการ Microsoft Power Apps
- ยังไม่มีการกำหนดลิขสิทธิ์ที่ให้ผู้ใช้มีสิทธิ์ในการดำเนินการขั้นตอนการสร้างสภาพแวดล้อมให้ผู้ใช้ที่กำลังดำเนินการขั้นตอนนั้นโดยตรง

**โซลูชัน**

ตรวจสอบให้แน่ใจว่า ผู้ดูแลระบบผู้เช่าได้กำหนดให้ลิขสิทธิ์ Power Apps P2 ที่ถูกต้องโดยตรงให้กับผู้ใช้ที่จะดำเนินการขั้นตอนการสร้างสภาพแวดล้อม นี่คือแผนบริการ Microsoft Dynamics ที่ให้สิทธิ์นั้น

| หน่วยการเก็บสต็อกสินค้าของผลิตภัณฑ์โดยรวม (SKU)       | Power Apps แผนบริการ P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps สำหรับ Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps สำหรับ Dynamics 365 |

โปรดทราบว่า Microsoft Office SKU ที่หลากหลายยังให้สิทธิ์ พร้อมกับ Power Apps Plan 2 SKUs แบบสแตนด์อโลนอีกด้วย จุดสำคัญคือว่า หนึ่งใน SKUs เหล่านี้ต้องมีอยู่

1. ไปที่ [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments)
2. สร้างสภาพแวดล้อมโดยการปฏิบัติตามคำแนะนำใน [การเตรียมใช้งานทรัพยากรบุคคล](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)


[!INCLUDE[footer-include](../includes/footer-banner.md)]