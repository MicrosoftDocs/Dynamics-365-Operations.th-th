--- 
title: "เลตเตอร์ออฟเครดิตสำหรับการนำเข้า"
description: "กระบวนงานนี้นำไปสู่กระบวนการการนำเข้าเลตเตอร์ออฟเครดิต "
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 38d012fab8dc9ea06b55b960d72578af31291c09
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="import-a-letter-of-credit"></a><span data-ttu-id="f173b-103">เลตเตอร์ออฟเครดิตสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-103">Import a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f173b-104">กระบวนงานนี้นำไปสู่กระบวนการการนำเข้าเลตเตอร์ออฟเครดิต </span><span class="sxs-lookup"><span data-stu-id="f173b-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="f173b-105">ต้องตั้งค่าต่อไปนี้ก่อนที่กระบวนงานนี้จะเสร็จสมบูรณ์: สิ่งอำนวยความสะดวกธนาคาร การลงรายการบัญชีโพรไฟล์ ข้อตกลงสินเชื่อธนาคารและรายละเอียดธนาคารของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="f173b-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="f173b-106">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f173b-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="f173b-107">สร้างใบสั่งขายด้วยเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="f173b-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="f173b-108">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f173b-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f173b-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f173b-109">Click New.</span></span>
3. <span data-ttu-id="f173b-110">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f173b-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="f173b-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f173b-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f173b-113">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f173b-113">Expand the General section.</span></span>
7. <span data-ttu-id="f173b-114">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="f173b-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f173b-116">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="f173b-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f173b-118">ในฟิลด์วันที่ลงบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="f173b-119">ในฟิลด์วันที่การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="f173b-120">สังเกตว่า ฟิลด์ 'ชนิดเอกสารธนาคาร' ควรถูกเลือกกับค่า 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="f173b-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="f173b-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f173b-121">Click OK.</span></span>
14. <span data-ttu-id="f173b-122">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f173b-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="f173b-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f173b-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f173b-125">ขยายส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="f173b-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="f173b-126">คลิกแท็บการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="f173b-127">ในฟิลด์วันที่การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="f173b-128">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="f173b-129">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f173b-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="f173b-130">กำหนดรายละเอียดเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="f173b-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="f173b-131">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="f173b-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="f173b-132">คลิกเลตเตอร์ออฟเครดิต/การเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="f173b-133">ในฟิลด์วันที่ใบสมัคร ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f173b-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="f173b-134">ตรวจสอบว่า ฟิลด์ 'บัญชีธนาคาร' มีบัญชีธนาคารที่มีใช้งานเริ่มต้นซึ่งเป็นไปตามวันที่ใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="f173b-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="f173b-135">ในฟิลด์หมายเลขเอกสารธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="f173b-136">ในฟิลด์วันที่รับสินค้า ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f173b-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="f173b-137">ขยายส่วนเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f173b-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="f173b-138">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f173b-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="f173b-139">ขยายส่วนรายละเอียดธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f173b-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="f173b-140">ในฟิลด์ธนาคารผู้แจ้งเครดิต ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="f173b-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="f173b-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f173b-142">Click Save.</span></span>
33. <span data-ttu-id="f173b-143">คลิกนำข้อมูลการจัดส่งของใบสั่งซื้อมาใช้</span><span class="sxs-lookup"><span data-stu-id="f173b-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="f173b-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-144">Close the page.</span></span>
35. <span data-ttu-id="f173b-145">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="f173b-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="f173b-146">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="f173b-146">Click Confirm.</span></span>
37. <span data-ttu-id="f173b-147">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="f173b-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="f173b-148">คลิกเลตเตอร์ออฟเครดิต/การเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="f173b-149">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="f173b-149">Click Process.</span></span>
40. <span data-ttu-id="f173b-150">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="f173b-150">Click Confirm.</span></span>
    * <span data-ttu-id="f173b-151">ตรวจสอบว่า ยอดดุลสินเชื่อได้ลดจำนวนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="f173b-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="f173b-152">ในตัวอย่างนี้มียอดซื้อ = 500.00 วงเงินสินเชื่อ = 10000.00 ดังนั้น ดังนั้นยอดดุลสินเชื่อ = 9500.00</span><span class="sxs-lookup"><span data-stu-id="f173b-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="f173b-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-153">Close the page.</span></span>
