---
title: ธุรกรรมของหนังสือค้ำประกัน
description: 'กระบวนงานนี้นำไปสู่กระบวนการทำหนังสือค้ำประกัน '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566849cfcedd29f4bb92d08a17b67e16b1cbc372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225380"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="7991c-103">ธุรกรรมของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7991c-104">กระบวนงานนี้นำไปสู่กระบวนการทำหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="7991c-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="7991c-105">งานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนการทำให้ขั้นตอนนี้สำเร็จ:</span><span class="sxs-lookup"><span data-stu-id="7991c-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="7991c-106">ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์ของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="7991c-107">สร้างข้อตกลงสินเชื่อธนาคารสำหรับหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="7991c-108">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="7991c-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="7991c-109">สร้างใบสั่งขายโดยมีหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="7991c-110">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7991c-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7991c-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7991c-111">Click New.</span></span>
3. <span data-ttu-id="7991c-112">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7991c-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="7991c-113">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="7991c-113">Expand the General section.</span></span>
5. <span data-ttu-id="7991c-114">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7991c-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="7991c-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7991c-116">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7991c-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="7991c-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7991c-118">ในฟิลด์ชนิดเอกสารธของนาคาร ให้เลือก 'หนังสือค้ำประกัน'</span><span class="sxs-lookup"><span data-stu-id="7991c-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="7991c-119">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7991c-119">Click OK.</span></span>
11. <span data-ttu-id="7991c-120">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7991c-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="7991c-121">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7991c-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="7991c-122">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="7991c-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="7991c-123">คลิกแท็บ การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7991c-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="7991c-124">หมายเหตุ: เลือกการควบคุมวันที่จัดส่ง = ไม่มี</span><span class="sxs-lookup"><span data-stu-id="7991c-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="7991c-125">ในฟิลด์วันที่จัดส่งที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7991c-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="7991c-126">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7991c-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="7991c-127">กระบวนการสร้างคำขอหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="7991c-128">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="7991c-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="7991c-129">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="7991c-130">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="7991c-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="7991c-131">คลิกคำขอ เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="7991c-132">ในฟิลด์ชนิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7991c-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="7991c-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7991c-134">ในฟิลด์ค่า ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7991c-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="7991c-135">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7991c-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="7991c-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-136">Click OK.</span></span>
10. <span data-ttu-id="7991c-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7991c-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="7991c-138">กระบวนการส่งหนังสือค้ำประกันไปที่ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7991c-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="7991c-139">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="7991c-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7991c-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7991c-141">คลิกส่งไปที่ธนาคาร เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="7991c-142">ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7991c-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="7991c-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7991c-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="7991c-145">กระบวนรับหนังสือค้ำประกันจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7991c-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="7991c-146">คลิกรับจากธนาคาร เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="7991c-147">ในฟิลด์หมายเลขธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7991c-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="7991c-148">ตรวจสอบมูลค่าในฟิลด์การคำนวณกำไรและค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7991c-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="7991c-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-149">Click OK.</span></span>
4. <span data-ttu-id="7991c-150">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7991c-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="7991c-151">ตรวจสอบเรกคอร์ดว่า 'ได้รับจากธนาคาร' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7991c-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="7991c-152">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7991c-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="7991c-153">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="7991c-153">Click Lines.</span></span>
    * <span data-ttu-id="7991c-154">ตรวจสอบการลงบัญชีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7991c-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="7991c-155">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7991c-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="7991c-156">กระบวนการมอบหนังสือค้ำประกันให้แก่ผู้รับผลประโยชน์</span><span class="sxs-lookup"><span data-stu-id="7991c-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="7991c-157">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7991c-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7991c-158">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7991c-159">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="7991c-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="7991c-160">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="7991c-161">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="7991c-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="7991c-162">คลิกมอบให้แก่ผู้รับผลประโยชน์ เพื่อกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="7991c-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-163">Click OK.</span></span>
8. <span data-ttu-id="7991c-164">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="7991c-165">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7991c-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="7991c-166">คลิกมอบให้แก่ผู้รับผลประโยชน์ เพื่อกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="7991c-167">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-167">Click OK.</span></span>
12. <span data-ttu-id="7991c-168">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7991c-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="7991c-169">ตรวจสอบความถูกต้องของเรกคอร์ดว่า 'มอบให้แก่ผู้รับผลประโยชน์' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7991c-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="7991c-170">กระบวนการเพิ่มมูลค่าของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="7991c-171">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7991c-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7991c-172">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7991c-173">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="7991c-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="7991c-174">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="7991c-175">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="7991c-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="7991c-176">คลิกเพิ่มค่า เพื่อเปิดแบบฟอร์มกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="7991c-177">ในฟิลด์มูลค่าที่จะเพิ่ม ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="7991c-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="7991c-178">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-178">Click OK.</span></span>
9. <span data-ttu-id="7991c-179">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="7991c-180">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7991c-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="7991c-181">คลิกเพิ่มค่า เพื่อเปิดแบบฟอร์มกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="7991c-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-182">Click OK.</span></span>
13. <span data-ttu-id="7991c-183">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7991c-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="7991c-184">ตรวจสอบเรกคอร์ดว่า 'เพิ่มค่า' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7991c-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="7991c-185">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7991c-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="7991c-186">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7991c-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="7991c-187">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="7991c-187">Click Lines.</span></span>
    * <span data-ttu-id="7991c-188">ตรวจสอบการลงบัญชีรายการสมุดรายวันที่ลงรายการแล้ว</span><span class="sxs-lookup"><span data-stu-id="7991c-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="7991c-189">กระบวนการชำระบัญชีของหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="7991c-190">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7991c-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7991c-191">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7991c-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7991c-192">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="7991c-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="7991c-193">คลิกหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="7991c-194">บนบานหน้าต่างดำเนินการ ให้คลิกหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="7991c-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="7991c-195">คลิกชำระบัญชี เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="7991c-196">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-196">Click OK.</span></span>
8. <span data-ttu-id="7991c-197">ไปที่ การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > หนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="7991c-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="7991c-198">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7991c-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="7991c-199">คลิกชำระบัญชี เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7991c-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="7991c-200">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7991c-200">Click OK.</span></span>
12. <span data-ttu-id="7991c-201">ขยายส่วนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7991c-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="7991c-202">ตรวจสอบเรกคอร์ดว่า 'ชำระบัญชี' หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7991c-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="7991c-203">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7991c-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="7991c-204">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7991c-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="7991c-205">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="7991c-205">Click Lines.</span></span>
    * <span data-ttu-id="7991c-206">ตรวจสอบการลงบัญชีรายการสมุดรายวันที่ลงรายการแล้ว</span><span class="sxs-lookup"><span data-stu-id="7991c-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="7991c-207">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7991c-207">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]