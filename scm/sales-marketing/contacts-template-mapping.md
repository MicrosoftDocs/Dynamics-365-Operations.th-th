---
title: "ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: th-th
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) 

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์เอนทิตี้ผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Microsoft Dynamics 365 for Sales (Sales) ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ผู้ติดต่อ (ผู้ติดต่อ) ใน Sales ไปยังผู้ติดต่อ (ลูกค้า) Finance and Operations:

- **ชื่อของเท็มเพลต:**

    - ผู้ติดต่อไปยังผู้ติดต่อ (Sales ไปยัง Fin and Ops)
    - ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops)

- **ชื่อของงานในโครงการ:**

    - ผู้ติดต่อ
    - ผู้ติดต่อไปยังลูกค้า

จำเป็นต้องมีงานการซิงโครไนส์ต่อไปนี้ก่อนการซิงโครไนส์ผู้ติดต่อ: บัญชี (Sales ไปยัง Fin and Ops)

## <a name="entity-sets"></a>การตั้งค่าเอนทิตี้

| ใบสั่งขาย    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| ผู้ติดต่อ | การติดต่อ | ผู้ติดต่อ CDS           |
| ผู้ติดต่อ | บัญชี | ลูกค้า V2           |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการผู้ติดต่อใน Sales และซิงโครไนส์ไปยัง Common Data Service (CDS) และ Finance and Operations

ผู้ติดต่อใน Sales สามารถกลายเป็น ผู้ติดต่อ ใน CDS และ Finance and Operations อีกทางหนึ่งคือ สามารถกลายเป็นบัญชีผู้ใช้ใน CDS และลูกค้าใน Finance and Operations เมื่อต้องการระบุว่าผู้ติดต่อควรจะเบิกสินค้าใน Sales สำหรับการซิงโครไนส์กับ CDS และ Finance and Operations (ตัวอย่างเช่น ผู้ติดต่อใน Sales &gt; ติดต่อใน CDS &gt; ผู้ติดต่อใน Finance and Operations) ระบบจะค้นหาคุณสมบัติต่อไปนี้ในผู้ติดต่อใน Sales:

- **ซิงค์กับบัญชีใน CDS และลูกค้าใน Finance and Operations:** ผู้ติดต่อที่มีการตั้งค่า **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่**
- **ซิงค์กับผู้ติดต่อใน CDS และผู้ติดต่อใน Finance and Operations:** ผู้ติดต่อที่มีการตั้งค่า **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ไม่ใช่** และ **บริษัท** (บัญชี/ผู้ติดต่อหลัก) ที่ชี้ไปยังบัญชี (ที่ไม่ใช่ผู้ติดต่อ)

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales 

มีการเพิ่มฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** ใหม่ไปยังผู้ติดต่อ ฟิลด์นี้จะถูกใช้เพื่อแยกความแตกต่างของผู้ติดต่อที่มีกิจกรรมการขายและผู้ติดต่อที่ไม่มีกิจกรรมการขาย **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่** สำหรับผู้ติดต่อที่มีใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ที่เกี่ยวข้องเท่านั้น เฉพาะผู้ติดต่อเหล่านั้นที่จะถูกซิงโครไนส์กับ Finance and Operations เป็นลูกค้า

มีการเพิ่มฟิลด์ **IsCompanyAnAccount** ใหม่ไปยังผู้ติดต่อ ฟิลด์นี้จะถูกใช้เพื่อบ่งชี้ว่าผู้ติดต่อเชื่อมโยงกับบริษัท (บัญชี/ผู้ติดต่อหลัก) ของชนิด **บัญชี** หรือไม่ ข้อมูลนี้จะถูกใช้ในการระบุผู้ติดต่อที่ควรซิงโครไนส์กับ Finance and Operations เป็นผู้ติดต่อ

มีการเพิ่มฟิลด์ **หมายเลขผู้ติดต่อ** ไปยังผู้ติดต่อเพื่อช่วยรับประกันคีย์ธรรมชาติและคีย์เฉพาะสำหรับการรวม เมื่อมีการสร้างผู้ติดต่อใหม่ ค่า **หมายเลขผู้ติดต่อ** จะถูกสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **CON** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **CON-01000-BVRCPS**

