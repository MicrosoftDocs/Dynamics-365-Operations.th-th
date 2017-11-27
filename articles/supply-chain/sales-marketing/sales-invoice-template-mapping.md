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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="73204-103">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="73204-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="73204-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="73204-105">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="73204-105">Templates and tasks</span></span>

<span data-ttu-id="73204-106">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="73204-107">**ชื่อของเท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="73204-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="73204-108">ใบแจ้งหนี้การขาย (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="73204-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="73204-109">**ชื่อของงานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="73204-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="73204-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="73204-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="73204-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="73204-111">SalesInvoiceLine</span></span>

<span data-ttu-id="73204-112">ซิงค์งานที่จำเป็นก่อนการซิงค์ส่วนหัวและรายการของใบแจ้งหนี้การขาย:</span><span class="sxs-lookup"><span data-stu-id="73204-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="73204-113">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="73204-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="73204-114">บัญชี (Sales ไปยัง Fin and Ops) (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="73204-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="73204-115">ผู้ติดต่อ (Sales ไปยัง Fin and Ops) (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="73204-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="73204-116">ส่วนหัวและรายการของใบสั่งขาย (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="73204-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="73204-117">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="73204-117">Entity set</span></span>

| <span data-ttu-id="73204-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73204-118">Finance and Operations</span></span>                               | <span data-ttu-id="73204-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="73204-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="73204-120">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="73204-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="73204-121">ส่วนหัวใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="73204-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="73204-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="73204-122">SalesInvoice</span></span>     | <span data-ttu-id="73204-123">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="73204-123">Invoices</span></span>       |
| <span data-ttu-id="73204-124">รายการในใบแจ้งหนี้การขายของลูกค้าที่รักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="73204-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="73204-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="73204-125">SalesInvoiceLine</span></span> | <span data-ttu-id="73204-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="73204-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="73204-127">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="73204-127">Entity flow</span></span>

<span data-ttu-id="73204-128">ใบแจ้งหนี้การขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="73204-129">ในขณะนี้ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบน **ส่วนหัวของใบแจ้งหนี้การขาย** ไม่ได้รวมอยู่ในการซิงค์จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="73204-130">ทั้งนี้เนื่องจาก Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="73204-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="73204-131">มีการรวมภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="73204-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="73204-132">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="73204-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="73204-133">**ฟิลด์หมายเลขใบแจ้งหนี้** ถูกเพิ่มไปยังเอนทิตี้ **ใบแจ้งหนี้** และแสดงขึ้นบนหน้า</span><span class="sxs-lookup"><span data-stu-id="73204-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="73204-134">ปุ่ม **สร้างใบแจ้งหนี้** บนหน้า **ใบสั่งขาย** ถูกซ่อนอยู่เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และถูกซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="73204-135">หน้า **ใบแจ้งหนี้** จะไม่สามารถแก้ไขได้เนื่องจากใบแจ้งหนี้จะถูกซิงค์จาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73204-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="73204-136">**สถานะของใบสั่งขาย** จะเปลี่ยนเป็น **ใบแจ้งหนี้** โดยอัตโนมัติเมื่อมีการซิงค์ใบแจ้งหนี้ที่เกี่ยวข้องจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="73204-137">นอกจากนี้ เจ้าของใบสั่งขายที่มีการสร้างใบแจ้งหนี้จะยังถูกกำหนดเป็นเจ้าของของใบแจ้งหนี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="73204-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="73204-138">ซึ่งทำให้เจ้าของใบสั่งขายสามารถดูใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="73204-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="73204-139">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="73204-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="73204-140">ก่อนที่จะซิงค์ใบแจ้งหนี้การขาย จำเป็นต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="73204-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="73204-141">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="73204-141">Setup in Sales</span></span>

- <span data-ttu-id="73204-142">ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="73204-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="73204-143">ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **วิธีการคำนวณส่วนลด** ถูกตั้งค่าเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="73204-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="73204-144">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73204-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="73204-145">งาน SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="73204-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="73204-146">อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS** ใน **ต้นทาง** > **CDS**</span><span class="sxs-lookup"><span data-stu-id="73204-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="73204-147">เท็มเพลตเริ่มต้นสำหรับ **SalesOrder_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="73204-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="73204-148">ค่าเท็มเพลตเริ่มต้นสำหรับ **Account_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="73204-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="73204-149">ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="73204-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="73204-150">ให้แน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่ใน **ต้นทาง** > **CDS สำหรับ InvoiceCountryRegionId** ไปยัง **BillingAddress_Country**</span><span class="sxs-lookup"><span data-stu-id="73204-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="73204-151">ค่าเท็มเพลตคือ **ValueMap** โดยมีประเทศต่าง ๆ จำนวนมากถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="73204-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="73204-152">จำเป็นต้องใช้ **รายการราคา** เพื่อสร้างใบแจ้งหนี้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="73204-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="73204-153">อัพเดต **ValueMap** ใน **CDS** > **ปลายทางสำหรับ pricelevelid.name [ชื่อรายการราคา]** ไปยัง **รายการราคา** ที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="73204-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="73204-154">คุณสามารถใช้ค่าเริ่มต้น **รายการราคา** สำหรับสกุลเงินเดียวหรือใช้ **ValueMap** ถ้าคุณมี **รายการราคา** ในสกุลเงินหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="73204-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="73204-155">ค่าเท็มเพลตสำหรับ **pricelevelid.name [ชื่อรายการราคา]** คือ **ValueMap** ตาม **สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="73204-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="73204-156">usd: CRM Service USA (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="73204-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="73204-157">งาน SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="73204-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="73204-158">ให้แน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่ใน **ต้นทาง** > **CDS สำหรับหน่วยวัด**</span><span class="sxs-lookup"><span data-stu-id="73204-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="73204-159">ให้แน่ใจว่า **ValueMap** ที่จำเป็นสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่ใน **ต้นทาง** > **การแม็ป CDS**</span><span class="sxs-lookup"><span data-stu-id="73204-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="73204-160">ค่าเท็มเพลตที่มี **ValueMap** ถูกกำหนดสำหรับ **SalesUnitSymbol ให้กับ Quantity_UOM**</span><span class="sxs-lookup"><span data-stu-id="73204-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="73204-161">อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS ใน ต้นทาง** > **CDS**</span><span class="sxs-lookup"><span data-stu-id="73204-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="73204-162">เท็มเพลตเริ่มต้นสำหรับ **SalesInvoicer_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="73204-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="73204-163">ค่าเท็มเพลตเริ่มต้นสำหรับ **Product_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="73204-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="73204-164">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73204-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="73204-165">**เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="73204-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="73204-166">คุณจำเป็นต้องตั้งค่าการแม็ปค่าสำหรับการแม็ปฟิลด์เหล่านี้ ซึ่งเฉพาะสำหรับข้อมูลในองค์กรระหว่างเอนทิตี้ที่ถูกซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="73204-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="73204-167">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73204-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-2.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="73204-172">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="73204-172">Related topics</span></span>

[<span data-ttu-id="73204-173">ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="73204-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="73204-174">ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73204-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="73204-175">ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73204-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="73204-176">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="73204-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="73204-177">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="73204-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


