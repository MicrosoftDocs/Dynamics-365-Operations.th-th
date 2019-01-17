---
title: "ซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

เท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Finance and Operations ไปยัง Sales) – โดยตรง](products-template-mapping-direct.md)

หัวข้อนี้อธิบายเฉพาะความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** และ **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)**

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

**ชื่อของเท็มเพลตในการรวมข้อมูล:**

- ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Sales)

**ชื่อของงานในโครงการการรวมข้อมูล:**

- ผลิตภัณฑ์

เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service)** รวมการแม็ปหนึ่งที่ไม่ได้ถูกรวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)** การแม็ปนี้ช่วยให้มั่นใจว่าหน่วยสินค้าคงคลังที่จำเป็นสำหรับการซิงโครไนส์ระดับสินค้าคงคลังถูกรวมอยู่

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Field Service): ผลิตภัณฑ์

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct1.png)](./media/FSProduct1.png)

