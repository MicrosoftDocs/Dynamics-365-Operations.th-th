---
title: "ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้ คุณควรทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration)

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) โดยตรงจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition

## <a name="data-flow-in-prospect-to-cash"></a>โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales

[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration) เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) ใน Sales ไปยังเอนทิตีผู้ติดต่อ (ลูกค้า) ใน Finance and Operations:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:**

    - ผู้ติดต่อ (Sales ไปยัง Fin and Ops) - ตรง
    - ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) - ตรง

- **ชื่อของงานในโครงการการรวมข้อมูล:**

    - ผู้ติดต่อ
    - ผู้ติดต่อไปยังลูกค้า

จำเป็นต้องมีงานการซิงโครไนส์ต่อไปนี้ก่อนที่จะเกิดการซิงโครไนส์ผู้ติดต่อได้: บัญชี (Sales ไปยัง Fin and Ops)

## <a name="entity-sets"></a>การตั้งค่าเอนทิตี้

| ใบสั่งขาย    | Finance and Operations |
|----------|------------------------|
| ผู้ติดต่อ | ผู้ติดต่อ CDS           |
| ผู้ติดต่อ | ลูกค้า V2           |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

ผู้ติดต่อจะถูกจัดการใน Sales และจะถูกซิงโครไนส์ไปยัง Finance and Operations

ผู้ติดต่อใน Sales สามารถกลายเป็นผู้ติดต่อหรือลูกค้าได้ใน Finance and Operations เพื่อระบุว่าผู้ติดต่อใน Sales ควรถูกซิงโครไนส์กับ Finance and Operations ในฐานะผู้ติดต่อหรือลูกค้าหรือไม่ ระบบจะดูที่คุณสมบัติต่อไปนี้ขในผู้ติดต่อใน Sales:

- **การซิงโครไนส์ไปยังลูกค้าใน Finance and Operations:** ผู้ติดต่อที่ซึ่ง **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่**
- **การซิงโครไนส์ไปยังผู้ติดต่อใน Finance and Operations:** ผู้ติดต่อที่ซึ่ง **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ไม่ใช่** และ **บริษัท** (บัญชี/ผู้ติดต่อหลัก) ชี้ไปยังบัญชี (ไม่ใช่ผู้ติดต่อ)

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

มีการเพิ่มฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** ใหม่ ไปยังผู้ติดต่อ ฟิลด์นี้จะถูกใช้เพื่อแยกความแตกต่างของผู้ติดต่อที่มีกิจกรรมการขายและผู้ติดต่อที่ไม่มีกิจกรรมการขาย **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่** สำหรับผู้ติดต่อที่มีใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ที่เกี่ยวข้องเท่านั้น เฉพาะผู้ติดต่อเหล่านั้นที่จะถูกซิงโครไนส์กับ Finance and Operations ในฐานะลูกค้า

มีการเพิ่มฟิลด์ **IsCompanyAnAccount** ใหม่ ไปยังผู้ติดต่อ ฟิลด์นี้บ่งชี้ว่าผู้ติดต่อถูกเชื่อมโยงกับบริษัท (บัญชี/ผู้ติดต่อหลัก) ของชนิด **บัญชี** หรือไม่ ข้อมูลนี้จะถูกใช้ในการระบุผู้ติดต่อที่ควรซิงโครไนส์กับ Finance and Operations ในฐานะผู้ติดต่อ

มีการเพิ่มฟิลด์ **หมายเลขผู้ติดต่อ** ไปยังผู้ติดต่อ เพื่อช่วยรับประกันคีย์ธรรมชาติและคีย์เฉพาะสำหรับการรวม เมื่อมีการสร้างผู้ติดต่อใหม่ ค่า **หมายเลขผู้ติดต่อ** จะถูกสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **CON** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **CON-01000-BVRCPS**

เมื่อมีการใช้งานโซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขผู้ติดต่อ** สำหรับผู้ติดต่อที่มีอยู่โดยใช้ลำดับหมายเลขที่มีการกล่าวถึงก่อนหน้านี้ สคริปต์การอัพเกรดยังตั้งค่าฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่** สำหรับผู้ติดต่อใด ๆ ที่มีกิจกรรมการขายอีกด้วย

## <a name="in-finance-and-operations"></a>ใน Finance and Operations

ผู้ติดต่อจะถูกแท็กโดยใช้คุณสมบัติ **IsContactPersonExternallyMaintained** คุณสมบัตินี้บ่งชี้ว่าผู้ติดต่อที่กำหนดถูกรักษาไว้ภายนอก ในกรณีนี้ ผู้ติดต่อที่ถูกรักษาไว้ภายนอกจะถูกรักษาไว้ใน Sales

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

### <a name="contact-to-customer"></a>ผู้ติดต่อไปยังลูกค้า

- จำเป็นต้องมี **CustomerGroup** ใน Finance and Operations เพื่อช่วยในการป้องกันข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ปได้ จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales

    ค่าเท็มเพลตเริ่มต้นคือ **10**

- โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองที่จำเป็นใน Finance and Operations ได้ คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้

    - **SiteId** – นอกจากนี้คุณยังสามารถกำหนดไซต์เริ่มต้นบนผลิตภัณฑ์ใน Finance and Operations ได้ด้วย จำเป็นต้องมีไซต์เพื่อสร้างใบสั่งขายและใบเสนอราคาใน Finance and Operations

        ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **SiteId** ไว้

    - **WarehouseId** – นอกจากนี้คุณยังสามารถกำหนดคลังสินค้าเริ่มต้นบนผลิตภัณฑ์ใน Finance and Operations ได้ด้วย จำเป็นต้องมีคลังสินค้าเพื่อสร้างใบสั่งขายและใบเสนอราคาใน Finance and Operations

        ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **WarehouseId** ไว้

    - **LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations
    
        ค่าเท็มเพลตเริ่มต้นสำหรับคือ **en-us**

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล 

> [!NOTE]
> การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations

### <a name="contact-to-contact"></a>ผู้ติดต่อไปยังผู้ติดต่อ

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>ผู้ติดต่อไปยังลูกค้า

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](prospect-to-cash.md)

[ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping-direct.md)

[ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping-direct.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping-direct.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-invoice-template-mapping-direct.md)



