---
title: การจัดลำดับงานที่สั่งการโดยระบบ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการจัดลำดับงานที่สั่งการโดยระบบ ฟังก์ชันนี้ช่วยให้คุณสามารถเรียงลำดับและกรองข้อมูลใบสั่งงานที่ระบบนำเสนอให้กับผู้ใช้สำหรับการดำเนินการ ซึ่งมีประโยชน์ในกรณีที่ต้องใช้เงื่อนไขเพิ่มเติมเพื่อขับเคลื่อนกระบวนการเบิกสินค้าของคลังสินค้า
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5387aaf5a5e0d20ac22595fbea86a25fdf38a771
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831133"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="56052-105">การจัดลำดับงานที่สั่งการโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="56052-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56052-106">การจัดลำดับงานที่สั่งการโดยระบบช่วยให้คุณสามารถเรียงลำดับและกรองข้อมูลใบสั่งงานที่ระบบนำเสนอให้กับผู้ใช้สำหรับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="56052-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="56052-107">ซึ่งมีประโยชน์ในกรณีที่เงื่อนไขเพิ่มเติม (เช่น เวลาของการจัดส่ง โซนการเบิกสินค้า โพรไฟล์สถานที่ หรือการรวมกันของเงื่อนไขต่างๆ) จำเป็นต้องใช้ในการขับเคลื่อนกระบวนการเบิกสินค้าของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="56052-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="56052-108">ฟังก์ชันนี้จะขยายฟังก์ชันการเบิกสินค้าที่สั่งการโดยระบบปัจจุบันโดยการเพิ่มใบสั่งการสอบถามที่สั่งการโดยระบบ ซึ่งผู้ใช้สามารถตั้งค่าลำดับและการสอบถามอย่างน้อยหนึ่งรายการที่จะประเมินใบสั่งงานทั้งหมดที่ถูกสร้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="56052-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="56052-109">เฉพาะใบสั่งงานที่ตรงกับเกณฑ์ที่ระบุไว้ในการตั้งค่าของรายการเมนูของอุปกรณ์เคลื่อนที่เท่านั้นที่จะถูกบันทึกและนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="56052-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="56052-110">ดังนั้น ฟังก์ชันนี้ช่วยให้สามารถเพิ่มประสิทธิภาพของกระบวนการเบิกสินค้าในคลังสินค้าตามที่ระบุใบสั่งงานที่ตรงกับเกณฑ์ที่ระบุ กำหนดให้กับรายการเมนูของอุปกรณ์เคลื่อนที่ที่ถูกต้อง แล้วจากนั้น นำเสนอให้กับผู้ปฏิบัติงานตามชุดทักษะที่ระบุ อุปกรณ์การเบิกสินค้า หรือความต้องการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="56052-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="56052-111">ถ้าต้องใช้เงื่อนไขที่แตกต่างกัน จะต้องใช้รายการเมนูของอุปกรณ์เคลื่อนที่หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="56052-112">เปิดคุณลักษณะการจัดลำดับงานที่สั่งการโดยระบบแบบทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="56052-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="56052-113">ก่อนที่คุณจะสามารถใช้การจัดลำดับงานที่สั่งการโดยระบบ คุณลักษณะต้องเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="56052-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="56052-114">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="56052-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="56052-115">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="56052-116">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="56052-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="56052-117">**ชื่อคุณลักษณะ:** *การจัดลำดับงานที่สั่งการโดยระบบแบบทั่วทั้งองค์กร*</span><span class="sxs-lookup"><span data-stu-id="56052-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="56052-118">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="56052-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="56052-119">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="56052-119">Make demo data available</span></span>

