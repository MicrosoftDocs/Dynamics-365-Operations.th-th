---
title: การเติมสินค้าตามขีดจำกัดของโซน
description: การเติมสินค้าตามโซนใช้กลยุทธ์การเติมสินค้าต่ำสุด/สูงสุด (ต่ำสุด/สูงสุด) แต่จะประเมินโซนคลังสินค้าทั้งหมด แทนที่จะเป็นเฉพาะที่ตั้งแต่ละแห่ง ดังนั้น ผู้จัดการคลังสินค้าสามารถเรียนรู้ได้อย่างรวดเร็วมากขึ้น เมื่อจำเป็นต้องมีสินค้าคงคลังเพิ่มเติมในโซนการเบิกสินค้า
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6aaa139fb206c035b25b7056e681d086fde6447f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245069"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="a8aea-104">การเติมสินค้าตามขีดจำกัดของโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8aea-105">การเติมสินค้าตามโซนใช้กลยุทธ์ [การเติมสินค้า](replenishment.md) ต่ำสุด/สูงสุด (ต่ำสุด/สูงสุด) แต่จะประเมินโซนคลังสินค้าทั้งหมด แทนที่จะเป็นเฉพาะสถานที่แต่ละแห่ง</span><span class="sxs-lookup"><span data-stu-id="a8aea-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="a8aea-106">ดังนั้น ผู้จัดการคลังสินค้าสามารถเรียนรู้ได้อย่างรวดเร็วมากขึ้น เมื่อจำเป็นต้องมีสินค้าคงคลังเพิ่มเติมในโซนการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="a8aea-107">การตั้งค่าสำหรับคุณลักษณะนี้คล้ายกับการตั้งค่าสำหรับการเติมสินค้าตามสถานที่</span><span class="sxs-lookup"><span data-stu-id="a8aea-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="a8aea-108">อย่างไรก็ตาม เมื่อคุณตั้งค่าเท็มเพลตสำหรับการเติมสินค้าต่ำสุด/สูงสุด คุณยังสามารถระบุได้ว่าควรประเมินขีดจำกัดสำหรับแต่ละสถานที่ หรือสำหรับแต่ละโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="a8aea-109">ถ้าคุณตั้งค่าการประเมินที่ยึดตามโซน คุณต้องเพิ่มโซนเฉพาะไปยังการสอบถามการเลือกโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="a8aea-110">เช่นเดียวกับการเติมสินค้าต่ำสุด/สูงสุดตามสถานที่ การเติมสินค้าต่ำสุด/สูงสุดตามโซนเวลา จะยึดตามการตั้งค่าขีดจำกัดของสินค้าคงคลังต่ำสุดที่ทริกเกอร์การสร้างงานการเติมสินค้าสำหรับรายการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a8aea-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="a8aea-111">งานการเติมสินค้านี้จะเพิ่มสินค้าคงคลังจนถึงขีดจำกัดสูงสุดที่ระบุสำหรับโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="a8aea-112">กระบวนการเติมสินค้าของโซนสำหรับผลิตภัณฑ์ย่อยไม่ได้รับการสนับสนุนในการนำออกใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a8aea-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="a8aea-113">โดยต่างจากการเติมสินค้าต่ำสุด/สูงสุดตามสถานที่ การเติมสินค้าต่ำสุด/สูงสุดตามโซนไม่จำเป็นต้องมีสถานที่คงที่ในการประเมินว่า สถานที่ควรจะจัดเก็บรายการเฉพาะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="a8aea-114">ดังนั้น การเติมสินค้าตามโซนช่วยให้คุณสามารถใช้การเติมสินค้าต่ำสุด/สูงสุด ถึงแม้ว่าคุณจะไม่มีสถานที่คงที่สำหรับสินค้าหรือตัวแปรสินค้าแต่ละรายการในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="a8aea-115">เมื่อปริมาณในโซนอยู่ต่ำกว่าขีดจำกัดต่ำสุดที่ระบุ งานการเติมสินค้าจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a8aea-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="a8aea-116">คำสั่งสถานที่จะกำหนดสถานที่เฉพาะที่ควรใช้ในการจัดเก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a8aea-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="a8aea-117">เปิดคุณลักษณะการเติมสินค้าของขีดจำกัดโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="a8aea-118">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การเติมสินค้าของขีดจำกัดโซน* ต้องมีการเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8aea-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a8aea-119">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a8aea-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a8aea-120">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a8aea-121">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="a8aea-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a8aea-122">**ชื่อคุณลักษณะ:** *การเติมสินค้าของขีดจำกัดโซน*</span><span class="sxs-lookup"><span data-stu-id="a8aea-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="a8aea-123">ตั้งค่าการเติมสินค้าตามโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="a8aea-124">เมื่อต้องการตั้งค่าการเติมสินค้าตามโซน คุณต้องตั้งค่าคอนฟิกระบบหลายส่วน</span><span class="sxs-lookup"><span data-stu-id="a8aea-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="a8aea-125">ส่วนนี้จะแนะนำการตั้งค่าต่างๆ และระบุค่าข้อมูลของการสาธิตซึ่งคุณสามารถป้อนได้ ถ้าคุณต้องการทำงานผ่านสถานการณ์จำลองในตอนท้ายของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="a8aea-126">ตั้งค่ารหัสคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="a8aea-126">Set up directive codes</span></span>

