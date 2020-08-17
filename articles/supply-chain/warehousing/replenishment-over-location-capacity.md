---
title: การเติมสินค้าตามความจุของสถานที่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับลักษณะการทำงานการเติมสินค้าตามความจุของสถานที่ ลักษณะการทำงานนี้จะเปิดใช้งานการเติมสินค้าทั้งหมดที่จำเป็นสำหรับวันที่จะสร้าง และจัดการความพร้อมในการทำงานของการเติมสินค้า เพื่อให้แน่ใจว่าสินค้าคงคลังในสถานที่เบิกสินค้าจะไม่หมดหรือไม่เกินความจุ
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5591af5fce4eb3fc901919b98f654faa5e160c54
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652270"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="aca58-104">การเติมสินค้าตามความจุของสถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aca58-105">บางคลังสินค้าที่มีปริมาณสูงหรือพื้นที่จำกัดพื้นที่ต้องจัดส่งสินค้าปริมาณเพิ่มเติมในหนึ่งวัน เพื่อที่จะให้พอดีกับสถานที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="aca58-106">ลักษณะการทำงาน *การเติมสินค้าตามความจุของสถานที่* จะเปิดใช้งานการเติมสินค้าทั้งหมดที่จำเป็นสำหรับวันที่จะสร้าง และจัดการความพร้อมในการทำงานของการเติมสินค้า เพื่อให้แน่ใจว่าสินค้าคงคลังในสถานที่เบิกสินค้าจะไม่หมดหรือไม่เกินความจุ</span><span class="sxs-lookup"><span data-stu-id="aca58-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="aca58-107">ลักษณะการทำงานนี้เปิดให้งานการเติมสินค้าถูกสร้างมากขึ้น ซึ่งจะพอดีกับสถานที่เก็บ และจะบล็อคงานการเติมสินค้าจากการดำเนินการให้เสร็จสมบูรณ์เมื่อสถานที่เก็บเต็ม</span><span class="sxs-lookup"><span data-stu-id="aca58-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="aca58-108">เมื่อสินค้าคงคลังในสถานที่เบิกสินค้าลดลงต่ำกว่าขีดจำกัดที่จัดโครงแบบ งานการเติมสินค้ามากขึ้นจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="aca58-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="aca58-109">เปิดใช้งานลักษณะการทำงานการเติมสินค้าตามความจุของสถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="aca58-110">เมื่อต้องการทำให้คุณลักษณะนี้พร้อมใช้งาน ให้เปิดใช้งานคุณลักษณะต่อไปนี้ใน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (ในใบสั่งนี้):</span><span class="sxs-lookup"><span data-stu-id="aca58-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="aca58-111">การบล็อคงานทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="aca58-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="aca58-112">การเติมสินค้าตามความจุของสถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="aca58-113">ตั้งค่าคุณลักษณะสำหรับสถานการณ์ตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="aca58-114">ส่วนนี้ให้คำแนะนำและตัวอย่างที่แสดงวิธีการตั้งค่าลักษณะการทำงานนี้ และจัดเตรียมข้อมูลตัวอย่างสำหรับสถานการณ์จำลองตัวอย่างที่ให้ไว้ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="aca58-115">เปิดใช้งานข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="aca58-115">Enable sample data</span></span>

