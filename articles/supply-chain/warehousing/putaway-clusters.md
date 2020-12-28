---
title: คลัสเตอร์ของการสำรองสินค้า
description: คลัสเตอร์ของการสำรองสินค้านำเสนอวิธีการเลือกแผ่นป้ายทะเบียนหลายใบในเวลาเดียวกันแล้วใช้สำหรับการสำรองในสถานที่เก็บต่าง ๆ โดยทั่วไปแล้วจะมีประโยชน์มากสำหรับธุรกิจขายปลีก ป้ายทะเบียนจะไม่มีการจัดเก็บสินค้าคงคลังเต็มจำนวน
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a330ddccbd17c92443232fc8488e36a59235773
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512341"
---
# <a name="putaway-clusters"></a><span data-ttu-id="c4995-104">คลัสเตอร์ของการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4995-105">คลัสเตอร์ของการสำรองสินค้านำเสนอวิธีการเลือกแผ่นป้ายทะเบียนหลายใบในเวลาเดียวกันแล้วใช้สำหรับการสำรองในสถานที่เก็บต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c4995-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="c4995-106">กระบวนการนี้มักจะถูกอ้างอิงเป็น *ระบบ Milk Run*</span><span class="sxs-lookup"><span data-stu-id="c4995-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="c4995-107">คลัสเตอร์ของการสำรองสินค้ามีประโยชน์มากสำหรับธุรกิจขายปลีก โดยทั่วไปป้ายทะเบียนจะไม่มีการจัดเก็บสินค้าคงคลังเต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="c4995-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="c4995-108">เปิดคุณลักษณะคลัสเตอร์ของการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="c4995-109">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="c4995-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c4995-110">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="c4995-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c4995-111">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c4995-112">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c4995-113">**ชื่อคุณลักษณะ:** *คุณลักษณะคลัสเตอร์ของการสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="c4995-114">การตั้งค่าสำหรับสถานการณ์ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c4995-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="c4995-115">โพรไฟล์ของคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-115">Cluster profiles</span></span>

