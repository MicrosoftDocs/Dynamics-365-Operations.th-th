--- 
title: "ลงทะเบียนค่าคอมมิชชันการขาย"
description: "กระบวนงานนี้แสดงวิธีการคำนวณและการลงทะเบียนค่าคอมมิชชันการขาย "
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0fad3c62f926e508e09a265a600194b7ea595bf0
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="register-sales-commissions"></a><span data-ttu-id="2c025-103">ลงทะเบียนค่าคอมมิชชันการขาย</span><span class="sxs-lookup"><span data-stu-id="2c025-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c025-104">กระบวนงานนี้แสดงวิธีการคำนวณและการลงทะเบียนค่าคอมมิชชันการขาย </span><span class="sxs-lookup"><span data-stu-id="2c025-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="2c025-105">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="2c025-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="2c025-106">ก่อนที่จะเริ่มคู่มือนี้ เรียกใช้คุ่มือที่เรียกว่า "ตั้งค่ากฎค่าคอมมิชชันการขาย" เพื่อให้แน่ใจว่า คุณได้ตั้งค่าการคำนวณค่าคอมมิชชันที่จำเป็นทั้งหมดแล้ว </span><span class="sxs-lookup"><span data-stu-id="2c025-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="2c025-107">จดบันทึกหมายเลขลูกค้าและสินค้าที่คุณได้เลือกไว้สำหรับกระบวนการค่าคอมมิชชัน และใช้เมื่อถูกถามเพื่อสร้างใบสั่งขายในคู่มือนี้</span><span class="sxs-lookup"><span data-stu-id="2c025-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="2c025-108">ออกใบแจ้งหนี้ใบสั่งขายที่ทำให้พนักงานขายมีสิทธิ์ได้รับค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2c025-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="2c025-109">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2c025-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="2c025-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2c025-110">Click New.</span></span>
3. <span data-ttu-id="2c025-111">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2c025-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2c025-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c025-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2c025-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2c025-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2c025-114">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2c025-114">Click OK.</span></span>
7. <span data-ttu-id="2c025-115">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2c025-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="2c025-116">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="2c025-116">Click Change view.</span></span>
9. <span data-ttu-id="2c025-117">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="2c025-117">Click Header view.</span></span>
10. <span data-ttu-id="2c025-118">ขยายส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="2c025-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="2c025-119">ค่าในฟิลด์กลุ่มการขายแสดงถึงกลุ่มที่มีการกำหนดพนักงานขายหนึ่งคนหรือมากกว่าให้ </span><span class="sxs-lookup"><span data-stu-id="2c025-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="2c025-120">บุคลากรในกลุ่มจะเป็นคนที่จะได้รับค่าคอมมิชชันเมื่อใบสั่งออกใบแจ้งหนี้ ตามอัตราที่กำหนดไว้ล่วงหน้าและการกระจายสินค้า</span><span class="sxs-lookup"><span data-stu-id="2c025-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="2c025-121">ค่าจะถูกคัดลอกจากบัตรลูกค้า แต่คุณสามารถเปลี่ยนถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c025-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="2c025-122">กลุ่มการขายจะได้รับการคัดลอกไปยังรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2c025-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="2c025-123">คุณสามารถเปลี่ยนได้เพื่อให้แตกต่างจากสิ่งที่อยู่ในส่วนหัวและ/หรือระหว่างรายการ</span><span class="sxs-lookup"><span data-stu-id="2c025-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="2c025-124">ค่าในฟิลด์กลุ่มค่าคอมมิชชันแสดงถึง กลุ่มที่คุณสร้างสำหรับลูกค้าอย่างน้อยหนึ่งคนพร้อมวัตถุประสงค์การติดตามค่าคอมมิชชัน </span><span class="sxs-lookup"><span data-stu-id="2c025-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="2c025-125">ค่าจะถูกคัดลอกจากบัตรลูกค้า แต่คุณสามารถเปลี่ยนแปลงได้เมื่อต้องการ </span><span class="sxs-lookup"><span data-stu-id="2c025-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="2c025-126">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2c025-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="2c025-127">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="2c025-127">Click Change view.</span></span>
13. <span data-ttu-id="2c025-128">คลิกมุมมองรายการ</span><span class="sxs-lookup"><span data-stu-id="2c025-128">Click Line view.</span></span>
14. <span data-ttu-id="2c025-129">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2c025-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2c025-130">ในรายการ ให้เลือกสินค้าที่คุณได้ตั้งค่าสำหรับค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2c025-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="2c025-131">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="2c025-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2c025-132">จดบันทึกยอดเงินสุทธิของรายการ </span><span class="sxs-lookup"><span data-stu-id="2c025-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="2c025-133">ซึ่งจะแสดงการรายได้จากการขาย ในตัวอย่างนี้เป็นพื้นฐานสำหรับการคำนวณค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2c025-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="2c025-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2c025-134">Click Save.</span></span>
18. <span data-ttu-id="2c025-135">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2c025-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="2c025-136">คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2c025-136">Click Invoice.</span></span>
20. <span data-ttu-id="2c025-137">ขยายส่วน พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="2c025-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="2c025-138">ในฟิลด์ ปริมาณ ให้เลือก 'ทั้งหมด'</span><span class="sxs-lookup"><span data-stu-id="2c025-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="2c025-139">เลือก ใช่ ในฟิลด์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="2c025-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="2c025-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2c025-140">Click OK.</span></span>
24. <span data-ttu-id="2c025-141">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2c025-141">Click OK.</span></span>
    * <span data-ttu-id="2c025-142">อาจใช้เวลาสักครู่เพื่อลงรายบัญชีธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="2c025-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="2c025-143">อนุญาตให้การประมวลผลเสร็จสมบูรณ์ และห้ามปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c025-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="2c025-144">ตรวจทานค่าคอมมิชชันการขายที่ลงทะเบียนแล้ว</span><span class="sxs-lookup"><span data-stu-id="2c025-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="2c025-145">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2c025-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="2c025-146">คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2c025-146">Click Invoice.</span></span>