<span data-ttu-id="aca58-116">เมื่อต้องการดำเนินการ [สถานการณ์ตัวอย่าง](#example-scenario) โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="aca58-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="aca58-117">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="aca58-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="aca58-118">โพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-118">Location profile</span></span>

<span data-ttu-id="aca58-119">เปิดใช้งานฟังก์ชันการทำงานเติมสินค้าตามความจุบนโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="aca58-120">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> โพรไฟล์สถานที่**</span><span class="sxs-lookup"><span data-stu-id="aca58-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="aca58-121">ในบานหน้าต่างด้านซ้าย เลือก **PICK-06**</span><span class="sxs-lookup"><span data-stu-id="aca58-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="aca58-122">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="aca58-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="aca58-123">บนแท็บด่วน **การเติมสินค้า** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="aca58-124">**เกินความจุของสถานที่เก็บ:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="aca58-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="aca58-125">เมื่อเปิดใช้งาน กำลังการผลิตสูงสุดของสถานที่จะได้รับอนุญาตให้เกินงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="aca58-126">การทำเช่นนี้จะเปิดใช้งานฟิลด์อื่นๆ บนแท็บด่วน **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="aca58-127">**ชนิดขีดจำกัดของความพร้อมในการทำงาน:** *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="aca58-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="aca58-128">ฟิลด์นี้กำหนดวิธีการที่จะใช้ในการกำหนดว่าควรจะปล่อยงานเพิ่มเติมเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="aca58-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="aca58-129">คุณสามารถปล่อยงานตามปริมาณหรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="aca58-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="aca58-130">*เปอร์เซ็นต์* – เลือกตัวเลือกนี้เพื่อใช้ความจุที่เป็นเปอร์เซ็นต์ ซึ่งยึดตามขีดจำกัดการเก็บสต็อกหรือปริมาตร</span><span class="sxs-lookup"><span data-stu-id="aca58-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="aca58-131">การเลือกตัวเลือกนี้จะเปิดใช้งานฟิลด์ **เปอร์เซ็นต์ที่มีปริมาณมากเกินไป** และปิดใช้งานฟิลด์ที่เกี่ยวข้องกับปริมาณสองฟิลด์ **ปริมาณที่มากเกินไป** และ **หน่วยที่มากเกินไป**</span><span class="sxs-lookup"><span data-stu-id="aca58-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="aca58-132">คุณสามารถใช้ตัวเลือกนี้ ถ้าสถานที่เบิกสินค้าใช้ปริมาตร</span><span class="sxs-lookup"><span data-stu-id="aca58-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="aca58-133">ถ้าเลือกตัวเลือกนี้ ให้ตั้งค่าฟิลด์ **เปอร์เซ็นต์ที่มีปริมาณมากเกินไป** เป็นเปอร์เซ็นต์ ซึ่งการทำงานการเติมสินค้ามากขึ้นจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="aca58-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="aca58-134">*ปริมาณ* – เลือกตัวเลือกนี้เพื่อใช้ค่าปริมาณที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="aca58-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="aca58-135">การเลือกตัวเลือกนี้จะปิดใช้งานฟิลด์ **เปอร์เซ็นต์ที่ปริมาณมากเกินไป** และเปิดใช้งานฟิลด์ **ปริมาณที่มากเกินไป** และ **หน่วยที่มากเกินไป**</span><span class="sxs-lookup"><span data-stu-id="aca58-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="aca58-136">ใช้ตัวเลือกนี้ เมื่อคุณไม่ได้ใช้ปริมาตรสำหรับสถานที่เก็บที่มีการเติมสินค้า หรือเมื่อคุณมีปริมาณที่สอดคล้องกัน ที่คุณต้องการให้มีการนำสินค้าคงคลังไปยังสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="aca58-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="aca58-137">ถ้าเลือกตัวเลือกนี้ ให้ตั้งค่าฟิลด์ **ปริมาณที่มากเกินไป** และ **หน่วยที่มากเกินไป** ไปที่ปริมาณและหน่วยที่งานการเติมสินค้ามากขึ้นจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="aca58-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="aca58-138">**ปริมาณที่มากเกินไป:** *0.65*</span><span class="sxs-lookup"><span data-stu-id="aca58-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="aca58-139">ฟิลด์นี้กำหนดปริมาณที่มากเกินไปสำหรับสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="aca58-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="aca58-140">งานจะพร้อมใช้งานเมื่อใดก็ตามที่ผลรวมของปริมาณคงเหลือในสถานที่เก็บ และปริมาณงานต่ำกว่าค่านี้</span><span class="sxs-lookup"><span data-stu-id="aca58-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="aca58-141">งานการเติมสินค้าใดๆ ที่อยู่เหนือค่านี้จะถูกบล็อค และต้องปลดบล็อคด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="aca58-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="aca58-142">ขีดจำกัดการเก็บสต็อกในสถานที่เก็บจะถูกพิจารณาเมื่อมีการคำนวณปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="aca58-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="aca58-143">**หน่วยที่มากเกินไป:** *PL*</span><span class="sxs-lookup"><span data-stu-id="aca58-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="aca58-144">ฟิลด์นี้ชกำหนดหน่วยที่สัมพันธ์กับปริมาณที่มากเกินไป</span><span class="sxs-lookup"><span data-stu-id="aca58-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="aca58-145">ในกรณีนี้ งานการเติมสินค้ามากขึ้นจะพร้อมใช้งาน เมื่อสถานที่เก็บลดลงไปที่แท่นวางสินค้า 0.65 (PL)</span><span class="sxs-lookup"><span data-stu-id="aca58-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="aca58-146">**เปอร์เซ็นต์โอเวอร์โฟลว์**</span><span class="sxs-lookup"><span data-stu-id="aca58-146">**Overflow percentage**</span></span>

        <span data-ttu-id="aca58-147">ฟิลด์นี้กำหนดเปอร์เซ็นต์ที่มากเกินไปสำหรับสถานที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="aca58-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="aca58-148">งานจะพร้อมใช้งานเมื่อใดก็ตามที่ผลรวมของปริมาณคงเหลือในสถานที่เก็บ และปริมาณงานต่ำกว่าเปอร์เซ็นต์นี้</span><span class="sxs-lookup"><span data-stu-id="aca58-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="aca58-149">เปอร์เซ็นต์ของปริมาณงานการเติมสินค้าใดๆ ที่อยู่เหนือค่านี้จะถูกบล็อค และต้องปลดบล็อคด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="aca58-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="aca58-150">ขีดจำกัดการเก็บสต็อกในสถานที่เก็บจะถูกพิจารณาเมื่อมีการคำนวณเปอร์เซ็นต์ของปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="aca58-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="aca58-151">ถ้าไม่มีการกำหนดขีดจำกัดการเก็บสต็อกในสถานที่ เปอร์เซ็นต์ของปริมาณงานจะมีการคำนวณโดยปริมาตร ถ้ามีข้อจำกัดของปริมาตรสำหรับโพรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aca58-152">ถ้าคุณกำลังใช้ข้อมูลสาธิตสำหรับนิติบุคคล **USMF** และเพิ่งเปิดใช้งานลักษณะการทำงาน *การกำหนดตำแหน่งป้ายทะเบียนตามสถานที่* คุณต้องปิดการตั้งค่า **เปิดใช้งานการกำหนดตำแหน่งป้ายทะเบียน** สำหรับโพรไฟล์สถาน **BULK-06** เพื่อทำตามขั้นตอนบนอุปกรณ์เคลื่อนที่ในสถานการณ์จำลองตัวอย่างให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="aca58-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="aca58-153">รหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="aca58-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="aca58-154">เมื่อต้องการตั้งค่ารหัสขั้นตอนของเวฟตามที่อธิบายไว้ที่นี่ คุณอาจต้องใช้ [การจัดการลักษณะการทำงาน](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งานลักษณะการทำงานที่มีชื่อว่า *รหัสขั้นตอนของเวฟแบบกว้างขององค์กร*</span><span class="sxs-lookup"><span data-stu-id="aca58-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="aca58-155">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> รหัสขั้นตอนของเวฟ**</span><span class="sxs-lookup"><span data-stu-id="aca58-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="aca58-156">เลือก **สร้าง** และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="aca58-157">**รหัสขั้นตอนของเวฟ:** *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="aca58-158">**คำอธิบายขั้นตอนของเวฟ:** *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="aca58-159">**ชนิดของขั้นตอนเวฟ:** *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="aca58-160">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="aca58-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="aca58-161">แม่แบบการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-161">Replenishment template</span></span>

<span data-ttu-id="aca58-162">แม่แบบการเติมสินค้าคือ ชุดของกฎที่ควบคุมเวลาและวิธีการเติมสินค้าสถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="aca58-163">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="aca58-164">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="aca58-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="aca58-165">ในส่วน **ภาพรวม** ให้เลือกรายการที่มีฟิลด์ **แม่แบบการเติมสินค้า** ตั้งค่าให้กับ *ความต้องการเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="aca58-166">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-166">Set the following values:</span></span>

    - <span data-ttu-id="aca58-167">**รหัสขั้นตอนของเวฟ:** *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="aca58-168">**อนุญาตให้ความต้องการเวฟใช้ปริมาณที่ไม่ได้จอง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="aca58-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="aca58-169">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="aca58-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="aca58-170">เท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="aca58-170">Wave template</span></span>

1. <span data-ttu-id="aca58-171">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="aca58-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="aca58-172">ในบานหน้าต่างด้านซ้าย ตั้งค่าฟิลด์ **ชนิดแม่แบบเวฟ** เป็น *การจัดส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="aca58-173">เลือกแม่แบบ **61 การจัดส่งสินค้า** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="aca58-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="aca58-174">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="aca58-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="aca58-175">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **กำหนดให้การนำงานการเพิ่มเติมสินค้าออกใช้เป็นอัตโนมัติ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="aca58-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="aca58-176">ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อสร้างงานการเติมสินค้าตามความต้องการ และนำออกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="aca58-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="aca58-177">คุณต้องเพิ่มวิธีของเวฟการเพิ่มเติมสินค้าไปยังแม่แบบเวฟ และสร้างแม่แบบการเติมสินค้าของชนิด **ความต้องการเวฟ**</span><span class="sxs-lookup"><span data-stu-id="aca58-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="aca58-178">ตั้งค่าแม่แบบการเติมสินค้าในหน้า **แม่แบบการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="aca58-179">เมื่อต้องการตั้งค่าแม่แบบการเติมสินค้า คุณต้องเพิ่มวิธีการเติมข้อมูลลงในแม่แบบเวฟ</span><span class="sxs-lookup"><span data-stu-id="aca58-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="aca58-180">บนแท็บด่วน **วิธีการ** ในคอลัมน์ **วิธีการที่เลือก** ให้ค้นหารายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="aca58-181">**ชื่อวิธีการ:** *เติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="aca58-182">**ชื่อ:** *การเติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="aca58-183">ตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** สำหรับรายการนี้ไปที่ *เติมสินค้า*</span><span class="sxs-lookup"><span data-stu-id="aca58-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="aca58-184">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="aca58-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="aca58-185">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="aca58-185">Example scenario</span></span>

<span data-ttu-id="aca58-186">หลังจากที่คุณได้ทำให้ข้อมูลตัวอย่างที่อธิบายไว้ก่อนหน้านี้ทั้งหมดพร้อมใช้งานแล้ว และตั้งค่าแล้ว คุณสามารถทำงานกับสถานการณ์จำลองนี้ เพื่อลองใช้ลักษณะการทำงาน *การเติมสินค้าตามความจุของสถานที่*</span><span class="sxs-lookup"><span data-stu-id="aca58-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="aca58-187">ค่าที่แสดงในสถานการณ์สมมตินี้สมมติว่าคุณกำลังทำงานกับข้อมูลสาธิตมาตรฐาน ซึ่งคุณเลือกนิติบุคคล **USMF** และคุณได้เตรียมเรกคอร์ดตัวอย่างที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="aca58-188">นอกจากนี้สถานการณ์จำลองนี้ยังทำหน้าที่เป็นตัวอย่างที่แสดงว่าคุณลักษณะนี้สามารถใช้ในการตั้งค่าการผลิตได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="aca58-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="aca58-189">สร้างงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="aca58-190">สร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="aca58-190">Create sales order 1</span></span>

1. <span data-ttu-id="aca58-191">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="aca58-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="aca58-192">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบสำหรับการสร้างใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="aca58-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="aca58-193">ในกล่องโต้ตอบ ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="aca58-194">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="aca58-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="aca58-195">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="aca58-196">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="aca58-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="aca58-197">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="aca58-197">The new sales order is opened.</span></span> <span data-ttu-id="aca58-198">ซึ่งรวมรายการว่างใหม่บนแท็บด่วน **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="aca58-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="aca58-199">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="aca58-200">**หมายเลขสินค้า:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="aca58-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="aca58-201">**ปริมาณ:** *40*</span><span class="sxs-lookup"><span data-stu-id="aca58-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="aca58-202">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **สินค้าคงคลัง \> การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="aca58-203">บนหน้า **การจองสินค้า** ให้เลือก **จองล็อต**</span><span class="sxs-lookup"><span data-stu-id="aca58-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="aca58-204">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aca58-204">Close the page.</span></span>
1. <span data-ttu-id="aca58-205">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="aca58-206">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการจัดส่งที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="aca58-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="aca58-207">มีการสร้างเวฟการเติมสินค้าด้วย</span><span class="sxs-lookup"><span data-stu-id="aca58-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="aca58-208">นอกจากนี้คุณยังได้รับข้อความแจ้งเตือนที่ระบุว่า "รหัสงาน XXXX ไม่สามารถปลดบล็อคได้ เนื่องจากมีงานการเติมสินค้าที่ยังไม่เสร็จสิ้น"</span><span class="sxs-lookup"><span data-stu-id="aca58-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="aca58-209">สร้างใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="aca58-209">Create sales order 2</span></span>

1. <span data-ttu-id="aca58-210">บนหน้า **ใบสั่งขายทั้งหมด** บนบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบสำหรับการสร้างใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="aca58-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="aca58-211">ในกล่องโต้ตอบ ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="aca58-212">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="aca58-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="aca58-213">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="aca58-214">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="aca58-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="aca58-215">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="aca58-215">The new sales order is opened.</span></span> <span data-ttu-id="aca58-216">ซึ่งรวมรายการว่างใหม่บนแท็บด่วน **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="aca58-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="aca58-217">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="aca58-218">**หมายเลขสินค้า:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="aca58-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="aca58-219">**ปริมาณ:** *60*</span><span class="sxs-lookup"><span data-stu-id="aca58-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="aca58-220">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **สินค้าคงคลัง \> การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="aca58-221">บนหน้า **การจองสินค้า** ให้เลือก **จองล็อต**</span><span class="sxs-lookup"><span data-stu-id="aca58-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="aca58-222">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aca58-222">Close the page.</span></span>
1. <span data-ttu-id="aca58-223">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="aca58-224">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการจัดส่งที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="aca58-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="aca58-225">มีการสร้างเวฟการเติมสินค้าด้วย</span><span class="sxs-lookup"><span data-stu-id="aca58-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="aca58-226">นอกจากนี้คุณยังได้รับข้อความแจ้งเตือนที่ระบุว่า "รหัสงาน XXXX ไม่สามารถปลดบล็อคได้ เนื่องจากมีงานการเติมสินค้าที่ยังไม่เสร็จสิ้น"</span><span class="sxs-lookup"><span data-stu-id="aca58-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="aca58-227">สร้างใบสั่งขาย 3</span><span class="sxs-lookup"><span data-stu-id="aca58-227">Create sales order 3</span></span>

1. <span data-ttu-id="aca58-228">บนหน้า **ใบสั่งขายทั้งหมด** บนบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบสำหรับการสร้างใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="aca58-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="aca58-229">ในกล่องโต้ตอบ ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="aca58-230">**บัญชีลูกค้า:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="aca58-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="aca58-231">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="aca58-232">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="aca58-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="aca58-233">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="aca58-233">The new sales order is opened.</span></span> <span data-ttu-id="aca58-234">ซึ่งรวมรายการว่างใหม่บนแท็บด่วน **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="aca58-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="aca58-235">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aca58-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="aca58-236">**หมายเลขสินค้า:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="aca58-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="aca58-237">**ปริมาณ:** *30*</span><span class="sxs-lookup"><span data-stu-id="aca58-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="aca58-238">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **สินค้าคงคลัง \> การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="aca58-239">บนหน้า **การจองสินค้า** ให้เลือก **จองล็อต**</span><span class="sxs-lookup"><span data-stu-id="aca58-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="aca58-240">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aca58-240">Close the page.</span></span>
1. <span data-ttu-id="aca58-241">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="aca58-242">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการจัดส่งที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="aca58-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="aca58-243">มีการสร้างเวฟการเติมสินค้าด้วย</span><span class="sxs-lookup"><span data-stu-id="aca58-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="aca58-244">นอกจากนี้คุณยังได้รับข้อความแจ้งเตือนที่ระบุว่า "รหัสงาน XXXX ไม่สามารถปลดบล็อคได้ เนื่องจากมีงานการเติมสินค้าที่ยังไม่เสร็จสิ้น"</span><span class="sxs-lookup"><span data-stu-id="aca58-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="aca58-245">ดูรายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="aca58-245">View work details</span></span>

1. <span data-ttu-id="aca58-246">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="aca58-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="aca58-247">ในส่วน **ภาพรวม** ให้กรองคอลัมน์ **คลังสินค้า** สำหรับคลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="aca58-248">คุณควรเห็นว่ามีการสร้างเจ็ดรหัสงานสำหรับใบสั่งขายที่มีความต้องการสามใบ</span><span class="sxs-lookup"><span data-stu-id="aca58-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="aca58-249">สามในเจ็ดรหัสงานมีค่าของ **ชนิดใบสั่งงาน** เป็น *การเติมสินค้า* และสี่รหัสงานมีค่าของ **ชนิดใบสั่งงาน** เป็น *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="aca58-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="aca58-250">รหัสงานทั้งสามที่มีค่าของ **ชนิดใบสั่งงาน** เป็น *การเติมสินค้า* มีสถานที่ *เบิกสินค้า* และ *ส่งสินค้า* เดียวกันในส่วนของ **รายการ**:</span><span class="sxs-lookup"><span data-stu-id="aca58-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="aca58-251">**เบิก:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="aca58-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="aca58-252">**ส่ง:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="aca58-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="aca58-253">รหัสงานสองรหัสสร้างสำหรับใบสั่งขาย1</span><span class="sxs-lookup"><span data-stu-id="aca58-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="aca58-254">จดบันทึกรหัสงานสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="aca58-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="aca58-255">ทั้งนี้ขึ้นอยู่กับปริมาณคงคลังคงเหลือของคุณ ปริมาณงานที่สร้างขึ้นอาจแตกต่างกันเล็กน้อย</span><span class="sxs-lookup"><span data-stu-id="aca58-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="aca58-256">อย่างไรก็ตาม โดยรวมแล้ว ส่วนหัวของงานที่สร้างขึ้นควรตรงกับตัวอย่างสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="aca58-257">รหัสป้ายทะเบียนตามสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="aca58-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="aca58-258">ในสถานการณ์นี้ คุณจะใช้แอปคลังสินค้า (หรือตัวเลียนแบบ) ซึ่งคุณต้องระบุป้ายทะเบียนเพื่อให้สถานการณ์การเบิกสินค้าและการเติมสินค้าเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aca58-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="aca58-259">เมื่อต้องการค้นหารหัสป้ายทะเบียนที่คุณจะต้องใช้ในภายหลัง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="aca58-260">ไปยัง **การบริหารสินค้าคงคลัง \> การสอบถาม และรายงาน \> รายการปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="aca58-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="aca58-261">เลือกปุ่ม **แสดงตัวกรอง** เพื่อเปิดบานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="aca58-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="aca58-262">ป้อนเงื่อนไขการกรองข้อมูลต่อไปนี้ เพื่อเรียกใช้แผ่นป้ายทะเบียนสำหรับสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="aca58-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="aca58-263">ใช้ตัวกรอง *เริ่มต้นด้วย*</span><span class="sxs-lookup"><span data-stu-id="aca58-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="aca58-264">**หมายเลขสินค้า:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="aca58-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="aca58-265">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="aca58-266">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="aca58-266">Select **Apply**.</span></span>
1. <span data-ttu-id="aca58-267">บนบานหน้าต่างการดำเนินการ เลือก **มิติ**</span><span class="sxs-lookup"><span data-stu-id="aca58-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="aca58-268">ในกล่องโต้ตอบ **การแสดงมิติ** ในส่วน **มิติการจัดเก็บ** เลือกค่าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="aca58-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="aca58-269">ในส่วน **ธุรกรรม** ให้เลือก **หมายเลขสินค้า** และ **ปริมาณ \<\> 0**</span><span class="sxs-lookup"><span data-stu-id="aca58-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="aca58-270">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="aca58-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="aca58-271">กริด **คงคลังคงเหลือ** แสดงหมายเลขป้ายทะเบียนสำหรับสินค้า *T0100* ในแต่ละสถานที่</span><span class="sxs-lookup"><span data-stu-id="aca58-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="aca58-272">จดป้ายทะเบียนที่อยู่ในแต่ละสถานที่ เนื่องจากคุณจะต้องใช้ข้อมูลนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="aca58-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="aca58-273">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aca58-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="aca58-274">ขั้นตอนของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="aca58-274">Process steps</span></span>

<span data-ttu-id="aca58-275">คุณจะดำเนินการเติมสินค้าที่ตั้งของคลังสินค้าสำหรับสองรหัสงานแรก</span><span class="sxs-lookup"><span data-stu-id="aca58-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="aca58-276">งานในงานการเติมสินค้าที่สามจะถูกบล็อคจนกว่าระดับสินค้าคงคลังในสถานที่เบิกสินค้าจะอยู่ต่ำกว่าขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="aca58-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="aca58-277">การเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-277">Replenishment</span></span>

1. <span data-ttu-id="aca58-278">ลงชื่อเข้าใช้แอปคลังสินค้าในฐานะผู้ใช้ในคลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="aca58-279">(ป้อน *61* เป็นรหัสผู้ใช้และ *1* เป็นรหัสผ่าน)</span><span class="sxs-lookup"><span data-stu-id="aca58-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="aca58-280">ไปที่ **สินค้าคงคลัง \> การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="aca58-281">คุณได้รับพร้อมท์ให้ดำเนินงานการเติมสินค้าแรก</span><span class="sxs-lookup"><span data-stu-id="aca58-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="aca58-282">หมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้าแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="aca58-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="aca58-283">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="aca58-284">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="aca58-285">ระบบสร้างหมายเลขป้ายทะเบียนเป้าหมายสำหรับป้ายทะเบียนใหม่สำหรับสินค้าที่เบิก</span><span class="sxs-lookup"><span data-stu-id="aca58-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="aca58-286">เลือก **ตกลง** เพื่อยืนยันค่า</span><span class="sxs-lookup"><span data-stu-id="aca58-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="aca58-287">งานการส่งสินค้าจะแสดงขึ้นเพื่อให้ผู้ใช้สามารถส่งป้ายทะเบียนเป้าหมายลงในสถานที่การเติมสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="aca58-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="aca58-288">สถานที่ *ส่ง* ควรจะเป็น **06A01R2S1B**</span><span class="sxs-lookup"><span data-stu-id="aca58-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="aca58-289">ยืนยันรายละเอียดการส่ง และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="aca58-290">คุณได้รับข้อความ "ทำงานสำเร็จ" และรายละเอียดของงานการเบิกการเติมสินค้าครั้งถัดไปจะแสดงขึ้น: หมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="aca58-291">สถานที่เบิกสินค้าจะเหมือนกับสถานที่การเติมสินค้าแรก</span><span class="sxs-lookup"><span data-stu-id="aca58-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="aca58-292">ดังนั้น ป้ายทะเบียนดังกล่าวจะมีรหัสป้ายทะเบียนเดียวกันกับที่ใช้สำหรับงานการเติมสินค้าครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="aca58-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="aca58-293">ทำซ้ำขั้นตอนก่อนหน้านี้ เพื่อทำงานการเติมสินค้าให้เสร็จสมบูรณ์สำหรับงานที่สอง</span><span class="sxs-lookup"><span data-stu-id="aca58-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="aca58-294">ป้ายทะเบียนของปริมาณและเป้าหมายจะแตกต่างจากป้ายทะเบียนของปริมาณและเป้าหมายสำหรับงานครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="aca58-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="aca58-295">หลังจากงานการเติมสินค้าที่สองเสร็จสมบูรณ์แล้ว คุณจะได้รับข้อความ "ทำงานสำเร็จ"</span><span class="sxs-lookup"><span data-stu-id="aca58-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="aca58-296">อุปกรณ์เคลื่อนที่ยังแจ้งให้คุณทราบว่ามีงานที่ไม่พร้อมใช้งาน ถึงแม้ว่าบางงานการเติมสินค้าจะยังคงอยู่</span><span class="sxs-lookup"><span data-stu-id="aca58-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="aca58-297">ลักษณะการทำงานนี้เกิดขึ้นเนื่องจากงานการเติมสินค้ามีสถานะความพร้อมใช้งาน *ค้างอยู่* และถูกทำเครื่องหมายเป็น **ถูกบล็อค**</span><span class="sxs-lookup"><span data-stu-id="aca58-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="aca58-298">สถานะ *ที่ค้างอยู่* ถูกทริกเกอร์เนื่องจากโพรไฟล์สถานที่สำหรับสถานที่เบิกสินค้าที่มีการกำหนดงานมีค่า **ปริมาณที่มากเกินไป** เป็น *0.65 PL*</span><span class="sxs-lookup"><span data-stu-id="aca58-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="aca58-299">งานการเติมสินค้าก่อนหน้าสองงานที่กรอกข้อมูลสถานที่เกือบถึงขีดจำกัดที่มากเกินไปสำหรับสินค้า *T0100*</span><span class="sxs-lookup"><span data-stu-id="aca58-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="aca58-300">(การแปลงหน่วยสำหรับสินค้าเป็น *1 PL = 100 ea*) ดังนั้น งานการเติมสินค้าที่เหลืออาจทำให้สถานที่เกินขีดจำกัดมากเกินไป</span><span class="sxs-lookup"><span data-stu-id="aca58-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="aca58-301">จนกว่าจะมีการเบิกสินค้าคงคลังจากสถานที่เก็บให้ต่ำกว่าขีดจำกัดการปล่อยงานบนรายการเมนูของอุปกรณ์เคลื่อนที่ งานการเติมสินค้านี้จะยังคงถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="aca58-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="aca58-302">การเลือกใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="aca58-302">Sales order pick</span></span>

<span data-ttu-id="aca58-303">ก่อนที่จะทำงานการเติมสินค้าที่เหลือให้เสร็จสมบูรณ์ สถานที่เบิกสินค้าต้องทำให้สินค้าคงคลังลดถึงระดับที่งานการเติมสินค้าที่เหลืออยู่สามารถปลดบล็อคได้</span><span class="sxs-lookup"><span data-stu-id="aca58-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="aca58-304">กล่าวคือ ผลรวมของปริมาณของปริมาณคงคลังคงเหลือในสถานที่ และปริมาณการเติมสินค้าต้องไม่เกินค่าของ **ปริมาณที่มากเกินไป**</span><span class="sxs-lookup"><span data-stu-id="aca58-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="aca58-305">เมื่อผลรวมนี้น้อยกว่าปริมาณที่มากเกินไป งานการเติมสินค้าที่เหลือจะถูกปลดบล็อค</span><span class="sxs-lookup"><span data-stu-id="aca58-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="aca58-306">ลงชื่อเข้าใช้แอปคลังสินค้าในฐานะผู้ใช้ในคลังสินค้า *61*</span><span class="sxs-lookup"><span data-stu-id="aca58-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="aca58-307">(ป้อน *61* เป็นรหัสผู้ใช้และ *1* เป็นรหัสผ่าน)</span><span class="sxs-lookup"><span data-stu-id="aca58-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="aca58-308">ไปที่ **ขาออก \> การเบิกสินค้าการขาย**</span><span class="sxs-lookup"><span data-stu-id="aca58-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="aca58-309">ป้อนรหัสงานแรกสำหรับใบสั่งขาย1</span><span class="sxs-lookup"><span data-stu-id="aca58-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="aca58-310">อ้างอิงถึงรหัสงานสำหรับใบสั่งขายที่คุณได้ทำบันทึกของก่อนหน้านี้ บนหน้า **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="aca58-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="aca58-311">รหัสงานที่คุณป้อนที่นี่จะสร้างงานการเบิกสินค้าสำหรับปริมาณ 10 ea จากสถานที่ที่แยกต่างหากสองแห่ง</span><span class="sxs-lookup"><span data-stu-id="aca58-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="aca58-312">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-312">Select **OK**.</span></span>

    <span data-ttu-id="aca58-313">หน้างาน **ใบสั่งขาย: การเบิกสินค้า** จะแสดงหมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้าสำหรับสถานที่เก็บแรก</span><span class="sxs-lookup"><span data-stu-id="aca58-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="aca58-314">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="aca58-315">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="aca58-316">**ใบสั่งขาย: หน้างานการเบิกสินค้า** จะแสดงหมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้าสำหรับสถานที่เก็บถัดไป</span><span class="sxs-lookup"><span data-stu-id="aca58-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="aca58-317">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="aca58-318">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="aca58-319">**ใบสั่งขาย: หน้าการส่ง** แนะนำให้คุณย้ายงานการเบิกสินค้าที่เสร็จสมบูรณ์ทั้งหมดไปยังสถานที่การจัดเตรียมขาออก</span><span class="sxs-lookup"><span data-stu-id="aca58-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="aca58-320">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-320">Select **OK**.</span></span>

    <span data-ttu-id="aca58-321">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="aca58-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="aca58-322">ป้อนรหัสงานที่สองสำหรับใบสั่งขาย1</span><span class="sxs-lookup"><span data-stu-id="aca58-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="aca58-323">มีเพียงงานการเบิกสินค้าเดียวสำหรับรหัสงานนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="aca58-324">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-324">Select **OK**.</span></span>

    <span data-ttu-id="aca58-325">**ใบสั่งขาย: หน้างานการเบิกสินค้า** จะแสดงหมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="aca58-326">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="aca58-327">ป้ายทะเบียนที่คุณระบุจะเป็นหนึ่งในป้ายทะเบียนที่ระบบสร้างขึ้นจากงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="aca58-328">เมื่อต้องการตรวจสอบให้แน่ใจว่าคุณได้บันทึรหัสป้ายทะเบียนที่ถูกต้อง ให้ตรวจสอบสินค้าคงคลังในหน้า **รายการปริมาณคงคลังคงเหลือ** สำหรับสินค้า สถานที่เก็บ และปริมาณ</span><span class="sxs-lookup"><span data-stu-id="aca58-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="aca58-329">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="aca58-330">ยืนยันคำสั่งสำหรับงานการส่งไปยังสถานที่การจัดเตรียมขาออก</span><span class="sxs-lookup"><span data-stu-id="aca58-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="aca58-331">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-331">Select **OK**.</span></span>

    <span data-ttu-id="aca58-332">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="aca58-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="aca58-333">ใบสั่งขาย2 ถูกบล็อคจากการเบิกสินค้า เนื่องจากงานการเติมสินค้าที่เชื่อมโยงไปไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aca58-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="aca58-334">ปัจจุบัน ยังคงมีปริมาณ 30 ea ในสถานที่เบิกสินค้า และปริมาณการเติมสินค้าสำหรับใบสั่งขาย2 คือ 60 ea</span><span class="sxs-lookup"><span data-stu-id="aca58-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="aca58-335">ผลรวมของปริมาณคงคลังคงเหลือและสินค้าคงคลังการเติมสินค้า (90 ea) เกินกว่าปริมาณที่มากเกินไป 0.65 PL (หรือ 65 ea)</span><span class="sxs-lookup"><span data-stu-id="aca58-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="aca58-336">ก่อนงานการเติมสินค้าเสร็จสมบูรณ์ ใบสั่งขาย3 ต้องมีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="aca58-337">ป้อนรหัสงานสำหรับใบสั่งขาย3</span><span class="sxs-lookup"><span data-stu-id="aca58-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="aca58-338">มีเพียงงานการเบิกสินค้าเดียวสำหรับรหัสงานนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="aca58-339">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-339">Select **OK**.</span></span>

    <span data-ttu-id="aca58-340">**ใบสั่งขาย: หน้างานการเบิกสินค้า** จะแสดงหมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="aca58-341">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="aca58-342">ป้ายทะเบียนที่คุณระบุจะเป็นหนึ่งในป้ายทะเบียนที่ระบบสร้างขึ้นจากงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="aca58-343">เมื่อต้องการตรวจสอบให้แน่ใจว่าคุณได้บันทึรหัสป้ายทะเบียนที่ถูกต้อง ให้ตรวจสอบสินค้าคงคลังในหน้า **รายการปริมาณคงคลังคงเหลือ** สำหรับสินค้า สถานที่เก็บ และปริมาณ</span><span class="sxs-lookup"><span data-stu-id="aca58-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="aca58-344">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="aca58-345">ยืนยันคำสั่งสำหรับงานการส่งไปยังสถานที่การจัดเตรียมขาออก</span><span class="sxs-lookup"><span data-stu-id="aca58-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="aca58-346">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-346">Select **OK**.</span></span>

    <span data-ttu-id="aca58-347">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="aca58-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="aca58-348">ทันทีที่ผลรวมของปริมาณคงคลังคงเหลือในสถานที่เบิกสินค้าและปริมาณการเติมสินค้าต่ำกว่าขีดจำกัด คุณจะสามารถประมวลผลงานการเติมสินค้าที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="aca58-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="aca58-349">กลับไปที่หน้า **รายละเอียดของงาน** และสังเกตว่าความพร้อมใช้งานของงานการเติมสินค้าสำหรับการเติมสินค้าสุดท้าย (สำหรับใบสั่งขาย 2) ถูก *เปิด* เนื่องจากมีพื้นที่ว่างเพียงพอในสถานที่เพื่อรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="aca58-350">ขณะนี้คุณสามารถประมวลผลงานการเติมสินค้านี้ผ่านทางอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="aca58-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="aca58-351">ไปที่ **สินค้าคงคลัง \> การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="aca58-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="aca58-352">คุณได้รับพร้อมท์ให้ดำเนินงานการเติมสินค้าที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="aca58-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="aca58-353">หมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้าแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="aca58-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="aca58-354">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="aca58-355">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="aca58-356">ระบบสร้างหมายเลขป้ายทะเบียนเป้าหมายสำหรับป้ายทะเบียนใหม่สำหรับสินค้าที่เบิก</span><span class="sxs-lookup"><span data-stu-id="aca58-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="aca58-357">เลือก **ตกลง** เพื่อยืนยันค่า</span><span class="sxs-lookup"><span data-stu-id="aca58-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="aca58-358">งานการส่งสินค้าจะแสดงขึ้นเพื่อให้ผู้ใช้สามารถส่งป้ายทะเบียนเป้าหมายลงในสถานที่การเติมสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="aca58-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="aca58-359">สถานที่ *ส่ง* ควรจะเป็น **06A01R2S1B**</span><span class="sxs-lookup"><span data-stu-id="aca58-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="aca58-360">ยืนยันรายละเอียดการส่ง และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="aca58-361">คุณได้รับข้อความ "ทำงานสำเร็จ" และ "ไม่มีงานที่พร้อมใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="aca58-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="aca58-362">ขณะนี้คุณสามารถเบิกสินค้าตามใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="aca58-362">You can now pick sales order 2.</span></span> <span data-ttu-id="aca58-363">จะไม่มีการปลดบล็อคเมื่องานการเติมสินค้าที่เชื่อมโยงกับใบสั่งขายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aca58-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="aca58-364">ป้อนรหัสงานสำหรับใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="aca58-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="aca58-365">มีเพียงงานการเบิกสินค้าเดียวสำหรับรหัสงานนี้</span><span class="sxs-lookup"><span data-stu-id="aca58-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="aca58-366">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-366">Select **OK**.</span></span>

    <span data-ttu-id="aca58-367">**ใบสั่งขาย: หน้างานการเบิกสินค้า** จะแสดงหมายเลขสินค้า ปริมาณ และสถานที่ที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="aca58-368">ในฟิลด์ **LP** ให้ป้อนหมายเลขป้ายทะเบียนสำหรับสินค้าในที่ตั้งที่แสดง</span><span class="sxs-lookup"><span data-stu-id="aca58-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="aca58-369">ป้ายทะเบียนที่คุณระบุจะเป็นป้ายทะเบียนที่ระบบสร้างขึ้นจากงานการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="aca58-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="aca58-370">เมื่อต้องการตรวจสอบให้แน่ใจว่าคุณได้บันทึรหัสป้ายทะเบียนที่ถูกต้อง ให้ตรวจสอบสินค้าคงคลังในหน้า **รายการปริมาณคงคลังคงเหลือ** สำหรับสินค้า สถานที่เก็บ และปริมาณ</span><span class="sxs-lookup"><span data-stu-id="aca58-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="aca58-371">เลือกปุ่ม **ตกลง** (สัญลักษณ์เครื่องหมายถูก)</span><span class="sxs-lookup"><span data-stu-id="aca58-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="aca58-372">ยืนยันคำสั่งสำหรับงานการส่งไปยังสถานที่การจัดเตรียมขาออก</span><span class="sxs-lookup"><span data-stu-id="aca58-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="aca58-373">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="aca58-373">Select **OK**.</span></span>

    <span data-ttu-id="aca58-374">คุณได้รับข้อความแสดงข้อความ "ทำงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="aca58-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="aca58-375">หมายเหตุและเคล็ดลับ</span><span class="sxs-lookup"><span data-stu-id="aca58-375">Notes and tips</span></span>

- <span data-ttu-id="aca58-376">ฟังก์ชันนี้ทำงานกับการเติมสินค้าทุกชนิด: ความต้องการของเวฟ ต่ำสุด/สูงสุด ความต้องการโหลด และการแบ่งช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="aca58-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="aca58-377">คุณสามารถแทนที่ความพร้อมใช้งานของงานการเติมสินค้าสำหรับแต่ละหัวข้องานจากหน้า **รายละเอียดงาน** หากคุณต้องการได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="aca58-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="aca58-378">เมื่อระบบกำหนดความพร้อมในการทำงานของการเติมสินค้า จะถือว่าสินค้าคงคลังใดๆ ที่อยู่ในสถานที่เก็บอยู่แล้วก่อนที่จะทำงานใดๆ เป็นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aca58-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="aca58-379">งานของใบสั่งขายแต่ละใบจะเชื่อมโยงกับงานการเติมสินค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="aca58-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="aca58-380">ไม่มีฟังก์ชันความพร้อมใช้งานของงานการขายที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="aca58-380">There is no corresponding sales work availability functionality.</span></span>
