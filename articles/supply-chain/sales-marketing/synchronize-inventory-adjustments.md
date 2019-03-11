---
title: ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: aa54945cea5821da163e1f6ea1747ac29b31a3ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "308379"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเกี่ยวกับเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Finance and Operations เป็น Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations

**เท็มเพลตในการรวมข้อมูล**
- การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Finance and Operations)
- การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Finance and Operations)

**งานในโครงการการรวมข้อมูล**
- การปรับปรุงสินค้าคงคลัง
- การโอนย้ายสินค้าคงคลัง

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   ส่วนหัวและรายการสมุดรายวันการปรับปรุงสินค้าคงคลัง CDS |
| msdyn_inventoryadjustmentproducts | ส่วนหัวและรายการสมุดรายวันการโอนย้ายสินค้าคงคลัง CDS   |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
การปรับปรุงและการโอนย้ายสินค้าคงคลังที่ทำไว้ใน Field Service จะซิงโครไนซ์กับ Finance and Operations หลังจากที่  **ลงรายการบัญชีสถานะ** ถูกเปลี่ยนจาก **สร้างแล้ว** เป็น **ลงรายการบัญชีแล้ว** หากเป็นเช่นนั้น ใบสั่งโอนย้ายหรือการปรับปรุงจะถูกล็อค และกลายเป็นแบบอ่านอย่างเดียว ซึ่งหมายความว่า การปรับปรุงและการโอนย้ายสามารถลงรายการบัญชีใน Finance and Operations แต่ไม่สามารถแก้ไขได้ ใน Finance and Operations คุณสามารถตั้งค่าชุดงานเพื่อลงรายการบัญชีการปรับปรุง และโอนย้ายสมุดรายวันสินค้าคงคลังที่สร้างขึ้นระหว่างการรวมโดยอัตโนมัติ ดูข้อกำหนดเบื้องต้นต่อไปนี้สำหรับรายละเอียดเกี่ยวกับวิธีการเปิดใช้งานชุดงาน

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service 
มีการเพิ่มฟิลด์ **หน่วยสินค้าคงคลัง** ไปยังเอนทิตี **ผลิตภัณฑ์** ฟิลด์นี้จำเป็นต้องใช้นับตั้งแต่หน่วยการขายและหน่วยสินค้าคงคลังไม่เหมือนกันเสมอใน Finance and Operations และหน่วยสินค้าคงคลังจำเป็นสำหรับสินค้าคงคลังในคลังสินค้าใน Finance and Operations
เมื่อคุณตั้งค่าผลิตภัณฑ์ในผลิตภัณฑ์การปรับปรุงสินค้าคงคลังสำหรับทั้งการปรับปรุงสินค้าคงคลังและการโอนย้ายสินค้าคงคลัง หน่วยจะถูกดึงมาจากค่าผลิตภัณฑ์ของสินค้าคงคลัง ถ้าค่าถูกพบ ฟิลด์ **หน่วย** จะถูกล็อคในผลิตภัณฑ์การปรับปรุงสินค้าคงคลัง

มีการเพิ่มฟิลด์ **ลงรายการบัญชีสถานะ** ไปยังทั้งเอนทิตี **การปรับปรุงสินค้าคงคลัง** และเอนทิตี **การโอนย้ายสินค้าคงคลัง** ฟิลด์นี้จะใช้เป็นตัวกรองสำหรับเวลาที่มีการส่งการปรับปรุงหรือการโอนย้ายไปยัง Finance and Operations ค่าเริ่มต้นสำหรับฟิลด์นี้จะถูกสร้างขึ้น (1) แต่จะไม่ได้ถูกส่งไปยัง Finance and Operations เมื่อคุณปรับปรุงค่าที่จะลงรายการบัญชี (2) ค่านั้นจะถูกส่งไปยัง Finance and Operations แต่หลังจากนั้นคุณจะไม่สามารถเปลี่ยนแปลงสิ่งใดได้ในการปรับปรุงหรือการโอนย้าย หรือเพิ่มรายการใหม่

มีการเพิ่มฟิลด์ **ลำดับหมายเลข** ไปยังเอนทิตี **ผลิตภัณฑ์ของการปรับปรุงสินค้าคงคลัง** ฟิลด์นี้ช่วยให้มั่นใจว่าการรวมมีหมายเลขเฉพาะ เพื่อให้การรวมสามารถสร้างและอัพเดตการปรับปรุง เมื่อคุณสร้างผลิตภัณฑ์การปรับปรุงสินค้าคงคลังครั้งแรก จะมีการสร้างเรกคอร์ดใหม่ในเอนทิตี **P2C AutoNumber** เพื่อรักษาชุดหมายเลขและคำนำหน้าที่จะใช้

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

### <a name="finance-and-operations"></a>Finance and Operations
สามารถลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวมที่สร้างขึ้นโดยใช้ชุดงานโดยอัตโนมัติได้ นี่จะถูกเปิดใช้งานจาก **การจัดการสินค้าคงคลัง > งานประจำงวด > การรวม CDS > ลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวม**

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Finance and Operations): การปรับปรุงสินค้าคงคลัง

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Finance and Operations): การโอนย้ายสินค้าคงคลัง

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSTrans1.png)](./media/FSTrans1.png)
