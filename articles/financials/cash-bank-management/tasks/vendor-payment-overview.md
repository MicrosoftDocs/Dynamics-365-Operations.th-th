--- 
title: "ภาพรวมการชำระเงินของผู้จัดจำหน่าย"
description: "คำแนะนำของงานนี้จะนำคุณผ่านวิธีการต่างๆที่ใช้ในการสร้างการชำระเงินของผู้จัดจำหน่าย รวมถึงวิธีการใช้ข้อเสนอการชำระเงิน หรือการชำระเงินด้วยตนเองแบบครั้งเดียว "
author: kweekley
manager: AnnBe
ms.date: 10/30/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 707048bb0beb08c5cd8f97590195ef4f7d21c74f
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="vendor-payment-overview"></a><span data-ttu-id="777f5-103">ภาพรวมการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="777f5-103">Vendor payment overview</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="777f5-104">คำแนะนำของงานนี้จะนำคุณผ่านวิธีการต่างๆที่ใช้ในการสร้างการชำระเงินของผู้จัดจำหน่าย รวมถึงวิธีการใช้ข้อเสนอการชำระเงิน หรือการชำระเงินด้วยตนเองแบบครั้งเดียว </span><span class="sxs-lookup"><span data-stu-id="777f5-104">This task guide will walk you through various methods used to create vendor payments, including how to use a payment proposal or manually entering a one-off payment.</span></span> <span data-ttu-id="777f5-105">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="777f5-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="777f5-106">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-106">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="777f5-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="777f5-107">Click New.</span></span>
3. <span data-ttu-id="777f5-108">เลือก สมุดชำระเงินรายวันที่จะบันทึกการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="777f5-108">Select the payment journal in which to save the vendor payments.</span></span> 
4. <span data-ttu-id="777f5-109">เลือก สมุดรายวัน หรือป้อนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="777f5-109">Select the journal or manually enter it.</span></span>
5. <span data-ttu-id="777f5-110">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="777f5-110">Click Lines.</span></span>
6. <span data-ttu-id="777f5-111">คลิก ข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-111">Click Payment proposal.</span></span>
7. <span data-ttu-id="777f5-112">คลิกสร้างข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-112">Click Create payment proposal.</span></span>
    * <span data-ttu-id="777f5-113">ข้อเสนอการชำระเงินเป็นการสอบถามที่ใช้ในการเลือกใบแจ้งหนี้สำหรับการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="777f5-113">The payment proposal is a query used to select invoices for payment.</span></span> <span data-ttu-id="777f5-114">คุณสามารถแก้ไขรายการใบแจ้งหนี้ที่จะชำระเงินก่อนที่จะสร้างการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="777f5-114">You can edit the list of invoices to pay before creating or generating the vendor payments.</span></span>  
8. <span data-ttu-id="777f5-115">เลือก ใบแจ้งหนี้สำหรับการชำระเงินตามวันที่ครบกำหนดชำระ วันที่ให้ส่วนลดเงินสด หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="777f5-115">Select invoices for payment by due date, cash discount, or both.</span></span> 
9. <span data-ttu-id="777f5-116">ป้อนวันที่สำหรับการเปรียบเทียบกับวันที่ครบกำหนดชำระ หรือวันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="777f5-116">Enter the date for comparing to the due date or cash discount.</span></span> 
10. <span data-ttu-id="777f5-117">ไม่จำเป็นต้องระบุ: ป้อนวันชำระเงินที่ใช้สำหรับการชำระเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="777f5-117">Optional: Enter a payment date used for all payments.</span></span>
    * <span data-ttu-id="777f5-118">วันที่ที่กรอกที่นี่จะเป็นวันที่ชำระเงินสำหรับการชำระเงินทั้งหมดที่เกิดขึ้น โดยไม่คำนึงถึงวันที่ครบกำหนดหรือวันที่ตามส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="777f5-118">The date entered here will be the payment date for all payments created, regardless of the due date or cash discount date.</span></span>  
