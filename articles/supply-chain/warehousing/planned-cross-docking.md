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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017770"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="1a8f1-104">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="1a8f1-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a8f1-105">หัวข้อนี้จะอธิบายถึงการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="1a8f1-106">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าคือกระบวนการของคลังสินค้าซึ่งปริมาณสินค้าคงคลังที่จำเป็นสำหรับใบสั่งจะถูกส่งตรงจากการรับสินค้าหรือการสร้างไปยังท่าออกที่ถูกต้องหรือพื้นที่ที่จัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="1a8f1-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="1a8f1-107">สินค้าคงคลังที่เหลือทั้งหมดจากต้นทางขาเข้าจะถูกส่งไปยังสถานที่เก็บสินค้าที่ถูกต้องโดยผ่านกระบวนการสำรองสินค้าปกติ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="1a8f1-108">การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าช่วยให้ผู้ปฏิบัติงานข้ามการสำรองสินค้าขาเข้าและการเบิกสิค้าขาออกของสินค้าคงคลังที่มีการทำเครื่องหมายสำหรับใบสั่งขาออกอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="1a8f1-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="1a8f1-109">ดังนั้นจำนวนครั้งที่สินค้าคงคลังถูกสัมผัสจะถูกย่อให้เล็กที่สุดเท่าที่จะเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="1a8f1-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="1a8f1-110">นอกจากนี้เนื่องจากมีการโต้ตอบกับระบบน้อยลง การประหยัดเวลาและพื้นที่บนชั้นร้านค้าของคลังสินค้าจะเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a8f1-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="1a8f1-111">ก่อนที่จะสามารถรันการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าได้ ผู้ใช้ต้องตั้งค่าคอนฟิกเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าใหม่ ซึ่งจะมีการระบุแหล่งที่มาของการจัดหาวัสดุและชุดอื่นๆ ของความต้องการสำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="1a8f1-112">เมื่อสร้างใบสั่งขาออกจะต้องมีการทำเครื่องหมายรายการสำหรับใบสั่งขาเข้าที่มีสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="1a8f1-113">ในขณะรับใบสั่งขาเข้า การตั้งค่าการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะระบุความต้องการของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและสร้างงานการเคลื่อนย้ายสำหรับปริมาณที่ต้องการโดยขึ้นอยู่กับการตั้งค่าของคำสั่งสถานที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="1a8f1-114">รายการความเคลื่อนไหวของสินค้าคงคลังจะ **ไม่** ลงทะเบียนเมื่อมีการยกเลิกการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ถึงแม้ว่าจะมีการเปิดใช้การตั้งค่าสำหรับความสามารถนี้ในพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="1a8f1-115">เปิดใช้งานลักษณะการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="1a8f1-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="1a8f1-116">ก่อนที่คุณจะสามารถใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า คุณลักษณะการทำงานต้องเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="1a8f1-117">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="1a8f1-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1a8f1-118">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1a8f1-119">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1a8f1-120">**ชื่อคุณลักษณะ:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="1a8f1-121">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="1a8f1-122">สร้างวิธีการลงรายการบัญชีการบรรทุกใหม่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-122">Regenerate load posting methods</span></span>

