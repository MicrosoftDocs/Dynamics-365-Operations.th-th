--- 
title: "จัดทำเงื่อนไขการชำระเงินของลูกค้า"
description: "กระบวนงานนี้กำหนดส่วนลดเงินสดและการตั้งค่าวันที่ครบกำหนด "
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 49f4047ab4bff6bdfbe8326a6680f9d8f9762c95
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="51648-103">จัดทำเงื่อนไขการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="51648-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51648-104">กระบวนงานนี้กำหนดส่วนลดเงินสดและการตั้งค่าวันที่ครบกำหนด </span><span class="sxs-lookup"><span data-stu-id="51648-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="51648-105">คู่มือของงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="51648-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="51648-106">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > วันชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51648-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="51648-107">การตั้งค่าของเงื่อนไขการชำระเงินที่ใช้ร่วมกันสำหรับบัญชีลูกหนี้และบัญชีเจ้าหนี้ </span><span class="sxs-lookup"><span data-stu-id="51648-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="51648-108">ถ้าคุณได้กำหนดไว้ในโมดูล จะพร้อมใช้งานในโมดูลอื่นๆด้วย </span><span class="sxs-lookup"><span data-stu-id="51648-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="51648-109">สำหรับคู่มืองานนี้ ได้มีการตั้งค่าเงื่อนไขการชำระเงินทั้งหมดภายใต้บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="51648-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="51648-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="51648-110">Click New.</span></span>
    * <span data-ttu-id="51648-111">สร้างวันชำระเงินถ้าเงื่อนไขการชำระเงินที่คุณต้องการให้ระบุวันของสัปดาห์ (วันจันทร์ อังคาร เป็นต้น) หรือระบุวันที่ของเดือน (วันที่ 5 วันที่ 10 เป็นต้น)</span><span class="sxs-lookup"><span data-stu-id="51648-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="51648-112">ในฟิลด์วันชำระเงิน ให้ป้อนรหัสสำหรับวันชำระเงินในฟิลด์วันชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51648-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="51648-113">ในฟิลด์คำอธิบายงาน ให้ป้อนคำอธิบายของวันชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51648-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="51648-114">ในฟิลด์สัปดาห์/เดือน ให้เลือกสัปดาห์หรือเดือน</span><span class="sxs-lookup"><span data-stu-id="51648-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="51648-115">ถ้าคุณต้องการป้อนวันของสัปดาห์เช่น วันจันทร์ ให้เลือกสัปดาห์ </span><span class="sxs-lookup"><span data-stu-id="51648-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="51648-116">ถ้าคุณต้องการป้อนวันที่ในเดือนเช่น วันที่ 10 ให้เลือกเดือน </span><span class="sxs-lookup"><span data-stu-id="51648-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="51648-117">มีการเลือกเดือนสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="51648-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="51648-118">ในฟิลด์วันของเดือน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="51648-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="51648-119">ควรป้อนวันที่เป็นตัวเลขเช่น '10' และไม่ใช่ 'วันที่ 10'</span><span class="sxs-lookup"><span data-stu-id="51648-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="51648-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51648-120">Click Save.</span></span>
