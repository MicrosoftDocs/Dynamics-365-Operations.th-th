---
title: ตรวจสอบการดำเนินการวางแผนหลัก
description: หัวข้อนี้อธิบายถึงวิธีการที่ผู้วางแผนการผลิตสามารถดูได้ว่ากำลังรันการวางแผนหลักอยู่หรือไม่
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6e7fdd51670ea63efc04e883703f1763955115b
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781930"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="e294e-103">ตรวจสอบการดำเนินการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="e294e-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="e294e-104">ใช้แผนภูมิ Gantt เพื่อแสดงความคืบหน้าของการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="e294e-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="e294e-105">จากเพจ **ดูความคืบหน้าของการวางแผนหลัก** คุณสามารถดูรายละเอียดของการวางแผนหลักในอดีตรันเป็นแผนภูมิ Gantt ได้</span><span class="sxs-lookup"><span data-stu-id="e294e-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="e294e-106">ฟังก์ชันนี้จะช่วยให้คุณเข้าใจเวลาที่ใช้ในระยะของการวางแผนหลักต่างๆ</span><span class="sxs-lookup"><span data-stu-id="e294e-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="e294e-107">สำหรับงานการวางแผนที่ใช้งานอยู่ปัจจุบัน คุณสามารถใช้เพจ **ดูความคืบหน้าของการวางแผนหลัก** เพื่อติดตามความคืบหน้าและดูเวลาที่เหลืออยู่โดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="e294e-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="e294e-108">เปิดและใช้คุณลักษณะการแสดงภาพความคืบหน้าของแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="e294e-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="e294e-109">เมื่อต้องการใช้ฟังก์ชันนี้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e294e-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="e294e-110">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** บนแท็บ **ใหม่** ให้เลือก **การแสดงภาพความคืบหน้าของการวางแผนหลัก** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="e294e-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="e294e-111">ถ้าคุณลักษณะไม่ปรากฏบนแท็บ **ใหม่** ให้ดูที่แท็บ **ไม่ได้เปิดใช้งาน** และ **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e294e-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="e294e-112">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="e294e-112">Select **Enable now**.</span></span> <span data-ttu-id="e294e-113">หรือเลือก **กำหนดการ** แล้วเลือกเวลาที่คุณต้องการเปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e294e-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="e294e-114">เพจ **ดูความคืบหน้าของการวางแผนหลัก** สามารถแสดงทั้งงานการวางแผนในอดีต และงานการวางแผนที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="e294e-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="e294e-115">เมื่อต้องการดูงานการวางแผนในอดีต มีสองตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e294e-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="e294e-116">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก** และหลังจากนั้น ในบานหน้าต่างการดำเนินการ เลือก **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="e294e-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="e294e-117">เมื่อเลือกงานที่ต้องการแล้ว เลือก **การสอบถาม** และหลังจากนั้นเลือก **ดูความคืบหน้า**</span><span class="sxs-lookup"><span data-stu-id="e294e-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="e294e-118">ไปที่ **การวางแผนหลัก \> พื้นที่ทำงาน \> การวางแผนหลัก** บนไทล์การวางแผนหลัก คลิก **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="e294e-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="e294e-119">เมื่อเลือกงานที่ต้องการแล้ว เลือก **การสอบถาม** และหลังจากนั้นเลือก **ดูความคืบหน้า**</span><span class="sxs-lookup"><span data-stu-id="e294e-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e294e-120">เมื่อต้องการดูงานการวางแผนที่ใช้งานอยู่ มีสองตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e294e-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="e294e-121">ไปที่ **การวาง \> พื้นที่ทำงาน \> การวางแผนหลัก** บนบานหน้าต่างการดำเนินการ เลือก **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="e294e-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="e294e-122">เมื่อเลือกงานที่ต้องการแล้ว เลือก **การสอบถาม** และหลังจากนั้นเลือก **ดูความคืบหน้า**</span><span class="sxs-lookup"><span data-stu-id="e294e-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="e294e-123">ไปที่ **การวางแผนหลัก \> พื้นที่ทำงาน \> การวางแผนหลัก** บนไทล์การวางแผนหลัก คลิก **ดูความคืบหน้า**</span><span class="sxs-lookup"><span data-stu-id="e294e-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="e294e-124">เมื่อเลือกงานที่ต้องการแล้ว เลือก **การสอบถาม** และหลังจากนั้นเลือก **ดูความคืบหน้า**</span><span class="sxs-lookup"><span data-stu-id="e294e-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e294e-125">โปรดทราบว่าคุณสามารถดูงานที่ใช้งานอยู่ได้เฉพาะเมื่องานการวางแผนกำลังประมวลผลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e294e-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="e294e-126">วิเคราะห์งานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="e294e-126">Analyze a master planning job</span></span>

