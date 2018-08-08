--- 
title: "ภาพรวมการชำระเงินของลูกค้า"
description: "คำแนะนำของงานนี้นำไปสู่วิธีการต่างๆ ที่เคยป้อนการชำระเงินของลูกค้า "
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7ec39168af2e6738fc5fa11163d093c230401df3
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="customer-payment-overview"></a><span data-ttu-id="9617c-103">ภาพรวมการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9617c-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9617c-104">คำแนะนำของงานนี้นำไปสู่วิธีการต่างๆ ที่เคยป้อนการชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="9617c-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="9617c-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="9617c-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9617c-106">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9617c-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9617c-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9617c-107">Click New.</span></span>
3. <span data-ttu-id="9617c-108">เลือกสมุดรายวันการชำระเงินที่จะบันทึกการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9617c-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="9617c-109">เลือกหรือป้อนสมุดรายวันด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9617c-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="9617c-110">คลิก ป้อนการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9617c-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="9617c-111">ป้อนการชำระเงินของลูกค้าจะใช้บันทึกการชำระเงินของลูกค้าหนึ่งในแต่ละครั้ง </span><span class="sxs-lookup"><span data-stu-id="9617c-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="9617c-112">คุณป้อนข้อมูลการชำระเงินที่ด้านบน และจากนั้น คุณสามารถทำเครื่องหมายในใบแจ้งหนี้ที่ชำระ ด้วยการชำระเงิน ทั้งหมดจากหน้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9617c-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="9617c-113">ป้อนลูกค้าจากการชำระเงินที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="9617c-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="9617c-114">ถ้าคุณไม่ทราบเกี่ยวกับลูกค้าแต่ทราบเกี่ยวกับธุรกรรมที่มีการชำระเงิน คุณสามารถใช้ฟิลธุรกรรมเพื่อป้อนการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="9617c-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="9617c-115">ป้อนหรือเลือกใบแจ้งหนี้ในฟิลด์ธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="9617c-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="9617c-116">ลูกค้าจะค่าเริ่มต้นโดยอัตโนมัติหลังจากที่คุณเลือกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9617c-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="9617c-117">ในฟิลด์ การอ้างอิงการชำระเงิน ให้ป้อนการอ้างอิงการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9617c-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="9617c-118">การอ้างอิงการชำระเงินอาจเป็นหมายเลขเช็คของลูกค้าหรือการอ้างอิงจากการชำระเงินทางอิเล็กทรอนิกส์ของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="9617c-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="9617c-119">การอ้างอิงการชำระเงินจะจำเป็นหากคุณทำเครื่องหมายเพื่อรวมการชำระเงินในใบนำฝาก</span><span class="sxs-lookup"><span data-stu-id="9617c-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="9617c-120">เลือกว่าการชำระเงินจะรวมอยู่ในใบนำฝากธนาคารหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9617c-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="9617c-121">ป้อนจำนวนการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9617c-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="9617c-122">ยอดการชำระเงินจะไม่เป็นค่าเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="9617c-122">The payment amount will not default.</span></span> <span data-ttu-id="9617c-123">แต่จะต้องถูกป้อนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9617c-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="9617c-124">ทำเครื่องหมายใบแจ้งหนี้ว่าได้รับการชำระเงินโดยลูกค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="9617c-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="9617c-125">ถ้าการชำระเงินเป็นการชำระเงินล่วงหน้า คุณจะไม่จำเป็นต้องทำเครื่องหมายใบแจ้งหนี้สำหรับการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="9617c-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="9617c-126">การชำระเงินยังคงสามารถบันทึกและลงรายการบัญชีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="9617c-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="9617c-127">การชำระเงินเปลี่ยนเป็นใบแจ้งหนี้สามารถเกิดขึ้นได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9617c-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="9617c-128">ป้อนจำนวนของการชำระเงินที่ควรชำระกับใบแจ้งหนี้ที่ทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="9617c-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="9617c-129">ฟิลด์นี้สามารถใช้ได้เมื่อมีการชำระเงินสำหรับการชำระเงินบางส่วน </span><span class="sxs-lookup"><span data-stu-id="9617c-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="9617c-130">ถ้าคุณไม่ได้ป้อนยอดเงิน ยอดเงินที่จะชำระจะกำหนดให้คุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9617c-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="9617c-131">คลิก บันทึกในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="9617c-131">Click Save in journal.</span></span>
    * <span data-ttu-id="9617c-132">ก่อนที่คุณบันทึกการชำระเงินในสมุดรายวัน ตรวจสอบให้แน่ใจว่าบัญชีตรงข้ามได้ถูกกำหนด </span><span class="sxs-lookup"><span data-stu-id="9617c-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="9617c-133">การใช้บันทึกในสมุดรายวันจะบันทึกการชำระเงินและย้ายไปที่สมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="9617c-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="9617c-134">จากนั้นคุณสามารถดำเนินการป้อนการชำระเงินถัดไป</span><span class="sxs-lookup"><span data-stu-id="9617c-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="9617c-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9617c-135">Close the page.</span></span>
