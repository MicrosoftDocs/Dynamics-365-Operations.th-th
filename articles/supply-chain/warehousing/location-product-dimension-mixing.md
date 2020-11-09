---
title: การผสมมิติของผลิตภัณฑ์ในสถานที่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง ฟังก์ชันของโพรไฟล์สถานที่นี้จะช่วยปรับปรุงการจัดการสถานที่เมื่อมีการใช้ผลิตภัณฑ์ย่อยหรือผลิตภัณฑ์ที่มีมิติ เช่น ในอุตสาหกรรมแฟชั่น ซึ่งช่วยให้คุณสามารถเลือกว่าจะรวมการตั้งค่าคอนฟิก สี ลักษณะ และขนาด ให้กับโพรไฟล์ที่ตั้งเฉพาะหรือไม่ หรือมีมิติหรือหนึ่งในมิติเหล่านี้เท่านั้นที่สามารถนำไปวางกับสถานที่เดียวกันได้
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017172"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="14b16-105">การผสมมิติของผลิตภัณฑ์ในสถานที่</span><span class="sxs-lookup"><span data-stu-id="14b16-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14b16-106">การผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้งคือฟังก์ชันของโพรไฟล์สถานที่ที่จะช่วยปรับปรุงการจัดการสถานที่เมื่อมีการใช้ผลิตภัณฑ์ย่อยหรือผลิตภัณฑ์ที่มีมิติ เช่น ในอุตสาหกรรมแฟชั่น</span><span class="sxs-lookup"><span data-stu-id="14b16-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="14b16-107">ซึ่งช่วยให้คุณสามารถเลือกว่าจะรวมการตั้งค่าคอนฟิก สี ลักษณะ และขนาด ให้กับโพรไฟล์ที่ตั้งเฉพาะหรือไม่ หรือมีมิติหรือหนึ่งในมิติเหล่านี้เท่านั้นที่สามารถนำไปวางกับสถานที่เดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="14b16-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="14b16-108">เปิดคุณลักษณะการผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="14b16-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="14b16-109">ก่อนที่คุณจะสามารถใช้การผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง คุณลักษณะต้องเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="14b16-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="14b16-110">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="14b16-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="14b16-111">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="14b16-112">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="14b16-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="14b16-113">**ชื่อคุณลักษณะ:** *เปิดคุณลักษณะการผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="14b16-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="14b16-114">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="14b16-114">Setup</span></span>