<span data-ttu-id="a8aea-127">[รหัสคำสั่ง](control-warehouse-location-directives.md) ช่วยให้คุณเฉพาะเจาะจงมากขึ้น เมื่อคุณคุณกำหนดเท็มเพลตสถานที่ที่ใช้ในเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="a8aea-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="a8aea-128">แต่ละรหัสสร้างค่าทั่วไปที่คุณสามารถอ้างอิงถึงเวลาที่คุณตั้งค่าคอนฟิกเท็มเพลตแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="a8aea-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="a8aea-129">ดูและแก้ไขรหัสคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="a8aea-129">View and edit directive codes</span></span>

<span data-ttu-id="a8aea-130">เมื่อต้องการดูหรือแก้ไขรหัสคำสั่งของคุณ ให้ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> รหัสคำสั่ง**</span><span class="sxs-lookup"><span data-stu-id="a8aea-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="a8aea-131">จัดเตรียมรหัสคำสั่งข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a8aea-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="a8aea-132">ตัวอย่างนี้แสดงวิธีการจัดเตรียมรหัสคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="a8aea-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="a8aea-133">ถ้าคุณกำลังวางแผนที่จะทำงานโดยผ่านสถานการณ์จำลองในตอนท้ายของหัวข้อนี้ ให้ใช้ค่าข้อมูลสาธิตที่ระบุไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="a8aea-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="a8aea-134">มิฉะนั้น ให้ใช้ค่าของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a8aea-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="a8aea-135">เลือกนิติบุคคล **USMF** เพื่อทำงานกับข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a8aea-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="a8aea-136">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> รหัสคำสั่ง**</span><span class="sxs-lookup"><span data-stu-id="a8aea-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="a8aea-137">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-138">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-139">**รหัสคำสั่ง:** _การเติมสินค้าของโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="a8aea-140">**คำอธิบายคำสั่ง:**_การเติมสินค้าของโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="a8aea-141">เลือก **บันทึก** เพื่อบันทึกรหัสใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="a8aea-142">ตั้งค่าเท็มเพลตการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-142">Set up replenishment templates</span></span>

<span data-ttu-id="a8aea-143">[เท็มเพลตการเติมสินค้าต่ำสุด/สูงสุด](tasks/set-up-min-max-replenishment-process.md) คือกลไกหลักสำหรับการรักษาระดับที่ดีที่สุดในสถานที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="a8aea-144">ในเท็มเพลตเหล่านี้ คุณต้องตั้งค่ากฎที่จะใช้ในการเติมสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="a8aea-145">การเติมสินค้าที่สามารถใช้เท็มเพลตได้ รวมถึงการเติมสินค้าตามโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="a8aea-146">ดูและแก้ไขเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-146">View and edit replenishment templates</span></span>

