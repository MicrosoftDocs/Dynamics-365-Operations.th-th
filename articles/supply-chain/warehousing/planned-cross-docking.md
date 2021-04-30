---
title: การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้
description: หัวข้อนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า ซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911259"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="6c148-104">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="6c148-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c148-105">หัวข้อนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="6c148-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="6c148-106">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าคือกระบวนการของคลังสินค้าซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="6c148-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="6c148-107">สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="6c148-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="6c148-108">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าช่วยให้ผู้ปฏิบัติงานข้ามการสำรองสินค้าขาเข้าและการเบิกสิค้าขาออกของสินค้าคงคลังที่มีการทำเครื่องหมายสำหรับใบสั่งขาออกอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c148-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="6c148-109">ดังนั้นจำนวนครั้งที่สินค้าคงคลังถูกสัมผัสจะถูกย่อให้เล็กที่สุดเท่าที่จะเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="6c148-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="6c148-110">นอกจากนี้เนื่องจากมีการโต้ตอบกับระบบน้อยลง การประหยัดเวลาและพื้นที่บนชั้นร้านค้าของคลังสินค้าจะเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="6c148-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="6c148-111">ก่อนที่คุณจะสามารถรันการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้ คุณต้องตั้งค่าคอนฟิกเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าใหม่ ซึ่งจะมีการระบุแหล่งที่มาของการจัดหาวัสดุและชุดอื่นๆ ของความต้องการสำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="6c148-112">เมื่อสร้างใบสั่งขาออกจะต้องมีการทำเครื่องหมายรายการสำหรับใบสั่งขาเข้าที่มีสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6c148-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="6c148-113">คุณสามารถเลือกฟิลด์รหัสสั่งบนแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้ ในลักษณะเดียวกับที่คุณตั้งค่าการเพิ่มเติมสินค้าและใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6c148-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="6c148-114">ในขณะรับใบสั่งขาเข้า การตั้งค่าการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะระบุความต้องการของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและสร้างงานการเคลื่อนย้ายสำหรับปริมาณที่ต้องการโดยขึ้นอยู่กับการตั้งค่าของคำสั่งสถานที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6c148-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="6c148-115">รายการความเคลื่อนไหวของสินค้าคงคลังจะ *ไม่* ลงทะเบียนเมื่อมีการยกเลิกการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ถึงแม้ว่าจะมีการเปิดใช้การตั้งค่าสำหรับความสามารถนี้ในพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="6c148-116">เปิดใช้งานลักษณะการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="6c148-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="6c148-117">ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในหัวข้อนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดคุณลักษณะต่อไปนี้ในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="6c148-118">*การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้*</span><span class="sxs-lookup"><span data-stu-id="6c148-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="6c148-119">*เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่มีคำสั่งสถานที่*</span><span class="sxs-lookup"><span data-stu-id="6c148-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="6c148-120">คุณลักษณะนี้ช่วยให้สามารถระบุฟิลด์ **รหัสคำสั่ง** บนแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้คล้ายกับวิธีการตั้งค่าแม่แบบการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="6c148-121">การเปิดใช้งานคุณลักษณะนี้จะป้องกันคุณไม่ให้เพิ่มรหัสข้อควบคุมบนรายการแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าสำหรับรายการ *เบิกสินค้า* สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="6c148-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="6c148-122">ซึ่งช่วยให้มั่นใจว่าจะสามารถกําหนดสถานที่ส่งครั้งสุดท้ายระหว่างการสร้างงานก่อนที่จะพิจารณาแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="6c148-123">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="6c148-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="6c148-124">สร้างวิธีการลงรายการบัญชีการบรรทุกใหม่</span><span class="sxs-lookup"><span data-stu-id="6c148-124">Regenerate load posting methods</span></span>