<span data-ttu-id="56052-120">เมื่อต้องการดำเนินการสถานการณ์โดยใช้ค่าที่แสดงในหัวข้อนี้ คุณต้องทำงานในระบบที่มีการติดตั้งข้อมูลสาธิตมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="56052-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="56052-121">นอกจากนี้ คุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="56052-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="56052-122">สถานการณ์จำลองใช้คลังสินค้า *51* จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="56052-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56052-123">ก่อนที่คุณจะนำใบสั่งออกใช้กับคลังสินค้า ต้องตรวจสอบให้แน่ใจว่าสถานที่เบิกสินค้ามีสินค้าคงคลังเพียงพอสำหรับสินค้าทั้งหมดในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="56052-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="56052-124">ข้อมูล USMF เริ่มต้นควรสนับสนุนสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="56052-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="56052-125">ถ้าคุณไม่ได้ใช้ข้อมูลสาธิต ตรวจทานการตั้งค่า **คำสั่งสถานที่** เพื่อเรียนรู้สถานที่เบิกสินค้าที่จะใช้สำหรับการเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="56052-126">ถ้าคุณต้องปรับปรุงสินค้าคงคลัง คุณสามารถสร้างการเคลื่อนไหวด้วยตนเอง ใช้การเติมสินค้า หรือใช้โฟลว์อื่นใดๆ</span><span class="sxs-lookup"><span data-stu-id="56052-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="56052-127">ตั้งค่ารายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="56052-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="56052-128">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="56052-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="56052-129">ในรายการของรายการเมนูของอุปกรณ์เคลื่อนที่ เลือก **การเบิกสินค้าขาย – ระบบ**</span><span class="sxs-lookup"><span data-stu-id="56052-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="56052-130">รายการเมนูที่จำเป็นควรมีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="56052-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="56052-131">ยืนยันการตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="56052-132">บน FastTab **ทั่วไป** ควรตั้งค่าฟิลด์ **สั่งการโดย** เป็น *สั่งการโดยระบบ*</span><span class="sxs-lookup"><span data-stu-id="56052-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="56052-133">FastTab **คลาสงาน** ควรแสดงการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="56052-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="56052-134">รหัสคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="56052-134">Work class ID</span></span> | <span data-ttu-id="56052-135">ชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="56052-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="56052-136">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-136">Sales</span></span> | <span data-ttu-id="56052-137">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-137">Sales orders</span></span> |
        | <span data-ttu-id="56052-138">การเบิกสินค้า SO</span><span class="sxs-lookup"><span data-stu-id="56052-138">SO Pick</span></span> | <span data-ttu-id="56052-139">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-139">Sales orders</span></span> |

