---
title: การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้
description: หัวข้อนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า ซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556277"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="218ee-104">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="218ee-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="218ee-105">หัวข้อนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="218ee-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="218ee-106">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าคือกระบวนการของคลังสินค้าซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="218ee-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="218ee-107">สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="218ee-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="218ee-108">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าช่วยให้ผู้ปฏิบัติงานข้ามการสำรองสินค้าขาเข้าและการเบิกสิค้าขาออกของสินค้าคงคลังที่มีการทำเครื่องหมายสำหรับใบสั่งขาออกอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="218ee-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="218ee-109">ดังนั้นจำนวนครั้งที่สินค้าคงคลังถูกสัมผัสจะถูกย่อให้เล็กที่สุดเท่าที่จะเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="218ee-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="218ee-110">นอกจากนี้เนื่องจากมีการโต้ตอบกับระบบน้อยลง การประหยัดเวลาและพื้นที่บนชั้นร้านค้าของคลังสินค้าจะเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="218ee-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="218ee-111">ก่อนที่จะสามารถรันการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้ ผู้ใช้ต้องตั้งค่าคอนฟิกเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าใหม่ ซึ่งจะมีการระบุแหล่งที่มาของการจัดหาวัสดุและชุดอื่นๆ ของความต้องการสำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="218ee-112">เมื่อสร้างใบสั่งขาออกจะต้องมีการทำเครื่องหมายรายการสำหรับใบสั่งขาเข้าที่มีสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="218ee-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="218ee-113">ในขณะรับใบสั่งขาเข้า การตั้งค่าการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะระบุความต้องการของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและสร้างงานการเคลื่อนย้ายสำหรับปริมาณที่ต้องการโดยขึ้นอยู่กับการตั้งค่าของคำสั่งสถานที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="218ee-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="218ee-114">รายการความเคลื่อนไหวของสินค้าคงคลังจะ **ไม่** ลงทะเบียนเมื่อมีการยกเลิกการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ถึงแม้ว่าจะมีการเปิดใช้การตั้งค่าสำหรับความสามารถนี้ในพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="218ee-115">เปิดใช้งานลักษณะการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="218ee-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="218ee-116">ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในหัวข้อนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดคุณลักษณะต่อไปนี้ในลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="218ee-117">*การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้*</span><span class="sxs-lookup"><span data-stu-id="218ee-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="218ee-118">*เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่มีคำสั่งสถานที่*</span><span class="sxs-lookup"><span data-stu-id="218ee-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="218ee-119">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="218ee-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="218ee-120">สร้างวิธีการลงรายการบัญชีการบรรทุกใหม่</span><span class="sxs-lookup"><span data-stu-id="218ee-120">Regenerate load posting methods</span></span>

