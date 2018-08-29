--- 
title: "กำหนดการแม็ปแบบจำลอง ER และเลือกแหล่งข้อมูลสำหรับรายการเหล่านั้น"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 2beda3555274fee3f17ad13c54c6823307216385
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="18630-103">กำหนดการแม็ปแบบจำลอง ER และเลือกแหล่งข้อมูลสำหรับรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="18630-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18630-104">ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถเลือกแหล่งข้อมูลสำหรับแบบจำลองข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="18630-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="18630-105">แหล่งข้อมูลจะผูกกับส่วนประกอบแต่ละของแบบจำลองข้อมูลที่เลือกไว้ในขณะออกแบบ และเติมข้อมูลทางธุรกิจไปที่แบบจำลองข้อมูลขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="18630-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="18630-106">ในตัวอย่างนี้ คุณจะเลือกแหล่งข้อมูลสำหรับแบบจำลองข้อมูลที่มีอยู่ที่สร้างไว้แล้วสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำขั้นตอนเหล่านี้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนอย่างแรกให้เสร็จสมบูรณ์ในกระบวนงาน "สร้างแบบจำลองข้อมูลใหม่"l</span><span class="sxs-lookup"><span data-stu-id="18630-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="18630-107">เปิดแผนภูมิการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="18630-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="18630-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="18630-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="18630-109">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="18630-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="18630-110">แทรกการแม็ปแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="18630-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="18630-111">ในแผนภูมิ เลือก 'การชำระเงิน(แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="18630-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="18630-112">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="18630-112">Click Designer.</span></span>
3. <span data-ttu-id="18630-113">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="18630-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="18630-114">Click New.</span></span>
    * <span data-ttu-id="18630-115">การดำเนินการนี้จะสร้างเรกคอร์ดใหม่ที่จะแม็ปแบบจำลองข้อมูลไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="18630-116">ในตัวอย่างนี้ คุณจะแม็ปแบบจำลองข้อมูลไปยังแหล่งข้อมูลสำหรับชนิดการชำระเงินที่ต้องการ: การโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="18630-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="18630-117">มันเป็นไปได้สำหรับการออกแบบการแม็ปมากกว่าหนึ่งรายการสำหรับแบบจำลองข้อมูลเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="18630-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="18630-118">ตัวอย่างเช่น คุณสามารถสร้างการแม็ปสำหรับชนิดต่างๆของการชำระเงิน เช่น สำหรับเดบิตโดยตรง หรือสำหรับการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="18630-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="18630-119">ในตัวอย่างนี้ คุณจะสร้างการแม็ปสำหรับการโอนย้ายเครดิต</span><span class="sxs-lookup"><span data-stu-id="18630-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="18630-120">ในฟิลด์ชื่อ พิมพ์ 'การแม็ป CT'</span><span class="sxs-lookup"><span data-stu-id="18630-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="18630-121">การแม็ป CT</span><span class="sxs-lookup"><span data-stu-id="18630-121">CT mapping</span></span>  
6. <span data-ttu-id="18630-122">ในฟิลด์คำอธิบาย พิมพ์ 'รูปแบบการชำระเงิน CT ในการแม็ป'</span><span class="sxs-lookup"><span data-stu-id="18630-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="18630-123">การแม็ปรูปแบบการชำระเงิน CT</span><span class="sxs-lookup"><span data-stu-id="18630-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="18630-124">ในฟิลด์คำนิยาม พิมพ์ 'CustomerCreditTransferInitiation'</span><span class="sxs-lookup"><span data-stu-id="18630-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="18630-125">เลือก การเริ่มต้นการโอนย้ายเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="18630-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="18630-126">แก้ไขการเปลี่ยนแปลงของคำนิยาม</span><span class="sxs-lookup"><span data-stu-id="18630-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="18630-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="18630-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="18630-128">กำหนดแหล่งข้อมูลที่ต้องระบุสำหรับการแม็ปแบบจำลองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="18630-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="18630-129">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="18630-129">Click Designer.</span></span>
2. <span data-ttu-id="18630-130">ในแผนภูมิ เลือก 'Dynamics 365 for Operations\Table records'</span><span class="sxs-lookup"><span data-stu-id="18630-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="18630-131">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="18630-131">Click Add root.</span></span>
    * <span data-ttu-id="18630-132">ป้อนแหล่งข้อมูลนี้เพื่อเข้าถึงธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="18630-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="18630-133">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="18630-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="18630-134">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="18630-134">Transactions</span></span>  