1. <span data-ttu-id="56052-140">ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถามลำดับงานที่สั่งการโดยระบบ**</span><span class="sxs-lookup"><span data-stu-id="56052-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="56052-141">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="56052-141">Select **Edit**.</span></span>
1. <span data-ttu-id="56052-142">ลบรายการที่มีอยู่ แล้วจากนั้น ยืนยันการดำเนินการโดยเลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="56052-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="56052-143">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="56052-144">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="56052-145">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="56052-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="56052-146">**ฟิลด์คำอธิบาย:** *ปริมาณงานน้อยกว่า 20 และจากมากไปน้อย*</span><span class="sxs-lookup"><span data-stu-id="56052-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="56052-147">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="56052-147">Select **Save**.</span></span>
1. <span data-ttu-id="56052-148">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="56052-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="56052-149">บนแท็บ **เข้าร่วม** ขยายลำดับชั้นการเข้าร่วมเพื่อแสดงตาราง **รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="56052-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="56052-150">เลือกตาราง **รายการงาน** เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="56052-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="56052-151">เลือก **เพิ่มการรวมตาราง**</span><span class="sxs-lookup"><span data-stu-id="56052-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="56052-152">ในรายการที่ปรากฏขึ้น ให้ค้นหาและเลือกแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="56052-153">**โหมดเข้าร่วม:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="56052-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="56052-154">**ความสัมพันธ์:** *สถานที่ (สถานที่)*</span><span class="sxs-lookup"><span data-stu-id="56052-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="56052-155">เลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="56052-155">Select **Select**.</span></span>

    <span data-ttu-id="56052-156">สถานที่จะถูกเพิ่มเข้าในตารางเข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="56052-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="56052-157">บนแท็บ **การเรียงลำดับ** ให้เลือก **เพิ่ม** เพื่อเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="56052-158">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="56052-159">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="56052-160">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="56052-161">**ฟิลด์:** *ปริมาณงาน* (ในกล่องข้อความที่ปรากฏขึ้น ให้เลือก **ใช่** เพื่อเพิ่มการเรียงลำดับไปยังฟิลด์นี้)</span><span class="sxs-lookup"><span data-stu-id="56052-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="56052-162">**ทิศทางการค้นหา:** *การเรียงจากมากไปน้อย*</span><span class="sxs-lookup"><span data-stu-id="56052-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="56052-163">เลือกแท็บ **ช่วง**</span><span class="sxs-lookup"><span data-stu-id="56052-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="56052-164">ถ้าควรรวมเฉพาะเกณฑ์ของงานในการจัดลำดับ คุณสามารถระบุได้บนแท็บ **ช่วง** ในตัวอย่างนี้คุณต้องการรวมเฉพาะงานที่มีปริมาณน้อยกว่า 20 รายการ (หน่วยวัดต่ำสุด)</span><span class="sxs-lookup"><span data-stu-id="56052-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="56052-165">โปรดสังเกตว่าบางรายการถูกรวมอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="56052-165">Notice that some lines are already included.</span></span> <span data-ttu-id="56052-166">ไม่ควรลบรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="56052-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="56052-167">เลือก **เพิ่ม** เพื่อเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="56052-168">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="56052-169">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="56052-170">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="56052-171">**ฟิลด์:** *ปริมาณงานของสินค้าคงคลัง*</span><span class="sxs-lookup"><span data-stu-id="56052-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="56052-172">**เงื่อนไข:** *\<20* (น้อยกว่า 20)</span><span class="sxs-lookup"><span data-stu-id="56052-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="56052-173">เลือก **เพิ่ม** เพื่อเพิ่มรายการอื่น</span><span class="sxs-lookup"><span data-stu-id="56052-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="56052-174">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="56052-175">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="56052-176">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="56052-177">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="56052-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="56052-178">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="56052-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="56052-179">เลือก **เพิ่ม** เพื่อเพิ่มรายการอื่น</span><span class="sxs-lookup"><span data-stu-id="56052-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="56052-180">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="56052-181">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="56052-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="56052-182">**ตารางสืบทอด:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="56052-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="56052-183">**ฟิลด์:** *รหัสโพรไฟล์สถานที่*</span><span class="sxs-lookup"><span data-stu-id="56052-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="56052-184">**เงื่อนไข:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="56052-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="56052-185">ตรวจสอบให้แน่ใจว่าได้รวมเครื่องหมายอัศเจรีย์ (*!*) อยู่ด้านหน้าของ *STAGE*</span><span class="sxs-lookup"><span data-stu-id="56052-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="56052-186">เลือก **ตกลง** เพื่อบันทึกและปิดการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="56052-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="56052-187">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="56052-187">Select **Save**.</span></span>
1. <span data-ttu-id="56052-188">ปิดหน้าเพื่อกลับไปที่หน้า **รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="56052-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="56052-189">การตั้งค่านี้จะกำหนดเกณฑ์ที่จะใช้ในการให้ฟีดงานที่มีสิทธิ์ไปยังรายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="56052-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="56052-190">ถ้าคุณเพิ่มรายการเงื่อนไขเพิ่มเติมลงในการสอบถาม ระบบจะใช้รายการการสอบถามที่มีหมายเลขลำดับต่ำสุดเป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="56052-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="56052-191">กล่าวคือ งานที่มีสิทธิ์ทั้งหมดสำหรับหมายเลขลำดับ 1 จะแสดงให้กับผู้ใช้ก่อน แล้วจากนั้น งานทั้งหมดสำหรับลำดับหมายเลข 2</span><span class="sxs-lookup"><span data-stu-id="56052-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="56052-192">ดังนั้น ถ้าต้องใช้ช่วงและการเรียงลำดับที่ระบุร่วมกัน ควรมีการระบุในการสอบถามลำดับงานที่สั่งการโดยระบบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="56052-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="56052-193">การตั้งค่านี้จะบันทึกงานใดๆ ที่มีอย่างน้อยหนึ่งรายการที่มีปริมาณน้อยกว่า 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="56052-194">ดังนั้น ถ้างานมีรายการที่ปริมาณเท่ากับ 20 ชิ้น หรือมากกว่า 20 ชิ้น จะมีผลบังคับใช้ ถ้ามีอย่างน้อยหนึ่งรายการที่ปริมาณน้อยกว่า 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="56052-195">คำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="56052-195">Location directives</span></span>

