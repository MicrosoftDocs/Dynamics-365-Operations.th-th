---
title: การรวมบัญชีสินค้า - การใช้ประโยชน์สถานที่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันที่ช่วยให้ง่ายสำหรับผู้จัดการคลังสินค้าในการดูและกรองการใช้ประโยชน์สถานที่เชิงปริมาตรในคลังสินค้า ผู้จัดการสามารถเลือกสถานที่และสร้างงานการย้ายสินค้าคงคลังได้โดยตรงจากหน้าการรวมบัญชีสินค้าเพื่อรวมบัญชีสินค้า และดังนั้นจึงทำให้มีการใช้พื้นที่คลังสินค้าได้มากขึ้น
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438808"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="29016-104">การรวมบัญชีสินค้า - การใช้ประโยชน์สถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29016-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันที่ช่วยให้ง่ายสำหรับผู้จัดการคลังสินค้าในการดูและกรองการใช้ประโยชน์สถานที่เชิงปริมาตรในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="29016-106">ผู้จัดการสามารถเลือกสถานที่และสร้างงานการย้ายสินค้าคงคลังได้โดยตรงจากหน้า **การรวมบัญชีสินค้า** เพื่อรวมบัญชีสินค้า และดังนั้นจึงทำให้มีการใช้พื้นที่คลังสินค้าได้มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="29016-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="29016-107">เปิดคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="29016-107">Turn on the features</span></span>

<span data-ttu-id="29016-108">ก่อนที่คุณจะสามารถใช้คุณลักษณะที่อธิบายไว้ในหัวข้อนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="29016-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="29016-109">ผู้ดูแลระบบสามารถใช้พื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะเหล่านี้ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="29016-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="29016-110">เปิดใช้งานคุณลักษณะทั้งสองรายการต่อไปนี้ ตามลำดับที่แสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="29016-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="29016-111">(คุณลักษณะทั้งสองรายการมีไว้สำหรับโมดูล **การบริหารคลังสินค้า**)</span><span class="sxs-lookup"><span data-stu-id="29016-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="29016-112">สถานะสถานที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-112">Warehouse location status</span></span>
2. <span data-ttu-id="29016-113">การใช้ประโยชน์สถานที่รวมบัญชีสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="29016-114">สถานะสถานที่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-114">Warehouse location status</span></span>

<span data-ttu-id="29016-115">คุณลักษณะ *สถานะสถานที่คลังสินค้า* จะเพิ่มฟิลด์ใหม่สี่ฟิลด์ไปยังหน้า **สถานที่** เพื่อติดตามข้อมูลเพิ่มเติมเกี่ยวกับสถานะปัจจุบันของสถานที่:</span><span class="sxs-lookup"><span data-stu-id="29016-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="29016-116">**หมายเลขสินค้า** – สินค้าที่อยู่ในสถานที่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="29016-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="29016-117">ถ้าสถานที่มีสินค้าหลายรายการ ฟิลด์นี้จะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="29016-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="29016-118">**วันที่และเวลาของกิจกรรมล่าสุด** – การประทับเวลาของธุรกรรมคลังสินค้าล่าสุดที่ดำเนินการเทียบกับสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="29016-119">**วันที่อายุหนี้** – วันที่ที่สินค้าคงคลังในสถานที่ถูกนำเข้าไปในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="29016-120">วันที่นี้จะคำนวณตามวันที่อายุหนี้ของป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="29016-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="29016-121">แม้ว่าวันที่นี้มีความถูกต้องสำหรับสถานที่ที่มีการติดตามป้ายทะเบียน แต่อาจไม่ถูกต้องสำหรับสถานที่ที่ไม่มีการติดตามป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="29016-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="29016-122">**สถานะของสถานที่** – สถานะของสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="29016-123">ค่าสี่ค่าพร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="29016-123">Four values are available:</span></span>

    - <span data-ttu-id="29016-124">**ไม่มีการกำหนด** – โปรไฟล์สถานที่ไม่ติดตามสถานะ</span><span class="sxs-lookup"><span data-stu-id="29016-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="29016-125">ดังนั้น จึงไม่ทราบสถานะปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="29016-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="29016-126">**ว่างเปล่า** – ในขณะนี้ไม่มีสินค้าคงคลังอยู่ในสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="29016-127">**การเบิกสินค้า** – มีการดำเนินการธุรกรรมขาออกเทียบกับสถานที่ หลังจากที่เป็นรายการที่ว่างล่าสุด</span><span class="sxs-lookup"><span data-stu-id="29016-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="29016-128">**ที่จัดเก็บ** – มีการดำเนินการเฉพาะธุรกรรมขาออก เนื่องจากเป็นสถานที่ว่างเปล่าล่าสุด</span><span class="sxs-lookup"><span data-stu-id="29016-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="29016-129">ฟิลด์เหล่านี้อนุญาตให้ผู้จัดการคลังสินค้าสามารถเรียกดูภาพรวมของสถานะของสถานที่ในคลังสินค้าได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="29016-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="29016-130">นอกจากนี้ ยังอนุญาตการรายงานและการกรองข้อมูลขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="29016-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="29016-131">ตั้งค่าการรวมบัญชีสินค้าและการใช้ประโยชน์สถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="29016-132">ส่วนนี้จะอธิบายวิธีการจัดเตรียมระบบของคุณในการใช้การรวมบัญชีสินค้าและการใช้ประโยชน์สถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="29016-133">กระบวนงานใช้ค่าตัวอย่างจากข้อมูลสาธิตมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="29016-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="29016-134">ถ้าคุณวางแผนที่จะทำงานผ่านสถานการณ์จำลองตัวอย่างที่ระบุไว้ในภายหลังในหัวข้อนี้ ให้เลือกนิติบุคคล **USMF** (ซึ่งประกอบด้วยข้อมูลสาธิตมาตรฐาน) และสร้างเรกคอร์ดแต่ละรายการที่อธิบายไว้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="29016-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="29016-135">ถ้าคุณไม่ได้วางแผนที่จะทำงานผ่านสถานการณ์จำลองตัวอย่าง ค่าที่ระบุไว้ที่นี่จะถือว่าเป็นตัวอย่างของชนิดของการตั้งค่าที่คุณต้องดำเนินการให้เสร็จสมบูรณ์เพื่อใช้คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="29016-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="29016-136">ผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="29016-136">Released product</span></span>