3. <span data-ttu-id="2c025-147">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2c025-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="2c025-148">คลิกธุรกรรมค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2c025-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="2c025-149">แท็บภาพรวมแสดงรายการที่แสดงถึงยอดค่าคอมมิชชันที่ชำระแก่พนักงานขายที่เกี่ยวข้องกับใบสั่งขายที่ออกใบแจ้งหนี้แล้ว </span><span class="sxs-lookup"><span data-stu-id="2c025-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="2c025-150">ลองตรวจทานรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="2c025-150">Let's review the details.</span></span>     
    * <span data-ttu-id="2c025-151">ถ้าคุณใช้คู่มือ "ตั้งค่ากฎค่าคอมมิชชันการขาย" เพื่อตั้งค่ากลุ่มการขายที่มีค่าคอมมิชชัน จะมีพนักงานขายสองคนจะได้รับค่าคอมมิชชันการขาย และค่าคอมมิชชันจะถูกแบ่งเท่าๆกันระหว่างสองคน</span><span class="sxs-lookup"><span data-stu-id="2c025-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="2c025-152">ในตัวอย่างนี้ มีการคำนวณยอดรวมของค่าคอมมิชชันเป็นเปอร์เซ็นต์ของรายได้การขาย (ยอดเงินสุทธิของรายการใบสั่ง)</span><span class="sxs-lookup"><span data-stu-id="2c025-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="2c025-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c025-153">Close the page.</span></span>
6. <span data-ttu-id="2c025-154">คลิกใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="2c025-154">Click Voucher.</span></span>
    * <span data-ttu-id="2c025-155">คุณสามารถตรวจทานธุรกรรมใบสำคัญสำหรับยอดเงินค่าคอมมิชชัน ที่ได้ลงรายการบัญชีค่าใช้จ่ายค่าคอมมิชชันที่กำหนดไว้ล่วงหน้า และบัญชีเจ้าหนี้ค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2c025-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


