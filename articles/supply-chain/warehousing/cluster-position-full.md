---
title: ตำแหน่งคลัสเตอร์เต็ม
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับคุณลักษณะตำแหน่งคลัสเตอร์เต็ม คุณลักษณะนี้นำเสนอทางเลือกสำหรับการบังคับใช้กฎการแบ่งงานที่เข้มงวดยิ่งขึ้นเมื่อมีการใช้การเบิกสินค้าคลัสเตอร์ เนื่องจากจะช่วยให้มีระยะเผื่อใหญ่ขึ้นสำหรับข้อผิดพลาดในข้อจำกัดตามปริมาตรของคอนเทนเเนอร์หรือโหลดบรรทุก
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c90380cb5d109e331a2552ba779525b66d10fa6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001110"
---
# <a name="cluster-position-full"></a><span data-ttu-id="a7f78-104">ตำแหน่งคลัสเตอร์เต็ม</span><span class="sxs-lookup"><span data-stu-id="a7f78-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7f78-105">คุณลักษณะ *ตำแหน่งคลัสเตอร์เต็ม* นำเสนอทางเลือกสำหรับการบังคับใช้กฎการแบ่งงานที่เข้มงวดยิ่งขึ้นเมื่อมีการใช้การเบิกสินค้าคลัสเตอร์ เนื่องจากจะช่วยให้มีระยะเผื่อใหญ่ขึ้นสำหรับข้อผิดพลาดในข้อจำกัดตามปริมาตรของคอนเทนเเนอร์หรือโหลดบรรทุก</span><span class="sxs-lookup"><span data-stu-id="a7f78-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="a7f78-106">ในสถานการณ์ทั่วไป สินค้าทั้งหมดในใบสั่งงานไม่พอดีกับคอนเทนเนอร์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a7f78-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="a7f78-107">ผู้ปฏิบัติงานคลังสินค้าที่มีการเบิกสินค้าคลัสเตอร์มีหลายตัวเลือกในสถานการณ์นี้: ต้องเปลี่ยนเป็นขนาดคอนเทนเนอร์ที่ใหญ่ขึ้นหรือทำงานกับหัวหน้างานของตนเองเพื่อให้หาทางแก้ไขอื่น</span><span class="sxs-lookup"><span data-stu-id="a7f78-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="a7f78-108">คุณลักษณะนี้จะให้คำแนะนำเกี่ยวกับความสามารถในการเรียกใช้ปุ่ม **แบบเต็ม** กับหนึ่งในหน่วยงานในคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a7f78-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="a7f78-109">ในรุ่นที่เก่ากว่า ตัวเลือกนี้จะพร้อมใช้งานสำหรับการเบิกสินค้าตามใบสั่งปกติไม่ใช่สำหรับการเบิกสินค้าคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a7f78-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="a7f78-110">อย่างไรก็ตาม คุณลักษณะนี้จะแตกต่างจากปุ่ม **แบบเต็ม** มาตรฐานในการยกเลิกงานที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="a7f78-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="a7f78-111">ไม่แนะนำให้ผู้ใช้เพิ่มช่องเก็บอื่นลงในคลัสเตอร์เดียวกันและไม่สร้างงานใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7f78-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="a7f78-112">เปิดคุณลักษณะตำแหน่งคลัสเตอร์เต็ม</span><span class="sxs-lookup"><span data-stu-id="a7f78-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="a7f78-113">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="a7f78-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a7f78-114">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a7f78-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="a7f78-115">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a7f78-116">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="a7f78-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a7f78-117">**ชื่อคุณลักษณะ:** *ตำแหน่งคลัสเตอร์เต็ม*</span><span class="sxs-lookup"><span data-stu-id="a7f78-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="a7f78-118">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="a7f78-118">Setup</span></span>

<span data-ttu-id="a7f78-119">ส่วนนี้จะให้แนวทางและตัวอย่างที่แสดงวิธีการตั้งค่าและใช้คุณลักษณะ *ตำแหน่งคลัสเตอร์เต็ม*</span><span class="sxs-lookup"><span data-stu-id="a7f78-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a7f78-120">ทำให้ข้อมูลตัวอย่างพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a7f78-120">Make sample data available</span></span>

