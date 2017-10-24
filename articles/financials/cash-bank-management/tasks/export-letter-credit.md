--- 
title: "เลตเตอร์ออฟเครดิตสำหรับการส่งออก"
description: "กระบวนงานนี้นำไปสู่กระบวนการเลตเตอร์ออฟเครดิตการส่งออก "
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa4b57825bcf81778d91ee01484511bb40f6bd7
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="c4a45-103">เลตเตอร์ออฟเครดิตสำหรับการส่งออก</span><span class="sxs-lookup"><span data-stu-id="c4a45-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4a45-104">กระบวนงานนี้นำไปสู่กระบวนการเลตเตอร์ออฟเครดิตการส่งออก </span><span class="sxs-lookup"><span data-stu-id="c4a45-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="c4a45-105">เลตเตอร์ออฟเครดิตคือ ข้อตกลงที่ออก โดยธนาคาร ที่ธนาคารตกลงเพื่อให้แน่ใจว่าการชำระเงินในนามของผู้ซื้อ ว่าตรงตามเงื่อนไขของข้อตกลงระหว่างผู้ซื้อและผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="c4a45-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="c4a45-106">ดำเนินงานกระบวนงาน 'ตั้งค่าสินเชื่อธนาคารและการลงรายการบัญชีโพรไฟล์' และกระบวนงาน 'เลตเตอร์ออฟเครดิต สร้างข้อตกลงสินเชื่อธนาคาร' ก่อนกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="c4a45-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="c4a45-107">ต้องเลือกบริษัทสาธิต USMF เพื่อเรียกใช้กระบวนงานนี้ได้อย่างเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c4a45-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="c4a45-108">สร้างใบสั่งขายสำหรับเลตเตอร์ออฟเครดิตการส่งออก</span><span class="sxs-lookup"><span data-stu-id="c4a45-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="c4a45-109">ไปที่บัญชีลูกหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c4a45-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c4a45-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4a45-110">Click New.</span></span>
3. <span data-ttu-id="c4a45-111">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c4a45-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c4a45-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c4a45-114">ขยายหรือยุบส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="c4a45-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="c4a45-115">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c4a45-116">เลือกไซต์ที่สินค้าที่จะออกได้ถูกจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="c4a45-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="c4a45-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c4a45-118">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c4a45-119">เลือกคลังสินค้าที่สินค้าที่จะออกได้ถูกจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="c4a45-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="c4a45-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c4a45-121">สังเกตว่า ฟิลด์ 'ชนิดเอกสารธนาคาร' ควรถูกเลือกกับค่า 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="c4a45-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="c4a45-122">ในฟิลด์ชนิดของเอกสารธนาคาร ให้เลือก 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="c4a45-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="c4a45-123">ขยายหรือยุบส่วนการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="c4a45-124">เลือกการควบคุมวันที่จัดส่ง = ไม่มี</span><span class="sxs-lookup"><span data-stu-id="c4a45-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="c4a45-125">ในฟิลด์วันที่ขอรับสินค้า ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c4a45-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="c4a45-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c4a45-126">Click OK.</span></span>
15. <span data-ttu-id="c4a45-127">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c4a45-128">เลือกสินค้าที่ต้องการจะออก/ขาย</span><span class="sxs-lookup"><span data-stu-id="c4a45-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="c4a45-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="c4a45-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c4a45-131">ในฟิลด์ราคาต่อหน่วย ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="c4a45-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="c4a45-132">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="c4a45-133">คลิกแท็บการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="c4a45-134">ในฟิลด์วันที่จัดส่งที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c4a45-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="c4a45-135">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c4a45-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="c4a45-136">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="c4a45-137">คลิกเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="c4a45-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="c4a45-138">ในฟิลด์หมายเลขเอกสารธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="c4a45-139">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c4a45-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="c4a45-140">ขยายหรือยุบส่วนรายละเอียดธนาคาร</span><span class="sxs-lookup"><span data-stu-id="c4a45-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="c4a45-141">ในฟิลด์ธนาคารผู้ออก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="c4a45-142">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="c4a45-143">ในฟิลด์ธนาคารผู้แจ้งเครดิต ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="c4a45-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="c4a45-145">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="c4a45-146">คลิกนำการจัดส่งของใบสั่งขายมาใช้</span><span class="sxs-lookup"><span data-stu-id="c4a45-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="c4a45-147">คลิกออกเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="c4a45-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="c4a45-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c4a45-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="c4a45-149">ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-149">Post Packing slip</span></span>
1. <span data-ttu-id="c4a45-150">ในบานหน้าต่างการดำเนินการ ให้คลิก เบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="c4a45-151">คลิก ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="c4a45-152">ขยายหรือยุบส่วนพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4a45-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="c4a45-153">ในฟิลด์ปริมาณ ให้เลือก "ทั้งหมด"</span><span class="sxs-lookup"><span data-stu-id="c4a45-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="c4a45-154">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="c4a45-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="c4a45-155">ในฟิลด์วันที่ในบันทึกการจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c4a45-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="c4a45-156">เลือกหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="c4a45-157">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c4a45-158">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c4a45-158">Click OK.</span></span>
10. <span data-ttu-id="c4a45-159">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c4a45-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="c4a45-160">ลงรายการบัญชีใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="c4a45-160">Post sales invoice</span></span>
1. <span data-ttu-id="c4a45-161">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c4a45-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="c4a45-162">คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c4a45-162">Click Invoice.</span></span>
3. <span data-ttu-id="c4a45-163">ขยายหรือยุบส่วนภาพรวม</span><span class="sxs-lookup"><span data-stu-id="c4a45-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="c4a45-164">เลือกหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="c4a45-165">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c4a45-166">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="c4a45-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="c4a45-167">ในฟิลด์ วันที่ในใบแจ้งหนี้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c4a45-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="c4a45-168">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c4a45-168">Click OK.</span></span>
9. <span data-ttu-id="c4a45-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c4a45-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="c4a45-170">สถานะการจัดส่งเอกสารแล้ว</span><span class="sxs-lookup"><span data-stu-id="c4a45-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="c4a45-171">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="c4a45-172">คลิกเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="c4a45-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="c4a45-173">ขยายหรือยุบส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="c4a45-174">หมายเหตุ: ฟิลด์ 'เอกสารที่ส่ง' ควรถูกตั้งเป็น 'ใช่'</span><span class="sxs-lookup"><span data-stu-id="c4a45-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="c4a45-175">ตรวจสอบเลตเตอร์ออฟเครดิตสำหรับการส่งออก</span><span class="sxs-lookup"><span data-stu-id="c4a45-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="c4a45-176">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > เลตเตอร์ออฟเครดิตสำหรับการส่งออกและการเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="c4a45-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="c4a45-177">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c4a45-178">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c4a45-179">ตรวจสอบว่า เลตเตอร์ออฟเครดิตการส่งออกมีสถานะการจัดส่งเป็น 'ออกใบแจ้งหนี้แล้ว'</span><span class="sxs-lookup"><span data-stu-id="c4a45-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="c4a45-180">การชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c4a45-180">Customer payment</span></span>
1. <span data-ttu-id="c4a45-181">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c4a45-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c4a45-182">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c4a45-182">Click New.</span></span>
3. <span data-ttu-id="c4a45-183">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c4a45-184">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c4a45-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c4a45-185">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c4a45-186">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-186">Click Lines.</span></span>
7. <span data-ttu-id="c4a45-187">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="c4a45-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="c4a45-188">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="c4a45-189">คลิกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c4a45-189">Click Settlement.</span></span>
10. <span data-ttu-id="c4a45-190">เลือกกล่องกาเครื่องหมายในส่วนหัวของยอดรวม</span><span class="sxs-lookup"><span data-stu-id="c4a45-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="c4a45-191">หมายเหตุ: ตั้งค่าฟิลด์แสดงเป็น 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="c4a45-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="c4a45-192">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="c4a45-193">เลือกหรือล้างกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="c4a45-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="c4a45-194">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c4a45-194">Click OK.</span></span>
14. <span data-ttu-id="c4a45-195">คลิกแท็บการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c4a45-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="c4a45-196">ตรวจสอบหมายเลขเอกสารของธนาคารและรายละเอียดหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c4a45-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="c4a45-197">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c4a45-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="c4a45-198">ตรวจสอบเลตเตอร์ออฟเครดิตสำหรับการส่งออกหลังจากการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c4a45-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="c4a45-199">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > เลตเตอร์ออฟเครดิตสำหรับการส่งออกและการเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="c4a45-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="c4a45-200">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c4a45-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c4a45-201">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c4a45-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c4a45-202">ตรวจสอบว่า สถานะการจัดส่ง = การชำระเงินที่ได้รับ และยอดดุล = 0.00</span><span class="sxs-lookup"><span data-stu-id="c4a45-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


