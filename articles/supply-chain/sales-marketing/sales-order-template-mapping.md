---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales 

## <a name="template-and-tasks"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales

- **ชื่อของเท็มเพลตในการรวมข้อมูล** 

    - ใบสั่งขาย (Fin and Ops ไปยัง Sales)
    
- **ชื่อของงานในโครงการการรวมข้อมูล**

    - OrderHeader
    - OrderLine

ซิงค์งานที่จำเป็นก่อนการซิงค์ส่วนหัวและรายการของใบแจ้งหนี้การขาย:

- ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales)
- บัญชี (Sales ไปยัง Fin and Ops) (ถ้าใช้)
- ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) (ถ้าใช้)

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Finance and Operations |    Common Data Service (CDS)         |     ใบสั่งขาย      |
|------------------------|----------------|----------------|
| ส่วนหัวของใบสั่งขาย CDS| SalesOrder     | SalesOrders |
| รายการในใบสั่งขาย CDS  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

ใบสั่งขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales

ตัวกรองในเท็มเพลตช่วยให้แน่ใจว่ามีเฉพาะใบสั่งขายที่เกี่ยวข้องเท่านั้นที่รวมอยู่ในการซิงค์:

- ทั้งลูกค้าที่สั่งซื้อและที่ออกใบแจ้งหนี้ในใบสั่งขายที่มีต้นกำเนิดมาจาก Sales เท่านั้นที่จะรวมอยู่ในการซิงค์ ใน Finance and Operations ฟิลด์ **OrderingCustomerIsExternallyMaintained** และ **InvoiceCustomerIsExternallyMaintained** ถูกใช้ในการติดตามการซิงโครไนส์ในเอนทิตีข้อมูล

- **ใบสั่งขาย** ใน Finance and Operations ต้องได้รับการยืนยัน เฉพาะใบสั่งขายที่ยืนยันแล้วหรือใบสั่งขายที่มีสถานะการประมวลผลสูง ตัวอย่างเช่น สถานะจัดส่งแล้ว หรือออกใบแจ้งหนี้แล้ว ที่จะถูกซิงค์ไปยัง Sales

- หลังจากสร้างหรือปรับเปลี่ยนใบสั่งขาย ชุดงาน **คำนวณยอดขายรวม** ใน Finance and Operations จะต้องถูกดำเนินการ เฉพาะใบสั่งขายที่มีการคำนวณยอดขายรวมเท่านั้นที่จะถูกซิงค์ไปยัง CDS และ Sales

> [!NOTE]
> ในขณะนี้ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบน **ส่วนหัวของใบสั่งขาย** ไม่ได้รวมอยู่ในการซิงค์จาก Finance and Operations ไปยัง Sales ทั้งนี้เนื่องจาก Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว มีการรวมภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการ

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

ฟิลด์ใหม่จะถูกเพิ่มลงในเอนทิตี้ **ใบสั่ง** และแสดงขึ้นบนหน้า:

- **รักษาไว้สำหรับภายนอก** - ถูกตั้งค่าเป็น **ใช่** เมื่อใบสั่งมาจาก Finance and Operations

- **สถานะการประมวลผล** - ใช้เพื่อแสดงสถานะการประมวลผลใบสั่งใน Finance and Operations ค่าได้แก่:

    - ใช้งาน
    - วันที่ยืนยัน
    - บันทึกการจัดส่ง
    - ออกใบแจ้งหนี้แล้ว
    - เบิกสินค้าแล้ว
    - เบิกสินค้าแล้วบางส่วน
    - บรรจุแล้วบางส่วน
    - จัดส่งสินค้าแล้ว
    - จัดส่งแล้วบางส่วน
    - ออกใบแจ้งหนี้แล้วบางส่วน
    - ยกเลิก

การตั้งค่า **มีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น** จะใช้ในสถานการณ์จำลองอื่นใบสั่งขายอื่น (การซิงค์จาก Sales ไปยัง Finance and Operation) เพื่อติดตามว่าใบสั่งขายถูกสร้างขึ้นจาก **ผลิตภัณฑ์รักษาไว้สำหรับภายนอก** ทั้งหมด ในกรณีที่ผลิตภัณฑ์ได้รับการรักษาใน Finance and Operations ลักษณะการทำงานนี้ช่วยรับประกันว่า คุณจะไม่พยายามซิงโครไนส์รายการในใบสั่งขายที่มีผลิตภัณฑ์ที่ไม่รู้จักใน Finance and Operations
 
ปุ่ม **สร้างใบแจ้งหนี้**, **ยกเลิกใบสั่ง**, **คำนวณใหม่**, **เรียกดูผลิตภัณฑ์** และ **ค้นหาที่อยู่** บนหน้า **ใบสั่งขาย** ถูกซ่อนไว้สำหรับใบสั่งที่รักษาไว้สำหรับภายนอกเนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และซิงค์ไปยัง Sales หน้าใบสั่งจะไม่สามารถแก้ไขได้เนื่องจากข้อมูลในใบสั่งจะถูกซิงค์จาก Finance and Operations
 
**สถานะของใบสั่งขาย** จะยังคงใช้งานอยู่เพื่อให้แน่ใจว่าการเปลี่ยนแปลงจาก Finance and Operations สามารถดำเนินไปยัง **ใบสั่งขาย** ใน Sales ได้ ซึ่งจะถูกควบคุมโดยการตั้งค่า **Statecode [สถานะ]** เริ่มต้นเป็น **ที่ใช้งานอยู่** ในโครงการการรวมข้อมูล

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป 