<span data-ttu-id="a7f78-121">เมื่อต้องการดำเนินการ [สถานการณ์ตัวอย่าง](#example-scenario) โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="a7f78-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a7f78-122">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="a7f78-123">นอกจากนี้ คุณยังสามารถใช้สถานการณ์ตัวอย่างนี้เป็นคำแนะนำสำหรับการทำงานกับคุณลักษณะนี้ในระบบการทำงานจริง</span><span class="sxs-lookup"><span data-stu-id="a7f78-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="a7f78-124">อย่างไรก็ตาม ในกรณีดังกล่าว คุณต้องแทนที่ค่าของคุณเองสำหรับการตั้งค่าที่อธิบายไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="a7f78-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="a7f78-125">โพรไฟล์ของคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a7f78-125">Cluster profiles</span></span>

<span data-ttu-id="a7f78-126">คุณต้องระบุว่าจะมีการสร้างรหัสคลัสเตอร์โดยอัตโนมัติหรือไม่ มีการใช้กี่ตำแหน่ง คลัสเตอร์เสียหายเมื่อใด และการจัดลำดับและตรวจสอบงานการเบิกสินค้าเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="a7f78-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="a7f78-127">ไปที่ **การบริหารคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> โพรไฟล์ของคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a7f78-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="a7f78-128">ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ด **สร้างคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a7f78-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="a7f78-129">บนแท็บด่วน **ทั่วไป** ให้ตรวจสอบค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="a7f78-130">**สร้างรหัสคลัสเตอร์:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="a7f78-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="a7f78-131">**เรียกใช้ตำแหน่ง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="a7f78-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="a7f78-132">**จำนวนของตำแหน่ง:** *2*</span><span class="sxs-lookup"><span data-stu-id="a7f78-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="a7f78-133">**ชื่อตำแหน่ง:** *หมายเลข*</span><span class="sxs-lookup"><span data-stu-id="a7f78-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="a7f78-134">**แบ่งคลัสเตอร์ที่::** *วาง*</span><span class="sxs-lookup"><span data-stu-id="a7f78-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="a7f78-135">**ชนิดการยืนยันการเรียงลำดับ:** *การสแกนตำแหน่ง*</span><span class="sxs-lookup"><span data-stu-id="a7f78-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="a7f78-136">ในแท็บด่วน **การเรียงลำดับคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a7f78-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="a7f78-137">ตารางควรจะว่างเปล่า (นั่นคือไม่ควรมีรายการ)</span><span class="sxs-lookup"><span data-stu-id="a7f78-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="a7f78-138">เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="a7f78-138">Work templates</span></span>

<span data-ttu-id="a7f78-139">คุณต้องกำหนดวิธีการสร้างงานการเบิกสินค้าสำหรับการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a7f78-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="a7f78-140">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="a7f78-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a7f78-141">ที่ด้านบนของหน้า ให้ตั้งค่าฟิลด์ **ชนิดของใบสั่งงาน** เป็น *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="a7f78-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="a7f78-142">ตรวจสอบให้แน่ใจว่ามีการแสดงรายการเท็มเพลตงานต่อไปนี้จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a7f78-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="a7f78-143">ถ้าไม่มี คุณจะไม่สามารถทำสถานการณ์นี้ให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="a7f78-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="a7f78-144">ลำดับขั้น 61 SO</span><span class="sxs-lookup"><span data-stu-id="a7f78-144">61 SO Stage</span></span>
    - <span data-ttu-id="a7f78-145">การเบิกสินค้าคลัสเตอร์ 61 SO</span><span class="sxs-lookup"><span data-stu-id="a7f78-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="a7f78-146">คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="a7f78-146">Location directives</span></span>

<span data-ttu-id="a7f78-147">คุณต้องระบุตำแหน่งที่มีการเบิกสินค้าและจัดเก็บสินค้าไว้</span><span class="sxs-lookup"><span data-stu-id="a7f78-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="a7f78-148">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="a7f78-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a7f78-149">ในส่วนหัวรายการ ให้ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="a7f78-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="a7f78-150">ตรวจสอบให้แน่ใจว่ามีการแสดงคำสั่งใบสั่งขายต่อไปนี้จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a7f78-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="a7f78-151">ถ้าไม่มี คุณจะไม่สามารถทำสถานการณ์นี้ให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="a7f78-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="a7f78-152">การเบิกสินค้าคลัสเตอร์ 61</span><span class="sxs-lookup"><span data-stu-id="a7f78-152">61 Cluster pick</span></span>
    - <span data-ttu-id="a7f78-153">ใบสั่งเบิกสินค้า 61 SO</span><span class="sxs-lookup"><span data-stu-id="a7f78-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a7f78-154">รายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="a7f78-154">Mobile device menu items</span></span>

<span data-ttu-id="a7f78-155">คุณต้องตั้งค่าคอนฟิกรายการเมนูอุปกรณ์เคลื่อนที่เพื่อใช้งานที่มีอยู่ที่กำกับโดยการเลือกคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="a7f78-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="a7f78-156">ในรายการเมนูของอุปกรณ์เคลื่อนที่สำหรับการเบิกสินค้าคลัสเตอร์ ต้องมีการเปิดใช้งานพารามิเตอร์ **อนุญาตการแบ่งงาน** และต้องเพิ่มคลาสงาน *การเบิกสินค้า SO*</span><span class="sxs-lookup"><span data-stu-id="a7f78-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="a7f78-157">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="a7f78-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a7f78-158">ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ด **การสร้างการเบิกสินค้าคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a7f78-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="a7f78-159">เลือก **แก้ไข** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a7f78-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="a7f78-160">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a7f78-161">**สั่งการโดย:** *การเบิกสินค้าคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="a7f78-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="a7f78-162">**สร้างป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="a7f78-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="a7f78-163">**อนุญาตการแบ่งงาน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="a7f78-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="a7f78-164">**รหัสโพรไฟล์ของคลัสเตอร์:** *สร้างคลัสเตอร์*</span><span class="sxs-lookup"><span data-stu-id="a7f78-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="a7f78-165">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a7f78-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="a7f78-166">บนแท็บด่วน **คลาสงาน** ให้เพิ่มสองรายการต่อไปนี้ ตามต้องการ:</span><span class="sxs-lookup"><span data-stu-id="a7f78-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="a7f78-167">รายการ 1 (โดยทั่วไปจะแสดงในข้อมูลสาธิต):</span><span class="sxs-lookup"><span data-stu-id="a7f78-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="a7f78-168">**รหัสคลาสงาน:** *การขาย*</span><span class="sxs-lookup"><span data-stu-id="a7f78-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="a7f78-169">**ชนิดของใบสั่งงาน:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="a7f78-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="a7f78-170">รายการ 2 (อาจไม่แสดงในข้อมูลสาธิต):</span><span class="sxs-lookup"><span data-stu-id="a7f78-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="a7f78-171">**รหัสคลาสงาน:** *การเบิกสินค้า SO*</span><span class="sxs-lookup"><span data-stu-id="a7f78-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="a7f78-172">**ชนิดของใบสั่งงาน:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="a7f78-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="a7f78-173">ไปที่ **การตั้งค่าการยืนยันงาน** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a7f78-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="a7f78-174">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a7f78-174">Select **Edit**.</span></span>
1. <span data-ttu-id="a7f78-175">ป้อนค่าต่อไปนี้ลงในรายการในตาราง</span><span class="sxs-lookup"><span data-stu-id="a7f78-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="a7f78-176">**ชนิดงาน** - *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="a7f78-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="a7f78-177">**การยืนยันผลิตภัณฑ์** - *เลือกกล่องกาเครื่องหมาย*</span><span class="sxs-lookup"><span data-stu-id="a7f78-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="a7f78-178">เลือก **บันทึก** ในบานหน้าต่างการดำเนินการและปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="a7f78-179">สร้างงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-179">Create picking work</span></span>

<span data-ttu-id="a7f78-180">ก่อนที่คุณจะสามารถเริ่มต้นการเบิกสินค้าคลัสเตอร์ คุณต้องสร้างงานขาออกบางส่วน</span><span class="sxs-lookup"><span data-stu-id="a7f78-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="a7f78-181">โพรไฟล์คลัสเตอร์ที่คุณสร้างไว้ก่อนหน้านี้จะระบุตำแหน่งของคลัสเตอร์สองตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="a7f78-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="a7f78-182">ดังนั้น ต้องสร้างรหัสงานอย่างน้อยสองรหัสสำหรับการเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a7f78-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="a7f78-183">สำหรับสถานการณ์นี้ ธุรกรรมจะเกิดขึ้นในคลังสินค้า *61* และจะมีการใช้รายการ *L0101* และ *T0100*</span><span class="sxs-lookup"><span data-stu-id="a7f78-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="a7f78-184">ข้อมูลสาธิตควรมีปริมาณสินค้าคงคลังคงเหลือเพียงพอสำหรับสินค้าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a7f78-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="a7f78-185">ตรวจสอบให้แน่ใจว่าคุณมีสินค้าคงคลังเพียงพอสำหรับการทำธุรกรรมให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a7f78-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="a7f78-186">สร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="a7f78-186">Create sales order 1</span></span>

1. <span data-ttu-id="a7f78-187">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a7f78-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a7f78-188">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="a7f78-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="a7f78-189">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a7f78-190">**บัญชีลูกค้า:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="a7f78-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="a7f78-191">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="a7f78-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a7f78-192">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a7f78-192">Select **OK**.</span></span>
1. <span data-ttu-id="a7f78-193">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="a7f78-193">The new sales order is opened.</span></span> <span data-ttu-id="a7f78-194">บนกริดแท็บด่วน **บรรทัดใบสั่งขาย** ให้เพิ่มบรรทัดที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="a7f78-195">**หมายเลขสินค้า:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="a7f78-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="a7f78-196">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="a7f78-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="a7f78-197">บนแท็บด่วน **รายละเอียดรายการ** บนแท็บ **การนำส่ง** ตั้งค่าฟิลด์ **วันที่จัดส่งที่ยืนยัน** เป็นวันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="a7f78-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f78-198">บนแท็บด่วน **รายการใบสั่งขาย** ให้เพิ่มบรรทัดที่สองที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="a7f78-199">**หมายเลขสินค้า:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a7f78-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="a7f78-200">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="a7f78-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a7f78-201">บนแท็บด่วน **รายละเอียดรายการ** บนแท็บ **การนำส่ง** ตั้งค่าฟิลด์ **วันที่จัดส่งที่ยืนยัน** เป็นวันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="a7f78-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f78-202">สำหรับแต่ละรายการที่คุณเพิ่งเพิ่ม ให้ทำตามขั้นตอนต่อไปนี้ในการจองสินค้าคงคลัง:</span><span class="sxs-lookup"><span data-stu-id="a7f78-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="a7f78-203">เลือกรายการที่จะสำรอง</span><span class="sxs-lookup"><span data-stu-id="a7f78-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="a7f78-204">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **สินค้าคงคลัง \> การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a7f78-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="a7f78-205">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a7f78-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="a7f78-206">ปิดหน้า **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a7f78-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="a7f78-207">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a7f78-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a7f78-208">เมื่อการนำออกใช้เสร็จสมบูรณ์ คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการบรรทุกที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="a7f78-209">สร้างใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="a7f78-209">Create sales order 2</span></span>

1. <span data-ttu-id="a7f78-210">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a7f78-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a7f78-211">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="a7f78-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="a7f78-212">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a7f78-213">**บัญชีลูกค้า:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="a7f78-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="a7f78-214">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="a7f78-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a7f78-215">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a7f78-215">Select **OK**.</span></span>
1. <span data-ttu-id="a7f78-216">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="a7f78-216">The new sales order is opened.</span></span> <span data-ttu-id="a7f78-217">บนกริดแท็บด่วน **บรรทัดใบสั่งขาย** ให้เพิ่มบรรทัดที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="a7f78-218">**หมายเลขสินค้า:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a7f78-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="a7f78-219">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="a7f78-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a7f78-220">บนแท็บด่วน **รายละเอียดรายการ** บนแท็บ **การนำส่ง** ตั้งค่าฟิลด์ **วันที่จัดส่งที่ยืนยัน** เป็นวันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="a7f78-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f78-221">บนแท็บด่วน **รายการใบสั่งขาย** ให้เพิ่มบรรทัดที่สองที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="a7f78-222">**หมายเลขสินค้า:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="a7f78-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="a7f78-223">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="a7f78-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a7f78-224">บนแท็บด่วน **รายละเอียดรายการ** บนแท็บ **การนำส่ง** ตั้งค่าฟิลด์ **วันที่จัดส่งที่ยืนยัน** เป็นวันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="a7f78-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a7f78-225">สำหรับแต่ละรายการที่คุณเพิ่งเพิ่ม ให้ทำตามขั้นตอนต่อไปนี้ในการจองสินค้าคงคลัง:</span><span class="sxs-lookup"><span data-stu-id="a7f78-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="a7f78-226">เลือกรายการที่จะสำรอง</span><span class="sxs-lookup"><span data-stu-id="a7f78-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="a7f78-227">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **สินค้าคงคลัง \> การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a7f78-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="a7f78-228">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a7f78-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="a7f78-229">ปิดหน้า **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a7f78-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="a7f78-230">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a7f78-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a7f78-231">เมื่อการนำออกใช้เสร็จสมบูรณ์ คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการบรรทุกที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="a7f78-232">เรียกดูรหัสงานและหมายเลขป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="a7f78-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="a7f78-233">มีการสร้างรหัสงานสองรายการ ซึ่งแต่ละรายการมีรายการการเบิกสินค้าสองรายการ</span><span class="sxs-lookup"><span data-stu-id="a7f78-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="a7f78-234">ทำตามขั้นตอนต่อไปนี้เพื่อค้นหารหัสงานและการกำหนดป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="a7f78-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="a7f78-235">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="a7f78-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a7f78-236">ในตาราง **ภาพรวม** ให้ค้นหาคอลัมน์ **หมายเลขใบสั่ง** สำหรับใบสั่งขายสองใบที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="a7f78-237">สำหรับใบสั่งขายแต่ละใบ จดบันทึกรหัสงานที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="a7f78-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="a7f78-238">เลือกแถวสำหรับใบสั่งขายแต่ละใบที่จะแสดงข้อมูลที่เกี่ยวข้องในตาราง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="a7f78-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="a7f78-239">จดบันทึกของสถานที่ที่จะเบิกสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="a7f78-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="a7f78-240">ไปยัง **การบริหารสินค้าคงคลัง \> การสอบถาม และรายงาน \> รายการปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="a7f78-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="a7f78-241">ในบานหน้าต่างการดำเนินการ เลือก **มิติ** เพื่อเปิดกล่องโต้ตอบ **การแสดงมิติ**</span><span class="sxs-lookup"><span data-stu-id="a7f78-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="a7f78-242">ตรวจสอบให้แน่ใจว่ามีการเลือกกล่องกาเครื่องหมาย **ป้ายทะเบียน**, **คลังสินค้า** และ **หมายเลขสินค้า** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a7f78-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="a7f78-243">ในบานหน้าต่าง **ตัวกรอง** ให้ตั้งค่าตัวกรองต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7f78-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="a7f78-244">**หมายเลขสินค้า** – **เป็นหนึ่งใน** - *L0101* และ *T100*</span><span class="sxs-lookup"><span data-stu-id="a7f78-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="a7f78-245">**คลังสินค้า** – **เริ่มต้นด้วย** – *61*</span><span class="sxs-lookup"><span data-stu-id="a7f78-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="a7f78-246">จดบันทึกค่า **ป้ายทะเบียน** ที่แสดง</span><span class="sxs-lookup"><span data-stu-id="a7f78-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="a7f78-247">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="a7f78-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="a7f78-248">การดำเนินการของลำดับขั้นอุปกรณ์เคลื่อนที่-การตั้งค่าการยืนยันงานสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a7f78-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="a7f78-249">ลงชื่อเข้าใช้แอปคลังสินค้าในฐานะผู้ใช้ในคลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="a7f78-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="a7f78-250">ไปที่ **ขาออก \> การสร้างการเบิกสินค้าคลัสเตอร์**</span><span class="sxs-lookup"><span data-stu-id="a7f78-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="a7f78-251">หน้า **งาน: กำหนดงานให้กับคลัสเตอร์** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="a7f78-252">ป้อนรหัสงานสำหรับใบสั่งขาย 1 เพื่อกำหนดให้กับตำแหน่งคลัสเตอร์ 1</span><span class="sxs-lookup"><span data-stu-id="a7f78-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="a7f78-253">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-254">ป้อนรหัสงานสำหรับใบสั่งขาย 2 เพื่อกำหนดให้กับตำแหน่งคลัสเตอร์ 2</span><span class="sxs-lookup"><span data-stu-id="a7f78-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="a7f78-255">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f78-256">หน้า **งาน: การสร้างการเบิกสินค้าคลัสเตอร์: เบิกสินค้า** จะปรากฏขึ้นและแสดง *สินค้า L0101 2 PL*</span><span class="sxs-lookup"><span data-stu-id="a7f78-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="a7f78-257">เนื่องจากโพรไฟล์ของคลัสเตอร์ตั้งค่าจำนวนของตำแหน่งเป็น 2 ระบบจะนำคุณไปยังการเบิกสินค้าการรวมครั้งแรกโดยอัตโนมัติ: แท่นวางสินค้าสอง (PL) สองรายการของสินค้า *L0101*</span><span class="sxs-lookup"><span data-stu-id="a7f78-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="a7f78-258">ในช่วงเวลาใดๆ ในระหว่างขั้นตอนต่อไปนี้ คุณสามารถเลือกแท็บ **รายละเอียด** เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับงาน เช่น สถานที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="a7f78-259">ตั้งค่าฟิลด์ **ITEM** เป็น *L0101*</span><span class="sxs-lookup"><span data-stu-id="a7f78-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="a7f78-260">ฟิลด์นี้จะยืนยันหมายเลขสินค้า ซึ่งจำเป็นสำหรับรายการเมนูนี้ (คุณได้ตั้งค่าคอนฟิกก่อนหน้านี้โดยการเลือก **การตั้งค่าการยืนยันงาน** จากหน้า **รายการเมนูของอุปกรณ์เคลื่อนที่** เมื่อคุณสร้างรายการเมนูนี้)</span><span class="sxs-lookup"><span data-stu-id="a7f78-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="a7f78-261">ป้อนหมายเลขป้ายทะเบียนที่สัมพันธ์กับสินค้าในที่ตั้งที่มีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="a7f78-262">คุณจะเลือกแท่นวางสินค้าสองแท่น</span><span class="sxs-lookup"><span data-stu-id="a7f78-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="a7f78-263">ตั้งค่าฟิลด์ **LP** เป็น *LP\_PICK\_01*</span><span class="sxs-lookup"><span data-stu-id="a7f78-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="a7f78-264">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f78-265">หน้า **งาน: เรียงลำดับ: การสร้างการเบิกสินค้าคลัสเตอร์** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="a7f78-266">ที่นี่คุณจะเรียงลำดับแท่นวางสินค้าที่เบิกสินค้าสองแท่นลงในตำแหน่งการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="a7f78-267">ตำแหน่งนี้อาจเป็นโหลดบรรทุกหรือคอนเทนเนอร์ที่ใช้ในการแยกสินค้าคงคลังที่เบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a7f78-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="a7f78-268">ดูรายละเอียดที่จะแสดงสำหรับสินค้า (*L0101*) และปริมาณ (*20* ea) ที่จะเรียงลำดับในตำแหน่ง 1 (สำหรับใบสั่งขาย 1)</span><span class="sxs-lookup"><span data-stu-id="a7f78-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="a7f78-269">ตั้งค่าฟิลด์ **POSITION NA** เป็น *1*</span><span class="sxs-lookup"><span data-stu-id="a7f78-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="a7f78-270">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-271">ดูรายละเอียดที่จะแสดงสำหรับสินค้า (*L0101*) และปริมาณ (*20* ea) ที่จะเรียงลำดับในตำแหน่ง 2 (สำหรับใบสั่งขาย 2)</span><span class="sxs-lookup"><span data-stu-id="a7f78-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="a7f78-272">ตั้งค่าฟิลด์ **POSITION NA** เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="a7f78-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="a7f78-273">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f78-274">หน้า **งาน: การสร้างการเบิกสินค้าคลัสเตอร์: เบิกสินค้า** จะปรากฏขึ้นและแสดง *สินค้า T0100 7 ea*</span><span class="sxs-lookup"><span data-stu-id="a7f78-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="a7f78-275">ในสถานการณ์นี้ ตำแหน่ง 1 ไม่สามารถยอมรับปริมาณทั้งหมดของสินค้าที่ต้องมีการเบิกเพื่อดำเนินการตามใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="a7f78-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="a7f78-276">ตำแหน่งต้องมีการทำเครื่องหมายเป็นแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="a7f78-276">A position must be marked as full.</span></span> <span data-ttu-id="a7f78-277">ในสถานการณ์นี้ คุณจะทำการเบิกสินค้าบางส่วนของสินค้ารายการที่สอง</span><span class="sxs-lookup"><span data-stu-id="a7f78-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="a7f78-278">สินค้ารายการที่สองจะถูกเบิกบางส่วนสำหรับตำแหน่ง 1 และจะมีการสร้างงานใหม่เพื่อเบิกปริมาณที่เหลือเพื่อดำเนินการตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a7f78-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="a7f78-279">เลือกปุ่มเมนู (บางครั้งอาจเรียกว่า แฮมเบอร์เกอร์ หรือปุ่มแฮมเบอร์เกอร์) แล้วจากนั้น เลือก ยกเลิก เพื่อออกจากงาน การปรับปรุงใน **ตำแหน่งแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="a7f78-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="a7f78-280">ระบุตำแหน่งที่เป็นแบบเต็มและเลือก *1*</span><span class="sxs-lookup"><span data-stu-id="a7f78-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="a7f78-281">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-282">ป้อนปริมาณการเบิกสินค้าที่ยังคงสามารถเบิกสินค้าได้เป็นตำแหน่ง 1</span><span class="sxs-lookup"><span data-stu-id="a7f78-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="a7f78-283">ระบบสามารถกำหนดหมายเลขสินค้าที่จะมีการเบิก</span><span class="sxs-lookup"><span data-stu-id="a7f78-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="a7f78-284">ป้อน *2*</span><span class="sxs-lookup"><span data-stu-id="a7f78-284">Enter *2*.</span></span>
1. <span data-ttu-id="a7f78-285">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-286">ยืนยันหมายเลขสินค้าเพื่อทำการเบิกสินค้าที่เหลือให้เสร็จสมบูรณ์ในตำแหน่ง 2</span><span class="sxs-lookup"><span data-stu-id="a7f78-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="a7f78-287">ตั้งค่าฟิลด์ **ITEM** เป็น *T0100*</span><span class="sxs-lookup"><span data-stu-id="a7f78-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="a7f78-288">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-289">ป้อนป้ายทะเบียนที่จะใช้ในการเบิกสินค้าจากโดยตั้งค่าฟิลด์ **LP** เป็น *LPREPL04*</span><span class="sxs-lookup"><span data-stu-id="a7f78-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="a7f78-290">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-291">ดูรายละเอียดที่จะแสดงสำหรับสินค้า (*T0100*) และปริมาณ (*2* ea) ที่จะเรียงลำดับในตำแหน่ง 2 (สำหรับใบสั่งขาย 2)</span><span class="sxs-lookup"><span data-stu-id="a7f78-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="a7f78-292">ตั้งค่าฟิลด์ **POSITION NA** เป็น *2*</span><span class="sxs-lookup"><span data-stu-id="a7f78-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="a7f78-293">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a7f78-294">ดูรายละเอียดที่จะแสดงสำหรับสินค้า (*T0100*) และปริมาณ (*2* ea) ที่จะเรียงลำดับในตำแหน่ง 1 (สำหรับใบสั่งขาย 1)</span><span class="sxs-lookup"><span data-stu-id="a7f78-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="a7f78-295">ตั้งค่าฟิลด์ **POSITION NA** เป็น *1*</span><span class="sxs-lookup"><span data-stu-id="a7f78-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="a7f78-296">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f78-297">หน้า **งาน: การสร้างการเบิกสินค้าคลัสเตอร์: เก็บ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a7f78-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="a7f78-298">ในสถานการณ์นี้ การเบิกสินค้าคลัสเตอร์เสร็จสมบูรณ์แล้ว และผู้ใช้จะได้รับการแนะนำให้จัดเก็บสินค้าที่เบิกจากตำแหน่ง 1 และตำแหน่ง 2 ลงในที่ตั้งสำหรับการจัดเตรียม *STAGE01*</span><span class="sxs-lookup"><span data-stu-id="a7f78-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="a7f78-299">ดูข้อมูลที่ในหน้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-299">Review the information on the page.</span></span> <span data-ttu-id="a7f78-300">ซึ่งแสดงให้เห็นว่าปริมาณรวม *44* จะเก็บอยู่ในสถานที่การจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="a7f78-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="a7f78-301">เลือก **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="a7f78-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a7f78-302">คุณได้รับข้อความ "คลัสเตอร์เสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="a7f78-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="a7f78-303">ตอนนี้คุณสามารถใช้รายการเมนู **การเบิกสินค้าขาย** เพื่อเบิกสินค้าปริมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="a7f78-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="a7f78-304">จากนั้นคุณสามารถใช้รายการเมนู **การบรรทุกสินค้าขาย** เพื่อย้ายสินค้าจากสถานที่การจัดเตรียมไปยังท่าการบรรทุกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a7f78-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