<span data-ttu-id="1a8f1-123">การใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้ล่วงหน้าจะถูกนำมาใช้เป็นวิธีการลงรายการบัญชีการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="1a8f1-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="1a8f1-124">หลังจากที่คุณเปิดใช้งานลักษณะการทำงานแล้ว คุณต้องสร้างวิธีการใหม่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="1a8f1-125">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> วิธีการลงรายการบัญชีการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="1a8f1-126">บนบานหน้าต่างการดำเนินการ เลือก **สร้างวิธีการใหม่**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="1a8f1-127">เมื่อการดำเนินการเสร็จสมบูรณ์แล้ว คุณควรจะเห็นวิธีการที่มีค่า **ชื่อวิธีการ** *planCrossDocking*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="1a8f1-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="1a8f1-129">สร้างเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="1a8f1-130">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="1a8f1-131">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1a8f1-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="1a8f1-132">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-133">**ลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="1a8f1-134">ฟิลด์นี้จะกำหนดใบสั่งที่จะมีการประเมินเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1a8f1-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="1a8f1-135">**รหัสเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="1a8f1-136">**คำอธิบาย:** *คลังสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="1a8f1-137">**นโยบายการนำออกใช้ความต้องการ** *ก่อนใบรับการจัดหาสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="1a8f1-138">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a8f1-139">การตั้งค่าบนแท็บด่วน **การวางแผน** ควบคุมวิธีการทำงานของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1a8f1-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="1a8f1-140">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-140">Set the following values:</span></span>

    - <span data-ttu-id="1a8f1-141">**ข้อกำหนดของความต้องการ:** *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="1a8f1-142">ฟิลด์นี้จะกำหนดความต้องการของสินค้าคงคลังที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="1a8f1-143">ถ้าต้องการให้มีการเชื่อมโยงความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือก *การทำเครื่องหมาย*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="1a8f1-144">ถ้าต้องการให้มีการจองสินค้าตามความต้องการกับการจัดหาวัสดุก่อนการนำออกใช้ ให้เลือกการ *การจองสินค้าสำหรับใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="1a8f1-145">**ชนิดของการระบุตำแหน่ง:** *สถานที่จัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="1a8f1-146">ฟิลด์นี้กำหนดว่างานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าควรใช้สถานที่ที่จัดเตรียม/การบรรทุกจากการจัดส่งหรือไม่ และควรใช้คำสั่งของสถานที่ในการค้นหาสถานที่การจัดเตรียม/การบรรทุกของตนเองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="1a8f1-147">**เท็มเพลตงาน** ปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="1a8f1-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="1a8f1-148">ฟิลด์นี้จะกำหนดเท็มเพลตงานที่ควรใช้เมื่อมีการสร้างงานการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="1a8f1-149">**ตรวจสอบความถูกต้องของใบรับการจัดหาสินค้าซ้ำ:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="1a8f1-150">ตัวเลือกนี้กำหนดว่าควรตรวจสอบความถูกต้องของการจัดหาวัสดุในระหว่างการรับสินค้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="1a8f1-151">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ทั้งหน้าต่างเวลาสูงสุดและช่วงวันหมดอายุจะถูกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="1a8f1-152">**ตรวจสอบความถูกต้องของหน้าต่างเวลา:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="1a8f1-153">ตัวเลือกนี้กำหนดว่าควรประเมินหน้าต่างเวลาสูงสุดเมื่อมีการเลือกแหล่งที่มาของการจัดหาวัสดุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="1a8f1-154">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ฟิลด์ที่เกี่ยวข้องกับหน้าต่างเวลาสูงสุดและหน้าต่างเวลาต่ำสุดจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="1a8f1-155">**หน้าต่างเวลาสูงสุด:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="1a8f1-156">ฟิลด์นี้กำหนดระยะเวลาสูงสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="1a8f1-157">**หน่วยของหน้าต่างเวลาสูงสุด:** *วัน*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="1a8f1-158">**หน้าต่างเวลาต่ำสุด:** *0*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="1a8f1-159">ฟิลด์นี้กำหนดระยะเวลาต่ำสุดที่อนุญาตระหว่างการมาถึงของการจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="1a8f1-160">**หน่วยของหน้าต่างเวลาต่ำสุด:** *วัน*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="1a8f1-161">**ช่วงวันหมดอายุ:** *0*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="1a8f1-162">*เงื่อนไขที่หมดอายุแรกออกก่อน (FEFO):* ฟิลด์นี้จะกำหนดจำนวนวันสูงสุดระหว่างวันหมดอายุของชุดงานที่หมดอายุแรกที่ปัจจุบันอยู่ในคลังสินค้าและชุดงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="1a8f1-163">บนแท็บด่วน **แหล่งที่มาของการจัดหาสินค้า** คุณสามารถระบุชนิดของการจัดหาวัสดุที่มีผลบังคับใช้สำหรับเท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="1a8f1-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="1a8f1-164">เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="1a8f1-165">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1a8f1-166">**แหล่งที่มาของการจัดหาสินค้า:** *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="1a8f1-167">สร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-167">Create a work class</span></span>

1. <span data-ttu-id="1a8f1-168">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="1a8f1-169">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="1a8f1-170">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-170">Set the following values:</span></span>

    - <span data-ttu-id="1a8f1-171">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="1a8f1-172">**คำอธิบาย:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="1a8f1-173">**ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="1a8f1-174">สร้างเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-174">Create a work template</span></span>