5. <span data-ttu-id="18630-135">ในฟิลด์ป้ายชื่อ ป้อน "ธุรกรรม"</span><span class="sxs-lookup"><span data-stu-id="18630-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="18630-136">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="18630-136">Transactions</span></span>  
6. <span data-ttu-id="18630-137">ในฟิลด์วิธีใช้ ป้อน 'รายการสมุดรายวันบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="18630-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="18630-138">รายการสมุดรายวันบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="18630-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="18630-139">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="18630-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="18630-140">เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="18630-140">Select Yes.</span></span>  
8. <span data-ttu-id="18630-141">ในฟิลด์ตาราง พิมพ์ 'LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="18630-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="18630-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="18630-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="18630-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="18630-143">Click OK.</span></span>
    * <span data-ttu-id="18630-144">เลือก ตาราง LedgerJournalTrans เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="18630-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="18630-145">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="18630-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="18630-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="18630-146">Click Add.</span></span>
    * <span data-ttu-id="18630-147">คลิก เพิ่มเพื่อเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="18630-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="18630-148">ในฟิลด์ชื่อ พิมพ์ '$EndToEndID'</span><span class="sxs-lookup"><span data-stu-id="18630-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="18630-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="18630-149">$EndToEndID</span></span>  
13. <span data-ttu-id="18630-150">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-150">Click Edit formula.</span></span>
14. <span data-ttu-id="18630-151">ในแผนภูมิ เลือก 'สตริง\เชื่อมเข้าด้วยกัน'</span><span class="sxs-lookup"><span data-stu-id="18630-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="18630-152">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="18630-152">Click Add function.</span></span>
16. <span data-ttu-id="18630-153">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="18630-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="18630-154">ในแผนภูมิ เลือก 'ธุรกรรม\ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="18630-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="18630-155">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-155">Click Add data source.</span></span>
19. <span data-ttu-id="18630-156">ในฟิลด์สูตร ป้อน 'CONCATENATE(Transactions.Voucher, "-", '</span><span class="sxs-lookup"><span data-stu-id="18630-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="18630-157">พิมพ์ [ , "-", ] ที่ส่วนท้ายสุดของสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="18630-158">ในแผนภูมิ เลือก 'สตริง\ข้อความ'</span><span class="sxs-lookup"><span data-stu-id="18630-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="18630-159">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="18630-159">Click Add function.</span></span>
22. <span data-ttu-id="18630-160">ในแผนภูมิ เลือก 'ธุรกรรม\รหัสเรกคอร์ด(RecId)'</span><span class="sxs-lookup"><span data-stu-id="18630-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="18630-161">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-161">Click Add data source.</span></span>
24. <span data-ttu-id="18630-162">ในฟิลด์สูตร ป้อน 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'</span><span class="sxs-lookup"><span data-stu-id="18630-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="18630-163">พิมพ์ [))] ที่ส่วนท้ายสุดของสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="18630-164">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="18630-164">Click Save.</span></span>
    * <span data-ttu-id="18630-165">ตรวจสอบให้แน่ใจว่า ไม่พบข้อผิดพลาดใดๆ สำหรับสูตรที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="18630-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="18630-166">ดูที่ แท็บข้อผิดพลาดด้านล่างตัวควบคุมตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="18630-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="18630-167">Close the page.</span></span>
27. <span data-ttu-id="18630-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="18630-168">Click OK.</span></span>
    * <span data-ttu-id="18630-169">เพิ่ม ฟิลด์ที่คำนวณไปยังแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="18630-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="18630-170">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="18630-170">Click Add.</span></span>
    * <span data-ttu-id="18630-171">คลิก เพิ่มเพื่อเพิ่มฟิลด์ที่คำนวณได้ใหม่</span><span class="sxs-lookup"><span data-stu-id="18630-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="18630-172">ในฟิลด์ชื่อ พิมพ์ '$Amount'</span><span class="sxs-lookup"><span data-stu-id="18630-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="18630-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="18630-173">$Amount</span></span>  
30. <span data-ttu-id="18630-174">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-174">Click Edit formula.</span></span>
31. <span data-ttu-id="18630-175">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="18630-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="18630-176">ในแผนภูมิ เลือก 'ธุรกรรม\เดบิต(เดบิตยอดเงินในสกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="18630-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="18630-177">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-177">Click Add data source.</span></span>
34. <span data-ttu-id="18630-178">ในฟิลด์สูตร ป้อน 'Transactions.AmountCurDebit - '</span><span class="sxs-lookup"><span data-stu-id="18630-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="18630-179">พิมพ์ [ - ] ที่ส่วนท้ายสุดของสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="18630-180">ในแผนภูมิ เลือก 'ธุรกรรม\เครดิต(เดบิตยอดเงินในสกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="18630-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="18630-181">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-181">Click Add data source.</span></span>
37. <span data-ttu-id="18630-182">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="18630-182">Click Save.</span></span>
38. <span data-ttu-id="18630-183">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="18630-183">Close the page.</span></span>
39. <span data-ttu-id="18630-184">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="18630-184">Click OK.</span></span>
    * <span data-ttu-id="18630-185">การดำเนินการนี้จะเพิ่มฟิลด์ที่คำนวณ $Amount ได้ลงในแหล่งข้อมูลที่เลือกสำหรับรูปแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="18630-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="18630-186">ในแผนภูมิ เลือก 'Transactions\$Amount'</span><span class="sxs-lookup"><span data-stu-id="18630-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="18630-187">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="18630-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="18630-188">ในแผนภูมิ ขยายหรือยุบ 'Transactions\$Amount'</span><span class="sxs-lookup"><span data-stu-id="18630-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="18630-189">ในแผนภูมิ ขยายหรือยุบ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="18630-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="18630-190">ในแผนภูมิ เลือก 'Dynamics 365 for Operations\Table records'</span><span class="sxs-lookup"><span data-stu-id="18630-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="18630-191">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="18630-191">Click Add root.</span></span>
    * <span data-ttu-id="18630-192">ป้อนแหล่งข้อมูลนี้เพื่อเข้าถึงรายละเอียดบัญชีธนาคารของบริษัท</span><span class="sxs-lookup"><span data-stu-id="18630-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="18630-193">ในฟิลด์ชื่อ พิมพ์ 'บัญชีธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="18630-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="18630-194">บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="18630-194">BankAccount</span></span>  
