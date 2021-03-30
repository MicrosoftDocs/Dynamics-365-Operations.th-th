---
title: ลงทะเบียนค่าคอมมิชชันการขาย
description: หัวข้อนี้จะอธิบายถึงวิธีการคำนวณและลงทะเบียนค่าคอมมิชชันการขาย
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82c8dc2f284923b5583bf983413a015b9ece8252
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205940"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="2090d-103">ลงทะเบียนค่าคอมมิชชันการขาย</span><span class="sxs-lookup"><span data-stu-id="2090d-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2090d-104">หัวข้อนี้จะอธิบายถึงวิธีการคำนวณและลงทะเบียนค่าคอมมิชชันการขาย</span><span class="sxs-lookup"><span data-stu-id="2090d-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="2090d-105">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="2090d-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="2090d-106">ก่อนที่จะเริ่มคู่มือนี้ เรียกใช้คุ่มือที่เรียกว่า "ตั้งค่ากฎค่าคอมมิชชันการขาย" เพื่อให้แน่ใจว่า คุณได้ตั้งค่าการคำนวณค่าคอมมิชชันที่จำเป็นทั้งหมดแล้ว </span><span class="sxs-lookup"><span data-stu-id="2090d-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="2090d-107">จดบันทึกหมายเลขลูกค้าและสินค้าที่คุณได้เลือกไว้สำหรับกระบวนการค่าคอมมิชชัน และใช้เมื่อถูกถามเพื่อสร้างใบสั่งขายในคู่มือนี้</span><span class="sxs-lookup"><span data-stu-id="2090d-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="2090d-108">ออกใบแจ้งหนี้ใบสั่งขายที่ทำให้พนักงานขายมีสิทธิ์ได้รับค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2090d-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="2090d-109">ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2090d-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="2090d-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2090d-110">Select **New**.</span></span>
3. <span data-ttu-id="2090d-111">ในฟิลด์ **บัญชีลูกค้า** ให้เลือกเรกคอร์ดที่ต้องการจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="2090d-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="2090d-112">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2090d-112">Select **OK**.</span></span>
5. <span data-ttu-id="2090d-113">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="2090d-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="2090d-114">เลือก **เปลี่ยนมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="2090d-114">Select **Change view**.</span></span>
7. <span data-ttu-id="2090d-115">เลือก **มุมมองส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="2090d-115">Select **Header view**.</span></span>
8. <span data-ttu-id="2090d-116">ขยายส่วน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="2090d-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="2090d-117">ค่าในฟิลด์ **กลุ่มการขาย** แสดงกลุ่มที่มีพนักงานขายที่ได้รับมอบหมายหนึ่งคนขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="2090d-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="2090d-118">บุคลากรในกลุ่มจะเป็นคนที่จะได้รับค่าคอมมิชชันเมื่อใบสั่งออกใบแจ้งหนี้ ตามอัตราที่กำหนดไว้ล่วงหน้าและการกระจายสินค้า</span><span class="sxs-lookup"><span data-stu-id="2090d-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="2090d-119">ค่าจะถูกคัดลอกจากบัตรลูกค้า แต่คุณสามารถเปลี่ยนถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2090d-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="2090d-120">กลุ่มการขายจะได้รับการคัดลอกไปยังรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2090d-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="2090d-121">คุณสามารถเปลี่ยนได้เพื่อให้แตกต่างจากสิ่งที่อยู่ในส่วนหัวและ/หรือระหว่างรายการ</span><span class="sxs-lookup"><span data-stu-id="2090d-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="2090d-122">ค่าในฟิลด์ **กลุ่มค่าคอมมิชชัน** แสดงถึงกลุ่มที่คุณสร้างสำหรับลูกค้าอย่างน้อยหนึ่งราย พร้อมวัตถุประสงค์ของการติดตามค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2090d-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="2090d-123">ค่าจะถูกคัดลอกจากบัตรลูกค้า แต่คุณสามารถเปลี่ยนถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2090d-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="2090d-124">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="2090d-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="2090d-125">เลือก **เปลี่ยนมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="2090d-125">Select **Change view**.</span></span>
11. <span data-ttu-id="2090d-126">เลือก **มุมมองรายการ**</span><span class="sxs-lookup"><span data-stu-id="2090d-126">Select **Line view**.</span></span>
12. <span data-ttu-id="2090d-127">ในเมนูแบบหล่นลงของฟิลด์ **หมายเลขสินค้า** ให้เลือกสินค้าที่คุณตั้งค่าไว้สำหรับค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2090d-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="2090d-128">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="2090d-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="2090d-129">จดบันทึกยอดเงินสุทธิของรายการ </span><span class="sxs-lookup"><span data-stu-id="2090d-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="2090d-130">ซึ่งจะแสดงการรายได้จากการขาย ในตัวอย่างนี้เป็นพื้นฐานสำหรับการคำนวณค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2090d-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="2090d-131">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2090d-131">Select **Save**.</span></span>
15. <span data-ttu-id="2090d-132">ในบานหน้าต่างการดำเนินการ เลือก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="2090d-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="2090d-133">เลือก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="2090d-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="2090d-134">ขยายส่วน **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="2090d-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="2090d-135">ในฟิลด์ **ปริมาณ** ให้เลือก **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2090d-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="2090d-136">เลือก **ใช่** ในฟิลด์ **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2090d-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="2090d-137">เลือก **ตกลง** แล้วจากนั้น เลือก **ตกลง** ในบานหน้าต่างถัดไป</span><span class="sxs-lookup"><span data-stu-id="2090d-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="2090d-138">อาจใช้เวลาสักครู่เพื่อลงรายบัญชีธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="2090d-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="2090d-139">อนุญาตให้การประมวลผลเสร็จสมบูรณ์ และห้ามปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2090d-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="2090d-140">ตรวจทานค่าคอมมิชชันการขายที่ลงทะเบียนแล้ว</span><span class="sxs-lookup"><span data-stu-id="2090d-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="2090d-141">บนบานหน้าต่างการดำเนินการ เลือก **ใบแจ้งหนี้** และจากนั้น เลือก **ใบแจ้งหนี้** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2090d-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="2090d-142">บนบานหน้าต่างการดำเนินการ เลือก **ใบแจ้งหนี้** และจากนั้น เลือก **ธุรกรรมค่าคอมมิชชัน**</span><span class="sxs-lookup"><span data-stu-id="2090d-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="2090d-143">แท็บ **ภาพรวม** แสดงรายการที่แสดงถึงยอดค่าคอมมิชชันที่ชำระแก่พนักงานขายที่เกี่ยวข้องกับใบสั่งขายที่ออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2090d-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="2090d-144">ลองตรวจทานรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="2090d-144">Let's review the details.</span></span>  
    - <span data-ttu-id="2090d-145">ถ้าคุณใช้คู่มือ "ตั้งค่ากฎค่าคอมมิชชันการขาย" เพื่อตั้งค่ากลุ่ม **การขายที่มีค่าคอมมิชชัน** จะมีพนักงานขายสองคนจะได้รับค่าคอมมิชชันการขาย และค่าคอมมิชชันจะถูกแบ่งเท่าๆ กันระหว่างพวกเขา</span><span class="sxs-lookup"><span data-stu-id="2090d-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="2090d-146">ในตัวอย่างนี้ มีการคำนวณยอดรวมของค่าคอมมิชชันเป็นเปอร์เซ็นต์ของรายได้การขาย (ยอดเงินสุทธิของรายการใบสั่ง)</span><span class="sxs-lookup"><span data-stu-id="2090d-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="2090d-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2090d-147">Close the page.</span></span>
4. <span data-ttu-id="2090d-148">เลือก **ใบสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="2090d-148">Select **Voucher**.</span></span> <span data-ttu-id="2090d-149">คุณสามารถตรวจทานธุรกรรมใบสำคัญสำหรับยอดเงินค่าคอมมิชชัน ที่ได้ลงรายการบัญชีค่าใช้จ่ายค่าคอมมิชชันที่กำหนดไว้ล่วงหน้า และบัญชีเจ้าหนี้ค่าคอมมิชชัน</span><span class="sxs-lookup"><span data-stu-id="2090d-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]