11. <span data-ttu-id="777f5-119">ไม่จำเป็นต้องระบุ: ป้อนวันชำระเงินขั้นต่ำสุดที่สามารถใช้เป็นวันชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-119">Optional: Enter a minimum payment date which may be used as the payment date.</span></span>
    * <span data-ttu-id="777f5-120">วันชำระเงินอย่างต่ำจะเป็นวันแรกสุดที่ใช้เมื่อสร้างการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="777f5-120">The minimum payment date will be the earliest date used when creating payments.</span></span> <span data-ttu-id="777f5-121">ตัวอย่างเช่น ถ้าใบแจ้งหนี้มีวันที่ครบกำหนดหลังจากวันชำระเงินขั้นต่ำสุด วันที่ครบกำหนดจะกลายเป็น วันชำระเงินแทนที่เป็นวันชำระเงินขั้นต่ำสุดเพื่อชำระใบแจ้งหนี้ในวันล่าสุดที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="777f5-121">For example, if an invoice has a due date after the minimum payment date, the due date will become the payment date instead of the minimum payment date in order to pay the invoice on the latest possible date.</span></span>  
12. <span data-ttu-id="777f5-122">ป้อนข้อจำกัดในการสอบถามเพิ่มเติมภายใต้เรกคอร์ดที่รวม</span><span class="sxs-lookup"><span data-stu-id="777f5-122">Enter additional query restrictions under Records to include.</span></span>
    * <span data-ttu-id="777f5-123">ตัวกรองมักถูกใช้เพื่อกำหนดรูปแบบของใบแจ้งหนี้ที่เลือกสำหรับการชำระเงินโดยเรียงตามกลุ่มผู้จัดจำหน่ายหรือวิธีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="777f5-123">The filter is often used to restrict the invoices selected for payment by vendor group or method of payment.</span></span> <span data-ttu-id="777f5-124">ตัวอย่างเช่น คุณอาจเพิ่มตัวกรองข้อมูลเพื่อชำระใบแจ้งหนี้ โดยใช้เช็คค่าจ้างนี้ทำงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="777f5-124">For example, you may add a filter to only pay invoices by check in this pay run.</span></span>  
13. <span data-ttu-id="777f5-125">ป้อนข้อจำกัดในการสอบถามเพิ่มเติม หรือค่าเริ่มต้นของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-125">Enter additional query restriction or payment defaults.</span></span> 
    * <span data-ttu-id="777f5-126">พารามิเตอร์เพิ่มเติมสามารถใช้เพื่อกำหนดสกุลเงินในการชำระเงิน หรือเพื่อเปิดใช้งานการชำระเงินส่วนกลางสำหรับชำระค่าจ้างนี้</span><span class="sxs-lookup"><span data-stu-id="777f5-126">The additional parameters can be used to define the payment currency or to enable centralized payments for this pay run.</span></span>  
14. <span data-ttu-id="777f5-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="777f5-127">Click OK.</span></span>
    * <span data-ttu-id="777f5-128">หลังจากการคลิกตกลง ผลลัพธ์ของแบบสอบถามจะปรากฏขึ้น </span><span class="sxs-lookup"><span data-stu-id="777f5-128">After clicking OK, the results of the query will appear.</span></span> <span data-ttu-id="777f5-129">ถ้าคุณไม่ต้องการแสดงตัวอย่างรายการใบแจ้งหนี้ที่เลือกไว้ชำระ คุณสามารถกลับไปที่แท็บด่วนพารามิเตอร์ และเปลี่ยนการตั้งค่าสร้างการชำระเงิน โดยไม่มีการแสดงตัวอย่างใบแจ้งหนี้ = ใช่</span><span class="sxs-lookup"><span data-stu-id="777f5-129">If you don't want to preview the list of invoices selected to pay, you can go back to the Parameters fast tab and change the setting Create payments without invoice preview = Yes.</span></span>  
