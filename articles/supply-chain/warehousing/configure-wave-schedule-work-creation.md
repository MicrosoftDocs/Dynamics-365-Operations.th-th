---
title: จัดกำหนดการการสร้างงานในระหว่างเวฟ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้วิธีการประมวลผลเวฟการสร้างงานตามกำหนดการ
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501233"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="b57fd-103">จัดกำหนดการการสร้างงานในระหว่างเวฟ</span><span class="sxs-lookup"><span data-stu-id="b57fd-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b57fd-104">ใช้คุณลักษณะ *การสร้างงานตามกำหนดการ* เนื่องจากเป็นส่วนหนึ่งของกระบวนการเวฟของคุณที่จะช่วยเพิ่มปริมาณที่สามารถประมวลผลเวฟได้ โดยการให้ระบบสร้างงานโดยใช้การประมวลผลแบบขนาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="b57fd-105">เมื่อมีการเปิดใช้งานฟังก์ชัน งานที่วางแผนไว้จะถูกสร้างขึ้นโดยอัตโนมัติ ซึ่งระบบจะประมวลผลเพื่อสร้างงานจริงในที่สุด</span><span class="sxs-lookup"><span data-stu-id="b57fd-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="b57fd-106">หากจํานวนของรายการจํานวนงานในศูนย์การผลิตของเวฟถึงขีดจำกัดที่กำหนดไว้ล่วงหน้า ระบบจะสร้างงานจริงอย่างรวดเร็วขึ้นโดยใช้การประมวลผลแบบขนานแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="b57fd-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="b57fd-107">เปิดใช้งานคุณลักษณะการสร้างงานตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="b57fd-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="b57fd-108">เปิดใช้งานคุณลักษณะในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="b57fd-108">Enable the feature in feature management</span></span>

<span data-ttu-id="b57fd-109">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การสร้างงานตามกำหนดการ* คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="b57fd-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b57fd-110">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b57fd-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b57fd-111">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b57fd-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b57fd-112">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="b57fd-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b57fd-113">**ชื่อคุณลักษณะ:** *การสร้างงานตามกำหนดการ*</span><span class="sxs-lookup"><span data-stu-id="b57fd-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="b57fd-114">ต้องเปิดใช้งานคุณลักษณะ *การบล็อคงานทั่วทั้งองค์กร* ก่อนที่คุณจะสามารถเปิดใช้งาน *การสร้างงานตามกำหนดการ*</span><span class="sxs-lookup"><span data-stu-id="b57fd-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="b57fd-115">เปิดใช้งานการประมวลผลชุดงานของเวฟด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b57fd-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="b57fd-116">หากต้องการใช้ประโยชน์จากวิธีการแบบอะซิงโครนัสแบบขนานเพื่อสร้างงานของคลังสินค้า กระบวนการเวฟของคุณจะต้องรันอยู่ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="b57fd-117">เพื่อตั้งค่ารายการนี้:</span><span class="sxs-lookup"><span data-stu-id="b57fd-117">To set this up:</span></span>

