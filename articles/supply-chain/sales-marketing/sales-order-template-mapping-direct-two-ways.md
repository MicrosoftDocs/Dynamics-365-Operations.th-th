---
title: "การซิงโครไนส์ของใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Microsoft Dynamics 365 for Sales และ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition"
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2017
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
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 19f2c5200d222b2bbff7119c2de2e2e138ca64e6
ms.contentlocale: th-th
ms.lasthandoff: 01/19/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a><span data-ttu-id="d3768-103">การซิงโครไนส์ของใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-103">Synchronization of sales orders directly between Sales and Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d3768-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Microsoft Dynamics 365 for Sales และ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="d3768-104">The topic discusses the templates and underlying tasks that are used to run synchronization of sales orders directly between Microsoft Dynamics 365 for Sales and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d3768-105">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="d3768-105">Templates and tasks</span></span>

<span data-ttu-id="d3768-106">เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="d3768-106">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="d3768-107">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="d3768-107">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d3768-108">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="d3768-108">The following templates and underlying tasks are used to run synchronization of sales orders directly between Sales and Finance and Operations:</span></span>

- <span data-ttu-id="d3768-109">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="d3768-109">**Names of the templates in Data integration:**</span></span> 

    - <span data-ttu-id="d3768-110">ใบสั่งขาย (Sales ไปยัง Fin and Ops) - ตรง</span><span class="sxs-lookup"><span data-stu-id="d3768-110">Sales Orders (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="d3768-111">ใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="d3768-111">Sales Orders (Fin and Ops to Sales) - Direct</span></span>

- <span data-ttu-id="d3768-112">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="d3768-112">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="d3768-113">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="d3768-113">OrderHeader</span></span>
    - <span data-ttu-id="d3768-114">OrderLine</span><span class="sxs-lookup"><span data-stu-id="d3768-114">OrderLine</span></span>

<span data-ttu-id="d3768-115">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ของส่วนหัวและรายการของใบแจ้งหนี้การขายได้:</span><span class="sxs-lookup"><span data-stu-id="d3768-115">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="d3768-116">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="d3768-116">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="d3768-117">บัญชี (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="d3768-117">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="d3768-118">ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="d3768-118">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="d3768-119">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="d3768-119">Entity set</span></span>

| <span data-ttu-id="d3768-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-120">Finance and Operations</span></span>  | <span data-ttu-id="d3768-121">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d3768-121">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="d3768-122">ส่วนหัวของใบสั่งขาย CDS</span><span class="sxs-lookup"><span data-stu-id="d3768-122">CDS sales order headers</span></span> | <span data-ttu-id="d3768-123">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="d3768-123">SalesOrders</span></span>       |
| <span data-ttu-id="d3768-124">รายการในใบสั่งขาย CDS</span><span class="sxs-lookup"><span data-stu-id="d3768-124">CDS sales order lines</span></span>   | <span data-ttu-id="d3768-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="d3768-125">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d3768-126">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="d3768-126">Entity flow</span></span>

<span data-ttu-id="d3768-127">มีการสร้างใบสั่งขายใน Sales และมีการซิงโครไนส์ไปยัง Finance and Operations เมื่อมีการทริกเกอร์ **รันโครงการ** สำหรับโครงการที่ขึ้นกับเท็มเพลต **ใบสั่งขาย (Sales ไปยัง Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="d3768-127">Sales orders are created in Sales and synchronized to Finance and Operations when **Run project** is triggered for a project based on the **Sales Orders (Sales to Fin and Ops) - Direct** template.</span></span> <span data-ttu-id="d3768-128">คุณสามารถเรียกใช้และซิงโครไนส์ใบสั่งขายจาก Sales ได้เท่านั้น เมื่อ **สั่งซื้อผลิตภัณฑ์** ประกอบด้วยผลิตภัณฑ์ที่ถูกจัดเก็บอยู่ภายนอก</span><span class="sxs-lookup"><span data-stu-id="d3768-128">You can only activate and synchronize orders from Sales if all **Order Products** consist of products that are externally maintained.</span></span> <span data-ttu-id="d3768-129">ดังนั้น จึงอาจไม่มีผลิตภัณฑ์ที่เขียนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d3768-129">Therefore, there can be no write-in products.</span></span> <span data-ttu-id="d3768-130">หลังจากที่มีการเรียกใช้ใบสั่ง ใบสั่งขายกลายเป็นแบบอ่านอย่างเดียวในอินเทอร์เฟสผู้ใช้ (UI)</span><span class="sxs-lookup"><span data-stu-id="d3768-130">After the order is activated, the sales order becomes read-only in the user interface (UI).</span></span> <span data-ttu-id="d3768-131">ณ จุดนั้น โปรแกรมปรับปรุงถูกสร้างจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-131">At that point, the updates are made from Finance and Operations.</span></span> <span data-ttu-id="d3768-132">หลังจากที่ใบสั่งขายที่มีสถานะเป็น **ยืนยันแล้ว** โครงการที่ขึ้นกับเท็มเพลต **ใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง** สามารถถูกใช้ในการซิงโครไนส์การอัพเดตหรือสถานะการเติมสินค้าจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-132">After the sales order has a status of **Confirmed**, the a project based on the **Sales Orders (Fin and Ops to Sales) - Direct** template can be used to synchronize updates or fulfillment status from Finance and Operations to Sales.</span></span>

<span data-ttu-id="d3768-133">คุณไม่ต้องสร้างใบสั่งใน Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-133">You don't have to create orders in Sales.</span></span> <span data-ttu-id="d3768-134">คุณสามารถสร้างใบสั่งขายใหม่ขึ้นได้ใน Finance and Operations แทน</span><span class="sxs-lookup"><span data-stu-id="d3768-134">You can create new sales orders in Finance and Operations instead.</span></span> <span data-ttu-id="d3768-135">หลังจากที่ใบสั่งขายที่มีสถานะเป็น **ยืนยันแล้ว** จะถูกซิงโครไนส์กับการขายตามที่อธิบายไว้ในย่อหน้าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d3768-135">After a sales order has a status of **Confirmed**, it's synchronized to Sales as described in the previous paragraph.</span></span>

<span data-ttu-id="d3768-136">ใน Finance and Operations ตัวกรองในเท็มเพลตช่วยรับรองว่า เฉพาะใบสั่งขายที่เกี่ยวข้องเท่านั้นจะถูกรวมอยู่ในการซิงโครไนส์:</span><span class="sxs-lookup"><span data-stu-id="d3768-136">In Finance and operations, filters in the template help guarantee that only the relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="d3768-137">ในใบสั่งขาย ทั้งลูกค้าที่สั่งซื้อและที่ออกใบแจ้งหนี้ต้องมีต้นกำเนิดมาจาก Sales ที่จะถูกรวมอยู่ในการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="d3768-137">On the sales order, both the ordering customer and the invoicing customer have to originate from Sales to be included in the synchronization.</span></span> <span data-ttu-id="d3768-138">ใน Finance and Operations ฟิลด์ **OrderingCustomerIsExternallyMaintained** และ **InvoiceCustomerIsExternallyMaintained** ถูกใช้ในการกรองใบสั่งขายจากเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3768-138">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to filter sales orders from the data entities.</span></span>
- <span data-ttu-id="d3768-139">ใบสั่งขายใน Finance and Operations ต้องได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="d3768-139">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="d3768-140">เฉพาะใบสั่งขายที่ยืนยันแล้วหรือใบสั่งขายที่มีสถานะการประมวลผลสูง เช่น **จัดส่งแล้ว** หรือ **ออกใบแจ้งหนี้แล้ว** จะถูกซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-140">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="d3768-141">หลังจากสร้างหรือปรับเปลี่ยนใบสั่งขาย ชุดงาน **คำนวณยอดขายรวม** ใน Finance and Operations จะต้องถูกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d3768-141">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="d3768-142">ใบสั่งขายที่ซึ่งยอดขายรวมถูกคำนวณเท่านั้น จะถูกซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-142">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

## <a name="freight-tax"></a><span data-ttu-id="d3768-143">อัตราภาษีค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="d3768-143">Freight tax</span></span>

<span data-ttu-id="d3768-144">Sales ไม่สนับสนุนภาษีที่ระดับส่วนหน้า เนื่องจากมีการจัดเก็บภาษีในระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="d3768-144">Sales doesn't support tax at the header level, because tax is stored at the line level.</span></span> <span data-ttu-id="d3768-145">เพื่อสนับสนุนภาษีที่ระดับส่วนหน้าจาก Finance and Operations เช่น ภาษีในค่าขนส่ง ระบบจะซิงโครไนส์ภาษีไปยัง Sales เป็นผลิตภัณฑ์เขียนเพิ่มที่ชื่อ **ภาษีค่าขนส่ง** และที่มียอดภาษีจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-145">To support tax at the header level from Finance and Operations, such as tax on freight, the system synchronizes tax to Sales as a write-in product that is named **Freight Tax**, and that has the tax amount from Finance and Operations.</span></span> <span data-ttu-id="d3768-146">ด้วยวิธีนี้ การคำนวณราคามาตรฐานใน Sales สามารถถูกใช้สำหรับผลรวมได้ แม้ว่าจะมีภาษีที่ระดับส่วนหน้าจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-146">In this way, the standard price calculation in Sales can be used for totals, even when there is tax at the header level from Finance and Operations.</span></span>

## <a name="discount-calculation-and-rounding"></a><span data-ttu-id="d3768-147">การคำนวณส่วนลดและการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="d3768-147">Discount calculation and rounding</span></span>

<span data-ttu-id="d3768-148">รูปแบบการคำนวณส่วนลดใน Sales แตกต่างจากแบบจำลองการคำนวณส่วนลดใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-148">The discount calculation model in Sales differs from the discount calculation model in Finance and Operations.</span></span> <span data-ttu-id="d3768-149">ใน Finance and Operations ยอดส่วนลดขั้นสุดท้ายในรายการขายอาจเป็นผลของชุดของเปอร์เซ็นต์ส่วนลดและยอดส่วนลด</span><span class="sxs-lookup"><span data-stu-id="d3768-149">In Finance and Operations, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="d3768-150">ถ้ายอดเงินส่วนลดขั้นสุดท้ายนี้ถูกหารด้วยปริมาณในรายการ การปัดเศษสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="d3768-150">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="d3768-151">อย่างไรก็ตาม การปัดเศษนี้จะไม่ถูกพิจารณา หากยอดส่วนลดที่ถูกปัดเศษถูกซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-151">However, this rounding isn't considered if a rounded per-unit discount amount is synchronized to Sales.</span></span> <span data-ttu-id="d3768-152">เพื่อช่วยรับรองว่า ยอดเงินส่วนลดทั้งหมดจากรายการขายใน Finance and Operations ถูกซิงโครไนส์กับ Sales อย่างถูกต้อง ยอดเงินเต็มจำนวนต้องถูกซิงโครไนส์โดยไม่มีการหารด้วยปริมาณสำหรับรายการ</span><span class="sxs-lookup"><span data-stu-id="d3768-152">To help guarantee that the full discount amount from a sales line in Finance and Operations is correctly synchronized to Sales, the full amount must be synchronized without being divided by the line quantity.</span></span> <span data-ttu-id="d3768-153">ดังนั้น คุณต้องกำหนด **วิธีการคำนวณส่วนลด** เป็น **สินค้าในรายการ** ใน Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-153">Therefore, you must define the **Discount calculation method** as **Line item** in Sales.</span></span>

<span data-ttu-id="d3768-154">เมื่อมีการซิงโครไนส์รายการใบสั่งขายจาก Sales ไปยัง Finance and Operations จะมีการใช้ยอดส่วนลดในรายการเต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="d3768-154">When a sales order line is synchronized from Sales to Finance and Operations, the full line discount amount is used.</span></span> <span data-ttu-id="d3768-155">เนื่องจาก Finance and Operations ไม่มีฟิลด์ที่สามารถจัดเก็บยอดส่วนลดเต็มจำนวนสำหรับรายการได้ ปริมาณถูกหารด้วยปริมาณและจัดเก็บไว้ในฟิลด์ **ส่วนลดต่อรายการ**</span><span class="sxs-lookup"><span data-stu-id="d3768-155">Because Finance and Operations has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="d3768-156">การปัดเศษใดๆ ที่เกิดขึ้นระหว่างการหารนี้ จะถูกจัดเก็บในฟิลด์ **ค่าธรรมเนียมการขาย** ในรายการขาย</span><span class="sxs-lookup"><span data-stu-id="d3768-156">Any rounding that occurs in this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example"></a><span data-ttu-id="d3768-157">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d3768-157">Example</span></span>

<span data-ttu-id="d3768-158">**การซิงโครไนส์จาก Sales ไปยัง Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="d3768-158">**Synchronization from Sales to Finance and Operations**</span></span>

- <span data-ttu-id="d3768-159">**Sales:** ปริมาณ = 3 ส่วนลดต่อรายการ = $10.00</span><span class="sxs-lookup"><span data-stu-id="d3768-159">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
- <span data-ttu-id="d3768-160">**Finance and Operations:**ปริมาณ = 3 ยอดเงินส่วนลดต่อรายการ = $3.33 ค่าธรรมเนียมการขาย =-$0.01</span><span class="sxs-lookup"><span data-stu-id="d3768-160">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span> 

<span data-ttu-id="d3768-161">**การซิงโครไนส์จาก Finance and Operations ไปยัง Sales**</span><span class="sxs-lookup"><span data-stu-id="d3768-161">**Synchronization from Finance and Operations to Sales**</span></span>

- <span data-ttu-id="d3768-162">**Finance and Operations:**ปริมาณ = 3 ยอดเงินส่วนลดต่อรายการ = $3.33 ค่าธรรมเนียมการขาย =-$0.01</span><span class="sxs-lookup"><span data-stu-id="d3768-162">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span>
- <span data-ttu-id="d3768-163">**Sales:** ปริมาณ = 3 ส่วนลดต่อรายการ = (3 × $3.33) + $0.01 = $10.00</span><span class="sxs-lookup"><span data-stu-id="d3768-163">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d3768-164">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-164">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="d3768-165">ฟิลด์ใหม่ได้ถูกเพิ่มลงในเอนทิตี้ **ใบสั่ง** และแสดงขึ้นบนหน้า:</span><span class="sxs-lookup"><span data-stu-id="d3768-165">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="d3768-166">**ถูกรักษาไว้ภายนอก** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เมื่อใบสั่งมาจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-166">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="d3768-167">**สถานะการประมวลผล** – ฟิลด์นี้แสดงสถานะการประมวลผลใบสั่งใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-167">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="d3768-168">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d3768-168">The following values are available:</span></span>

    - <span data-ttu-id="d3768-169">**ร่าง** – สถานะเริ่มต้นเมื่อใบสั่งถูกสร้างขึ้นใน Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-169">**Draft** – The initial status when an order is created in Sales.</span></span> <span data-ttu-id="d3768-170">ใน Sales เฉพาะใบสั่งที่มีสถานะการประมวลผลนี้เท่านั้นสามารถถูกแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="d3768-170">In Sales, only orders with this processing status can be edited.</span></span>
    - <span data-ttu-id="d3768-171">**เปิดใช้งาน** – สถานะหลังจากใบสั่งถูกเรียกใช้ใน Sales โดยการใช้ปุ่ม **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="d3768-171">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    - <span data-ttu-id="d3768-172">**วันที่ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="d3768-172">**Confirmed**</span></span>
    - <span data-ttu-id="d3768-173">**บันทึกการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="d3768-173">**Packing Slip**</span></span>
    - <span data-ttu-id="d3768-174">**ออกใบแจ้งหนี้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="d3768-174">**Invoiced**</span></span>
    - <span data-ttu-id="d3768-175">**เบิกสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="d3768-175">**Picked**</span></span>
    - <span data-ttu-id="d3768-176">**เบิกสินค้าแล้วบางส่วน**</span><span class="sxs-lookup"><span data-stu-id="d3768-176">**Partially Picked**</span></span>
    - <span data-ttu-id="d3768-177">**บรรจุแล้วบางส่วน**</span><span class="sxs-lookup"><span data-stu-id="d3768-177">**Partially Packed**</span></span>
    - <span data-ttu-id="d3768-178">**จัดส่งสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="d3768-178">**Shipped**</span></span>
    - <span data-ttu-id="d3768-179">**จัดส่งแล้วบางส่วน**</span><span class="sxs-lookup"><span data-stu-id="d3768-179">**Partially Shipped**</span></span>
    - <span data-ttu-id="d3768-180">**ออกใบแจ้งหนี้แล้วบางส่วน**</span><span class="sxs-lookup"><span data-stu-id="d3768-180">**Partially Invoiced**</span></span>
    - <span data-ttu-id="d3768-181">**ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="d3768-181">**Cancelled**</span></span>

<span data-ttu-id="d3768-182">การตั้งค่า **มีเฉพาะผลิตภัณฑ์ที่รักษาไว้ภายนอก** ถูกใช้ในระหว่างการเรียกใช้ใบสั่ง เพื่อติดตามได้อย่างสม่ำเสมอว่าใบสั่งขายประกอบด้วยผลิตภัณฑ์ที่รักษาไว้ภายนอกทั้งหมดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d3768-182">The **Has Externally Maintained Products Only** setting is used during order activation to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="d3768-183">ถ้าใบสั่งขายประกอบด้วยผลิตภัณฑ์ที่รักษาไว้ภายนอกทั้งหมด ผลิตภัณฑ์จะมีการจัดเก็บอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-183">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="d3768-184">การตั้งค่าระบบนี้ช่วยรับประกันว่า คุณจะไม่เรียกใช้และพยายามที่จะซิงโครไนส์รายการใบสั่งขายที่มีผลิตภัณฑ์ที่ไม่รู้จักใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-184">This setting helps guarantee that you don't activate and try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="d3768-185">ปุ่ม **สร้างใบแจ้งหนี้** **ยกเลิกใบสั่ง** **คำนวณใหม่** **เรียกดูผลิตภัณฑ์** และ **ค้นหาที่อยู่** บนหน้า **ใบสั่งขาย** ถูกซ่อนไว้สำหรับใบสั่งที่รักษาไว้ภายนอก เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-185">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="d3768-186">ใบสั่งเหล่านี้จะไม่สามารถถูกแก้ไขได้ เนื่องจากข้อมูลในใบสั่งขายจะถูกซิงโครไนส์จาก Finance and Operations หลังจากการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="d3768-186">These orders can't be edited, because sales order information will be synchronized from Finance and Operations after activation.</span></span>

<span data-ttu-id="d3768-187">สถานะของใบสั่งขายจะยังคง **ใช้งานอยู่** เพื่อช่วยรับประกันว่า การเปลี่ยนแปลงจาก Finance and Operations สามารถดำเนินไปยังใบสั่งขายใน Sales ได้</span><span class="sxs-lookup"><span data-stu-id="d3768-187">The sales order status will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="d3768-188">เพื่อควบคุมลักษณะการทำงานนี้ ตั้งค่าค่า **Statecode \[สถานะ\]** เริ่มต้น เป็น **ใช้งานอยู่** ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3768-188">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d3768-189">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="d3768-189">Preconditions and mapping setup</span></span>

<span data-ttu-id="d3768-190">ก่อนที่คุณจะซิงโครไนส์ใบสั่งขาย จำเป็นที่คุณต้องปรับปรุงการตั้งค่าต่อไปนี้ในระบบ:</span><span class="sxs-lookup"><span data-stu-id="d3768-190">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="d3768-191">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-191">Setup in Sales</span></span>

- <span data-ttu-id="d3768-192">ต้องแน่ใจว่ามีการตั้งค่าสิทธิ์สำหรับทีมงานที่ผู้ใช้จากชุดการเชื่อมต่อของคุณใน Sales ถูกกำหนดให้</span><span class="sxs-lookup"><span data-stu-id="d3768-192">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="d3768-193">ถ้าคุณกำลังใช้ข้อมูลสาธิต โดยปกติผู้ใช้จะมีการเข้าถึงของผู้ดูแลระบบ แต่ทีมงานจะไม่มีการเข้าถึงของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="d3768-193">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="d3768-194">ถ้าทีมงานไม่มีการเข้าถึงของผู้ดูแลระบบ เมื่อคุณรันโครงการจากการรวมข้อมูล คุณจะได้รับข้อความแสดงข้อผิดพลาดที่แจ้งว่า หลักทีมงานขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="d3768-194">If the team doesn't have admin access, when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="d3768-195">ไปที่ **การตั้งค่า** &gt; **ความปลอดภัย** &gt; **ทีมงาน** เลือกทีมที่เกี่ยวข้อง เลือก **จัดการบทบาท** และเลือกบทบาทที่มีสิทธิ์ที่เหมาะสม เช่น **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="d3768-195">Go to **Settings** &gt; **Security** &gt; **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="d3768-196">ไปยัง **การตั้งค่า** &gt; **การจัดการ** &gt; **การตั้งค่าระบบ** &gt; **Sales** และต้องมั่นใจว่ามีใช้การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d3768-196">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="d3768-197">ตัวเลือก **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d3768-197">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="d3768-198">ฟิลด์ **วิธีการคำนวณส่วนลด** ถูกกำหนดเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="d3768-198">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="d3768-199">ตั้งค่าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3768-199">Setup in Finance and Operations</span></span>

- <span data-ttu-id="d3768-200">ไปยัง **การขายและการตลาด** &gt; **งานประจำงวด** &gt; **คำนวณยอดขายรวม** และตั้งค่างานที่จะรันเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d3768-200">Go to **Sales and marketing** &gt; **Periodic tasks** &gt; **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="d3768-201">ตั้งค่าตัวเลือก **คำนวณผลรวมสำหรับใบสั่งขาย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d3768-201">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="d3768-202">ขั้นตอนนี้สำคัญ เนื่องจากเฉพาะใบสั่งขายที่ซึ่งยอดขายรวมถูกคำนวณ จะถูกซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-202">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="d3768-203">ความถี่ของชุดงานควรถูกปรับให้เข้ากับความถี่ของการซิงโครไนส์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d3768-203">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a><span data-ttu-id="d3768-204">การตั้งค่าในใบสั่งขาย (Sales ไปยัง Fin and Ops) - โครงการการรวมข้อมูลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="d3768-204">Setup in the Sales Orders (Sales to Fin and Ops) - Direct Data integration project</span></span>

- <span data-ttu-id="d3768-205">ต้องแน่ใจว่าการแม็ปที่ต้องการ มีอยู่สำหรับ **Shipto\_country** ไปยัง **DeliveryAddressCountryRegionISOCode**</span><span class="sxs-lookup"><span data-stu-id="d3768-205">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="d3768-206">คุณสามารถทำให้ค่าเริ่มต้นว่างเปล่าได้ในแผนผังค่า เพื่อหลีกเลี่ยงการพิมพ์ประเทศสำหรับใบสั่งประจำชาติ</span><span class="sxs-lookup"><span data-stu-id="d3768-206">You can make blank a default value in the value map to avoid having to type country for national orders.</span></span> <span data-ttu-id="d3768-207">ตั้งค่าด้านซ้ายเป็น 'ว่าง' และตั้งค่าด้านขวาเป็นประเทศหรือภูมิภาคที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d3768-207">Set the left side to 'Blank', and set the right side to the desired country or region.</span></span>

    <span data-ttu-id="d3768-208">ค่าของเท็มเพลตคือ แผนผังค่าที่มีการแม็ปหลายประเทศหรือภูมิภาค และที่ซึ่ง 'ว่าง' = US</span><span class="sxs-lookup"><span data-stu-id="d3768-208">The template value is a value map where several countries or regions are mapped, and where 'Blank' = US.</span></span>

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a><span data-ttu-id="d3768-209">การตั้งค่าในใบสั่งขาย (Fin and Ops ไปยัง Sales) - โครงการการรวมข้อมูลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="d3768-209">Setup in the Sales Orders (Fin and Ops to Sales) - Direct Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="d3768-210">งาน SalesHeader</span><span class="sxs-lookup"><span data-stu-id="d3768-210">SalesHeader task</span></span>

- <span data-ttu-id="d3768-211">จำเป็นต้องใช้รายการราคาเพื่อสร้างใบสั่งใน Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-211">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="d3768-212">อัพเดตแผนผังค่าสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** ไปยังรายการราคาที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="d3768-212">Update the value map for **pricelevelid.name \[Price List Name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="d3768-213">คุณสามารถใช้รายการราคาเริ่มต้นสำหรับสกุลเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d3768-213">You can use the default price list for a single currency.</span></span> <span data-ttu-id="d3768-214">อีกทางหนึ่งคือ ถ้าคุณมีรายการราคาในหลายสกุลเงิน คุณสามารถใช้แผนผังค่าได้</span><span class="sxs-lookup"><span data-stu-id="d3768-214">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="d3768-215">ค่าเท็มเพลตเริ่มต้นสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** คือ **CRM Service USA (ตัวอย่าง)**</span><span class="sxs-lookup"><span data-stu-id="d3768-215">The default template value for **pricelevelid.name \[Price List Name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="d3768-216">งาน SalesLine</span><span class="sxs-lookup"><span data-stu-id="d3768-216">SalesLine task</span></span>

- <span data-ttu-id="d3768-217">ตรวจสอบให้แน่ใจว่าแผนผังค่าที่ต้องการสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d3768-217">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>
- <span data-ttu-id="d3768-218">ตรวจสอบให้แน่ใจว่า มีการกำหนดหน่วยที่จำเป็นใน Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-218">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="d3768-219">ค่าเท็มเพลตที่มีแผนผังค่าถูกกำหนดสำหรับ **SalesUnitSymbol** ไปยัง **oumid.name**</span><span class="sxs-lookup"><span data-stu-id="d3768-219">A template value that has a value map is defined for **SalesUnitSymbol** to **oumid.name**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d3768-220">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3768-220">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="d3768-221">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d3768-221">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="d3768-222">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="d3768-222">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="d3768-223">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3768-223">The following illustrations show an example of a template mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="d3768-224">การแม็ปแสดงว่าข้อมูลฟิลด์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations หรือจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="d3768-224">The mapping shows which field information will be synchronized from Sales to Finance and Operations, or from Finance and Operations to Sales.</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a><span data-ttu-id="d3768-225">ใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="d3768-225">Sales Orders (Fin and Ops to Sales) - Direct: OrderHeader</span></span>

<span data-ttu-id="d3768-226">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span><span class="sxs-lookup"><span data-stu-id="d3768-226">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a><span data-ttu-id="d3768-227">ใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง: OrderLine</span><span class="sxs-lookup"><span data-stu-id="d3768-227">Sales Orders (Fin and Ops to Sales) - Direct: OrderLine</span></span>

<span data-ttu-id="d3768-228">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span><span class="sxs-lookup"><span data-stu-id="d3768-228">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a><span data-ttu-id="d3768-229">ใบสั่งขาย (Sales ไปยัง Fin and Ops) - ตรง: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="d3768-229">Sales Orders (Sales to Fin and Ops) - Direct: OrderHeader</span></span>

<span data-ttu-id="d3768-230">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span><span class="sxs-lookup"><span data-stu-id="d3768-230">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a><span data-ttu-id="d3768-231">ใบสั่งขาย (Sales ไปยัง Fin and Ops) - ตรง: OrderLine</span><span class="sxs-lookup"><span data-stu-id="d3768-231">Sales Orders (Sales to Fin and Ops) - Direct: OrderLine</span></span>

<span data-ttu-id="d3768-232">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span><span class="sxs-lookup"><span data-stu-id="d3768-232">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3768-233">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="d3768-233">Related topics</span></span>

[<span data-ttu-id="d3768-234">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="d3768-234">Prospect to cash</span></span>](prospect-to-cash.md)

