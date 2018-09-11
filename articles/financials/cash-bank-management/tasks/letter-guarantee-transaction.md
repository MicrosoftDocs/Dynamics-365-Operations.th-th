--- 
title: "ธุรกรรมของหนังสือค้ำประกัน"
description: "กระบวนงานนี้นำไปสู่กระบวนการทำหนังสือค้ำประกัน "
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3b15133106d751c28029862217427e47085044f4
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="0334d-103">ธุรกรรมของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0334d-104">กระบวนงานนี้นำไปสู่กระบวนการทำหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="0334d-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="0334d-105">งานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนการทำให้ขั้นตอนนี้สำเร็จ:</span><span class="sxs-lookup"><span data-stu-id="0334d-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="0334d-106">ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์ของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="0334d-107">สร้างข้อตกลงสินเชื่อธนาคารสำหรับหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="0334d-108">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="0334d-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="0334d-109">สร้างใบสั่งขายโดยมีหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="0334d-110">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0334d-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0334d-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0334d-111">Click New.</span></span>
3. <span data-ttu-id="0334d-112">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0334d-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="0334d-113">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0334d-113">Expand the General section.</span></span>
5. <span data-ttu-id="0334d-114">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0334d-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="0334d-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0334d-116">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0334d-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="0334d-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0334d-118">ในฟิลด์ชนิดเอกสารธของนาคาร ให้เลือก 'หนังสือค้ำประกัน'</span><span class="sxs-lookup"><span data-stu-id="0334d-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="0334d-119">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0334d-119">Click OK.</span></span>
11. <span data-ttu-id="0334d-120">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0334d-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="0334d-121">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0334d-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="0334d-122">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="0334d-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="0334d-123">คลิกแท็บ การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0334d-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="0334d-124">หมายเหตุ: เลือกการควบคุมวันที่จัดส่ง = ไม่มี</span><span class="sxs-lookup"><span data-stu-id="0334d-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="0334d-125">ในฟิลด์วันที่จัดส่งที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0334d-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="0334d-126">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0334d-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="0334d-127">กระบวนการสร้างคำขอหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="0334d-128">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="0334d-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="0334d-129">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="0334d-130">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="0334d-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="0334d-131">คลิกคำขอ เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="0334d-132">ในฟิลด์ชนิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0334d-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="0334d-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0334d-134">ในฟิลด์ค่า ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0334d-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="0334d-135">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="0334d-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="0334d-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-136">Click OK.</span></span>
10. <span data-ttu-id="0334d-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0334d-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="0334d-138">กระบวนการส่งหนังสือค้ำประกันไปที่ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0334d-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="0334d-139">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="0334d-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0334d-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0334d-141">คลิกส่งไปที่ธนาคาร เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="0334d-142">ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0334d-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="0334d-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0334d-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="0334d-145">กระบวนรับหนังสือค้ำประกันจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="0334d-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="0334d-146">คลิกรับจากธนาคาร เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="0334d-147">ในฟิลด์หมายเลขธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0334d-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="0334d-148">ตรวจสอบมูลค่าในฟิลด์การคำนวณกำไรและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0334d-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="0334d-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-149">Click OK.</span></span>
4. <span data-ttu-id="0334d-150">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0334d-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="0334d-151">ตรวจสอบเรกคอร์ดว่า 'ได้รับจากธนาคาร' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0334d-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="0334d-152">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0334d-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="0334d-153">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="0334d-153">Click Lines.</span></span>
    * <span data-ttu-id="0334d-154">ตรวจสอบการลงบัญชีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0334d-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="0334d-155">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0334d-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="0334d-156">กระบวนการมอบหนังสือค้ำประกันให้แก่ผู้รับผลประโยชน์</span><span class="sxs-lookup"><span data-stu-id="0334d-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="0334d-157">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0334d-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0334d-158">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0334d-159">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="0334d-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="0334d-160">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="0334d-161">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="0334d-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="0334d-162">คลิกมอบให้แก่ผู้รับผลประโยชน์ เพื่อกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="0334d-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-163">Click OK.</span></span>
8. <span data-ttu-id="0334d-164">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="0334d-165">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0334d-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0334d-166">คลิกมอบให้แก่ผู้รับผลประโยชน์ เพื่อกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="0334d-167">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-167">Click OK.</span></span>
12. <span data-ttu-id="0334d-168">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0334d-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="0334d-169">ตรวจสอบความถูกต้องของเรกคอร์ดว่า 'มอบให้แก่ผู้รับผลประโยชน์' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0334d-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="0334d-170">กระบวนการเพิ่มมูลค่าของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="0334d-171">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0334d-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0334d-172">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0334d-173">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="0334d-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="0334d-174">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="0334d-175">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="0334d-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="0334d-176">คลิกเพิ่มค่า เพื่อเปิดแบบฟอร์มกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="0334d-177">ในฟิลด์มูลค่าที่จะเพิ่ม ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0334d-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="0334d-178">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-178">Click OK.</span></span>
9. <span data-ttu-id="0334d-179">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="0334d-180">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0334d-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0334d-181">คลิกเพิ่มค่า เพื่อเปิดแบบฟอร์มกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="0334d-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-182">Click OK.</span></span>
13. <span data-ttu-id="0334d-183">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0334d-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="0334d-184">ตรวจสอบเรกคอร์ดว่า 'เพิ่มค่า' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0334d-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="0334d-185">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0334d-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="0334d-186">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0334d-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="0334d-187">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="0334d-187">Click Lines.</span></span>
    * <span data-ttu-id="0334d-188">ตรวจสอบการลงบัญชีรายการสมุดรายวันที่ลงรายการแล้ว</span><span class="sxs-lookup"><span data-stu-id="0334d-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="0334d-189">กระบวนการชำระบัญชีของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="0334d-190">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0334d-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0334d-191">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0334d-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0334d-192">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="0334d-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="0334d-193">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="0334d-194">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="0334d-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="0334d-195">คลิกชำระบัญชี เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="0334d-196">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-196">Click OK.</span></span>
8. <span data-ttu-id="0334d-197">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="0334d-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="0334d-198">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0334d-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0334d-199">คลิกชำระบัญชี เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="0334d-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="0334d-200">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0334d-200">Click OK.</span></span>
12. <span data-ttu-id="0334d-201">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0334d-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="0334d-202">ตรวจสอบเรกคอร์ดว่า 'ชำระบัญชี' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0334d-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="0334d-203">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0334d-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0334d-204">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0334d-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="0334d-205">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="0334d-205">Click Lines.</span></span>
    * <span data-ttu-id="0334d-206">ตรวจสอบการลงบัญชีรายการสมุดรายวันที่ลงรายการแล้ว</span><span class="sxs-lookup"><span data-stu-id="0334d-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="0334d-207">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0334d-207">Close the page.</span></span>


