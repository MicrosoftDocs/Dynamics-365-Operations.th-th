---
title: ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: 6b56eb545f87c31ef30d6a897f48539068583486
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843444"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service 

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ระดับปริมาณคงคลังคงเหลือจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

**เท็มเพลตในการรวมข้อมูล**
- สินค้าคงคลังของผลิตภัณฑ์ (Fin and Ops ไปยัง Field Service)
  
**งานในโครงการการรวมข้อมูล**
- สินค้าคงคลังของผลิตภัณฑ์

จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของระดับสินค้าคงคลังจะเกิดขึ้นได้:
- คลังสินค้า (Fin and Ops ไปยัง Field Service) 
- ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Fin and Ops ไปยัง Sales) 

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | สินค้าคงคลังคงเหลือ CDS ตามคลังสินค้า     |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
ข้อมูลระดับสินค้าคงคลังจาก Finance and Operation ถูกส่งไปยัง Field Service สำหรับผลิตภัณฑ์ที่เลือก ข้อมูลระดับสินค้าคงคลังรวม: 
- ปริมาณคงคลังคงเหลือ (ปริมาณทางกายภาพที่บันทึกในปัจจุบันที่อยู่ในคลังสินค้า)
- ปริมาณที่อยู่ระหว่างการสั่ง (ปริมาณรวมที่บันทึกไว้ในใบสั่ง เช่น ใบสั่งขาย)
- ปริมาณที่สั่ง (ปริมาณรวมที่สั่งที่บันทึกไว้ เช่น ใบสั่งซื้อ)

ข้อมูลนี้จะถูกรวบรวมสำหรับแต่ละผลิตภัณฑ์ที่นำออกใช้สำหรับคลังสินค้าแต่ละรายการ และซิงโครไนส์ตามการติดตามการเปลี่ยนแปลง เมื่อระดับสินค้าคงคลังมีการเปลี่ยนแปลง

ใน Field Service โซลูชันการรวมสร้างสมุดรายวันสินค้าคงคลังสำหรับผลต่าง เพื่อเรียกระดับใน Field Service เพื่อให้ตรงกับระดับใน Finance and Operations

Finance and Operations จะทำหน้าที่เป็นต้นแบบสำหรับระดับสินค้าคงคลัง ดังนั้น จึงจำเป็นต้องตั้งค่าการรวมสำหรับใบสั่งงาน การโอนย้าย และการปรับปรุงจาก Field Service ไปยัง Finance and Operations ถ้ามีการใช้ฟังก์ชันนี้ใน Field Service ร่วมกับการซิงโครไนส์ของระดับสินค้าคงคลังจาก Finance and Operations

ผลิตภัณฑ์และคลังสินค้าที่ซึ่งระดับสินค้าคงคลังเป็นต้นฉบับจาก Finance and Operations และสามารถควบคุมได้ด้วยการสอบถามและการกรองขั้นสูง (Power Query)

> [!NOTE]
> คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Services ได้ ( **ถูกรักษาไว้ภายนอก = No**) แล้วแมปเข้ากับคลังสินค้าเดียวใน Finance and Operations แบบสอบถามขั้นสูง และการกรองข้อมูลฟังก์ชัน นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
เอนทิตี **สินค้าคงคลังของผลิตภัณฑ์ภายนอก** ถูกใช้สำหรับ backend ในการรวมเท่านั้น เอนทิตีนี้รับค่าระดับสินค้าคงคลังจาก Finance and Operations ในการรวม และจากนั้น แปลงค่าเหล่านั้นเป็นสมุดรายวันสินค้าคงคลัง Manuel ซึ่งจากนั้น เปลี่ยนแปลงผลิตภัณฑ์สินค้าคงคลังในคลังสินค้า

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

### <a name="data-integration"></a>การรวมข้อมูล
สำหรับโครงการที่จะทำงาน คุณต้องตรวจสอบให้แน่ใจว่ามีการอัพเดตคีย์การรวมสำหรับ msdynce_externalproductinventories
1.  ไปที่ **การรวมข้อมูล > ชุดการเชื่อมต่อ**
2.  เลือกชุดการเชื่อมต่อที่ใช้
3.  บนแท็บ **คีย์การรวม** ตรวจสอบให้แน่ใจว่ามีการเพิ่มคีย์ต่อไปนี้ลงใน msdynce_externalproductinventories:
      - msdynce_productnumber (หมายเลขผลิตภัณฑ์)
      - msdynce_warehouseid (รหัสคลังสินค้า)
      
### <a name="data-integration-project"></a>โครงการการรวมข้อมูล
คุณสามารถใช้ตัวกรองข้อมูลกับการสอบถามและการกรองขั้นสูงในการควบคุมว่า เฉพาะผลิตภัณฑ์และคลังสินค้าที่ต้องการที่ส่งข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>สินค้าคงคลังของผลิตภัณฑ์ (Fin and Ops ไปยัง Field Service): สินค้าคงคลังของผลิตภัณฑ์

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
