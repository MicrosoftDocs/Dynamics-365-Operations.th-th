---
title: ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 06d7ff272ecb79abded3c3d3ade1f6bc0ef1f095
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742366"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations กับผลิตภัณฑ์ใน Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service ตรงกัน

เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)

หัวข้อนี้อธิบายความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง**

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

**ชื่อของเท็มเพลตในการรวมข้อมูล:**

- ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)

**ชื่อของงานในโครงการการรวมข้อมูล:**

- ผลิตภัณฑ์ - ผลิตภัณฑ์

เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ประกอบด้วย การแม็ปหนึ่งรายการที่ไม่รวมอยู่ในเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง** การแม็ปนี้ช่วยให้มั่นใจว่า ฟิลด์เฉพาะ Field Service ที่ต้องการ **ชนิดผลิตภัณฑ์บริการ** ถูกตั้งค่าอย่างถูกต้อง

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

มีการใช้การแม็ปค่าต่อไปนี้

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

ใน Finance and Operations ค่า **ชนิดผลิตภัณฑ์ Field Service** ในเอนทิตีข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ซึ่งสามารถขายได้** จะถูกคำนวณดังนี้:

- **สินค้าคงคลัง:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = จริง
- **NonInventory:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = เท็จ
- **บริการ:** ชนิดผลิตภัณฑ์ = บริการ

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service): ผลิตภัณฑ์ - ผลิตภัณฑ์ 

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct.png)](./media/FSProduct.png)
