---
title: การกำหนดตำแหน่งป้ายทะเบียนตามสถานที่
description: การกำหนดสถานที่ของป้ายทะเบียนจะช่วยให้คุณสามารถดูได้ว่าป้ายทะเบียนอยู่ในแท่นวางสินค้าหลายแห่ง เช่น สถานที่ที่ใช้ชั้นเก็บสินค้าของแท่นวางสินค้าที่มีความลึกเป็นสองเท่า
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017133"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="d0f46-103">การกำหนดตำแหน่งป้ายทะเบียนตามสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0f46-104">การกำหนดสถานที่ของป้ายทะเบียนจะช่วยให้คุณสามารถดูได้ว่าป้ายทะเบียนอยู่ในแท่นวางสินค้าหลายแห่ง เช่น สถานที่ที่ใช้ชั้นเก็บสินค้าของแท่นวางสินค้าที่มีความลึกเป็นสองเท่า</span><span class="sxs-lookup"><span data-stu-id="d0f46-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="d0f46-105">คุณลักษณะจะเพิ่มหมายเลขลำดับให้กับป้ายทะเบียนแต่ละป้ายที่วางลงในสถานที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d0f46-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="d0f46-106">หมายเลขลำดับนี้จะใช้เพื่อสั่งป้ายทะเบียนในสถานที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d0f46-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="d0f46-107">คุณลักษณะที่สนับสนุนอย่างชาญฉลาดจึงสนับสนุนสถานการณ์ที่ลูกค้าใช้ระบบชั้นเก็บสินค้าแรงโน้มถ่วงและที่ต้องรู้ เพื่อวัตถุประสงค์ในการเบิกสินค้าซึ่งเป็นป้ายทะเบียนที่หันหน้าเข้า</span><span class="sxs-lookup"><span data-stu-id="d0f46-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="d0f46-108">หัวข้อนี้แสดงสถานการณ์จำลองที่แสดงวิธีการตั้งค่าและใช้คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d0f46-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="d0f46-109">เปิดคุณลักษณะการกำหนดตำแหน่งป้ายทะเบียนสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="d0f46-110">ก่อนที่คุณจะสามารถใช้การกำหนดสถานที่ของป้ายทะเบียน คุณลักษณะต้องเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="d0f46-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="d0f46-111">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d0f46-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d0f46-112">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d0f46-113">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="d0f46-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d0f46-114">**ชื่อคุณลักษณะ:** *การกำหนดตำแหน่งป้ายทะเบียนสถานที่*</span><span class="sxs-lookup"><span data-stu-id="d0f46-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d0f46-115">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="d0f46-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="d0f46-116">ทำให้ข้อมูลตัวอย่างพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d0f46-116">Make sample data available</span></span>

<span data-ttu-id="d0f46-117">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้ค่าที่แนะนำนี้ คุณต้องทำงานในระบบที่มีการติดตั้งข้อมูลตัวอย่างมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="d0f46-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="d0f46-118">นอกจากนี้คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d0f46-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="d0f46-119">ตั้งค่าคุณลักษณะสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="d0f46-120">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อตั้งค่าคุณลักษณะ *การกำหนดตำแหน่งป้ายทะเบียนสถานที่* สำหรับสถานการณ์จำลองที่แสดงอยู่ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="d0f46-121">โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-121">Location profiles</span></span>