15. <span data-ttu-id="777f5-130">เลือก ปุ่มภาพรวมของการชำระเงินแสดงเพื่อดูการชำระเงินที่จะถูกสร้างสำหรับผู้จัดจำหน่ายในใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="777f5-130">Choose the Show payment overview button to view the payments that will be created for the vendor on the invoice selected.</span></span>
16. <span data-ttu-id="777f5-131">เลือกปุ่ม ซ่อนภาพรวมการชำระ เพื่อซ่อนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-131">Choose the Hide payment overview button to hide the payments.</span></span> 
17. <span data-ttu-id="777f5-132">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-132">Click Create payments.</span></span>
    * <span data-ttu-id="777f5-133">ก่อนการเลือกจะสร้างการชำระเงิน คุณสามารถคลิกขวาบนกริด และส่งออกรายการใบแจ้งหนี้ไปที่ Excel </span><span class="sxs-lookup"><span data-stu-id="777f5-133">Before choosing Create payments, you can right click on the grid and export the list of invoices to Excel.</span></span> <span data-ttu-id="777f5-134">ปุ่มการสร้างการชำระเงินจะสร้างการชำระเงินของผู้จัดจำหน่ายในสมุดการชำระเงินรายวัน</span><span class="sxs-lookup"><span data-stu-id="777f5-134">The Create payments button will create the vendor payments in the payment journal.</span></span>  
18. <span data-ttu-id="777f5-135">สแกนการชำระเงินของคุณ และตรวจสอบว่าวิธีการชำระเงินถูกกำหนดสำหรับการชำระเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="777f5-135">Scan your payments and make sure the method of payment is defined for all payments.</span></span> 
    * <span data-ttu-id="777f5-136">ถ้าคุณสร้างการชำระเงิน เช่น การพิมพ์เช็ค หรือการสร้างการชำระเงินทางอิเล็กทรอนิกส์ จะต้องมีการกำหนดวิธีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="777f5-136">If you generate the payments, such as printing a check or creating an electronic payment, the method of payment must be defined.</span></span> <span data-ttu-id="777f5-137">วิธีการชำระเงินก็จะเริ่มต้นจากการสร้างการชำระเงินผ่านบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="777f5-137">The method of payment will also default the bank account from the payment will be made.</span></span>  
19. <span data-ttu-id="777f5-138">คลิก สร้างเพื่อสร้างการชำระเงินที่ใช้ครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="777f5-138">Click New to create a one-off payment.</span></span>
    * <span data-ttu-id="777f5-139">การชำระเงินที่ใช้ครั้งเดียวกับสมุดการชำระเงินรายวันสามารถถูกเพิ่มได้ทุกเมื่อก่อนที่จะลงรายการบัญชี </span><span class="sxs-lookup"><span data-stu-id="777f5-139">A one-off payment can be added to a payment journal at any time prior to posting.</span></span> <span data-ttu-id="777f5-140">ซึ่งทำสำเร็จได้โดยการคลิกปุ่ม สร้าง และการบวกเพิ่มข้อมูลการชำระเงินด้วยตนเอง แทนที่จะใช้ในข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-140">This is done by clicking the New button and adding the payment information manually, rather than using the Payment proposal.</span></span>  
20. <span data-ttu-id="777f5-141">เลือก ผู้จัดจำหน่ายที่จะทำการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-141">Select the vendor to whom the payment will be made.</span></span>
21. <span data-ttu-id="777f5-142">ถ้าใบแจ้งหนี้มีการชำระค่าจ้าง เลือกธุรกรรมการชำระเพื่อเลือกใบแจ้งหนี้สำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-142">If an invoice exists to pay, select Settle transactions to select the invoice for payment.</span></span>
    * <span data-ttu-id="777f5-143">ถ้านี่เป็นการชำระเงินล่วงหน้า ขั้นตอนนี้เป็นทางเลือก </span><span class="sxs-lookup"><span data-stu-id="777f5-143">If this is a prepayment, this step is optional.</span></span> <span data-ttu-id="777f5-144">คุณสามารถสร้างการชำระเงิน โดยไม่เลือกใบแจ้งหนี้ใดๆ</span><span class="sxs-lookup"><span data-stu-id="777f5-144">You can create the payment without selecting any invoice.</span></span>  