14. <span data-ttu-id="9617c-136">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="9617c-136">Click Lines.</span></span>
    * <span data-ttu-id="9617c-137">เมื่อเปิดรายการ คุณจะเห็นการชำระเงินใดๆ คุณบันทึกบนหน้าการชำระเงินให้ลูกค้าป้อน และบันทึกลงในสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="9617c-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="9617c-138">คุณสามารถจะใช้หน้านี้เพื่อป้อนการชำระเงินของลูกค้าใหม่ หรือแก้ไขการชำระเงินของลูกค้าที่มีอยู่ก่อนที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="9617c-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="9617c-139">คลิก สร้าง เพื่อสร้างการชำระเงินอื่น</span><span class="sxs-lookup"><span data-stu-id="9617c-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="9617c-140">เลือก ลูกค้าจากการชำระเงินที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="9617c-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="9617c-141">ถ้าคุณไม่ทราบเกี่ยวกับลูกค้าแต่ทราบเกี่ยวกับใบแจ้งหนี้ที่ชำระโดยการชำระเงิน ใช้ฟิลด์ใบแจ้งหนี้เพื่อป้อนหรือเลือกใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="9617c-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="9617c-142">ลูกค้าจะกำหนดค่าเริ่มต้นหลังจากเลือกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9617c-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="9617c-143">คลิกการชำระธุรกรรมเพื่อทำเครื่องหมายในใบแจ้งหนี้ที่ชำระเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="9617c-143">Click Settle transactions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="9617c-144">คุณไม่ต้องระบุการชำระเงินกับใบแจ้งหนี้ใดๆ </span><span class="sxs-lookup"><span data-stu-id="9617c-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="9617c-145">ถ้านี่เป็นการชำระเงินล่วงหน้า หรือถ้าคุณไม่ทราบว่าใบแจ้งหนี้ได้ถูกชำระแล้ว คุณสามารถป้อน และลงรายการบัญชีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="9617c-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="9617c-146">การชำระเงินสามารถชำระกับใบแจ้งหนี้ในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="9617c-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="9617c-147">ทำเครื่องหมายใบแจ้งหนี้ที่ชำระโดยการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9617c-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="9617c-148">ป้อนจำนวนของการชำระเงินที่จะถูกชำระไปยังใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9617c-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="9617c-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9617c-149">Click OK.</span></span>
21. <span data-ttu-id="9617c-150">ในฟิลด์การอ้างอิงการชำระเงิน ป้อนการอ้างอิงการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9617c-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="9617c-151"> </span><span class="sxs-lookup"><span data-stu-id="9617c-151">.</span></span>
    * <span data-ttu-id="9617c-152">การอ้างอิงการชำระเงินจะจำเป็นหากคุณทำเครื่องหมายเพื่อรวมการชำระเงินในใบนำฝาก</span><span class="sxs-lookup"><span data-stu-id="9617c-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="9617c-153">ลงรายการบัญชีการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9617c-153">Post the customer payments.</span></span> 