<span data-ttu-id="d0f46-122">คุณลักษณะต้องเปิดอยู่ในโพรไฟล์สถานที่สำหรับทุกสถานที่ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="d0f46-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="d0f46-123">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="d0f46-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="d0f46-124">ในรายการโพรไฟล์สถานที่ในบานหน้าต่างด้านซ้าย ให้เลือก **BULK-06**</span><span class="sxs-lookup"><span data-stu-id="d0f46-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="d0f46-125">บนแท็บด่วน **ทั่วไป** จะมีการเพิ่มตัวเลือกใหม่สองตัวเลือกโดยคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="d0f46-126">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-126">Set the following values:</span></span>

    - <span data-ttu-id="d0f46-127">**เปิดใช้งานตำแหน่งป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="d0f46-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="d0f46-128">เมื่อมีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ตำแหน่งป้ายทะเบียนจะถูกเก็บรักษาไว้สำหรับป้ายทะเบียนในสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-128">When this option is set to *Yes* , the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="d0f46-129">**แสดงตำแหน่งของป้ายทะเบียนอุปกรณ์เคลื่อนที่:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="d0f46-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="d0f46-130">เมื่อมีการตั้งค่าตัวเลือกนี้เป็น *ใช่* ตำแหน่งป้ายทะเบียนจะแสดงต่อผู้ใช้อุปกรณ์เคลื่อนที่ในระหว่างการปรับปรุงและการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="d0f46-130">When this option is set to *Yes* , the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="d0f46-131">คุณสามารถเปลี่ยนการตั้งค่าของตัวเลือกนี้ได้เฉพาะเมื่อเปิดใช้งานคุณลักษณะแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d0f46-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="d0f46-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d0f46-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="d0f46-133">คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-133">Location directives</span></span>