1. <span data-ttu-id="1a8f1-175">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1a8f1-176">ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="1a8f1-177">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังแท็บ **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="1a8f1-178">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-179">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1a8f1-180">**เท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="1a8f1-181">**คำอธิบายเท็มเพลตงาน:** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="1a8f1-182">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="1a8f1-183">บนแท็บด่วน **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="1a8f1-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a8f1-184">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-185">**ชนิดงาน:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="1a8f1-186">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="1a8f1-187">เลือก **สร้าง** เพื่อเพิ่มบรรทัดอื่นและตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="1a8f1-188">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="1a8f1-189">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="1a8f1-190">เลือก **บันทึก** และยืนยันว่ามีการเลือกกล่องกาเครื่องหมาย **ที่ถูกต้อง** สำหรับเท็มเพลต *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="1a8f1-191">รหัสคลาสงานสำหรับชนิดงาน *การเบิกสินค้า* และ *การวาง* ต้องเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="1a8f1-192">สร้างคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-192">Create location directives</span></span>

1. <span data-ttu-id="1a8f1-193">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1a8f1-194">ในบานหน้าต่างด้านซ้าย ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="1a8f1-195">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="1a8f1-196">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1a8f1-197">**ชื่อ:** *การวางส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า 51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="1a8f1-198">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="1a8f1-199">**ไซต์:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-199">**Site:** *5*</span></span>
    - <span data-ttu-id="1a8f1-200">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a8f1-201">เลือก **บันทึก** เพื่อให้แท็บด่วน **รายการ** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="1a8f1-202">บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="1a8f1-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a8f1-203">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-204">**ปริมาณเริ่มต้น:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="1a8f1-205">**ปริมาณสิ้นสุด:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="1a8f1-206">เลือก **บันทึก** เพื่อให้แท็บด่วน **การดำเนินคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="1a8f1-207">บนแท็บด่วน **การดำเนินการของคำสั่งสถานที่** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="1a8f1-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a8f1-208">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-209">**ชื่อ:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="1a8f1-210">**การใช้สถานที่คงที่:** *สถานที่คงที่และไม่คงที่*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="1a8f1-211">เลือก **บันทึก** เพื่อให้ปุ่ม **แก้ไขการสอบถาม** บน **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="1a8f1-212">เลือก **แก้ไขการสอบถาม** เพื่อเปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1a8f1-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="1a8f1-213">บนแท็บ **ช่วง** ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่าคอนฟิกสองบรรทัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="1a8f1-214">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-214">Line 1:</span></span>

        - <span data-ttu-id="1a8f1-215">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="1a8f1-216">**ตารางที่ได้รับมา:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="1a8f1-217">**ฟิลด์:** *คลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="1a8f1-218">**เงื่อนไข:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="1a8f1-219">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-219">Line 2:</span></span>

        - <span data-ttu-id="1a8f1-220">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="1a8f1-221">**ตารางที่ได้รับมา:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="1a8f1-222">**ฟิลด์:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="1a8f1-223">**เงื่อนไข:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="1a8f1-224">เลือก **ตกลง** เพื่อปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1a8f1-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="1a8f1-225">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="1a8f1-226">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1a8f1-227">ในรายการเมนูในบานหน้าต่างด้านซ้าย ให้เลือก **การสำรองการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="1a8f1-228">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-228">Select **Edit**.</span></span>
1. <span data-ttu-id="1a8f1-229">บนแท็บด่วน **คลาสงาน** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="1a8f1-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a8f1-230">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-231">**รหัสคลาสงาน:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="1a8f1-232">**ชนิดของใบสั่งงาน:** *ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="1a8f1-233">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="1a8f1-234">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="1a8f1-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="1a8f1-235">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-235">Create a purchase order</span></span>

<span data-ttu-id="1a8f1-236">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งซื้อเป็นแหล่งที่มาของการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="1a8f1-237">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="1a8f1-238">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1a8f1-239">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-240">**บัญชีผู้จัดจำหน่าย:** *104*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="1a8f1-241">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a8f1-242">เลือก **ตกลง** แล้วจดบันทึกหมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="1a8f1-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="1a8f1-243">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="1a8f1-244">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-245">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1a8f1-246">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="1a8f1-247">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-247">Create a sales order</span></span>

