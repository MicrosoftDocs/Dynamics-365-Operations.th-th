---
title: ซิงโครไนส์ใบสั่งงานที่มีโครงการจาก Field Service ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "329861"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>ซิงโครไนส์ใบสั่งงานที่มีโครงการจาก Field Service ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

เท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)

หัวข้อนี้อธิบายเฉพาะความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** และ **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**

ความแตกต่างหลักที่ว่า เท็มเพลตนี้รวมการแม็ปของหมายเลขโครงการที่มอบหมายไปยังใบสั่งงานใน Field Service ซึ่งทำให้มั่นใจว่าใบสั่งขายที่สร้างใน Finance and Operations รวมหมายเลขโครงการและการออกใบแจ้งหนี้สามารถเกิดขึ้นได้ในโครงการที่เกี่ยวข้อง นอกจากนี้ เท็มเพลตที่ใช้การกรองและการสอบถามขั้นสูง

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
