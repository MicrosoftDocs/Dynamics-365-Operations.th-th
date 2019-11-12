---
title: ซิงโครไนส์ใบสั่งงานจากกับโครงการจาก Field Service ไปยัง Supply Chain Management
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Dynamics 365 Field Service ไปยัง Dynamics 365 Supply Chain Management
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5c57b8d1e09fd57611accec83ec3da4bc596fd00
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627562"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>ซิงโครไนส์ใบสั่งงานจากกับโครงการจาก Field Service ไปยัง Supply Chain Management

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Dynamics 365 Field Service ไปยัง Dynamics 365 Supply Chain Management

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

เท็มเพลต **ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Supply Chain Management)** ที่ใช้ เป็นไปตามเท็มเพลต **ใบสั่งงาน (Field Service ไปยัง Supply Chain Management)** สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์ใบสั่งงานใน Field Service กับใบสั่งขายใน Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)

หัวข้อนี้อธิบายความแตกต่างระหว่างสองเท็มเพลตเท่านั้น:
- **ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management)**
- **ใบสั่งงาน (Field Service ไปยัง Supply Chain Management)**

ความแตกต่างหลักที่ว่า เท็มเพลตนี้รวมการแม็ปของหมายเลขโครงการที่มอบหมายไปยังใบสั่งงานใน Field Service ซึ่งทำให้มั่นใจว่าใบสั่งขายที่สร้างใน Supply Chain Management รวมหมายเลขโครงการ และการออกใบแจ้งหนี้สามารถเกิดขึ้นได้ในโครงการที่เกี่ยวข้อง นอกจากนี้ เท็มเพลตที่ใช้การกรองและการสอบถามขั้นสูง

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

**ชื่อของเท็มเพลตในการรวมข้อมูล:**

- ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management)

**ชื่อของงานในโครงการการรวมข้อมูล:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
มีการเพิ่มฟิลด์ **โครงการภายนอก** ไปยังเอนทิตีของใบสั่งงาน ฟิลด์นี้คือการค้นหา และซื้อการระบุป้ายใบสั่งงานของคุณกับโครงการที่ใบสั่งขายจะถูกเชื่อมต่อไปยังโครงการภายใน Supply Chain Management เมื่อ **สถานะของระบบ** เปลี่ยนแปลงจากเปิด – อยู่ระหว่างการดำเนินงาน(690,970,000) เป็นสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อค และคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderHeader

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderHeaderProject

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderProduct

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderService

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP4.png)](./media/FSWOP4.png)