<span data-ttu-id="e294e-127">ในแผนภูมิ Gantt คุณสามารถขยายกระบวนการวางแผนแต่ละขั้นตอนต่อไปนี้ได้ เพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับเวลาที่ใช้</span><span class="sxs-lookup"><span data-stu-id="e294e-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="e294e-128">การเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e294e-128">Initializing</span></span>
- <span data-ttu-id="e294e-129">การลบและการแทรกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e294e-129">Deleting and inserting data</span></span>
- <span data-ttu-id="e294e-130">การวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="e294e-130">Coverage planning</span></span>
- <span data-ttu-id="e294e-131">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="e294e-131">Delays</span></span>
- <span data-ttu-id="e294e-132">ข้อความการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e294e-132">Action messages</span></span>
- <span data-ttu-id="e294e-133">การพิจารณาขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="e294e-133">Finalization</span></span>
- <span data-ttu-id="e294e-134">การยืนยันอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e294e-134">Auto-firming</span></span>

<span data-ttu-id="e294e-135">แผนภูมิ Gantt เป็นเครื่องมือที่มีประโยชน์ ถ้าคุณต้องการดูผลกระทบของการใช้ข่าวสารเกี่ยวกับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e294e-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="e294e-136">การนำทางในแผนภูมิ Gantt</span><span class="sxs-lookup"><span data-stu-id="e294e-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="e294e-137">เมื่อต้องการขยายกลุ่มที่เลือก และแสดงรายละเอียด ให้เลือกเครื่องหมายบวก (**+**) ในมุมมองแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="e294e-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="e294e-138">ถ้าต้องการยุบกลุ่มที่เลือก ให้เลือกเครื่องหมายลบ (**-**) ในมุมมองแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="e294e-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="e294e-139">คุณสามารถใช้แป้นพิมพ์ของคุณสำหรับการนำทาง</span><span class="sxs-lookup"><span data-stu-id="e294e-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="e294e-140">ใช้คีย์ **ลูกศรขึ้น** และ **ลูกศรลง** เพื่อย้ายระหว่างแถว</span><span class="sxs-lookup"><span data-stu-id="e294e-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="e294e-141">ใช้คีย์ **ลูกศรขวา** และ **ลูกศรซ้าย** เพื่อขยายและยุบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e294e-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="e294e-142">ถ้าต้องการเปิดหรือปิดระดับทั้งหมดในแผนภูมิ Gantt ให้เลือก **ขยายทั้งหมด** หรือ **ยุบทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e294e-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="e294e-143">เมื่อต้องการดูเวลาการประมวลผลที่เกี่ยวข้อง ให้วางเมาส์เหนืองาน</span><span class="sxs-lookup"><span data-stu-id="e294e-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="e294e-144">(งานเป็นระดับต่ำสุดในแผนภูมิ Gantt)</span><span class="sxs-lookup"><span data-stu-id="e294e-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="e294e-145">ดูการรันการวางแผนหลักเพิ่มเติมเพื่อเปรียบเทียบงาน</span><span class="sxs-lookup"><span data-stu-id="e294e-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="e294e-146">โดยการเลือกงานการวางแผนหลักในฟิลด์ **แสดงการรันการวางแผนหลักเพิ่มเติม** คุณสามารถดูการรันการวางแผนหลักเพิ่มเติมในแผนภูมิ Gantt และเปรียบเทียบงานสองงาน</span><span class="sxs-lookup"><span data-stu-id="e294e-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="e294e-147">การแสดงระดับ BOM</span><span class="sxs-lookup"><span data-stu-id="e294e-147">BOM-level display</span></span>