42. <span data-ttu-id="f173b-154">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f173b-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="f173b-155">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f173b-155">Click Save.</span></span>
44. <span data-ttu-id="f173b-156">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="f173b-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="f173b-157">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="f173b-157">Click Confirm.</span></span>
    * <span data-ttu-id="f173b-158">แก้ไขเลตเตอร์ออฟเครดิต เนื่องจากมีการเปลี่ยนแปลงในราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="f173b-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="f173b-159">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="f173b-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="f173b-160">คลิกเลตเตอร์ออฟเครดิต/การเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="f173b-161">แก้ไขเลตเตอร์ออฟเครดิต เนื่องจากมีการเปลี่ยนแปลงในราคาต่อหน่วยการซื้อ</span><span class="sxs-lookup"><span data-stu-id="f173b-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="f173b-162">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="f173b-162">Click Process.</span></span>
49. <span data-ttu-id="f173b-163">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="f173b-163">Click Amend.</span></span>
50. <span data-ttu-id="f173b-164">คลิกลบ</span><span class="sxs-lookup"><span data-stu-id="f173b-164">Click Remove.</span></span>
51. <span data-ttu-id="f173b-165">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f173b-165">Click Yes.</span></span>
52. <span data-ttu-id="f173b-166">คลิกนำข้อมูลการจัดส่งของใบสั่งซื้อมาใช้</span><span class="sxs-lookup"><span data-stu-id="f173b-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="f173b-167">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="f173b-167">Click Process.</span></span>
54. <span data-ttu-id="f173b-168">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="f173b-168">Click Confirm.</span></span>
    * <span data-ttu-id="f173b-169">ตรวจสอบว่า ยอดดุลสินเชื่อได้ลดจำนวนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="f173b-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="f173b-170">ในตัวอย่างนี้มียอดซื้อที่แก้ไขแล้ว = 600.00 วงเงินสินเชื่อ = 10000.00 ดังนั้น ดังนั้นยอดดุลสินเชื่อ = 9400.00</span><span class="sxs-lookup"><span data-stu-id="f173b-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="f173b-171">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="f173b-172">ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-172">Post Packing slip</span></span>
1. <span data-ttu-id="f173b-173">ในบานหน้าต่างการดำเนินการ ให้คลิก รับ</span><span class="sxs-lookup"><span data-stu-id="f173b-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f173b-174">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="f173b-174">Click Product receipt.</span></span>
3. <span data-ttu-id="f173b-175">ในฟิลด์ PurchParmTable_Num ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="f173b-176">เลือกหมายเลขการจัดส่งที่สร้างขึ้นด้วยการอ้างอิงต่อเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="f173b-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="f173b-177">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f173b-178">ในฟิลด์วันที่ใบรับสินค้า ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="f173b-179">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f173b-179">Click OK.</span></span>
7. <span data-ttu-id="f173b-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-180">Close the page.</span></span>
8. <span data-ttu-id="f173b-181">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="f173b-182">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="f173b-183">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > นำเข้าเลตเตอร์ออฟเครดิตและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="f173b-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="f173b-184">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f173b-185">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f173b-186">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-186">Verify the Import letter of credit status.</span></span>  
4. <span data-ttu-id="f173b-187">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-187">Close the page.</span></span>
5. <span data-ttu-id="f173b-188">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="f173b-189">ลงรายการบัญชีใบแจ้งหนี้การซื้อ</span><span class="sxs-lookup"><span data-stu-id="f173b-189">Post purchase invoice</span></span>
1. <span data-ttu-id="f173b-190">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f173b-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="f173b-191">เลือกใบสั่งซื้อที่สร้างขึ้นด้วยเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="f173b-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="f173b-192">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f173b-193">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f173b-194">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f173b-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="f173b-195">คลิกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f173b-195">Click Invoice.</span></span>
6. <span data-ttu-id="f173b-196">ในฟิลด์หมายเลข ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f173b-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="f173b-197">ในฟิลด์หมายเลขการจัดส่ง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f173b-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="f173b-198">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f173b-199">ในฟิลด์ วันที่ในใบแจ้งหนี้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="f173b-200">คลิก อัพเดตสถานะการจับคู่</span><span class="sxs-lookup"><span data-stu-id="f173b-200">Click Update match status.</span></span>
11. <span data-ttu-id="f173b-201">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f173b-201">Click Post.</span></span>
12. <span data-ttu-id="f173b-202">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-202">Close the page.</span></span>
13. <span data-ttu-id="f173b-203">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="f173b-204">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="f173b-205">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > นำเข้าเลตเตอร์ออฟเครดิตและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="f173b-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="f173b-206">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f173b-207">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f173b-208">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า 2</span><span class="sxs-lookup"><span data-stu-id="f173b-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="f173b-209">ตรวจสอบ :  สถานะการจัดส่ง = รายละเอียดสินเชื่อธนาคารที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f173b-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="f173b-210">คลิกที่มุมมอง</span><span class="sxs-lookup"><span data-stu-id="f173b-210">Click View.</span></span>
5. <span data-ttu-id="f173b-211">คลิกพิมพ์ใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="f173b-211">Click Print application.</span></span>
6. <span data-ttu-id="f173b-212">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f173b-212">Click OK.</span></span>
    * <span data-ttu-id="f173b-213">ตรวจสอบว่าได้มีการพิมพ์ใบสมัครเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="f173b-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="f173b-214">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-214">Close the page.</span></span>