47. <span data-ttu-id="18630-195">ในฟิลด์ป้ายชื่อ ป้อน 'บัญชีธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="18630-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="18630-196">บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="18630-196">Bank Account</span></span>  
48. <span data-ttu-id="18630-197">ในฟิลด์วิธีใช้ ป้อน 'บัญชีธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="18630-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="18630-198">บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="18630-198">Bank Account</span></span>  
49. <span data-ttu-id="18630-199">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="18630-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="18630-200">เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="18630-200">Select Yes.</span></span>  
50. <span data-ttu-id="18630-201">ในฟิลด์ตาราง พิมพ์ 'BankAccountTable'</span><span class="sxs-lookup"><span data-stu-id="18630-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="18630-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="18630-202">BankAccountTable</span></span>  
51. <span data-ttu-id="18630-203">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="18630-203">Click OK.</span></span>
    * <span data-ttu-id="18630-204">เลือก ตาราง BankAccountTable เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="18630-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="18630-205">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="18630-205">Click Add root.</span></span>
    * <span data-ttu-id="18630-206">ป้อนแหล่งข้อมูลนี้เพื่อเข้าถึงข้อกำหนดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="18630-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="18630-207">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="18630-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="18630-208">บริษัท</span><span class="sxs-lookup"><span data-stu-id="18630-208">Company</span></span>  
54. <span data-ttu-id="18630-209">ในฟิลด์ป้ายชื่อ พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="18630-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="18630-210">ข้อมูลบริษัท</span><span class="sxs-lookup"><span data-stu-id="18630-210">Company information</span></span>  
55. <span data-ttu-id="18630-211">ในฟิลด์วิธีใช้ ป้อน 'ข้อมูลบริษัท'</span><span class="sxs-lookup"><span data-stu-id="18630-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="18630-212">ข้อมูลบริษัท</span><span class="sxs-lookup"><span data-stu-id="18630-212">Company information</span></span>  
56. <span data-ttu-id="18630-213">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="18630-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="18630-214">เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="18630-214">Select Yes.</span></span>  
57. <span data-ttu-id="18630-215">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="18630-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="18630-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="18630-216">CompanyInfo</span></span>  
58. <span data-ttu-id="18630-217">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="18630-217">Click OK.</span></span>
    * <span data-ttu-id="18630-218">เลือก ตาราง CompanyInfo เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="18630-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="18630-219">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="18630-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="18630-220">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="18630-220">Click Add root.</span></span>
    * <span data-ttu-id="18630-221">แทรกฟิลด์ที่คำนวณได้เป็นแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="18630-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="18630-222">ในฟิลด์ชื่อ ให้พิมพ์ 'ระยะเวลาประมวลผลข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="18630-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="18630-223">ระยะเวลาการประมวลผลข้อมูล</span><span class="sxs-lookup"><span data-stu-id="18630-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="18630-224">ในฟิลด์ป้ายชื่อ ป้อน 'วันที่ & เวลาการประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="18630-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="18630-225">วันที่ & เวลาการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="18630-225">Processing date & time</span></span>  
63. <span data-ttu-id="18630-226">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="18630-226">Click Edit formula.</span></span>
64. <span data-ttu-id="18630-227">ในแผนภูมิ ให้เลือก 'วันที่/เวลา\SESSIONNOW'</span><span class="sxs-lookup"><span data-stu-id="18630-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="18630-228">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="18630-228">Click Add function.</span></span>
66. <span data-ttu-id="18630-229">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="18630-229">Click Save.</span></span>
67. <span data-ttu-id="18630-230">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="18630-230">Close the page.</span></span>
68. <span data-ttu-id="18630-231">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="18630-231">Click OK.</span></span>
    * <span data-ttu-id="18630-232">เพิ่ม ฟิลด์คำนวณ วันที่และเวลาประมวลผล เป็นแหล่งข้อมูลสำหรับแบบจำลองข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="18630-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="18630-233">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="18630-233">Click Save.</span></span>
70. <span data-ttu-id="18630-234">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="18630-234">Close the page.</span></span>
71. <span data-ttu-id="18630-235">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="18630-235">Close the page.</span></span>
72. <span data-ttu-id="18630-236">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="18630-236">Close the page.</span></span>