1. <span data-ttu-id="d0f46-134">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="d0f46-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d0f46-135">ในบานหน้าต่างด้านซ้าย ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="d0f46-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="d0f46-136">ในรายการของคำสั่งสถานที่ ให้เลือก **ใบสั่งเบิกสินค้า 61 SO**</span><span class="sxs-lookup"><span data-stu-id="d0f46-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="d0f46-137">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="d0f46-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d0f46-138">บนแท็บด่วน **บรรทัด** ให้เลือกบรรทัดที่มีค่า **หมายเลขลำดับ** *2*</span><span class="sxs-lookup"><span data-stu-id="d0f46-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="d0f46-139">บนแท็บด่วน **การดำเนินการคำสั่งสถานที่** ให้เลือกบรรทัดที่มีค่า **ชื่อของการ** *เบิกสินค้าน้อยกว่าแท่นวางสินค้า* (ควรเป็นบรรทัดเดียว) และเปลี่ยนค่าของ **หมายเลขลำดับ** เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="d0f46-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="d0f46-140">เลือก **สร้าง** ด้านบนกริดเพื่อเพิ่มบรรทัดสำหรับการดำเนินการคำสั่งสถานที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="d0f46-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="d0f46-141">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d0f46-142">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d0f46-143">**ชื่อ:** *ตำแหน่งการเบิกสินค้า1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="d0f46-144">ในขณะที่บรรทัดใหม่ยังคงถูกเลือกอยู่ ให้เลือก **แก้ไขการสอบถาม** ด้านบนของกริด</span><span class="sxs-lookup"><span data-stu-id="d0f46-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="d0f46-145">ในตัวแก้ไขการสอบถาม ให้เลือกแท็บ **รวม**</span><span class="sxs-lookup"><span data-stu-id="d0f46-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="d0f46-146">ขยายการรวมตาราง **สถานที่ตั้ง** เพื่อแสดงการรวมกับตาราง **มิติสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="d0f46-147">ขยายการรวมตาราง **มิติสินค้าคงคลัง** เพื่อแสดงการรวมกับตาราง **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="d0f46-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="d0f46-148">เลือก **มิติสินค้าคงคลัง** แล้วเลือก **เพิ่มการรวมตาราง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-148">Select **Inventory dimensions** , and then select **Add table join**.</span></span>
1. <span data-ttu-id="d0f46-149">ในรายการของตารางที่ปรากฏในคอลัมน์ **ความสัมพันธ์** ให้เลือก **ป้ายทะเบียน (ป้ายทะเบียน)**</span><span class="sxs-lookup"><span data-stu-id="d0f46-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="d0f46-150">เลือก **เลือก** เพื่อเพิ่ม **ป้ายทะเบียน** ในการรวมตาราง **มิติสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="d0f46-151">ในขณะที่ **ป้ายทะเบียน** ยังคงถูกเลือกอยู่ ให้เลือก **เพิ่มการรวมตาราง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="d0f46-152">ในรายการของตารางที่ปรากฏในคอลัมน์ **ความสัมพันธ์** ให้เลือก **การกำหนดตำแหน่งป้ายทะเบียนสถานที่ (ป้ายทะเบียน)**</span><span class="sxs-lookup"><span data-stu-id="d0f46-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="d0f46-153">เลือก **เลือก** เพื่อเพิ่ม **การกำหนดตำแหน่งป้ายทะเบียนสถานที่** ในการรวมตาราง **มิติสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="d0f46-154">![การรวมตาราง](media/LpTableJoin.png "การรวมตาราง")</span><span class="sxs-lookup"><span data-stu-id="d0f46-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="d0f46-155">เลือก **ตกลง** เพื่อยืนยันตารางที่รวมที่อัปเดตแล้วและปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="d0f46-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="d0f46-156">บนแท็บด่วน **การดำเนินการคำสั่งสถานที่** เลือก **แก้ไขการสอบถาม** อีกครั้งเพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="d0f46-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="d0f46-157">บนแท็บ **ช่วงระยะ** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="d0f46-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d0f46-158">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d0f46-159">**ตาราง:** *การกำหนดตำแหน่งป้ายทะเบียนสถานที่*</span><span class="sxs-lookup"><span data-stu-id="d0f46-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="d0f46-160">**ตารางที่ได้รับมา:** *การกำหนดตำแหน่งป้ายทะเบียนสถานที่*</span><span class="sxs-lookup"><span data-stu-id="d0f46-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="d0f46-161">**ฟิลด์:** *ตำแหน่งป้ายทะเบียน*</span><span class="sxs-lookup"><span data-stu-id="d0f46-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="d0f46-162">**เงื่อนไข:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="d0f46-163">![ช่วงใหม่](media/LpPositionCriteria.png "ช่วงใหม่")</span><span class="sxs-lookup"><span data-stu-id="d0f46-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="d0f46-164">เลือก **ตกลง** เพื่อยืนยันการเปลี่ยนแปลงของคุณ และปิดตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="d0f46-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="d0f46-165">ตั้งค่าข้อมูลตัวอย่างสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="d0f46-166">สำหรับสถานการณ์นี้ ผู้ใช้ต้องลงชื่อเข้าใช้ไปยังแอปอุปกรณ์เคลื่อนที่ของคลังสินค้าโดยใช้ผู้ปฏิบัติงานที่มีการตั้งค่าสำหรับคลังสินค้า *61* เพื่อดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="d0f46-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="d0f46-167">ผู้ใช้ต้องทำธุรกรรมให้เสร็จสมบูรณ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="d0f46-167">The user must also complete transactions.</span></span>

<span data-ttu-id="d0f46-168">เนื่องจากคุณลักษณะ *การกำหนดตำแหน่งป้ายทะเบียนสถานที่* เพิ่มรหัสใหม่สำหรับตำแหน่งป้ายทะเบียนในสถานที่หนึ่ง คุณต้องสร้างข้อมูลบางอย่างเพื่อสนับสนุนสถานการณ์จำลองดังกล่าวก่อน</span><span class="sxs-lookup"><span data-stu-id="d0f46-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="d0f46-169">การตรวจนับสถานที่แรกทันที</span><span class="sxs-lookup"><span data-stu-id="d0f46-169">Spot-count the first location</span></span>