<span data-ttu-id="c4995-116">โปรไฟล์ของคลัสเตอร์ของการสำรองสินค้ากำหนดสถานที่ที่สินค้าจะไป ขึ้นอยู่กับสถานที่เก็บที่กำหนดให้กับสินค้าเมื่อเวลาของการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="c4995-117">ถ้าต้องการคลัสเตอร์ที่แตกต่างกัน ควรสร้างคลัสเตอร์ของการสำรองสินค้าที่แตกต่างกัน หนึ่งรายการสำหรับรายการเมนูบนอุปกรณ์เคลื่อนที่แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="c4995-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="c4995-118">ไปที่ **การบริหารคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> โพรไฟล์ของคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c4995-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="c4995-119">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c4995-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4995-120">บนมุมมอง **ส่วนหัว** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c4995-121">**รหัสโปรไฟล์คลัสเตอร์ของการสำรองสินค้า:** *คลัสเตอร์ของการสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4995-122">**ชื่อรหัสโปรไฟล์คลัสเตอร์ของการสำรองสินค้า:** *คลัสเตอร์ของการสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4995-123">**ชนิดของคลัสเตอร์:** *การสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="c4995-124">**หมายเลขลำดับ:** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c4995-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="c4995-125">เลือก **บันทึก** เพื่อทำให้ฟิลด์ที่จำเป็นบนแท็บด่วน **ทั่วไป** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c4995-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="c4995-126">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c4995-127">**การกำหนดเวลาการกำหนดคลัสเตอร์:** *เมื่อได้รับสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="c4995-128">ฟิลด์นี้กำหนดว่าจะมีการกำหนดคลัสเตอร์การสำรองสินค้าทันทีเมื่อได้รับสินค้าคงคลังหรือไม่ หรือควรจะเรียงลำดับในภายหลังหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c4995-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="c4995-129">**กฎการกำหนดคลัสเตอร์:** *ด้วยตนเอง*</span><span class="sxs-lookup"><span data-stu-id="c4995-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="c4995-130">ฟิลด์นี้กำหนดว่าจะทำการกำหนดคลัสเตอร์โดยอัตโนมัติด้วยระบบหรือด้วยตนเองโดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c4995-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="c4995-131">**รหัสคำสั่ง:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="c4995-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="c4995-132">**ค้นหาคลัสเตอร์ของการสำรองสินค้า:** *การรับสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="c4995-133">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c4995-133">The following values are available:</span></span>

        - <span data-ttu-id="c4995-134">**การรับสินค้า** – พบที่ตั้งทันทีในระหว่างการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="c4995-135">**ปิดคลัสเตอร์** – พบที่ตั้งเมื่อปิดคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="c4995-136">**สั่งการโดยผู้ใช้** – พบที่ตั้งเมื่อป้ายทะเบียนถูกเบิกจากคลัสเตอร์สำหรับการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="c4995-137">ในกรณีนี้ จะไม่มีการระบุที่ตั้งเมื่อมีการสร้างงานการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="c4995-138">ในระหว่างการสำรองสินค้าเอง ผู้ใช้ต้องสแกนป้ายทะเบียนหรือรหัสงานที่จะเริ่มต้นการวางขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="c4995-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="c4995-139">ระบบจะค้นหาสถานที่เก็บสำรองอีกครั้ง และบอกผู้ใช้สถานที่ที่จะใช้ในการเก็บปริมาณที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="c4995-140">**คลัสเตอร์การสำรองสินค้าต่อผู้ใช้:** *ไม่ใช่*</span><span class="sxs-lookup"><span data-stu-id="c4995-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="c4995-141">ฟิลด์นี้กำหนดว่าแต่ละคลัสเตอร์ควรจะไม่ซ้ำกันสำหรับแต่ละผู้ใช้เมื่อมีการกำหนดคลัสเตอร์โดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c4995-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="c4995-142">พร้อมใช้งานเฉพาะเมื่อฟิลด์ **กฎการกำหนดคลัสเตอร์** มีการตั้งค่าเป็น *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="c4995-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="c4995-143">**ข้อจำกัดหน่วยนับ:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="c4995-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="c4995-144">ฟิลด์นี้จะกำหนดหน่วยที่ต้องได้รับสำหรับโปรไฟล์เพื่อให้มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="c4995-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="c4995-145">ถ้าฟิลด์นี้ว่าง ระบบจะมีผลบังคับใช้ทุกหน่วย</span><span class="sxs-lookup"><span data-stu-id="c4995-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="c4995-146">**การแบ่งหน่วยงาน:** *แต่ละรายการ*</span><span class="sxs-lookup"><span data-stu-id="c4995-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="c4995-147">ฟิลด์นี้กำหนดว่าควรมีการรวมบัญชีสินค้าคงคลังทั้งหมด (โดยใช้รหัสคลัสเตอร์และป้ายทะเบียน) บนป้ายทะเบียนหนึ่งเมื่อปิดคลัสเตอร์ และไม่ว่าควรจะเป็นป้ายทะเบียนเดี่ยวหรือแยกต่างหากบนป้ายทะเบียนที่ได้รับหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c4995-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="c4995-148">ฟิลด์นี้จะไม่พร้อมใช้งานเมื่อฟิลด์ **ค้นหาคลัสเตอร์ของการสำรองสินค้า** มีการตั้งค่าเป็น *การรับสินค้า*</span><span class="sxs-lookup"><span data-stu-id="c4995-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="c4995-149">**คลัสเตอร์ยังคงมีอยู่เป็นป้ายทะเบียนหลัก:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="c4995-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="c4995-150">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* เมื่อขั้นตอนการวางเสร็จสมบูรณ์ รหัสคลัสเตอร์จะกลายเป็นป้ายทะเบียนหลัก และสินค้าทั้งหมดบนรหัสคลัสเตอร์จะถูกเชื่อมโยงกับป้ายทะเบียนหลักนั้น</span><span class="sxs-lookup"><span data-stu-id="c4995-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="c4995-151">บนแท็บด่วน **การเรียงลำดับของคลัสเตอร์** คุณสามารถกำหนดเงื่อนไขการเรียงลำดับการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="c4995-152">เลือก **สร้าง** บนแถบเครื่องมือเพื่อเพิ่มบรรทัด แล้วจากนั้นตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="c4995-153">**หมายเลขลำดับ:** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c4995-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="c4995-154">**ชื่อฟิลด์:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="c4995-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="c4995-155">ฟิลด์นี้จะกำหนดฟิลด์ที่บรรทัดนี้ควรใช้เป็นเงื่อนไขการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="c4995-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="c4995-156">**การเรียงลำดับ:** *น้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="c4995-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="c4995-157">ฟิลด์นี้กำหนดว่าควรจะทำการเรียงลำดับในลำดับจากน้อยไปมากหรือจากมากไปน้อย</span><span class="sxs-lookup"><span data-stu-id="c4995-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="c4995-158">บน FastTab **แม่แบบงานคลัสเตอร์** ให้เลือก **สร้าง** บนแถบเครื่องมือ แล้วจากนั้นตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="c4995-159">**ชนิดของใบสั่งงาน:** *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="c4995-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="c4995-160">**แม่แบบงาน:** *61 PO โดยตรง*</span><span class="sxs-lookup"><span data-stu-id="c4995-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="c4995-161">ในบานหน้าต่างการดำเนินการ ให้เลือก **บันทึก** แล้วเลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="c4995-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="c4995-162">ในกล่องโต้ตอบ **คลัสเตอร์ของการสำรองสินค้า** บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดที่สองไปยังการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="c4995-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="c4995-163">อัปเดตรายการการสอบถามดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c4995-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="c4995-164">ตาราง</span><span class="sxs-lookup"><span data-stu-id="c4995-164">Table</span></span> | <span data-ttu-id="c4995-165">ตารางสืบทอด</span><span class="sxs-lookup"><span data-stu-id="c4995-165">Derived table</span></span> | <span data-ttu-id="c4995-166">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c4995-166">Field</span></span> | <span data-ttu-id="c4995-167">เกณฑ์</span><span class="sxs-lookup"><span data-stu-id="c4995-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="c4995-168">งาน</span><span class="sxs-lookup"><span data-stu-id="c4995-168">Work</span></span> | <span data-ttu-id="c4995-169">งาน</span><span class="sxs-lookup"><span data-stu-id="c4995-169">Work</span></span> | <span data-ttu-id="c4995-170">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-170">Warehouse</span></span> | <span data-ttu-id="c4995-171">*61*</span><span class="sxs-lookup"><span data-stu-id="c4995-171">*61*</span></span> |
    | <span data-ttu-id="c4995-172">งาน</span><span class="sxs-lookup"><span data-stu-id="c4995-172">Work</span></span> | <span data-ttu-id="c4995-173">งาน</span><span class="sxs-lookup"><span data-stu-id="c4995-173">Work</span></span> | <span data-ttu-id="c4995-174">รหัสงาน</span><span class="sxs-lookup"><span data-stu-id="c4995-174">Work ID</span></span> | <span data-ttu-id="c4995-175">ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="c4995-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="c4995-176">เลือก **ตกลง** เพื่อบันทึกการสอบถามและปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="c4995-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="c4995-177">ในบานหน้าต่างการดำเนินการ เลือก **บันทึก** และปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c4995-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4995-178">ฟิลด์ในโปรไฟล์คลัสเตอร์ที่ปรากฏเป็นสีจางเมื่อ **สร้างรหัสคลัสเตอร์** ตั้งค่าเป็น *ใช่* ไม่พร้อมใช้งานและไม่ได้รับการพิจารณาเมื่อมีการใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="c4995-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="c4995-179">รายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c4995-179">Mobile device menu items</span></span>

