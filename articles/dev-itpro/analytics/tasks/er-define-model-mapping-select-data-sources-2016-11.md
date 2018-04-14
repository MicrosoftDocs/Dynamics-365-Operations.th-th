--- 
title: "กำหนดการแม็ปแบบจำลองและเลือกแหล่งข้อมูลสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถเลือกแหล่งข้อมูลสำหรับแบบจำลองข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER)"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e04ff56da694b9c72a72b0a7f130433f34241e78
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="b21a6-103">กำหนดการแม็ปแบบจำลองและเลือกแหล่งข้อมูลสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="b21a6-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b21a6-104">ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถเลือกแหล่งข้อมูลสำหรับแบบจำลองข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="b21a6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="b21a6-105">แหล่งข้อมูลจะผูกกับส่วนประกอบแต่ละของแบบจำลองข้อมูลที่เลือกไว้ในขณะออกแบบ และเติมข้อมูลทางธุรกิจไปที่แบบจำลองข้อมูลขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="b21a6-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="b21a6-106">ในตัวอย่างนี้ คุณจะเลือกแหล่งข้อมูลสำหรับแบบจำลองข้อมูลที่มีอยู่ที่สร้างไว้แล้วสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำขั้นตอนเหล่านี้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนอย่างแรกให้เสร็จสมบูรณ์ในกระบวนงาน "สร้างแบบจำลองข้อมูลใหม่"l</span><span class="sxs-lookup"><span data-stu-id="b21a6-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="b21a6-107">เปิดแผนภูมิการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b21a6-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="b21a6-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b21a6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b21a6-109">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b21a6-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="b21a6-110">แทรกการแม็ปแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="b21a6-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="b21a6-111">ในแผนภูมิ เลือก 'การชำระเงิน(แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="b21a6-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="b21a6-112">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b21a6-112">Click Designer.</span></span>
3. <span data-ttu-id="b21a6-113">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="b21a6-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b21a6-114">Click New.</span></span>
    * <span data-ttu-id="b21a6-115">การดำเนินการนี้จะสร้างเรกคอร์ดใหม่ที่จะแม็ปแบบจำลองข้อมูลไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="b21a6-116">ในตัวอย่างนี้ คุณจะแม็ปแบบจำลองข้อมูลไปยังแหล่งข้อมูลสำหรับชนิดการชำระเงินที่ต้องการ: การโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="b21a6-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="b21a6-117">มันเป็นไปได้สำหรับการออกแบบการแม็ปมากกว่าหนึ่งรายการสำหรับแบบจำลองข้อมูลเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b21a6-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="b21a6-118">ตัวอย่างเช่น คุณสามารถสร้างการแม็ปสำหรับชนิดต่างๆของการชำระเงิน เช่น สำหรับเดบิตโดยตรง หรือสำหรับการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="b21a6-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="b21a6-119">ในตัวอย่างนี้ คุณจะสร้างการแม็ปสำหรับการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="b21a6-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="b21a6-120">ในฟิลด์ชื่อ พิมพ์ 'การแม็ป CT'</span><span class="sxs-lookup"><span data-stu-id="b21a6-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="b21a6-121">การแม็ป CT</span><span class="sxs-lookup"><span data-stu-id="b21a6-121">CT mapping</span></span>  