1. <span data-ttu-id="d0f46-170">เปิดแอปคลังสินค้าบนอุปกรณ์เคลื่อนที่ และลงชื่อเข้าใช้คลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="d0f46-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="d0f46-171">ไปที่ **สินค้าคงคลัง \> การตรวจนับทันที**</span><span class="sxs-lookup"><span data-stu-id="d0f46-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="d0f46-172">บนหน้า **การตรวจนับทันที** ให้ตั้งค่าฟิลด์ **สถานที่ตั้ง** เป็น *01A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="d0f46-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="d0f46-173">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-173">Select **OK**.</span></span>

    <span data-ttu-id="d0f46-174">หน้าแสดงสถานที่ตั้งที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="d0f46-174">The page shows the location that you entered.</span></span> <span data-ttu-id="d0f46-175">นอกจากนี้ยังแสดงข้อความต่อไปนี้: "สถานที่เสร็จสมบูรณ์ เพิ่มป้ายทะเบียนหรือสินค้าใหม่หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="d0f46-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="d0f46-176">เลือก **รีเฟรช** เพื่อเพิ่มจำนวนในสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="d0f46-177">ในหน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** ให้เลือกฟิลด์ **สินค้า** แล้วป้อนค่า *A0001*</span><span class="sxs-lookup"><span data-stu-id="d0f46-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="d0f46-178">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-178">Select **OK**.</span></span>
1. <span data-ttu-id="d0f46-179">ใน **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** ให้เลือกฟิลด์ **ป้ายทะเบียน** แล้วป้อนค่า *LP1001* (หรือหมายเลขป้ายทะเบียนอื่นๆ ที่คุณเลือก)</span><span class="sxs-lookup"><span data-stu-id="d0f46-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="d0f46-180">หน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** แสดง **ตำแหน่งป้ายทะเบียน 1**</span><span class="sxs-lookup"><span data-stu-id="d0f46-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="d0f46-181">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-181">Select **OK**.</span></span>

    <span data-ttu-id="d0f46-182">ขณะนี้คุณต้องระบุปริมาณของสินค้าที่จะตรวจนับบนป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d0f46-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="d0f46-183">ตั้งค่าฟิลด์ **ปริมาณ** เป็น *10*</span><span class="sxs-lookup"><span data-stu-id="d0f46-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="d0f46-184">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-184">Select **OK**.</span></span>

    <span data-ttu-id="d0f46-185">หน้าแสดงสถานที่ตั้งที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="d0f46-185">The page shows the location that you entered.</span></span> <span data-ttu-id="d0f46-186">นอกจากนี้ยังแสดงข้อความต่อไปนี้: "สถานที่เสร็จสมบูรณ์ เพิ่มป้ายทะเบียนหรือสินค้าใหม่หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="d0f46-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="d0f46-187">เลือก **รีเฟรช** เพื่อเพิ่มการตรวจนับอื่นในสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="d0f46-188">ในหน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** ให้เลือกฟิลด์ **สินค้า** แล้วป้อนค่า *A0002*</span><span class="sxs-lookup"><span data-stu-id="d0f46-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="d0f46-189">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-189">Select **OK**.</span></span>
1. <span data-ttu-id="d0f46-190">ในหน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** ให้เลือกฟิลด์ **ป้ายทะเบียน** แล้วป้อนค่า *LP1002* (หรือหมายเลขป้ายทะเบียนอื่นๆ ที่คุณเลือก ซึ่งแตกต่างจากหมายเลขป้ายทะเบียนที่คุณระบุไว้ก่อนหน้านี้)</span><span class="sxs-lookup"><span data-stu-id="d0f46-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="d0f46-191">เปลี่ยนตำแหน่งป้ายทะเบียนโดยตั้งค่าฟิลด์ **ตำแหน่งป้ายทะเบียน** เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="d0f46-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="d0f46-192">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-192">Select **OK**.</span></span>
1. <span data-ttu-id="d0f46-193">ระบุปริมาณของสินค้าที่จะตรวจนับบนป้ายทะเบียนโดยการตั้งค่าฟิลด์ **ปริมาณ** เป็น *10*</span><span class="sxs-lookup"><span data-stu-id="d0f46-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="d0f46-194">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-194">Select **OK**.</span></span>

    <span data-ttu-id="d0f46-195">หน้าแสดงสถานที่ตั้งที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="d0f46-195">The page shows the location that you entered.</span></span> <span data-ttu-id="d0f46-196">นอกจากนี้ยังแสดงข้อความต่อไปนี้: "สถานที่เสร็จสมบูรณ์ เพิ่มป้ายทะเบียนหรือสินค้าใหม่หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="d0f46-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="d0f46-197">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-197">Select **OK**.</span></span>