<span data-ttu-id="e294e-148">ระดับตามสูตรการผลิต (BOM) แสดงแตกต่างกันสำหรับการวางแผนความครอบคลุม ความล่าช้า การดำเนินการ และการยืนยันยอด</span><span class="sxs-lookup"><span data-stu-id="e294e-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="e294e-149">**การวางแผนความครอบคลุม** – ระดับ BOM จะแสดงตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="e294e-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e294e-150">จะมีการคำนวณจากบนลงล่าง</span><span class="sxs-lookup"><span data-stu-id="e294e-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="e294e-151">**ตัวอย่าง** : ระดับ BOM 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e294e-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e294e-152">**ความล่าช้า** – ระดับ BOM จะแสดงเป็นระดับ BOM การวางแผนความครอบคลุมคูณด้วย –1</span><span class="sxs-lookup"><span data-stu-id="e294e-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="e294e-153">(กล่าวคือ มีเครื่องหมายลบ)</span><span class="sxs-lookup"><span data-stu-id="e294e-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="e294e-154">**ตัวอย่าง** : ระดับ BOM –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="e294e-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="e294e-155">**ข้อความแสดงการดำเนินการ** – ระดับ BOM จะแสดงตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="e294e-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e294e-156">จะมีการคำนวณจากบนลงล่าง</span><span class="sxs-lookup"><span data-stu-id="e294e-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="e294e-157">**ตัวอย่าง** : ระดับ BOM 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e294e-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e294e-158">**การยืนยันอัตโนมัติ** – ระดับ BOM จะแสดงเป็น 999 ลบด้วยระดับ BOM สำหรับการวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="e294e-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="e294e-159">**ตัวอย่าง** : ระดับ BOM 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="e294e-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="e294e-160">ตารางต่อไปนี้สรุปลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="e294e-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="e294e-161">ระดับ BOM ที่แสดง</span><span class="sxs-lookup"><span data-stu-id="e294e-161">BOM level that is shown</span></span> | <span data-ttu-id="e294e-162">สินค้าขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="e294e-162">End item</span></span> | <span data-ttu-id="e294e-163">Subcomponent</span><span class="sxs-lookup"><span data-stu-id="e294e-163">Subcomponent</span></span> | <span data-ttu-id="e294e-164">วัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="e294e-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="e294e-165">การวางแผนความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="e294e-165">Coverage planning</span></span> | <span data-ttu-id="e294e-166">0</span><span class="sxs-lookup"><span data-stu-id="e294e-166">0</span></span> | <span data-ttu-id="e294e-167">1</span><span class="sxs-lookup"><span data-stu-id="e294e-167">1</span></span> | <span data-ttu-id="e294e-168">2</span><span class="sxs-lookup"><span data-stu-id="e294e-168">2</span></span> |
| <span data-ttu-id="e294e-169">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="e294e-169">Delays</span></span> | <span data-ttu-id="e294e-170">0</span><span class="sxs-lookup"><span data-stu-id="e294e-170">0</span></span> | <span data-ttu-id="e294e-171">-1</span><span class="sxs-lookup"><span data-stu-id="e294e-171">–1</span></span> | <span data-ttu-id="e294e-172">-2</span><span class="sxs-lookup"><span data-stu-id="e294e-172">–2</span></span> |
| <span data-ttu-id="e294e-173">ข้อความแสดงการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e294e-173">Action message</span></span> | <span data-ttu-id="e294e-174">0</span><span class="sxs-lookup"><span data-stu-id="e294e-174">0</span></span> | <span data-ttu-id="e294e-175">1</span><span class="sxs-lookup"><span data-stu-id="e294e-175">1</span></span> | <span data-ttu-id="e294e-176">2</span><span class="sxs-lookup"><span data-stu-id="e294e-176">2</span></span> |
| <span data-ttu-id="e294e-177">การยืนยันอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e294e-177">Auto-firming</span></span> | <span data-ttu-id="e294e-178">999</span><span class="sxs-lookup"><span data-stu-id="e294e-178">999</span></span> | <span data-ttu-id="e294e-179">998</span><span class="sxs-lookup"><span data-stu-id="e294e-179">998</span></span> | <span data-ttu-id="e294e-180">997</span><span class="sxs-lookup"><span data-stu-id="e294e-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="e294e-181">แสดงความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="e294e-181">Visualize progress</span></span>

<span data-ttu-id="e294e-182">ถ้าคุณดูงานการวางแผนหลักที่กำลังรันอยู่ในขณะนี้ ความคืบหน้ากำลังแสดงผ่านสีในแผนภูมิ Gantt</span><span class="sxs-lookup"><span data-stu-id="e294e-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="e294e-183">สีดังต่อไปนี้นำไปใช้กับชุดรูปแบบสีฟ้า</span><span class="sxs-lookup"><span data-stu-id="e294e-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="e294e-184">สำหรับชุดรูปแบบสีอื่นๆ สีจะแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e294e-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="e294e-185">**สีน้ำเงิน** – งานการวางแผนที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e294e-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="e294e-186">**สีส้ม** – งานที่อยู่ระหว่างดำเนินการอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e294e-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="e294e-187">**สีฟ้า** – การประเมินสำหรับงานที่เหลืออยู่</span><span class="sxs-lookup"><span data-stu-id="e294e-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="e294e-188">สีจะแสดงเฉพาะในระดับต่ำสุดในแผนภูมิ Gantt</span><span class="sxs-lookup"><span data-stu-id="e294e-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="e294e-189">เลือก **ขยายทั้งหมด** เพื่อดูงานทั้งหมดในงานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="e294e-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="e294e-190">การประเมินของงานที่เหลืออยู่ตามงานการวางแผนหลักในอดีต</span><span class="sxs-lookup"><span data-stu-id="e294e-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="e294e-191">รันการวางแผนหลักและติดตามเวลาการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="e294e-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="e294e-192">บนแดชบอร์ดเริ่มต้น ให้เลือก **การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="e294e-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="e294e-193">ในฟิลด์ **แผน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e294e-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="e294e-194">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="e294e-194">Select **Run**.</span></span>
1. <span data-ttu-id="e294e-195">ตั้งค่าตัวเลือก **ติดตามเวลาประมวลผล** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e294e-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="e294e-196">ในฟิลด์ **จำนวนของเธรด** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e294e-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="e294e-197">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="e294e-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="e294e-198">ในกริด ให้เลือกแถวที่มีฟิลด์ **ฟิลด์** ตั้งค่าให้กับ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="e294e-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="e294e-199">ในฟิลด์ **เกณฑ์** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e294e-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="e294e-200">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e294e-200">Select **OK**.</span></span>