6. <span data-ttu-id="b21a6-122">ในฟิลด์คำอธิบาย พิมพ์ 'รูปแบบการชำระเงิน CT ในการแม็ป'</span><span class="sxs-lookup"><span data-stu-id="b21a6-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="b21a6-123">การแม็ปรูปแบบการชำระเงิน CT</span><span class="sxs-lookup"><span data-stu-id="b21a6-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="b21a6-124">ในฟิลด์คำนิยาม พิมพ์ 'CustomerCreditTransferInitiation'</span><span class="sxs-lookup"><span data-stu-id="b21a6-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="b21a6-125">เลือก การเริ่มต้นการโอนย้ายเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="b21a6-126">แก้ไขการเปลี่ยนแปลงของคำนิยาม</span><span class="sxs-lookup"><span data-stu-id="b21a6-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="b21a6-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b21a6-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="b21a6-128">กำหนดแหล่งข้อมูลที่ต้องระบุสำหรับการแม็ปแบบจำลองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="b21a6-129">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b21a6-129">Click Designer.</span></span>
2. <span data-ttu-id="b21a6-130">ในแผนภูมิ เลือก 'Dynamics 365 for Operations\Table records'</span><span class="sxs-lookup"><span data-stu-id="b21a6-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="b21a6-131">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="b21a6-131">Click Add root.</span></span>
    * <span data-ttu-id="b21a6-132">ป้อนแหล่งข้อมูลนี้เพื่อเข้าถึงธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b21a6-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="b21a6-133">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b21a6-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="b21a6-134">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b21a6-134">Transactions</span></span>  
5. <span data-ttu-id="b21a6-135">ในฟิลด์ป้ายชื่อ ป้อน "ธุรกรรม"</span><span class="sxs-lookup"><span data-stu-id="b21a6-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="b21a6-136">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b21a6-136">Transactions</span></span>  
6. <span data-ttu-id="b21a6-137">ในฟิลด์วิธีใช้ ป้อน 'รายการสมุดรายวันบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="b21a6-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="b21a6-138">รายการสมุดรายวันบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="b21a6-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="b21a6-139">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="b21a6-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b21a6-140">เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="b21a6-140">Select Yes.</span></span>  
8. <span data-ttu-id="b21a6-141">ในฟิลด์ตาราง พิมพ์ 'LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="b21a6-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="b21a6-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="b21a6-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="b21a6-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b21a6-143">Click OK.</span></span>
    * <span data-ttu-id="b21a6-144">เลือก ตาราง LedgerJournalTrans เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="b21a6-145">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="b21a6-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="b21a6-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b21a6-146">Click Add.</span></span>
    * <span data-ttu-id="b21a6-147">คลิก เพิ่มเพื่อเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="b21a6-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="b21a6-148">ในฟิลด์ชื่อ พิมพ์ '$EndToEndID'</span><span class="sxs-lookup"><span data-stu-id="b21a6-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="b21a6-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="b21a6-149">$EndToEndID</span></span>  
13. <span data-ttu-id="b21a6-150">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-150">Click Edit formula.</span></span>
14. <span data-ttu-id="b21a6-151">ในแผนภูมิ เลือก 'สตริง\เชื่อมเข้าด้วยกัน'</span><span class="sxs-lookup"><span data-stu-id="b21a6-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="b21a6-152">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-152">Click Add function.</span></span>
16. <span data-ttu-id="b21a6-153">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b21a6-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="b21a6-154">ในแผนภูมิ เลือก 'ธุรกรรม\ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="b21a6-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="b21a6-155">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-155">Click Add data source.</span></span>
19. <span data-ttu-id="b21a6-156">ในฟิลด์สูตร ป้อน 'CONCATENATE(Transactions.Voucher, "-", '</span><span class="sxs-lookup"><span data-stu-id="b21a6-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="b21a6-157">พิมพ์ [ , "-", ] ที่ส่วนท้ายสุดของสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="b21a6-158">ในแผนภูมิ เลือก 'สตริง\ข้อความ'</span><span class="sxs-lookup"><span data-stu-id="b21a6-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="b21a6-159">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-159">Click Add function.</span></span>
22. <span data-ttu-id="b21a6-160">ในแผนภูมิ เลือก 'ธุรกรรม\รหัสเรกคอร์ด(RecId)'</span><span class="sxs-lookup"><span data-stu-id="b21a6-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="b21a6-161">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-161">Click Add data source.</span></span>
24. <span data-ttu-id="b21a6-162">ในฟิลด์สูตร ป้อน 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'</span><span class="sxs-lookup"><span data-stu-id="b21a6-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="b21a6-163">พิมพ์ [))] ที่ส่วนท้ายสุดของสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="b21a6-164">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b21a6-164">Click Save.</span></span>
    * <span data-ttu-id="b21a6-165">ตรวจสอบให้แน่ใจว่า ไม่พบข้อผิดพลาดใดๆ สำหรับสูตรที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b21a6-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="b21a6-166">ดูที่ แท็บข้อผิดพลาดด้านล่างตัวควบคุมตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="b21a6-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-167">Close the page.</span></span>