<span data-ttu-id="218ee-121">การใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้าจะถูกนำมาใช้เป็นวิธีการลงรายการบัญชีการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="218ee-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="218ee-122">หลังจากที่คุณเปิดใช้งานลักษณะการทำงานแล้ว คุณต้องสร้างวิธีการใหม่</span><span class="sxs-lookup"><span data-stu-id="218ee-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="218ee-123">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> วิธีการลงรายการบัญชีการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="218ee-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="218ee-124">บนบานหน้าต่างการดำเนินการ เลือก **สร้างวิธีการใหม่**</span><span class="sxs-lookup"><span data-stu-id="218ee-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="218ee-125">เมื่อการดำเนินการเสร็จสมบูรณ์แล้ว คุณควรจะเห็นวิธีการที่มีค่า **ชื่อวิธีการ** *planCrossDocking*</span><span class="sxs-lookup"><span data-stu-id="218ee-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="218ee-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="218ee-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="218ee-127">สร้างเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="218ee-128">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า**</span><span class="sxs-lookup"><span data-stu-id="218ee-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="218ee-129">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="218ee-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="218ee-130">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="218ee-131">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="218ee-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="218ee-132">ฟิลด์นี้จะกำหนดใบสั่งที่จะมีการประเมินเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="218ee-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="218ee-133">**รหัสเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="218ee-134">**คำอธิบาย:** *คลังสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="218ee-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="218ee-135">**นโยบายการนำออกใช้ความต้องการ** *ก่อนใบรับการจัดหาสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="218ee-136">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="218ee-137">การตั้งค่าบนแท็บด่วน **การวางแผน** ควบคุมวิธีการทำงานของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="218ee-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="218ee-138">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-138">Set the following values:</span></span>

    - <span data-ttu-id="218ee-139">**ข้อกำหนดของความต้องการ:** *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="218ee-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="218ee-140">ฟิลด์นี้จะกำหนดความต้องการของสินค้าคงคลังที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="218ee-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="218ee-141">ถ้าต้องการให้มีการเชื่อมโยงความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือก *การทำเครื่องหมาย*</span><span class="sxs-lookup"><span data-stu-id="218ee-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="218ee-142">ถ้าต้องการให้มีการจองสินค้าตามความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือกการ *การจองสินค้าสำหรับใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="218ee-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="218ee-143">**ชนิดของการระบุตำแหน่ง:** *สถานที่จัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="218ee-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="218ee-144">ฟิลด์นี้กำหนดว่างานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าควรใช้สถานที่ที่จัดเตรียม/การบรรทุกจากการจัดส่งหรือไม่ และควรใช้คำสั่งของสถานที่ในการค้นหาสถานที่การจัดเตรียม/การบรรทุกของตนเองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="218ee-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="218ee-145">**เท็มเพลตงาน** ปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="218ee-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="218ee-146">ฟิลด์นี้จะกำหนดเท็มเพลตงานที่ควรใช้เมื่อมีการสร้างงานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="218ee-147">**ตรวจสอบความถูกต้องของใบรับการจัดหาสินค้าซ้ำ:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="218ee-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="218ee-148">ตัวเลือกนี้กำหนดว่าควรตรวจสอบความถูกต้องของการจัดหาวัสดุในระหว่างการรับสินค้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="218ee-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="218ee-149">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ทั้งหน้าต่างเวลาสูงสุดและช่วงวันหมดอายุจะถูกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="218ee-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="218ee-150">**รหัสคำสั่ง:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="218ee-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="218ee-151">ตัวเลือกนี้ช่วยให้ระบบสามารถใช้ใบสั่งสถานที่เพื่อช่วยระบุสถานที่ที่ดีที่สุดที่จะย้ายสินค้าคงคลังในการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="218ee-152">คุณสามารถตั้งค่าโดยการกําหนดรหัสข้อกําหนดให้กับแม่แบบการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เกี่ยวข้องแต่ละแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="218ee-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="218ee-153">รหัสข้อความแต่ละรหัสจะระบุถึงข้อความเฉพาะของสถานที่</span><span class="sxs-lookup"><span data-stu-id="218ee-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="218ee-154">**ตรวจสอบความถูกต้องของหน้าต่างเวลา:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="218ee-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="218ee-155">ตัวเลือกนี้กำหนดว่าควรประเมินหน้าต่างเวลาสูงสุดเมื่อมีการเลือกแหล่งที่มาของการจัดหาวัสดุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="218ee-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="218ee-156">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ฟิลด์ที่เกี่ยวข้องกับหน้าต่างเวลาสูงสุดและหน้าต่างเวลาต่ำสุดจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="218ee-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="218ee-157">**หน้าต่างเวลาสูงสุด:** *5*</span><span class="sxs-lookup"><span data-stu-id="218ee-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="218ee-158">ฟิลด์นี้กำหนดระยะเวลาสูงสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="218ee-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="218ee-159">**หน่วยของหน้าต่างเวลาสูงสุด:** *วัน*</span><span class="sxs-lookup"><span data-stu-id="218ee-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="218ee-160">**หน้าต่างเวลาต่ำสุด:** *0*</span><span class="sxs-lookup"><span data-stu-id="218ee-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="218ee-161">ฟิลด์นี้กำหนดระยะเวลาต่ำสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="218ee-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="218ee-162">**หน่วยของหน้าต่างเวลาต่ำสุด:** *วัน*</span><span class="sxs-lookup"><span data-stu-id="218ee-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="218ee-163">**ช่วงวันหมดอายุ:** *0*</span><span class="sxs-lookup"><span data-stu-id="218ee-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="218ee-164">*เงื่อนไขที่หมดอายุแรกออกก่อน (FEFO):* ฟิลด์นี้จะกำหนดจำนวนวันสูงสุดระหว่างวันหมดอายุของชุดงานที่หมดอายุแรกที่ปัจจุบันอยู่ในคลังสินค้าและชุดงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="218ee-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="218ee-165">บนแท็บด่วน **แหล่งที่มาของการจัดหาสินค้า** คุณสามารถระบุชนิดของการจัดหาวัสดุที่มีผลบังคับใช้สำหรับเท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="218ee-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="218ee-166">เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="218ee-167">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="218ee-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="218ee-168">**แหล่งที่มาของการจัดหาสินค้า:** *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="218ee-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="218ee-169">สร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="218ee-169">Create a work class</span></span>