22. <span data-ttu-id="777f5-145">ทำเครื่องหมายที่ใบแจ้งหนี้ที่จะชำระ</span><span class="sxs-lookup"><span data-stu-id="777f5-145">Mark any invoices that will be paid.</span></span>
    * <span data-ttu-id="777f5-146">ถ้าคุณใช้ธุรกรรมการเงินเพื่อเลือกใบแจ้งหนี้สำหรับการชำระเงิน ยอดการชำระเงินจะถูกคำนวณโดยอัตโนมัติตามที่คุณได้ทำเครื่องหมายสำหรับการชำระเงินบนใบแจ้งหนี้ และจำนวนเงินที่คุณป้อนในยอดเงินชำระ</span><span class="sxs-lookup"><span data-stu-id="777f5-146">If you use the Settle transactions to select the invoices for payment, the payment amount will automatically be calculated based on what invoices you mark for payment, and what amount you enter in the Amount to settle.</span></span>  
23. <span data-ttu-id="777f5-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="777f5-147">Click OK.</span></span>
24. <span data-ttu-id="777f5-148">ถ้าคุณต้องการลบการชำระเงิน ทำเครื่องหมายที่แถว</span><span class="sxs-lookup"><span data-stu-id="777f5-148">If you want to delete a payment, mark the row.</span></span>
25. <span data-ttu-id="777f5-149">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="777f5-149">Click Delete.</span></span>
    * <span data-ttu-id="777f5-150">การลบการชำระเงินจะลบเฉพาะการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="777f5-150">Deleting a payment will only delete the payment.</span></span> <span data-ttu-id="777f5-151">ใบแจ้งหนี้ใดๆ ที่ถูกทำเครื่องหมายสำหรับการชำระเงินจะยังคงพร้อมที่จะถูกชำระโดยการชำระเงินอื่น</span><span class="sxs-lookup"><span data-stu-id="777f5-151">Any invoices marked for payment will still be available to be paid by another payment.</span></span>  
26. <span data-ttu-id="777f5-152">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="777f5-152">Click Yes.</span></span>
27. <span data-ttu-id="777f5-153">เลือก สร้างการชำระเงิน เพื่อพิมพ์เช็ค หรือสร้างไฟล์การชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="777f5-153">Choose Generate payment to print Checks or create the electronic payment file.</span></span>
28. <span data-ttu-id="777f5-154">เลือก วิธีการออกใบแจ้งหนี้ที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="777f5-154">Select the method of payment that you want to generate.</span></span>
    * <span data-ttu-id="777f5-155">สมุดรายวันการชำระเงินสามารถประกอบด้วย การชำระเงินสำหรับทั้งเช็คและการชำระเงินทางอิเล็กทรอนิกส์ แต่คุณสามารถสร้างรูปแบบประเภทการชำระเงินได้เพียงหนึ่งประเภทเท่านั้นในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="777f5-155">The payment journal can contain payments for both Checks and electronic payments, but you can only generate one payment type at a time.</span></span>  
29. <span data-ttu-id="777f5-156">เลือก บัญชีธนาคารที่จะสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-156">Select the bank account from which to generate the payments.</span></span>
30. <span data-ttu-id="777f5-157">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="777f5-157">Click OK.</span></span>
    * <span data-ttu-id="777f5-158">การชำระเงินจะถูกสร้างขึ้นสำหรับการชำระเงินที่ตรงกับวิธีการชำระเงินและบัญชีธนาคารที่คุณเลือกไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="777f5-158">Payments will only be generated for payments that match the Method of payment and Bank account you selected.</span></span>  
31. <span data-ttu-id="777f5-159">ถ้าคุณกำลังสร้างเช็ค เลือกเอกสารเพื่อให้แน่ใจว่าปลายทางการพิมพ์ถูกต้องสำหรับเช็ค</span><span class="sxs-lookup"><span data-stu-id="777f5-159">If you are generating Checks, choose Document to ensure the correct print destination for the Checks.</span></span>
32. <span data-ttu-id="777f5-160">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="777f5-160">Click OK.</span></span>
33. <span data-ttu-id="777f5-161">คลิก ตกลง เพื่อสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="777f5-161">Click OK to generate the payments.</span></span>
34. <span data-ttu-id="777f5-162">คลิก ลงรายการบัญชี ถ้าการชำระเงินได้รับอนุมัติและถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="777f5-162">Click Post if all the payments are approved and generated.</span></span> 