27. <span data-ttu-id="b21a6-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b21a6-168">Click OK.</span></span>
    * <span data-ttu-id="b21a6-169">เพิ่ม ฟิลด์ที่คำนวณไปยังแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="b21a6-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="b21a6-170">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b21a6-170">Click Add.</span></span>
    * <span data-ttu-id="b21a6-171">คลิก เพิ่มเพื่อเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="b21a6-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="b21a6-172">ในฟิลด์ชื่อ พิมพ์ '$Amount'</span><span class="sxs-lookup"><span data-stu-id="b21a6-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="b21a6-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="b21a6-173">$Amount</span></span>  
30. <span data-ttu-id="b21a6-174">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-174">Click Edit formula.</span></span>
31. <span data-ttu-id="b21a6-175">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b21a6-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="b21a6-176">ในแผนภูมิ เลือก 'ธุรกรรม\เดบิต(เดบิตยอดเงินในสกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b21a6-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="b21a6-177">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-177">Click Add data source.</span></span>
34. <span data-ttu-id="b21a6-178">ในฟิลด์สูตร ป้อน 'Transactions.AmountCurDebit - '</span><span class="sxs-lookup"><span data-stu-id="b21a6-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="b21a6-179">พิมพ์ [ - ] ที่ส่วนท้ายสุดของสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="b21a6-180">ในแผนภูมิ เลือก 'ธุรกรรม\เครดิต(เดบิตยอดเงินในสกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b21a6-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="b21a6-181">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-181">Click Add data source.</span></span>
37. <span data-ttu-id="b21a6-182">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b21a6-182">Click Save.</span></span>
38. <span data-ttu-id="b21a6-183">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-183">Close the page.</span></span>
39. <span data-ttu-id="b21a6-184">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b21a6-184">Click OK.</span></span>
    * <span data-ttu-id="b21a6-185">การดำเนินการนี้จะเพิ่มฟิลด์ที่คำนวณ $Amount ได้ลงในแหล่งข้อมูลที่เลือกสำหรับรูปแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="b21a6-186">ในแผนภูมิ เลือก 'Transactions\$Amount'</span><span class="sxs-lookup"><span data-stu-id="b21a6-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="b21a6-187">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b21a6-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="b21a6-188">ในแผนภูมิ ขยายหรือยุบ 'Transactions\$Amount'</span><span class="sxs-lookup"><span data-stu-id="b21a6-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="b21a6-189">ในแผนภูมิ ขยายหรือยุบ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b21a6-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="b21a6-190">ในแผนภูมิ เลือก 'Dynamics 365 for Operations\Table records'</span><span class="sxs-lookup"><span data-stu-id="b21a6-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="b21a6-191">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="b21a6-191">Click Add root.</span></span>
    * <span data-ttu-id="b21a6-192">ป้อนแหล่งข้อมูลนี้เพื่อเข้าถึงรายละเอียดบัญชีธนาคารของบริษัท</span><span class="sxs-lookup"><span data-stu-id="b21a6-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="b21a6-193">ในฟิลด์ชื่อ พิมพ์ 'บัญชีธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="b21a6-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="b21a6-194">บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="b21a6-194">BankAccount</span></span>  