1. <span data-ttu-id="218ee-170">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="218ee-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="218ee-171">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="218ee-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="218ee-172">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-172">Set the following values:</span></span>

    - <span data-ttu-id="218ee-173">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="218ee-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="218ee-174">**คำอธิบาย:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="218ee-175">**ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="218ee-176">สร้างเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="218ee-176">Create a work template</span></span>

1. <span data-ttu-id="218ee-177">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="218ee-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="218ee-178">ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="218ee-179">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังแท็บ **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="218ee-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="218ee-180">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="218ee-181">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="218ee-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="218ee-182">**เท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="218ee-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="218ee-183">**คำอธิบายเท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="218ee-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="218ee-184">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="218ee-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="218ee-185">บนแท็บด่วน **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="218ee-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="218ee-186">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="218ee-187">**ชนิดงาน:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="218ee-188">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="218ee-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="218ee-189">เลือก **สร้าง** เพื่อเพิ่มบรรทัดอื่นและตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="218ee-190">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="218ee-191">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="218ee-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="218ee-192">เลือก **บันทึก** และยืนยันว่ามีการเลือกกล่องกาเครื่องหมาย **ที่ถูกต้อง** สำหรับเท็มเพลต *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="218ee-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="218ee-193">รหัสคลาสงานสำหรับชนิดงาน *การเบิกสินค้า* และ *การวาง* ต้องเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="218ee-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="218ee-194">สร้างคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="218ee-194">Create location directives</span></span>

1. <span data-ttu-id="218ee-195">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="218ee-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="218ee-196">ในบานหน้าต่างด้านซ้าย ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="218ee-197">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="218ee-198">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="218ee-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="218ee-199">**ชื่อ:** *การวางส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="218ee-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="218ee-200">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="218ee-201">**ไซต์:** *5*</span><span class="sxs-lookup"><span data-stu-id="218ee-201">**Site:** *5*</span></span>
    - <span data-ttu-id="218ee-202">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="218ee-203">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="218ee-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="218ee-204">บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="218ee-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="218ee-205">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="218ee-206">**ปริมาณเริ่มต้น:** *1*</span><span class="sxs-lookup"><span data-stu-id="218ee-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="218ee-207">**ปริมาณสิ้นสุด:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="218ee-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="218ee-208">เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="218ee-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="218ee-209">บนแท็บด่วน **การดำเนินการของคำสั่งสถานที่** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="218ee-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="218ee-210">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="218ee-211">**ชื่อ:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="218ee-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="218ee-212">**การใช้สถานที่คงที่:** *สถานที่คงที่และไม่คงที่*</span><span class="sxs-lookup"><span data-stu-id="218ee-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="218ee-213">เลือก **บันทึก** เพื่อให้ปุ่ม **แก้ไขการสอบถาม** บน **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="218ee-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="218ee-214">เลือก **แก้ไขการสอบถาม** เพื่อเปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="218ee-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="218ee-215">บนแท็บ **ช่วง** ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่าคอนฟิกสองบรรทัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="218ee-216">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="218ee-216">Line 1:</span></span>

        - <span data-ttu-id="218ee-217">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="218ee-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="218ee-218">**ตารางที่ได้รับมา:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="218ee-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="218ee-219">**ฟิลด์:** *คลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="218ee-220">**เงื่อนไข:** *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="218ee-221">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="218ee-221">Line 2:</span></span>

        - <span data-ttu-id="218ee-222">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="218ee-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="218ee-223">**ตารางที่ได้รับมา:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="218ee-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="218ee-224">**ฟิลด์:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="218ee-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="218ee-225">**เงื่อนไข:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="218ee-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="218ee-226">เลือก **ตกลง** เพื่อปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="218ee-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="218ee-227">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="218ee-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="218ee-228">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="218ee-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="218ee-229">ในรายการเมนูในบานหน้าต่างด้านซ้าย ให้เลือก **การสำรองการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="218ee-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="218ee-230">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="218ee-230">Select **Edit**.</span></span>
1. <span data-ttu-id="218ee-231">บนแท็บด่วน **คลาสงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="218ee-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="218ee-232">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="218ee-233">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="218ee-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="218ee-234">**ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="218ee-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="218ee-235">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="218ee-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="218ee-236">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="218ee-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="218ee-237">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="218ee-237">Create a purchase order</span></span>

