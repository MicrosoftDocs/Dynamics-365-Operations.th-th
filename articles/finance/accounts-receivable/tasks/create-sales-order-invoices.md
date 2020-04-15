---
title: สร้างใบแจ้งหนี้สำหรับใบสั่งขาย
description: 'คู่มือของงานนี้อธิบายถึงการออกใบแจ้งหนี้ใบสั่งขาย รวมถึงการผสานใบแจ้งหนี้และการประมวลผลชุดงาน '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c504ef36f61613c7aa7db5a1e5ddba6e69cd7285
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140293"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="910fa-103">สร้างใบแจ้งหนี้สำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="910fa-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="910fa-104">คู่มือของงานนี้อธิบายถึงการออกใบแจ้งหนี้ใบสั่งขาย รวมถึงการผสานใบแจ้งหนี้และการประมวลผลชุดงาน </span><span class="sxs-lookup"><span data-stu-id="910fa-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="910fa-105">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="910fa-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="910fa-106">สร้างใบแจ้งหนี้จากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="910fa-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="910fa-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ใบสั่ง > ใบสั่งขายที่จัดส่งสินค้าแล้วแต่ยังไม่ได้ออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="910fa-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="910fa-108">เลือกใบสั่งขายจากรายการ</span><span class="sxs-lookup"><span data-stu-id="910fa-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="910fa-109">ใน **บานหน้าต่างการดำเนินการ** **คลิก ใบแจ้งหนี้ > สร้าง > ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="910fa-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="910fa-110">โปรดทราบว่า ใบสั่งขายนี้มีหลายบันทึกการจัดส่งมาเชื่อมโยงด้วย </span><span class="sxs-lookup"><span data-stu-id="910fa-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="910fa-111">ซึ่งจะแสดงเฉพาะคำ <multiple> หลากหลาย แทนที่จะเป็นหมายเลขบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="910fa-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="910fa-112">ขยายส่วน **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="910fa-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="910fa-113">ต้องตั้งค่าการลงรายการบัญชีเป็น ใช่ เพื่อลงรายการบัญชีใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="910fa-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="910fa-114">คุณสามารถปิดการลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="910fa-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="910fa-115">อย่างไรก็ตาม คุณสามารถได้ผลลัพธ์เดียวกันจากการสร้างใบแจ้งหนี้ชั่วคราวแทนที่การสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="910fa-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="910fa-116">ตัวเลือกนี้ใช้สำหรับชุดงาน</span><span class="sxs-lookup"><span data-stu-id="910fa-116">This option is used for batch jobs.</span></span> <span data-ttu-id="910fa-117">แบบสอบถามจะรันเมื่อชุดงานรัน</span><span class="sxs-lookup"><span data-stu-id="910fa-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="910fa-118">ในฟิลด์ **พิมพ์** ให้เลือก 'หลังจาก'</span><span class="sxs-lookup"><span data-stu-id="910fa-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="910fa-119">ให้เลือก **ใช่** สำหรับการ **พิมพ์ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="910fa-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="910fa-120">การจัดการการพิมพ์สามารถพิมพ์หลายสำเนาของใบแจ้งหนี้ได้ และยังส่งใบแจ้งหนี้ผ่านทางอีเมลเป็นไฟล์ PDF ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="910fa-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="910fa-121">ในฟิลด์ **ค่าธรรมเนียมการพิมพ์** ให้เลือก 'สรุป'</span><span class="sxs-lookup"><span data-stu-id="910fa-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="910fa-122">ในฟิลด์ **การตรวจสอบวงเงินสินเชื่อ** ให้เลือก 'ยอดดุล'</span><span class="sxs-lookup"><span data-stu-id="910fa-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="910fa-123">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="910fa-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="910fa-124">รวมใบสั่งต่างๆเป็นใบแจ้งหนี้ใบเดียว</span><span class="sxs-lookup"><span data-stu-id="910fa-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="910fa-125">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ใบสั่ง > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="910fa-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="910fa-126">ค้นหาลูกค้าที่มีหลายใบแจ้งหนี้ที่เปิดค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="910fa-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="910fa-127">เลือกใบสั่งขายที่เปิดค้างไว้หลายใบจากลูกค้ารายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="910fa-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="910fa-128">ใน **บานหน้าต่างการดำเนินการ** **คลิก ใบแจ้งหนี้ > สร้าง > ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="910fa-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="910fa-129">ขยายส่วน **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="910fa-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="910fa-130">ในฟิลด์ **ปริมาณ** ให้เลือก "ทั้งหมด"</span><span class="sxs-lookup"><span data-stu-id="910fa-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="910fa-131">หมายเหตุว่า มีใบแจ้งหนี้สองใบแสดงอยู่ในส่วนภาพรวม </span><span class="sxs-lookup"><span data-stu-id="910fa-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="910fa-132">ขณะนี้ให้ผสานสองใบนั้นให้กลายเป็นใบแจ้งหนี้เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="910fa-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="910fa-133">ในฟิลด์ **อัพเดตบทสรุปสำหรับ** ให้เลือก 'บัญชีใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="910fa-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="910fa-134">คลิก **จัดเรียง** เพือผสานใบสั่งขายหลายใบให้เป็นใบแจ้งหนี้ใบเดียว</span><span class="sxs-lookup"><span data-stu-id="910fa-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="910fa-135">ใบสั่งขายสองใบขณะนี้ได้ถูกผสานไว้ในใบแจ้งหนี้เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="910fa-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="910fa-136">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="910fa-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="910fa-137">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="910fa-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="910fa-138">ลงรายการบัญชีใบแจ้งหนี้ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="910fa-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="910fa-139">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ใบแจ้งหนี้ > การออกใบแจ้งหนี้เป็นชุด > ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="910fa-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="910fa-140">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="910fa-140">Click **Select**.</span></span>
3. <span data-ttu-id="910fa-141">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="910fa-141">Click **OK**.</span></span>
4. <span data-ttu-id="910fa-142">คลิก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="910fa-142">Click **Batch**.</span></span>
5. <span data-ttu-id="910fa-143">ให้เลือก **ใช่** ใน **การประมวลผลชุดงาน**.</span><span class="sxs-lookup"><span data-stu-id="910fa-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="910fa-144">คลิก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="910fa-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="910fa-145">เลือก **วัน**</span><span class="sxs-lookup"><span data-stu-id="910fa-145">Select **Days**.</span></span>
8. <span data-ttu-id="910fa-146">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="910fa-146">Click **OK**.</span></span>
9. <span data-ttu-id="910fa-147">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="910fa-147">Click **OK**.</span></span>
10. <span data-ttu-id="910fa-148">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="910fa-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="910fa-149">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="910fa-149">Click **Yes**.</span></span>

