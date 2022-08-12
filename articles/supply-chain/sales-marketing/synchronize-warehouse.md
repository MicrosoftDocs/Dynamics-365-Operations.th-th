---
title: ซิงโครไนส์คลังสินค้าจาก Supply Chain Management ไปยัง Field Service
description: บทความนี้อธิบายเกี่ยวกับเทมเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service
author: Henrikan
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8b86b6a59344299a7a2d277543c3186ed2b8cee4
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103247"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>ซิงโครไนส์คลังสินค้าจาก Supply Chain Management ไปยัง Field Service

[!include[banner](../includes/banner.md)]



บทความนี้อธิบายเกี่ยวกับเทมเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์คลังสินค้าจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>เทมเพลตและงาน
เทมเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการเรียกใช้การซิงโครไนส์คลังสินค้าจาก Supply Chain Management ไปยัง Field Service

**เทมเพลตในการรวมข้อมูล**
- คลังสินค้า (Supply Chain Management ไปยัง Field Service)

**งานในโครงการการรวมข้อมูล**
- คลังสินค้า

## <a name="table-set"></a>ชุดตาราง
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | คลังสินค้า                             |

## <a name="table-flow"></a>โฟลว์ของตาราง
คลังสินค้าที่สร้างขึ้นและรักษาไว้ใน Supply Chain Management สามารถซิงโครไนส์กับ Field Service ได้ ผ่านทางโครงการรวมข้อมูล Microsoft Dataverse อาจมีการควบคุมคลังสินค้าที่คุณต้องการที่ซิงโครไนส์กับ Field Service พร้อมกับแบบสอบถามขั้นสูง และการกรองข้อมูลในโครงการ มีการสร้างคลังสินค้าที่ซิงโครไนส์จาก Supply Chain Management ใน Field Service กับคอลัมน์ **ได้รับการรักษาไว้ภายนอก** ถูกตั้งค่าเป็น **ใช่** และเรกคอร์ดเป็นแบบอ่านอย่างเดียว

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
เพื่อสนับสนุนการรวมระหว่าง Field Service และ Supply Chain Management ต้องมีฟังก์ชันเพิ่มเติมจากโซลูชัน CRM ของ Field Service ในโซลูชัน คอลัมน์ **จะเก็บรักษาภายนอก** ได้ถูกเพิ่มไปยังตาราง **คลังสินค้า (msdyn_warehouses)** คอลัมน์นี้ช่วยระบุว่ามีจัดการคลังสินค้าจาก Supply Chain Management หรือว่ามีอยู่เฉพาะใน Field Service การตั้งค่าสำหรับคอลัมน์นี้รวมถึง:
- **ใช่** – คลังสินค้าสร้างจาก Supply Chain Management และจะไม่สามารถแก้ไขได้ใน Sales
- **ไม่** – มีการป้อนคลังสินค้าโดยตรงใน Field Service และรักษาไว้ที่นี่

คอลัมน์ **รักษาไว้สำหรับภายนอก** ช่วยควบคุมการซิงโครไนส์ของระดับสินค้าคงคลัง การปรับปรุง การโอนย้าย และการใช้บนใบสั่งงาน เฉพาะคลังสินค้าที่มี **รักษาไว้สำหรับภายนอก** ถูกตั้งค่าเป็น **ใช่** สามารถถูกซิงโครไนส์โดยตรงไปยังคลังสินค้าเดียวกันในระบบอื่นๆ ได้ 

> [!NOTE]
> คุณจะสามารถสร้างคลังสินค้าหลายแห่งใน Field Service ได้ (โดยที่ **ถูกรักษาไว้สำหรับภายนอก** = ไม่) แล้วแมปเข้ากับคลังสินค้าเดียว ซึ่งมีแบบสอบถามขั้นสูงและฟังก์ชันการกรองข้อมูล จะมีการใช้ในสถานการณ์ที่คุณต้องการให้ Field service เป็นหลักของระดับสินค้าคงคลังโดยละเอียด และส่งเพียงการปรับปรุงไปยัง Supply Chain Management ในกรณีนี้ Field service จะไม่ได้รับการปรับปรุงระดับสินค้าคงคลังจาก Supply Chain Management สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) และ [ซิงโครไนส์ใบสั่งงานใน Field Service ไปยังใบสั่งขายที่เชื่อมโยงกับโครงการใน Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแมปและข้อกำหนดเบื้องต้น
### <a name="data-integration-project"></a>โครงการการรวมข้อมูล
ก่อนการซิงโครไนส์คลังสินค้า ตรวจสอบว่าได้ปรับปรุงการสอบถามขั้นสูง และการกรองข้อมูลโครงการที่จะรวมเฉพาะคลังสินค้าที่คุณต้องการนำมาจาก Supply Chain Management ไปยัง Field Service หมายเหตุว่า คุณจะต้องการคลังสินค้าที่ใน Field Service เพื่อใช้ในใบสั่งงาน การปรับปรุง และการโอนย้าย  

เพื่อให้แน่ใจว่ามี **คีย์การรวม** อยู่ สำหรับ **msdyn_warehouses**:
1. ไปยังการรวมข้อมูล
2. เลือกแท็บ **การตั้งค่าการเชื่อมต่อ**
3. เลือกชุดของการเชื่อมต่อที่ใช้สำหรับการซิงโครไนส์ใบสั่งผลิต
4. เลือกแท็บ **คีย์การรวม**
5. ค้นหา msdyn_workorders และยืนยันว่าคีย์ **msdyn_name (ชื่อ)** ถูกเพิ่ม ถ้าไม่แสดงขึ้น ให้เพิ่มโดยการคลิก **เพิ่มคีย์** แล้วคลิก **บันทึก** ที่ด้านบนของหน้า

## <a name="template-mapping-in-data-integration"></a>การแมปเทมเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแมปเทมเพลตในการรวมข้อมูล

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>คลังสินค้า (Supply Chain Management ไปยัง Field Service): คลังสินค้า

[![การแมปเทมเพลตในการรวมข้อมูล](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
