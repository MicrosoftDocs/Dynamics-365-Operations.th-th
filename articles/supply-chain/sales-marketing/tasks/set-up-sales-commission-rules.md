---
title: ตั้งค่ากฎค่าส่งเสริมการขายให้แก่ผู้ขาย
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าและการเปิดใช้งานการคำนวณค่าคอมมิชชันการขายและการติดตาม '
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ed7ec4ca74e4b6863ab2feff7f20de319789038
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556770"
---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="50eed-103">ตั้งค่ากฎค่าส่งเสริมการขายให้แก่ผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="50eed-103">Set up sales commission rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50eed-104">กระบวนงานนี้แสดงวิธีการตั้งค่าและการเปิดใช้งานการคำนวณค่าคอมมิชชันการขายและการติดตาม </span><span class="sxs-lookup"><span data-stu-id="50eed-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="50eed-105">กระบวนงานแสดงวิธีการสร้างทั้งลูกค้าและกลุ่มค่าคอมมิชชันสินค้า และจากนั้น แสดงวิธีการเชื่อมโยงลูกค้าและผลิตภัณฑ์ไปที่กลุ่มที่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="50eed-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="50eed-106">กลุ่มเหล่านั้นจะใช้ในการตั้งค่าการคำนวณค่าคอมมิชชันเพื่อสร้างลูกค้า สินค้า และชุดข้อมูลของพนักงานขาย ที่ต้องจับคู่โดยใบสั่งขายเพื่อให้สิทธิ์ผู้ขายกับค่าคอมมิชชัน </span><span class="sxs-lookup"><span data-stu-id="50eed-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="50eed-107">การสร้างกลุ่มค่าคอมมิชชันลูกค้าและสินค้านั้นไม่จำเป็น เนื่องจากสามารถคำนวณค่าคอมมิชชันสำหรับแต่ละลูกค้าและ/หรือสินค้าได้ </span><span class="sxs-lookup"><span data-stu-id="50eed-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="50eed-108">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="50eed-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="50eed-109">ตั้งค่ากลุ่มค่าคอมมิชชันและอัตราค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="50eed-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="50eed-110">ไปที่การขายและการตลาด > ค่าคอมมิชชัน > กลุ่มลูกค้าสำหรับค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="50eed-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="50eed-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="50eed-111">Click New.</span></span>
3. <span data-ttu-id="50eed-112">ในฟิลด์กลุ่ม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="50eed-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="50eed-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="50eed-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="50eed-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="50eed-114">Click Save.</span></span>
6. <span data-ttu-id="50eed-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-115">Close the page.</span></span>
7. <span data-ttu-id="50eed-116">ไปที่การขายและการตลาด > ค่าคอมมิชชัน > กลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="50eed-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="50eed-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="50eed-117">Click New.</span></span>
9. <span data-ttu-id="50eed-118">ในฟิลด์กลุ่ม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="50eed-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="50eed-119">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="50eed-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="50eed-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-120">Close the page.</span></span>
12. <span data-ttu-id="50eed-121">ไปที่การขายและการตลาด > ค่าคอมมิชชัน > กลุ่มการขาย</span><span class="sxs-lookup"><span data-stu-id="50eed-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="50eed-122">กลุ่มการขายที่มีค่าคอมมิชชันระบุพนักงานในบทบาทพนักงานขายที่มีสิทธิ์จะได้รับค่าคอมมิชชัน เมื่อลูกค้าที่เชื่อมโยงกับกลุ่มการขายที่เกี่ยวข้องซื้อสินค้าบางรายการ</span><span class="sxs-lookup"><span data-stu-id="50eed-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="50eed-123">ในบริษัทข้อมูลสาธิต USMF มีกลุ่มการขายที่เรียกว่า "ตัวแทนจำหน่ายของสหรัฐอเมริกา"</span><span class="sxs-lookup"><span data-stu-id="50eed-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="50eed-124">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="50eed-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="50eed-125">คลิกพนักงานขาย</span><span class="sxs-lookup"><span data-stu-id="50eed-125">Click Sales rep..</span></span>
    * <span data-ttu-id="50eed-126">หน้าพนักงานขายแสดงรายการของผู้ขายของบริษัทที่สัมพันธ์กับกลุ่มค่าคอมมิชชันที่เฉพาะเจาะจง </span><span class="sxs-lookup"><span data-stu-id="50eed-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="50eed-127">คุณสามารถกำหนดพนักงานขายหลายคนให้กับกลุ่มเดียวกัน และกำหนดสัดส่วนของค่าคอมมิชชันที่สอดคล้องกันให้เป็นค่าเปอร์เซ็นต์ </span><span class="sxs-lookup"><span data-stu-id="50eed-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="50eed-128">ส่วนแบ่งค่าคอมมิชชันรวมระหว่างพนักงานทั้งหมดต้องไม่เกิน 100</span><span class="sxs-lookup"><span data-stu-id="50eed-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="50eed-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="50eed-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="50eed-130">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="50eed-130">Click Edit.</span></span>
