---
title: "ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์การปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์การปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations

**ชื่อของเท็มเพลตในการรวมข้อมูล:**
- การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Finance and Operations)
- การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Finance and Operations)

**ชื่อของงานในโครงการการรวมข้อมูล:**
- การปรับปรุงสินค้าคงคลัง
- การโอนย้ายสินค้าคงคลัง

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   ส่วนหัวและรายการสมุดรายวันการปรับปรุงสินค้าคงคลัง CDS |
| msdyn_inventoryadjustmentproducts | ส่วนหัวและรายการสมุดรายวันการโอนย้ายสินค้าคงคลัง CDS   |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
การปรับปรุงและการโอนย้ายสินค้าคงคลังที่ทำไว้ใน Field Service จะซิงโครไนซ์กับ Finance and Operations เมื่อ **ลงรายการบัญชีสถานะ** ถูกเปลี่ยนจาก สร้างแล้ว เป็นลงรายการบัญชีแล้ว เมื่อสิ่งนี้เกิดขึ้น ใบสั่งการปรับปรุงหรือการโอนย้ายจะถูกล็อค และกลายเป็นแบบอ่านอย่างเดียว เนื่องจากการปรับปรุงและการโอนย้ายอาจถูกลงรายการบัญชีใน Finance and Operations และดังนั้นจึงไม่สามารถปรับเปลี่ยนได้
ใน Finance and Operations คุณสามารถตั้งค่าชุดงานเพื่อลงรายการบัญชีการปรับปรุง และโอนย้ายสมุดรายวันสินค้าคงคลังที่สร้างขึ้นด้วยการรวมโดยอัตโนมัติ ดูข้อกำหนดเบื้องต้นด้านล่างนี้สำหรับรายละเอียดเกี่ยวกับวิธีการเปิดใช้งานชุดงาน

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service 
มีการเพิ่มฟิลด์หน่วยสินค้าคงคลังไปยังเอนทิตีผลิตภัณฑ์ ฟิลด์นี้จำเป็นต้องใช้นับตั้งแต่หน่วยการขายและหน่วยสินค้าคงคลังไม่เหมือนกันเสมอใน Operations และสำหรับสินค้าคงคลังในคลังสินค้าใน operations เราต้องการหน่วยสินค้าคงคลัง
เมื่อคุณตั้งค่าผลิตภัณฑ์ในผลิตภัณฑ์การปรับปรุงสินค้าคงคลังสำหรับทั้งการปรับปรุงสินค้าคงคลังและการโอนย้ายสินค้าคงคลัง หน่วยจะถูกดึงมาจากค่าผลิตภัณฑ์ของสินค้าคงคลังของผลิตภัณฑ์ ถ้าค่าถูกพบ ฟิลด์หน่วยจะถูกล็อคในผลิตภัณฑ์การปรับปรุงสินค้าคงคลัง

มีการเพิ่มฟิลด์การลงรายการบัญชีสถานะไปยังทั้งเอนทิตีการปรับปรุงสินค้าคงคลังและเอนทิตีการโอนย้ายสินค้าคงคลัง ฟิลด์นี้จะใช้เป็นตัวกรองสำหรับเวลาที่มีการส่งการปรับปรุงหรือการโอนย้ายไปยังการดำเนินงาน ฟิลด์นี้ถูกตั้งค่าเริ่มต้นเป็น สร้างแล้ว (1) และจากนั้น จะไม่ถูกไปยังการดำเนินงาน รายการที่คุณเปลี่ยนคือ ลงรายการบัญชีแล้ว (2) ซึ่งจะถูกส่งไปยังการดำเนินงาน แต่คุณจะไม่สามารถเปลี่ยนแปลงสิ่งใดได้ในการปรับปรุงหรือการโอนย้าย หรือเพิ่มรายการใหม่
มีการเพิ่มฟิลด์ลำดับหมายเลขไปยังเอนทิตีผลิตภัณฑ์ของการปรับปรุงสินค้าคงคลัง ฟิลด์นี้ช่วยให้การรวมมีหมายเลขเฉพาะ ดังนั้นการรวมจะทราบว่าจะทำการสร้าง และจะทำการปรับปรุงเมื่อใด เมื่อคุณสร้างผลิตภัณฑ์การปรับปรุงสินค้าคงคลังครั้งแรก จะมีการสร้างเรกคอร์ดใหม่ในเอนทิตี P2C AutoNumber เพื่อรักษาชุดหมายเลขและคำนำหน้าที่จะใช้

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

### <a name="in-finance-and-operations"></a>ใน Finance and Operations
สามารถลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวมที่สร้างขึ้นโดยการรวมกับชุดงานโดยอัตโนมัติได้ นี่จะถูกเปิดใช้งานจาก: การจัดการสินค้าคงคลัง > งานประจำงวด > การรวม CDS > ลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวม

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Finance and Operations): การปรับปรุงสินค้าคงคลัง

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Finance and Operations): การโอนย้ายสินค้าคงคลัง

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSTrans1.png)](./media/FSTrans1.png)