<span data-ttu-id="a8aea-147">เท็มเพลตการเติมสินค้าคือ ชุดของกฎที่ควบคุมเวลาและวิธีการเติมสินค้าสถานที่</span><span class="sxs-lookup"><span data-stu-id="a8aea-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="a8aea-148">คุณเลือกเท็มเพลตเพื่อควบคุมว่าจะดำเนินการเพิ่มเติมสินเมื่อใดและอย่างไร</span><span class="sxs-lookup"><span data-stu-id="a8aea-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="a8aea-149">เพื่อดูหรือแก้ไขเท็มเพลตการเติมสินค้าของคุณ ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a8aea-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="a8aea-150">จัดเตรียมเท็มเพลตการเติมข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a8aea-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="a8aea-151">ตัวอย่างนี้แสดงวิธีการจัดเตรียมเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="a8aea-152">ถ้าคุณกำลังวางแผนที่จะทำงานโดยผ่านสถานการณ์จำลองในตอนท้ายของหัวข้อนี้ ให้ใช้ค่าข้อมูลสาธิตที่ระบุไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="a8aea-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="a8aea-153">มิฉะนั้น ให้ใช้ค่าของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a8aea-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="a8aea-154">เลือกนิติบุคคล **USMF** เพื่อทำงานกับข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a8aea-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="a8aea-155">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a8aea-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="a8aea-156">ให้เลือก **แก้ไข** เพื่อเปลี่ยนหน้าไปในโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a8aea-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="a8aea-157">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="a8aea-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="a8aea-158">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-158">In the new row, set the following values.</span></span> <span data-ttu-id="a8aea-159">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a8aea-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="a8aea-160">**เท็มเพลตการเติมสินค้า:** _การเติมสินค้าต่ำสุด/สูงสุดของโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="a8aea-161">**คำอธิบาย:** _การเติมสินค้าต่ำสุด/สูงสุดของโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="a8aea-162">**ชนิดการเติมสินค้า:** _ต่ำสุดหรือสูงสุด_</span><span class="sxs-lookup"><span data-stu-id="a8aea-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="a8aea-163">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a8aea-163">Select **Save**.</span></span>
1. <span data-ttu-id="a8aea-164">ในขณะที่แถวใหม่ยังคงถูกเลือกในกริด **ภาพรวม** ให้เลือก **สร้าง** ข้างบนกริด **รายละเอียดเท็มเพลตการเติมสินค้า** เพื่อเพิ่มแถวที่เชื่อมโยงกับเท็มเพลตการเติมสินค้า *เท็มเพลตการเติมสินค้าต่ำสุด/สูงสุดของโซน* ที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a8aea-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="a8aea-165">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-166">**หมายเลขลำดับ:** ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="a8aea-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="a8aea-167">**คำอธิบาย:** ป้อน _การเติมสินค้าของโซนการเบิกสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="a8aea-168">**หน่วยการเติมสินค้า:** เลือก _ชิ้น_</span><span class="sxs-lookup"><span data-stu-id="a8aea-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="a8aea-169">**ชนิดคำขอ:** ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="a8aea-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="a8aea-170">**รหัสคำสั่ง:** ฟิลด์นี้เชื่อมโยงเท็มเพลตการเติมสินค้ากับคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="a8aea-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="a8aea-171">เลือกรหัสคำสั่งข้อมูลสาธิตที่คุณสร้างไว้ก่อนหน้านี้ (_การเติมสินค้าของโซน_)</span><span class="sxs-lookup"><span data-stu-id="a8aea-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="a8aea-172">**เท็มเพลตงาน** ปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="a8aea-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="a8aea-173">**ปริมาณต่ำสุด:** ฟิลด์นี้จะตั้งค่าปริมาณที่การเติมสินค้าจะทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="a8aea-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="a8aea-174">ป้อน _50_</span><span class="sxs-lookup"><span data-stu-id="a8aea-174">Enter _50_.</span></span>
    - <span data-ttu-id="a8aea-175">**ปริมาณสูงสุด:** ฟิลด์นี้จะตั้งค่าปริมาณสูงสุดของสินค้าที่สามารถแสดงในโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="a8aea-176">งานการเติมสินค้าที่สร้างขึ้นจะเพิ่มสินค้าคงคลังในปริมาณนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="a8aea-177">ป้อน _150_</span><span class="sxs-lookup"><span data-stu-id="a8aea-177">Enter _150_.</span></span>
    - <span data-ttu-id="a8aea-178">**หน่วย:** ฟิลด์นี้จะตั้งค่าหน่วยสำหรับค่าต่ำสุดและสูงสุด</span><span class="sxs-lookup"><span data-stu-id="a8aea-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="a8aea-179">เลือก _ชิ้น_</span><span class="sxs-lookup"><span data-stu-id="a8aea-179">Select _ea_.</span></span>
    - <span data-ttu-id="a8aea-180">**การเพิ่มความต้องการ:** เลือก _ปัดเศษขึ้น_</span><span class="sxs-lookup"><span data-stu-id="a8aea-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="a8aea-181">**เติมสินค้าในสถานที่คงที่ที่ว่างเปล่า:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="a8aea-182">**เติมสินค้าเฉพาะในสถานที่คงที่:** ล้างกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-183">**โหมดการสอบถามผลิตภัณฑ์:** เลือก _การสอบถามผลิตภัณฑ์_</span><span class="sxs-lookup"><span data-stu-id="a8aea-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="a8aea-184">**ขอบเขตขีดจำกัดการเติมสินค้า:** ฟิลด์นี้กำหนดว่าเท็มเพลตจะประเมินตามโซนหรือตามสถานที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a8aea-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="a8aea-185">เลือก _โซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-185">Select _Zone_.</span></span>
    - <span data-ttu-id="a8aea-186">**คลังสินค้า:** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="a8aea-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="a8aea-187">เลือก **เลือกผลิตภัณฑ์** ที่อยู่ด้านบนกริด **รายละเอียดเท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a8aea-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="a8aea-188">ในกล่องโต้ตอบ **การสอบถามผลิตภัณฑ์** บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-189">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-190">**ตาราง:** _สินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="a8aea-191">**ตารางสืบทอด:** _สินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="a8aea-192">**ฟิลด์:** _Iหมายเลขสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="a8aea-193">**เกณฑ์:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="a8aea-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="a8aea-194">เลือก **ตกลง** เพื่อบันทึกการสอบถามของคุณและปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="a8aea-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="a8aea-195">เลือก **เลือกโซนที่จะเติมสินค้า** ที่อยู่ด้านบนกริด **รายละเอียดเท็มเพลตการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a8aea-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="a8aea-196">ในกล่องโต้ตอบ **การสอบถามโซน** บนแท็บ **ช่วง** เพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-197">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-198">**ตาราง:** _โซนคลังสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="a8aea-199">**ตารางสืบทอด:** _โซนคลังสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="a8aea-200">**ฟิลด์:** _รหัสโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="a8aea-201">**เกณฑ์:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="a8aea-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="a8aea-202">เลือก **ตกลง** เพื่อบันทึกการสอบถามของคุณและปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="a8aea-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="a8aea-203">ตั้งค่าคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="a8aea-203">Set up location directives</span></span>

