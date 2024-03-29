---
title: ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Supply Chain Management
description: บทความนี้อธิบายเกี่ยวกับเทมเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service
author: Henrikan
ms.date: 04/30/2019
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
ms.openlocfilehash: e59e50a4f54bac749b3d860404a3ecd444d99a89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854107"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>ซิงโครไนส์การโอนและการปรับปรุงสินค้าคงคลังจาก Field Service ไปยัง Supply Chain Management

[!include[banner](../includes/banner.md)]



บทความนี้อธิบายเกี่ยวกับเทมเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ของการปรับปรุงและการโอนย้ายสินค้าคงคลังจาก Dynamics 365 Supply Chain Management เป็น Dynamics 365 Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>เทมเพลตและงาน
เทมเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์การโอนย้ายและการปรับปรุงสินค้าคงคลังโดยตรงจาก Field Service ไปยัง Supply Chain Management

**เทมเพลตในการรวมข้อมูล**
- การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management)
- การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management)

**งานในโครงการการรวมข้อมูล**
- การปรับปรุงสินค้าคงคลัง
- การโอนย้ายสินค้าคงคลัง

## <a name="table-set"></a>ชุดตาราง
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | ส่วนหัวและรายการสมุดรายวันการปรับปรุงสินค้าคงคลัง Dataverse |
| msdyn_inventoryadjustmentproducts | ส่วนหัวและรายการสมุดรายวันการโอนย้ายสินค้าคงคลัง Dataverse   |

## <a name="table-flow"></a>โฟลว์ของตาราง
การปรับปรุงและการโอนย้ายสินค้าคงคลังที่ทำไว้ใน Field Service จะซิงโครไนซ์กับ Supply Chain Management หลังจากที่ **ลงรายการบัญชีสถานะ** ถูกเปลี่ยนจาก **สร้างแล้ว** เป็น **ลงรายการบัญชีแล้ว** หากเป็นเช่นนั้น ใบสั่งโอนย้ายหรือการปรับปรุงจะถูกล็อค และกลายเป็นแบบอ่านอย่างเดียว ซึ่งหมายความว่า การปรับปรุงและการโอนย้ายสามารถลงรายการบัญชีใน Supply Chain Management แต่ไม่สามารถแก้ไขได้ ใน Supply Chain Management คุณสามารถตั้งค่าชุดงานเพื่อลงรายการบัญชีการปรับปรุง และโอนย้ายสมุดรายวันสินค้าคงคลังที่สร้างขึ้นระหว่างการรวมโดยอัตโนมัติ ดูข้อกำหนดเบื้องต้นต่อไปนี้สำหรับรายละเอียดเกี่ยวกับวิธีการเปิดใช้งานชุดงาน

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service 
มีการเพิ่มคอลัมน์ **หน่วยสินค้าคงคลัง** ไปยังตาราง **ผลิตภัณฑ์** คอลัมน์นี้จำเป็นต้องใช้นับตั้งแต่หน่วยการขายและหน่วยสินค้าคงคลังไม่เหมือนกันเสมอใน Supply Chain Management และหน่วยสินค้าคงคลังจำเป็นสำหรับสินค้าคงคลังในคลังสินค้าใน Supply Chain Management
เมื่อคุณตั้งค่าผลิตภัณฑ์ในผลิตภัณฑ์การปรับปรุงสินค้าคงคลังสำหรับทั้งการปรับปรุงสินค้าคงคลังและการโอนย้ายสินค้าคงคลัง หน่วยจะถูกดึงมาจากค่าผลิตภัณฑ์ของสินค้าคงคลัง ถ้าค่าถูกพบ คอลัมน์ **หน่วย** จะถูกล็อคในผลิตภัณฑ์การปรับปรุงสินค้าคงคลัง

มีการเพิ่มคอลัมน์ **ลงรายการบัญชีสถานะ** ไปยังทั้งตาราง **การปรับปรุงสินค้าคงคลัง** และตาราง **การโอนย้ายสินค้าคงคลัง** คอลัมน์นี้จะใช้เป็นตัวกรองสำหรับเวลาที่มีการส่งการปรับปรุงหรือการโอนย้ายไปยัง Supply Chain Management ค่าเริ่มต้นสำหรับคอลัมน์นี้จะถูกสร้างขึ้น (1) แต่จะไม่ได้ถูกส่งไปยัง Supply Chain Management เมื่อคุณปรับปรุงค่าที่จะลงรายการบัญชี (2) ค่านั้นจะถูกส่งไปยัง Supply Chain Management แต่หลังจากนั้นคุณจะไม่สามารถเปลี่ยนแปลงสิ่งใดได้ในการปรับปรุงหรือการโอนย้าย หรือเพิ่มรายการใหม่

มีการเพิ่มคอลัมน์ **ลำดับหมายเลข** ไปยังตาราง **ผลิตภัณฑ์ของการปรับปรุงสินค้าคงคลัง** คอลัมน์นี้ช่วยให้มั่นใจว่าการรวมมีหมายเลขเฉพาะ เพื่อให้การรวมสามารถสร้างและอัปเดตการปรับปรุง เมื่อคุณสร้างผลิตภัณฑ์การปรับปรุงสินค้าคงคลังครั้งแรก จะมีการสร้างเรกคอร์ดใหม่ในตาราง **P2C AutoNumber** เพื่อรักษาชุดหมายเลขและคำนำหน้าที่จะใช้

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแมปและข้อกำหนดเบื้องต้น

### <a name="supply-chain-management"></a>Supply Chain Management
สามารถลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวมที่สร้างขึ้นโดยใช้ชุดงานโดยอัตโนมัติได้ นี่จะถูกเปิดใช้งานจาก **การจัดการสินค้าคงคลัง > งานประจำงวด > การรวม Dataverse > ลงรายการบัญชีสมุดรายวันสินค้าคงคลังการรวม**

## <a name="template-mapping-in-data-integration"></a>การแมปเทมเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงการแมปเทมเพลตในการรวมข้อมูล

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management): การปรับปรุงสินค้าคงคลัง

[![การแมปเทมเพลตในการรวมข้อมูล การปรับปรุงสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management): การปรับปรุงสินค้าคงคลัง](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management): การโอนย้ายสินค้าคงคลัง

[![การแมปเทมเพลตในการรวมข้อมูล การโอนย้ายสินค้าคงคลัง (Field Service ไปยัง Supply Chain Management): การโอนย้ายสินค้าคงคลัง](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]