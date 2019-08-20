---
title: ซิงโครไนส์ผลิตภัณฑ์กับหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835705"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์ผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์ที่มีหน่วยสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Field Service)** ที่ใช้ ขึ้นอยู่กับเท็มเพลต **ผลิตภัณฑ์ Field Service (Fin and Ops ไปยัง Field Service)** สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ Field Service (Finance and Operations ไปยัง Field Service)](field-service-product.md)

หัวข้อนี้อธิบายความแตกต่างระหว่างสองเท็มเพลตเท่านั้น: 
- **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Sales)**
- **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** 

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

**ชื่อของเท็มเพลตในการรวมข้อมูล:**

- ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Sales)

**ชื่อของงานในโครงการการรวมข้อมูล:**

- ผลิตภัณฑ์

เท็มเพลต **ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Field Service)** รวมการแม็ปหนึ่งที่ไม่ได้ถูกรวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ Field Service (Fin and Ops ไปยัง Field Service)** การแม็ปนี้ช่วยให้มั่นใจว่าหน่วยสินค้าคงคลังที่จำเป็นสำหรับการซิงโครไนส์ระดับสินค้าคงคลังถูกรวมอยู่

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Field Service): ผลิตภัณฑ์

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct1.png)](./media/FSProduct1.png)
