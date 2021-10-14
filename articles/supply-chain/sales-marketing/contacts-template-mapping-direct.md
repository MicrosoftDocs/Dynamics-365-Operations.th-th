---
title: ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อและรายชื่อลูกค้าใน Supply Chain Management
description: หัวข้อนี้จะอธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Dynamics 365 Sales ไปยัง Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 10/25/2018
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
ms.openlocfilehash: ef51a97c38f446cd267ac8a621ce2a1f66efad18
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579051"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อและรายชื่อลูกค้าใน Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้มีแนวโน้มจะเป็นลูกค้าเงินสด คุณควรคุ้นเคยกับ [รวมข้อมูลลงใน Microsoft Dataverse สำหรับแอป](/powerapps/administrator/data-integrator)

หัวข้อนี้จะอธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ตารางผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) โดยตรงจาก Dynamics 365 Sales ไปยัง Dynamics 365 Supply Chain Management

## <a name="data-flow-in-prospect-to-cash"></a>โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Supply Chain Management และ Sales แม่แบบของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดที่มีให้ใช้งานร่วมกันกับคุณลักษณะการรวมข้อมูล ช่วยให้เกิดกระแสของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Supply Chain Management และ Sales ภาพประกอบต่อไปนี้ แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Supply Chain Management และ Sales

[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงแม่แบบที่พร้อมใช้งาน ให้เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration) เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ตารางผู้ติดต่อ (ผู้ติดต่อ) ใน Sales ไปยังตารางผู้ติดต่อ (ลูกค้า) ใน Supply Chain Management

- **ชื่อของเท็มเพลตในการรวมข้อมูล**

    - ผู้ติดต่อ (Sales to Supply Chain Management) - โดยตรง
    - ผู้ติดต่อไปยังลูกค้า (Sales to Supply Chain Management) - โดยตรง

- **ชื่อของงานในโครงการการรวมข้อมูล**

    - ผู้ติดต่อ
    - ผู้ติดต่อไปยังลูกค้า

ก่อนที่จะซิงโครไนส์ผู้ติดต่อ คุณต้องทำการซิงโครไนส์: บัญชี (Sales ไปยัง Supply Chain Management) ก่อน

## <a name="entity-sets"></a>การตั้งค่าเอนทิตี้

| ใบสั่งขาย    | Supply Chain Management |
|----------|------------------------|
| ผู้ติดต่อ | ผู้ติดต่อ Dataverse           |
| ผู้ติดต่อ | ลูกค้า V2           |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

ผู้ติดต่อจะถูกจัดการใน Sales และถูกซิงโครไนส์ไปยัง Supply Chain Management

ผู้ติดต่อใน Sales สามารถเป็นผู้ติดต่อหรือลูกค้าก็ได้ใน Supply Chain Management เพื่อที่จะระบุว่าผู้ติดต่อใน Sales ที่จะซิงโครไนส์ไปยัง Supply Chain Management ควรจะมีฐานะเป็นผู้ติดต่อหรือลูกค้า ระบบจะพิจารณาจากคุณสมบัติจากผู้ติดต่อใน Sales ดังต่อไปนี้:

- **การซิงโครไนส์ไปยังลูกค้าใน Supply Chain Management:** ผู้ติดต่อที่ซึ่ง **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่**
- **การซิงโครไนส์ไปยังผู้ติดต่อใน Supply Chain Management:** ผู้ติดต่อที่ซึ่ง **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ไม่ใช่** และ **บริษัท** (บัญชี/ผู้ติดต่อหลัก) ชี้ไปยังบัญชี (ไม่ใช่ผู้ติดต่อ)

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

มีการเพิ่มคอลัมน์ **เป็นลูกค้าที่ใช้งานอยู่** ใหม่ ไปยังผู้ติดต่อ คอลัมน์นี้จะถูกใช้เพื่อแยกความแตกต่างของผู้ติดต่อที่มีกิจกรรมการขายและผู้ติดต่อที่ไม่มีกิจกรรมการขาย **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่** สำหรับผู้ติดต่อที่มีใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ที่เกี่ยวข้องเท่านั้น เฉพาะผู้ติดต่อเหล่านั้นที่จะถูกซิงโครไนส์กับ Supply Chain Management ในฐานะลูกค้า