<span data-ttu-id="a8aea-204">ซึ่งแตกต่างจากการเติมสินค้าต่ำสุด/สูงสุดตามสถานที่ การเติมสินค้าต่ำสุด/สูงสุดตามโซนต้องการให้คุณตั้งค่าทั้งคำสั่งสถานที่เบิกสินค้าและคำสั่งสถานที่เก็บสำรอง เนื่องจากระบบจะตรวจสอบโซนทั้งหมด แทนที่จะตรวจสอบเฉพาะสถานที่เบิกสินค้าสำหรับงานขาออก</span><span class="sxs-lookup"><span data-stu-id="a8aea-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="a8aea-205">ดูและแก้ไขคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="a8aea-205">View and edit location directives</span></span>

<span data-ttu-id="a8aea-206">เมื่อต้องการดูหรือแก้ไขคำสั่งสถานที่ของคุณ ให้ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="a8aea-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="a8aea-207">สำหรับตัวอย่างที่แสดงวิธีใช้การตั้งค่าเพื่อสร้างคำสั่งสถานที่เบิกสินค้าและสถานที่เก็บสำรองที่ต้องการ ให้ดูที่ส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a8aea-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="a8aea-208">จัดเตรียมคำสั่งสถานที่ของข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a8aea-208">Prepare demo data location directives</span></span>