<span data-ttu-id="6c148-125">การใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้าจะถูกนำมาใช้เป็นวิธีการลงรายการบัญชีการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="6c148-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="6c148-126">หลังจากที่คุณเปิดใช้งานลักษณะการทำงานแล้ว คุณต้องสร้างวิธีการใหม่</span><span class="sxs-lookup"><span data-stu-id="6c148-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="6c148-127">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> วิธีการลงรายการบัญชีการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="6c148-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="6c148-128">บนบานหน้าต่างการดำเนินการ เลือก **สร้างวิธีการใหม่**</span><span class="sxs-lookup"><span data-stu-id="6c148-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="6c148-129">เมื่อการดำเนินการเสร็จสมบูรณ์แล้ว คุณควรจะเห็นวิธีการที่มีค่า **ชื่อวิธีการ** *planCrossDocking*</span><span class="sxs-lookup"><span data-stu-id="6c148-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="6c148-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6c148-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="6c148-131">สร้างเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="6c148-132">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6c148-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="6c148-133">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6c148-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="6c148-134">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="6c148-135">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c148-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="6c148-136">ฟิลด์นี้จะกำหนดใบสั่งที่จะมีการประเมินเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6c148-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="6c148-137">**รหัสเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="6c148-138">**คำอธิบาย:** *คลังสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="6c148-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="6c148-139">**นโยบายการนำออกใช้ความต้องการ** *ก่อนใบรับการจัดหาสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="6c148-140">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c148-141">การตั้งค่าบนแท็บด่วน **การวางแผน** ควบคุมวิธีการทำงานของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6c148-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="6c148-142">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-142">Set the following values:</span></span>

    - <span data-ttu-id="6c148-143">**ข้อกำหนดของความต้องการ:** *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="6c148-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="6c148-144">ฟิลด์นี้จะกำหนดความต้องการของสินค้าคงคลังที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c148-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="6c148-145">ถ้าต้องการให้มีการเชื่อมโยงความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือก *การทำเครื่องหมาย*</span><span class="sxs-lookup"><span data-stu-id="6c148-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="6c148-146">ถ้าต้องการให้มีการจองสินค้าตามความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือกการ *การจองสินค้าสำหรับใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="6c148-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="6c148-147">**ชนิดของการระบุตำแหน่ง:** *สถานที่จัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="6c148-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="6c148-148">ฟิลด์นี้กำหนดว่างานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าควรใช้สถานที่ที่จัดเตรียม/การบรรทุกจากการจัดส่งหรือไม่ และควรใช้คำสั่งของสถานที่ในการค้นหาสถานที่การจัดเตรียม/การบรรทุกของตนเองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6c148-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="6c148-149">**เท็มเพลตงาน** ปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="6c148-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="6c148-150">ฟิลด์นี้จะกำหนดเท็มเพลตงานที่ควรใช้เมื่อมีการสร้างงานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="6c148-151">**ตรวจสอบความถูกต้องของใบรับการจัดหาสินค้าซ้ำ:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="6c148-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="6c148-152">ตัวเลือกนี้กำหนดว่าควรตรวจสอบความถูกต้องของการจัดหาวัสดุในระหว่างการรับสินค้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6c148-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="6c148-153">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ทั้งหน้าต่างเวลาสูงสุดและช่วงวันหมดอายุจะถูกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="6c148-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="6c148-154">**รหัสคำสั่ง:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="6c148-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="6c148-155">ตัวเลือกนี้เปิดใช้งานโดยคุณลักษณะ *แม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าด้วยคำสั่งสถานที่*</span><span class="sxs-lookup"><span data-stu-id="6c148-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="6c148-156">ระบบใช้ใบสั่งสถานที่เพื่อช่วยระบุสถานที่ที่ดีที่สุดที่จะย้ายสินค้าคงคลังในการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="6c148-157">คุณสามารถตั้งค่าโดยการกําหนดรหัสข้อกําหนดให้กับแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เกี่ยวข้องแต่ละแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="6c148-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="6c148-158">ถ้ามีการกำหนดรหัสสถานที่ ระบบจะไม่ค้นหาคำสั่งสถานที่ตามรหัสสถานที่เมื่อต้องสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="6c148-159">ด้วยวิธีนี้ คุณสามารถจํากัดข้อความของสถานที่ที่จะใช้กับแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="6c148-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="6c148-160">**ตรวจสอบความถูกต้องของหน้าต่างเวลา:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="6c148-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="6c148-161">ตัวเลือกนี้กำหนดว่าควรประเมินหน้าต่างเวลาสูงสุดเมื่อมีการเลือกแหล่งที่มาของการจัดหาวัสดุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6c148-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="6c148-162">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ฟิลด์ที่เกี่ยวข้องกับหน้าต่างเวลาสูงสุดและหน้าต่างเวลาต่ำสุดจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6c148-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="6c148-163">**หน้าต่างเวลาสูงสุด:** *5*</span><span class="sxs-lookup"><span data-stu-id="6c148-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="6c148-164">ฟิลด์นี้กำหนดระยะเวลาสูงสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c148-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="6c148-165">**หน่วยของหน้าต่างเวลาสูงสุด:** *วัน*</span><span class="sxs-lookup"><span data-stu-id="6c148-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="6c148-166">**หน้าต่างเวลาต่ำสุด:** *0*</span><span class="sxs-lookup"><span data-stu-id="6c148-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="6c148-167">ฟิลด์นี้กำหนดระยะเวลาต่ำสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c148-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="6c148-168">**หน่วยของหน้าต่างเวลาต่ำสุด:** *วัน*</span><span class="sxs-lookup"><span data-stu-id="6c148-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="6c148-169">**ช่วงวันหมดอายุ:** *0*</span><span class="sxs-lookup"><span data-stu-id="6c148-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="6c148-170">*เงื่อนไขที่หมดอายุแรกออกก่อน (FEFO):* ฟิลด์นี้จะกำหนดจำนวนวันสูงสุดระหว่างวันหมดอายุของชุดงานที่หมดอายุแรกที่ปัจจุบันอยู่ในคลังสินค้าและชุดงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="6c148-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="6c148-171">บนแท็บด่วน **แหล่งที่มาของการจัดหาสินค้า** คุณสามารถระบุชนิดของการจัดหาวัสดุที่มีผลบังคับใช้สำหรับเท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="6c148-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="6c148-172">เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="6c148-173">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c148-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6c148-174">**แหล่งที่มาของการจัดหาสินค้า:** *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="6c148-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="6c148-175">สร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-175">Create a work class</span></span>