<span data-ttu-id="1a8f1-248">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างใบสั่งขายเป็นแหล่งที่มาของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="1a8f1-249">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1a8f1-250">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1a8f1-251">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-252">**บัญชีลูกค้า:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="1a8f1-253">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a8f1-254">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-254">Select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-255">มีการเพิ่มบรรทัดใหม่ในแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1a8f1-256">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1a8f1-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a8f1-257">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1a8f1-258">**ปริมาณ:** *3*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="1a8f1-259">สร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="1a8f1-259">Create planned cross-docking</span></span>

<span data-ttu-id="1a8f1-260">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้จากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="1a8f1-261">ในหน้า **รายละเอียดใบสั่งขาย** สำหรับใบสั่งขายที่คุณเพิ่งสร้างขึ้นในบานหน้าต่างการดำเนินการบนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="1a8f1-262">การดำเนินการนำออกใช้ไปยังคลังสินค้าจะสร้างบรรทัดการจัดส่งและการบรรทุกสำหรับบรรทัดใบสั่งขายและพยายามปันส่วนสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="1a8f1-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="1a8f1-263">คุณได้รับข้อความแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a8f1-263">You receive an informational message.</span></span> <span data-ttu-id="1a8f1-264">คุณได้รับข้อความแจ้งเตือนต่อไปนี้: "ไม่มีการสร้างงานสำหรับเวฟ XXXX</span><span class="sxs-lookup"><span data-stu-id="1a8f1-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="1a8f1-265">ดูล็อกประวัติการสร้างงานสำหรับรายละเอียด "</span><span class="sxs-lookup"><span data-stu-id="1a8f1-265">See the work creation history log for details."</span></span> <span data-ttu-id="1a8f1-266">ลักษณะการทำงานนี้คาดไว้ เนื่องจากไม่มีสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="1a8f1-267">บนแท็บด่วน **รายการใบสั่งขาย** บนเมนู **คลังสินค้า** เลือก **รายละเอียดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="1a8f1-268">หน้า **รายละเอียดการจัดส่ง** จะปรากฏขึ้นและแสดงการจัดส่งที่สร้างขึ้นสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="1a8f1-269">บนแท็บด่วน **รายการการบรรทุก** โปรดสังเกตว่าฟิลด์ **ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** ถูกตั้งค่าเป็น *3*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="1a8f1-270">เนื่องจากไม่มีสินค้าคงคลังที่มีอยู่ในคลังสินค้า แต่แหล่งที่มาของการจัดหาวัสดุที่ถูกต้องจะมาถึงภายในหน้าต่างเวลาที่กำหนดไว้ในเท็มเพลตการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a8f1-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="1a8f1-271">บนแท็บด่วน **รายการการบรรทุก** ให้เลือก **การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้** เพื่อดูรายละเอียดของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a8f1-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="1a8f1-272">ประมวลผลการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="1a8f1-273">การรับใบสั่งซื้อบนแอปคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1a8f1-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="1a8f1-274">ระบบจะได้รับปริมาณ 5 จากใบสั่งซื้อไปยังสถานที่รับสินค้าและสร้างงานสองชิ้น</span><span class="sxs-lookup"><span data-stu-id="1a8f1-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="1a8f1-275">รหัสงานแรกที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า* และเชื่อมโยงกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="1a8f1-276">มีปริมาณ 3 และส่งไปยังสถานที่จัดส่งขั้นสุดท้ายเพื่อให้สามารถจัดส่งสินค้าได้ทันที</span><span class="sxs-lookup"><span data-stu-id="1a8f1-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="1a8f1-277">รหัสงานที่สองที่สร้างขึ้นมีค่า **ชนิดของใบสั่งงาน** *ใบสั่งซื้อ* และเชื่อมโยงกับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="1a8f1-278">มีปริมาณที่เหลืออยู่ของ 2 ซึ่งไม่ใช่การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและถูกส่งตรงไปยังการสำรองสินค้าไปที่การจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="1a8f1-279">ลงชื่อเข้าใช้อุปกรณ์เคลื่อนที่ในฐานะผู้ใช้ในคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="1a8f1-280">ไปที่ **ขาเข้า \> รับการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="1a8f1-281">ในฟิลด์ **PONum** ให้ป้อนหมายเลขใบสั่งซื้อของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="1a8f1-282">ในฟิลด์ **ปริมาณ** ให้ป้อน *5*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="1a8f1-283">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-283">Select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-284">บนหน้าถัดไปให้ตั้งค่าฟิลด์ **สินค้า** เป็น *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="1a8f1-285">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-285">Select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-286">บนหน้าถัดไปให้ยืนยันค่า **PONum** **สินค้า** และ **ปริมาณ** โดยเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="1a8f1-287">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="1a8f1-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="1a8f1-288">เลือก **ยกเลิก** เพื่อออก</span><span class="sxs-lookup"><span data-stu-id="1a8f1-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="1a8f1-289">สำรองสินค้าไปยังการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="1a8f1-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="1a8f1-290">ในปัจจุบันรหัสงานทั้งสองจะมีป้ายทะเบียนเป้าหมายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="1a8f1-291">เมื่อต้องการดำเนินการขั้นตอนต่อไปให้เสร็จสมบูรณ์ คุณต้องได้รับรหัสงานและรหัสป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="1a8f1-292">คุณจะได้รับข้อมูลนี้จากรายละเอียดงานสำหรับบรรทัดใบสั่งซื้อและบรรทัดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="1a8f1-293">อีกทางหนึ่งคือคุณสามารถไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน** และกรองข้อมูลสำหรับงานที่มีค่า **คลังสินค้า** เป็น *51*</span><span class="sxs-lookup"><span data-stu-id="1a8f1-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="1a8f1-294">บนอุปกรณ์เคลื่อนที่ ให้ไปที่ **ขาเข้า \> การสำรองการซื้อ** แล้วป้อนป้ายทะเบียนเป้าหมายจากงาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="1a8f1-295">ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมายจากรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="1a8f1-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="1a8f1-296">หน้าการเบิกสินค้าของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าจะแสดงสถานที่เบิกสินค้า ( *RECV* ) ป้ายทะเบียนเป้าหมาย ( *ป้ายทะเบียน* ) สินค้า ( *A0001* ) และปริมาณ ( *3* )</span><span class="sxs-lookup"><span data-stu-id="1a8f1-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="1a8f1-297">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-297">Select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-298">ในฟิลด์ **LP เป้าหมาย** ให้ป้อนป้ายทะเบียนเป้าหมายสำหรับรหัสป้ายทะเบียนที่ควรจะวาง (ส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า) ไปยังสถานที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="1a8f1-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="1a8f1-299">คุณสามารถเลือกรหัสป้ายทะเบียนใดๆ ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1a8f1-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="1a8f1-300">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-300">Select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-301">บนหน้าถัดไป ในฟิลด์ **รหัส** ให้ป้อนรหัสป้ายทะเบียนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="1a8f1-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="1a8f1-302">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-302">Select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-303">ยืนยันงานสำหรับการเบิกปริมาณ 2 ที่เหลือ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="1a8f1-304">บนหน้าถัดไป ให้เลือก **เสร็จสิ้น** เพื่อจบกระบวนการเบิกสินค้าและเริ่มกระบวนการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="1a8f1-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="1a8f1-305">แอปบนอุปกรณ์เคลื่อนที่จะนำเสนอที่ตั้งและป้ายทะเบียนที่จะนำสินค้าไปวาง</span><span class="sxs-lookup"><span data-stu-id="1a8f1-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="1a8f1-306">ยืนยันการจัดเก็บจำนวนมากของ **การวาง** โดยการเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="1a8f1-307">บนหน้าถัดไปให้ยืนยัน **การวาง** การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าโดยเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1a8f1-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="1a8f1-308">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="1a8f1-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="1a8f1-309">เลือก **ยกเลิก** เพื่อออก</span><span class="sxs-lookup"><span data-stu-id="1a8f1-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="1a8f1-310">ภาพประกอบต่อไปนี้แสดงวิธีการทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่เสร็จสมบูรณ์ที่อาจปรากฏใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1a8f1-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="1a8f1-311">![การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว](media/PlannedCrossDockingWork.png "การทำงานของการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเสร็จสมบูรณ์แล้ว")</span><span class="sxs-lookup"><span data-stu-id="1a8f1-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