<span data-ttu-id="a8aea-209">เมื่อต้องการจัดเตรียมข้อมูลสาธิตเพื่อให้สามารถใช้ในสถานการณ์ที่ส่วนท้ายของหัวข้อนี้ คุณต้องสร้างคำสั่งสถานที่สองคำสั่งนี้: หนึ่งคำสั่งสำหรับการเบิกสินค้า และหนึ่งคำสั่งสำหรับการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="a8aea-210">สร้างคำสั่งการเบิกสินค้าสำหรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="a8aea-211">เลือกนิติบุคคล **USMF** เพื่อทำงานกับข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="a8aea-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="a8aea-212">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="a8aea-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a8aea-213">ในบานหน้าต่างด้านซ้าย ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น _การเติมสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="a8aea-214">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคำสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="a8aea-215">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-215">Set the following values:</span></span>

    - <span data-ttu-id="a8aea-216">**หมายเลขลำดับ:** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a8aea-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="a8aea-217">**ชื่อ:** ป้อน _การเบิกสินค้าตามโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="a8aea-218">**ชนิดงาน:** เลือก _เบิกสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="a8aea-219">**ไซต์:** เลือก _6_</span><span class="sxs-lookup"><span data-stu-id="a8aea-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="a8aea-220">**คลังสินค้า:** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="a8aea-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="a8aea-221">**รหัสคำสั่ง:** ให้ปล่อยฟิลด์นี้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="a8aea-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="a8aea-222">**SKU ที่หลากหลาย:** กำหนดตัวเลือกนี้เป็น _ไม่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="a8aea-223">เลือก **บันทึก** เพื่อสร้างคำสั่งที่มีการตั้งค่าที่คุณตั้งค่าคอนฟิกจนถึงขณะนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="a8aea-224">บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a8aea-225">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a8aea-226">**หมายเลขลำดับ:** ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="a8aea-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="a8aea-227">**ปริมาณเริ่มต้น:** ป้อน _0_</span><span class="sxs-lookup"><span data-stu-id="a8aea-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="a8aea-228">**ปริมาณสิ้นสุด:** ป้อน _10000000_</span><span class="sxs-lookup"><span data-stu-id="a8aea-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="a8aea-229">**หน่วย:** ให้ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="a8aea-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="a8aea-230">**ค้นหาปริมาณ:** เลือก _ไม่มี_</span><span class="sxs-lookup"><span data-stu-id="a8aea-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="a8aea-231">**จำกัดตามหน่วย:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-232">**ปัดเศษขึ้นเป็นหน่วย:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-233">**ระบุตำแหน่งปริมาณการบรรจุ:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-234">**อนุญาตการแบ่ง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="a8aea-235">เลือก **บันทึก** เพื่อบันทึกรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="a8aea-236">ในขณะที่รายการใหม่ของคุณยังคงถูกเลือกอยู่ในกริด **รายการ** ให้เลือก **สร้าง** บน FastTab **การดำเนินการของคำสั่งสถานที่** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-237">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-238">**หมายเลขลำดับ:** ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="a8aea-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="a8aea-239">**ชื่อ:** ป้อน _เบิกสินค้าจากกลุ่ม_</span><span class="sxs-lookup"><span data-stu-id="a8aea-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="a8aea-240">**การใช้งานสถานที่คงที่:** เลือก _สถานที่คงที่และไม่คงที่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="a8aea-241">**อนุญาตสินค้าคงคลังค่าลบ:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-242">**เปิดใช้งานชุดงาน:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-243">**กลยุทธ์:** เลือก _ไม่มี_</span><span class="sxs-lookup"><span data-stu-id="a8aea-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="a8aea-244">เลือก **บันทึก** เพื่อบันทึกการดำเนินการใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="a8aea-245">ในขณะที่การดำเนินการใหม่ของคุณยังคงถูกเลือกอยู่ ให้เลือก **แก้ไขการสอบถาม** ด้านบนกริด **การดำเนินการคำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="a8aea-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="a8aea-246">กล่องโต้ตอบการสอบถามจะปรากฏขึ้น ซึ่งคุณสามารถเลือกสถานที่ที่จะเติมสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="a8aea-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="a8aea-247">บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-248">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-249">**ตาราง:** _สถานที่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="a8aea-250">**ตารางสืบทอด:** _สถานที่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="a8aea-251">**ฟิลด์:** _รหัสโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="a8aea-252">**เกณฑ์:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="a8aea-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="a8aea-253">เลือก **ตกลง** เพื่อบันทึกการสอบถามของคุณและปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="a8aea-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="a8aea-254">เลือก **บันทึก** เพื่อบันทึกคำสั่งสถานที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8aea-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="a8aea-255">สร้างคำสั่งการสำรองสินค้าสำหรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="a8aea-256">บนหน้า **คำสั่งสถานที่** ในบานหน้าต่างด้านซ้าย ให้ตรวจสอบให้แน่ใจว่าฟิลด์ **ชนิดของใบสั่งงาน** ยังคงถูกตั้งค่าเป็น _การเติมสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="a8aea-257">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคำสั่งใหม่อีกรายการหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a8aea-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="a8aea-258">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-258">Set the following values:</span></span>

    - <span data-ttu-id="a8aea-259">**หมายเลขลำดับ:** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a8aea-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="a8aea-260">**ชื่อ:** ป้อน _การสำรองสินค้าตามโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="a8aea-261">**ชนิดของใบสั่งงาน:** เลือก _การสำรองสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="a8aea-262">**ไซต์:** เลือก _6_</span><span class="sxs-lookup"><span data-stu-id="a8aea-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="a8aea-263">**คลังสินค้า:** เลือก _61_</span><span class="sxs-lookup"><span data-stu-id="a8aea-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="a8aea-264">**รหัสคำสั่ง:** เลือก _การเติมสินค้าตามโซน_ เพื่อเชื่อมโยงคำสั่งสถานที่นี้กับเท็มเพลตการเติมสินค้าที่คุณสร้างไว้ก่อนหน้านี้โดยใช้รหัสที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="a8aea-265">**SKU ที่หลากหลาย:** กำหนดตัวเลือกนี้เป็น _ไม่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="a8aea-266">เลือก **บันทึก** เพื่อสร้างคำสั่งที่มีการตั้งค่าที่คุณตั้งค่าคอนฟิกจนถึงขณะนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="a8aea-267">บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a8aea-268">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a8aea-269">**หมายเลขลำดับ:** ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="a8aea-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="a8aea-270">**ปริมาณเริ่มต้น:** ป้อน _0_</span><span class="sxs-lookup"><span data-stu-id="a8aea-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="a8aea-271">**ปริมาณสิ้นสุด:** ป้อน _10000000_</span><span class="sxs-lookup"><span data-stu-id="a8aea-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="a8aea-272">**หน่วย:** ให้ปล่อยฟิลด์นี้ให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="a8aea-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="a8aea-273">**ค้นหาปริมาณ:** เลือก _ไม่มี_</span><span class="sxs-lookup"><span data-stu-id="a8aea-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="a8aea-274">**จำกัดตามหน่วย:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-275">**ปัดเศษขึ้นเป็นหน่วย:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-276">**ระบุตำแหน่งปริมาณการบรรจุ:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-277">**อนุญาตการแบ่ง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="a8aea-278">เลือก **บันทึก** เพื่อบันทึกรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="a8aea-279">ในขณะที่รายการใหม่ของคุณยังคงถูกเลือกอยู่ในกริด **รายการ** ให้เลือก **สร้าง** บน FastTab **การดำเนินการของคำสั่งสถานที่** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-280">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-281">**หมายเลขลำดับ:** ป้อน _1_</span><span class="sxs-lookup"><span data-stu-id="a8aea-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="a8aea-282">**ชื่อ:** ป้อน _การสำรองสินค้าตามโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="a8aea-283">**การใช้งานสถานที่คงที่:** เลือก _สถานที่คงที่และไม่คงที่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="a8aea-284">**อนุญาตสินค้าคงคลังค่าลบ:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-285">**เปิดใช้งานชุดงาน:** ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="a8aea-286">**กลยุทธ์:** เลือก _รวมบัญชี_</span><span class="sxs-lookup"><span data-stu-id="a8aea-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="a8aea-287">เลือก **บันทึก** เพื่อบันทึกการดำเนินการใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="a8aea-288">ในขณะที่การดำเนินการใหม่ของคุณยังคงถูกเลือกอยู่ ให้เลือก **แก้ไขการสอบถาม** ด้านบนกริด **การดำเนินการคำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="a8aea-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="a8aea-289">กล่องโต้ตอบการสอบถามจะปรากฏขึ้น ที่ซึ่งคุณสามารถเลือกโซนที่จะเติมสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="a8aea-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="a8aea-290">โซนนี้ควรเป็นโซนเดียวกันกับที่ระบุไว้ในเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="a8aea-291">บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="a8aea-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="a8aea-292">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="a8aea-293">**ตาราง:** _สถานที่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="a8aea-294">**ตารางสืบทอด:** _สถานที่_</span><span class="sxs-lookup"><span data-stu-id="a8aea-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="a8aea-295">**ฟิลด์:** _รหัสโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="a8aea-296">**เกณฑ์:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="a8aea-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="a8aea-297">เลือก **ตกลง** เพื่อบันทึกการสอบถามของคุณและปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="a8aea-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="a8aea-298">เลือก **บันทึก** เพื่อบันทึกคำสั่งสถานที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8aea-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="a8aea-299">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="a8aea-299">Scenario</span></span>

