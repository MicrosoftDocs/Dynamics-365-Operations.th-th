--- 
title: "สร้างใบแจ้งหนี้สำหรับใบสั่งขาย"
description: "คู่มือของงานนี้อธิบายถึงการออกใบแจ้งหนี้ใบสั่งขาย รวมถึงการผสานใบแจ้งหนี้และการประมวลผลชุดงาน "
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 928fed092bdb49fcea68c488346482da5a986e5a
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="63eaa-103">สร้างใบแจ้งหนี้สำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="63eaa-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63eaa-104">คู่มือของงานนี้อธิบายถึงการออกใบแจ้งหนี้ใบสั่งขาย รวมถึงการผสานใบแจ้งหนี้และการประมวลผลชุดงาน </span><span class="sxs-lookup"><span data-stu-id="63eaa-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="63eaa-105">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="63eaa-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="63eaa-106">สร้างใบแจ้งหนี้จากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="63eaa-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="63eaa-107">ไปที่ บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อที่จัดส่งสินค้าแล้วแต่ไม่ได้ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="63eaa-108">เลือกใบสั่งขายจากรายการ</span><span class="sxs-lookup"><span data-stu-id="63eaa-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="63eaa-109">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="63eaa-110">คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-110">Click Invoice.</span></span>
    * <span data-ttu-id="63eaa-111">โปรดทราบว่า ใบสั่งขายนี้มีหลายบันทึกการจัดส่งมาเชื่อมโยงด้วย </span><span class="sxs-lookup"><span data-stu-id="63eaa-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="63eaa-112">ซึ่งจะแสดงเฉพาะคำ <multiple> หลากหลาย แทนที่จะเป็นหมายเลขบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="63eaa-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="63eaa-113">ขยายส่วน พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="63eaa-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="63eaa-114">ต้องตั้งค่าการลงรายการบัญชีเป็น ใช่ เพื่อลงรายการบัญชีใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="63eaa-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="63eaa-115">คุณสามารถปิดการลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="63eaa-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="63eaa-116">อย่างไรก็ตาม คุณสามารถได้ผลลัพธ์เดียวกันจากการสร้างใบแจ้งหนี้ชั่วคราวแทนที่การสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="63eaa-117">ตัวเลือกนี้ใช้สำหรับชุดงาน</span><span class="sxs-lookup"><span data-stu-id="63eaa-117">This option is used for batch jobs.</span></span> <span data-ttu-id="63eaa-118">แบบสอบถามจะรันเมื่อชุดงานรัน</span><span class="sxs-lookup"><span data-stu-id="63eaa-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="63eaa-119">ในฟิลด์การพิมพ์ ให้เลือก 'หลังจาก'</span><span class="sxs-lookup"><span data-stu-id="63eaa-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="63eaa-120">เลือก ใช่ สำหรับการพิมพ์ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="63eaa-121">การจัดการการพิมพ์สามารถพิมพ์หลายสำเนาของใบแจ้งหนี้ได้ และยังส่งใบแจ้งหนี้ผ่านทางอีเมลเป็นไฟล์ PDF ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="63eaa-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="63eaa-122">ในฟิลด์ค่ารรมเนียมการพิมพ์ ให้เลือก 'สรุป'</span><span class="sxs-lookup"><span data-stu-id="63eaa-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="63eaa-123">ในฟิลด์การตรวจสอบวงเงินสินเชื่อ ให้เลือก 'ยอดดุล'</span><span class="sxs-lookup"><span data-stu-id="63eaa-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="63eaa-124">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="63eaa-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="63eaa-125">รวมใบสั่งต่างๆเป็นใบแจ้งหนี้ใบเดียว</span><span class="sxs-lookup"><span data-stu-id="63eaa-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="63eaa-126">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="63eaa-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="63eaa-127">ค้นหาลูกค้าที่มีหลายใบแจ้งหนี้ที่เปิดค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="63eaa-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="63eaa-128">เลือกใบสั่งขายที่เปิดค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="63eaa-128">Select an open sales order.</span></span>
4. <span data-ttu-id="63eaa-129">เลือกใบสั่งขายที่เปิดค้างอยู่อีกใบหนึ่งสำหรับลูกค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="63eaa-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="63eaa-130">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="63eaa-131">คลิกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-131">Click Invoice.</span></span>
7. <span data-ttu-id="63eaa-132">ขยายส่วน พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="63eaa-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="63eaa-133">ในฟิลด์ ปริมาณ ให้เลือก 'ทั้งหมด'</span><span class="sxs-lookup"><span data-stu-id="63eaa-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="63eaa-134">หมายเหตุว่า มีใบแจ้งหนี้สองใบแสดงอยู่ในส่วนภาพรวม </span><span class="sxs-lookup"><span data-stu-id="63eaa-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="63eaa-135">ขณะนี้ให้ผสานสองใบนั้นให้กลายเป็นใบแจ้งหนี้เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="63eaa-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="63eaa-136">ในฟิลด์อัพเดตบทสรุปสำหรับ ให้เลือก 'บัญชีใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="63eaa-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="63eaa-137">คลิกการเตรียมการผสานใบสั่งขายหลายใบให้เป็นใบแจ้งหนี้เดี่ยว</span><span class="sxs-lookup"><span data-stu-id="63eaa-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="63eaa-138">ใบสั่งขายสองใบขณะนี้ได้ถูกผสานไว้ในใบแจ้งหนี้เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="63eaa-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="63eaa-139">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="63eaa-139">Click Cancel.</span></span>
12. <span data-ttu-id="63eaa-140">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="63eaa-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="63eaa-141">ลงรายการบัญชีใบแจ้งหนี้ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="63eaa-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="63eaa-142">ไปที่ บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ชุดงาน > ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63eaa-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="63eaa-143">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="63eaa-143">Click Select.</span></span>
3. <span data-ttu-id="63eaa-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="63eaa-144">Click OK.</span></span>
4. <span data-ttu-id="63eaa-145">คลิกชุดงาน</span><span class="sxs-lookup"><span data-stu-id="63eaa-145">Click Batch.</span></span>
5. <span data-ttu-id="63eaa-146">คลิกที่ ใช่ เพื่อเปิดใช้งานการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="63eaa-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="63eaa-147">การเกิดซ้ำ </span><span class="sxs-lookup"><span data-stu-id="63eaa-147">Click Recurrence.</span></span>
7. <span data-ttu-id="63eaa-148">เลือกวัน</span><span class="sxs-lookup"><span data-stu-id="63eaa-148">Select Days</span></span>
8. <span data-ttu-id="63eaa-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="63eaa-149">Click OK.</span></span>
9. <span data-ttu-id="63eaa-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="63eaa-150">Click OK.</span></span>
10. <span data-ttu-id="63eaa-151">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="63eaa-151">Click Cancel.</span></span>
11. <span data-ttu-id="63eaa-152">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="63eaa-152">Click Yes.</span></span>