มีการเพิ่มคอลัมน์ **IsCompanyAnAccount** ใหม่ ไปยังผู้ติดต่อ คอลัมน์นี้บ่งชี้ว่าผู้ติดต่อถูกเชื่อมโยงกับบริษัท (บัญชี/ผู้ติดต่อหลัก) ของชนิด **บัญชี** หรือไม่ ข้อมูลนี้จะถูกใช้ในการระบุผู้ติดต่อที่จะซิงโครไนส์กับ Supply Chain Management ในฐานะผู้ติดต่อ

มีการเพิ่มคอลัมน์ **หมายเลขผู้ติดต่อ** ไปยังผู้ติดต่อ เพื่อช่วยรับประกันคีย์ธรรมชาติและคีย์เฉพาะสำหรับการรวม เมื่อมีการสร้างผู้ติดต่อใหม่ ค่า **หมายเลขผู้ติดต่อ** จะถูกสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **CON** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **CON-01000-BVRCPS**

เมื่อมีการใช้งานโซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าคอลัมน์ **หมายเลขผู้ติดต่อ** สำหรับผู้ติดต่อที่มีอยู่ โดยใช้ลำดับหมายเลขที่มีการกล่าวถึงก่อนหน้านี้ นอกจากนี้ สคริปต์การอัพเกรดยังตั้งค่าคอลัมน์ **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่** สำหรับผู้ติดต่อใดๆ ที่มีกิจกรรมการขายอีกด้วย

## <a name="in-supply-chain-management"></a>ใน Supply Chain Management

ผู้ติดต่อจะถูกแท็กโดยใช้คุณสมบัติ **IsContactPersonExternallyMaintained** คุณสมบัตินี้บ่งชี้ว่าผู้ติดต่อที่กำหนดถูกรักษาไว้ภายนอก ในกรณีนี้ ผู้ติดต่อที่ถูกรักษาไว้ภายนอกจะถูกรักษาไว้ใน Sales

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

### <a name="contact-to-customer"></a>ผู้ติดต่อไปยังลูกค้า

- **CustomerGroup** จำเป็นต้องใช้ใน Supply Chain Management เพื่อช่วยในการป้องกันข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ปได้ จากนั้น ค่าเริ่มต้นจะถูกนำมาใช้ ถ้าคอลัมน์ถูกปล่อยว่างไว้ใน Sales

    ค่าเท็มเพลตเริ่มต้นคือ **10**

- โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตที่จำเป็นด้วยตนเองใน Supply Chain Management ได้ คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้

    - **SiteId** – นอกจากนี้คุณยังสามารถกำหนดไซต์เริ่มต้นบนผลิตภัณฑ์ใน Supply Chain Management ได้ด้วย จำเป็นต้องมีไซต์เพื่อสร้างใบสั่งขายและใบเสนอราคาใน Supply Chain Management

        ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **SiteId** ไว้

    - **WarehouseId** – นอกจากนี้คุณยังสามารถกำหนดคลังสินค้าเริ่มต้นบนผลิตภัณฑ์ใน Supply Chain Management ได้ด้วย จำเป็นต้องมีคลังสินค้าเพื่อสร้างใบสั่งขายและใบเสนอราคาใน Supply Chain Management

        ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **WarehouseId** ไว้

    - **LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management
    
        ค่าเท็มเพลตเริ่มต้นสำหรับคือ **en-us**

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล 

> [!NOTE]
> การแม็ปจะช่วยแสดงให้เห็นว่า ข้อมูลคอลัมน์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Supply Chain Management

### <a name="contact-to-contact-example"></a>ตัวอย่างผู้ติดต่อไปยังผู้ติดต่อ

![การแม็ปเท็มเพลตผู้ติดต่อไปยังผู้ติดต่อในตัวรวมข้อมูล](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer-example"></a>ตัวอย่างผู้ติดต่อไปยังลูกค้า

![การแม็ปเท็มเพลตผู้ติดต่อไปยังลูกค้าในตัวรวมข้อมูล](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ผู้ที่มีแนวโน้มจะเป็นลูกค้ากับเงินสด](prospect-to-cash.md)

[ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management](accounts-template-mapping-direct.md)

[ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping-direct.md)

[การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]