1. <span data-ttu-id="29016-137">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="29016-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="29016-138">ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *M9201* และเปิดหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="29016-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="29016-139">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้าคงคลัง** ในกลุ่ม **คลังสินค้า** เลือก **มิติทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="29016-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="29016-140">บนหน้า **มิติทางกายภาพ** บนบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="29016-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="29016-141">มีการเพิ่มบรรทัดใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="29016-141">A new line is added to the grid.</span></span> <span data-ttu-id="29016-142">ฟิลด์ **หมายเลขสินค้า** จะถูกกำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="29016-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="29016-143">ในฟิลด์ **หน่วย** ให้เลือก *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="29016-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="29016-144">ฟิลด์ที่เหลือในบรรทัดถูกตั้งค่าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="29016-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="29016-145">เลือก **บันทึก** และปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="29016-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="29016-146">โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-146">Location profile</span></span>

1. <span data-ttu-id="29016-147">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="29016-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="29016-148">ในรายการของโพรไฟล์สถานที่ ให้เลือก **FLOOR-05**</span><span class="sxs-lookup"><span data-stu-id="29016-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="29016-149">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="29016-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="29016-150">บน FastTab **ทั่วไป** โปรดตรวจสอบให้แน่ใจว่าได้ตั้งค่าทั้งสองตัวเลือกต่อไปนี้เป็น *ใช่*:</span><span class="sxs-lookup"><span data-stu-id="29016-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="29016-151">เปิดใช้งานสินค้าในสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-151">Enable item in location</span></span>
    - <span data-ttu-id="29016-152">เปิดใช้งานสถานะสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-152">Enable location status</span></span>