<span data-ttu-id="14b16-115">สถานที่ทุกแห่งในคลังสินค้าจะต้องมีโพรไฟล์สถานที่เกี่ยวข้องกัน ซึ่งอธิบายคุณสมบัติของสถานที่ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="14b16-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="14b16-116">ดังนั้นที่ตั้งทั้งหมดที่ใช้โพรไฟล์ที่ตั้งเดียวกันจะสามารถอนุญาตให้มีการผสมมิติผลิตภัณฑ์หลังจากที่ตั้งค่าไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="14b16-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="14b16-117">ตั้งค่าคอนฟิกโพรไฟล์สถานที่เพื่ออนุญาตการผสมมิติผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="14b16-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="14b16-118">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="14b16-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="14b16-119">ในรายการโพรไฟล์สถานที่ให้เลือก **จำนวนมาก**</span><span class="sxs-lookup"><span data-stu-id="14b16-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="14b16-120">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="14b16-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="14b16-121">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **เปิดใช้งานการผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="14b16-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14b16-122">คุณสามารถกำหนดตัวเลือกนี้เป็น *ใช่* เฉพาะเมื่อมีการตั้งค่าตัวเลือก **อนุญาตให้มีสินค้าผสม** เป็น *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="14b16-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="14b16-123">บนแท็บด่วน **การผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง** ให้ตั้งค่าตัวเลือก **ขนาด** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="14b16-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="14b16-124">ในสถานการณ์ที่อธิบายไว้ในหัวข้อนี้สามารถทำการผสมเฉพาะสำหรับผลิตภัณฑ์ที่มีมิติ **ขนาด** แตกต่างกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="14b16-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="14b16-125">อย่างไรก็ตาม ตัวเลือกอื่นก็พร้อมใช้งานเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="14b16-125">However, other options are also available.</span></span>
1. <span data-ttu-id="14b16-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="14b16-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="14b16-127">สร้างผลิตภัณฑ์หลักและผลิตภัณฑ์ย่อยใหม่</span><span class="sxs-lookup"><span data-stu-id="14b16-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="14b16-128">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="14b16-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="14b16-129">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="14b16-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="14b16-130">ในกล่องโต้ตอบ **ผลิตภัณฑ์ใหม่** ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="14b16-131">**ชนิดผลิตภัณฑ์:** *สินค้า*</span><span class="sxs-lookup"><span data-stu-id="14b16-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="14b16-132">**ชนิดย่อยของผลิตภัณฑ์:** *ผลิตภัณฑ์หลัก*</span><span class="sxs-lookup"><span data-stu-id="14b16-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="14b16-133">**หมายเลขของผลิตภัณฑ์:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="14b16-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="14b16-134">**ชื่อผลิตภัณฑ์:** *ขนาด B0001*</span><span class="sxs-lookup"><span data-stu-id="14b16-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="14b16-135">**กลุ่มมิติของผลิตภัณฑ์:** *ขนาด*</span><span class="sxs-lookup"><span data-stu-id="14b16-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="14b16-136">**เทคโนโลยีการตั้งค่าคอนฟิก:** *ผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า*</span><span class="sxs-lookup"><span data-stu-id="14b16-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="14b16-137">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="14b16-137">Select **OK**.</span></span>
1. <span data-ttu-id="14b16-138">บนหน้า **รายละเอียดผลิตภัณฑ์** บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="14b16-139">**สร้างผลิตภัณฑ์ย่อยโดยอัตโนมัติ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="14b16-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="14b16-140">**กลุ่มขนาด:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="14b16-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="14b16-141">ถ้าต้องการดูตัวแปรที่กำหนดไว้ล่วงหน้าในบานหน้าต่างการดำเนินการ ให้เลือก **ผลิตภัณฑ์ย่อย**</span><span class="sxs-lookup"><span data-stu-id="14b16-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="14b16-142">หน้า **ผลิตภัณฑ์ย่อย** จะปรากฏขึ้นและแสดงรายการของตัวแปรจากการตั้งค่าคอนฟิกของกลุ่มขนาด</span><span class="sxs-lookup"><span data-stu-id="14b16-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="14b16-143">นำผลิตภัณฑ์ออกใช้ที่บริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="14b16-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="14b16-144">ในบานหน้าต่างการดำเนินการ เลือก **นำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="14b16-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="14b16-145">บนหน้า **เลือกผลิตภัณฑ์ที่จะนำออกใช้** ให้ยืนยันว่าหมายเลขผลิตภัณฑ์ *B0001* อยู่ในรายการแล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="14b16-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="14b16-146">เลือก **ถัดไป** เพื่อยืนยันผลิตภัณฑ์ย่อยที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="14b16-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="14b16-147">บนหน้า **เลือกบริษัทที่จะนำไปใช้** ให้เลือก *USMF* แล้วเลือก **ถัดไป** เพื่อยืนยันการเลือก</span><span class="sxs-lookup"><span data-stu-id="14b16-147">On the **Select companies to release to** page, select *USMF* , and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="14b16-148">บนหน้า **ยืนยันการเลือก** ให้เลือก **เสร็จสิ้น** เพื่อทำการนำออกใช้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="14b16-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="14b16-149">คุณได้รับข้อความแสดงข้อความ "การดำเนินการเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="14b16-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="14b16-150">อัปเดตผลิตภัณฑ์ที่นำออกใช้ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="14b16-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="14b16-151">ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าสู่บริษัท **USMF**</span><span class="sxs-lookup"><span data-stu-id="14b16-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="14b16-152">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้** เพื่อสร้างผลิตภัณฑ์ที่นำออกใช้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="14b16-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="14b16-153">ค้นหาและเลือกหมายเลขสินค้า *B0001* เพื่อเปิดหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="14b16-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="14b16-154">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="14b16-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="14b16-155">บนแท็บด่วน **ทั่วไป** โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่าฟิลด์ **กลุ่มแบบจำลองสินค้า** เป็น *FIFO*</span><span class="sxs-lookup"><span data-stu-id="14b16-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="14b16-156">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **การตั้งค่า** ให้เลือก **กลุ่มมิติ**</span><span class="sxs-lookup"><span data-stu-id="14b16-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="14b16-157">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-157">Set the following values:</span></span>

    - <span data-ttu-id="14b16-158">**กลุ่มมิติการจัดเก็บ:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="14b16-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="14b16-159">**กลุ่มมิติการติดตาม:** *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="14b16-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="14b16-160">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="14b16-160">Select **OK**.</span></span>
