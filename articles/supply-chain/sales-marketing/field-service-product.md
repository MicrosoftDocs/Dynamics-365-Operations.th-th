---
title: "ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: th-th
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>ซิงโครไนส์ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

เท็มเพลต **ผลิตภัณฑ์ Field Service (Fin และ Ops ไปยัง Field Service)** ที่ใช้ เป็นไปตามเท็มเพลต **ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง** จากผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Fin และ Ops ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)

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

