---
title: ข้อมูลใบแจ้งหนี้ที่สำคัญในระบบบัญชีเจ้าหนี้โดยใช้กลุ่มใบแจ้งหนี้
description: หัวข้อนี้จะอธิบายวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227171"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="90258-103">ข้อมูลใบแจ้งหนี้ที่สำคัญในระบบบัญชีเจ้าหนี้โดยใช้กลุ่มใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90258-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90258-104">หัวข้อนี้จะอธิบายวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90258-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="90258-105">แล้วใช้กลุ่มใบแจ้งหนี้เพื่อจับคู่ใบแจ้งหนี้กับใบสั่งซื้อ และทำให้ค่าใช้จ่ายในหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="90258-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="90258-106">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="90258-106">Create a purchase order</span></span>
1. <span data-ttu-id="90258-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="90258-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="90258-108">เลือก **สร้าง** เพื่อสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="90258-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="90258-109">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือกผู้จัดจำหน่ายสำหรับรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="90258-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="90258-110">ตัวอย่างเช่น เลือกผู้จัดจำหน่าย **1001**</span><span class="sxs-lookup"><span data-stu-id="90258-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="90258-111">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="90258-111">Select **OK**.</span></span>
5. <span data-ttu-id="90258-112">ในฟิลด์ **หมายเลขสินค้า** ให้เลือกหมายเลขสินค้าบริการในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="90258-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="90258-113">ตัวอย่างเช่น เลือก **S0001**</span><span class="sxs-lookup"><span data-stu-id="90258-113">For example, select **S0001**.</span></span> <span data-ttu-id="90258-114">ยอดเงินสุทธิคือ 75.00 </span><span class="sxs-lookup"><span data-stu-id="90258-114">The net amount is 75.00.</span></span>  <span data-ttu-id="90258-115">ซึ่งเป็นยอดเงินที่คาดหมายในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90258-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="90258-116">บนบานหน้าต่างการดำเนินการ เลือก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="90258-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="90258-117">เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="90258-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="90258-118">สร้างและลงรายการบัญชีและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90258-118">Create and post and invoice</span></span>
1. <span data-ttu-id="90258-119">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > ทะเบียนใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="90258-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="90258-120">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="90258-120">Select **New**.</span></span>
3. <span data-ttu-id="90258-121">เปิดการค้นหาเพื่อเลือกชื่อของทะเบียนใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="90258-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="90258-122">เลือกชื่อทะเบียนใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="90258-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="90258-123">เลือก **รายการ** เพื่อเปิดการลงทะเบียนและป้อนรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="90258-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="90258-124">ในการค้นหา เลือกผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="90258-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="90258-125">ตัวอย่างเช่น เลือกผู้จัดจำหน่าย **1001**</span><span class="sxs-lookup"><span data-stu-id="90258-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="90258-126">ในฟิลด์ **ใบแจ้งหนี้** ให้ป้อนหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="90258-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="90258-127">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90258-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="90258-128">ในฟิลด์ **เครดิต** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="90258-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="90258-129">ในฟิลด์ **ใบสั่งซื้อ** ให้เปิดรายการแบบหล่นลงเพื่อเลือกใบสั่งซื้อที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="90258-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="90258-130">ในฟิลด์ **อนุมัติโดย** ให้เน้นผู้อนุมัติในรายการแบบหล่นลง และคลิก **เลือก** เพื่อเลือกผู้อนุมัตินั้น</span><span class="sxs-lookup"><span data-stu-id="90258-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="90258-131">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="90258-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="90258-132">เปิดใบแจ้งหนี้จากกลุ่มและจับคู่กับใบสั่งซื้อเพื่อทำให้กระบวนการใบแจ้งหนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="90258-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="90258-133">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > กลุ่มใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="90258-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="90258-134">เลือก **ใบสั่งซื้อ** เพื่อสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบแจ้งหนี้ในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="90258-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="90258-135">เลือกใบแจ้งหนี้ที่คุณต้องการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="90258-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="90258-136">เลือก **ปรับปรุงสถานะการจับคู่** เพื่อทำการจับคู่ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="90258-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="90258-137">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="90258-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="90258-138">เลือก **เปลี่ยนมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="90258-138">Select **Change view**.</span></span>
7. <span data-ttu-id="90258-139">เลือก **มุมมองกริด**</span><span class="sxs-lookup"><span data-stu-id="90258-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="90258-140">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="90258-140">Select **Post**.</span></span>
9. <span data-ttu-id="90258-141">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="90258-141">Close the form.</span></span>
10. <span data-ttu-id="90258-142">ในบานหน้าต่างการนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="90258-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="90258-143">เลือกผู้จัดจำหน่ายที่อยู่บนใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="90258-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="90258-144">ตัวอย่างเช่น เลือกผู้จัดจำหน่าย **1001**</span><span class="sxs-lookup"><span data-stu-id="90258-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="90258-145">ในบานหน้าต่างการดำเนินการ เลือก **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="90258-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="90258-146">เลือก **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="90258-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="90258-147">เลือกใบแจ้งหนี้ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="90258-147">Select the invoice that you created.</span></span> <span data-ttu-id="90258-148">ทะเบียนใบแจ้งหนี้คงค้างมีการกลับรายการ และลงรายการบัญชีค่าใช้จ่ายที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="90258-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]