1. <span data-ttu-id="14b16-161">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **การตั้งค่า** ให้เลือก **ลำดับชั้นการจอง**</span><span class="sxs-lookup"><span data-stu-id="14b16-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="14b16-162">ตั้งค่าฟิลด์ **ลำดับชั้นการจอง** เป็น *ค่าเริ่มต้น* แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="14b16-162">Set the **Reservation hierarchy** field to *Default* , and then select **OK**.</span></span>
1. <span data-ttu-id="14b16-163">บนแท็บด่วน **ทั่วไป** ในส่วน **การจัดการ** ให้สังเกตว่าการเลือกของคุณได้รับการอัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="14b16-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="14b16-164">บนแท็บด่วน **การซื้อ** ในฟิลด์ **ราคา** ให้ป้อน *10*</span><span class="sxs-lookup"><span data-stu-id="14b16-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="14b16-165">ในแท็บด่วน **จัดการต้นทุน** ในฟิลด์ **กลุ่มสินค้า** ป้อน *เสียง*</span><span class="sxs-lookup"><span data-stu-id="14b16-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="14b16-166">บนแท็บด่วน **การซื้อ** ในฟิลด์ **ราคา** ให้ป้อน *10*</span><span class="sxs-lookup"><span data-stu-id="14b16-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="14b16-167">บนแท็บด่วน **คลังสินค้า** ในฟิลด์ **รหัสกลุ่มลำดับของหน่วย** ให้ป้อน *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="14b16-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="14b16-168">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="14b16-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="14b16-169">สร้างคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="14b16-169">Create a location directive</span></span>

