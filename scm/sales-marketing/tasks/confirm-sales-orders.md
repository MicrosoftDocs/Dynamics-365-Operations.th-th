--- 
title: "ยืนยันใบสั่งขาย"
description: "ขั้นตอนนี้อธิบายวิธีการยืนยันใบสั่งขาย "
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="6376e-103">ยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6376e-103">Confirm sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6376e-104">ขั้นตอนนี้อธิบายวิธีการยืนยันใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="6376e-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="6376e-105">คุณจะได้เห็นวิธีการยืนยันใบสั่งทีละใบ และวิธีการยืนยันใบสั่งหลายใบพร้อมกันในครั้งเดียว </span><span class="sxs-lookup"><span data-stu-id="6376e-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="6376e-106">งานเหล่านี้อาจจะสามารถกระทำโดยผู้ประมวลผลใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="6376e-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="6376e-107">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตบริษัท USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="6376e-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6376e-108">ก่อนที่คุณเริ่ม ตรวจสอบว่ามีใบสั่งขายหลายใบสำหรับลูกค้ารายเดียวกันเปิดอยู่ </span><span class="sxs-lookup"><span data-stu-id="6376e-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="6376e-109">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ลูกค้า US-027</span><span class="sxs-lookup"><span data-stu-id="6376e-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="6376e-110">ยืนยันใบสั่งขายใบเดียว</span><span class="sxs-lookup"><span data-stu-id="6376e-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="6376e-111">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6376e-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6376e-112">ในรายการ ค้นหาและเลือกใบสั่งที่คุณต้องการจะยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6376e-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="6376e-113">คลิกลิงค์หมายเลขใบสั่งขายเพื่อเปิดใบสั่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6376e-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="6376e-114">ในบานหน้าต่างการดำเนินการ คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="6376e-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="6376e-115">คลิกยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6376e-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="6376e-116">ขยายหรือยุบส่วนพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6376e-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="6376e-117">ตรวจสอบให้แน่ใจว่าฟิลด์การลงรายการบัญชีใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="6376e-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="6376e-118">ตั้งค่าตัวเลือกการพิมพ์ใบยืนยันการขายเป็นใช่</span><span class="sxs-lookup"><span data-stu-id="6376e-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="6376e-119">การเช็คฟิลด์วงเงินสินเชื่อเป็นการระบุวิธีการที่ใช้ในการคำนวณสินเชื่อคงเหลือของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="6376e-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="6376e-120">โดยค่าเริ่มต้นจะถูกคัดลอกมาจากหน้าพารามิเตอร์บัญชีลูกหนี้ </span><span class="sxs-lookup"><span data-stu-id="6376e-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="6376e-121">ถ้าคุณต้องการข้ามการตรวจสอบวงเงินสินเชื่อเมื่อมีการยืนยันใบสั่งขาย ให้ตั้งค่าวงเงินสินเชื่อโดยเลือกเครื่องหมายเป็นไม่มี </span><span class="sxs-lookup"><span data-stu-id="6376e-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="6376e-122">อย่างไรก็ตาม คุณควรทราบว่าแม้ว่าถ้าฟิลด์นี้ถูกกำหนดเป็นไม่มี การตรวจสอบวงเงินสินเชื่อจะยังคงต้องทำถ้าเลือกตัวเลือกบังคับสำหรับวงเงินสินเชื่อในข้อมูลหลักของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6376e-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="6376e-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6376e-123">Click OK.</span></span>
9. <span data-ttu-id="6376e-124">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="6376e-124">Click Yes.</span></span>
10. <span data-ttu-id="6376e-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6376e-125">Close the page.</span></span>
11. <span data-ttu-id="6376e-126">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6376e-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="6376e-127">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="6376e-127">Click Change view.</span></span>
13. <span data-ttu-id="6376e-128">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="6376e-128">Click Header view.</span></span>
    * <span data-ttu-id="6376e-129">เมื่อมีการยืนยันใบสั่ง สถานะของเอกสารจะตั้งค่าเป็นการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6376e-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="6376e-130">ในบานหน้าต่างการดำเนินการ คลิกขาย</span><span class="sxs-lookup"><span data-stu-id="6376e-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="6376e-131">คลิกการยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6376e-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="6376e-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6376e-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="6376e-133">ยืนยันใบสั่งขายหลายใบพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="6376e-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="6376e-134">ไปที่ การขายและการตลาด > ใบสั่งขาย > การยืนยันใบสั่ง > ยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6376e-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="6376e-135">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="6376e-135">Click Select.</span></span>
3. <span data-ttu-id="6376e-136">บนรายการบนแท็บการกำหนดช่วง หาและเลือกเรกคอร์ดที่อ้างอิงฟิลด์บัญชีลูกค้า </span><span class="sxs-lookup"><span data-stu-id="6376e-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="6376e-137">ในฟิลด์เงื่อนไข ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6376e-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6376e-138">ในรายการ ค้นหาและเลือกบัญชีลูกค้าที่มีใบสั่งหลายใบซึ่งคุณต้องการยืนยันโดยรวม</span><span class="sxs-lookup"><span data-stu-id="6376e-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="6376e-139">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือกบัญชี US-027</span><span class="sxs-lookup"><span data-stu-id="6376e-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="6376e-140">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6376e-140">Click OK.</span></span>
    * <span data-ttu-id="6376e-141">แท็บภาพรวมแสดงรายการของใบสั่งที่ตรงกับเกณฑ์การสอบถาม </span><span class="sxs-lookup"><span data-stu-id="6376e-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="6376e-142">รายการต่อไปนี้จะถูกรวมในรายการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6376e-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="6376e-143">การอัพเดตสรุปสำหรับฟิลด์ที่ระบุพารามิเตอร์โดยใบสั่งหลายใบจะสรุปเข้าในเอกสารใบยืนยันหนึ่งฉบับ </span><span class="sxs-lookup"><span data-stu-id="6376e-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="6376e-144">โดยค่าเริ่มต้นตัวเลือกจะถูกคัดลอกจากค่าเริ่มต้นสำหรับการตั้งค่าอัพเดตสรุปบนหน้าพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="6376e-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="6376e-145">ในฟิลด์อัพเดตสรุป เลือก 'ใบสั่ง'</span><span class="sxs-lookup"><span data-stu-id="6376e-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="6376e-146">พารามิเตอร์ขั้นต่ำที่จำเป็นเพื่อการสร้างอัพเดตสรุปคือ บัญชีใบแจ้งหนี้และสกุลเงิน </span><span class="sxs-lookup"><span data-stu-id="6376e-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="6376e-147">ซึ่งหมายความว่า การอัพเดตสรุปที่มีบัญชีใบแจ้งหนี้ที่แตกต่างกันและสกุลเงินที่แตกต่างกันนั้นไม่ได้รับอนุญาต </span><span class="sxs-lookup"><span data-stu-id="6376e-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="6376e-148">สามารถตั้งค่าพารามิเตอร์เพิ่มเติมได้ในหน้าพาราเดตสรุปซึ่งสามารถเข้าถึงได้จากหน้าพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="6376e-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="6376e-149">ในฟิลด์ใบสั่งขาย คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6376e-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6376e-150">ในรายการ ให้เลือกหมายเลขใบสั่งซื้อที่คุณต้องการใบสั่งสรุป</span><span class="sxs-lookup"><span data-stu-id="6376e-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="6376e-151">คลิกการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="6376e-151">Click Arrange.</span></span>
11. <span data-ttu-id="6376e-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6376e-152">Click OK.</span></span>
12. <span data-ttu-id="6376e-153">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6376e-153">Click OK.</span></span>


