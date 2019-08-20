---
title: ข้อมูลใบแจ้งหนี้ที่สำคัญในระบบบัญชีเจ้าหนี้โดยใช้กลุ่มใบแจ้งหนี้
description: 'คู่มือของงานนี้จะแสดงวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้ '
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843228"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="f344a-103">ข้อมูลใบแจ้งหนี้ที่สำคัญในระบบบัญชีเจ้าหนี้โดยใช้กลุ่มใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f344a-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f344a-104">คู่มือของงานนี้จะแสดงวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="f344a-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="f344a-105">แล้วใช้กลุ่มใบแจ้งหนี้เพื่อจับคู่ใบแจ้งหนี้กับใบสั่งซื้อ และทำให้ค่าใช้จ่ายในหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f344a-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f344a-106">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f344a-106">Create a purchase order</span></span>
1. <span data-ttu-id="f344a-107">ไปที่ บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f344a-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="f344a-108">คลิก สร้าง เพื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f344a-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="f344a-109">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f344a-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="f344a-110">เลือกผู้จัดจำหน่ายจากรายการ </span><span class="sxs-lookup"><span data-stu-id="f344a-110">Select the vendor from the list.</span></span> <span data-ttu-id="f344a-111">ตัวอย่างเช่น ผู้จัดจำหน่าย 1001</span><span class="sxs-lookup"><span data-stu-id="f344a-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="f344a-112">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f344a-112">Click OK.</span></span>
6. <span data-ttu-id="f344a-113">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f344a-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="f344a-114">ค้นหาหมายเลขสินค้าบริการจากรายการ </span><span class="sxs-lookup"><span data-stu-id="f344a-114">Find the services item number in the list.</span></span> <span data-ttu-id="f344a-115">ตัวอย่างเช่น เลือก S0001</span><span class="sxs-lookup"><span data-stu-id="f344a-115">For example, select S0001.</span></span>
8. <span data-ttu-id="f344a-116">คลิกที่หมายเลขสินค้า และเลือก</span><span class="sxs-lookup"><span data-stu-id="f344a-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="f344a-117">ยอดเงินสุทธิคือ 75.00 </span><span class="sxs-lookup"><span data-stu-id="f344a-117">The net amount is 75.00.</span></span>  <span data-ttu-id="f344a-118">ซึ่งเป็นยอดเงินที่คาดหมายในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f344a-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="f344a-119">ในบานหน้าต่างการดำเนินการ คลิกที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="f344a-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="f344a-120">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="f344a-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="f344a-121">สร้างและลงรายการบัญชีและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f344a-121">Create and post and invoice</span></span>
1. <span data-ttu-id="f344a-122">ไปที่บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > ทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f344a-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="f344a-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f344a-123">Click New.</span></span>
3. <span data-ttu-id="f344a-124">เปิดการค้นหาเพื่อเลือกชื่อของทะเบียนใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="f344a-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="f344a-125">เลือกชื่อทะเบียนใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="f344a-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="f344a-126">คลิกที่รายการเพื่อเปิดการลงทะเบียนและป้อนรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f344a-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="f344a-127">ในการค้นหา เลือกผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="f344a-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="f344a-128">ตัวอย่างเช่น คลิกที่ผู้จัดจำหน่าย 1001</span><span class="sxs-lookup"><span data-stu-id="f344a-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="f344a-129">ในฟิลด์ใบแจ้งหนี้ ให้ป้อนหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f344a-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="f344a-130">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f344a-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f344a-131">ในฟิลด์เครดิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="f344a-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="f344a-132">ในฟิลด์ใบสั่งซื้อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f344a-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="f344a-133">เลือกใบสั่งซื้อที่คุณสร้างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="f344a-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="f344a-134">ในฟิลด์อนุมัติโดย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f344a-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="f344a-135">ให้เน้นที่ผู้อนุมัติและคลิกที่เลือกเพื่อเลือกผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f344a-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="f344a-136">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f344a-136">Click Post.</span></span>
15. <span data-ttu-id="f344a-137">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="f344a-137">Close the form.</span></span>
16. <span data-ttu-id="f344a-138">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="f344a-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="f344a-139">เปิดใบแจ้งหนี้จากกลุ่มและจับคู่กับใบสั่งซื้อเพื่อทำให้กระบวนการใบแจ้งหนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f344a-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="f344a-140">ไปที่บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > กลุ่มใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f344a-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="f344a-141">คลิกที่ใบสั่งซื้อเพื่อสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบแจ้งหนี้ในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f344a-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="f344a-142">เลือกใบแจ้งหนี้ที่คุณต้องการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="f344a-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="f344a-143">คลิกที่อัพเดตสถานะการจับคู่เพื่อทำการจับคู่ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f344a-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="f344a-144">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f344a-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="f344a-145">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="f344a-145">Click Change view.</span></span>
7. <span data-ttu-id="f344a-146">คลิกมุมมองกริด</span><span class="sxs-lookup"><span data-stu-id="f344a-146">Click Grid view.</span></span>
8. <span data-ttu-id="f344a-147">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f344a-147">Click Post.</span></span>
9. <span data-ttu-id="f344a-148">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="f344a-148">Close the form.</span></span>
10. <span data-ttu-id="f344a-149">ไปที่ บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f344a-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="f344a-150">เลือกผู้จัดจำหน่ายที่อยู่บนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="f344a-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="f344a-151">ตัวอย่างเช่น เลือกผู้จัดจำหน่าย 1001</span><span class="sxs-lookup"><span data-stu-id="f344a-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="f344a-152">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f344a-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f344a-153">ในบานหน้าต่างการดำเนินการ คลิกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="f344a-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="f344a-154">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="f344a-154">Click Transactions.</span></span>
15. <span data-ttu-id="f344a-155">เลือกใบแจ้งหนี้ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f344a-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="f344a-156">ทะเบียนใบแจ้งหนี้คงค้างมีการกลับรายการ และลงรายการบัญชีค่าใช้จ่ายที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f344a-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