1. <span data-ttu-id="14b16-170">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="14b16-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="14b16-171">ในบานหน้าต่างด้านซ้าย ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="14b16-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="14b16-172">ในรายการให้เลือกคำสั่งสถานที่ที่มีชื่อ *24 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="14b16-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="14b16-173">บนแท็บด่วน **การดำเนินการของคำสั่งสถานที่** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="14b16-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="14b16-174">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="14b16-175">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="14b16-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="14b16-176">บรรทัดใหม่ควรอยู่หน้ารายการที่มีอยู่ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="14b16-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="14b16-177">เมื่อต้องการทำการเปลี่ยนแปลง ให้ใช้ปุ่ม **ย้ายขึ้น** และ **ย้ายลง** บนแถบเครื่องมือหรือเปลี่ยนค่า **หมายเลขลำดับ** ของบรรทัดที่มีอยู่เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="14b16-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="14b16-178">**ชื่อ:** *ใส่ในโพรไฟล์สถานที่จำนวนมาก*</span><span class="sxs-lookup"><span data-stu-id="14b16-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="14b16-179">**การใช้สถานที่คงที่:** *สถานที่คงที่และไม่คงที่*</span><span class="sxs-lookup"><span data-stu-id="14b16-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="14b16-180">**อนุญาตสินค้าคงคลังค่าลบ:** *ยกเลิกการเลือกกล่องกาเครื่องหมายนี้ (=ไม่)*</span><span class="sxs-lookup"><span data-stu-id="14b16-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="14b16-181">**เปิดใช้งานชุดงาน:** *ยกเลิกการเลือกกล่องกาเครื่องหมายนี้ (=ไม่)*</span><span class="sxs-lookup"><span data-stu-id="14b16-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="14b16-182">**กลยุทธ์:** *ไม่มี*</span><span class="sxs-lookup"><span data-stu-id="14b16-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="14b16-183">ในขณะที่บรรทัดใหม่ยังคงถูกเลือกอยู่ ให้เลือก **แก้ไขการสอบถาม** ด้านบนของกริด</span><span class="sxs-lookup"><span data-stu-id="14b16-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="14b16-184">ในกล่องโต้ตอบ บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="14b16-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="14b16-185">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="14b16-186">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="14b16-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="14b16-187">**ตารางที่ได้รับมา:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="14b16-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="14b16-188">**ฟิลด์:** *รหัสโพรไฟล์สถานที่*</span><span class="sxs-lookup"><span data-stu-id="14b16-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="14b16-189">**เกณฑ์:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="14b16-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="14b16-190">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="14b16-190">Select **OK**.</span></span>
1. <span data-ttu-id="14b16-191">บนหน้า **คำสั่งสถานที่** บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="14b16-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="14b16-192">ในฟิลด์ **กลยุทธ์** บนแท็บด่วน **การดำเนินการของคำสั่งสถานที่** ถ้าคุณใช้กลยุทธ์สถานที่ *การรวมบัญชี* การตั้งค่าของแท็บด่วน **การผสมมิติของผลิตภัณฑ์ที่อนุญาต** บน **โพรไฟล์สถานที่** จะถูกแทนที่และสินค้าจะถูกนำไปสถานที่เดียวกันแม้ว่าลักษณะการทำงานนี้จะไม่ได้รับอนุญาตตามการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="14b16-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="14b16-193">สร้างรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="14b16-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="14b16-194">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="14b16-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="14b16-195">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างรายการเมนูที่จะใช้สำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="14b16-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="14b16-196">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="14b16-197">**ชื่อรายการในเมนู:** *การรับรายการ PO*</span><span class="sxs-lookup"><span data-stu-id="14b16-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="14b16-198">**ชื่อเรื่อง:** *การรับรายการ PO*</span><span class="sxs-lookup"><span data-stu-id="14b16-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="14b16-199">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="14b16-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="14b16-200">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="14b16-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="14b16-201">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="14b16-202">**กระบวนการสร้างงาน:** *การรับรายการและการสำรองสินค้าของใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="14b16-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="14b16-203">**สร้างป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="14b16-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="14b16-204">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="14b16-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="14b16-205">ตั้งค่าคอนฟิกเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="14b16-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="14b16-206">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="14b16-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="14b16-207">ในรายการเมนู ให้เลือก **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="14b16-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="14b16-208">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="14b16-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="14b16-209">ในรายการ **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้ค้นหาและเลือกรายการเมนู **การรับรายการ PO**</span><span class="sxs-lookup"><span data-stu-id="14b16-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="14b16-210">เลือกปุ่มลูกศรขวาเพื่อย้ายรายการเมนู **การรับรายการ PO** ไปยังรายการ **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="14b16-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="14b16-211">ด้วยวิธีนี้คุณจะเพิ่มรายการเมนูใหม่ของคุณไปยังเมนูที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14b16-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="14b16-212">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="14b16-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="14b16-213">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="14b16-213">Scenario</span></span>

<span data-ttu-id="14b16-214">สถานการณ์จำลองนี้แสดงให้เห็นถึงความแตกต่างของผลิตภัณฑ์ย่อยสองตัวที่มีอยู่ในที่ตั้งเดียวกันเมื่อโพรไฟล์สถานที่ไม่อนุญาตให้มีสินค้าผสม แต่มีการเปิดใช้งานคุณลักษณะ *การผสมมิติผลิตภัณฑ์ของตำแหน่งที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="14b16-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="14b16-215">ในกรณีนี้คุณจะใช้ตัวแปร **ขนาด** เป็นเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="14b16-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="14b16-216">ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่ามีสถานที่ว่างเปล่าในคลังสินค้า *24* ที่ใช้โพรไฟล์สภานที่ตั้ง *จำนวนมาก*</span><span class="sxs-lookup"><span data-stu-id="14b16-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="14b16-217">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="14b16-217">Create a purchase order</span></span>

