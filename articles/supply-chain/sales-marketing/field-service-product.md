---
title: การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service
description: บทความนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service ตรงกัน
author: Henrikan
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860564"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>การซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Field Service

[!include[banner](../includes/banner.md)]

บทความนี้อธิบายเทมเพลตและงานพื้นฐานที่ใช้ในการทำซิงโครไนส์ผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service

เท็มเพลตที่ใช้กับ **ผลิตภัณฑ์ใน Field Service (Supply Chain Management ไปยัง Field Service)** มีพื้นฐานบนเท็มเพลตของ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง** เท็มเพลตของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสด สำหรับข้อมูลเพิ่มเติม ดู [ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)

บทความนี้อธิบายเพียวความแตกต่างระหว่างเทมเพลต **ผลิตภัณฑ์ของ Field Service (Supply Chain Management ไปยัง Field Service)** และ **ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) – โดยตรง**

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