1. <span data-ttu-id="29016-153">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="29016-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="29016-154">ถ้าตัวเลือก **เปิดใช้งานสินค้าในสถานที่** และ **เปิดใช้งานสถานะสถานที่** ถูกตั้งค่าไว้แล้วเป็น *ใช่* ให้ข้ามไปยังแนะนำสำหรับการตั้งค่า FastTab **มิติ** ในขั้นตอนที่10</span><span class="sxs-lookup"><span data-stu-id="29016-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="29016-155">ถ้าไม่ได้มีการตั้งค่าตัวเลือกเป็น *ใช่* ไว้แล้ว คุณต้องรันการตรวจสอบความสอดคล้องกันสำหรับโมดูล **การบริหารคลังสินค้า** หลังจากที่คุณตั้งค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="29016-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="29016-156">ในกรณีนี้ ให้ดำเนินการต่อไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="29016-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="29016-157">เมื่อต้องการรันการตรวจสอบความสอดคล้องกัน ให้ไปที่ **การจัดการระบบ \> งานประจำงวด \> ฐานข้อมูล \> การตรวจสอบความสอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="29016-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="29016-158">ในกล่องโต้ตอบ **การตรวจสอบความสอดคล้องกัน** ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29016-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="29016-159">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="29016-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="29016-160">**ตรวจสอบ/แก้ไข:** *ตรวจสอบ*</span><span class="sxs-lookup"><span data-stu-id="29016-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="29016-161">**วันที่เริ่มต้น:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="29016-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="29016-162">**การตรวจสอบความสอดคล้องกันของสถานะของสถานที่สินค้าคงคลัง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="29016-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="29016-163">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="29016-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="29016-164">เมื่อการตรวจสอบเสร็จสมบูรณ์ คุณจะได้รับข้อความ</span><span class="sxs-lookup"><span data-stu-id="29016-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="29016-165">เปิด [ศูนย์ปฏิบัติการ](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) เพื่อดูข้อความ</span><span class="sxs-lookup"><span data-stu-id="29016-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="29016-166">เลือก **รายละเอียดข้อความ** เพื่อดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="29016-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="29016-167">ถ้าข้อความสำหรับสถานะการตรวจสอบความสอดคล้องกันกล่าวว่า "พบข้อมูลสถานะของสถานที่ที่ไม่ถูกต้องสำหรับสถานที่ XXXX ในคลังสินค้า XX" คุณต้องรันการตรวจสอบความสอดคล้องกันอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="29016-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="29016-168">เวลานี้ ให้ตั้งค่าฟิลด์ **ตรวจสอบ/แก้ไข** เพื่อ *แก้ไขข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="29016-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="29016-169">ดูข้อความเพื่อให้แน่ใจว่าไม่พบข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="29016-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="29016-170">ขณะนี้คุณต้องทำการตั้งค่าโพรไฟล์สถานที่ให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="29016-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="29016-171">กลับไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่** เลือกโพรไฟล์สถานที่ **FLOOR-05** และจากนั้น บนบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="29016-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="29016-172">บน FastTab **มิติ** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29016-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="29016-173">**เปอร์เซ็นต์การใช้ปริมาตร:** *100*</span><span class="sxs-lookup"><span data-stu-id="29016-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="29016-174">**วิธีการเชิงปริมาตรที่ใช้สำหรับสถานที่สินค้าคงคลัง:** *ใช้ปริมาตรของสถานที่*</span><span class="sxs-lookup"><span data-stu-id="29016-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="29016-175">**ความสูงของสถานที่จริง:** *10*</span><span class="sxs-lookup"><span data-stu-id="29016-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="29016-176">**ความกว้างของสถานที่จริง:** *10*</span><span class="sxs-lookup"><span data-stu-id="29016-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="29016-177">**ความลึกของสถานที่จริง:** *10*</span><span class="sxs-lookup"><span data-stu-id="29016-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="29016-178">**น้ำหนักสูงสุด:** *100*</span><span class="sxs-lookup"><span data-stu-id="29016-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="29016-179">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="29016-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="29016-180">รายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="29016-180">Mobile device menu items</span></span>

1. <span data-ttu-id="29016-181">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="29016-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="29016-182">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างรายการเมนูสำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="29016-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="29016-183">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29016-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="29016-184">**ชื่อรายการในเมนู:** *ปรับปรุงใน*</span><span class="sxs-lookup"><span data-stu-id="29016-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="29016-185">**ชื่อเรื่อง:** *ปรับปรุงใน*</span><span class="sxs-lookup"><span data-stu-id="29016-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="29016-186">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="29016-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="29016-187">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="29016-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="29016-188">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29016-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="29016-189">**กระบวนการสร้างงาน:** *การปรับปรุงใน*</span><span class="sxs-lookup"><span data-stu-id="29016-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="29016-190">**ชนิดของการปรับปรุงสินค้าคงคลัง:** *ปรับปรุงใน*</span><span class="sxs-lookup"><span data-stu-id="29016-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="29016-191">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="29016-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="29016-192">เมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="29016-192">Mobile device menu</span></span>

1. <span data-ttu-id="29016-193">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="29016-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="29016-194">ในรายการของเมนู ให้เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="29016-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="29016-195">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="29016-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="29016-196">ในรายการ **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้ค้นหาและเลือกรายการเมนู **ปรับปรุงใน**</span><span class="sxs-lookup"><span data-stu-id="29016-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="29016-197">เลือกปุ่มลูกศรขวาเพื่อย้าย **ปรับปรุงใน** ไปยังรายการ **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="29016-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="29016-198">ด้วยวิธีนี้ คุณจะเพิ่มรายการเมนูใหม่ไปยังเมนูที่เลือก</span><span class="sxs-lookup"><span data-stu-id="29016-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="29016-199">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="29016-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="29016-200">ชนิดของความเคลื่อนไหว</span><span class="sxs-lookup"><span data-stu-id="29016-200">Movement types</span></span>

