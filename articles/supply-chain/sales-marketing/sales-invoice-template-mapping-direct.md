---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Sales"
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="beb67-103">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้โดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="beb67-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="beb67-105">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="beb67-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="beb67-106">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="beb67-107">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="beb67-108">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="beb67-109">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="beb67-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="beb67-110">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="beb67-110">Templates and tasks</span></span>

<span data-ttu-id="beb67-111">เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="beb67-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="beb67-112">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="beb67-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="beb67-113">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Finance and Operations ไปยัง Sales:</span><span class="sxs-lookup"><span data-stu-id="beb67-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="beb67-114">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ใบแจ้งหนี้การขาย (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="beb67-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="beb67-115">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="beb67-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="beb67-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="beb67-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="beb67-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="beb67-117">SalesInvoiceLine</span></span>

<span data-ttu-id="beb67-118">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ของส่วนหัวและรายการของใบแจ้งหนี้การขายได้:</span><span class="sxs-lookup"><span data-stu-id="beb67-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="beb67-119">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="beb67-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="beb67-120">บัญชี (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="beb67-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="beb67-121">ผู้ติดต่อ (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="beb67-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="beb67-122">ส่วนหัวและรายการของใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="beb67-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="beb67-123">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="beb67-123">Entity set</span></span>

| <span data-ttu-id="beb67-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="beb67-124">Finance and Operations</span></span>                               | <span data-ttu-id="beb67-125">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="beb67-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="beb67-126">ส่วนหัวใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="beb67-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="beb67-127">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="beb67-127">Invoices</span></span>       |
| <span data-ttu-id="beb67-128">รายการในใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="beb67-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="beb67-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="beb67-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="beb67-130">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="beb67-130">Entity flow</span></span>

<span data-ttu-id="beb67-131">ใบแจ้งหนี้การขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="beb67-132">ในขณะนี้ ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบนส่วนหัวของใบแจ้งหนี้การขาย ไม่ได้รวมอยู่ในการซิงโครไนส์จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="beb67-133">Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="beb67-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="beb67-134">อย่างไรก็ตาม ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการจะรวมอยู่ในการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="beb67-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="beb67-135">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="beb67-136">ฟิลด์ **หมายเลขใบแจ้งหนี้** ถูกเพิ่มไปยังเอนทิตี้ **ใบแจ้งหนี้** และแสดงขึ้นบนหน้า</span><span class="sxs-lookup"><span data-stu-id="beb67-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="beb67-137">ปุ่ม **สร้างใบแจ้งหนี้** บนหน้า **ใบสั่งขาย** ถูกซ่อนอยู่ เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และถูกซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="beb67-138">หน้า **ใบแจ้งหนี้** จะไม่สามารถแก้ไขได้ เนื่องจากใบแจ้งหนี้จะถูกซิงค์จาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="beb67-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="beb67-139">ค่า **สถานะของใบสั่งขาย** จะเปลี่ยนเป็น **ใบแจ้งหนี้** โดยอัตโนมัติ เมื่อมีการซิงค์ใบแจ้งหนี้ที่เกี่ยวข้องจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="beb67-140">นอกจากนี้ เจ้าของใบสั่งขายที่มีการสร้างใบแจ้งหนี้จะยังถูกกำหนดให้เป็นเจ้าของของใบแจ้งหนี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="beb67-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="beb67-141">ดังนั้น เจ้าของใบสั่งขายสามารถดูใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="beb67-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="beb67-142">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="beb67-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="beb67-143">ก่อนที่คุณจะซิงค์ใบแจ้งหนี้การขาย จำเป็นที่คุณต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="beb67-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="beb67-144">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-144">Setup in Sales</span></span>

<span data-ttu-id="beb67-145">ไปยัง **การตั้งค่า** > **การดูแล** > **การตั้งค่าระบบ** > **การขาย** และต้องมั่นใจว่ามีใช้การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="beb67-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="beb67-146">ตัวเลือก **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="beb67-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="beb67-147">ฟิลด์ **วิธีการคำนวณส่วนลด** ถูกกำหนดเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="beb67-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="beb67-148">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="beb67-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="beb67-149">งาน SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="beb67-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="beb67-150">ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **InvoiceCountryRegionId** ไปยัง **BillingAddress\_Country**</span><span class="sxs-lookup"><span data-stu-id="beb67-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="beb67-151">ค่าของเท็มเพลตคือ แผนผังค่าที่แม็ปหลายประเทศหรือภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="beb67-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="beb67-152">จำเป็นต้องใช้รายการราคาเพื่อสร้างใบแจ้งหนี้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="beb67-153">อัพเดตแผนผังค่าสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** ไปยังรายการราคาที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="beb67-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="beb67-154">คุณสามารถใช้รายการราคาเริ่มต้นสำหรับสกุลเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="beb67-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="beb67-155">อีกทางหนึ่งคือ ถ้าคุณมีรายการราคาในหลายสกุลเงิน คุณสามารถใช้แผนผังค่าได้</span><span class="sxs-lookup"><span data-stu-id="beb67-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="beb67-156">ค่าเท็มเพลตสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** คือแผนผังค่าที่ขึ้นอยู่กับสกุลเงินที่มี USD = บริการ CRM USA (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="beb67-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="beb67-157">งาน SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="beb67-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="beb67-158">ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **หน่วยวัด**</span><span class="sxs-lookup"><span data-stu-id="beb67-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="beb67-159">ตรวจสอบให้แน่ใจว่าแผนผังค่าที่ต้องการสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่</span><span class="sxs-lookup"><span data-stu-id="beb67-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="beb67-160">ค่าเท็มเพลตที่มีแผนผังค่าถูกกำหนดสำหรับ **SalesUnitSymbol** ไปยัง **Quantity\_UOM**</span><span class="sxs-lookup"><span data-stu-id="beb67-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="beb67-161">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="beb67-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="beb67-162">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="beb67-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="beb67-163">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="beb67-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="beb67-164">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="beb67-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="beb67-165">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="beb67-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="beb67-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="beb67-166">SalesInvoiceHeader</span></span>

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="beb67-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="beb67-168">SalesInvoiceLine</span></span>

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="beb67-170">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="beb67-170">Related topics</span></span>

[<span data-ttu-id="beb67-171">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="beb67-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="beb67-172">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="beb67-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="beb67-173">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="beb67-174">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="beb67-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="beb67-175">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="beb67-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