<span data-ttu-id="14b16-218">คุณจะสร้างใบสั่งซื้อที่มีสามบรรทัด ได้แก่ สองบรรทัดสำหรับหมายเลขผลิตภัณฑ์เดียวกันแต่มีผลิตภัณฑ์ย่อย **ขนาด** แตกต่างกัน และบรรทัดที่สามสำหรับผลิตภัณฑ์อื่นที่ไม่มีผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="14b16-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="14b16-219">ไปที่ **บัญชีเจ้าหนี้ \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="14b16-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="14b16-220">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="14b16-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="14b16-221">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="14b16-222">**บัญชีผู้จัดจำหน่าย:** *1001*</span><span class="sxs-lookup"><span data-stu-id="14b16-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="14b16-223">**คลังสินค้า:** *24*</span><span class="sxs-lookup"><span data-stu-id="14b16-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="14b16-224">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="14b16-224">Select **OK**.</span></span>
1. <span data-ttu-id="14b16-225">มีการสร้างใบสั่งซื้อและมีการเพิ่มบรรทัดใหม่บนแท็บด่วน **บรรทัดใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="14b16-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="14b16-226">สร้างบันทึกย่อของหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="14b16-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="14b16-227">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="14b16-228">**หมายเลขสินค้า:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="14b16-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="14b16-229">**ขนาด** *L*</span><span class="sxs-lookup"><span data-stu-id="14b16-229">**Size** *L*</span></span>
    - <span data-ttu-id="14b16-230">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="14b16-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="14b16-231">เลือก **สร้างบรรทัด** ด้านบนกริดเพื่อเพิ่มบรรทัดใบสั่งซื้อที่สอง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="14b16-232">**หมายเลขสินค้า:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="14b16-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="14b16-233">**ขนาด** *XL*</span><span class="sxs-lookup"><span data-stu-id="14b16-233">**Size** *XL*</span></span>
    - <span data-ttu-id="14b16-234">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="14b16-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="14b16-235">เลือก **สร้างรายการ** เพื่อเพิ่มรายการที่สาม และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14b16-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="14b16-236">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="14b16-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="14b16-237">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="14b16-237">**Quantity:** *1*</span></span>

