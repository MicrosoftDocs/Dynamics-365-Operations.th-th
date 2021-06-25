---
title: ไม่สามารถลดปริมาณได้เมื่อยกเลิกใบสั่งขาย
description: ไม่สามารถลดปริมาณได้เมื่อยกเลิกใบสั่งขาย
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230847"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="db658-103">ไม่สามารถลดปริมาณได้เมื่อยกเลิกใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="db658-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="db658-104">รหัสข้อผิดพลาด: SYS138831</span><span class="sxs-lookup"><span data-stu-id="db658-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="db658-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="db658-105">Symptoms</span></span>

<span data-ttu-id="db658-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db658-106">The system shows the following error message:</span></span>

> <span data-ttu-id="db658-107">ไม่สามารถลดปริมาณได้</span><span class="sxs-lookup"><span data-stu-id="db658-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="db658-108">จํานวนรายการความเคลื่อนไหวของสินค้าคงคลังในใบสั่งต่ำเกินไป เนื่องจากปริมาณหรือบางส่วนของธุรกรรมถูกอ้างอิงโดยใบสั่งผลผลิตหรือใบสั่งผลิต หรือมีการเลือกกับธุรกรรมอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="db658-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="db658-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="db658-109">Cause</span></span>

<span data-ttu-id="db658-110">ถ้างานสัมพันธ์กับใบสั่งขาย คุณจะไม่สามารถยกเลิกใบสั่งขายได้จนกว่างานจะถูกยกเลิกและกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="db658-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="db658-111">ข้อกำหนดนี้ใช้ได้ ถึงแม้ว่างานที่เชื่อมโยงกับใบสั่งขายปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="db658-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="db658-112">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="db658-112">Resolution</span></span>

<span data-ttu-id="db658-113">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db658-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="db658-114">ยกเลิกงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="db658-114">Cancel open work.</span></span>
1. <span data-ttu-id="db658-115">ลบงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="db658-115">Delete the load.</span></span>
1. <span data-ttu-id="db658-116">ลดปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="db658-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="db658-117">ยกเลิกงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="db658-117">Cancel open work</span></span>

<span data-ttu-id="db658-118">หากต้องการยกเลิกงานที่เปิด ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="db658-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="db658-119">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การล้าง \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="db658-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="db658-120">ในฟิลด์ **รหัสงาน** ให้ระบุรหัสของงานที่คุณต้องการยกเลิก และในปัจจุบันมี **ค่าสถานะงาน** เป็น *เปิด* *อยู่ระหว่างดำเนินการ* *ยกเลิก* *รวม* หรือ *ปิด*</span><span class="sxs-lookup"><span data-stu-id="db658-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="db658-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="db658-121">Select **OK**.</span></span>
1. <span data-ttu-id="db658-122">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="db658-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="db658-123">ลบงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="db658-123">Delete the load</span></span>

<span data-ttu-id="db658-124">หากต้องการลบจำนวนงานในศูนย์การผลิต ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="db658-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="db658-125">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="db658-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="db658-126">เปิดใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="db658-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="db658-127">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **คลังสินค้า \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="db658-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="db658-128">บนหน้า **งาน** บนบานหน้าต่างการดำเนินการในแท็บ **งาน** ในกลุ่ม **งาน** เลือก **ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="db658-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="db658-129">ยืนยันว่าฟิลด์ **สถานะงาน** ถูกตั้งเป็น *ยกเลิกแล้ว*</span><span class="sxs-lookup"><span data-stu-id="db658-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="db658-130">ปิดหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="db658-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="db658-131">บนหน้ารายละเอียดใบสั่งขาย บนแท็บด่วน **รายการใบสั่งขาย** ให้เลือก **คลังสินค้า \> รายละเอียดจำนวนงานในศูนย์การผลิต**</span><span class="sxs-lookup"><span data-stu-id="db658-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="db658-132">บนบานหน้าต่างการดำเนินการ ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="db658-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="db658-133">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการลบจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="db658-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="db658-134">ปิดหน้า **จำนวนงานในศูนย์การผลิต**</span><span class="sxs-lookup"><span data-stu-id="db658-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="db658-135">ลดปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="db658-135">Reduce the picked quantity</span></span>

<span data-ttu-id="db658-136">เมื่องานทั้งหมดถูกยกเลิก ให้ปฏิบัติตามขั้นตอนเหล่านี้เพื่อลดปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="db658-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="db658-137">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="db658-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="db658-138">เปิดใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="db658-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="db658-139">บนแท็บด่วน **รายการใบสั่งขาย** ให้เลือก **อัปเดตรายการ \> เบิกสินค้า** จากแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="db658-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="db658-140">บนหน้า **เบิกสินค้า** ในส่วน **ธุรกรรม** ให้เลือกรายการที่มีการตั้งค่าฟิลด์ **สถานะการออกใช้** เป็น *เบิกสินค้าแล้ว*</span><span class="sxs-lookup"><span data-stu-id="db658-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="db658-141">ในส่วน **ธุรกรรม** ให้เลือก **เพิ่มรายการการเบิกสินค้า** จากแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="db658-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="db658-142">ในส่วน **รายการเบิกสินค้า** ให้เลือก **ยืนยันการเบิกสินค้าทั้งหมด** จากแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="db658-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="db658-143">ปิดหน้า **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="db658-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="db658-144">ในหน้ารายละเอียดใบสั่งขาย บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งขาย** ในกลุ่ม **รักษา** เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="db658-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="db658-145">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยกเลิกใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="db658-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
