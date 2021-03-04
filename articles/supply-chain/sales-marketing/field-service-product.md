---
title: การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service ตรงกัน
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d96d1cd91bad4f950868074d9558cb403821d73f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438645"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำซิงโครไนส์ผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365  Field Service

เท็มเพลตที่ใช้กับ **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** มีพื้นฐานบนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง** เท็มเพลตของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)

หัวข้อนี้อธิบายเพียวความแตกต่างระหว่างเท็มเพลต **ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง**

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

**ชื่อของเท็มเพลตในการรวมข้อมูล:**

- ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)

**ชื่อของงานในโครงการการรวมข้อมูล:**

- ผลิตภัณฑ์ - ผลิตภัณฑ์

เท็มเพลต **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** รวมแม็ปที่ไม่ได้ใช้บนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง** การแม็ปนี้ช่วยให้มั่นใจว่า ฟิลด์เฉพาะ Field Service ที่ต้องการ **ชนิดผลิตภัณฑ์บริการ** ถูกตั้งค่าอย่างถูกต้อง

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

มีการใช้การแม็ปค่าต่อไปนี้

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

ใน Supply Chain Management ค่า **ชนิดผลิตภัณฑ์ Field Service** ในเอนทิตีข้อมูล **ผลิตภัณฑ์ที่สามารถนำออกมาขายได้** สามารถคำนวณได้ดังนี้:

- **สินค้าคงคลัง:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = จริง
- **NonInventory:** ชนิดผลิตภัณฑ์ = กลุ่มผลิตภัณฑ์และแบบจำลองสินค้า ผลิตภัณฑ์ที่เก็บในคลัง = เท็จ
- **บริการ:** ชนิดผลิตภัณฑ์ = บริการ

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service): ผลิตภัณฑ์ - ผลิตภัณฑ์

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]