<span data-ttu-id="d0f46-198">งานเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="d0f46-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="d0f46-199">การตรวจนับสถานที่ที่สองทันที</span><span class="sxs-lookup"><span data-stu-id="d0f46-199">Spot-count the second location</span></span>

1. <span data-ttu-id="d0f46-200">บนหน้า **การตรวจนับทันที** ให้ตั้งค่าฟิลด์ **สถานที่ตั้ง** เป็น *01A01R1S2B*</span><span class="sxs-lookup"><span data-stu-id="d0f46-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="d0f46-201">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-201">Select **OK**.</span></span>

    <span data-ttu-id="d0f46-202">หน้าแสดงสถานที่ตั้งที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="d0f46-202">The page shows the location that you entered.</span></span> <span data-ttu-id="d0f46-203">นอกจากนี้ยังแสดงข้อความต่อไปนี้: "สถานที่เสร็จสมบูรณ์ เพิ่มป้ายทะเบียนหรือสินค้าใหม่หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="d0f46-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="d0f46-204">เลือก **รีเฟรช** เพื่อเพิ่มจำนวนในสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="d0f46-205">ในหน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** ให้เลือกฟิลด์ **สินค้า** แล้วป้อนค่า *A0002*</span><span class="sxs-lookup"><span data-stu-id="d0f46-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="d0f46-206">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-206">Select **OK**.</span></span>
1. <span data-ttu-id="d0f46-207">บนหน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** ให้เลือกฟิลด์ **ป้ายทะเบียน** แล้วป้อนค่า *LP1003* (หรือหมายเลขป้ายทะเบียนอื่นๆ ที่คุณเลือก ซึ่งแตกต่างจากหมายเลขป้ายทะเบียนทั้งสองที่คุณระบุไว้ในกระบวนการก่อนหน้านี้)</span><span class="sxs-lookup"><span data-stu-id="d0f46-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="d0f46-208">หน้า **การตรวจนับตามรอบ: เพิ่มป้ายทะเบียนหรือสินค้าใหม่** แสดง **ตำแหน่งป้ายทะเบียน 1**</span><span class="sxs-lookup"><span data-stu-id="d0f46-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="d0f46-209">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-209">Select **OK**.</span></span>
1. <span data-ttu-id="d0f46-210">ระบุปริมาณของสินค้าที่จะตรวจนับบนป้ายทะเบียนโดยการตั้งค่าฟิลด์ **ปริมาณ** เป็น *10*</span><span class="sxs-lookup"><span data-stu-id="d0f46-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="d0f46-211">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-211">Select **OK**.</span></span>

    <span data-ttu-id="d0f46-212">หน้าแสดงสถานที่ตั้งที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="d0f46-212">The page shows the location that you entered.</span></span> <span data-ttu-id="d0f46-213">นอกจากนี้ยังแสดงข้อความต่อไปนี้: "สถานที่เสร็จสมบูรณ์ เพิ่มป้ายทะเบียนหรือสินค้าใหม่หรือไม่"</span><span class="sxs-lookup"><span data-stu-id="d0f46-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="d0f46-214">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-214">Select **OK**.</span></span>