<span data-ttu-id="218ee-238">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งซื้อเป็นแหล่งที่มาของการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="218ee-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="218ee-239">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="218ee-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="218ee-240">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="218ee-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="218ee-241">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="218ee-242">**บัญชีผู้จัดจำหน่าย:** *104*</span><span class="sxs-lookup"><span data-stu-id="218ee-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="218ee-243">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="218ee-244">เลือก **ตกลง** แล้วจดบันทึกหมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="218ee-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="218ee-245">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="218ee-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="218ee-246">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="218ee-247">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="218ee-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="218ee-248">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="218ee-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="218ee-249">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="218ee-249">Create a sales order</span></span>

<span data-ttu-id="218ee-250">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งขายเป็นแหล่งที่มาของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="218ee-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="218ee-251">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="218ee-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="218ee-252">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="218ee-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="218ee-253">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="218ee-254">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="218ee-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="218ee-255">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="218ee-256">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-256">Select **OK**.</span></span>
1. <span data-ttu-id="218ee-257">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="218ee-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="218ee-258">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="218ee-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="218ee-259">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="218ee-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="218ee-260">**ปริมาณ:** *3*</span><span class="sxs-lookup"><span data-stu-id="218ee-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="218ee-261">สร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="218ee-261">Create planned cross-docking</span></span>