1. <span data-ttu-id="b57fd-118">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="b57fd-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="b57fd-119">บนแท็บ **ทั่วไป** ตั้งค่า **ประมวลผลเวฟในชุดงาน** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="b57fd-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="b57fd-120">หรือคุณยังสามารถเลือก **กลุ่มชุดงานการประมวลผลเวฟ** ที่จัดสรรไว้ เพื่อป้องกันไม่ให้การประมวลผลคิวชุดงานของคุณรันพร้อมกันกับกระบวนการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b57fd-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="b57fd-121">ตั้งค่า **เวลารอการล็อค (ms)** ที่ใช้เมื่อระบบประมวลผลเวฟหลายเวฟในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b57fd-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="b57fd-122">สำหรับกระบวนการเวฟที่ใหญ่ที่สุด เราขอแนะนำค่า *60000*</span><span class="sxs-lookup"><span data-stu-id="b57fd-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="b57fd-123">เปิดใช้งานวิธีการขั้นตอนเวฟใหม่ด้วยตนเองจากเท็มเพลตเวฟที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b57fd-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="b57fd-124">เริ่มต้นโดยการสร้างวิธีการขั้นตอนของเวฟใหม่และเปิดใช้งานวิธีการดังกล่าวเพื่อการประมวลผลงานแบบอะซิงโครนัสแบบขนาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="b57fd-125">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="b57fd-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="b57fd-126">เลือก  **สร้างวิธีการใหม่** และโปรดทราบว่า *WHSScheduleWorkCreationWaveStepMethod* ถูกเพิ่มเข้าในรายการของวิธีการกระบวนการเวฟที่คุณสามารถใช้ในเท็มเพลตเวฟการจัดส่งของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="b57fd-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="b57fd-127">เลือกเรกคอร์ดที่มี **ชื่อวิธีการ** *WHSScheduleWorkCreationWaveStepMethod* และเลือก **การตั้งค่าคอนฟิกงาน**</span><span class="sxs-lookup"><span data-stu-id="b57fd-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="b57fd-128">เพื่อเพิ่มแถวใหม่ไปยังกริด เลือก **สร้าง** ในบานหน้าต่างการดำเนินการ และใช้การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b57fd-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="b57fd-129">**คลังสินค้า** - เลือกคลังสินค้าที่คุณจะใช้จัดกำหนดการการประมวลผลการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="b57fd-130">**จํานวนงานของชุดงานสูงสุด** - ระบุจํานวนงานของชุดงานสูงสุด</span><span class="sxs-lookup"><span data-stu-id="b57fd-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="b57fd-131">ในกรณีส่วนใหญ่ ค่านี้ควรอยู่ในช่วงตั้งแต่ 8-16 อย่างไรก็ตาม ขอแนะนำว่าคุณควรลองใช้การตั้งค่าที่เหมาะสมตามสถานการณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b57fd-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="b57fd-132">**กลุ่มชุดงานการประมวลผลเวฟ** - เลือกกลุ่มชุดงานการประมวลผลเวฟที่จัดสรรไว้ เพื่อให้การประมวลผลคิวชุดงานของคุณมีประสิทธิภาพสูงสุด</span><span class="sxs-lookup"><span data-stu-id="b57fd-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="b57fd-133">ขณะนี้คุณพร้อมที่จะอัพเดตเท็มเพลตเวฟที่มีอยู่ (หรือสร้างเท็มเพลตใหม่) เพื่อใช้วิธีการประมวลผลเวฟ *การสร้างงานตามกำหนดการ*</span><span class="sxs-lookup"><span data-stu-id="b57fd-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="b57fd-134">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="b57fd-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="b57fd-135">เลือก **แก้ไข** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b57fd-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="b57fd-136">ในบานหน้าต่างรายการ ให้เลือกเท็มเพลตเวฟที่คุณต้องการอัพเดต (หากคุณทดสอบโดยใช้ข้อมูลสาธิต คุณสามารถใช้ *24 ค่าเริ่มต้นการจัดส่ง*)</span><span class="sxs-lookup"><span data-stu-id="b57fd-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="b57fd-137">ขยาย FastTab **วิธีการ** และเลือกแถวที่มี **ชื่อ** *การสร้างงานตามกำหนดการ* ในกริด **วิธีการที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="b57fd-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="b57fd-138">เลือกลูกศรที่ชี้ไปที่คอลัมน์ **วิธีการที่เลือก** เพื่อย้ายแถวที่เลือกไปที่คอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="b57fd-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="b57fd-139">(คุณสามารถมีวิธีการเลือกได้เพียงหนึ่งวิธีเท่านั้นในแต่ละครั้งที่ใช้ *WHSScheduleWorkCreationWaveStepMethod* หรือ *createWork* ดังนั้น แถวที่มีอยู่ที่มี **ชื่อวิธีการ** *createWork* จะถูกย้ายไปยังกริด **วิธีการที่เหลือ** โดยอัตโนมัติ)</span><span class="sxs-lookup"><span data-stu-id="b57fd-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="b57fd-140">ตั้งค่าข้อมูลขีดจำกัดการประมวลผลงานเวฟ</span><span class="sxs-lookup"><span data-stu-id="b57fd-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="b57fd-141">ระบบจะสร้างข้อมูลขีดจำกัดการประมวลผลงานเวฟเริ่มต้นในครั้งแรกที่กระบวนการเวฟรัน โดยใช้การประมวลผลตามงานใดๆ</span><span class="sxs-lookup"><span data-stu-id="b57fd-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="b57fd-142">ข้อมูลจะถูกใช้ในการควบคุมเวลาที่การประมวลผลเวฟจะรันแบบอะซิงโครนัสและยึดตามงาน ซึ่งช่วยให้สามารถประมวลผลและสร้างงานพร้อมกันได้</span><span class="sxs-lookup"><span data-stu-id="b57fd-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="b57fd-143">ในครั้งแรก ข้อมูลเริ่มต้นจะใช้ค่าขีดจำกัดเป็น 15 สำหรับจํานวนรายการโหลดต่ำสุด (MINIMUMWAVELOADLINES)</span><span class="sxs-lookup"><span data-stu-id="b57fd-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="b57fd-144">นี่หมายความว่าเมื่อระบบประมวลผลเวฟที่มีรายการโหลดมากกว่า 15 รายการ ระบบจะใช้การประมวลผลงานแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="b57fd-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="b57fd-145">คุณสามารถแทรก/อัพเดตข้อมูลนี้ด้วยตนเองในตาราง **WHSWaveTaskProcessingThresholdParameters** ในสภาพแวดล้อมการทดสอบของคุณ แต่ถ้าคุณต้องเปลี่ยนการตั้งค่านี้ในสภาพแวดล้อมการผลิต คุณต้องติดต่อ Microsoft Support เพื่อร้องขอการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b57fd-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="b57fd-146">ทำงานกับคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="b57fd-146">Work with the feature</span></span>