<span data-ttu-id="14b16-238">1.เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="14b16-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="14b16-239">รับบรรทัดใบสั่งซื้อในแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="14b16-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="14b16-240">ลงชื่อเข้าใช้ไปยังแอปคลังสินค้าในฐานะผู้ใช้ที่สามารถใช้งานคลังสินค้า *24*</span><span class="sxs-lookup"><span data-stu-id="14b16-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="14b16-241">เลือกเมนู **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="14b16-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="14b16-242">เลือก **การรับรายการ PO**</span><span class="sxs-lookup"><span data-stu-id="14b16-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="14b16-243">เลือกฟิลด์ **PONUM** จากนั้นป้อนหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="14b16-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="14b16-244">ยืนยันการป้อนข้อมูลของคุณโดยเลือกปุ่มยืนยัน (✔) ที่ด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="14b16-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="14b16-245">ป้อนหมายเลขรายการจากใบสั่งซื้อที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="14b16-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="14b16-246">เลือกฟิลด์ **LINENUM** แล้วใช้แผ่นหมายเลขเพื่อป้อน *1*</span><span class="sxs-lookup"><span data-stu-id="14b16-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="14b16-247">ยืนยันรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="14b16-247">Confirm your entry.</span></span>
1. <span data-ttu-id="14b16-248">ป้อนปริมาณที่จะรับ</span><span class="sxs-lookup"><span data-stu-id="14b16-248">Enter the quantity to receive.</span></span> <span data-ttu-id="14b16-249">เลือกปุ่มเครื่องหมายบวก ( **+** ) สองครั้งเพื่อเพิ่มค่าในฟิลด์ **ปริมาณ** เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="14b16-249">Select the plus sign ( **+** ) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="14b16-250">ลงทะเบียนรายการของคุณโดยเลือกปุ่ม (✔) ที่ด้านล่างของหน้าแล้วยืนยันรายการของคุณโดยเลือกปุ่ม (✔) อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="14b16-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="14b16-251">ดูข้อมูลในหน้า **ใบสั่งซื้อ: ใส่**</span><span class="sxs-lookup"><span data-stu-id="14b16-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="14b16-252">หน้านี้แสดงงานที่สร้างขึ้นสำหรับการสำรองสินค้า (งาน 1)</span><span class="sxs-lookup"><span data-stu-id="14b16-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="14b16-253">สถานที่เก็บที่มีการสำรองสินค้าที่ได้รับแล้ว ป้ายทะเบียน สินค้า ขนาด และปริมาณของงาน **การรับรายการ PO** ที่คุณดำเนินการเสร็จสมบูรณ์จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="14b16-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="14b16-254">ยืนยันงานการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="14b16-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="14b16-255">ทำซ้ำขั้นตอนที่ 4 ถึง 11 สำหรับบรรทัดใบสั่งซื้อ 2</span><span class="sxs-lookup"><span data-stu-id="14b16-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="14b16-256">อย่างไรก็ตามในขั้นตอนที่ 8 ให้ระบุปริมาณ *1*</span><span class="sxs-lookup"><span data-stu-id="14b16-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="14b16-257">งานการสำรองสินค้าใหม่ (งาน 2) ถูกสร้างขึ้นสำหรับสถานที่เก็บเดียวกันกับงาน 1</span><span class="sxs-lookup"><span data-stu-id="14b16-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="14b16-258">ทำซ้ำขั้นตอนที่ 4 ถึง 11 อีกครั้งสำหรับบรรทัดใบสั่งซื้อ 2</span><span class="sxs-lookup"><span data-stu-id="14b16-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="14b16-259">ในขั้นตอนที่ 8 ให้ระบุปริมาณที่เหลือเป็น *1*</span><span class="sxs-lookup"><span data-stu-id="14b16-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="14b16-260">งานการสำรองสินค้าใหม่ (งาน 3) ถูกสร้างขึ้นสำหรับสถานที่เก็บเดียวกันกับงาน 1 และงาน 2</span><span class="sxs-lookup"><span data-stu-id="14b16-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="14b16-261">ลักษณะการทำงานนี้เกิดขึ้นเนื่องจากมีการใช้กลยุทธ์คำสั่งของสถานที่เก็บ *การรวมบัญชี* และแท็บด่วน **การผสมมิติของผลิตภัณฑ์ที่ได้รับอนุญาต** ในการตั้งค่า *จำนวนมาก* ของ **โพรไฟล์สถาน** ที่อนุญาตให้มีการรวมผลิตภัณฑ์ย่อย **ขนาด** ในสถานที่</span><span class="sxs-lookup"><span data-stu-id="14b16-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="14b16-262">ทำซ้ำขั้นตอนที่ 4 ถึง 11 สำหรับบรรทัดใบสั่งซื้อ 3</span><span class="sxs-lookup"><span data-stu-id="14b16-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="14b16-263">ในขั้นตอนที่ 8 ให้ระบุปริมาณ *1* สำหรับหมายเลขสินค้า *A0001*</span><span class="sxs-lookup"><span data-stu-id="14b16-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="14b16-264">งานการสำรองสินค้าใหม่ (งาน 4) ถูกสร้างขึ้นสำหรับสถานที่เก็บอื่นที่ไม่ใช่ที่ตั้งที่ใช้สำหรับบรรทัดใบสั่งซื้อ 1 และ 2</span><span class="sxs-lookup"><span data-stu-id="14b16-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="14b16-265">ลักษณะการทำงานนี้เกิดขึ้นเนื่องจากโพรไฟล์สถานที่ไม่อนุญาตสำหรับผลิตภัณฑ์ผสม แต่ไม่อนุญาตให้มีมิติผสมของผลิตภัณฑ์หลักเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="14b16-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="14b16-266">เลือกปุ่มเมนูที่ด้านบนของหน้า (บางครั้งอาจเรียกว่าแฮมเบอร์เกอร์หรือปุ่มแฮมเบอร์เกอร์) แล้วเลือก **ยกเลิก** เพื่อออกจาก **การรับรายการ PO**</span><span class="sxs-lookup"><span data-stu-id="14b16-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="14b16-267">คุณสามารถทำซ้ำสถานการณ์จำลองนี้ได้ แต่ครั้งนี้ให้ตั้งค่า **ขนาด** - *ไม่* ภายใต้แท็บด่วน **อนุญาตการรวมมิติของผลิตภัณฑ์** บน *จำนวนมาก* ของ **โพรไฟล์สถานที่** ดังนั้นจึงไม่สามารถผสมมิติของผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="14b16-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles** , so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="14b16-268">ในกรณีนี้เมื่อคุณได้รับใบสั่งซื้อ ผลิตภัณฑ์ย่อยแต่ละรายการจะถูกวางไปยังที่ตั้งใหม่</span><span class="sxs-lookup"><span data-stu-id="14b16-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>