<span data-ttu-id="56052-196">ถ้าคุณกำลังใช้ข้อมูล Contoso เริ่มต้น การสอบถามสำหรับการดำเนินการคำสั่งสถานที่ไม่จำเป็นต้องมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="56052-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="56052-197">อย่างไรก็ตาม ถ้าต้องการตรวจสอบให้แน่ใจว่าคำสั่งสถานที่จะบันทึกสินค้าในใบสั่งขาย เมื่อคุณใช้คุณลักษณะในสภาพแวดล้อมที่ไม่ใช่ Contoso ให้สร้างคำสั่งสถานที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="56052-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="56052-198">เมื่อต้องการตรวจสอบการตั้งค่าในสภาพแวดล้อมการสาธิต ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="56052-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="56052-199">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="56052-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="56052-200">ในฟิลด์ **ชนิดใบสั่งงาน** เลือก *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="56052-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="56052-201">เลือกคำสั่งสถานที่ที่มีชื่อว่า *51 เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="56052-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="56052-202">บน FastTab **การดำเนินการคำสั่งสถานที่** ให้เลือกรายการสำหรับการดำเนินการ **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="56052-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="56052-203">เลือก **แก้ไขการสอบถาม** เหนือกริด</span><span class="sxs-lookup"><span data-stu-id="56052-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="56052-204">รีวิวการสอบถาม **ช่วง**</span><span class="sxs-lookup"><span data-stu-id="56052-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="56052-205">ค้นหารายการที่ซึ่งฟิลด์ **ฟิลด์** ถูกตั้งค่าเป็น *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="56052-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="56052-206">ตรวจสอบให้แน่ใจว่าฟิลด์ **เงื่อนไข** ว่างเปล่า (นั่นคือ ไม่มีข้อจำกัด)</span><span class="sxs-lookup"><span data-stu-id="56052-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="56052-207">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="56052-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="56052-208">สร้างงานการเบิกสินค้าตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-208">Create sales order picking work</span></span>

<span data-ttu-id="56052-209">ก่อนที่จะรันการเบิกสินค้าที่สั่งการโดยระบบ จะมีการสร้างงานขาออกบางงาน</span><span class="sxs-lookup"><span data-stu-id="56052-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="56052-210">สำหรับสถานการณ์นี้ คุณจะสร้างใบสั่งขายสี่ใบที่ยึดตามการสอบถามลำดับงานที่สั่งการโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="56052-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="56052-211">คุณจะจองปริมาณสินค้าคงคลังสำหรับใบสั่งขายแต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="56052-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="56052-212">ดังนั้น สินค้าคงคลังที่จองไว้จะไม่สามารถถูกดึงมาจากคลังสินค้าสำหรับใบสั่งอื่นๆ ได้ ถ้าไม่มีการยกเลิกการจองสินค้าคงคลัง หรือยกเลิกการจองสินค้าคงคลังบางส่วน</span><span class="sxs-lookup"><span data-stu-id="56052-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="56052-213">จากนั้น คุณจะนำใบสั่งขายแต่ละใบออกใช้ไปที่คลังสินค้าเพื่อสร้างงานขาออก</span><span class="sxs-lookup"><span data-stu-id="56052-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="56052-214">ใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="56052-214">Sales order 1</span></span>

1. <span data-ttu-id="56052-215">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="56052-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="56052-216">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="56052-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="56052-217">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="56052-218">ในส่วน **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-004*</span><span class="sxs-lookup"><span data-stu-id="56052-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="56052-219">ในส่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **คลังสินค้า** เป็น *51*</span><span class="sxs-lookup"><span data-stu-id="56052-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="56052-220">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="56052-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="56052-221">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="56052-222">เพิ่มรายการไปยังใบสั่งขายใหม่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="56052-223">**หมายเลขสินค้า:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="56052-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="56052-224">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="56052-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="56052-225">บนเมนู **สินค้าคงคลัง** ด้านบนกริด ให้เลือก **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="56052-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="56052-226">บนหน้า **การจอง** เลือก **จองล็อต** เพื่อจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="56052-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="56052-227">ปิดหน้า **การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="56052-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="56052-228">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** เลือก **นำออกใช้ไปยังคลังสินค้า** เพื่อสร้างงานสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="56052-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="56052-229">คุณได้รับข้อความที่ให้ข้อมูลที่แสดงรหัสเวฟและรหัสการจัดส่งที่สร้างขึ้นสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="56052-230">ใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="56052-230">Sales order 2</span></span>

