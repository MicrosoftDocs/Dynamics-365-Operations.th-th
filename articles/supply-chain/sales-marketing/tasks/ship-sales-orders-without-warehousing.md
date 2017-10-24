--- 
title: "จัดส่งใบสั่งขายโดยไม่มีคลังสินค้า"
description: "คำแนะนำนี้อธิบายวิธีการอัพเดตใบสั่งขายเมื่อมีการจัดส่งผลิตภัณฑ์ให้กับลูกค้า "
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f1b9dd4b99bcbcc6cfbc5cfd8e3271fa80c628c
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="f81af-103">จัดส่งใบสั่งขายโดยไม่มีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f81af-103">Ship sales orders without warehousing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f81af-104">คำแนะนำนี้อธิบายวิธีการอัพเดตใบสั่งขายเมื่อมีการจัดส่งผลิตภัณฑ์ให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="f81af-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="f81af-105">คู่มือจะเกี่ยวข้องกับขั้นตอนการเติมสินค้าที่ไม่ได้ถูกตั้งค่าสำหรับการจัดการคลังสินค้า (ไม่มีคลังสินค้าทั้งแบบพื้นฐานหรือแบบขั้นสูง) และดังนั้นจึงไม่จำเป็นต้องลงทะเบียนผลิตภัณฑ์ก่อนที่จะจัดส่งสินค้า </span><span class="sxs-lookup"><span data-stu-id="f81af-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="f81af-106">คุณสามารถทำตามขั้นตอนเหล่านี้กับข้อมูลของคุณ หรือกับบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f81af-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="f81af-107">ในทั้งสองกรณี ก่อนที่คุณจะเริ่มงานนี้ ให้สร้างใบสั่งขายสำหรับสินค้าคงคลังที่มีปริมาณมากกว่า 1</span><span class="sxs-lookup"><span data-stu-id="f81af-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="f81af-108">เพื่อหลีกเลี่ยงข้อผิดพลาดในการลงรายการบัญชี คุณต้องตรวจสอบว่า ปริมาณผลิตภัณฑ์คงเหลือในไซต์และคลังสินค้าที่คุณเลือกในใบสั่งนั้นครอบคลุมปริมาณในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="f81af-109">ลงรายการบัญชีบันทึกการจัดส่งสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="f81af-110">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f81af-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="f81af-111">ในรายการ ให้ค้นหาและเลือกใบสั่งคุณได้สร้างขึ้นสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="f81af-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="f81af-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f81af-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f81af-113">ในบานหน้าต่างการดำเนินการ ให้คลิกเบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="f81af-114">คลิกลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="f81af-115">ขยายหรือยุบส่วนพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="f81af-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="f81af-116">ในฟิลด์ ปริมาณ ให้เลือก 'ทั้งหมด'</span><span class="sxs-lookup"><span data-stu-id="f81af-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="f81af-117">ตัวเลือกอื่นๆได้แก่ จัดส่งทันทีและเบิกสินค้าแล้ว </span><span class="sxs-lookup"><span data-stu-id="f81af-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="f81af-118">ถ้ารายการใบสั่งที่จะจัดส่งเป็นบางส่วนและฟิลด์จัดส่งทันทีบนรายการใบสั่งที่ประกอบด้วยปริมาณ คุณอาจเลือก จัดส่งทันที </span><span class="sxs-lookup"><span data-stu-id="f81af-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="f81af-119">ถ้าขั้นตอนการเติมสินค้าขององค์กรของคุณมีการเบิกสินค้าเป็นกระบวนการแยกต่างหาก ที่มีการจัดการและการลงทะเบียนโดยรายการเบิกสินค้า คุณอาจเลือก เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="f81af-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="f81af-120">ตรวจสอบว่า ตัวเลือกการลงรายการบัญชีได้ถูกตั้งค่าเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="f81af-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="f81af-121">ตั้งค่าตัวเลือกการพิมพ์บันทึกการจัดส่งเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="f81af-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="f81af-122">แท็บภาพรวมประกอบด้วยรายการของบันทึกการจัดส่งที่จะมีการสร้างขึ้นในการลงรายการบัญชีนี้ </span><span class="sxs-lookup"><span data-stu-id="f81af-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="f81af-123">ถ้าคุณจัดส่งใบสั่งแต่ละใบ โดยทั่วไปจะมีหนึ่งบันทึกการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="f81af-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="f81af-124">อย่างไรก็ตาม ถ้ารายการของใบสั่งนั้นจะถูกจัดส่งจากไซต์อื่น การลงรายการบัญชีจะถูกแบ่งออกโดยอัตโนมัติเป็นจำนวนเอกสารที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="f81af-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="f81af-125">ซึ่งเป็นเงื่อนไขบังคับที่ไม่สามารถเปลี่ยนแปลงได้ </span><span class="sxs-lookup"><span data-stu-id="f81af-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="f81af-126">ในทำนองเดียวกัน การลงรายการบัญชีจะยังสามารถถูกแบ่งออกเป็นหลายเอกสาร ถ้ารายการใบสั่งจะถูกจัดส่งไปที่ที่อยู่การจัดส่งที่แตกต่างกัน และมีการตั้งค่านโยบายการจัดส่งเพื่อต้องการการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="f81af-127">บนแท็บรายการ ให้เลือกแถวสำหรับรายการใบสั่งที่จะมีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="f81af-128">ในฟิลด์อัพเดต ป้อนหมายเลขที่ต่ำกว่าปริมาณเดิม</span><span class="sxs-lookup"><span data-stu-id="f81af-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="f81af-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f81af-129">Click OK.</span></span>
12. <span data-ttu-id="f81af-130">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f81af-130">Click Yes.</span></span>
13. <span data-ttu-id="f81af-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f81af-131">Close the page.</span></span>
14. <span data-ttu-id="f81af-132">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f81af-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="f81af-133">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="f81af-133">Click Change view.</span></span>
16. <span data-ttu-id="f81af-134">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="f81af-134">Click Header view.</span></span>
    * <span data-ttu-id="f81af-135">ถ้ารายการในใบสั่งทั้งหมดมีการจัดส่งทั้งหมดแล้ว สถานะใบสั่งจะเปลี่ยนจาก เปิด เป็น จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="f81af-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="f81af-136">ในตัวอย่างนี้ รายการใบสั่งได้ถูกจัดส่งเป็นบางส่วน </span><span class="sxs-lookup"><span data-stu-id="f81af-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="f81af-137">นี่เป็นเหตุผลว่าทำไมสถานะใบสั่งยังคงเป็น เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="f81af-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="f81af-138">มีการตั้งค่าฟิลด์สถานะเอกสารไปที่บันทึกการจัดส่ง เนื่องจากมีรายการใบสั่งอย่างน้อยหนึ่งรายการได้ถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="f81af-139">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f81af-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="f81af-140">คลิกปริมาณในรายการ</span><span class="sxs-lookup"><span data-stu-id="f81af-140">Click Line quantity.</span></span>
19. <span data-ttu-id="f81af-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f81af-141">Close the page.</span></span>
20. <span data-ttu-id="f81af-142">ในบานหน้าต่างการดำเนินการ ให้คลิก เบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="f81af-143">คลิกบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f81af-143">Click Packing slip.</span></span>
    * <span data-ttu-id="f81af-144">หน้าสมุดรายวันบันทึกการจัดส่งประกอบด้วย เอกสารบันทึกการจัดส่งทั้งหมดที่ถูกสร้างขึ้นสำหรับใบสั่งของคุณ </span><span class="sxs-lookup"><span data-stu-id="f81af-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="f81af-145">คุณสามารถตรวจทานรายละเอียดของแต่ละเอกสาร และพิมพ์เอกสารเหล่านั้น ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f81af-145">You can review details of each document and print them, if you wish.</span></span>  


