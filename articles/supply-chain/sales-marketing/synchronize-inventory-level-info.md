---
title: "ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service 

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ข้อมูลระดับสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของระดับปริมาณคงคลังคงเหลือจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

**ชื่อของเท็มเพลตในการรวมข้อมูล:**
- สินค้าคงคลังของผลิตภัณฑ์ (Finance and Operations ไปยัง Field Service)
  
**ชื่อของงานในโครงการการรวมข้อมูล:**
- สินค้าคงคลังของผลิตภัณฑ์

จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของระดับสินค้าคงคลังจะเกิดขึ้นได้:
- คลังสินค้า (Finance and Operations ไปยัง Field Service) 
- ผลิตภัณฑ์ Field Service ที่มีหน่วยสินค้าคงคลัง (Finance and Operations ไปยัง Sales) 

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | สินค้าคงคลังคงเหลือ CDS ตามคลังสินค้า     |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
ข้อมูลระดับสินค้าคงคลังจาก Finance and Operation ถูกส่งไปยัง Field Service สำหรับผลิตภัณฑ์ที่เลือก ข้อมูลระดับสินค้าคงคลังรวม: 
- ปริมาณคงคลังคงเหลือ (ปริมาณทางกายภาพที่บันทึกในปัจจุบันที่อยู่ในคลังสินค้า)
- ปริมาณที่อยู่ระหว่างการสั่ง (ปริมาณรวมที่บันทึกไว้ในใบสั่ง - เช่น ใบสั่งขาย)
- ปริมาณที่สั่ง (ปริมาณรวมที่สั่งที่บันทึกไว้ - เช่น ใบสั่งซื้อ)

ข้อมูลนี้จะถูกรวบรวมสำหรับแต่ละผลิตภัณฑ์ที่นำออกใช้สำหรับคลังสินค้าแต่ละรายการ และซิงโครไนส์ตามการติดตามการเปลี่ยนแปลง เมื่อระดับสินค้าคงคลังมีการเปลี่ยนแปลง

ใน Field Service โซลูชันการรวมสร้างสมุดรายวันสินค้าคงคลังสำหรับผลต่าง เพื่อเรียกระดับใน Field Service เพื่อให้ตรงกับระดับใน Finance and Operations

Finance and Operations จะทำหน้าที่เป็นต้นแบบสำหรับระดับสินค้าคงคลัง ดังนั้น จึงจำเป็นต้องตั้งค่าการรวมสำหรับใบสั่งงาน การโอนย้าย และการปรับปรุงจาก Field Service ไปยัง Finance and Operations ถ้ามีการใช้ฟังก์ชันนี้ใน Field Service ร่วมกับการซิงโครไนส์ของระดับสินค้าคงคลังจาก Finance and Operations

ผลิตภัณฑ์และคลังสินค้าที่ซึ่งระดับสินค้าคงคลังเป็นต้นฉบับจาก Finance and Operations และสามารถควบคุมได้ด้วยการสอบถามและการกรองขั้นสูง (Power Query)

หมายเหตุ: คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Services ได้ (ด้วย ถูกรักษาไว้ภายนอก = ไม่) แล้วจากนั้นแม็ปเข้ากับคลังสินค้าเดียวใน Finance and Operations ด้วยแบบสอบถามขั้นสูงและการกรองข้อมูลฟังก์ชัน นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations ดูข้อมูลเพิ่มเติมในการซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations และซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
เอนทิตีสินค้าคงคลังของผลิตภัณฑ์ภายนอกเป็นเอนทิตีใหม่ที่จะใช้สำหรับ backend ในการรวมเท่านั้น ซึ่งรับค่าระดับสินค้าคงคลังจาก Finance and Operations ในการรวม และจากนั้น แปลงค่าเหล่านั้นเป็นสมุดรายวันสินค้าคงคลัง Manuel ซึ่งจากนั้น เปลี่ยนแปลงผลิตภัณฑ์สินค้าคงคลังในคลังสินค้า 

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

### <a name="in-the-data-integration-project"></a>ในโครงการการรวมข้อมูล
ใช้ตัวกรองข้อมูลกับการสอบถามและการกรองขั้นสูงในการควบคุมว่า เฉพาะผลิตภัณฑ์และคลังสินค้าที่ต้องการที่ส่งข้อมูลระดับสินค้าคงคลังจาก Finance and Operations ไปยัง Field Service

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>สินค้าคงคลังของผลิตภัณฑ์ (Finance and Operations ไปยัง Field Service): สินค้าคงคลังของผลิตภัณฑ์

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

