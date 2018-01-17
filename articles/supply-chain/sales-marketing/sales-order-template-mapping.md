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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="49a18-103">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="49a18-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="49a18-105">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="49a18-105">Template and tasks</span></span>

<span data-ttu-id="49a18-106">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="49a18-107">**ชื่อของเท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="49a18-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="49a18-108">ใบสั่งขาย (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="49a18-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="49a18-109">**ชื่อของงานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="49a18-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="49a18-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="49a18-110">OrderHeader</span></span>
    - <span data-ttu-id="49a18-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="49a18-111">OrderLine</span></span>

<span data-ttu-id="49a18-112">ซิงค์งานที่จำเป็นก่อนการซิงค์ส่วนหัวและรายการของใบแจ้งหนี้การขาย:</span><span class="sxs-lookup"><span data-stu-id="49a18-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="49a18-113">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="49a18-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="49a18-114">บัญชี (Sales ไปยัง Fin and Ops) (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="49a18-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="49a18-115">ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="49a18-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="49a18-116">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="49a18-116">Entity set</span></span>

| <span data-ttu-id="49a18-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-117">Finance and Operations</span></span> |    <span data-ttu-id="49a18-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="49a18-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="49a18-119">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="49a18-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="49a18-120">ส่วนหัวของใบสั่งขาย CDS</span><span class="sxs-lookup"><span data-stu-id="49a18-120">CDS sales order headers</span></span>| <span data-ttu-id="49a18-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="49a18-121">SalesOrder</span></span>     | <span data-ttu-id="49a18-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="49a18-122">SalesOrders</span></span> |
| <span data-ttu-id="49a18-123">รายการในใบสั่งขาย CDS</span><span class="sxs-lookup"><span data-stu-id="49a18-123">CDS sales order lines</span></span>  | <span data-ttu-id="49a18-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="49a18-124">SalesOrderLine</span></span> | <span data-ttu-id="49a18-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="49a18-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="49a18-126">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="49a18-126">Entity flow</span></span>

<span data-ttu-id="49a18-127">ใบสั่งขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="49a18-128">ตัวกรองในเท็มเพลตช่วยให้แน่ใจว่ามีเฉพาะใบสั่งขายที่เกี่ยวข้องเท่านั้นที่รวมอยู่ในการซิงค์:</span><span class="sxs-lookup"><span data-stu-id="49a18-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="49a18-129">ทั้งลูกค้าที่สั่งซื้อและที่ออกใบแจ้งหนี้ในใบสั่งขายที่มีต้นกำเนิดมาจาก Sales เท่านั้นที่จะรวมอยู่ในการซิงค์</span><span class="sxs-lookup"><span data-stu-id="49a18-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="49a18-130">ใน Finance and Operations ฟิลด์ **OrderingCustomerIsExternallyMaintained** และ **InvoiceCustomerIsExternallyMaintained** ถูกใช้ในการติดตามการซิงโครไนส์ในเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49a18-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="49a18-131">**ใบสั่งขาย** ใน Finance and Operations ต้องได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="49a18-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="49a18-132">เฉพาะใบสั่งขายที่ยืนยันแล้วหรือใบสั่งขายที่มีสถานะการประมวลผลสูง ตัวอย่างเช่น สถานะจัดส่งแล้ว หรือออกใบแจ้งหนี้แล้ว ที่จะถูกซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="49a18-133">หลังจากสร้างหรือปรับเปลี่ยนใบสั่งขาย ชุดงาน **คำนวณยอดขายรวม** ใน Finance and Operations จะต้องถูกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="49a18-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="49a18-134">เฉพาะใบสั่งขายที่มีการคำนวณยอดขายรวมเท่านั้นที่จะถูกซิงค์ไปยัง CDS และ Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="49a18-135">ในขณะนี้ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบน **ส่วนหัวของใบสั่งขาย** ไม่ได้รวมอยู่ในการซิงค์จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="49a18-136">ทั้งนี้เนื่องจาก Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="49a18-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="49a18-137">มีการรวมภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="49a18-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="49a18-138">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="49a18-139">ฟิลด์ใหม่จะถูกเพิ่มลงในเอนทิตี้ **ใบสั่ง** และแสดงขึ้นบนหน้า:</span><span class="sxs-lookup"><span data-stu-id="49a18-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="49a18-140">**รักษาไว้สำหรับภายนอก** - ถูกตั้งค่าเป็น **ใช่** เมื่อใบสั่งมาจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="49a18-141">**สถานะการประมวลผล** - ใช้เพื่อแสดงสถานะการประมวลผลใบสั่งใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="49a18-142">ค่าได้แก่:</span><span class="sxs-lookup"><span data-stu-id="49a18-142">Values are:</span></span>

    - <span data-ttu-id="49a18-143">ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="49a18-143">Active</span></span>
    - <span data-ttu-id="49a18-144">วันที่ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="49a18-144">Confirmed</span></span>
    - <span data-ttu-id="49a18-145">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="49a18-145">Packing Slip</span></span>
    - <span data-ttu-id="49a18-146">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="49a18-146">Invoiced</span></span>
    - <span data-ttu-id="49a18-147">เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="49a18-147">Picked</span></span>
    - <span data-ttu-id="49a18-148">เบิกสินค้าแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="49a18-148">Partially Picked</span></span>
    - <span data-ttu-id="49a18-149">บรรจุแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="49a18-149">Partially Packed</span></span>
    - <span data-ttu-id="49a18-150">จัดส่งสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="49a18-150">Shipped</span></span>
    - <span data-ttu-id="49a18-151">จัดส่งแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="49a18-151">Partially Shipped</span></span>
    - <span data-ttu-id="49a18-152">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="49a18-152">Partially Invoiced</span></span>
    - <span data-ttu-id="49a18-153">ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="49a18-153">Cancelled</span></span>

<span data-ttu-id="49a18-154">การตั้งค่า **มีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น** จะใช้ในสถานการณ์จำลองอื่นใบสั่งขายอื่น (การซิงค์จาก Sales ไปยัง Finance and Operation) เพื่อติดตามว่าใบสั่งขายถูกสร้างขึ้นจาก **ผลิตภัณฑ์รักษาไว้สำหรับภายนอก** ทั้งหมด ในกรณีที่ผลิตภัณฑ์ได้รับการรักษาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="49a18-155">ลักษณะการทำงานนี้ช่วยรับประกันว่า คุณจะไม่พยายามซิงโครไนส์รายการในใบสั่งขายที่มีผลิตภัณฑ์ที่ไม่รู้จักใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="49a18-156">ปุ่ม **สร้างใบแจ้งหนี้**, **ยกเลิกใบสั่ง**, **คำนวณใหม่**, **เรียกดูผลิตภัณฑ์** และ **ค้นหาที่อยู่** บนหน้า **ใบสั่งขาย** ถูกซ่อนไว้สำหรับใบสั่งที่รักษาไว้สำหรับภายนอกเนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="49a18-157">หน้าใบสั่งจะไม่สามารถแก้ไขได้เนื่องจากข้อมูลในใบสั่งจะถูกซิงค์จาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="49a18-158">**สถานะของใบสั่งขาย** จะยังคงใช้งานอยู่เพื่อให้แน่ใจว่าการเปลี่ยนแปลงจาก Finance and Operations สามารถดำเนินไปยัง **ใบสั่งขาย** ใน Sales ได้</span><span class="sxs-lookup"><span data-stu-id="49a18-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="49a18-159">ซึ่งจะถูกควบคุมโดยการตั้งค่า **Statecode [สถานะ]** เริ่มต้นเป็น **ที่ใช้งานอยู่** ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49a18-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="49a18-160">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="49a18-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="49a18-161">ก่อนที่จะซิงค์ใบสั่งขาย จำเป็นต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49a18-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="49a18-162">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-162">Setup in Sales</span></span>

- <span data-ttu-id="49a18-163">ให้สิทธิ์สำหรับทีมงานที่ผู้ใช้ (จาก **การตั้งค่าการเชื่อมต่อ** ของ Sales ของคุณ) ถูกกำหนดให้</span><span class="sxs-lookup"><span data-stu-id="49a18-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="49a18-164">ถ้าคุณกำลังใช้ข้อมูลสาธิต โดยปกติผู้ใช้จะสามารถเข้าใช้ได้ แต่ทีมงานจะไม่สามารถเข้าใช้ได้</span><span class="sxs-lookup"><span data-stu-id="49a18-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="49a18-165">หากไม่มีสิ่งนี้ คุณจะได้รับข้อผิดพลาดที่แสดงว่าทีมงานหลักหายไปเมื่อรันโครงการจากตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49a18-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="49a18-166">ภายใต้ **การตั้งค่า** > **ความปลอดภัย** > **ทีมงาน** เลือกทีมงานที่เกี่ยวข้อง คลิก **จัดการบทบาท** และเลือกบทบาทที่มีสิทธิ์ที่เหมาะสม เช่น ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="49a18-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="49a18-167">ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="49a18-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="49a18-168">ภายใต้ **การตั้งค่า** > **การจัดการ** > **การตั้งค่าระบบ** > **การขาย** ให้แน่ใจว่า **วิธีการคำนวณส่วนลด** ถูกตั้งค่าเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="49a18-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="49a18-169">ตั้งค่าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="49a18-170">ตั้งค่า **การขายและการตลาด** > **งานประจำงวด** > **คำนวณยอดขายรวม** เพื่อรันเป็นชุดงานที่มีการตั้งค่า **คำนวณยอดรวมสำหรับใบสั่งขาย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="49a18-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="49a18-171">สิ่งนี้เป็นสิ่งสำคัญเนื่องจากเฉพาะใบสั่งขายที่มีการคำนวณยอดขายรวมเท่านั้นที่จะถูกซิงค์ไปยัง CDS และ Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="49a18-172">ความถี่ของชุดงานควรถูกปรับให้เข้ากับความถี่ของการซิงโครไนส์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="49a18-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="49a18-173">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49a18-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="49a18-174">งาน SalesHeader</span><span class="sxs-lookup"><span data-stu-id="49a18-174">SalesHeader task</span></span>

- <span data-ttu-id="49a18-175">อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS ใน ต้นทาง** > **CDS**</span><span class="sxs-lookup"><span data-stu-id="49a18-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="49a18-176">ค่าเท็มเพลตเริ่มต้นสำหรับ **Account_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="49a18-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="49a18-177">ค่าเท็มเพลตเริ่มต้นสำหรับ **InvoiceAccount_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="49a18-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="49a18-178">ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="49a18-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="49a18-179">ให้แน่ใจว่าการแม็ปที่จำเป็นมีอยู่ใน **ต้นทาง** > **CDS สำหรับ InvoiceCountryRegionId ไปยัง BillingAddress_Country** และสำหรับ **DeliveryCountryRegionId ไปยัง DeliveryAddress_Country**</span><span class="sxs-lookup"><span data-stu-id="49a18-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="49a18-180">ค่าเท็มเพลตคือ **ValueMap** โดยมีประเทศต่าง ๆ จำนวนมากถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="49a18-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="49a18-181">จำเป็นต้องใช้ **รายการราคา** เพื่อสร้างใบสั่งใน Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="49a18-182">อัพเดต **ValueMap** ใน **CDS** > **ปลายทาง** สำหรับ **pricelevelid.name [ชื่อรายการราคา]** ไปยัง **รายการราคา** ที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="49a18-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="49a18-183">คุณสามารถใช้ค่าเริ่มต้น **รายการราคา** สำหรับสกุลเงินเดียวหรือใช้ **ValueMap** ถ้าคุณมี **รายการราคา** ในสกุลเงินหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="49a18-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="49a18-184">ค่าเท็มเพลตเริ่มต้นสำหรับ **pricelevelid.name [ชื่อรายการราคา]** คือ CRM Service USA (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="49a18-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="49a18-185">งาน SalesLine</span><span class="sxs-lookup"><span data-stu-id="49a18-185">SalesLine task</span></span>

- <span data-ttu-id="49a18-186">อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS ใน ต้นทาง** > **CDS**</span><span class="sxs-lookup"><span data-stu-id="49a18-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="49a18-187">เท็มเพลตเริ่มต้นสำหรับ **SalesOrder_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="49a18-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="49a18-188">ค่าเท็มเพลตเริ่มต้นสำหรับ **Product_Organization_OrganizationId** คือ ORG001</span><span class="sxs-lookup"><span data-stu-id="49a18-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="49a18-189">ให้แน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่ใน **ต้นทาง** > **CDS** สำหรับ **DeliveryCountryRegionId** ไปยัง **DeliveryAddress_Country**</span><span class="sxs-lookup"><span data-stu-id="49a18-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="49a18-190">ค่าเท็มเพลตคือ **ValueMap** โดยมีประเทศต่าง ๆ จำนวนมากถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="49a18-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="49a18-191">ให้แน่ใจว่า **ValueMap** ที่จำเป็นสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่ใน **ต้นทาง** > **การแม็ป CDS**</span><span class="sxs-lookup"><span data-stu-id="49a18-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="49a18-192">ค่าเท็มเพลตที่มี **ValueMap** ถูกกำหนดสำหรับ **SalesUnitSymbol ให้กับ Quantity_UOM**</span><span class="sxs-lookup"><span data-stu-id="49a18-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="49a18-193">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49a18-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="49a18-194">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49a18-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="49a18-195">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="49a18-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="49a18-196">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49a18-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="49a18-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="49a18-197">OrderHeader</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="49a18-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="49a18-200">OrderLine</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="49a18-203">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="49a18-203">Related topics</span></span>

[<span data-ttu-id="49a18-204">ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="49a18-205">ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="49a18-206">ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="49a18-207">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49a18-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="49a18-208">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="49a18-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