1. <span data-ttu-id="29016-201">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> ชนิดการเคลื่อนย้าย**</span><span class="sxs-lookup"><span data-stu-id="29016-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="29016-202">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** แล้วจากนั้น ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29016-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="29016-203">**รหัสชนิดของการเคลื่อนย้าย:** *CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="29016-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="29016-204">**คำอธิบาย:** *รวมบัญชีสถานที่*</span><span class="sxs-lookup"><span data-stu-id="29016-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="29016-205">**รหัสคลาสงาน:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="29016-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="29016-206">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="29016-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="29016-207">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="29016-207">Example scenario</span></span>

<span data-ttu-id="29016-208">สถานการณ์จำลองต่อไปนี้ใช้แอปคลังสินค้าบนอุปกรณ์เคลื่อนที่เพื่อทำ *การปรับปรุงใน* สินค้าคงคลังเป็นสถานที่สองแห่งในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="29016-209">เพิ่มสินค้าคงคลังไปยังสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-209">Add inventory to locations</span></span>

1. <span data-ttu-id="29016-210">ลงชื่อเข้าใช้อุปกรณ์เคลื่อนที่ในฐานะผู้ใช้ที่ถูกตั้งค่าสำหรับคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="29016-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="29016-211">ไปที่ **สินค้าคงคลัง \> ปรับปรุงใน**</span><span class="sxs-lookup"><span data-stu-id="29016-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="29016-212">ขณะนี้คุณจะป้อนการปรับปรุงสถานที่แรก</span><span class="sxs-lookup"><span data-stu-id="29016-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="29016-213">ในงาน **การปรับปรุงใน** ให้เลือกสถานที่ที่จะทำการปรับปรุงสินค้าคงคลังให้</span><span class="sxs-lookup"><span data-stu-id="29016-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="29016-214">ในฟิลด์ **LOC** เลือก *LP-001*</span><span class="sxs-lookup"><span data-stu-id="29016-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="29016-215">ยืนยันสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-215">Confirm the location.</span></span>
1. <span data-ttu-id="29016-216">สร้างรหัสป้ายทะเบียนสำหรับสินค้าที่จะเพิ่มลงในสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="29016-217">ในฟิลด์ **LP** ป้อน *LP00101*</span><span class="sxs-lookup"><span data-stu-id="29016-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="29016-218">ยืนยันป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="29016-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="29016-219">ป้อนสินค้าที่จะเพิ่มลงในป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="29016-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="29016-220">ในฟิลด์ **ITEM** ให้ป้อน *M9201*</span><span class="sxs-lookup"><span data-stu-id="29016-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="29016-221">ยืนยันสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-221">Confirm the item.</span></span>
1. <span data-ttu-id="29016-222">ป้อนปริมาณของสินค้าที่จะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="29016-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="29016-223">ในฟิลด์ **QTY** ให้ป้อน *10*</span><span class="sxs-lookup"><span data-stu-id="29016-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="29016-224">ยืนยันปริมาณ</span><span class="sxs-lookup"><span data-stu-id="29016-224">Confirm the quantity.</span></span>

    <span data-ttu-id="29016-225">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="29016-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="29016-226">ขณะนี้คุณจะป้อนการปรับปรุงสถานที่ที่สอง</span><span class="sxs-lookup"><span data-stu-id="29016-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="29016-227">ในงาน **การปรับปรุงใน** ให้เลือกสถานที่ที่จะทำการปรับปรุงสินค้าคงคลังให้</span><span class="sxs-lookup"><span data-stu-id="29016-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="29016-228">ในฟิลด์ **LOC** เลือก *LP-002*</span><span class="sxs-lookup"><span data-stu-id="29016-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="29016-229">ยืนยันสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-229">Confirm the location.</span></span>
