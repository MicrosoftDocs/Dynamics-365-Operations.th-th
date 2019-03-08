---
title: ดำเนินการจดหมายเรียกเก็บเงิน
description: 'กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีจดหมายเรียกเก็บเงิน '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "358864"
---
# <a name="process-collection-letters"></a><span data-ttu-id="d4e2b-103">ดำเนินการจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4e2b-104">กระบวนงานนี้แสดงวิธีการสร้าง การพิมพ์ และการลงรายการบัญชีจดหมายเรียกเก็บเงิน </span><span class="sxs-lookup"><span data-stu-id="d4e2b-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="d4e2b-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="d4e2b-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="d4e2b-106">ตั้งค่าลำดับจดหมายเรียกเก็บเงินบนโพรไฟล์การลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="d4e2b-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="d4e2b-107">ไปที่ **สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > โพรไฟล์การลงรายการบัญชีลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="d4e2b-108">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-108">Click **Edit**.</span></span>
3. <span data-ttu-id="d4e2b-109">เลือกลำดับจดหมายเรียกเก็บเงินจากรายการแบบหล่นลง </span><span class="sxs-lookup"><span data-stu-id="d4e2b-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="d4e2b-110">ถ้าคุณไม่ต้องการสร้างจดหมายเรียกเก็บเงินสำหรับธุรกรรมโดยใช้โพรไฟล์การลงบัญชีนี้ ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="d4e2b-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="d4e2b-111">ขยายแท็บข้อจำกัดตารางเพื่อเปลี่ยนวิธีการประมวลผลจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="d4e2b-112">ถ้าฟิลด์นี้ถูกตั้งค่าเป็น **ใช่** แล้วจดหมายเรียกเก็บเงินจะถูกสร้างสำหรับโพรไฟล์การลงบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="d4e2b-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="d4e2b-113">สร้างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-113">Create collection letters</span></span>
1. <span data-ttu-id="d4e2b-114">ไปที่ **สินเชื่อและการเรียกเก็บเงิน > จดหมายเรียกเก็บเงิน > สร้างจดหมายเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="d4e2b-115">เลือกชนิดธุรกรรมซึ่งคุณจะเรียกเก็บจดหมาย</span><span class="sxs-lookup"><span data-stu-id="d4e2b-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="d4e2b-116">ธุรกรรมที่ค้างอยู่ทั้งหมดของชนิดนี้ทั้งหมดจะถูกรวมในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="d4e2b-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="d4e2b-117">ในฟิลด์ **จดหมายเรียกเก็บเงิน** เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d4e2b-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="d4e2b-118">ป้อนวันที่ของจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="d4e2b-119">เลือกโพรไฟล์การลงรายการบัญชี ถ้าคุณเปลี่ยน **ใช้โพรไฟล์การลงรายการบัญชีจาก** เป็น **เลือก**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="d4e2b-120">มีตัวเลือกโพรไฟล์การลงรายการบัญชี 2 ตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="d4e2b-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="d4e2b-121">**บัญชี** – ใช้โพรไฟล์การลงรายการบัญชีที่ถูกกำหนดให้กับบัญชีลูกค้าสำหรับดอกเบี้ยตั๋วเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="d4e2b-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="d4e2b-122">**เลือก** – ใช้โพรไฟล์การลงบัญชีที่คุณเลือกในฟิลด์ **โพรไฟล์การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="d4e2b-123">ขยายส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="d4e2b-124">คลิก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-124">Click **Filter**.</span></span>
7. <span data-ttu-id="d4e2b-125">ในฟิลด์ **เงื่อนไข** ป้อนรหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d4e2b-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="d4e2b-126">ตัวอย่างเช่น ป้อน 'US-001'</span><span class="sxs-lookup"><span data-stu-id="d4e2b-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="d4e2b-127">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="d4e2b-127">Click **OK**.</span></span>
9. <span data-ttu-id="d4e2b-128">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="d4e2b-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="d4e2b-129">พิมพ์จดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-129">Print collection letters</span></span>
1. <span data-ttu-id="d4e2b-130">ไปที่ **สินเชื่อและการเรียกเก็บเงิน > จดหมายเรียกเก็บเงิน > ตรวจทานและดำเนินการจดหมายเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="d4e2b-131">ในฟิลด์ **สถานะ** เลือก **สร้างแล้ว**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="d4e2b-132">ในฟิลด์ **พิมพ์แล้ว** เลือก **ไม่มีการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="d4e2b-133">คลิก **พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-133">Click **Print**.</span></span>
5. <span data-ttu-id="d4e2b-134">คลิก **บันทึกจดหมายเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="d4e2b-135">ขยายส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="d4e2b-136">ป้อนวันที่ตัดยอดสำหรับการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d4e2b-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="d4e2b-137">คลิก **ตกลง** เพื่อพิมพ์จดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="d4e2b-138">ลงรายการบัญชีจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="d4e2b-139">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-139">Click **Post**.</span></span>
   2. <span data-ttu-id="d4e2b-140">ป้อนวันที่ลงรายการบัญชีสำหรับจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="d4e2b-141">ขยายส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="d4e2b-142">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="d4e2b-142">Click **OK**.</span></span>
   5. <span data-ttu-id="d4e2b-143">ในฟิลด์ **สถานะ** เลือก **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="d4e2b-144">ในฟิลด์ **พิมพ์แล้ว** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d4e2b-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="d4e2b-145">ควบคุมจดหมายเรียกเก็บเงินที่ระดับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d4e2b-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="d4e2b-146">นอกจากนี้ คุณยังสามารถตั้งค่าจดหมายเรียกเก็บเงินที่ระดับลูกค้า เพื่อให้มีการติดตามรหัสจดหมายเรียกเก็บเงินสำหรับแต่ละธุรกรรม แต่การประมวลผลจดหมายเรียกเก็บเงินจะยึดตามระดับจดหมายเรียกเก็บเงินเดียวที่ถูกจัดเก็บสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d4e2b-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="d4e2b-147">จดหมายเรียกเก็บเงินเดียวจะประกอบด้วยธุรกรรมทั้งหมดที่พ้นกำหนดสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d4e2b-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="d4e2b-148">เนื่องจากขณะนี้มีการติดตามจำนวนวันปลอดหนี้ในระดับลูกค้า จดหมายเรียกเก็บเงินถัดไปจะไม่ถูกส่งจนกว่าจะมีการส่งผ่านจำนวนวันปลอดหนี้สำหรับจดหมายเรียกเก็บเงินถัดไปตามลำดับ ถึงแม้ว่าธุรกรรมจะกลายเป็นพ้นกำหนด หลังจากจดหมายเรียกเก็บเงินล่าสุดถูกส่งไป</span><span class="sxs-lookup"><span data-stu-id="d4e2b-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="d4e2b-149">ตัวเลือกนี้ช่วยลดจำนวนของจดหมายเรียกเก็บเงินที่คุณจะส่งให้ลูกค้าแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="d4e2b-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="d4e2b-150">ตั้งค่าลูกค้าเพื่อควบคุมจดหมายเรียกเก็บเงินที่ระดับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d4e2b-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="d4e2b-151">ไปยัง **สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > พารามิเตอร์ลูกหนี้** และคลิกแท็บ **คอลเลกชัน**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="d4e2b-152">เปลี่ยนค่าของ **สร้างจดหมายเรียกเก็บเงินสำหรับแต่ละ** เป็น **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="d4e2b-153">ไปที่ **สินเชื่อและการเรียกเก็บเงิน > จดหมายเรียกเก็บเงิน > ตรวจทานและดำเนินการจดหมายเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="d4e2b-154">ระบบจะสร้างจดหมายเรียกเก็บเงินรายการเดียวเท่านั้นสำหรับลูกค้าที่มีธุรกรรมที่พ้นกำหนดชำระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d4e2b-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="d4e2b-155">ละเว้นการชำระเงินและใบลดหนี้ เมื่อมีการคำนวณรหัสจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="d4e2b-156">ถ้าคุณรวมการชำระเงินและใบลดหนี้ในธุรกรรมที่จะรวมอยู่ในจดหมายเรียกเก็บเงิน คุณอาจมีการชำระเงินหรือใบลดหนี้ที่จะทริกเกอร์จดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d4e2b-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="d4e2b-157">คุณสามารถควบคุมวิธีการที่การชำระเงินและใบลดหนี้ควบคุมรหัสจดหมายเรียกเก็บเงินโดยการเปลี่ยนค่าของพารามิเตอร์ **ละเว้นการชำระเงินและใบลดหนี้ เมื่อคำนวณรหัสจดหมายเรียกเก็บเงิน** ได้</span><span class="sxs-lookup"><span data-stu-id="d4e2b-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="d4e2b-158">ในการละเว้นการชำระเงินและใบลดหนี้ เมื่อมีการคำนวณรหัสจดหมายเรียกเก็บเงิน ทำการดำเนินการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d4e2b-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="d4e2b-159">ไปยัง **สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > พารามิเตอร์ลูกหนี้** และคลิกแท็บ **คอลเลกชัน**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="d4e2b-160">เปลี่ยนค่าของ **ละเว้นการชำระเงินและใบลดหนี้ เมื่อมีการคำนวณรหัสจดหมายเรียกเก็บเงิน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d4e2b-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