1. <span data-ttu-id="56052-231">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="56052-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="56052-232">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="56052-233">**บัญชีลูกค้า:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="56052-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="56052-234">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="56052-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="56052-235">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="56052-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="56052-236">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="56052-237">เพิ่มรายการไปยังใบสั่งขายใหม่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="56052-238">**หมายเลขสินค้า:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="56052-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="56052-239">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="56052-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="56052-240">เลือก **สร้างรายการ** เพื่อเพิ่มรายการที่สอง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="56052-241">**หมายเลขสินค้า:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="56052-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="56052-242">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="56052-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="56052-243">จองสินค้าคงคลังสำหรับทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="56052-244">นำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="56052-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="56052-245">ใบสั่งขาย 3</span><span class="sxs-lookup"><span data-stu-id="56052-245">Sales order 3</span></span>

1. <span data-ttu-id="56052-246">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างใบสั่งขาย 3</span><span class="sxs-lookup"><span data-stu-id="56052-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="56052-247">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="56052-248">**บัญชีลูกค้า:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="56052-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="56052-249">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="56052-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="56052-250">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="56052-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="56052-251">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="56052-252">เพิ่มรายการไปยังใบสั่งขายใหม่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="56052-253">**หมายเลขสินค้า:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="56052-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="56052-254">**ปริมาณ:** *7*</span><span class="sxs-lookup"><span data-stu-id="56052-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="56052-255">เลือก **สร้างรายการ** เพื่อเพิ่มรายการที่สอง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="56052-256">**หมายเลขสินค้า:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="56052-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="56052-257">**ปริมาณ:** *8*</span><span class="sxs-lookup"><span data-stu-id="56052-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="56052-258">จองสินค้าคงคลังสำหรับทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="56052-259">นำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="56052-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="56052-260">ใบสั่งขาย 4</span><span class="sxs-lookup"><span data-stu-id="56052-260">Sales order 4</span></span>