8. <span data-ttu-id="f173b-215">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-215">Close the page.</span></span>
9. <span data-ttu-id="f173b-216">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="f173b-217">ลงรายการบัญชีสมุดรายวันการชำระเงินของผู้จัดจำหน่าย สำหรับใบแจ้งหนี้การซื้อที่สร้างขึ้นด้วยเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="f173b-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="f173b-218">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f173b-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f173b-219">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f173b-219">Click New.</span></span>
3. <span data-ttu-id="f173b-220">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="f173b-221">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f173b-222">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="f173b-222">Click Lines.</span></span>
6. <span data-ttu-id="f173b-223">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f173b-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="f173b-224">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="f173b-225">คลิกธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f173b-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="f173b-226">ขยายส่วนยอดรวม</span><span class="sxs-lookup"><span data-stu-id="f173b-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="f173b-227">ในฟิลด์แสดง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="f173b-228">ตรวจสอบว่า ฟิลด์หมายเลขเอกสารของธนาคารและหมายเลขการจัดส่งได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="f173b-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="f173b-229">เลือกการทำเครื่องหมายกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="f173b-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="f173b-230">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f173b-230">Click OK.</span></span>
13. <span data-ttu-id="f173b-231">คลิกแท็บการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f173b-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="f173b-232">ตรวจสอบว่า ฟิลด์หมายเลขเอกสารของธนาคารและหมายเลขการจัดส่งได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="f173b-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="f173b-233">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f173b-233">Click Post.</span></span>
15. <span data-ttu-id="f173b-234">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-234">Close the page.</span></span>
16. <span data-ttu-id="f173b-235">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="f173b-236">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้าหลังจากการชำระเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f173b-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="f173b-237">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > นำเข้าเลตเตอร์ออฟเครดิตและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="f173b-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="f173b-238">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f173b-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f173b-239">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f173b-240">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f173b-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="f173b-241">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="f173b-242">ตรวจสอบวงเงินสินเชื่อธนาคารและรายงานการใช้ประโยชน์</span><span class="sxs-lookup"><span data-stu-id="f173b-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="f173b-243">ไปที่การจัดการเงินสดและธนาคาร > การสอบถามและรายงาน > เลตเตอร์ออฟเครดิตหรือหนังสือค้ำประกัน > สินเชื่อธนาคารและรายงานการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f173b-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="f173b-244">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="f173b-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="f173b-245">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="f173b-245">Click Filter.</span></span>
    * <span data-ttu-id="f173b-246">กำหนดฟิลด์เกณฑ์กับบัญชีธนาคารที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f173b-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="f173b-247">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f173b-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="f173b-248">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f173b-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f173b-249">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f173b-249">Click OK.</span></span>
7. <span data-ttu-id="f173b-250">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f173b-250">Click OK.</span></span>
    * <span data-ttu-id="f173b-251">ตรวจสอบรายงานซึ่งแสดงรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="f173b-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="f173b-252">ตรวจสอบรายงานที่แสดงธุรกรรมกับหมายเลขเอกสารธนาคาร วงเงินสินเชื่อ ยอดเงินที่ใช้ และยอดดุลสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="f173b-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="f173b-253">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f173b-253">Close the page.</span></span>