<span data-ttu-id="d0f46-215">งานเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="d0f46-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="d0f46-216">รายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="d0f46-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="d0f46-217">การตรวจนับทันทีจากแอปบนมือถือสร้างงานการตรวจนับตามรอบใน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d0f46-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="d0f46-218">งานต้องการให้มีการยอมรับการตรวจนับก่อนที่จะลงรายการบัญชีไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d0f46-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="d0f46-219">ลงชื่อเข้าใช้ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d0f46-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="d0f46-220">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="d0f46-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="d0f46-221">บนแท็บ **ภาพรวม** ให้ค้นหาบรรทัดที่มีค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="d0f46-222">**ชนิดของใบสั่งงาน:** *การตรวจนับตามรอบ*</span><span class="sxs-lookup"><span data-stu-id="d0f46-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="d0f46-223">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="d0f46-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="d0f46-224">**สถานะงาน:** *ค้างอยู่รอการตรวจทาน*</span><span class="sxs-lookup"><span data-stu-id="d0f46-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="d0f46-225">มีการสร้างรหัสงานสองรหัสสำหรับบรรทัดเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="d0f46-226">ต้องยอมรับการตรวจนับสำหรับทั้งสองรหัสงานนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="d0f46-227">ในกริดให้เลือกรหัสงานแรกสำหรับชนิดของใบสั่งงาน *การตรวจนับตามรอบ*</span><span class="sxs-lookup"><span data-stu-id="d0f46-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="d0f46-228">บนบานหน้าต่างการดำเนินการในแท็บ **งาน** ในกลุ่ม **งาน** เลือก **การตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="d0f46-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="d0f46-229">แสดงสองบรรทัดสำหรับสินค้าแต่ละสินค้าและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d0f46-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="d0f46-230">ค่าในฟิลด์ **ปริมาณที่ตรวจนับ** **สถานที่** **ป้ายทะเบียน** และ **สินค้า** ควรตรงกับรายการตรวจนับที่คุณสร้างขึ้นบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-230">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="d0f46-231">ถ้าฟิลด์ใดฟิลด์หนึ่งเหล่านี้ไม่สามารถมองเห็นได้ ให้เลือก **มิติการแสดงผล** บนบานหน้าต่างการดำเนินการเพื่อเพิ่มมิติเหล่านั้นไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="d0f46-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="d0f46-232">เลือกทั้งสองบรรทัด</span><span class="sxs-lookup"><span data-stu-id="d0f46-232">Select both lines.</span></span>
1. <span data-ttu-id="d0f46-233">ในบานหน้าต่างการดำเนินการ เลือก **ยอมรับการตรวจนับ**</span><span class="sxs-lookup"><span data-stu-id="d0f46-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="d0f46-234">คุณได้รับข้อความแสดงข้อความ "การลงรายการบัญชี - สมุดรายวัน"</span><span class="sxs-lookup"><span data-stu-id="d0f46-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="d0f46-235">เลือก **รายละเอียดข้อความ** เพื่อดูหมายเลขสมุดรายวันที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d0f46-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="d0f46-236">ปิดรายละเอียดข้อความ</span><span class="sxs-lookup"><span data-stu-id="d0f46-236">Close the message details.</span></span>
1. <span data-ttu-id="d0f46-237">รีเฟรชหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="d0f46-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="d0f46-238">รหัสงานแรกถูกปิดแล้วและไม่มีการแสดงอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d0f46-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="d0f46-239">เมื่อต้องการดูงานที่ปิดแล้ว ให้เลือกกล่องกาเครื่องหมาย **ปิดการแสดง** ด้านบนกริด</span><span class="sxs-lookup"><span data-stu-id="d0f46-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="d0f46-240">ขณะนี้คุณจะยอมรับงานสำหรับป้ายทะเบียนในสถานที่ *01A01R1S2B*</span><span class="sxs-lookup"><span data-stu-id="d0f46-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="d0f46-241">ในแท็บ **ภาพรวม** ให้เลือกรหัสงานที่สองสำหรับชนิดของใบสั่งงาน *การตรวจนับตามรอบ*</span><span class="sxs-lookup"><span data-stu-id="d0f46-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="d0f46-242">บนบานหน้าต่างการดำเนินการในแท็บ **งาน** ในกลุ่ม **งาน** เลือก **การตรวจนับตามรอบ**</span><span class="sxs-lookup"><span data-stu-id="d0f46-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="d0f46-243">แสดงบรรทัดเดียวสำหรับสินค้าและป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d0f46-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="d0f46-244">ค่าในฟิลด์ **ปริมาณที่ตรวจนับ** **สถานที่** **ป้ายทะเบียน** และ **สินค้า** ควรตรงกับรายการตรวจนับที่คุณสร้างขึ้นบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-244">The values in the **Counted quantity** , **Location** , **License plate** , and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="d0f46-245">เลือกบรรทัด</span><span class="sxs-lookup"><span data-stu-id="d0f46-245">Select the line.</span></span>
1. <span data-ttu-id="d0f46-246">ในบานหน้าต่างการดำเนินการ เลือก **ยอมรับการตรวจนับ**</span><span class="sxs-lookup"><span data-stu-id="d0f46-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="d0f46-247">คุณได้รับข้อความแสดงข้อความ "การลงรายการบัญชี - สมุดรายวัน"</span><span class="sxs-lookup"><span data-stu-id="d0f46-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="d0f46-248">เลือก **รายละเอียดข้อความ** เพื่อดูหมายเลขสมุดรายวันที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d0f46-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="d0f46-249">ปิดรายละเอียดข้อความ</span><span class="sxs-lookup"><span data-stu-id="d0f46-249">Close the message details.</span></span>
1. <span data-ttu-id="d0f46-250">รีเฟรชหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="d0f46-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="d0f46-251">รหัสงานที่สองถูกปิดแล้วและไม่มีการแสดงอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d0f46-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="d0f46-252">เมื่อต้องการดูงานที่ปิดแล้ว ให้เลือกกล่องกาเครื่องหมาย **ปิดการแสดง** ด้านบนกริด</span><span class="sxs-lookup"><span data-stu-id="d0f46-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="d0f46-253">คงเหลือตามสถานที่</span><span class="sxs-lookup"><span data-stu-id="d0f46-253">On-hand by location</span></span>