<span data-ttu-id="c4995-180">รายการเมนูของอุปกรณ์เคลื่อนที่ใหม่สองรายการจะพร้อมใช้งานสำหรับคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="c4995-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="c4995-181">รายการเมนู **รับและเรียงลำดับคลัสเตอร์** เพื่อเรียงลำดับสินค้าคงคลังที่ได้รับลงในคลัสเตอร์ของการสำรองสินค้าเมื่อมีการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="c4995-182">รายการเมนู **คลัสเตอร์ของการสำรองสินค้า** ใช้เพื่อสำรองคลัสเตอร์หลังจากที่ได้รับการกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="c4995-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="c4995-183">การรับและการเรียงลำดับคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-183">Receive and sort cluster</span></span>

<span data-ttu-id="c4995-184">สร้างรายการเมนูของอุปกรณ์เคลื่อนที่ใหม่สำหรับการรับสินค้าคงคลังและการเรียงลำดับเข้าในคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="c4995-185">รายการเมนูนี้จะสร้างงานขาเข้าหลังจากที่ได้รับสินค้าคงคลัง ซึ่งบ่งชี้ว่าจะมีการใช้รายการเมนูการรับสินค้าสำหรับคลัสเตอร์ของการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="c4995-186">รายการเมนู **การรับและการเรียงลำดับคลัสเตอร์** สามารถใช้กับรายการเมนูการรับสินค้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="c4995-187">การรับรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4995-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="c4995-188">การรับสินค้าใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4995-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="c4995-189">การรับสินค้าของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="c4995-189">Load item receiving</span></span>