1. <span data-ttu-id="6c148-176">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="6c148-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="6c148-177">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="6c148-178">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-178">Set the following values:</span></span>

    - <span data-ttu-id="6c148-179">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c148-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="6c148-180">**คำอธิบาย:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="6c148-181">**ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="6c148-182">สร้างเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-182">Create a work template</span></span>

1. <span data-ttu-id="6c148-183">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="6c148-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6c148-184">ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="6c148-185">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังแท็บ **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="6c148-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="6c148-186">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c148-187">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c148-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6c148-188">**เท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="6c148-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="6c148-189">**คำอธิบายเท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="6c148-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="6c148-190">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6c148-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="6c148-191">บนแท็บด่วน **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="6c148-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c148-192">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c148-193">**ชนิดงาน:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="6c148-194">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c148-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="6c148-195">เลือก **สร้าง** เพื่อเพิ่มบรรทัดอื่นและตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="6c148-196">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6c148-197">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c148-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="6c148-198">เลือก **บันทึก** และยืนยันว่ามีการเลือกกล่องกาเครื่องหมาย **ที่ถูกต้อง** สำหรับเท็มเพลต *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="6c148-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="6c148-199">รหัสคลาสงานสำหรับชนิดงาน *การเบิกสินค้า* และ *การวาง* ต้องเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="6c148-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="6c148-200">สร้างคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="6c148-200">Create location directives</span></span>

