--- 
title: "เลตเตอร์ออฟเครดิตสำหรับการส่งออก"
description: "กระบวนงานนี้นำไปสู่กระบวนการเลตเตอร์ออฟเครดิตการส่งออก "
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 730a6cc6ed4872f8d0ad92b89665587f472f6791
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="export-letter-of-credit"></a><span data-ttu-id="46f74-103">เลตเตอร์ออฟเครดิตสำหรับการส่งออก</span><span class="sxs-lookup"><span data-stu-id="46f74-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46f74-104">กระบวนงานนี้นำไปสู่กระบวนการเลตเตอร์ออฟเครดิตการส่งออก </span><span class="sxs-lookup"><span data-stu-id="46f74-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="46f74-105">เลตเตอร์ออฟเครดิตคือ ข้อตกลงที่ออก โดยธนาคาร ที่ธนาคารตกลงเพื่อให้แน่ใจว่าการชำระเงินในนามของผู้ซื้อ ว่าตรงตามเงื่อนไขของข้อตกลงระหว่างผู้ซื้อและผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="46f74-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="46f74-106">ดำเนินงานกระบวนงาน 'ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์' และกระบวนงาน 'เลตเตอร์ออฟเครดิต สร้างข้อตกลงสินเชื่อธนาคาร' ก่อนกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="46f74-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="46f74-107">ต้องเลือกบริษัทสาธิต USMF เพื่อเรียกใช้กระบวนงานนี้ได้อย่างเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="46f74-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="46f74-108">สร้างใบสั่งขายสำหรับเลตเตอร์ออฟเครดิตการส่งออก</span><span class="sxs-lookup"><span data-stu-id="46f74-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="46f74-109">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="46f74-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="46f74-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="46f74-110">Click New.</span></span>
3. <span data-ttu-id="46f74-111">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="46f74-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="46f74-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="46f74-114">ขยายหรือยุบส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="46f74-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="46f74-115">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46f74-116">เลือกไซต์ที่สินค้าที่จะออกได้ถูกจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="46f74-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="46f74-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="46f74-118">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46f74-119">เลือกคลังสินค้าที่สินค้าที่จะออกได้ถูกจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="46f74-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="46f74-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="46f74-121">สังเกตว่า ฟิลด์ 'ชนิดเอกสารธนาคาร' ควรถูกเลือกกับค่า 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="46f74-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="46f74-122">ในฟิลด์ชนิดของเอกสารธนาคาร ให้เลือก 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="46f74-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="46f74-123">ขยายหรือยุบส่วนการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="46f74-124">เลือกการควบคุมวันที่จัดส่ง = ไม่มี</span><span class="sxs-lookup"><span data-stu-id="46f74-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="46f74-125">ในฟิลด์วันที่ขอรับสินค้า ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46f74-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="46f74-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="46f74-126">Click OK.</span></span>
15. <span data-ttu-id="46f74-127">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46f74-128">เลือกสินค้าที่ต้องการจะออก/ขาย</span><span class="sxs-lookup"><span data-stu-id="46f74-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="46f74-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="46f74-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="46f74-131">ในฟิลด์ราคาต่อหน่วย ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="46f74-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="46f74-132">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="46f74-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="46f74-133">คลิกแท็บการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="46f74-134">ในฟิลด์วันที่จัดส่งที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46f74-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="46f74-135">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46f74-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="46f74-136">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="46f74-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="46f74-137">คลิกเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="46f74-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="46f74-138">ในฟิลด์หมายเลขเอกสารธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="46f74-139">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="46f74-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="46f74-140">ขยายหรือยุบส่วนรายละเอียดธนาคาร</span><span class="sxs-lookup"><span data-stu-id="46f74-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="46f74-141">ในฟิลด์ธนาคารผู้ออก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="46f74-142">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="46f74-143">ในฟิลด์ธนาคารผู้แจ้งเครดิต ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="46f74-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="46f74-145">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="46f74-146">คลิกนำการจัดส่งของใบสั่งขายมาใช้</span><span class="sxs-lookup"><span data-stu-id="46f74-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="46f74-147">คลิกออกเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="46f74-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="46f74-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="46f74-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="46f74-149">ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-149">Post Packing slip</span></span>
1. <span data-ttu-id="46f74-150">ในบานหน้าต่างการดำเนินการ ให้คลิก เบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="46f74-151">คลิก ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="46f74-152">ขยายหรือยุบส่วนพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="46f74-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="46f74-153">ในฟิลด์ปริมาณ ให้เลือก "ทั้งหมด"</span><span class="sxs-lookup"><span data-stu-id="46f74-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="46f74-154">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="46f74-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="46f74-155">ในฟิลด์วันที่ในบันทึกการจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46f74-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="46f74-156">เลือกหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="46f74-157">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="46f74-158">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="46f74-158">Click OK.</span></span>
10. <span data-ttu-id="46f74-159">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="46f74-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="46f74-160">ลงรายการบัญชีใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="46f74-160">Post sales invoice</span></span>
1. <span data-ttu-id="46f74-161">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="46f74-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="46f74-162">คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="46f74-162">Click Invoice.</span></span>
3. <span data-ttu-id="46f74-163">ขยายหรือยุบส่วนภาพรวม</span><span class="sxs-lookup"><span data-stu-id="46f74-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="46f74-164">เลือกหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="46f74-165">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="46f74-166">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="46f74-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="46f74-167">ในฟิลด์ วันที่ในใบแจ้งหนี้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46f74-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="46f74-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="46f74-168">Click OK.</span></span>
9. <span data-ttu-id="46f74-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="46f74-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="46f74-170">สถานะการจัดส่งเอกสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="46f74-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="46f74-171">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="46f74-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="46f74-172">คลิกเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="46f74-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="46f74-173">ขยายหรือยุบส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="46f74-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="46f74-174">หมายเหตุ: ฟิลด์ 'เอกสารที่ส่ง' ควรถูกตั้งเป็น 'ใช่'</span><span class="sxs-lookup"><span data-stu-id="46f74-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="46f74-175">ตรวจสอบเลตเตอร์ออฟเครดิตสำหรับการส่งออก</span><span class="sxs-lookup"><span data-stu-id="46f74-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="46f74-176">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > เลตเตอร์ออฟเครดิตสำหรับการส่งออกและการเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="46f74-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="46f74-177">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46f74-178">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="46f74-179">ตรวจสอบว่า เลตเตอร์ออฟเครดิตการส่งออกมีสถานะการจัดส่งเป็น 'ออกใบแจ้งหนี้แล้ว'</span><span class="sxs-lookup"><span data-stu-id="46f74-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="46f74-180">การชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="46f74-180">Customer payment</span></span>
1. <span data-ttu-id="46f74-181">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="46f74-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="46f74-182">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="46f74-182">Click New.</span></span>
3. <span data-ttu-id="46f74-183">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="46f74-184">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="46f74-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="46f74-185">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="46f74-186">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="46f74-186">Click Lines.</span></span>
7. <span data-ttu-id="46f74-187">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="46f74-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="46f74-188">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="46f74-189">คลิกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="46f74-189">Click Settlement.</span></span>
10. <span data-ttu-id="46f74-190">เลือกกล่องกาเครื่องหมายในส่วนหัวของยอดรวม</span><span class="sxs-lookup"><span data-stu-id="46f74-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="46f74-191">หมายเหตุ: ตั้งค่าฟิลด์แสดงเป็น 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="46f74-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="46f74-192">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="46f74-193">เลือกหรือล้างกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="46f74-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="46f74-194">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="46f74-194">Click OK.</span></span>
14. <span data-ttu-id="46f74-195">คลิกแท็บการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="46f74-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="46f74-196">ตรวจสอบหมายเลขเอกสารของธนาคารและรายละเอียดหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="46f74-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="46f74-197">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="46f74-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="46f74-198">ตรวจสอบเลตเตอร์ออฟเครดิตสำหรับการส่งออกหลังจากการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="46f74-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="46f74-199">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > เลตเตอร์ออฟเครดิตสำหรับการส่งออกและการเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="46f74-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="46f74-200">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="46f74-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46f74-201">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="46f74-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="46f74-202">ตรวจสอบว่า สถานะการจัดส่ง = การชำระเงินที่ได้รับ และยอดดุล = 0.00</span><span class="sxs-lookup"><span data-stu-id="46f74-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


