---
title: นำเข้าเลตเตอร์ออฟเครดิต
description: 'กระบวนงานนี้นำไปสู่กระบวนการการนำเข้าเลตเตอร์ออฟเครดิต '
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac0b1aacbf0e5dbe69a8125dc0a1373de0957d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225404"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="975e6-103">นำเข้าเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-103">Import letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="975e6-104">กระบวนงานนี้นำไปสู่กระบวนการการนำเข้าเลตเตอร์ออฟเครดิต </span><span class="sxs-lookup"><span data-stu-id="975e6-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="975e6-105">ต้องตั้งค่าต่อไปนี้ก่อนที่กระบวนงานนี้จะเสร็จสมบูรณ์: สิ่งอำนวยความสะดวกธนาคาร การลงรายการบัญชีโพรไฟล์ ข้อตกลงสินเชื่อธนาคารและรายละเอียดธนาคารของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="975e6-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="975e6-106">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="975e6-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="975e6-107">สร้างใบสั่งขายด้วยเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="975e6-108">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="975e6-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="975e6-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="975e6-109">Click New.</span></span>
3. <span data-ttu-id="975e6-110">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="975e6-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="975e6-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="975e6-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="975e6-113">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="975e6-113">Expand the General section.</span></span>
7. <span data-ttu-id="975e6-114">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="975e6-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="975e6-116">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="975e6-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="975e6-118">ในฟิลด์วันที่ลงบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="975e6-119">ในฟิลด์วันที่การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="975e6-120">สังเกตว่า ฟิลด์ 'ชนิดเอกสารธนาคาร' ควรถูกเลือกกับค่า 'เลตเตอร์ออฟเครดิต'</span><span class="sxs-lookup"><span data-stu-id="975e6-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="975e6-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="975e6-121">Click OK.</span></span>
14. <span data-ttu-id="975e6-122">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="975e6-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="975e6-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="975e6-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="975e6-125">ขยายส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="975e6-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="975e6-126">คลิกแท็บการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="975e6-127">ในฟิลด์วันที่การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="975e6-128">ในฟิลด์วันที่จัดส่งที่ยืนยัน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="975e6-129">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="975e6-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="975e6-130">กำหนดรายละเอียดเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="975e6-131">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="975e6-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="975e6-132">คลิกเลตเตอร์ออฟเครดิต/การเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="975e6-133">ในฟิลด์วันที่ใบสมัคร ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="975e6-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="975e6-134">ตรวจสอบว่า ฟิลด์ 'บัญชีธนาคาร' มีบัญชีธนาคารที่มีใช้งานเริ่มต้นซึ่งเป็นไปตามวันที่ใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="975e6-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="975e6-135">ในฟิลด์หมายเลขเอกสารธนาคาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="975e6-136">ในฟิลด์วันที่รับสินค้า ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="975e6-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="975e6-137">ขยายส่วนเอกสารธนาคาร</span><span class="sxs-lookup"><span data-stu-id="975e6-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="975e6-138">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="975e6-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="975e6-139">ขยายส่วนรายละเอียดธนาคาร</span><span class="sxs-lookup"><span data-stu-id="975e6-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="975e6-140">ในฟิลด์ธนาคารผู้แจ้งเครดิต ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="975e6-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="975e6-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="975e6-142">Click Save.</span></span>
33. <span data-ttu-id="975e6-143">คลิกนำข้อมูลการจัดส่งของใบสั่งซื้อมาใช้</span><span class="sxs-lookup"><span data-stu-id="975e6-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="975e6-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-144">Close the page.</span></span>
35. <span data-ttu-id="975e6-145">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="975e6-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="975e6-146">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="975e6-146">Click Confirm.</span></span>
37. <span data-ttu-id="975e6-147">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="975e6-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="975e6-148">คลิกเลตเตอร์ออฟเครดิต/การเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="975e6-149">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="975e6-149">Click Process.</span></span>
40. <span data-ttu-id="975e6-150">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="975e6-150">Click Confirm.</span></span>
    * <span data-ttu-id="975e6-151">ตรวจสอบว่า ยอดดุลสินเชื่อได้ลดจำนวนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="975e6-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="975e6-152">ในตัวอย่างนี้มียอดซื้อ = 500.00 วงเงินสินเชื่อ = 10000.00 ดังนั้น ดังนั้นยอดดุลสินเชื่อ = 9500.00</span><span class="sxs-lookup"><span data-stu-id="975e6-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="975e6-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-153">Close the page.</span></span>