ก่อนที่จะซิงค์ใบสั่งขาย จำเป็นต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:

### <a name="setup-in-sales"></a>การตั้งค่าใน Sales

- ให้สิทธิ์สำหรับทีมงานที่ผู้ใช้ (จาก **การตั้งค่าการเชื่อมต่อ** ของ Sales ของคุณ) ถูกกำหนดให้ ถ้าคุณกำลังใช้ข้อมูลสาธิต โดยปกติผู้ใช้จะสามารถเข้าใช้ได้ แต่ทีมงานจะไม่สามารถเข้าใช้ได้ หากไม่มีสิ่งนี้ คุณจะได้รับข้อผิดพลาดที่แสดงว่าทีมงานหลักหายไปเมื่อรันโครงการจากตัวรวมข้อมูล 

    - ภายใต้ **การตั้งค่า** > **ความปลอดภัย** > **ทีมงาน** เลือกทีมงานที่เกี่ยวข้อง คลิก **จัดการบทบาท** และเลือกบทบาทที่มีสิทธิ์ที่เหมาะสม เช่น ผู้ดูแลระบบ

- ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่** 

- ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **วิธีการคำนวณส่วนลด** ถูกตั้งค่าเป็น **สินค้าในรายการ** 

### <a name="setup-in-finance-and-operations"></a>ตั้งค่าใน Finance and Operations

ตั้งค่า **การขายและการตลาด** > **งานประจำงวด** > **คำนวณยอดขายรวม** เพื่อรันเป็นชุดงานที่มีการตั้งค่า **คำนวณยอดรวมสำหรับใบสั่งขาย** เป็น **ใช่** สิ่งนี้เป็นสิ่งสำคัญเนื่องจากเฉพาะใบสั่งขายที่มีการคำนวณยอดขายรวมเท่านั้นที่จะถูกซิงค์ไปยัง CDS และ Sales ความถี่ของชุดงานควรถูกปรับให้เข้ากับความถี่ของการซิงโครไนส์ใบสั่งขาย

### <a name="setup-in-the-data-integration-project"></a>การตั้งค่าในโครงการการรวมข้อมูล

#### <a name="salesheader-task"></a>งาน SalesHeader

- อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS ใน ต้นทาง** > **CDS**

    - ค่าเท็มเพลตเริ่มต้นสำหรับ **Account_Organization_OrganizationId** คือ ORG001
    - ค่าเท็มเพลตเริ่มต้นสำหรับ **InvoiceAccount_Organization_OrganizationId** คือ ORG001
    - ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId** คือ ORG001

- ให้แน่ใจว่าการแม็ปที่จำเป็นมีอยู่ใน **ต้นทาง** > **CDS สำหรับ InvoiceCountryRegionId ไปยัง BillingAddress_Country** และสำหรับ **DeliveryCountryRegionId ไปยัง DeliveryAddress_Country**

    - ค่าเท็มเพลตคือ **ValueMap** โดยมีประเทศต่าง ๆ จำนวนมากถูกแม็ป

- จำเป็นต้องใช้ **รายการราคา** เพื่อสร้างใบสั่งใน Sales อัพเดต **ValueMap** ใน **CDS** > **ปลายทาง** สำหรับ **pricelevelid.name [ชื่อรายการราคา]** ไปยัง **รายการราคา** ที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน คุณสามารถใช้ค่าเริ่มต้น **รายการราคา** สำหรับสกุลเงินเดียวหรือใช้ **ValueMap** ถ้าคุณมี **รายการราคา** ในสกุลเงินหลายอย่าง
    
    - ค่าเท็มเพลตเริ่มต้นสำหรับ **pricelevelid.name [ชื่อรายการราคา]** คือ CRM Service USA (ตัวอย่าง) 

#### <a name="salesline-task"></a>งาน SalesLine

- อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS ใน ต้นทาง** > **CDS** 
    
    - เท็มเพลตเริ่มต้นสำหรับ **SalesOrder_Organization_OrganizationId** คือ ORG001
    - ค่าเท็มเพลตเริ่มต้นสำหรับ **Product_Organization_OrganizationId** คือ ORG001

- ให้แน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่ใน **ต้นทาง** > **CDS** สำหรับ **DeliveryCountryRegionId** ไปยัง **DeliveryAddress_Country**

    - ค่าเท็มเพลตคือ **ValueMap** โดยมีประเทศต่าง ๆ จำนวนมากถูกแม็ป
    
- ให้แน่ใจว่า **ValueMap** ที่จำเป็นสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่ใน **ต้นทาง** > **การแม็ป CDS**

    - ค่าเท็มเพลตที่มี **ValueMap** ถูกกำหนดสำหรับ **SalesUnitSymbol ให้กับ Quantity_UOM**

## <a name="template-mapping-in-data-integrator"></a>การแม็ปเท็มเพลตในตัวรวมข้อมูล

> [!NOTE]
> ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล

### <a name="orderheader"></a>OrderHeader

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping.md)

[ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping.md)

[ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อใน Finance and Operations](contacts-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations](sales-quotation-template-mapping.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales](sales-invoice-template-mapping.md)