<span data-ttu-id="b57fd-147">เมื่อเปิดใช้งานฟังก์ชัน *การสร้างงานตามกำหนดการ* การประมวลผลเวฟจะสร้างงานที่วางแผนไว้ ซึ่งจะใช้โดยกระบวนการสร้างงานใหม่ในที่สุด</span><span class="sxs-lookup"><span data-stu-id="b57fd-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="b57fd-148">ในระหว่างการสร้างงาน งานจะถูกบล็อคโดยใช้คุณลักษณะ *การบล็อคงานทั่วทั้งองค์กร*</span><span class="sxs-lookup"><span data-stu-id="b57fd-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="b57fd-149">แผนผังลำดับงานต่อไปนี้จะแสดงวิธีการสร้างงานที่วางแผนไว้ในระหว่างการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="b57fd-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![จัดกำหนดการสร้างงาน](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="b57fd-151">งานที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="b57fd-151">Planned work</span></span>

<span data-ttu-id="b57fd-152">หน้า **รายละเอียดของงานที่วางแผนไว้** (**การจัดการคลังสินค้า \> งาน \> รายละเอียดงานของงานที่วางแผนไว้**) แสดงข้อมูลเกี่ยวกับงานที่วางแผนไว้ ซึ่งมีการสร้างขึ้นในตอนเริ่มต้นในระหว่างการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="b57fd-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="b57fd-153">ค่า **สถานะกระบวนการ** ต่อไปนี้พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="b57fd-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="b57fd-154">**จัดคิวแล้ว** - งานที่วางแผนไว้รอที่จะถูกใช้ในการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="b57fd-155">**เสร็จสมบูรณ์** - งานที่วางแผนไว้ถูกใช้ในการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="b57fd-156">**ล้มเหลว** – การประมวลผลเวฟล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b57fd-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="b57fd-157">โปรดทราบว่างานที่วางแผนไว้สามารถอยู่ในสถานะ **ล้มเหลว** ที่มีหรือไม่มีงานจริงที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b57fd-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="b57fd-158">เมื่อกระบวนการสร้างงานจริงล้มเหลว งานจริงจะยังคงอยู่ในสถานะ *ยกเลิกแล้ว*</span><span class="sxs-lookup"><span data-stu-id="b57fd-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="b57fd-159">ชุดงานสำหรับกระบวนการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="b57fd-159">Batch job for the work creation process</span></span>

<span data-ttu-id="b57fd-160">เมื่อต้องการดูงานในชุดงานของเวฟการประมวลผล ให้เลือก **งานในชุดงาน** บนบานหน้าต่างการดำเนินการในหน้า **เวฟทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b57fd-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="b57fd-161">จากที่นี่ คุณสามารถดูรายละเอียดงานของชุดงานทั้งหมดสำหรับรหัสงานในชุดงานแต่ละรหัสได้</span><span class="sxs-lookup"><span data-stu-id="b57fd-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]