1. <span data-ttu-id="d0f46-254">ไปยัง **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ปริมาณคงคลังคงเหลือโดยสถานที่**</span><span class="sxs-lookup"><span data-stu-id="d0f46-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="d0f46-255">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-255">Set the following values:</span></span>

    - <span data-ttu-id="d0f46-256">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="d0f46-256">**Site:** *6*</span></span>
    - <span data-ttu-id="d0f46-257">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="d0f46-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="d0f46-258">**รีเฟรชระหว่างสถานที่ตั้ง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="d0f46-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="d0f46-259">โปรดสังเกตว่าสถานที่ตั้ง *01A01R1S1B* มีสองป้ายทะเบียน:</span><span class="sxs-lookup"><span data-stu-id="d0f46-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="d0f46-260">**A0001** ที่ฟิลด์ **ตำแหน่งป้ายทะเบียน** ถูกตั้งค่าเป็น *1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-260">**A0001** , where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="d0f46-261">**A0002** ที่ฟิลด์ **ตำแหน่งป้ายทะเบียน** ถูกตั้งค่าเป็น *2*</span><span class="sxs-lookup"><span data-stu-id="d0f46-261">**A0002** , where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="d0f46-262">โปรดสังเกตว่าสถานที่ตั้ง *01A01R1S2B* มีหนึ่งป้ายทะเบียน:</span><span class="sxs-lookup"><span data-stu-id="d0f46-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="d0f46-263">**A0002** ที่ฟิลด์ **ตำแหน่งป้ายทะเบียน** ถูกตั้งค่าเป็น *1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-263">**A0002** , where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="d0f46-264">สถานการณ์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d0f46-264">Sales order scenario</span></span>