1. <span data-ttu-id="56052-261">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างใบสั่งขาย 4</span><span class="sxs-lookup"><span data-stu-id="56052-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="56052-262">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="56052-263">**บัญชีลูกค้า:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="56052-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="56052-264">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="56052-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="56052-265">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="56052-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="56052-266">สร้างบันทึกย่อของหมายเลขใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="56052-267">เพิ่มรายการไปยังใบสั่งขายใหม่ และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="56052-268">**หมายเลขสินค้า:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="56052-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="56052-269">**ปริมาณ:** *25*</span><span class="sxs-lookup"><span data-stu-id="56052-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="56052-270">เลือก **สร้างรายการ** เพื่อเพิ่มรายการที่สอง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="56052-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="56052-271">**หมายเลขสินค้า:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="56052-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="56052-272">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="56052-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="56052-273">จองสินค้าคงคลังสำหรับทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="56052-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="56052-274">นำใบสั่งออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="56052-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="56052-275">รับรหัสงานสำหรับงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="56052-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="56052-276">ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="56052-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="56052-277">กรองข้อมูลในฟิลด์ **คลังสินค้า** เพื่อให้แสดงเฉพาะงานสำหรับคลังสินค้า *51* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56052-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="56052-278">ควรมีการสร้างรหัสงานสี่รหัส</span><span class="sxs-lookup"><span data-stu-id="56052-278">Four work IDs should have been created.</span></span> <span data-ttu-id="56052-279">จดบันทึกรหัสงานสำหรับใบสั่งขายแต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="56052-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="56052-280">รหัสใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="56052-280">Sales order ID</span></span> | <span data-ttu-id="56052-281">รหัสงาน</span><span class="sxs-lookup"><span data-stu-id="56052-281">Work ID</span></span> | <span data-ttu-id="56052-282">ปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="56052-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="56052-283">ใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="56052-283">Sales Order 1</span></span> | <span data-ttu-id="56052-284">รหัสงาน 1</span><span class="sxs-lookup"><span data-stu-id="56052-284">Work ID 1</span></span> | <span data-ttu-id="56052-285">20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-285">20 ea</span></span> |
    | <span data-ttu-id="56052-286">ใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="56052-286">Sales Order 2</span></span> | <span data-ttu-id="56052-287">รหัสงาน 2</span><span class="sxs-lookup"><span data-stu-id="56052-287">Work ID 2</span></span> | <span data-ttu-id="56052-288">6 ชิ้น (ผลรวมของทั้งสองรายการ)</span><span class="sxs-lookup"><span data-stu-id="56052-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="56052-289">ใบสั่งขาย 3</span><span class="sxs-lookup"><span data-stu-id="56052-289">Sales Order 3</span></span> | <span data-ttu-id="56052-290">รหัสงาน 3</span><span class="sxs-lookup"><span data-stu-id="56052-290">Work ID 3</span></span> | <span data-ttu-id="56052-291">15 ชิ้น (ผลรวมของทั้งสองรายการ)</span><span class="sxs-lookup"><span data-stu-id="56052-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="56052-292">ใบสั่งขาย 4</span><span class="sxs-lookup"><span data-stu-id="56052-292">Sales Order 4</span></span> | <span data-ttu-id="56052-293">รหัสงาน 4</span><span class="sxs-lookup"><span data-stu-id="56052-293">Work ID 4</span></span> | <span data-ttu-id="56052-294">35 ชิ้น (ผลรวมของทั้งสองรายการ)</span><span class="sxs-lookup"><span data-stu-id="56052-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="56052-295">ก่อนที่คุณจะรันโฟลว์บนอุปกรณ์เคลื่อนที่ ให้ตรวจสอบให้แน่ใจว่าเฉพาะงานที่คุณเพิ่งสร้างไว้อยู่ในสถานะ *เปิด* สำหรับคลังสินค้า *51* และชนิดใบสั่งงานชนิดใบสั่งงาน *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="56052-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="56052-296">มิฉะนั้น ผลลัพธ์ของการทดสอบอาจแตกต่างกัน เนื่องจากการเบิกสินค้าที่สั่งการโดยระบบจะรวมถึงงานที่มีสิทธิ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="56052-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="56052-297">ไปที่ **การจัดการคลังสินค้า \> งาน \> ขาออก \> เปิดงานการขาย**</span><span class="sxs-lookup"><span data-stu-id="56052-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="56052-298">ในกริด **เปิดงานการขาย** ในฟิลด์ **คลังสินค้า** เพื่อให้แสดงเฉพาะงานสำหรับคลังสินค้า *51* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56052-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="56052-299">ยืนยันว่าเฉพาะรหัสงานสี่รหัสที่คุณสร้างไว้ก่อนหน้านี้เท่านั้นที่จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="56052-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="56052-300">ปิดหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="56052-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="56052-301">การดำเนินการโฟลว์อุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="56052-301">Mobile device flow execution</span></span>

<span data-ttu-id="56052-302">โดยยึดตามการตั้งค่า ระบบจะป้อนงานของผู้ใช้ที่เรียงลำดับจากปริมาณของรายการงานสูงสุดไปต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="56052-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="56052-303">ปริมาณในทุกรายการจะน้อยกว่า 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="56052-304">โปรดจำไว้ว่าการตั้งค่านี้จะบันทึกงานใดๆ ที่มีอย่างน้อยหนึ่งรายการที่มีปริมาณน้อยกว่า 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="56052-305">ดังนั้น ถ้างานมีรายการอื่นซึ่งปริมาณเป็น 20 ชิ้น หรือมากกว่า 20 ชิ้น ก็จะมีผลบังคับใช้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="56052-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="56052-306">แอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="56052-306">Mobile app</span></span>