<span data-ttu-id="218ee-262">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้จากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="218ee-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="218ee-263">ในหน้า **รายละเอียดใบสั่งขาย** สำหรับใบสั่งขายที่คุณเพิ่งสร้างขึ้นในบานหน้าต่างการดำเนินการบนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="218ee-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="218ee-264">การดำเนินการนำออกใช้ไปยังคลังสินค้าจะสร้างบรรทัดการจัดส่งและการบรรทุกสำหรับบรรทัดใบสั่งขายและพยายามปันส่วนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="218ee-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="218ee-265">คุณได้รับข้อความแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="218ee-265">You receive an informational message.</span></span> <span data-ttu-id="218ee-266">คุณได้รับข้อความแจ้งเตือนต่อไปนี้: "ไม่มีการสร้างงานสำหรับเวฟ XXXX</span><span class="sxs-lookup"><span data-stu-id="218ee-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="218ee-267">ดูล็อกประวัติการสร้างงานสำหรับรายละเอียด "</span><span class="sxs-lookup"><span data-stu-id="218ee-267">See the work creation history log for details."</span></span> <span data-ttu-id="218ee-268">ลักษณะการทำงานนี้คาดไว้ เนื่องจากไม่มีสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="218ee-269">บนแท็บด่วน **รายการใบสั่งขาย** บนเมนู **คลังสินค้า** เลือก **รายละเอียดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="218ee-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="218ee-270">หน้า **รายละเอียดการจัดส่ง** จะปรากฏขึ้นและแสดงการจัดส่งที่สร้างขึ้นสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="218ee-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="218ee-271">บนแท็บด่วน **รายการการบรรทุก** โปรดสังเกตว่าฟิลด์ **ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** ถูกตั้งค่าเป็น *3*</span><span class="sxs-lookup"><span data-stu-id="218ee-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="218ee-272">เนื่องจากไม่มีสินค้าคงคลังที่มีอยู่ในคลังสินค้า แต่แหล่งที่มาของการจัดหาวัสดุที่ถูกต้องจะมาถึงภายในหน้าต่างเวลาที่กำหนดไว้ในเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="218ee-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="218ee-273">บนแท็บด่วน **รายการการบรรทุก** ให้เลือก **การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** เพื่อดูรายละเอียดของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="218ee-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="218ee-274">ประมวลผลการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="218ee-275">การรับใบสั่งซื้อบนแอปคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="218ee-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="218ee-276">ระบบจะได้รับปริมาณ 5 จากใบสั่งซื้อไปยังสถานที่รับสินค้าและสร้างงานสองชิ้น</span><span class="sxs-lookup"><span data-stu-id="218ee-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="218ee-277">รหัสงานแรกที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า* และเชื่อมโยงกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="218ee-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="218ee-278">มีปริมาณ 3 และส่งไปยังสถานที่จัดส่งขั้นสุดท้ายเพื่อให้สามารถจัดส่งสินค้าได้ทันที</span><span class="sxs-lookup"><span data-stu-id="218ee-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="218ee-279">รหัสงานที่สองที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *ใบสั่งซื้อ* และเชื่อมโยงกับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="218ee-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="218ee-280">มีปริมาณที่เหลืออยู่ของ 2 ซึ่งไม่ใช่การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและถูกส่งตรงไปยังการสำรองสินค้าไปที่การจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="218ee-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="218ee-281">ลงชื่อเข้าใช้อุปกรณ์เคลื่อนที่ในฐานะผู้ใช้ในคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="218ee-282">ไปที่ **ขาเข้า \> รับการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="218ee-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="218ee-283">ในฟิลด์ **PONum** ให้ป้อนหมายเลขใบสั่งซื้อของคุณ</span><span class="sxs-lookup"><span data-stu-id="218ee-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="218ee-284">ในฟิลด์ **ปริมาณ** ให้ป้อน *5*</span><span class="sxs-lookup"><span data-stu-id="218ee-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="218ee-285">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-285">Select **OK**.</span></span>
1. <span data-ttu-id="218ee-286">บนหน้าถัดไปให้ตั้งค่าฟิลด์ **สินค้า** เป็น *A0001*</span><span class="sxs-lookup"><span data-stu-id="218ee-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="218ee-287">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-287">Select **OK**.</span></span>
1. <span data-ttu-id="218ee-288">บนหน้าถัดไปให้ยืนยันค่า **PONum** **สินค้า** และ **ปริมาณ** โดยเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="218ee-289">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="218ee-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="218ee-290">เลือก **ยกเลิก** เพื่อออก</span><span class="sxs-lookup"><span data-stu-id="218ee-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="218ee-291">สำรองสินค้าไปยังการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="218ee-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="218ee-292">ในปัจจุบันรหัสงานทั้งสองจะมีป้ายทะเบียนเป้าหมายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="218ee-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="218ee-293">เมื่อต้องการดำเนินการขั้นตอนต่อไปให้เสร็จสมบูรณ์ คุณต้องได้รับรหัสงานและรหัสป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="218ee-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="218ee-294">คุณจะได้รับข้อมูลนี้จากรายละเอียดงานสำหรับบรรทัดใบสั่งซื้อและบรรทัดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="218ee-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="218ee-295">อีกทางหนึ่งคือคุณสามารถไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน** และกรองข้อมูลสำหรับงานที่มีค่า **คลังสินค้า** เป็น *51*</span><span class="sxs-lookup"><span data-stu-id="218ee-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="218ee-296">บนอุปกรณ์เคลื่อนที่ ให้ไปที่ **ขาเข้า \> การสำรองการซื้อ** แล้วป้อนป้ายทะเบียนเป้าหมายจากงาน</span><span class="sxs-lookup"><span data-stu-id="218ee-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="218ee-297">ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมายจากรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="218ee-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="218ee-298">หน้าการเบิกสินค้าของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะแสดงสถานที่เบิกสินค้า (*RECV*) ป้ายทะเบียนเป้าหมาย (*ป้ายทะเบียน*) สินค้า (*A0001*) และปริมาณ (*3*)</span><span class="sxs-lookup"><span data-stu-id="218ee-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="218ee-299">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-299">Select **OK**.</span></span>
1. <span data-ttu-id="218ee-300">ในฟิลด์ **LP เป้าหมาย** ให้ป้อนป้ายทะเบียนเป้าหมายสำหรับรหัสป้ายทะเบียนที่ควรจะวาง (ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า) ไปยังสถานที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="218ee-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="218ee-301">คุณสามารถเลือกรหัสป้ายทะเบียนใดๆ ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="218ee-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="218ee-302">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-302">Select **OK**.</span></span>
1. <span data-ttu-id="218ee-303">บนหน้าถัดไป ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="218ee-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="218ee-304">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-304">Select **OK**.</span></span>
1. <span data-ttu-id="218ee-305">ยืนยันงานสำหรับการเบิกปริมาณ 2 ที่เหลือ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="218ee-306">บนหน้าถัดไป ให้เลือก **เสร็จสิ้น** เพื่อจบกระบวนการเบิกสินค้าและเริ่มกระบวนการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="218ee-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="218ee-307">แอปบนอุปกรณ์เคลื่อนที่จะนำเสนอที่ตั้งและป้ายทะเบียนที่จะนำสินค้าไปวาง</span><span class="sxs-lookup"><span data-stu-id="218ee-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="218ee-308">ยืนยันการจัดเก็บจำนวนมากของ **การวาง** โดยการเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="218ee-309">บนหน้าถัดไปให้ยืนยัน **การวาง** การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าโดยเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="218ee-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="218ee-310">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="218ee-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="218ee-311">เลือก **ยกเลิก** เพื่อออก</span><span class="sxs-lookup"><span data-stu-id="218ee-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="218ee-312">ภาพประกอบต่อไปนี้แสดงวิธีการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เสร็จสมบูรณ์ที่อาจปรากฏใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="218ee-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="218ee-313">![การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว](media/PlannedCrossDockingWork.png "การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว")</span><span class="sxs-lookup"><span data-stu-id="218ee-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]