1. <span data-ttu-id="c4995-190">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="c4995-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c4995-191">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c4995-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4995-192">บนมุมมอง **ส่วนหัว** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c4995-193">**ชื่อรายการเมนู:** *การรับและการเรียงลำดับคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="c4995-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="c4995-194">**ชื่อ:** *การรับและการเรียงลำดับคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="c4995-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="c4995-195">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="c4995-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c4995-196">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="c4995-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c4995-197">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c4995-198">**กระบวนการสร้างงาน:** *การรับสินค้าใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="c4995-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="c4995-199">**สร้างป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="c4995-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="c4995-200">**กำหนดคลัสเตอร์ของการสำรองสินค้า:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="c4995-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="c4995-201">ตัวเลือก **กำหนดคลัสเตอร์ของการสำรองสินค้า** จะพร้อมใช้งานสำหรับกิจกรรม *กระบวนการสร้างงาน* หนึ่งขั้นตอนสำหรับการได้รับสินค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c4995-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="c4995-202">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="c4995-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="c4995-203">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c4995-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="c4995-204">การสำรองสินค้าแบบคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-204">Cluster putaway</span></span>

<span data-ttu-id="c4995-205">สร้างรายการเมนูของอุปกรณ์เคลื่อนที่ใหม่สำหรับการสำรองคลัสเตอร์หลังจากที่ได้รับการกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="c4995-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="c4995-206">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="c4995-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c4995-207">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c4995-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4995-208">บนมุมมอง **ส่วนหัว** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c4995-209">**ชื่อรายการเมนู:** *การสำรองสินค้าของคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="c4995-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4995-210">**ชื่อ:** *การสำรองสินค้าของคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="c4995-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c4995-211">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="c4995-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c4995-212">**ใช้งานที่มีอยู่:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="c4995-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="c4995-213">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **สั่งการโดย** เป็น *การสำรองสินค้าของคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="c4995-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="c4995-214">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="c4995-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="c4995-215">บนแท็บด่วน **คลาสของงาน** ให้ตั้งค่าคลาสของงานที่ถูกต้องสำหรับรายการเมนูของอุปกรณ์เคลื่อนที่นี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="c4995-216">**รหัสคลาสงาน:** *การซื้อ*</span><span class="sxs-lookup"><span data-stu-id="c4995-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="c4995-217">**ชนิดของใบสั่งงาน:** *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="c4995-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="c4995-218">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c4995-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="c4995-219">เมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c4995-219">Mobile device menu</span></span>

