--- 
title: "สร้างกำหนดการจัดส่ง"
description: "กระบวนงานนี้อธิบายวิธีการสร้างกำหนดการจัดส่งสำหรับใบสั่งขาย "
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 956edeac33f8531ecebef64301f2318333000429
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="9fe3f-103">สร้างกำหนดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-103">Create a delivery schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fe3f-104">กระบวนงานนี้อธิบายวิธีการสร้างกำหนดการจัดส่งสำหรับใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="9fe3f-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="9fe3f-105">กำหนดการจัดส่งจะใช้เมื่อมีการร้องขอปริมาณหรือใบเสนอราคาให้จัดส่งหลายรายการ </span><span class="sxs-lookup"><span data-stu-id="9fe3f-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="9fe3f-106">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="9fe3f-107">สร้างกำหนดการการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-107">Create delivery schedule</span></span>
1. <span data-ttu-id="9fe3f-108">ไปที่ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9fe3f-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="9fe3f-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-109">Click New.</span></span>
3. <span data-ttu-id="9fe3f-110">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9fe3f-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="9fe3f-111">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9fe3f-111">Click OK.</span></span>
5. <span data-ttu-id="9fe3f-112">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9fe3f-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="9fe3f-113">ในฟิลด์ปริมาณ ให้ป้อนตัวเลขที่มีค่ามากกว่า 1</span><span class="sxs-lookup"><span data-stu-id="9fe3f-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="9fe3f-114">คลิก รายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="9fe3f-114">Click Sales order line.</span></span>
8. <span data-ttu-id="9fe3f-115">คลิก กำหนดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="9fe3f-116">หน้ากำหนดการจัดส่งเป็นที่ซึ่งคุณสามารถระบุหมายเลขของการจัดส่งที่ปริมาณรวมของรายการใบสั่งจะถูกจัดส่งไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9fe3f-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="9fe3f-117">โดยค่าเริ่มต้น ระบบจะคัดลอกปริมาณรวมและรายละเอียดการจัดส่งอื่นของรายการขายเดิมไปยังรายการกำหนดการจัดส่งแรก </span><span class="sxs-lookup"><span data-stu-id="9fe3f-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="9fe3f-118">ในตัวอย่างนี้ เราจะสร้างกำหนดการสำหรับการจัดส่งสองรายการ ซึ่งวันจัดส่งครั้งที่สองจะอ๊อฟเซ็ตไปหนึ่งสัปดาห์จากวันจัดส่งครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="9fe3f-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="9fe3f-119">ในฟิลด์ปริมาณ ให้ป้อนหมายเลขที่เป็นส่วนหนึ่งของปริมาณรวม</span><span class="sxs-lookup"><span data-stu-id="9fe3f-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="9fe3f-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-120">Click New.</span></span>
11. <span data-ttu-id="9fe3f-121">ในฟิลด์ปริมาณ ให้ป้อนปริมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="9fe3f-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="9fe3f-122">ในฟิลด์วันจัดส่งที่ร้องขอ ให้ป้อนวันที่ซึ่งก็คือหนึ่งสัปดาห์ถัดจากวันที่ของรายการจัดส่งแรก</span><span class="sxs-lookup"><span data-stu-id="9fe3f-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="9fe3f-123">ตัวเลือกสองตัวเลือกในปุ่มด่วนของการแปลงค่าธรรมเนียมจะควบคุมวิธีที่คุณต้องการให้ค่าธรรมเนียมที่จะแจกจ่ายในรายการกำหนดการจัดส่ง หลังจากที่คุณได้กำหนดให้กับรายการใบสั่งต้นฉบับแล้ว </span><span class="sxs-lookup"><span data-stu-id="9fe3f-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="9fe3f-124">ถ้าคุณเลือกที่การคัดลอกยอดเงินรวม ยอดเงินค่าธรรมเนียมเดียวกันจะถูกคัดลอกไปแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="9fe3f-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="9fe3f-125">การปันส่วนไปที่ตัวเลือกรายการการจัดส่งจะแบ่งค่าธรรมเนียมออกเท่าๆกันในรายการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="9fe3f-126">ค่าธรรมเนียมคงที่เท่านั้นที่สามารถแบ่งออกได้ ในขณะที่ค่าธรรมเนียมผันแปรยังคงจะถูกคัดลอกไปยังรายการต่างๆ</span><span class="sxs-lookup"><span data-stu-id="9fe3f-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="9fe3f-127">ย้ายเคอร์เซอร์ไปจากรายการจัดส่งที่สองเพื่ออัพเดตหน้า</span><span class="sxs-lookup"><span data-stu-id="9fe3f-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="9fe3f-128">คุณสามารถติดตามปริมาณรวมที่ได้ปันส่วนไปยังรายการกำหนดการจัดส่งโดยการดูที่ฟิลด์ผลรวมและที่เหลืออยู่ </span><span class="sxs-lookup"><span data-stu-id="9fe3f-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="9fe3f-129">เมื่อปริมาณคงเหลือเป็นศูนย์ ปริมาณทั้งหมดจากรายการต้นฉบับมีการปันส่วนไปยังกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="9fe3f-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="9fe3f-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-130">Click OK.</span></span>
    * <span data-ttu-id="9fe3f-131">กำหนดการจัดส่งในขณะนี้ได้ถูกคัดลอกไปยังรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="9fe3f-132">รายการใบสั่งต้นฉบับที่อ้างอิงรายการการค้าได้ถูกแปลงเป็นรายการใบสั่งที่มีการจัดส่งหลายครั้ง </span><span class="sxs-lookup"><span data-stu-id="9fe3f-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="9fe3f-133">มีการทำเครื่องหมายด้วยไอคอนเฉพาะและทำหน้าที่เป็นส่วนหัวของรายการการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="9fe3f-134">รายการใหม่สองรายการที่อ้างอิงรายการการจัดส่ง ประกอบกันเป็นหนึ่งกำหนดการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="9fe3f-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="9fe3f-135">ใบสั่งจะถูกประมวลผลโดยเทียบกับรายการเหล่านี้และไม่ใช่รายการต้นฉบับ </span><span class="sxs-lookup"><span data-stu-id="9fe3f-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="9fe3f-136">ถ้ามีการพิมพ์เอกสารเช่น ใบยืนยันการจัดส่ง รายการเบิกสินค้า บันทึกการจัดส่ง หรือใบแจ้งหนี้ รายการจัดส่งเท่านั้นจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="9fe3f-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="9fe3f-137">รายการจัดส่งสามารถมีวันจัดส่ง ปริมาณ วิธีการจัดส่ง และมิติการจัดเก็บ ที่แตกต่างกัน เช่น ไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="9fe3f-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="9fe3f-138">อย่างไรก็ตาม มิติของผลิตภัณฑ์ต้องตรงกับสิ่งที่อยู่ในรายการทางการค้าเสมอ และไม่สามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="9fe3f-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="9fe3f-139">ในฟิลด์ปริมาณ ให้ป้อนหมายเลขที่มีค่ามากกว่าหมายเลขที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9fe3f-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="9fe3f-140">เลือกรายการทางการค้าเพื่อดูผลของการคำนวณซ้ำของปริมาณ</span><span class="sxs-lookup"><span data-stu-id="9fe3f-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="9fe3f-141">ในบานหน้าต่างการดำเนินการ ให้คลิก เบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="9fe3f-142">คลิกลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="9fe3f-143">ขยายส่วน พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="9fe3f-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="9fe3f-144">ในฟิลด์ ปริมาณ ให้เลือก 'ทั้งหมด'</span><span class="sxs-lookup"><span data-stu-id="9fe3f-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="9fe3f-145">โปรดทราบว่า จะมีสร้างบันทึกการจัดส่งสำหรับรายการกำหนดการจัดส่งสองรายการและไม่ใช่รายการใบสั่งต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="9fe3f-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="9fe3f-146">เลือกใช่ในฟิลด์พิมพ์บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="9fe3f-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9fe3f-147">Click OK.</span></span>
23. <span data-ttu-id="9fe3f-148">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="9fe3f-148">Click Yes.</span></span>
24. <span data-ttu-id="9fe3f-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9fe3f-149">Close the page.</span></span>