1. <span data-ttu-id="6c148-201">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="6c148-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="6c148-202">ในบานหน้าต่างด้านซ้าย ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="6c148-203">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="6c148-204">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c148-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6c148-205">**ชื่อ:** *การวางส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="6c148-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="6c148-206">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6c148-207">**ไซต์:** *5*</span><span class="sxs-lookup"><span data-stu-id="6c148-207">**Site:** *5*</span></span>
    - <span data-ttu-id="6c148-208">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c148-209">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6c148-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="6c148-210">บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="6c148-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c148-211">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c148-212">**ปริมาณเริ่มต้น:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c148-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="6c148-213">**ปริมาณสิ้นสุด:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="6c148-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="6c148-214">เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6c148-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="6c148-215">บนแท็บด่วน **การดำเนินการของคำสั่งสถานที่** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="6c148-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c148-216">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c148-217">**ชื่อ:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="6c148-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="6c148-218">**การใช้สถานที่คงที่:** *สถานที่คงที่และไม่คงที่*</span><span class="sxs-lookup"><span data-stu-id="6c148-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="6c148-219">เลือก **บันทึก** เพื่อให้ปุ่ม **แก้ไขการสอบถาม** บน **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6c148-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="6c148-220">เลือก **แก้ไขการสอบถาม** เพื่อเปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="6c148-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="6c148-221">บนแท็บ **ช่วง** ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่าคอนฟิกสองบรรทัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="6c148-222">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="6c148-222">Line 1:</span></span>

        - <span data-ttu-id="6c148-223">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="6c148-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="6c148-224">**ตารางที่ได้รับมา:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="6c148-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="6c148-225">**ฟิลด์:** *คลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="6c148-226">**เงื่อนไข:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="6c148-227">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="6c148-227">Line 2:</span></span>

        - <span data-ttu-id="6c148-228">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="6c148-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="6c148-229">**ตารางที่ได้รับมา:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="6c148-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="6c148-230">**ฟิลด์:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="6c148-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="6c148-231">**เงื่อนไข:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="6c148-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="6c148-232">เลือก **ตกลง** เพื่อปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="6c148-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="6c148-233">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="6c148-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="6c148-234">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="6c148-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6c148-235">ในรายการเมนูในบานหน้าต่างด้านซ้าย ให้เลือก **การสำรองการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="6c148-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="6c148-236">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="6c148-236">Select **Edit**.</span></span>
1. <span data-ttu-id="6c148-237">บนแท็บด่วน **คลาสงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="6c148-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c148-238">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c148-239">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c148-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="6c148-240">**ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6c148-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="6c148-241">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6c148-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="6c148-242">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="6c148-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="6c148-243">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6c148-243">Create a purchase order</span></span>

<span data-ttu-id="6c148-244">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งซื้อเป็นแหล่งที่มาของการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="6c148-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="6c148-245">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6c148-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="6c148-246">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6c148-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6c148-247">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6c148-248">**บัญชีผู้จัดจำหน่าย:** *104*</span><span class="sxs-lookup"><span data-stu-id="6c148-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="6c148-249">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c148-250">เลือก **ตกลง** แล้วจดบันทึกหมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="6c148-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="6c148-251">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="6c148-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="6c148-252">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="6c148-253">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6c148-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6c148-254">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="6c148-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="6c148-255">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6c148-255">Create a sales order</span></span>

<span data-ttu-id="6c148-256">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งขายเป็นแหล่งที่มาของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c148-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="6c148-257">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6c148-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6c148-258">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6c148-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6c148-259">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6c148-260">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="6c148-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="6c148-261">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c148-262">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-262">Select **OK**.</span></span>
1. <span data-ttu-id="6c148-263">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="6c148-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6c148-264">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c148-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="6c148-265">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6c148-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6c148-266">**ปริมาณ:** *3*</span><span class="sxs-lookup"><span data-stu-id="6c148-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="6c148-267">สร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="6c148-267">Create planned cross-docking</span></span>

