---
title: "ซิงโครไนส์ใบสั่งงานจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ใบสั่งงานที่มีหมายเลขโครงการจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>ซิงโครไนส์ใบสั่งงานที่มีโครงการจาก Field Service ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ใบสั่งงานที่มีหมายเลขโครงการจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

เท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)

หัวข้อนี้อธิบายเฉพาะความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** และ **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**

ผลต่างหลักคือ เท็มเพลตนี้รวมการแม็ปหมายเลขโครงการที่กำหนดให้กับใบสั่งผลิตใน Field Service เพื่อการรับประกันว่า ใบสั่งขายที่สร้างขึ้นใน Finance and Operations จะรวมหมายเลขโครงการ และการออกใบแจ้งหนี้สามารถเกิดขึ้นได้ในโครงการที่เกี่ยวข้อง นอกจากนี้ เท็มเพลตที่ใช้การกรองและการสอบถามขั้นสูง

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

**ชื่อของเท็มเพลตในการรวมข้อมูล:**

- ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Finance and Operations)

**ชื่อของงานในโครงการการรวมข้อมูล:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
มีการเพิ่มฟิลด์ **โครงการภายนอก** ไปยังเอนทิตีของใบสั่งงาน ฟิลด์นี้เป็นการค้นหา และซื้อการระบุป้ายใบสั่งงานของคุณกับโครงการที่มีโครงการที่ใบสั่งขายจะถูกเชื่อมต่อกับโครงการภายใน Finance and Operations เมื่อ **สถานะของระบบ** เปลี่ยนแปลงจากเปิด – อยู่ระหว่างการดำเนินงาน(690,970,000) เป็นสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อค และคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Finance and Operations): WorkOrderHeader

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Finance and Operations): WorkOrderHeaderProject

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Finance and Operations): WorkOrderProduct

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Finance and Operations): WorkOrderService

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP4.png)](./media/FSWOP4.png)