42. <span data-ttu-id="975e6-154">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="975e6-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="975e6-155">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="975e6-155">Click Save.</span></span>
44. <span data-ttu-id="975e6-156">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="975e6-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="975e6-157">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="975e6-157">Click Confirm.</span></span>
    * <span data-ttu-id="975e6-158">แก้ไขเลตเตอร์ออฟเครดิต เนื่องจากมีการเปลี่ยนแปลงในราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="975e6-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="975e6-159">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="975e6-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="975e6-160">คลิกเลตเตอร์ออฟเครดิต/การเรียกเก็บเงินสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="975e6-161">แก้ไขเลตเตอร์ออฟเครดิต เนื่องจากมีการเปลี่ยนแปลงในราคาต่อหน่วยการซื้อ</span><span class="sxs-lookup"><span data-stu-id="975e6-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="975e6-162">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="975e6-162">Click Process.</span></span>
49. <span data-ttu-id="975e6-163">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="975e6-163">Click Amend.</span></span>
50. <span data-ttu-id="975e6-164">คลิกลบ</span><span class="sxs-lookup"><span data-stu-id="975e6-164">Click Remove.</span></span>
51. <span data-ttu-id="975e6-165">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="975e6-165">Click Yes.</span></span>
52. <span data-ttu-id="975e6-166">คลิกนำข้อมูลการจัดส่งของใบสั่งซื้อมาใช้</span><span class="sxs-lookup"><span data-stu-id="975e6-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="975e6-167">คลิกกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="975e6-167">Click Process.</span></span>
54. <span data-ttu-id="975e6-168">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="975e6-168">Click Confirm.</span></span>
    * <span data-ttu-id="975e6-169">ตรวจสอบว่า ยอดดุลสินเชื่อได้ลดจำนวนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="975e6-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="975e6-170">ในตัวอย่างนี้มียอดซื้อที่แก้ไขแล้ว = 600.00 วงเงินสินเชื่อ = 10000.00 ดังนั้น ดังนั้นยอดดุลสินเชื่อ = 9400.00</span><span class="sxs-lookup"><span data-stu-id="975e6-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="975e6-171">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="975e6-172">ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-172">Post Packing slip</span></span>
1. <span data-ttu-id="975e6-173">ในบานหน้าต่างการดำเนินการ ให้คลิก รับ</span><span class="sxs-lookup"><span data-stu-id="975e6-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="975e6-174">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="975e6-174">Click Product receipt.</span></span>
3. <span data-ttu-id="975e6-175">ในฟิลด์ PurchParmTable_Num ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="975e6-176">เลือกหมายเลขการจัดส่งที่สร้างขึ้นด้วยการอ้างอิงต่อเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="975e6-177">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="975e6-178">ในฟิลด์วันที่ใบรับสินค้า ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="975e6-179">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="975e6-179">Click OK.</span></span>
7. <span data-ttu-id="975e6-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-180">Close the page.</span></span>
8. <span data-ttu-id="975e6-181">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="975e6-182">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="975e6-183">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > นำเข้าเลตเตอร์ออฟเครดิตและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="975e6-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="975e6-184">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="975e6-185">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="975e6-186">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="975e6-187">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-187">Close the page.</span></span>
5. <span data-ttu-id="975e6-188">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="975e6-189">ลงรายการบัญชีใบแจ้งหนี้การซื้อ</span><span class="sxs-lookup"><span data-stu-id="975e6-189">Post purchase invoice</span></span>
1. <span data-ttu-id="975e6-190">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="975e6-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="975e6-191">เลือกใบสั่งซื้อที่สร้างขึ้นด้วยเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="975e6-192">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="975e6-193">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="975e6-194">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="975e6-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="975e6-195">คลิกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="975e6-195">Click Invoice.</span></span>
6. <span data-ttu-id="975e6-196">ในฟิลด์หมายเลข ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="975e6-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="975e6-197">ในฟิลด์หมายเลขการจัดส่ง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="975e6-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="975e6-198">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="975e6-199">ในฟิลด์ วันที่ในใบแจ้งหนี้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="975e6-200">คลิก อัพเดตสถานะการจับคู่</span><span class="sxs-lookup"><span data-stu-id="975e6-200">Click Update match status.</span></span>
11. <span data-ttu-id="975e6-201">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="975e6-201">Click Post.</span></span>
12. <span data-ttu-id="975e6-202">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-202">Close the page.</span></span>
13. <span data-ttu-id="975e6-203">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="975e6-204">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="975e6-205">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > นำเข้าเลตเตอร์ออฟเครดิตและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="975e6-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="975e6-206">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="975e6-207">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="975e6-208">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า 2</span><span class="sxs-lookup"><span data-stu-id="975e6-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="975e6-209">ตรวจสอบ :  สถานะการจัดส่ง = รายละเอียดสินเชื่อธนาคารที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="975e6-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="975e6-210">คลิกที่มุมมอง</span><span class="sxs-lookup"><span data-stu-id="975e6-210">Click View.</span></span>
5. <span data-ttu-id="975e6-211">คลิกพิมพ์ใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="975e6-211">Click Print application.</span></span>
6. <span data-ttu-id="975e6-212">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="975e6-212">Click OK.</span></span>
    * <span data-ttu-id="975e6-213">ตรวจสอบว่าได้มีการพิมพ์ใบสมัครเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="975e6-214">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-214">Close the page.</span></span>
