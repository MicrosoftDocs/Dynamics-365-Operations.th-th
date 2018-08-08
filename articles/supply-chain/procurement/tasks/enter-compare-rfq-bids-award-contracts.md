--- 
title: "ป้อนและเปรียบเทียบการประมูล RFQ และให้สัญญา"
description: "กระบวนงานนี้แสดงให้คุณเห็นถึงวิธีการป้อนการตอบให้กับ RFQ การให้คะแนน และการเปรียบเทียบการประมูล และจากนั้น การให้การประมูลแก่ผู้จัดจำหน่าย "
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e2b07323fc7c66e2e551f3eabb8e4965b85e92f4
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="f00a9-103">ป้อนและเปรียบเทียบการประมูล RFQ และให้สัญญา</span><span class="sxs-lookup"><span data-stu-id="f00a9-103">Enter and compare RFQ bids and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f00a9-104">กระบวนงานนี้แสดงให้คุณเห็นถึงวิธีการป้อนการตอบให้กับ RFQ การให้คะแนน และการเปรียบเทียบการประมูล และจากนั้น การให้การประมูลแก่ผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="f00a9-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="f00a9-105">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f00a9-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="f00a9-106">ก่อนที่คุณจะเริ่ม คุณต้องมี RFQ ที่มีรายการสองรายการที่ได้ถูกส่งไปยังผู้จัดจำหน่ายสองราย</span><span class="sxs-lookup"><span data-stu-id="f00a9-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="f00a9-107">คุณสามารถรันกระบวนงาน "สร้างคำขอใบเสนอราคา" ให้เป็นข้อกำหนดเบื้องต้นเพื่อสร้างสิ่งนี้</span><span class="sxs-lookup"><span data-stu-id="f00a9-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="f00a9-108">คุณต้องตั้งค่าเกณฑ์การให้คะแนนก่อนที่คุณจะสามารถรันกระบวนงานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="f00a9-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="f00a9-109">ป้อนการตอบจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="f00a9-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="f00a9-110">ไปที่การจัดซื้อและการจัดหา > คำขอใบเสนอราคา > คำขอใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f00a9-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="f00a9-111">เลือก RFQ ที่มีสถานะ ส่งแล้ว และคลิกลิงค์บนหมายเลขกรณีของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="f00a9-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="f00a9-112">RFQ ควรถูกส่งไปยังผู้จัดจำหน่าย 2 ราย</span><span class="sxs-lookup"><span data-stu-id="f00a9-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="f00a9-113">คลิกส่วนหัวเพื่อไปที่รายการของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="f00a9-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="f00a9-114">เลือกผู้จัดจำหน่ายที่คุณต้องการป้อนการตอบสนองใน RFQ</span><span class="sxs-lookup"><span data-stu-id="f00a9-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="f00a9-115">คลิกป้อนการตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-115">Click Enter reply.</span></span>
6. <span data-ttu-id="f00a9-116">ในบานหน้าต่างการดำเนินการ คลิกตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="f00a9-117">คลิกคัดลอกข้อมูลเพื่อตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="f00a9-118">การดำเนินการนี้จะคัดลอกข้อมูลที่เลือก ตัวอย่างเช่น ปริมาณจากกรณี RFQ ไปยังการตอบ RFQ </span><span class="sxs-lookup"><span data-stu-id="f00a9-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="f00a9-119">อีกทางหนึ่งคือ คุณสามารถข้ามการดำเนินการนี้ได้และในฟิลด์การตอบสนองด้วยตนเอง เมื่อคุณแก้ไขการตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="f00a9-120">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f00a9-120">Click Edit.</span></span>
9. <span data-ttu-id="f00a9-121">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="f00a9-122">เลือกรายการใบเสนอราคาอื่น</span><span class="sxs-lookup"><span data-stu-id="f00a9-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="f00a9-123">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="f00a9-124">ให้คะแนนการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-124">Score the bid</span></span>
1. <span data-ttu-id="f00a9-125">คลิกส่วนหัวเพื่อไปยังการให้คะแนนของการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="f00a9-126">ขยายส่วนการให้คะแนนการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="f00a9-127">ในฟิลด์คะแนน ป้อนหมายสำหรับเกณฑ์การให้คะแนนหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="f00a9-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="f00a9-128">ถ้าคุณวางเมาส์เหนือเกณฑ์การให้คะแนน คำแนะนำเครื่องมือจะแสดงช่วงที่คุณต้องให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="f00a9-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="f00a9-129">ในการสาธิตนี้ คุณสามารถเพิ่มหมายเลขระหว่าง 1 และ 5 ให้กับเกณฑ์ใดๆได้</span><span class="sxs-lookup"><span data-stu-id="f00a9-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="f00a9-130">เลือกเงื่อนไขการให้คะแนนอีกรายการหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f00a9-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="f00a9-131">ในฟิลด์คะแนน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="f00a9-132">ขยายส่วนคำถาม</span><span class="sxs-lookup"><span data-stu-id="f00a9-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="f00a9-133">ถ้ากรณี RFQ มีแบบสอบถามที่ถูกส่งไปยังผู้จัดจำหน่าย คุณสามารถป้อนคำตอบในส่วนของคำถามได้</span><span class="sxs-lookup"><span data-stu-id="f00a9-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="f00a9-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="f00a9-135">ป้อนการตอบจากผู้จัดจำหน่ายอีกรายหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f00a9-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="f00a9-136">เลือกผู้จัดจำหน่ายต่อไป โดยการล้่างข้อมูลผู้จัดจำหน่ายที่คุณเพิ่งป้อนการตอบ และจากนั้นโดยการเลือกแถวสำหรับผู้จัดจำหน่ายต่อไป</span><span class="sxs-lookup"><span data-stu-id="f00a9-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="f00a9-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f00a9-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f00a9-138">คลิกป้อนการตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-138">Click Enter reply.</span></span>
4. <span data-ttu-id="f00a9-139">คลิกคัดลอกข้อมูลเพื่อตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="f00a9-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f00a9-140">Click Edit.</span></span>
6. <span data-ttu-id="f00a9-141">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="f00a9-142">เลือกรายการใบเสนอราคาอื่น</span><span class="sxs-lookup"><span data-stu-id="f00a9-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="f00a9-143">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="f00a9-144">ให้คะแนนการประมูลที่สอง</span><span class="sxs-lookup"><span data-stu-id="f00a9-144">Score the second bid</span></span>
1. <span data-ttu-id="f00a9-145">คลิกส่วนหัวเพื่อไปยังการให้คะแนนของการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="f00a9-146">ในฟิลด์คะแนน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="f00a9-147">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f00a9-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f00a9-148">ในฟิลด์คะแนน ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="f00a9-149">เปรียบเทียบการตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-149">Compare the replies</span></span>
1. <span data-ttu-id="f00a9-150">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f00a9-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="f00a9-151">คลิกเปรียบเทียบการตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-151">Click Compare replies.</span></span>
3. <span data-ttu-id="f00a9-152">ในฟิลด์อันดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="f00a9-153">หน้านี้แสดงการประมูลที่มีส่วนหัวและรายการ และคะแนนรวมในระดับหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="f00a9-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="f00a9-154">คุณสามารถเปรียบเทียบรายการได้โดยการจัดเรียงในกริด เพื่อให้รายการที่สามารถเปรียบเทียบได้นั้นอยู่ต่อกัน</span><span class="sxs-lookup"><span data-stu-id="f00a9-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="f00a9-155">ข้อมูลยังประกอบด้วย:   ปริมาณ: ปริมาณที่เสนอโดยผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="f00a9-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="f00a9-156">ซึ่งอาจไม่เท่ากับปริมาณที่ระบุใน RFQ</span><span class="sxs-lookup"><span data-stu-id="f00a9-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="f00a9-157">ยอดเงินสุทธิ: ราคาที่เสนอโดยผู้จัดจำหน่าย หลังจากการหักส่วนลดใดๆสำหรับสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="f00a9-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="f00a9-158">ความแตกต่าง: จำนวนของวันที่วันที่จัดส่งในหัวข้อการประมูลหรือรายการที่แตกต่างจากวันที่จัดส่งที่ร้องขอในส่วนหัวของ RFQ หรือรายการ RFQ</span><span class="sxs-lookup"><span data-stu-id="f00a9-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="f00a9-159">คุณสามารถป้อนอันดับสำหรับการประมูลแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="f00a9-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="f00a9-160">เลือกรายการส่วนหัวสำหรับการประมูลอื่น ที่คุณต้องการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="f00a9-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="f00a9-161">ในฟิลด์อันดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f00a9-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="f00a9-162">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f00a9-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="f00a9-163">การปฏิเสธการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-163">Reject a bid</span></span>
1. <span data-ttu-id="f00a9-164">เลือกรายการส่วนหัวสำหรับการประมูลอ ที่คุณต้องการปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="f00a9-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="f00a9-165">คุณสามารถยอมรับ ปฏิเสธ หรือส่งคืนการประมูลหนึ่งรายการ หรือรายการภายในการประมูลหนึ่งรายการในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="f00a9-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="f00a9-166">เลือกการทำเครื่องหมายกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="f00a9-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="f00a9-167">ถ้าคุณเลือกการทำเครื่องหมายกล่องกาเครื่องหมายในส่วนหัวของการประมูล จากนั้นรายการทั้งหมดจะถูกทำเครื่องหมายด้วย </span><span class="sxs-lookup"><span data-stu-id="f00a9-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="f00a9-168">คุณยังสามารถเลือกที่จะทำเครื่องหมายเซ็ตย่อยของรายการ ภายในการประมูลเพื่อปฏิเสธ หรือยอมรับรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="f00a9-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="f00a9-169">สามารถยอมรับการประมูลของผู้จัดจำหน่ายหนึ่งรายสำหรับรายการหลายรายการของ RFQ ได้ และจากนั้นให้รายการ RFQ อื่นๆแก่ผู้จัดจำหน่ายต่างๆ อย่างไรก็ตาม คุณต้องดำเนินการ 2 ขั้นตอน การประมูลหนึ่งรายการในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="f00a9-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="f00a9-170">ถ้ามีรายการรองอยู่ คุณสามารถยอมรับรายการประมูลเดิม หรือรายการสำรองได้อย่างใดอย่างหนึ่ง แต่ไม่ใช่ทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="f00a9-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="f00a9-171">คลิกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="f00a9-171">Click Reject.</span></span>
4. <span data-ttu-id="f00a9-172">คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00a9-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="f00a9-173">ในฟิลด์เหตุผลการปฏิเสธ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f00a9-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="f00a9-174">เหตุผลสำหรับการปฏิเสธจะถูกจัดเก็บในการตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="f00a9-175">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00a9-175">Click OK.</span></span>
7. <span data-ttu-id="f00a9-176">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00a9-176">Click OK.</span></span>
8. <span data-ttu-id="f00a9-177">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-177">Close the page.</span></span>
9. <span data-ttu-id="f00a9-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-178">Close the page.</span></span>
10. <span data-ttu-id="f00a9-179">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="f00a9-180">การยอมรับการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-180">Accept a bid</span></span>
1. <span data-ttu-id="f00a9-181">เลือกใบเสนอราคาที่คุณต้องการยอมรับ แล้วคลิกลิงค์ในฟิลด์คำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="f00a9-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="f00a9-182">ในบานหน้าต่างการดำเนินการ คลิกตอบ</span><span class="sxs-lookup"><span data-stu-id="f00a9-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="f00a9-183">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="f00a9-183">Click Accept.</span></span>
    * <span data-ttu-id="f00a9-184">ถ้าคุณได้ทำเครื่องหมายรายการเฉพาะ และไม่ได้ทำในรายการอื่นๆ จากนั้นการดำเนินการยอมรับจะรวมเฉพาะรายการที่ถูกทำเครื่องหมาย </span><span class="sxs-lookup"><span data-stu-id="f00a9-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="f00a9-185">ถ้าคุณต้องการยอมรับรายการทั้งหมดในการประมูล คุณไม่ต้องทำเครื่องหมายรายการ</span><span class="sxs-lookup"><span data-stu-id="f00a9-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="f00a9-186">คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00a9-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="f00a9-187">นี่อนุญาตให้คุณสามารถบันทึกเหตุผลสำหรับการยอมรับรายการประมูล </span><span class="sxs-lookup"><span data-stu-id="f00a9-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="f00a9-188">เหตุผลจะถูกจัดเก็บในรายการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="f00a9-189">ในฟิลด์เหตุผลการยอมรับ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f00a9-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="f00a9-190">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00a9-190">Click OK.</span></span>
