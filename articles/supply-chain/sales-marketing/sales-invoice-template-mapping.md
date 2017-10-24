---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales 

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Finance and Operations ไปยัง Sales

- **ชื่อของเท็มเพลตในการรวมข้อมูล** 

     - ใบแจ้งหนี้การขาย (Fin and Ops ไปยัง Sales)

- **ชื่อของงานในโครงการการรวมข้อมูล**

    - SalesInvoiceHeader
    - SalesInvoiceLine

ซิงค์งานที่จำเป็นก่อนการซิงค์ส่วนหัวและรายการของใบแจ้งหนี้การขาย:
-   ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales)
-   บัญชี (Sales ไปยัง Fin and Ops) (ถ้าใช้)
-   ผู้ติดต่อ (Sales ไปยัง Fin and Ops) (ถ้าใช้)
-   ส่วนหัวและรายการของใบสั่งขาย (Fin and Ops ไปยัง Sales)

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Finance and Operations                               | Common Data Service (CDS)              | ใบสั่งขาย          |
|------------------------------------------------------|------------------|----------------|
| ส่วนหัวใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก | SalesInvoice     | ใบแจ้งหนี้       |
| รายการในใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

ใบแจ้งหนี้การขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales

> [!NOTE]
> ในขณะนี้ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบน **ส่วนหัวของใบแจ้งหนี้การขาย** ไม่ได้รวมอยู่ในการซิงค์จาก Finance and Operations ไปยัง Sales ทั้งนี้เนื่องจาก Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว มีการรวมภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการ

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

-  **ฟิลด์หมายเลขใบแจ้งหนี้** ถูกเพิ่มไปยังเอนทิตี้ **ใบแจ้งหนี้** และแสดงขึ้นบนหน้า
 
-  ปุ่ม **สร้างใบแจ้งหนี้** บนหน้า **ใบสั่งขาย** ถูกซ่อนอยู่เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และถูกซิงค์ไปยัง Sales หน้า **ใบแจ้งหนี้** จะไม่สามารถแก้ไขได้เนื่องจากใบแจ้งหนี้จะถูกซิงค์จาก Finance and Operations
 
-  **สถานะของใบสั่งขาย** จะเปลี่ยนเป็น **ใบแจ้งหนี้** โดยอัตโนมัติเมื่อมีการซิงค์ใบแจ้งหนี้ที่เกี่ยวข้องจาก Finance and Operations ไปยัง Sales นอกจากนี้ เจ้าของใบสั่งขายที่มีการสร้างใบแจ้งหนี้จะยังถูกกำหนดเป็นเจ้าของของใบแจ้งหนี้อีกด้วย ซึ่งทำให้เจ้าของใบสั่งขายสามารถดูใบแจ้งหนี้ได้
 
## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

ก่อนที่จะซิงค์ใบแจ้งหนี้การขาย จำเป็นต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:

### <a name="setup-in-sales"></a>การตั้งค่าใน Sales

- ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่** 

- ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **วิธีการคำนวณส่วนลด** ถูกตั้งค่าเป็น **สินค้าในรายการ** 

### <a name="setup-in-the-data-integration-project"></a>การตั้งค่าในโครงการการรวมข้อมูล

#### <a name="salesinvoiceheader-task"></a>งาน SalesInvoiceHeader

- อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS** ใน **ต้นทาง** > **CDS** 

    -  เท็มเพลตเริ่มต้นสำหรับ **SalesOrder_Organization_OrganizationId** คือ ORG001
    -  ค่าเท็มเพลตเริ่มต้นสำหรับ **Account_Organization_OrganizationId** คือ ORG001
    -  ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId** คือ ORG001

- ให้แน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่ใน **ต้นทาง** > **CDS สำหรับ InvoiceCountryRegionId** ไปยัง **BillingAddress_Country**

    -  ค่าเท็มเพลตคือ **ValueMap** โดยมีประเทศต่าง ๆ จำนวนมากถูกแม็ป

- จำเป็นต้องใช้ **รายการราคา** เพื่อสร้างใบแจ้งหนี้ใน Sales อัพเดต **ValueMap** ใน **CDS** > **ปลายทางสำหรับ pricelevelid.name [ชื่อรายการราคา]** ไปยัง **รายการราคา** ที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน คุณสามารถใช้ค่าเริ่มต้น **รายการราคา** สำหรับสกุลเงินเดียวหรือใช้ **ValueMap** ถ้าคุณมี **รายการราคา** ในสกุลเงินหลายอย่าง

    -  ค่าเท็มเพลตสำหรับ **pricelevelid.name [ชื่อรายการราคา]** คือ **ValueMap** ตาม **สกุลเงิน**
    -  usd: CRM Service USA (ตัวอย่าง) 

#### <a name="salesinvoiceline-task"></a>งาน SalesInvoiceLine

- ให้แน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่ใน **ต้นทาง** > **CDS สำหรับหน่วยวัด**

- ให้แน่ใจว่า **ValueMap** ที่จำเป็นสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่ใน **ต้นทาง** > **การแม็ป CDS** 
    
    - ค่าเท็มเพลตที่มี **ValueMap** ถูกกำหนดสำหรับ **SalesUnitSymbol ให้กับ Quantity_UOM**
    
-  อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS ใน ต้นทาง** > **CDS** 

    -  เท็มเพลตเริ่มต้นสำหรับ **SalesInvoicer_Organization_OrganizationId** คือ ORG001
    -  ค่าเท็มเพลตเริ่มต้นสำหรับ **Product_Organization_OrganizationId** คือ ORG001
 
## <a name="template-mapping-in-data-integrator"></a>การแม็ปเท็มเพลตในตัวรวมข้อมูล

> [!NOTE]
> **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น คุณจำเป็นต้องตั้งค่าการแม็ปค่าสำหรับการแม็ปฟิลด์เหล่านี้ ซึ่งเฉพาะสำหรับข้อมูลในองค์กรระหว่างเอนทิตี้ที่ถูกซิงโครไนส์

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-2.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping.md)

[ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping.md)

[ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อใน Finance and Operations](contacts-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations](sales-quotation-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping.md)


