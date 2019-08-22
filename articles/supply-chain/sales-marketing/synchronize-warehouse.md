---
title: ซิงโครไนส์คลังสินค้าจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service
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
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835681"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์คลังสินค้าจาก Finance and Operations ไปยัง Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์คลังสินค้าจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

**เท็มเพลตในการรวมข้อมูล**
- คลังสินค้า (Fin and Ops ไปยัง Field Service)

**งานในโครงการการรวมข้อมูล**
- คลังสินค้า

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | คลังสินค้า                             |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
คลังสินค้าที่สร้างขึ้นและรักษาไว้ใน Finance and Operations สามารถซิงโครไนส์กับ Field Service ได้ ผ่านทางโครงการรวมข้อมูล Common Data Service (CDS) อาจมีการควบคุมคลังสินค้าที่คุณต้องการที่ซิงโครไนส์กับ Field Service พร้อมกับแบบสอบถามขั้นสูง และการกรองข้อมูลในโครงการ มีการสร้างคลังสินค้าที่ซิงโครไนส์จาก Finance and Operations ใน Field Service กับฟิลด์ **ได้รับการรักษา** ถูกตั้งค่าเป็น **ใช่** ภายนอก และเรกคอร์ดถูกทำให้เป็นแบบอ่านอย่างเดียว

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
เพื่อสนับสนุนการรวมระหว่าง Field Service และ Finance and Operations ต้องมีฟังก์ชันเพิ่มเติมจากโซลูชัน CRM ของ Field Service ในโซลูชัน ฟิลด์ **จะเก็บรักษาภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **คลังสินค้า (msdyn_warehouses)** ฟิลด์นี้ช่วยระบุว่ามีจัดการคลังสินค้าจาก Finance and Operations หรือมีเฉพาะใน Field Service การตั้งค่าสำหรับฟิลด์นี้รวมถึง:
- **ใช่** – คลังสินค้าที่สร้างจาก Finance and Operations และจะไม่สามารถแก้ไขได้ใน Sales
- **ไม่** – มีการป้อนคลังสินค้าโดยตรงใน Field Service และรักษาไว้ที่นี่

ฟิลด์ **รักษาไว้สำหรับภายนอก** ช่วยควบคุมการซิงโครไนส์ของระดับสินค้าคงคลัง การปรับปรุง การโอนย้าย และการใช้บนใบสั่งงาน เฉพาะคลังสินค้าที่มี **รักษาไว้สำหรับภายนอก** ถูกตั้งค่าเป็น **ใช่** สามารถถูกซิงโครไนส์โดยตรงไปยังคลังสินค้าเดียวกันในระบบอื่นๆ ได้ 

> [!NOTE]
> คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Service ได้ ( **รักษาไว้สำหรับภายนอก = No**) แล้วแมปเข้ากับคลังสินค้าเดียวใน Finance and Operations แบบสอบถามขั้นสูง และการกรองข้อมูลฟังก์ชัน นี่จะถูกใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งการปรับปรุงไปยัง Finance and Operations ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Finance and Operations สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น
### <a name="data-integration-project"></a>โครงการการรวมข้อมูล
ก่อนการซิงโครไนส์ของคลังสินค้า ตรวจสอบว่าได้ปรับปรุงการสอบถามขั้นสูง และการกรองข้อมูลโครงการที่จะรวมคลังสินค้าที่คุณต้องการนำมาจาก Finance and Operations ไปยัง Field Service หมายเหตุว่า คุณจะต้องการคลังสินค้าที่ใน Field Service เพื่อใช้ในใบสั่งงาน การปรับปรุง และการโอนย้าย  

เพื่อให้แน่ใจว่ามี **คีย์การรวม** อยู่ สำหรับ **msdyn_warehouses**:
1. ไปยังการรวมข้อมูล
2. เลือกแท็บ **การตั้งค่าการเชื่อมต่อ**
3. เลือกชุดของการเชื่อมต่อที่ใช้สำหรับการซิงโครไนส์ใบสั่งผลิต
4. เลือกแท็บ **คีย์การรวม**
5. ค้นหา msdyn_workorders และยืนยันว่าคีย์ **msdyn_name (ชื่อ)** ถูกเพิ่ม ถ้าไม่แสดงขึ้น ให้เพิ่มโดยการคลิก **เพิ่มคีย์** แล้วคลิก **บันทึก** ที่ด้านบนของหน้า

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>คลังสินค้า (Fin and Ops ไปยัง Field Service): คลังสินค้า

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/Warehouse1.png)](./media/Warehouse1.png)