7. <span data-ttu-id="f00a9-191">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00a9-191">Click OK.</span></span>
    * <span data-ttu-id="f00a9-192">เมื่อคุณคลิกตกลง จะมีการสร้างใบสั่งซื้อตามรายการที่รวมอยู่ในการยอมรับ RFQ </span><span class="sxs-lookup"><span data-stu-id="f00a9-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="f00a9-193">ถ้ามีการประมูลอื่นๆที่ยังไม่ได้ถูกประมวลผล (ถูกยอมรับ ถูกปฏิเสธ หรือถูกส่งคืน) จากนั้นระบบจะกระตุ้นให้คุณปฏิเสธการประมูลที่เหลืออยู่</span><span class="sxs-lookup"><span data-stu-id="f00a9-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="f00a9-194">ดูใบสั่งซื้อที่ได้ถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="f00a9-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="f00a9-195">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f00a9-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="f00a9-196">คลิกใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f00a9-196">Click Purchase order.</span></span>
    * <span data-ttu-id="f00a9-197">คุณสามารถดูใบสั่งซื้อที่ถูกสร้างได้ที่นี่ เมื่อคุณยอมรับการประมูล</span><span class="sxs-lookup"><span data-stu-id="f00a9-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="f00a9-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-198">Close the page.</span></span>
4. <span data-ttu-id="f00a9-199">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-199">Close the page.</span></span>
5. <span data-ttu-id="f00a9-200">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-200">Close the page.</span></span>
6. <span data-ttu-id="f00a9-201">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00a9-201">Close the page.</span></span>