<span data-ttu-id="a8aea-300">ส่วนนี้แสดงสถานการณ์จำลองตัวอย่างที่แสดงวิธีการทำงานกับคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="a8aea-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="a8aea-301">จัดเตรียมข้อมูลตัวอย่างที่จำเป็นสำหรับสถานการณ์จำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a8aea-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="a8aea-302">ก่อนที่คุณจะเริ่มทำงานในสถานการณ์สมมติ คุณต้องเรียกใช้ข้อมูลตัวอย่างและตั้งค่าคุณลักษณะตามที่อธิบายไว้ในส่วนนี้ และในส่วนก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="a8aea-303">ใช้นิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="a8aea-303">Use the USMF legal entity</span></span>

<span data-ttu-id="a8aea-304">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="a8aea-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a8aea-305">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a8aea-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="a8aea-306">จัดเตรียมข้อมูลตัวอย่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a8aea-306">Prepare additional sample data</span></span>

<span data-ttu-id="a8aea-307">หลังจากที่คุณเลือกนิติบุคคล **USMF** เพิ่มข้อมูลตัวอย่างเพิ่มเติมที่จำเป็น ตามที่อธิบายไว้ในส่วน [ตั้งค่าการเติมสินค้าตามโซน](#setup) ก่อนหน้าในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="a8aea-308">ตรวจสอบปริมาณคงคลังคงเหลือของคุณ</span><span class="sxs-lookup"><span data-stu-id="a8aea-308">Check your on-hand inventory</span></span>

<span data-ttu-id="a8aea-309">ทำตามขั้นตอนเหล่านี้เพื่อตรวจสอบให้แน่ใจว่าระบบของคุณมีสินค้าคงคลังที่เพียงพอสำหรับสนับสนุนสถานการณ์จำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a8aea-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="a8aea-310">ตรวจสอบให้แน่ใจว่ามีปริมาณคงคลังคงเหลือสำหรับสินค้า *A0001* ที่สถานที่สองแห่งในโซนการเบิกสินค้า (*FLOOR*) ที่ระบุในเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="a8aea-311">อย่างไรก็ตาม สินค้าคงคลังทั้งหมดควรน้อยกว่าปริมาณต่ำสุดที่กำหนด (*50*) ที่ระบุไว้ในเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="a8aea-312">ด้วยวิธีนี้ คุณสามารถจำลองวิธีที่การคำนวณเกิดขึ้นสำหรับทั้งโซน แทนที่จะเป็นสำหรับสถานที่เดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a8aea-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="a8aea-313">**ใช้กระบวนการคลังสินค้าใดๆ เพื่อปรับปรุงสินค้าคงคลังตามต้องการ**</span><span class="sxs-lookup"><span data-stu-id="a8aea-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="a8aea-314">ตรวจสอบให้แน่ใจว่ามีสินค้าคงคลังที่เพียงพอสำหรับสินค้า *A0001* ที่สถานที่เก็บสินค้าจำนวนมากที่ระบุไว้ในคำสั่งสถานที่ของการเบิกสินค้าตามโซน ซึ่งงานการเติมสินค้าควรเบิกสินค้าจากรหัสโซน *BULK*</span><span class="sxs-lookup"><span data-stu-id="a8aea-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="a8aea-315">สินค้าคงคลังทั้งหมดต้องมากกว่าปริมาณสูงสุดที่กำหนด (*150*) ที่ระบุไว้ในเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="a8aea-316">ไม่จำเป็นต้องระบุ แต่แนะนำ: ให้ทำตามขั้นตอนเหล่านี้เพื่อสร้างสมุดรายวันการปรับปรุงสินค้าคงคลัง:</span><span class="sxs-lookup"><span data-stu-id="a8aea-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="a8aea-317">ไปที่ **การจัดการสินค้าคงคลัง \> รายการสมุดบันทึกรายวัน \> สินค้า \> การปรับปรุงสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="a8aea-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="a8aea-318">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a8aea-318">Select **New**.</span></span>
    1. <span data-ttu-id="a8aea-319">ในกล่องโต้ตอบ **สร้างสมุดรายวันสินค้าคงคลัง** ในฟิลด์ **คลังสินค้า** ให้เลือก *61*</span><span class="sxs-lookup"><span data-stu-id="a8aea-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="a8aea-320">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a8aea-320">Select **OK**.</span></span>
    1. <span data-ttu-id="a8aea-321">บน FastTab **รายการสมุดรายวัน** ให้ใช้ปุ่ม **สร้าง** เพื่อเพิ่มรายการสามรายการไปยังกริด และตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="a8aea-322">หลังจากที่คุณตั้งค่าแต่ละรายการเสร็จแล้ว ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a8aea-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="a8aea-323">**รายการที่ 1:**</span><span class="sxs-lookup"><span data-stu-id="a8aea-323">**Line 1:**</span></span>

            - <span data-ttu-id="a8aea-324">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a8aea-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="a8aea-325">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="a8aea-325">**Site:** *6*</span></span>
            - <span data-ttu-id="a8aea-326">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="a8aea-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="a8aea-327">**สถานที่:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="a8aea-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="a8aea-328">**ป้ายทะเบียน:** เลือกป้ายทะเบียนที่มีอยู่ในรายการ หรือสร้างป้ายทะเบียนใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="a8aea-329">**ปริมาณ:** *1000*</span><span class="sxs-lookup"><span data-stu-id="a8aea-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="a8aea-330">**รายการที่ 2:**</span><span class="sxs-lookup"><span data-stu-id="a8aea-330">**Line 2:**</span></span>

            - <span data-ttu-id="a8aea-331">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a8aea-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="a8aea-332">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="a8aea-332">**Site:** *6*</span></span>
            - <span data-ttu-id="a8aea-333">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="a8aea-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="a8aea-334">**สถานที่:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="a8aea-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="a8aea-335">**ป้ายทะเบียน:** เลือกป้ายทะเบียนที่มีอยู่ในรายการ หรือสร้างป้ายทะเบียนใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="a8aea-336">**ปริมาณ:** *15*</span><span class="sxs-lookup"><span data-stu-id="a8aea-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="a8aea-337">**รายการที่ 3:**</span><span class="sxs-lookup"><span data-stu-id="a8aea-337">**Line 3:**</span></span>

            - <span data-ttu-id="a8aea-338">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a8aea-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="a8aea-339">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="a8aea-339">**Site:** *6*</span></span>
            - <span data-ttu-id="a8aea-340">**คลังสินค้า:** *61*</span><span class="sxs-lookup"><span data-stu-id="a8aea-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="a8aea-341">**สถานที่:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="a8aea-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="a8aea-342">**ป้ายทะเบียน:** เลือกป้ายทะเบียนที่มีอยู่ในรายการ หรือสร้างป้ายทะเบียนใหม่</span><span class="sxs-lookup"><span data-stu-id="a8aea-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="a8aea-343">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="a8aea-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="a8aea-344">บนบานหน้าต่างการดำเนินการ เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="a8aea-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="a8aea-345">แก้ไขข้อผิดพลาดใดๆ ที่พบ ก่อนที่คุณจะไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a8aea-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="a8aea-346">ในบานหน้าต่างการดำเนินการ ให้เลือก **ลงรายการบัญชี** เพื่อลงรายการบัญชีไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="a8aea-347">สถานการณ์จำลองตัวอย่าง: รันการเติมสินค้าต่ำสุด/สูงสุดตามโซน</span><span class="sxs-lookup"><span data-stu-id="a8aea-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="a8aea-348">หลังจากที่มีข้อมูลตัวอย่างของข้อกำหนดเบื้องต้นทั้งหมด คุณสามารถทริกเกอร์การเติมสินค้าโดยปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="a8aea-349">ไปที่ **การจัดการคลังสินค้า \> การเติมสินค้า \> การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a8aea-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="a8aea-350">ในกล่องโต้ตอบ **การเติมสินค้า** บน FastTab **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="a8aea-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="a8aea-351">ในกล่องโต้ตอบ **การสอบถาม** บนแท็บ **ช่วง** ให้แก้ไขแถวของตารางเริ่มต้นในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="a8aea-352">**ตาราง:** เลือก _เท็มเพลตการเติมสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="a8aea-353">**ตารางสืบทอด:** เลือก _เท็มเพลตการเติมสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="a8aea-354">**ฟิลด์:** เลือก _เท็มเพลตการเติมสินค้า_</span><span class="sxs-lookup"><span data-stu-id="a8aea-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="a8aea-355">**เกณฑ์:** เลือก _การเติมสินค้าต่ำสุด/สูงสุดตามโซน_</span><span class="sxs-lookup"><span data-stu-id="a8aea-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="a8aea-356">เท็มเพลตการเติมสินค้านี้เป็นเท็มเพลตการเติมสินค้าที่คุณสร้างขึ้นในขณะที่คุณกำลังเตรียมข้อมูลสาธิตสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="a8aea-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="a8aea-357">เลือก **ตกลง** เพื่อบันทึกการสอบถาม และกลับไปยังกล่องโต้ตอบ **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="a8aea-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="a8aea-358">เลือก **ตกลง** เพื่อรันเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a8aea-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="a8aea-359">ขณะนี้งานการเติมสินค้าจะถูกสร้างขึ้นเพื่อเบิกสินค้าในสินค้าคงคลังจากโซน *BULK* และเติมสินค้าไปยังโซน *FLOOR*</span><span class="sxs-lookup"><span data-stu-id="a8aea-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="a8aea-360">หมายเหตุและเคล็ดลับ</span><span class="sxs-lookup"><span data-stu-id="a8aea-360">Notes and tips</span></span>

<span data-ttu-id="a8aea-361">ต่อไปนี้เป็นหมายเหตุและเคล็ดลับบางประการสำหรับการทำงานกับคุณลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="a8aea-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="a8aea-362">เมื่อต้องการตั้งค่างานการเติมสินค้าที่จะไปยังโซนที่ต้องการ คุณสามารถเชื่อมโยงรายการเท็มเพลตการเติมสินค้าและคำสั่งสถานที่ในวิธีใดวิธีหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a8aea-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="a8aea-363">แก้ไขการสอบถามส่วนหัวของคำสั่งของสถานที่ และกรองรายการเท็มเพลตการเติมสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a8aea-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="a8aea-364">ใช้คำสั่งสถานที่ในรายการเท็มเพลตการเติมสินค้า และจับคู่กับคำสั่งสถานที่เก็บสำรอง</span><span class="sxs-lookup"><span data-stu-id="a8aea-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="a8aea-365">ถ้าคุณกำลังใช้สถานที่แบบไดนามิก งานการเติมสินค้าจะถูกสร้างขึ้นสำหรับสถานที่ที่พร้อมใช้งานแรก หรือสำหรับสถานที่ที่มีสินค้าคงคลังอยู่แล้ว ถ้ามีการตั้งค่าการดำเนินการคำสั่งสถานที่เพื่อใช้กลยุทธ์ **รวมบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a8aea-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="a8aea-366">ถ้าคุณกำลังใช้สถานที่คงที่ แทนที่จะเป็นโซน คุณควรใช้ [การเติมสินค้าต่ำสุด/สูงสุดมาตรฐาน](tasks/set-up-min-max-replenishment-process.md)</span><span class="sxs-lookup"><span data-stu-id="a8aea-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]