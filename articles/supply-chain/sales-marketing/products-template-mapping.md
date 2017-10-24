---
title: "ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ในการขาย"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ไปยัง Microsoft Dynamics 365 for Sales"
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ในการขาย

[!include[banner](../includes/banner.md)]

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration) 

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ไปยัง Microsoft Dynamics 365 for Sales

## <a name="template-and-task"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้จะใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) ไปยัง Microsoft Dynamics 365 for Sales (Sales)

-   ชื่อของเท็มเพลต: ผลิตภัณฑ์ (Fin and Ops ไปยังการขาย)

-   ชื่อของงานในโครงการ: ผลิตภัณฑ์

ซิงค์งานที่จำเป็นก่อนการซิงค์ผลิตภัณฑ์: ไม่มี

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| **Finance and Operations** | **CDS** | **ใบสั่งขาย**  |
|----------------------------|---------|------------|
| ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้ | ผลิตภัณฑ์ | ผลิตภัณฑ์   |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

ผลิตภัณฑ์จะถูกจัดการใน Finance and Operations และจะถูกซิงโครไนส์ไปยังการขาย เอนทิตี้ข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้** ใน Finance and Operations จะส่งออกผลิตภัณฑ์ที่ขายได้เท่านั้น ซึ่งหมายความว่า ผลิตภัณฑ์มีข้อมูลที่จำเป็นที่จะใช้ในใบสั่งขาย กฎเดียวกันนี้จะใช้เมื่อผลิตภัณฑ์ได้รับการตรวจสอบด้วยฟังก์ชัน **ตรวจสอบ** ในหน้า **ผลิตภัณฑ์ที่นำออกใช้**

**หมายเลขผลิตภัณฑ์** จะถูกใช้เป็นคีย์ ซึ่งหมายความว่า ผลิตภัณฑ์ย่อยจะซิงโครไนส์กับ CDS และการขายที่มี **รหัสผลิตภัณฑ์** เฉพาะ ต่อ **ผลิตภัณฑ์ย่อย**

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

ฟิลด์ใหม่ในผลิตภัณฑ์ **รักษาไว้สำหรับภายนอก** จะได้รับการเพิ่มในการขายเพื่อบ่งชี้ว่า ผลิตภัณฑ์ดังกล่าวถูกรักษาไว้จากภายนอก โดยค่าเริ่มต้นจะถูกตั้งเป็น **ใช่** ระหว่างการนำเข้าไปยังการขาย

-   **รักษาไว้สำหรับภายนอก = ใช่**: ผลิตภัณฑ์เกิดจาก Finance and Operations และไม่สามารถแก้ไขได้ในการขาย

-   **รักษาไว้สำหรับภายนอก = ไม่**: ผลิตภัณฑ์ถูกป้อนโดยตรงในการขาย

-   **รักษาไว้สำหรับภายนอก = ว่างเปล่า**: ผลิตภัณฑ์มีอยู่ในการขายก่อนที่จะเปิดใช้งานผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

ข้อมูล **รักษาไว้สำหรับภายนอก** จะใช้เพื่อให้มั่นใจว่ามีเฉพาะ **ใบเสนอราคา** และ **ใบสั่งขาย** ที่มี **ผลิตภัณฑ์รักษาไว้สำหรับภายนอก** เท่านั้นที่จะซิงค์กับ Finance and Operations

ระบบจะเพิ่ม **ผลิตภัณฑ์รักษาไว้สำหรับภายนอก** โดยอัตโนมัติใน **รายการราคา** แรกที่ถูกต้องที่มีสกุลเงินเดียวกัน โปรดทราบว่า รายการจะเรียงลำดับตามตัวอักษรของ **ชื่อ** ระบบจะใช้ราคาขายของผลิตภัณฑ์จาก Finance and Operations เป็นราคาใน **รายการราคา** ซึ่งหมายความว่าจำเป็นต้องมี **รายการราคา** ในการขายสำหรับแต่ละ **สกุลเงินการขายผลิตภัณฑ์** ใน Finance and Operations สกุลเงินของผลิตภัณฑ์ที่สามารถขายได้ที่นำออกใช้ จะถูกตั้งค่าเป็นสกุลเงินทางบัญชีในนิติบุคคล ที่ผลิตภัณฑ์ถูกส่งออก

> [!NOTE]
> การซิงค์ผลิตภัณฑ์จะไม่สำเร็จหากไม่มี **รายการราคา** ที่มีสกุลเงินที่ตรงกัน

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

-   ก่อนที่คุณจะรันการซิงค์แรก คุณต้องเติมข้อมูลใน **ตารางผลิตภัณฑ์เฉพาะ** สำหรับผลิตภัณฑ์ที่มีอยู่ใน Finance and Operations จะไม่มีการซิงค์ผลิตภัณฑ์ที่มีอยู่จนกว่างานนี้เสร็จสมบูรณ์

    -   ใน Finance and Operations ให้ใช้ค้นหาเพื่อค้นหา **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ**

    -   คลิก **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ** เพื่อรันงาน งานนี้จำเป็นต้องรันเพียงครั้งเดียวเท่านั้น

-   ตรวจสอบให้แน่ใจว่ามี **ValueMap** ที่จำเป็นสำหรับการขาย **หน่วยวัด** (UOM) ใน Finance and Operations อยู่ใน **ต้นทาง -\> CDS ในการแม็ป SalesUnitSymbol / DefaultSellingUnitOfMeasure**

-   อัพเดต **รหัสองค์กร CDS Organization_OrganizationId** ใน **ต้นทาง -\> CDS**

    -   ค่าเท็มเพลตเริ่มต้นจะถูกกำหนดเป็น ORG001

-   อัพเดต **ValueMap** สำหรับ **กลุ่มหน่วย** (**defaultuomscheduleid.name**) ใน **CDS -\> ปลายทาง** ให้ตรงกับ **กลุ่มหน่วย** ในการขาย

    -   ค่าเท็มเพลตเริ่มต้นคือ **หน่วยเริ่มต้น**

-   ตรวจสอบให้แน่ใจว่า มี UOM ผลิตภัณฑ์ที่ขายทั้งหมดจาก Finance and Operations ในการขายที่มีค่า **รายการเบิกสินค้า CDS**

-   ตรวจสอบให้แน่ใจว่ามี **รายการราคา** ในการขายสำหรับแต่ละสกุลเงินขายผลิตภัณฑ์ใน Finance and Operations

-   สามารถสร้างผลิตภัณฑ์ขึ้นในการขายโดยมีสถานะ **ร่าง** หรือ **ใช้งาน** ซึ่งจะถูกควบคุมใน **การตั้งค่าระบบ** ภายใต้ **การขาย** ในการขาย

    -   จำเป็นต้องเรียกใช้ผลิตภัณฑ์ที่สร้างขึ้นด้วยสถานะร่าง ก่อนที่จะสามารถเพิ่มผลิตภัณฑ์นี้ใน **ใบเสนอราคา** หรือ **ใบสั่งขาย**

## <a name="template-mapping-in-data-integrator"></a>การแม็ปเท็มเพลตในตัวรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/products-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตสำหรับผลิตภัณฑ์ในตัวรวมข้อมูล](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping.md)

[ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อใน Finance and Operations](contacts-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations](sales-quotation-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales](sales-invoice-template-mapping.md)