<span data-ttu-id="6c148-268">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้จากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6c148-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="6c148-269">ในหน้า **รายละเอียดใบสั่งขาย** สำหรับใบสั่งขายที่คุณเพิ่งสร้างขึ้นในบานหน้าต่างการดำเนินการบนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6c148-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6c148-270">การดำเนินการนำออกใช้ไปยังคลังสินค้าจะสร้างบรรทัดการจัดส่งและการบรรทุกสำหรับบรรทัดใบสั่งขายและพยายามปันส่วนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="6c148-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="6c148-271">คุณได้รับข้อความแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6c148-271">You receive an informational message.</span></span> <span data-ttu-id="6c148-272">คุณได้รับข้อความแจ้งเตือนต่อไปนี้: "ไม่มีการสร้างงานสำหรับเวฟ XXXX</span><span class="sxs-lookup"><span data-stu-id="6c148-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="6c148-273">ดูล็อกประวัติการสร้างงานสำหรับรายละเอียด "</span><span class="sxs-lookup"><span data-stu-id="6c148-273">See the work creation history log for details."</span></span> <span data-ttu-id="6c148-274">ลักษณะการทำงานนี้คาดไว้ เนื่องจากไม่มีสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="6c148-275">บนแท็บด่วน **รายการใบสั่งขาย** บนเมนู **คลังสินค้า** เลือก **รายละเอียดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="6c148-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="6c148-276">หน้า **รายละเอียดการจัดส่ง** จะปรากฏขึ้นและแสดงการจัดส่งที่สร้างขึ้นสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6c148-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="6c148-277">บนแท็บด่วน **รายการการบรรทุก** โปรดสังเกตว่าฟิลด์ **ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** ถูกตั้งค่าเป็น *3*</span><span class="sxs-lookup"><span data-stu-id="6c148-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="6c148-278">เนื่องจากไม่มีสินค้าคงคลังที่มีอยู่ในคลังสินค้า แต่แหล่งที่มาของการจัดหาวัสดุที่ถูกต้องจะมาถึงภายในหน้าต่างเวลาที่กำหนดไว้ในเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6c148-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="6c148-279">บนแท็บด่วน **รายการการบรรทุก** ให้เลือก **การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** เพื่อดูรายละเอียดของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6c148-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="6c148-280">ประมวลผลการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="6c148-281">การรับใบสั่งซื้อบนแอปคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="6c148-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="6c148-282">ระบบจะได้รับปริมาณ 5 จากใบสั่งซื้อไปยังสถานที่รับสินค้าและสร้างงานสองชิ้น</span><span class="sxs-lookup"><span data-stu-id="6c148-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="6c148-283">รหัสงานแรกที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า* และเชื่อมโยงกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6c148-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="6c148-284">มีปริมาณ 3 และส่งไปยังสถานที่จัดส่งขั้นสุดท้ายเพื่อให้สามารถจัดส่งสินค้าได้ทันที</span><span class="sxs-lookup"><span data-stu-id="6c148-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="6c148-285">รหัสงานที่สองที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *ใบสั่งซื้อ* และเชื่อมโยงกับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6c148-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="6c148-286">มีปริมาณที่เหลืออยู่ของ 2 ซึ่งไม่ใช่การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและถูกส่งตรงไปยังการสำรองสินค้าไปที่การจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="6c148-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="6c148-287">ลงชื่อเข้าใช้อุปกรณ์เคลื่อนที่ในฐานะผู้ใช้ในคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="6c148-288">ไปที่ **ขาเข้า \> รับการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="6c148-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="6c148-289">ในฟิลด์ **PONum** ให้ป้อนหมายเลขใบสั่งซื้อของคุณ</span><span class="sxs-lookup"><span data-stu-id="6c148-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="6c148-290">ในฟิลด์ **ปริมาณ** ให้ป้อน *5*</span><span class="sxs-lookup"><span data-stu-id="6c148-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="6c148-291">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-291">Select **OK**.</span></span>
1. <span data-ttu-id="6c148-292">บนหน้าถัดไปให้ตั้งค่าฟิลด์ **สินค้า** เป็น *A0001*</span><span class="sxs-lookup"><span data-stu-id="6c148-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="6c148-293">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-293">Select **OK**.</span></span>
1. <span data-ttu-id="6c148-294">บนหน้าถัดไปให้ยืนยันค่า **PONum** **สินค้า** และ **ปริมาณ** โดยเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="6c148-295">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="6c148-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6c148-296">เลือก **ยกเลิก** เพื่อออก</span><span class="sxs-lookup"><span data-stu-id="6c148-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="6c148-297">สำรองสินค้าไปยังการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="6c148-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="6c148-298">ในปัจจุบันรหัสงานทั้งสองจะมีป้ายทะเบียนเป้าหมายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6c148-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="6c148-299">เมื่อต้องการดำเนินการขั้นตอนต่อไปให้เสร็จสมบูรณ์ คุณต้องได้รับรหัสงานและรหัสป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="6c148-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="6c148-300">คุณจะได้รับข้อมูลนี้จากรายละเอียดงานสำหรับบรรทัดใบสั่งซื้อและบรรทัดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6c148-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="6c148-301">อีกทางหนึ่งคือคุณสามารถไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน** และกรองข้อมูลสำหรับงานที่มีค่า **คลังสินค้า** เป็น *51*</span><span class="sxs-lookup"><span data-stu-id="6c148-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="6c148-302">บนอุปกรณ์เคลื่อนที่ ให้ไปที่ **ขาเข้า \> การสำรองการซื้อ** แล้วป้อนป้ายทะเบียนเป้าหมายจากงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="6c148-303">ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมายจากรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="6c148-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="6c148-304">หน้าการเบิกสินค้าของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะแสดงสถานที่เบิกสินค้า (*RECV*) ป้ายทะเบียนเป้าหมาย (*ป้ายทะเบียน*) สินค้า (*A0001*) และปริมาณ (*3*)</span><span class="sxs-lookup"><span data-stu-id="6c148-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="6c148-305">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-305">Select **OK**.</span></span>
1. <span data-ttu-id="6c148-306">ในฟิลด์ **LP เป้าหมาย** ให้ป้อนป้ายทะเบียนเป้าหมายสำหรับรหัสป้ายทะเบียนที่ควรจะวาง (ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า) ไปยังสถานที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6c148-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="6c148-307">คุณสามารถเลือกรหัสป้ายทะเบียนใดๆ ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c148-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="6c148-308">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-308">Select **OK**.</span></span>
1. <span data-ttu-id="6c148-309">บนหน้าถัดไป ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="6c148-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="6c148-310">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-310">Select **OK**.</span></span>
1. <span data-ttu-id="6c148-311">ยืนยันงานสำหรับการเบิกปริมาณ 2 ที่เหลือ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="6c148-312">บนหน้าถัดไป ให้เลือก **เสร็จสิ้น** เพื่อจบกระบวนการเบิกสินค้าและเริ่มกระบวนการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="6c148-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="6c148-313">แอปบนอุปกรณ์เคลื่อนที่จะนำเสนอที่ตั้งและป้ายทะเบียนที่จะนำสินค้าไปวาง</span><span class="sxs-lookup"><span data-stu-id="6c148-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="6c148-314">ยืนยันการจัดเก็บจำนวนมากของ **การวาง** โดยการเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="6c148-315">บนหน้าถัดไปให้ยืนยัน **การวาง** การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าโดยเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6c148-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="6c148-316">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="6c148-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6c148-317">เลือก **ยกเลิก** เพื่อออก</span><span class="sxs-lookup"><span data-stu-id="6c148-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="6c148-318">ภาพประกอบต่อไปนี้แสดงวิธีการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เสร็จสมบูรณ์ที่อาจปรากฏใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6c148-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="6c148-319">![การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว](media/PlannedCrossDockingWork.png "การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว")</span><span class="sxs-lookup"><span data-stu-id="6c148-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]