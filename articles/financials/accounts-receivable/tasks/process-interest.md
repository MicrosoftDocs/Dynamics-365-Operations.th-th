--- 
title: "ประมวลผลดอกเบี้ย"
description: "กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีดอกเบี้ยตั๋วเงิน "
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a><span data-ttu-id="9b491-103">ประมวลผลดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="9b491-103">Process interest</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b491-104">กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีดอกเบี้ยตั๋วเงิน </span><span class="sxs-lookup"><span data-stu-id="9b491-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="9b491-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="9b491-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="9b491-106">ตั้งค่าดอกเบี้ยบนโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="9b491-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="9b491-107">ไปที่สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > โพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9b491-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="9b491-108">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="9b491-108">Click Edit.</span></span>
    * <span data-ttu-id="9b491-109">เลือกรหัสดอกเบี้ยจากรายการแบบหล่นลง </span><span class="sxs-lookup"><span data-stu-id="9b491-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="9b491-110">ถ้าคุณไม่ต้องการการคำนวณดอกเบี้ยสำหรับธุรกรรมโดยใช้โพรไฟล์การลงบัญชีนี้ ให้ปล่อยฟิลด์นี้ว่าง</span><span class="sxs-lookup"><span data-stu-id="9b491-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="9b491-111">แท็บข้อจำกัดตารางช่วยให้คุณสามารถเปลี่ยนวิธีการประมวลผลดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="9b491-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="9b491-112">ถ้าฟิลด์นี้ถูกตั้งค่าเป็น ใช่ ดอกเบี้ยจะถูกคำนวณสำหรับโพรไฟล์การลงบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="9b491-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="9b491-113">คำนวณดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="9b491-113">Calculate interest</span></span>
1. <span data-ttu-id="9b491-114">ไปที่สินเชื่อและการเรียกเก็บเงิน > ดอกเบี้ย > สร้างดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9b491-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="9b491-115">คุณต้องเลือกชนิดของธุรกรรมซึ่งคุณจะคำนวณดอกเบี้ย </span><span class="sxs-lookup"><span data-stu-id="9b491-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="9b491-116">ธุรกรรมที่ค้างอยู่ทั้งหมดของชนิดนี้ทั้งหมดจะถูกรวมในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="9b491-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="9b491-117">ถ้าคุณเลือกดอกเบี้ย คุณจะคำนวณดอกเบี้ยสำหรับดอกเบี้ย </span><span class="sxs-lookup"><span data-stu-id="9b491-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="9b491-118">คุณอาจต้องการตรวจสอบกฎหมายที่ควบคุมการคำนวณดอกเบี้ยสำหรับดอกเบี้ยก่อนที่จะรวมธุรกรรมเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9b491-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="9b491-119">ดอกเบี้ยจะถูกคำนวณจากวัน "วันที่สิ้นสุด" </span><span class="sxs-lookup"><span data-stu-id="9b491-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="9b491-120">ถ้าคุณไม่ได้ระบุ "วันที่เริ่มต้น" จากนั้นดอกเบี้ยตั๋วเงินทั้งหมดยังไม่ได้ลงรายการบัญชีจะถูกยกเลิก และดอกเบี้ยจะถูกคำนวณใหม่จากวันที่ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9b491-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="9b491-121">ป้อนวันที่ของดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9b491-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="9b491-122">ตัวเลือกโพรไฟล์การลงรายการบัญชีมี 3 ตัวเลือก:   บัญชี - ใช้โพรไฟล์การลงบัญชีที่ถูกกำหนดให้กับบัญชีลูกค้าสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="9b491-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="9b491-123">เลือก - ใช้โพรไฟล์การลงบัญชีที่คุณเลือกในฟิลด์โพรไฟล์การลงรายการบัญชี </span><span class="sxs-lookup"><span data-stu-id="9b491-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="9b491-124">ธุรกรรม - ใช้แต่ละโพรไฟล์การลงรายการบัญชีจากธุรกรรมที่มีการคำนวณดอกเบี้ยสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="9b491-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="9b491-125">ธุรกรรมที่ไม่มีโพรไฟล์การลงรายการบัญชีที่กำหนด จะใช้โพรไฟล์การลงรายการบัญชีที่ถูกระบุไว้ในพื้นที่ของบัญชีแยกประเภทและภาษีขายของแบบฟอร์มพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="9b491-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="9b491-126">เลือกโพรไฟล์การลงรายการบัญชีที่นี้ถ้าคุณจะเปลี่ยนแปลง "ใช้โพรไฟล์ลงรายการบัญชีจาก" เป็น "เลือก"</span><span class="sxs-lookup"><span data-stu-id="9b491-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="9b491-127">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="9b491-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="9b491-128">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="9b491-128">Click Filter.</span></span>
5. <span data-ttu-id="9b491-129">ในฟิลด์เงื่อนไข ป้อนรหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9b491-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="9b491-130">ตัวอย่างเช่น ป้อน 'US-001'..</span><span class="sxs-lookup"><span data-stu-id="9b491-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="9b491-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9b491-131">Click OK.</span></span>
7. <span data-ttu-id="9b491-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9b491-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="9b491-133">พิมพ์ดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9b491-133">Print interest notes</span></span>
1. <span data-ttu-id="9b491-134">ไปที่สินเชื่อและการเรียกเก็บเงิน > ดอกเบี้ย > ตรวจทานและดำเนินการดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9b491-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="9b491-135">ในฟิลด์สถานะ เลือก 'สร้างแล้ว'</span><span class="sxs-lookup"><span data-stu-id="9b491-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="9b491-136">ในฟิลด์พิมพ์ เลือก 'ไม่มีการพิมพ์'</span><span class="sxs-lookup"><span data-stu-id="9b491-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="9b491-137">คลิก พิมพ์</span><span class="sxs-lookup"><span data-stu-id="9b491-137">Click Print.</span></span>
5. <span data-ttu-id="9b491-138">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="9b491-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="9b491-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9b491-139">Click OK.</span></span>
7. <span data-ttu-id="9b491-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9b491-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="9b491-141">ลงรายการบัญชีดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9b491-141">Post the interest note</span></span>
1. <span data-ttu-id="9b491-142">เลือกดอกเบี้ยตั๋วเงินที่พร้อมจะลงรายการบัญชี (สถานะถูกสร้างแล้ว)</span><span class="sxs-lookup"><span data-stu-id="9b491-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="9b491-143">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="9b491-143">Click Post.</span></span>
3. <span data-ttu-id="9b491-144">ป้อนวันที่ลงรายการบัญชีสำหรับดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="9b491-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="9b491-145">เลือก ใช่ เพื่อสร้างธุรกรรมบัญชีแยกประเภททั่วไปสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="9b491-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="9b491-146">ถ้าคุณไม่ได้เลือก ใช่ ดอกเบี้ยบนดอกเบี้ยตั๋วเงินทั้งหมดของลูกค้าจะมีการสะสมและลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปในธุรกรรมหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="9b491-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="9b491-147">ขยายหรือยุบส่วนของเรกคอร์ดที่จะรวม </span><span class="sxs-lookup"><span data-stu-id="9b491-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="9b491-148">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9b491-148">Click OK.</span></span>
6. <span data-ttu-id="9b491-149">ในฟิลด์สถานะ เลือก 'ลงรายการบัญชีแล้ว'</span><span class="sxs-lookup"><span data-stu-id="9b491-149">In the Status field, select 'Posted'.</span></span>


