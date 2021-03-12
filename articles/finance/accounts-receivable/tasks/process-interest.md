---
title: ประมวลผลดอกเบี้ย
description: 'กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีดอกเบี้ยตั๋วเงิน '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad30984f55017ee275af15ddb4f1a46c6a50db69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992950"
---
# <a name="process-interest"></a><span data-ttu-id="89d77-103">ประมวลผลดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="89d77-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89d77-104">กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีดอกเบี้ยตั๋วเงิน </span><span class="sxs-lookup"><span data-stu-id="89d77-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="89d77-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="89d77-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="89d77-106">ตั้งค่าดอกเบี้ยบนโพรไฟล์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="89d77-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="89d77-107">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > โพรไฟล์การลงรายการบัญชีลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="89d77-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="89d77-108">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="89d77-108">Click **Edit**.</span></span>
3. <span data-ttu-id="89d77-109">ใน **fastTab การตั้งค่า** ในฟิลด์ **รหัสดอกเบี้ย** ให้เลือกรหัสดอกเบี้ยจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="89d77-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="89d77-110">ถ้าคุณไม่ต้องการการคำนวณดอกเบี้ยสำหรับธุรกรรมโดยใช้โพรไฟล์การลงบัญชีนี้ ให้ปล่อยฟิลด์นี้ว่าง</span><span class="sxs-lookup"><span data-stu-id="89d77-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="89d77-111">แท็บ **ข้อจำกัดตาราง** ช่วยให้คุณสามารถเปลี่ยนวิธีการประมวลผลดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="89d77-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="89d77-112">ถ้าฟิลด์นี้ถูกตั้งค่าเป็น ใช่ ดอกเบี้ยจะถูกคำนวณสำหรับโพรไฟล์การลงบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="89d77-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="89d77-113">คำนวณดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="89d77-113">Calculate interest</span></span>
1. <span data-ttu-id="89d77-114">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > สินเชื่อและการเรียกเก็บเงิน > ดอกเบี้ย > สร้างดอกเบี้ยตั๋วเงิน**</span><span class="sxs-lookup"><span data-stu-id="89d77-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="89d77-115">คุณต้องเลือกชนิดของธุรกรรมซึ่งคุณจะคำนวณดอกเบี้ย </span><span class="sxs-lookup"><span data-stu-id="89d77-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="89d77-116">ธุรกรรมที่ค้างอยู่ทั้งหมดของชนิดนี้ทั้งหมดจะถูกรวมในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="89d77-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="89d77-117">ถ้าคุณตั้งค่า **ดอกเบี้ย** เป็น 'ใช่' คุณจะคำนวณดอกเบี้ยในดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="89d77-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="89d77-118">คุณอาจต้องการตรวจสอบกฎหมายที่ควบคุมการคำนวณดอกเบี้ยสำหรับดอกเบี้ยก่อนที่จะรวมธุรกรรมเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="89d77-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="89d77-119">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่เริ่มต้นซึ่งข้อตกลงนี้จะมีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="89d77-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="89d77-120">ถ้าคุณไม่ได้ระบุ **วันที่เริ่มต้น** จากนั้น ดอกเบี้ยตั๋วเงินทั้งหมดที่ยังไม่ได้ลงรายการบัญชีจะถูกยกเลิก และดอกเบี้ยจะถูกคำนวณใหม่จากวันที่ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="89d77-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="89d77-121">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่ซึ่งจะมีการคำนวณดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="89d77-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="89d77-122">ในฟิลด์ **ใช้โพรไฟล์การลงรายการบัญชีจาก** เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89d77-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="89d77-123">มีตัวเลือกโพรไฟล์การลงรายการบัญชี 3 ตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="89d77-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="89d77-124">บัญชี – ใช้โพรไฟล์การลงรายการบัญชีที่ถูกกำหนดให้กับบัญชีลูกค้าสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="89d77-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="89d77-125">เลือก - ใช้โพรไฟล์การลงบัญชีที่คุณเลือกในฟิลด์โพรไฟล์การลงรายการบัญชี </span><span class="sxs-lookup"><span data-stu-id="89d77-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="89d77-126">ธุรกรรม - ใช้แต่ละโพรไฟล์การลงรายการบัญชีจากธุรกรรมที่มีการคำนวณดอกเบี้ยสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="89d77-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="89d77-127">ธุรกรรมที่ไม่มีโพรไฟล์การลงรายการบัญชีที่กำหนด จะใช้โพรไฟล์การลงรายการบัญชีที่ถูกระบุไว้ในพื้นที่ของบัญชีแยกประเภทและภาษีขายของแบบฟอร์มพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="89d77-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="89d77-128">ขยาย fastTab **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="89d77-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="89d77-129">คลิก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="89d77-129">Click **Filter**.</span></span>
9. <span data-ttu-id="89d77-130">ในฟิลด์ **เงื่อนไข** ป้อนรหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="89d77-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="89d77-131">ตัวอย่างเช่น ป้อน 'US-001'</span><span class="sxs-lookup"><span data-stu-id="89d77-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="89d77-132">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="89d77-132">Click **OK**.</span></span>
7. <span data-ttu-id="89d77-133">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="89d77-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="89d77-134">พิมพ์ดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="89d77-134">Print interest notes</span></span>
1. <span data-ttu-id="89d77-135">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > สินเชื่อและการเรียกเก็บเงิน > ดอกเบี้ย > ตรวจทานและดำเนินการดอกเบี้ยตั๋วเงิน**</span><span class="sxs-lookup"><span data-stu-id="89d77-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="89d77-136">ในฟิลด์ **สถานะ** เลือก 'สร้างแล้ว'</span><span class="sxs-lookup"><span data-stu-id="89d77-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="89d77-137">ในฟิลด์ **พิมพ์แล้ว** เลือก 'ไม่มีการพิมพ์'</span><span class="sxs-lookup"><span data-stu-id="89d77-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="89d77-138">คลิก **พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="89d77-138">Click **Print**.</span></span>
5. <span data-ttu-id="89d77-139">ขยาย fastTab **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="89d77-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="89d77-140">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="89d77-140">Click **OK**.</span></span>
7. <span data-ttu-id="89d77-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89d77-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="89d77-142">ลงรายการบัญชีดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="89d77-142">Post the interest note</span></span>
1. <span data-ttu-id="89d77-143">เลือกดอกเบี้ยตั๋วเงินที่พร้อมจะลงรายการบัญชี (สถานะถูกสร้างแล้ว)</span><span class="sxs-lookup"><span data-stu-id="89d77-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="89d77-144">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="89d77-144">Click **Post**.</span></span>
3. <span data-ttu-id="89d77-145">ป้อนวันที่ลงรายการบัญชีสำหรับดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="89d77-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="89d77-146">เลือก ใช่ เพื่อสร้างธุรกรรมบัญชีแยกประเภททั่วไปสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ </span><span class="sxs-lookup"><span data-stu-id="89d77-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="89d77-147">ถ้าคุณไม่ได้เลือก ใช่ ดอกเบี้ยบนดอกเบี้ยตั๋วเงินทั้งหมดของลูกค้าจะมีการสะสมและลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปในธุรกรรมหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="89d77-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="89d77-148">ขยาย fastTab **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="89d77-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="89d77-149">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="89d77-149">Click **OK**.</span></span>
6. <span data-ttu-id="89d77-150">ในฟิลด์ **สถานะ** เลือก 'ลงรายการบัญชีแล้ว'</span><span class="sxs-lookup"><span data-stu-id="89d77-150">In the **Status** field, select 'Posted'.</span></span>