17. <span data-ttu-id="50eed-131">ตั้งค่าส่วนแบ่งค่าคอมมิชชันเป็น '50'</span><span class="sxs-lookup"><span data-stu-id="50eed-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="50eed-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="50eed-132">Click New.</span></span>
19. <span data-ttu-id="50eed-133">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="50eed-134">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="50eed-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="50eed-135">เช่น กรองข้อมูลในฟิลด์ชื่อด้วยค่า 'Susan Burk'</span><span class="sxs-lookup"><span data-stu-id="50eed-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="50eed-136">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="50eed-136">Click Select.</span></span>
22. <span data-ttu-id="50eed-137">ตั้งค่าส่วนแบ่งค่าคอมมิชชันเป็น '50'</span><span class="sxs-lookup"><span data-stu-id="50eed-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="50eed-138">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="50eed-138">Click Save.</span></span>
24. <span data-ttu-id="50eed-139">ไปที่การขายและการตลาด > ค่าคอมมิชชัน > การคำนวณค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="50eed-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="50eed-140">ในหน้าการคำนวณค่าคอมมิชชัน คุณกำหนดอัตราค่าคอมมิชชันที่พนักงานจะได้รับสำหรับธุรกรรมการขาย เมื่อประกอบด้วยชุดข้อมูลที่มีการตั้งค่าไว้ล่วงหน้าของลูกค้าและผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="50eed-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="50eed-141">จากส่วนหนึ่งของการตั้งค่าอัตราค่าคอมมิชชัน คุณต้องระบุฐานการคำนวณค่าคอมมิชชันและควรรวม หรือไม่รวมส่วนลด </span><span class="sxs-lookup"><span data-stu-id="50eed-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="50eed-142">คุณยังสามารถป้อนรอบระยะเวลามีผลบังคับใช้สำหรับเมื่ออัตราค่าคอมมิชชันกำลังใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="50eed-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="50eed-143">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="50eed-143">Click New.</span></span>
26. <span data-ttu-id="50eed-144">ในฟิลด์รหัสสินค้า ให้เลือก 'กลุ่ม'</span><span class="sxs-lookup"><span data-stu-id="50eed-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="50eed-145">ในฟิลด์ความสัมพันธ์ของสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="50eed-146">ในรายการ ค้นหาและเลือกกลุ่มที่คุณสร้างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="50eed-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="50eed-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="50eed-148">ในฟิลด์รหัสลูกค้า ให้เลือก 'กลุ่ม'</span><span class="sxs-lookup"><span data-stu-id="50eed-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="50eed-149">ในฟิลด์ความสัมพันธ์ลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="50eed-150">ในรายการ เลือกกลุ่มที่คุณตั้งค่าก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="50eed-151">ในฟิลด์ความสัมพันธ์พนักงานขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="50eed-152">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="50eed-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50eed-153">รักษาตัวเลือก "ก่อนส่วนลดต่อรายการ"</span><span class="sxs-lookup"><span data-stu-id="50eed-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="50eed-154">เก็บตัวเลือก "รายได้" ไว้เป็นข้อมูลพื้นฐานสำหรับการคำนวณมูลค่าของค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="50eed-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="50eed-155">ในฟิลด์เปอร์เซ็นต์ค่าคอมมิชชัน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="50eed-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="50eed-156">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="50eed-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="50eed-157">ตั้งค่าการลงรายการบัญชีค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="50eed-157">Setting up commission posting</span></span>
1. <span data-ttu-id="50eed-158">ไปที่การขายและการตลาด > ค่าคอมมิชชัน > การลงรายการบัญชีค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="50eed-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="50eed-159">ค่าธรรมเนียมค่าคอมมิชชันจะชำระให้แก่พนักงาน และดังนั้นจึงต้องถูกตั้งค่าเพื่อให้แน่ใจว่ามีการลงบัญชีทางการเงินในบัญชีที่เหมาะสมของบัญชีแยกประเภททั่วไป </span><span class="sxs-lookup"><span data-stu-id="50eed-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="50eed-160">ซึ่งทำได้ในหน้าการลงรายการบัญชีค่าคอมมิชชัน </span><span class="sxs-lookup"><span data-stu-id="50eed-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="50eed-161">ตรวจทานการตั้งค่าที่พร้อมใช้งานสำหรับบริษัทปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="50eed-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="50eed-162">โดยทั่วไป ยอดเงินของค่าคอมมิชชันจะถูกลงรายการบัญชีในบัญชีค่าใช้จ่ายเฉพาะ และถูกออฟเซ็ตในบัญชีเจ้าหนี้ที่จัดสรรไว้ </span><span class="sxs-lookup"><span data-stu-id="50eed-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="50eed-163">ถ้าคุณไม่มีการตั้งค่ากฎการลงรายการบัญชีค่าคอมมิชชัน ระบบจะไม่สามารถทำการออกใบแจ้งหนี้ของใบสั่งขายที่มีค่าคอมมิชชันที่มีสิทธิ์ได้</span><span class="sxs-lookup"><span data-stu-id="50eed-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="50eed-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="50eed-165">กำหนดกลุ่มค่าคอมมิชชันให้ลูกค้าและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="50eed-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="50eed-166">ไปที่การขายและการตลาด > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="50eed-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="50eed-167">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="50eed-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="50eed-168">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="50eed-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="50eed-169">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="50eed-169">Click Edit.</span></span>
5. <span data-ttu-id="50eed-170">ขยายส่วนค่าเริ่มต้นของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="50eed-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="50eed-171">ในฟิลด์กลุ่มค่าคอมมิชชัน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="50eed-172">ในรายการ ให้เลือกกลุ่มที่คุณสร้างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="50eed-173">ในฟิลด์กลุ่มการขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="50eed-174">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="50eed-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="50eed-175">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="50eed-175">Click Save.</span></span>
11. <span data-ttu-id="50eed-176">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="50eed-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="50eed-177">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="50eed-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="50eed-178">ตัวอย่างเช่น กรองฟิลด์หมายเลขสินค้าด้วยค่า 'T0020'</span><span class="sxs-lookup"><span data-stu-id="50eed-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="50eed-179">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="50eed-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="50eed-180">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="50eed-180">Click Edit.</span></span>
15. <span data-ttu-id="50eed-181">ขยายส่วนการขาย</span><span class="sxs-lookup"><span data-stu-id="50eed-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="50eed-182">ในฟิลด์กลุ่มค่าคอมมิชชัน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="50eed-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="50eed-183">ในรายการ ให้เลือกกลุ่มค่าคอมมชชันที่คุณสร้างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="50eed-183">In the list, select the commission group that you created earlier.</span></span>

