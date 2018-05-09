--- 
title: "ดำเนินการจดหมายเรียกเก็บเงิน"
description: "กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีจดหมายเรียกเก็บเงิน "
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.openlocfilehash: cd53744abc4c43b8c7b97ee5cd057fff684c32e5
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="7251a-103">ดำเนินการจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7251a-104">กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีจดหมายเรียกเก็บเงิน </span><span class="sxs-lookup"><span data-stu-id="7251a-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="7251a-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="7251a-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="7251a-106">ตั้งค่าลำดับจดหมายเรียกเก็บเงินบนโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="7251a-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="7251a-107">ไปที่สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > โพรไฟล์การลงรายการบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7251a-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="7251a-108">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="7251a-108">Click Edit.</span></span>
    * <span data-ttu-id="7251a-109">เลือกลำดับจดหมายเรียกเก็บเงินจากรายการแบบหล่นลง </span><span class="sxs-lookup"><span data-stu-id="7251a-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="7251a-110">ถ้าคุณไม่ต้องการสร้างจดหมายเรียกเก็บเงินสำหรับธุรกรรมโดยใช้โพรไฟล์การลงบัญชีนี้ ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="7251a-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="7251a-111">แท็บข้อจำกัดตารางช่วยให้คุณสามารถเปลี่ยนวิธีการประมวลผลจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="7251a-112">ถ้าฟิลด์นี้ถูกตั้งค่าเป็น ใช่ แล้วจดหมายเรียกเก็บเงินจะถูกสร้างสำหรับโพรไฟล์การลงบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="7251a-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="7251a-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7251a-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="7251a-114">สร้างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-114">Create collection letters</span></span>
1. <span data-ttu-id="7251a-115">ไปที่สินเชื่อและการเรียกเก็บเงิน > จดหมายเรียกเก็บเงิน > สร้างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="7251a-116">คุณต้องเลือกชนิดของธุรกรรมซึ่งคุณจะเรียกเก็บจดหมาย </span><span class="sxs-lookup"><span data-stu-id="7251a-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="7251a-117">ธุรกรรมที่ค้างอยู่ทั้งหมดของชนิดนี้ทั้งหมดจะถูกรวมในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="7251a-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="7251a-118">ในฟิลด์จดหมายเรียกเก็บเงิน เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7251a-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="7251a-119">ป้อนวันที่ของจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="7251a-120">ตัวเลือกโพรไฟล์การลงรายการบัญชีมี 2 ตัวเลือก:   บัญชี - ใช้โพรไฟล์การลงบัญชีที่ถูกกำหนดให้กับบัญชีลูกค้าสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="7251a-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="7251a-121">เลือก - ใช้โพรไฟล์การลงบัญชีที่คุณเลือกในฟิลด์โพรไฟล์การลงรายการบัญชี </span><span class="sxs-lookup"><span data-stu-id="7251a-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="7251a-122">เลือกโพรไฟล์การลงรายการบัญชีถ้าคุณเปลี่ยน "ใช้โพรไฟล์ลงบัญชีจาก" เป็น "เลือก"</span><span class="sxs-lookup"><span data-stu-id="7251a-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="7251a-123">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="7251a-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="7251a-124">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="7251a-124">Click Filter.</span></span>
6. <span data-ttu-id="7251a-125">ในฟิลด์เกณฑ์ ในฟิลด์เกณฑ์ ให้ป้อนรหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7251a-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="7251a-126">ตัวอย่างเช่น ป้อน 'US-001'..</span><span class="sxs-lookup"><span data-stu-id="7251a-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="7251a-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7251a-127">Click OK.</span></span>
8. <span data-ttu-id="7251a-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7251a-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="7251a-129">พิมพ์จดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-129">Print collection letters</span></span>
1. <span data-ttu-id="7251a-130">ไปที่สินเชื่อและการเรียกเก็บเงิน > จดหมายเรียกเก็บเงิน > ตรวจทานและดำเนินการจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="7251a-131">ในฟิลด์สถานะ เลือก 'สร้างแล้ว'</span><span class="sxs-lookup"><span data-stu-id="7251a-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="7251a-132">ในฟิลด์พิมพ์ เลือก 'ไม่มีการพิมพ์'</span><span class="sxs-lookup"><span data-stu-id="7251a-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="7251a-133">คลิก พิมพ์</span><span class="sxs-lookup"><span data-stu-id="7251a-133">Click Print.</span></span>
5. <span data-ttu-id="7251a-134">คลิกบันทึกจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="7251a-135">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="7251a-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7251a-136">ป้อนวันที่ตัดยอดสำหรับการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="7251a-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="7251a-137">คลิกตกลงเพื่อพิมพ์จดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="7251a-138">ลงรายการบัญชีจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-138">Post the collection letter</span></span>
1. <span data-ttu-id="7251a-139">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="7251a-139">Click Post.</span></span>
2. <span data-ttu-id="7251a-140">ป้อนวันที่ลงรายการบัญชีสำหรับจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="7251a-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="7251a-141">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="7251a-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="7251a-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7251a-142">Click OK.</span></span>
5. <span data-ttu-id="7251a-143">ในฟิลด์สถานะ เลือก 'ลงรายการบัญชีแล้ว'</span><span class="sxs-lookup"><span data-stu-id="7251a-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="7251a-144">ในฟิลด์พิมพ์แล้ว ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7251a-144">In the Printed field, select an option.</span></span>