<span data-ttu-id="d0f46-265">หลังจากที่มีการตั้งค่าคุณลักษณะ *การกำหนดตำแหน่งป้ายทะเบียนสถานที่* และมีการจัดเตรียมสินค้าคงคลังแล้ว คุณต้องสร้างใบสั่งขายเพื่อสร้างงานการเบิกสินค้าที่จะตรงกับผู้ปฏิบัติงานของคลังสินค้าเพื่อเบิกสินค้า *A0002* จากสถานที่เก็บสินค้าคงคลังที่รหัสแท่นวางสินค้าอยู่ในตำแหน่ง *1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="d0f46-266">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d0f46-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d0f46-267">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d0f46-268">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d0f46-269">**บัญชีลูกค้า:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="d0f46-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="d0f46-270">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="d0f46-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="d0f46-271">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0f46-271">Select **OK**.</span></span>
1. <span data-ttu-id="d0f46-272">มีการเพิ่มบรรทัดใหม่ในกริดแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="d0f46-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d0f46-273">บนบรรทัดใหม่นี้ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d0f46-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="d0f46-274">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="d0f46-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="d0f46-275">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="d0f46-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="d0f46-276">บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d0f46-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d0f46-277">เลือกหน้า **การจองสินค้า** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองสินค้าคงคลังสำหรับบรรทัดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d0f46-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="d0f46-278">ปิดหน้า **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d0f46-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="d0f46-279">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d0f46-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d0f46-280">คุณได้รับข้อความที่ให้ข้อมูลที่บ่งชี้ถึงรหัสเวฟ และรหัสการจัดส่ง ที่สร้างขึ้นสำหรับใบสั่งนี้</span><span class="sxs-lookup"><span data-stu-id="d0f46-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="d0f46-281">บนแท็บด่วน **บรรทัดใบสั่งขาย** บนเมนู **คลังสินค้า** เหนือกริด เลือก **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="d0f46-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="d0f46-282">หน้า **งาน** จะปรากฏขึ้นและแสดงงานที่สร้างขึ้นสำหรับรายการขาย</span><span class="sxs-lookup"><span data-stu-id="d0f46-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="d0f46-283">จดบันทึกรหัสงานที่แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="d0f46-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="d0f46-284">สถานการณ์จำลองการเบิกสินค้าขาย</span><span class="sxs-lookup"><span data-stu-id="d0f46-284">Sales picking scenario</span></span>

1. <span data-ttu-id="d0f46-285">เปิดแอปบนอุปกรณ์เคลื่อนที่ และลงชื่อเข้าใช้คลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="d0f46-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="d0f46-286">ไปที่ **ขาออก \> เบิกสินค้าการขาย**</span><span class="sxs-lookup"><span data-stu-id="d0f46-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="d0f46-287">บนหน้า **สแกนรหัสงาน/รหัสป้ายทะเบียน** ให้เลือกฟิลด์ **รหัส** แล้วป้อนรหัสงานจากรายการขาย</span><span class="sxs-lookup"><span data-stu-id="d0f46-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="d0f46-288">โปรดสังเกตว่างานการเบิกสินค้าจะนำให้คุณเบิกสินค้า *A0002* จากสถานที่ตั้ง *01A01R1S2B*</span><span class="sxs-lookup"><span data-stu-id="d0f46-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="d0f46-289">คุณจะได้รับคำสั่งนี้เนื่องจากสินค้า *A0002* อยู่บนป้ายทะเบียนที่อยู่ในตำแหน่ง *1* ในสถานที่นั้น</span><span class="sxs-lookup"><span data-stu-id="d0f46-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="d0f46-290">![สถานที่ของตำแหน่ง 1](media/LocationLicensePlatePositioning.png "สถานที่ของตำแหน่ง 1")</span><span class="sxs-lookup"><span data-stu-id="d0f46-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="d0f46-291">ป้อนรหัสป้ายทะเบียนที่คุณสร้างไว้สำหรับสถานที่เก็บแล้วทำตามพร้อมต์เพื่อเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d0f46-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