เมื่อมีการเพิ่มโซลูชันการรวมสำหรับ Sales ไปยัง Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขผู้ติดต่อ** สำหรับผู้ติดต่อที่มีอยู่โดยใช้ลำดับหมายเลขที่มีการกล่าวถึงก่อนหน้านี้ สคริปต์การอัพเกรดยังตั้งค่าฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่** สำหรับผู้ติดต่อใด ๆ ที่มีกิจกรรมการขายอีกด้วย

## <a name="in-finance-and-operations"></a>ใน Finance and Operations 

ผู้ติดต่อจะถูกแท็กโดยใช้คุณสมบัติ **IsContactPersonExternallyMaintained** คุณสมบัตินี้บ่งชี้ว่าผู้ติดต่อที่กำหนดถูกรักษาไว้สำหรับภายนอก ในกรณีนี้ ผู้ติดต่อจะถูกรักษาไว้สำหรับภายนอกใน Sales

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

### <a name="contact-to-contact"></a>ผู้ติดต่อไปยังผู้ติดต่อ

- อัพเดต **รหัสองค์กร CDS** ในการแม็ป **ต้นทาง &gt; CDS**

    - ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId [รหัสองค์กร]** คือ **ORG001**
    - ค่าเท็มเพลตเริ่มต้นสำหรับ **PrimaryAccount_Organization_OrganizationId [รหัสองค์กร]** คือ **ORG001**

- จำเป็นต้องมี **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ป **CDS &gt; Operations** จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales เท็มเพลตเริ่มต้นสำหรับ **PrimaryAddressCountryRegionISOCode** คือ **USA**
- ตรวจสอบให้แน่ใจว่าค่าสำหรับฟิลด์ต่อไปนี้มีอยู่ใน Finance and Operations ถ้าไม่จำเป็นต้องใช้ข้อมูลใน Finance and Operations คุณสามารถลบการแม็ปออกจากการแม็ป **CDS &gt; ปลายทาง**

    - **ชื่อฟิลด์ใน Finance and Operations:** การตัดสินใจ
    - **การแม็ป:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>ผู้ติดต่อไปยังลูกค้า

- อัพเดต **รหัสองค์กร CDS** ในการแม็ป **ต้นทาง &gt; CDS** ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId [รหัสองค์กร]** คือ **ORG001**
- จำเป็นต้องมี **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ป **CDS &gt; ปลายทาง** จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales เท็มเพลตเริ่มต้นสำหรับ **PrimaryAddressCountryRegionISOCode** คือ **USA**
- จำเป็นต้องมี **CustomerGroup** ใน Finance and Operations เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ป **CDS &gt; ปลายทาง** จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales เท็มเพลตเริ่มต้นสำหรับ **CustomerGroupId** คือ **10**
- โดยการเพิ่มการแม็ปต่อไปนี้จาก **CDS&gt; ปลายทาง** คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองใน Finance and Operations คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้

    - **SiteId** - นอกจากนี้คุณยังสามารถกำหนดไซต์เริ่มต้นบนผลิตภัณฑ์ใน Finance and Operations จำเป็นต้องมีไซต์เพื่อสร้างใบสั่งขายและใบเสนอราคาใน Finance and Operations ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **SiteId** ไว้
    - **WarehouseId** - นอกจากนี้คุณยังสามารถกำหนดคลังสินค้าเริ่มต้นบนผลิตภัณฑ์ใน Finance and Operations จำเป็นต้องมีคลังสินค้าเพื่อสร้างใบสั่งขายและใบเสนอราคาใน Finance and Operations ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **WarehouseId** ไว้
    - **LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations เท็มเพลตเริ่มต้นสำหรับ **LanguageId** คือ **en-us**

## <a name="template-mapping-in-data-integrator"></a>การแม็ปเท็มเพลตในตัวรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล

### <a name="contact-to-contact"></a>ผู้ติดต่อไปยังผู้ติดต่อ

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตสำหรับผู้ติดต่อในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>ผู้ติดต่อไปยังลูกค้า

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตสำหรับผู้ติดต่อในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping.md)

[ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและบรรทัดของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations](sales-quotation-template-mapping.md)

