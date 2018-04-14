--- 
title: "ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้ใบแจ้งหนี้ของผู้จัดจำหน่าย"
description: "คู่มืองานนี้จะช่วยคุณสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อ และดูผลลัพธ์ของการจับคู่ใบสั่งซื้อ ใบรับ และใบแจ้งหนี้ (วิธีการจับคู่ 3 ทาง)"
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9fb328c63bef88c47f16cc20d1419d5daffa4457
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="6f908-103">ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้ใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="6f908-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f908-104">คู่มืองานนี้จะช่วยคุณสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อ และดูผลลัพธ์ของการจับคู่ใบสั่งซื้อ ใบรับ และใบแจ้งหนี้ (วิธีการจับคู่ 3 ทาง)</span><span class="sxs-lookup"><span data-stu-id="6f908-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="6f908-105">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6f908-105">Create a purchase order</span></span>
1. <span data-ttu-id="6f908-106">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6f908-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="6f908-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6f908-107">Click New.</span></span>
3. <span data-ttu-id="6f908-108">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6f908-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6f908-109">ค้นหาผู้จัดจำหน่ายเพื่อเลือก </span><span class="sxs-lookup"><span data-stu-id="6f908-109">Find a vendor to select.</span></span> <span data-ttu-id="6f908-110">ตัวอย่างเช่น เลื่อนลงไปที่ US-104</span><span class="sxs-lookup"><span data-stu-id="6f908-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="6f908-111">เลือกผู้จัดจำหน่าย US-104</span><span class="sxs-lookup"><span data-stu-id="6f908-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="6f908-112">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6f908-112">Click OK.</span></span>
7. <span data-ttu-id="6f908-113">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6f908-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6f908-114">เลือกสินค้าในสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="6f908-114">Select an inventory item.</span></span> <span data-ttu-id="6f908-115">ตัวอย่างเช่น เลือกสินค้าหมายเลข 1000</span><span class="sxs-lookup"><span data-stu-id="6f908-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="6f908-116">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="6f908-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="6f908-117">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="6f908-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="6f908-118">คุณสามารถแทนที่นโยบายการจับคู่ให้เป็นไม่มีการจับคู่ มีการจับคู่ 2 ทาง หรือมีการจับคู่ 3 ทาง</span><span class="sxs-lookup"><span data-stu-id="6f908-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="6f908-119">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="6f908-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="6f908-120">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="6f908-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="6f908-121">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6f908-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="6f908-122">รับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6f908-122">Receive the products</span></span>
1. <span data-ttu-id="6f908-123">ในบานหน้าต่างการดำเนินการ ให้คลิก รับ</span><span class="sxs-lookup"><span data-stu-id="6f908-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="6f908-124">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6f908-124">Click Product receipt.</span></span>
3. <span data-ttu-id="6f908-125">ในฟิลด์ใบรับสินค้า ให้ป้อนหมายเลขใบรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="6f908-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="6f908-126">ตัวอย่างเช่น ป้อน PR123</span><span class="sxs-lookup"><span data-stu-id="6f908-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="6f908-127">คลิก ตกลง เพื่อลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6f908-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="6f908-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6f908-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="6f908-129">สร้างใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="6f908-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="6f908-130">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อที่ได้รับแต่ไม่ได้ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6f908-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="6f908-131">เลือกใบสั่งซื้อที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="6f908-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="6f908-132">ในบานหน้าต่างการดำเนินการ คลิกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6f908-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="6f908-133">คลิกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6f908-133">Click Invoice.</span></span>
5. <span data-ttu-id="6f908-134">ในฟิลด์ หมายเลข ให้ป้อนหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6f908-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="6f908-135">ในฟิลด์ คำอธิบายใบแจ้งหนี้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6f908-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="6f908-136">ในฟิลด์ วันที่ในใบแจ้งหนี้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6f908-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="6f908-137">ในฟิลด์ราคาต่อหน่วย ให้ป้อนหมายเลข 1200</span><span class="sxs-lookup"><span data-stu-id="6f908-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="6f908-138">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="6f908-138">Click Add line.</span></span>
10. <span data-ttu-id="6f908-139">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6f908-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6f908-140">ในรายการ ให้ค้นหาหมายเลขสินค้าที่มีค่าธรรมเนียมการติดตั้ง </span><span class="sxs-lookup"><span data-stu-id="6f908-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="6f908-141">ตัวอย่างเช่น S0001</span><span class="sxs-lookup"><span data-stu-id="6f908-141">For example, S0001</span></span>
12. <span data-ttu-id="6f908-142">เลือกหมายเลขสินค้าที่มีค่าธรรมเนียมการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="6f908-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="6f908-143">โปรดทราบว่า การจับคู่จะไม่เกิดขึ้นหลังจากที่คุณทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6f908-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="6f908-144">คลิก อัพเดตสถานะการจับคู่</span><span class="sxs-lookup"><span data-stu-id="6f908-144">Click Update match status.</span></span>
14. <span data-ttu-id="6f908-145">ในบานหน้าต่างการดำเนินการ ให้คลิก ทบทวน</span><span class="sxs-lookup"><span data-stu-id="6f908-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="6f908-146">คลิก รายละเอียดการจับคู่</span><span class="sxs-lookup"><span data-stu-id="6f908-146">Click Matching details.</span></span>
    * <span data-ttu-id="6f908-147">การบริการรายการใหม่ไม่จำเป็นต้องถูกจับคู่ ดังนั้นสถานะคงอยู่ที่ "ไม่ดำเนินการ"</span><span class="sxs-lookup"><span data-stu-id="6f908-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="6f908-148">เลือกใบรับสินค้าสำหรับสินค้าคงคลังที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="6f908-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="6f908-149">รายการที่มีใบรับสินค้าได้รับการจับคู่ แต่ปริมาณหรือราคาไม่ตรงกัน ดังนั้นการจับคู่จึงไม่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="6f908-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="6f908-150">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6f908-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="6f908-151">หลังจากที่มีการจับคู่ราคาต่อหน่วย สถานะจะถูกอัพเดตเป็นผ่าน</span><span class="sxs-lookup"><span data-stu-id="6f908-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="6f908-152">ถ้านโยบายของคุณอนุญาตมีความขัดแย้งหรือถ้าการจับคู่เป็นเพียงแค่คำเตือน คุณยังคงสามารถลงรายการใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="6f908-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="6f908-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6f908-153">Close the page.</span></span>
19. <span data-ttu-id="6f908-154">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="6f908-154">Click Post.</span></span>
20. <span data-ttu-id="6f908-155">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="6f908-155">Close the form.</span></span>
    * <span data-ttu-id="6f908-156">โปรดทราบว่า จะไม่มีใบสั่งซื้อที่ถูกระบุเป็นได้รับแล้วแต่ไม่ได้ออกใบแจ้งหนี้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="6f908-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


