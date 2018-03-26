---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales"
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
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 347509a9556f15e7d880508e36516f04bc6964b7
ms.contentlocale: th-th
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales

## <a name="data-flow-in-prospect-to-cash"></a>โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด

โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales

[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration) เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Finance and Operations ไปยัง Sales:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** ใบแจ้งหนี้การขาย (Fin and Ops ไปยัง Sales) - ตรง
- **ชื่อของงานในโครงการการรวมข้อมูล:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ของส่วนหัวและรายการของใบแจ้งหนี้การขายได้:

- ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales) - ตรง
- บัญชี (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)
- ผู้ติดต่อ (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)
- ส่วนหัวและรายการของใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Finance and Operations                               | ใบสั่งขาย          |
|------------------------------------------------------|----------------|
| ส่วนหัวใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก | ใบแจ้งหนี้       |
| รายการในใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก   | InvoiceDetails |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

ใบแจ้งหนี้การขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales

> [!NOTE]
> ในขณะนี้ ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบนส่วนหัวของใบแจ้งหนี้การขาย ไม่ได้รวมอยู่ในการซิงโครไนส์จาก Finance and Operations ไปยัง Sales Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว อย่างไรก็ตาม ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการจะรวมอยู่ในการซิงโครไนส์

## <a name="prospect-to-cash-solution-for-sales"></a>โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales

- ฟิลด์ **หมายเลขใบแจ้งหนี้** ถูกเพิ่มไปยังเอนทิตี้ **ใบแจ้งหนี้** และแสดงขึ้นบนหน้า
- ปุ่ม **สร้างใบแจ้งหนี้** บนหน้า **ใบสั่งขาย** ถูกซ่อนอยู่ เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และถูกซิงค์ไปยัง Sales หน้า **ใบแจ้งหนี้** จะไม่สามารถแก้ไขได้ เนื่องจากใบแจ้งหนี้จะถูกซิงค์จาก Finance and Operations
- ค่า **สถานะของใบสั่งขาย** จะเปลี่ยนเป็น **ใบแจ้งหนี้** โดยอัตโนมัติ เมื่อมีการซิงค์ใบแจ้งหนี้ที่เกี่ยวข้องจาก Finance and Operations ไปยัง Sales นอกจากนี้ เจ้าของใบสั่งขายที่มีการสร้างใบแจ้งหนี้จะยังถูกกำหนดให้เป็นเจ้าของของใบแจ้งหนี้อีกด้วย ดังนั้น เจ้าของใบสั่งขายสามารถดูใบแจ้งหนี้ได้

## <a name="preconditions-and-mapping-setup"></a>การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป

ก่อนที่คุณจะซิงค์ใบแจ้งหนี้การขาย จำเป็นที่คุณต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:

### <a name="setup-in-sales"></a>การตั้งค่าใน Sales

ไปยัง **การตั้งค่า** > **การดูแล** > **การตั้งค่าระบบ** > **การขาย** และต้องมั่นใจว่ามีใช้การตั้งค่าต่อไปนี้:

- ตัวเลือก **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**
- ฟิลด์ **วิธีการคำนวณส่วนลด** ถูกกำหนดเป็น **สินค้าในรายการ**

### <a name="setup-in-the-data-integration-project"></a>การตั้งค่าในโครงการการรวมข้อมูล

#### <a name="salesinvoiceheader-task"></a>งาน SalesInvoiceHeader

- ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **InvoiceCountryRegionId** ไปยัง **BillingAddress\_Country**

    ค่าของเท็มเพลตคือ แผนผังค่าที่แม็ปหลายประเทศหรือภูมิภาค

- จำเป็นต้องใช้รายการราคาเพื่อสร้างใบแจ้งหนี้ใน Sales อัพเดตแผนผังค่าสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** ไปยังรายการราคาที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน คุณสามารถใช้รายการราคาเริ่มต้นสำหรับสกุลเงินเดียวกัน อีกทางหนึ่งคือ ถ้าคุณมีรายการราคาในหลายสกุลเงิน คุณสามารถใช้แผนผังค่าได้

    ค่าเท็มเพลตสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** คือแผนผังค่าที่ขึ้นอยู่กับสกุลเงินที่มี USD = บริการ CRM USA (ตัวอย่าง)  
    
#### <a name="salesinvoiceline-task"></a>งาน SalesInvoiceLine

- ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **หน่วยวัด**
- ตรวจสอบให้แน่ใจว่าแผนผังค่าที่ต้องการสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่

    ค่าเท็มเพลตที่มีแผนผังค่าถูกกำหนดสำหรับ **SalesUnitSymbol** ไปยัง **Quantity\_UOM**

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

> [!NOTE]
> ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล 

> [!NOTE]
> การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง

[ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](prospect-to-cash.md)

[ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations](accounts-template-mapping-direct.md)

[ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales](products-template-mapping-direct.md)

[ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อใน Finance and Operations](contacts-template-mapping-direct.md)

[ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales](sales-order-template-mapping-direct-two-ways.md)