1. <span data-ttu-id="56052-307">ลงชื่อเข้าใช้แอปคลังสินค้าในฐานะผู้ใช้ในคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="56052-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="56052-308">ไปที่ **ขาออก \> การเบิกสินค้าขาย – ระบบ**</span><span class="sxs-lookup"><span data-stu-id="56052-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="56052-309">มีการแสดงขั้นตอนการเบิกสินค้าสำหรับรหัสงาน *4*</span><span class="sxs-lookup"><span data-stu-id="56052-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="56052-310">รหัสงานนี้ถูกแสดงเป็นอันดับแรก เนื่องจากการตั้งค่าของใบสั่งการสอบถามที่สั่งการโดยระบบ ที่ซึ่งคุณได้ระบุว่างานควรถูกเรียงลำดับตามปริมาณรายการงานจากมากไปหาน้อย</span><span class="sxs-lookup"><span data-stu-id="56052-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="56052-311">ดำเนินการเบิกสินค้าที่ต้องการให้เสร็จสมบูรณ์ และย้ายเพื่อปิดรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="56052-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="56052-312">ถัดไป รหัสงาน *3* จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="56052-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="56052-313">หนึ่งในรายการงานอยู่ถัดไปในลำดับ ตามปริมาณของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="56052-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="56052-314">ดำเนินการเบิกสินค้าให้เสร็จสมบูรณ์ และย้ายเพื่อปิดรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="56052-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="56052-315">ถัดไป รหัสงาน *2* จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="56052-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="56052-316">รายการเบิกสินค้าของงานนี้อยู่ถัดไปในลำดับ</span><span class="sxs-lookup"><span data-stu-id="56052-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="56052-317">ดำเนินการเบิกสินค้าให้เสร็จสมบูรณ์ และย้ายเพื่อปิดรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="56052-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="56052-318">ไม่มีงานเพิ่มเติมที่ควรจะแสดงต่อคุณ</span><span class="sxs-lookup"><span data-stu-id="56052-318">No further work should be presented to you.</span></span> <span data-ttu-id="56052-319">รหัสงาน *1* ไม่มีสิทธิ์สำหรับรายการเมนูของอุปกรณ์เคลื่อนที่นี้ เนื่องจากการสอบถามระบุว่าส่วนหัวของงานจะได้รับการพิจารณาเฉพาะเมื่อปริมาณในรายการงานน้อยกว่า 20 ชิ้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56052-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="56052-320">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="56052-320">Tips</span></span>

<span data-ttu-id="56052-321">*รวม* การสอบถามลำดับงานที่สั่งการโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="56052-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="56052-322">สิ่งสำคัญคือคุณต้องจดจำข้อเท็จจริงนี้สำหรับการตั้งค่าบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="56052-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="56052-323">ตัวอย่างเช่น คุณต้องการให้รายการเมนูที่ระบุประมวลผลเฉพาะงานที่หน่วยของงานเป็น *ชิ้น* และคุณระบุข้อจำกัดดังกล่าวในแท็บ **ช่วง** ของการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="56052-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="56052-324">ในกรณีนี้ งานทั้งหมดที่ซึ่งรายการงานอย่างน้อยหนึ่งรายการมีการตั้งค่าหน่วยของงานเป็น *ชิ้น* จะถูกป้อนให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="56052-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="56052-325">ดังนั้น งานนี้ยังอาจรวมถึงงานที่รายการงานมีหน่วยของงาน ที่ไม่ใช่ *ชิ้น* (เช่น *กล่อง* หรือ *แท่นวางสินค้า*)</span><span class="sxs-lookup"><span data-stu-id="56052-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="56052-326">การสอบถามจะไม่รวมเฉพาะงานที่ซึ่งรายการงานไม่มีการตั้งค่าหน่วยของงานเป็น *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="56052-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="56052-327">ดังนั้น ในตัวอย่างจากสถานการณ์จำลองนี้ รหัสงาน *4* ยังถูกบันทึกโดยการสอบถามด้วย</span><span class="sxs-lookup"><span data-stu-id="56052-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="56052-328">เมื่อมีการสร้าง รายการสองรายการถูกเพิ่ม: หนึ่งรายการสำหรับ 25 ชิ้น และอีกรายการหนึ่งสำหรับ 10 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="56052-329">งานยังคงแสดงต่อผู้ใช้ เพราะรายการงานอย่างน้อยหนึ่งรายการมีปริมาณน้อยกว่า 20 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="56052-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="56052-330">ทั้งนี้ขึ้นอยู่กับสถานการณ์จำลอง คุณสามารถป้องกันไม่ให้เกิดลักษณะการทำงานนี้ได้โดยใช้การแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="56052-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]