1. <span data-ttu-id="29016-230">สร้างรหัสป้ายทะเบียนสำหรับสินค้าที่จะเพิ่มลงในสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="29016-231">ในฟิลด์ **LP** ป้อน *LP00201*</span><span class="sxs-lookup"><span data-stu-id="29016-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="29016-232">ยืนยันป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="29016-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="29016-233">ป้อนสินค้าที่จะเพิ่มลงในป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="29016-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="29016-234">ในฟิลด์ **ITEM** ให้ป้อน *M9201*</span><span class="sxs-lookup"><span data-stu-id="29016-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="29016-235">ยืนยันสินค้า</span><span class="sxs-lookup"><span data-stu-id="29016-235">Confirm the item.</span></span>
1. <span data-ttu-id="29016-236">ป้อนปริมาณของสินค้าที่จะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="29016-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="29016-237">ในฟิลด์ **QTY** ให้ป้อน *15*</span><span class="sxs-lookup"><span data-stu-id="29016-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="29016-238">ยืนยันปริมาณ</span><span class="sxs-lookup"><span data-stu-id="29016-238">Confirm the quantity.</span></span>

    <span data-ttu-id="29016-239">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="29016-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="29016-240">เลือกปุ่มเมนู (บางครั้งอาจเรียกว่า แฮมเบอร์เกอร์ หรือปุ่มแฮมเบอร์เกอร์) แล้วจากนั้น เลือก **ยกเลิก** เพื่อออกจากงาน **การปรับปรุงใน**</span><span class="sxs-lookup"><span data-stu-id="29016-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="29016-241">รวมบัญชีสถานที่</span><span class="sxs-lookup"><span data-stu-id="29016-241">Consolidate locations</span></span>

1. <span data-ttu-id="29016-242">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> การรวมบัญชีสินค้า**</span><span class="sxs-lookup"><span data-stu-id="29016-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="29016-243">ในส่วนหัว ให้เลือกคลังสินค้าที่จะทำการรวมบัญชีให้</span><span class="sxs-lookup"><span data-stu-id="29016-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="29016-244">ในฟิลด์ **คลังสินค้า** ให้ป้อน *51*</span><span class="sxs-lookup"><span data-stu-id="29016-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="29016-245">เรกคอร์ดจะแสดงขึ้นสำหรับสถานที่แต่ละแห่งที่ซึ่งสินค้า *M9201* ได้รับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="29016-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="29016-246">คอลัมน์ **เปอร์เซ็นต์การใช้ประโยชน์** แสดงการใช้เชิงปริมาตรของสถานที่แต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="29016-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="29016-247">เมื่อต้องการรวมบัญชีสินค้าคงคลัง ให้เลือกสถานที่ทั้งหมดที่ต้องมีการรวมบัญชี และจากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **รวมบัญชีสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="29016-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="29016-248">ในกล่องโต้ตอบ **รวมบัญชีสินค้าคงคลัง** ให้ระบุสถานที่และชนิดของการเคลื่อนย้ายที่ควรใช้เพื่อสร้างงานสำหรับการเคลื่อนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="29016-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="29016-249">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29016-249">Set the following values:</span></span>

    - <span data-ttu-id="29016-250">**สถานที่:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="29016-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="29016-251">**รหัสชนิดของการเคลื่อนย้าย:** *CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="29016-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="29016-252">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="29016-252">Select **OK**.</span></span>
1. <span data-ttu-id="29016-253">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงงานการเคลื่อนย้ายที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="29016-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="29016-254">จดบันทึกรหัสงานการเคลื่อนย้าย</span><span class="sxs-lookup"><span data-stu-id="29016-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="29016-255">ดูงานการเคลื่อนย้าย</span><span class="sxs-lookup"><span data-stu-id="29016-255">View movement work</span></span>

1. <span data-ttu-id="29016-256">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="29016-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="29016-257">ดูงานที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="29016-257">View the work that was created.</span></span> <span data-ttu-id="29016-258">ใช้รหัสงานการเคลื่อนย้ายจากการรวมบัญชีสินค้าคงคลัง เพื่อกรองข้อมูลหรือค้นหากริดงาน</span><span class="sxs-lookup"><span data-stu-id="29016-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="29016-259">ในสถานการณ์สมมตินี้ สถานที่ที่มีอยู่ที่มีสินค้าคงคลังถูกใช้เป็นสถานที่ของการรวมบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="29016-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="29016-260">ดังนั้น จึงมีการสร้างรหัสงานหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="29016-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="29016-261">ระบบจะสร้างรหัสงานหนึ่งรหัสสำหรับการย้ายแต่ละครั้งที่ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="29016-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="29016-262">ถ้าคุณระบุสถานที่เก็บที่มีสินค้าคงคลังอยู่แล้ว จะมีการสร้างรหัสงานหนึ่งรหัสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="29016-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="29016-263">ถ้าคุณระบุสถานที่ใหม่ จะมีการสร้างรหัสงานสองรหัส</span><span class="sxs-lookup"><span data-stu-id="29016-263">If you specify a new location, two work IDs are created.</span></span>