8. <span data-ttu-id="975e6-215">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-215">Close the page.</span></span>
9. <span data-ttu-id="975e6-216">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="975e6-217">ลงรายการบัญชีสมุดรายวันการชำระเงินของผู้จัดจำหน่าย สำหรับใบแจ้งหนี้การซื้อที่สร้างขึ้นด้วยเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="975e6-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="975e6-218">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="975e6-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="975e6-219">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="975e6-219">Click New.</span></span>
3. <span data-ttu-id="975e6-220">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="975e6-221">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="975e6-222">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="975e6-222">Click Lines.</span></span>
6. <span data-ttu-id="975e6-223">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="975e6-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="975e6-224">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="975e6-225">คลิกธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="975e6-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="975e6-226">ขยายส่วนยอดรวม</span><span class="sxs-lookup"><span data-stu-id="975e6-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="975e6-227">ในฟิลด์แสดง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="975e6-228">ตรวจสอบว่า ฟิลด์หมายเลขเอกสารของธนาคารและหมายเลขการจัดส่งได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="975e6-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="975e6-229">เลือกการทำเครื่องหมายกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="975e6-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="975e6-230">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="975e6-230">Click OK.</span></span>
13. <span data-ttu-id="975e6-231">คลิกแท็บการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="975e6-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="975e6-232">ตรวจสอบว่า ฟิลด์หมายเลขเอกสารของธนาคารและหมายเลขการจัดส่งได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="975e6-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="975e6-233">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="975e6-233">Click Post.</span></span>
15. <span data-ttu-id="975e6-234">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-234">Close the page.</span></span>
16. <span data-ttu-id="975e6-235">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="975e6-236">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้าหลังจากการชำระเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="975e6-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="975e6-237">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > นำเข้าเลตเตอร์ออฟเครดิตและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="975e6-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="975e6-238">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="975e6-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="975e6-239">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="975e6-240">ตรวจสอบสถานะเลตเตอร์ออฟเครดิตการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="975e6-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="975e6-241">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="975e6-242">ตรวจสอบวงเงินสินเชื่อธนาคารและรายงานการใช้ประโยชน์</span><span class="sxs-lookup"><span data-stu-id="975e6-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="975e6-243">ไปที่การจัดการเงินสดและธนาคาร > การสอบถามและรายงาน > เลตเตอร์ออฟเครดิตหรือหนังสือค้ำประกัน > สินเชื่อธนาคารและรายงานการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="975e6-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="975e6-244">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="975e6-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="975e6-245">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="975e6-245">Click Filter.</span></span>
    * <span data-ttu-id="975e6-246">กำหนดฟิลด์เกณฑ์กับบัญชีธนาคารที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="975e6-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="975e6-247">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="975e6-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="975e6-248">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="975e6-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="975e6-249">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="975e6-249">Click OK.</span></span>
7. <span data-ttu-id="975e6-250">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="975e6-250">Click OK.</span></span>
    * <span data-ttu-id="975e6-251">ตรวจสอบรายงานซึ่งแสดงรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="975e6-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="975e6-252">ตรวจสอบรายงานที่แสดงธุรกรรมกับหมายเลขเอกสารธนาคาร วงเงินสินเชื่อ ยอดเงินที่ใช้ และยอดดุลสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="975e6-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="975e6-253">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="975e6-253">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]