47. <span data-ttu-id="b21a6-195">ในฟิลด์ป้ายชื่อ ป้อน 'บัญชีธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="b21a6-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b21a6-196">บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="b21a6-196">Bank Account</span></span>  
48. <span data-ttu-id="b21a6-197">ในฟิลด์วิธีใช้ ป้อน 'บัญชีธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="b21a6-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b21a6-198">บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="b21a6-198">Bank Account</span></span>  
49. <span data-ttu-id="b21a6-199">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="b21a6-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b21a6-200">เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="b21a6-200">Select Yes.</span></span>  
50. <span data-ttu-id="b21a6-201">ในฟิลด์ตาราง พิมพ์ 'BankAccountTable'</span><span class="sxs-lookup"><span data-stu-id="b21a6-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="b21a6-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="b21a6-202">BankAccountTable</span></span>  
51. <span data-ttu-id="b21a6-203">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b21a6-203">Click OK.</span></span>
    * <span data-ttu-id="b21a6-204">เลือก ตาราง BankAccountTable เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="b21a6-205">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="b21a6-205">Click Add root.</span></span>
    * <span data-ttu-id="b21a6-206">ป้อนแหล่งข้อมูลนี้เพื่อเข้าถึงข้อกำหนดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="b21a6-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="b21a6-207">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="b21a6-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="b21a6-208">บริษัท</span><span class="sxs-lookup"><span data-stu-id="b21a6-208">Company</span></span>  
54. <span data-ttu-id="b21a6-209">ในฟิลด์ป้ายชื่อ พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b21a6-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="b21a6-210">ข้อมูลบริษัท</span><span class="sxs-lookup"><span data-stu-id="b21a6-210">Company information</span></span>  
55. <span data-ttu-id="b21a6-211">ในฟิลด์วิธีใช้ ป้อน 'ข้อมูลบริษัท'</span><span class="sxs-lookup"><span data-stu-id="b21a6-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="b21a6-212">ข้อมูลบริษัท</span><span class="sxs-lookup"><span data-stu-id="b21a6-212">Company information</span></span>  
56. <span data-ttu-id="b21a6-213">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="b21a6-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b21a6-214">เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="b21a6-214">Select Yes.</span></span>  
57. <span data-ttu-id="b21a6-215">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="b21a6-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="b21a6-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="b21a6-216">CompanyInfo</span></span>  
58. <span data-ttu-id="b21a6-217">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b21a6-217">Click OK.</span></span>
    * <span data-ttu-id="b21a6-218">เลือก ตาราง CompanyInfo เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="b21a6-219">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="b21a6-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="b21a6-220">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="b21a6-220">Click Add root.</span></span>
    * <span data-ttu-id="b21a6-221">แทรกฟิลด์ที่คำนวณได้เป็นแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="b21a6-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="b21a6-222">ในฟิลด์ชื่อ ให้พิมพ์ 'ระยะเวลาประมวลผลข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="b21a6-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="b21a6-223">ระยะเวลาการประมวลผลข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b21a6-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="b21a6-224">ในฟิลด์ป้ายชื่อ ป้อน 'วันที่ & เวลาการประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="b21a6-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="b21a6-225">วันที่ & เวลาการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="b21a6-225">Processing date & time</span></span>  
63. <span data-ttu-id="b21a6-226">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b21a6-226">Click Edit formula.</span></span>
64. <span data-ttu-id="b21a6-227">ในแผนภูมิ ให้เลือก 'วันที่/เวลา\SESSIONNOW'</span><span class="sxs-lookup"><span data-stu-id="b21a6-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="b21a6-228">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-228">Click Add function.</span></span>
66. <span data-ttu-id="b21a6-229">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b21a6-229">Click Save.</span></span>
67. <span data-ttu-id="b21a6-230">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-230">Close the page.</span></span>
68. <span data-ttu-id="b21a6-231">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b21a6-231">Click OK.</span></span>
    * <span data-ttu-id="b21a6-232">เพิ่ม ฟิลด์คำนวณ วันที่และเวลาประมวลผล เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b21a6-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="b21a6-233">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b21a6-233">Click Save.</span></span>
70. <span data-ttu-id="b21a6-234">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-234">Close the page.</span></span>
71. <span data-ttu-id="b21a6-235">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-235">Close the page.</span></span>
72. <span data-ttu-id="b21a6-236">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b21a6-236">Close the page.</span></span>