8. <span data-ttu-id="51648-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51648-121">Close the page.</span></span>
9. <span data-ttu-id="51648-122">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51648-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="51648-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="51648-123">Click New.</span></span>
    * <span data-ttu-id="51648-124">เงื่อนไขการชำระเงินจะใช้เพื่อกำหนดการคำนวณวันครบกำหนด </span><span class="sxs-lookup"><span data-stu-id="51648-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="51648-125">การตั้งค่าวันที่ส่วนลดเงินสดมีกำหนดในหน้าซึ่งแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="51648-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="51648-126">ในฟิลด์เงื่อนไขวิธีการชำระเงิน ให้ป้อน ID ในฟิลด์เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="51648-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="51648-127">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="51648-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="51648-128">เลือกวิธีการชำระเงินเช่น COD สุทธิ เดือนปัจจุบัน เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="51648-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="51648-129">วิธีการชำระเงินจะใช้เพื่อกำหนดจุดเริ่มต้นของวิธีการคำนวณวันครบกำหนดชำระ </span><span class="sxs-lookup"><span data-stu-id="51648-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="51648-130">ตัวอย่างเช่น ค่าสุทธิจะถูกใช้ ถ้าวันครบกำหนดเป็นจำนวนของเดือนหรือวันหลังจากวันที่ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="51648-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="51648-131">สามารถใช้ COD เมื่อต้องมีการชำระเงินซึ่งขึ้นกับใบแจ้งหนี้ ดังนั้นจึงไม่สามารถคำนวณวันครบกำหนดได้ </span><span class="sxs-lookup"><span data-stu-id="51648-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="51648-132">เลือกเดือนปัจจุบันสำหรับคู่มือของงานนี้</span><span class="sxs-lookup"><span data-stu-id="51648-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="51648-133">เลือกวันชำระเงินถ้าวันเฉพาะของสัปดาห์หรือวันที่ถูกรวมอยู่ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="51648-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="51648-134">คุณอาจป้อนปริมาณในหน่วยเดือนหรือวัน ขึ้นอยู่กับเงื่อนไขของการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="51648-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="51648-135">หรือคุณสามารถใช้กำหนดการชำระเงินหรือวันที่ชำระเงินเป็น 'เพิ่ม' ที่ส่วนสุดท้ายของวิธีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="51648-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="51648-136">ถ้าวันครบกำหนดจะเป็นทุกวันที่ 10 ของเดือน ให้เลือกวันชำระเงินเป็นของวันที่ 10</span><span class="sxs-lookup"><span data-stu-id="51648-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="51648-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51648-137">Click Save.</span></span>
16. <span data-ttu-id="51648-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="51648-138">Close the page.</span></span>
17. <span data-ttu-id="51648-139">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="51648-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="51648-140">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="51648-140">Click New.</span></span>
    * <span data-ttu-id="51648-141">หน้านี้จะใช้เพื่อกำหนดวิธีการคำนวณวันที่ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="51648-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="51648-142">ในฟิลด์ส่วนลดเงินสด ให้ป้อน ID ในฟิลด์ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="51648-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="51648-143">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="51648-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="51648-144">ถ้าส่วนลดเงินสดที่จัดระดับจะพร้อมใช้งาน ให้เลือกรหัสส่วนลดถัดไปที่เกี่ยวข้องหลังจากการหักส่วนลดเงินสดนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="51648-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="51648-145">ป้อนจำนวนวันที่ใช้ในการคำนวณวันที่ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="51648-145">Enter the number of days used to calculate the cash dicount date.</span></span>
    * <span data-ttu-id="51648-146">ถ้ามีเลือกหลักการสุทธิ จะมีการเพิ่มจำนวนวันจนที่วันที่ใบแจ้งหนี้เพื่อคำนวณวันที่ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="51648-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="51648-147">ป้อนเปอร์เซ็นต์ของส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="51648-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="51648-148">ป้อนบัญชีหลักที่ส่วนลดเงินสดที่จะลงรายการบัญชีสำหรับใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="51648-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="51648-149">ในฟิลด์บัญชีส่วนลดตรงข้าม ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="51648-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="51648-150">ถ้าคุณเลือก 'บัญชีผู้ใช้บนรายการใบแจ้งหนี้' ส่วนลดเงินสดจะลงรายการบัญชีเดียวกับบัญชีหลักสินทรัพย์/ค่าใช้จ่ายในรายการของใบแจ้งหนี้ของผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="51648-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="51648-151">ถ้าคุณเลือก 'ใช้บัญชีหลักสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย' ส่วนลดเงินสดจะลงรายการบัญชีไปยังบัญชีหลักที่คุณกำหนดใน 'บัญชีหลักสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย' </span><span class="sxs-lookup"><span data-stu-id="51648-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="51648-152">สำหรับตัวอย่างนี้ เลือก 'ใช้บัญชีหลักสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="51648-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="51648-153">ป้อนบัญชีหลักที่ส่วนลดเงินสดที่จะลงรายการบัญชีสำหรับใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="51648-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="51648-154">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="51648-154">Click Save.</span></span>