<span data-ttu-id="c4995-220">เพิ่มรายการเมนูที่คุณเพิ่งสร้างไปยังเมนูขาเข้าของแอปบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="c4995-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="c4995-221">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="c4995-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c4995-222">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c4995-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c4995-223">ในรายการเมนู ให้เลือก **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="c4995-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="c4995-224">ในรายการ **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้ค้นหาและเลือกรายการเมนู **การรับและการเรียงลำดับคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c4995-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="c4995-225">เลือกปุ่มลูกศรขวาเพื่อย้ายรายการเมนูที่เลือก ไปยังรายการ **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="c4995-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="c4995-226">ใช้ปุ่มลูกศรขึ้นหรือลูกศรลงเพื่อย้ายรายการเมนูไปยังตำแหน่งที่ต้องการในเมนู</span><span class="sxs-lookup"><span data-stu-id="c4995-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="c4995-227">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c4995-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c4995-228">ทำซ้ำขั้นตอนที่ 4 ถึง 7 เพื่อเพิ่มรายการเมนูที่เหลือ:</span><span class="sxs-lookup"><span data-stu-id="c4995-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="c4995-229">กำหนดคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-229">Assign cluster</span></span>
    - <span data-ttu-id="c4995-230">การสำรองสินค้าแบบคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c4995-231">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="c4995-231">Example scenario</span></span>

<span data-ttu-id="c4995-232">สถานการณ์จำลองนี้จำลองการประมวลผลคลัสเตอร์ของการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="c4995-233">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4995-233">Create a purchase order</span></span>

1. <span data-ttu-id="c4995-234">ไปที่ **บัญชีเจ้าหนี้ \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c4995-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="c4995-235">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c4995-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c4995-236">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c4995-237">**บัญชีผู้จัดจำหน่าย:** *1001*</span><span class="sxs-lookup"><span data-stu-id="c4995-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="c4995-238">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="c4995-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="c4995-239">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c4995-239">Select **OK**.</span></span>

    <span data-ttu-id="c4995-240">หน้า **ใบสั่งซื้อทั้งหมด** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c4995-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="c4995-241">บนหน้า **ใบสั่งซื้อทั้งหมด** บนแท็บด่วน **รายการใบสั่งซื้อ** ให้ใช้ปุ่ม **เพิ่มรายการ** เพื่อเพิ่มรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c4995-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="c4995-242">รายการใบสั่งซื้อ 1:</span><span class="sxs-lookup"><span data-stu-id="c4995-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="c4995-243">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c4995-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="c4995-244">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="c4995-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="c4995-245">รายการใบสั่งซื้อ 2:</span><span class="sxs-lookup"><span data-stu-id="c4995-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="c4995-246">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="c4995-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="c4995-247">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="c4995-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="c4995-248">รายการใบสั่งซื้อ 3:</span><span class="sxs-lookup"><span data-stu-id="c4995-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="c4995-249">**หมายเลขสินค้า:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="c4995-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="c4995-250">**ปริมาณ:** *30*</span><span class="sxs-lookup"><span data-stu-id="c4995-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="c4995-251">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c4995-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c4995-252">สร้างบันทึกย่อของหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4995-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="c4995-253">รับสินค้าคงคลังและสำรองจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c4995-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="c4995-254">การรับและการเรียงลำดับสินค้าคงคลังสู่คลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="c4995-255">ลงชื่อเข้าใช้ไปยังแอปคลังสินค้าในฐานะผู้ใช้ที่ตั้งค่าคลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="c4995-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="c4995-256">บนเมนูหลัก ให้เลือก **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="c4995-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="c4995-257">บนเมนู **ขาเข้า** เลือก **การรับและการเรียงลำดับคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c4995-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="c4995-258">ในฟิลด์ **Ponum** ให้ป้อนหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4995-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="c4995-259">เลือก **ตกลง** (ปุ่มสัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="c4995-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="c4995-260">เลือกฟิลด์ **สินค้า** ป้อนหมายเลขสินค้า *A0001* และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c4995-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="c4995-261">เลือกฟิลด์ **ปริมาณ** ป้อน *10* โดยใช้แผ่นหมายเลข แล้วเลือกปุ่มเครื่องหมายถูก</span><span class="sxs-lookup"><span data-stu-id="c4995-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="c4995-262">บนหน้างาน **ปริมาณ** ให้เลือก **ตกลง** (ปุ่มเครื่องหมายถูก) เพื่อยืนยันปริมาณที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="c4995-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="c4995-263">บนหน้างาน **สินค้า** ให้เลือก **ตกลง** เพื่อยืนยันว่ามีการป้อนสินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="c4995-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="c4995-264">เลือกฟิลด์ **รหัสคลัสเตอร์** และป้อนค่าเพื่อกำหนดรหัสสำหรับคลัสเตอร์ที่คุณกำลังสร้างอยู่</span><span class="sxs-lookup"><span data-stu-id="c4995-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="c4995-265">รหัสที่คุณป้อนที่นี่จะใช้เมื่อได้รับสินค้าที่เหลือสองรายการบนใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c4995-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="c4995-266">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c4995-266">Select **OK**.</span></span>

    <span data-ttu-id="c4995-267">หน้างาน **Ponum** จะปรากฏขึ้นและแสดงข้อความ "งานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="c4995-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="c4995-268">ขณะนี้ได้รับสินค้า *A0001* สู่สถานที่เก็บ *RECV* และกำหนดให้กับรหัสคลัสเตอร์ที่คุณป้อนไว้ในขั้นตอนที่10</span><span class="sxs-lookup"><span data-stu-id="c4995-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="c4995-269">ทำซ้ำขั้นตอนที่ 4 ถึง 11 เพื่อรับสินค้าที่เหลือสองรายการจากใบสั่งซื้อและกำหนดให้กับรหัสคลัสเตอร์:</span><span class="sxs-lookup"><span data-stu-id="c4995-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="c4995-270">ปริมาณของสินค้า *A0002* จำนวน *20* รายการ</span><span class="sxs-lookup"><span data-stu-id="c4995-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="c4995-271">ปริมาณของสินค้า *M9215* จำนวน *30* รายการ</span><span class="sxs-lookup"><span data-stu-id="c4995-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="c4995-272">ปิดคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-272">Close the cluster</span></span>

