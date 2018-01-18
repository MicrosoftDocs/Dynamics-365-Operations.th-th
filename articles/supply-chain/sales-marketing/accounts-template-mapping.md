---
title: "ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration) 

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Sales (Sales) ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations)

## <a name="template-and-task"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์บัญชีจาก Sales ไปยัง Finance and Operations:

- **ชื่อของเท็มเพลต:**บัญชี (Sales ไปยัง Fin and Ops)
- **ชื่อของงานในโครงการ:** บัญชี - บัญชี - ลูกค้า

ซิงค์งานที่จำเป็นก่อนการซิงค์บัญชี / ลูกค้า: ไม่มี

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| ใบสั่งขาย    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| บัญชี | บัญชี | ลูกค้า              |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

บัญชีจะถูกจัดการใน Sales และจะถูกซิงโครไนส์ไปยัง Finance and Operations โดยเป็นลูกค้า คุณสมบัติ **ถูกรักษาไว้สำหรับภายนอก** ในลูกค้าเหล่านี้ถูกตั้งค่าเป็น **ใช่** เพื่อติดตามลูกค้าที่มีต้นกำเนิดมาจาก Sales ในระหว่างการออกใบแจ้งหนี้ ข้อมูลนี้จะถูกใช้เพื่อกรองข้อมูลใบแจ้งหนี้ที่ถูกซิงค์โครไนซ์ไปยัง Sales

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

ฟิลด์ **หมายเลขบัญชี** จะพร้อมใช้งานบนหน้า **บัญชี** ซึ่งถูกทำให้เป็นคีย์เฉพาะและธรรมชาติเพื่อสนับสนุนการรวม คุณลักษณะคีย์ธรรมชาติของโซลูชันการจัดการความสัมพันธ์กับลูกค้า (CRM) อาจส่งผลกระทบต่อลูกค้าที่ใช้ฟิลด์ **หมายเลขบัญชี** อยู่แล้ว แต่จะไม่ส่งผลกระทบต่อลูกค้าที่ไม่ได้ใช้ค่า **หมายเลขบัญชี** สำหรับแต่ละบัญชี ในปัจจุบัน โซลูชันการรวมไม่สนับสนุนกรณีนี้

เมื่อมีการสร้างบัญชีใหม่ ถ้าค่า **หมายเลขบัญชี** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **ACC** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **ACC-01000-BVRCPS**

เมื่อมีการใช้โซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขบัญชี** สำหรับบัญชีที่มีอยู่ใน Sales ถ้าไม่มีค่า **หมายเลขบัญชี** ลำดับหมายเลขที่ได้อธิบายไว้ก่อนหน้านี้จะถูกนำมาใช้

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

- **CustomerGroupId** ที่แม็ปจาก **CDS &gt; ปลายทาง** จะต้องถูกอัพเดตเป็นค่าที่ถูกต้องใน Finance and Operations คุณสามารถระบุค่าเริ่มต้น หรือคุณสามารถตั้งค่าโดยใช้แผนผังค่า ค่าเท็มเพลตเริ่มต้นคือ **10**
- จำเป็นต้องมี **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ปจาก **CDS &gt; ปลายทาง** จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales

    - เท็มเพลตเริ่มต้นสำหรับ **AddressCountryRegionISOCode** คือ **USA**
    - เท็มเพลตเริ่มต้นสำหรับ **DeliveryAddressCountryRegionISOCode** คือ **USA**

- โดยการเพิ่มการแม็ปต่อไปนี้จาก **CDS&gt; ปลายทาง** คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองที่จำเป็นใน Finance and Operations คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้

    - **SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations สามารถนำไซต์เริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งได้ เท็มเพลตเริ่มต้นสำหรับ **SiteId** คือ **1**
    - **WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations สามารถนำคลังสินค้าเริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งใน Finance and Operations ได้ เท็มเพลตเริ่มต้นสำหรับ **WarehouseId** คือ **13**
    - **LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations โดยค่าเริ่มต้น จะใช้ภาษาจากส่วนหน้าของใบสั่งจากลูกค้า เท็มเพลตเริ่มต้นสำหรับ **LanguageId** คือ **en-us**

- อัพเดตรหัสองค์กรCDS (**Organization_OrganizationId**) ในการแม็ป **ต้นทาง &gt; CDS** ค่าเท็มเพลตเริ่มต้นคือ **ORG001**

## <a name="template-mapping-in-data-integrator"></a>การแม็ปเท็มเพลตในตัวรวมข้อมูล

> [!NOTE]
> ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น เมื่อต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่า การแม็ปค่าเกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่างทั้งสองรายการ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/accounts-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตสำหรับบัญชีในตัวรวมข้อมูล](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping.md)

[ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations](contacts-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations](sales-quotation-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales](sales-invoice-template-mapping.md)




