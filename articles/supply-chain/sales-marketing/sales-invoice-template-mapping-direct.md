---
title: ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Sales
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215987"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="43676-103">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="43676-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43676-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="43676-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="43676-105">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="43676-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="43676-106">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="43676-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="43676-107">แม่แบบของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดที่มีให้ใช้งานร่วมกันกับคุณลักษณะการรวมข้อมูล ช่วยให้เกิดกระแสของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="43676-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="43676-108">ภาพประกอบต่อไปนี้ แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="43676-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="43676-109">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="43676-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="43676-110">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="43676-110">Templates and tasks</span></span>

<span data-ttu-id="43676-111">เมื่อต้องการเข้าถึงแม่แบบที่พร้อมใช้งาน ให้เปิด [Power Apps ศูนย์การจัดการ](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="43676-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="43676-112">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="43676-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="43676-113">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Supply Chain Management ไปยัง Sales:</span><span class="sxs-lookup"><span data-stu-id="43676-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="43676-114">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ใบแจ้งหนี้การขาย (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="43676-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="43676-115">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="43676-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="43676-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="43676-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="43676-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="43676-117">SalesInvoiceLine</span></span>

<span data-ttu-id="43676-118">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ของส่วนหัวและรายการของใบแจ้งหนี้การขายได้:</span><span class="sxs-lookup"><span data-stu-id="43676-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="43676-119">ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) - โดยตรง</span><span class="sxs-lookup"><span data-stu-id="43676-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="43676-120">บัญชี (Sales ไปยัง Supply Chain Management) - โดยตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="43676-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="43676-121">ผู้ติดต่อ (Sales ไปยัง Supply Chain Management) - โดยตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="43676-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="43676-122">ส่วนหัวและรายการของใบสั่งขาย (Supply Chain Management ไปยัง Sales) - โดยตรง</span><span class="sxs-lookup"><span data-stu-id="43676-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="43676-123">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="43676-123">Entity set</span></span>

| <span data-ttu-id="43676-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-124">Supply Chain Management</span></span>                              | <span data-ttu-id="43676-125">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="43676-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="43676-126">ส่วนหัวใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="43676-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="43676-127">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="43676-127">Invoices</span></span>       |
| <span data-ttu-id="43676-128">รายการในใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="43676-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="43676-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="43676-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="43676-130">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="43676-130">Entity flow</span></span>

<span data-ttu-id="43676-131">ใบเสนอราคาขายจะถูกสร้างขึ้นใน Supply Chain Management และซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="43676-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="43676-132">ในขณะนี้ ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบนส่วนหัวของใบแจ้งหนี้การขายไม่ได้รวมอยู่ในการซิงโครไนส์จาก Supply Chain Managements ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="43676-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="43676-133">Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="43676-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="43676-134">อย่างไรก็ตาม ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการจะรวมอยู่ในการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="43676-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="43676-135">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="43676-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="43676-136">ฟิลด์ **หมายเลขใบแจ้งหนี้** ถูกเพิ่มไปยังเอนทิตี้ **ใบแจ้งหนี้** และแสดงขึ้นบนหน้า</span><span class="sxs-lookup"><span data-stu-id="43676-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="43676-137">ปุ่ม **สร้างใบแจ้งหนี้** บนหน้า **ใบสั่งขาย** ถูกซ่อนอยู่เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Supply Chain Management และถูกซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="43676-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="43676-138">หน้า **ใบแจ้งหนี้** จะไม่สามารถแก้ไขได้เนื่องจากใบแจ้งหนี้จะถูกซิงโครไนส์จาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="43676-139">ค่า **สถานะของใบสั่งขาย** จะเปลี่ยนเป็น **ใบแจ้งหนี้** โดยอัตโนมัติเมื่อใบแจ้งหนี้ที่เกี่ยวข้องจาก Supply Chain Management ซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="43676-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="43676-140">นอกจากนี้ เจ้าของใบสั่งขายที่มีการสร้างใบแจ้งหนี้จะยังถูกกำหนดให้เป็นเจ้าของของใบแจ้งหนี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="43676-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="43676-141">ดังนั้น เจ้าของใบสั่งขายสามารถดูใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="43676-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="43676-142">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="43676-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="43676-143">ก่อนที่คุณจะซิงค์ใบแจ้งหนี้การขาย จำเป็นที่คุณต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43676-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="43676-144">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="43676-144">Setup in Sales</span></span>

<span data-ttu-id="43676-145">ไปยัง **การตั้งค่า** > **การดูแล** > **การตั้งค่าระบบ** > **การขาย** และต้องมั่นใจว่ามีใช้การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43676-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="43676-146">ตัวเลือก **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="43676-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="43676-147">ฟิลด์ **วิธีการคำนวณส่วนลด** ถูกกำหนดเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="43676-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="43676-148">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="43676-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="43676-149">งาน SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="43676-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="43676-150">ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **InvoiceCountryRegionId** ไปยัง **BillingAddress\_Country**</span><span class="sxs-lookup"><span data-stu-id="43676-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="43676-151">ค่าของเท็มเพลตคือ แผนผังค่าที่แม็ปหลายประเทศหรือภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="43676-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="43676-152">จำเป็นต้องใช้รายการราคาเพื่อสร้างใบแจ้งหนี้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="43676-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="43676-153">อัพเดตแผนผังค่าสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** ไปยังรายการราคาที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="43676-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="43676-154">คุณสามารถใช้รายการราคาเริ่มต้นสำหรับสกุลเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="43676-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="43676-155">อีกทางหนึ่งคือ ถ้าคุณมีรายการราคาในหลายสกุลเงิน คุณสามารถใช้แผนผังค่าได้</span><span class="sxs-lookup"><span data-stu-id="43676-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="43676-156">ค่าเท็มเพลตสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** คือแผนผังค่าที่ขึ้นอยู่กับสกุลเงินที่มี USD = บริการ CRM USA (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="43676-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="43676-157">งาน SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="43676-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="43676-158">ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **หน่วยวัด**</span><span class="sxs-lookup"><span data-stu-id="43676-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="43676-159">ตรวจสอบให้แน่ใจว่ามีแผนผังค่าที่ต้องการสำหรับ **SalesUnitSymbol** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="43676-160">ค่าเท็มเพลตที่มีแผนผังค่าถูกกำหนดสำหรับ **SalesUnitSymbol** ไปยัง **Quantity\_UOM**</span><span class="sxs-lookup"><span data-stu-id="43676-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="43676-161">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="43676-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="43676-162">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="43676-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="43676-163">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="43676-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="43676-164">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="43676-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="43676-165">การแม็ปจะช่วยแสดงให้เห็นว่า ข้อมูลฟิลด์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="43676-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="43676-166">SalesInvoiceHeader</span></span>

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="43676-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="43676-168">SalesInvoiceLine</span></span>

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="43676-170">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="43676-170">Related topics</span></span>

[<span data-ttu-id="43676-171">ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด</span><span class="sxs-lookup"><span data-stu-id="43676-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="43676-172">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="43676-173">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="43676-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="43676-174">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="43676-175">การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43676-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