<span data-ttu-id="c4995-273">ก่อนที่จะมีการจัดเก็บสินค้าในคลัสเตอร์ ต้องปิดคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="c4995-274">ใน Supply Chain Management ให้ไปที่ **การจัดการคลังสินค้า \> งาน \> ขาออก \> คลัสเตอร์งาน**</span><span class="sxs-lookup"><span data-stu-id="c4995-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="c4995-275">บนหน้า **คลัสเตอร์งาน** ในส่วน **คลัสเตอร์งาน** ให้ค้นหาฟิลด์ **รหัสคลัสเตอร์** สำหรับรหัสคลัสเตอร์ที่คุณป้อนไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c4995-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="c4995-276">ถ้าไม่มีการแสดงคลัสเตอร์ แสดงว่าอาจปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="c4995-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="c4995-277">เมื่อต้องการกำหนดว่าคลัสเตอร์ปิดแล้วหรือไม่ ให้เลือกกล่องกาเครื่องหมาย **แสดงงานที่ปิด** และค้นหารหัสคลัสเตอร์ที่คุณป้อนไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c4995-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="c4995-278">จากนั้นทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c4995-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="c4995-279">ถ้าคลัสเตอร์ปิดแล้ว ให้ข้ามขั้นตอนที่เหลือของกระบวนงานนี้ และย้ายไปยังกระบวนงานถัดไป [จัดเก็บคลัสเตอร์](#put-the-cluster-away)</span><span class="sxs-lookup"><span data-stu-id="c4995-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="c4995-280">ถ้ายังไม่ได้ปิดคลัสเตอร์ ให้ทำตามขั้นตอนที่เหลือของกระบวนงานนี้เพื่อปิดคลัสเตอร์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c4995-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="c4995-281">จากนั้นเลื่อนไปยังกระบวนงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="c4995-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="c4995-282">ในส่วน **คลัสเตอร์งาน** ให้เลือกรหัสคลัสเตอร์ที่คุณป้อนไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c4995-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="c4995-283">บนหน้าต่างการดำเนินการ เลือก **ปิดคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c4995-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="c4995-284">หลังจากปิดคลัสเตอร์แล้ว จะไม่มีการแสดงในส่วน **คลัสเตอร์งาน** อีกต่อไป (ยกเว้นว่ามีการเลือกกล่องกาเครื่องหมาย **แสดงงานที่ปิด** )</span><span class="sxs-lookup"><span data-stu-id="c4995-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="c4995-285">จัดเก็บคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-285">Put the cluster away</span></span>

1. <span data-ttu-id="c4995-286">ลงชื่อเข้าใช้ไปยังแอปคลังสินค้าในฐานะผู้ใช้ที่ตั้งค่าคลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="c4995-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="c4995-287">บนเมนูหลัก ให้เลือก **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="c4995-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="c4995-288">บนเมนู **ขาเข้า** ให้เลือก **การสำรองสินค้าคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="c4995-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="c4995-289">เลือก **รหัสคลัสเตอร์** และป้อนรหัสคลัสเตอร์ที่คุณป้อนไว้ก่อนหน้านี้สำหรับคลัสเตอร์ที่ปิด</span><span class="sxs-lookup"><span data-stu-id="c4995-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="c4995-290">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c4995-290">Select **OK**.</span></span>

    <span data-ttu-id="c4995-291">หน้า **การสำรองสินค้าคลัสเตอร์: เบิกสินค้า** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c4995-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="c4995-292">แสดงรหัสคลัสเตอร์ สถานที่เบิกสินค้า สินค้า (ค่า *หลายค่า* จะแสดงขึ้น) และปริมาณรวมในคลัสเตอร์ที่ต้องเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="c4995-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="c4995-293">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c4995-293">Select **OK**.</span></span>

    <span data-ttu-id="c4995-294">หน้า **การสำรองสินค้าคลัสเตอร์: จัดเก็บ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c4995-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="c4995-295">คำแนะนำ **การจัดเก็บ** ระบุรหัสคลัสเตอร์ สถานที่เก็บ สินค้า ปริมาณรวม และรหัสป้ายทะเบียนสำหรับสินค้าที่ได้รับแล้วในคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="c4995-296">คุณมีตัวเลือกมาตรฐานที่จะแทนที่หรือผ่านขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="c4995-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="c4995-297">![การสำรองสินค้าของคลัสเตอร์: หน้าจัดเก็บ](media/Cluster_putaway-Put.png "การสำรองสินค้าของคลัสเตอร์: หน้าจัดเก็บ")</span><span class="sxs-lookup"><span data-stu-id="c4995-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="c4995-298">เลือก **ตกลง** เพื่อยืนยันการสำรองสินค้าของคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="c4995-299">ข้อความ "คลัสเตอร์เสร็จสมบูรณ์" จะแสดง</span><span class="sxs-lookup"><span data-stu-id="c4995-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="c4995-300">หมายเหตุและเคล็ดลับ</span><span class="sxs-lookup"><span data-stu-id="c4995-300">Notes and tips</span></span>

<span data-ttu-id="c4995-301">สำหรับกรณีที่รหัสคลัสเตอร์จะกลายเป็นป้ายทะเบียนหลักสำหรับแท่นวางสินค้าที่ซ้อนกัน ตำแหน่งการจัดเก็บจะมีการกำหนดโดยอัตโนมัติเมื่อมีการสแกนรหัสคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="c4995-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="c4995-302">ไม่ต้องสแกนป้ายทะเบียนเพิ่มเติม ถึงแม้ว่าจะมีการตั้งค่าการสร้างป้ายทะเบียนเป็นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c4995-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
