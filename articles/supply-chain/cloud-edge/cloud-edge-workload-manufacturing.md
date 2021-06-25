---
title: ปริมาณงานการดำเนินการผลิตสำหรับ Cloud และ edge scale unit
description: หัวข้อนี้จะอธิบายวิธีการทำงานของปริมาณงานการดำเนินการผลิตกับ Cloud และ edge scale unit
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184007"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="b042c-103">ปริมาณงานการดำเนินการผลิตสำหรับสเกลยูนิตในระบบคลาวด์และ Edge</span><span class="sxs-lookup"><span data-stu-id="b042c-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="b042c-104">ปริมาณงานการเริ่มการผลิตมีให้แสดงตัวอย่าง ณ เวลานี้</span><span class="sxs-lookup"><span data-stu-id="b042c-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="b042c-105">ฟังก์ชันธุรกิจบางอย่างไม่ได้รับการสนับสนุนอย่างเต็มที่ในตัวอย่างสำหรับสาธารณะเมื่อมีการใช้ปริมาณงาน scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="b042c-106">ในการดำเนินการผลิต scale units จะจัดส่งความสามารถต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b042c-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="b042c-107">ผู้ปฏิบัติงานเครื่องจักรและหัวหน้างานฝ่ายผลิตสามารถเข้าถึงแผนการผลิตที่มีการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="b042c-108">ผู้ปฏิบัติงานในเครื่องสามารถรักษาแผนให้ทันสมัยอยู่เสมอโดยการรันงานการผลิตที่แยกต่างหากและมีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="b042c-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="b042c-109">หัวหน้างานฝ่ายผลิตสามารถปรับปรุงแผนการดำเนินงานได้</span><span class="sxs-lookup"><span data-stu-id="b042c-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="b042c-110">ผู้ปฏิบัติงานสามารถเข้าถึงเวลาและการเข้างานสำหรับการตอกบัตรเข้าและการตอกบัตรออกบน edge เพื่อให้มั่นใจว่าการคำนวณการจ่ายค่าจ้างของผู้ปฏิบัติงานถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b042c-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="b042c-111">หัวข้อนี้จะอธิบายวิธีการทำงานของปริมาณงานการดำเนินการผลิตกับ Cloud และ edge scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="b042c-112">วงจรการผลิต</span><span class="sxs-lookup"><span data-stu-id="b042c-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="b042c-113">ดังภาพที่แสดงต่อไปนี้ วงจรการผลิตจะถูกแบ่งออกเป็นสามระยะ ได้แก่ *วางแผน* *ดำเนินการ* และ *จบการทำงาน*</span><span class="sxs-lookup"><span data-stu-id="b042c-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="b042c-114">[![ระยะการดำเนินการผลิตเมื่อมีการใช้สภาพแวดล้อมเดียว](media/mes-phases.png "ระยะการดำเนินการผลิตเมื่อมีการใช้สภาพแวดล้อมเดียว")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="b042c-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="b042c-115">ระยะของ _แผน_ รวมถึงข้อกำหนดผลิตภัณฑ์ การวางแผน การสร้างใบสั่งและการจัดกำหนดการ และการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="b042c-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="b042c-116">ขั้นตอนการนำออกใช้บ่งชี้การเปลี่ยนจากระยะ _แผน_ ไปยังระยะ _ดำเนินการ_</span><span class="sxs-lookup"><span data-stu-id="b042c-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="b042c-117">เมื่อมีการนำใบสั่งผลิตออกใช้ งานใบสั่งผลิตจะมองเห็นได้บนชั้นการผลิตและพร้อมสำหรับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b042c-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="b042c-118">เมื่องานการผลิตถูกทำเครื่องหมายเป็นเสร็จสมบูรณ์แล้ว จะย้ายระยะ _การดำเนินการ_ ไปยังระยะ _การเสร็จสิ้น_</span><span class="sxs-lookup"><span data-stu-id="b042c-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="b042c-119">ในระยะ _การเสร็จสิ้น_ การลงทะเบียนจากระยะ *การดำเนินการ* จะเป็นไปตามลำดับงานการอนุมัติ ซึ่งถูกคำนวณ อนุมัติ และโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="b042c-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="b042c-120">ในจุดนั้น ใบสั่งผลิตจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b042c-120">At that point, the production order is completed.</span></span> <span data-ttu-id="b042c-121">ดังนั้น เกณฑ์สำหรับการจ่ายค่าจ้างของผู้ปฏิบัติงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b042c-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="b042c-122">การแบ่งระยะดำเนินการเป็นปริมาณงานที่แยกกัน</span><span class="sxs-lookup"><span data-stu-id="b042c-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="b042c-123">ดังภาพที่แสดงต่อไปนี้ เมื่อมีการใช้ scale unit ระยะ _การดำเนินการ_ จะถูกแบ่งออกเป็นปริมาณงานที่แยกกัน</span><span class="sxs-lookup"><span data-stu-id="b042c-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="b042c-124">[![ระยะการดำเนินการผลิตเมื่อมีการใช้ scale unit](media/mes-phases-workloads.png "ระยะการดำเนินการผลิตเมื่อมีการใช้ scale unit")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="b042c-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="b042c-125">แบบจำลองเดี๋ยวนี้จะมาจากการติดตั้งอินสแตนซ์เดียวกับแบบจำลองที่ยึดตามฮับและ scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="b042c-126">ระยะ _แผน_ และ _การเสร็จสิ้น_ จะรันเป็นการดำเนินงานของฝ่ายสนับสนุนบนฮับ และปริมาณงานการดำเนินการผลิตจะรันบน scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="b042c-127">ข้อมูลจะถูกโอนย้ายแบบอะซิงโครนัสระหว่างฮับและ scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="b042c-128">เมื่อมีการนำใบสั่งผลิตออกใช้บนฮับ ข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการประมวลผลงานการผลิตจะถูกโอนย้ายไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="b042c-129">ข้อมูลนี้รวมถึง ใบสั่งผลิต กระบวนการผลิต รายการวัสดุ และผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b042c-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="b042c-130">ข้อมูลที่ไม่เกี่ยวข้องกับใบสั่งผลิต (เช่น กิจกรรมทางอ้อม รหัสการขาดงาน และพารามิเตอร์การผลิต) จะถูกโอนย้ายจากฮับไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="b042c-131">ในฐานะที่เป็นกฎ ข้อมูลที่มีต้นกำเนิดมาจากฮับและมีการโอนย้ายไปยัง scale unit. สามารถสร้างหรืออัปเดตได้บนฮับเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b042c-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="b042c-132">ตัวอย่างเช่น รหัสการขาดงานใหม่หรือกิจกรรมทางอ้อมไม่สามารถสร้างขึ้นบน scale unit&mdash;สามารถใช้สำหรับการลงทะเบียนได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b042c-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="b042c-133">การลงทะเบียนที่ทำบน scale unit ระหว่างการดำเนินการจะถูกโอนย้ายไปยังฮับ ซึ่งจะมีการประมวลผลการอนุมัติเวลาและการเข้างาน สินค้าคงคลัง และการอัปเดตทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="b042c-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="b042c-134">งานการดำเนินการผลิตที่สามารถรันบนปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="b042c-135">สามารถรันงานการดำเนินการผลิตต่อไปนี้บนปริมาณงานเมื่อมีการใช้ scale unit:</span><span class="sxs-lookup"><span data-stu-id="b042c-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="b042c-136">การตอกบัตรเข้า ล็อกอิน การตอกบัตรออก และการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="b042c-137">เริ่มต้นงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-137">Start job</span></span>
- <span data-ttu-id="b042c-138">การรวมกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-138">Bundle jobs</span></span>
- <span data-ttu-id="b042c-139">ความคืบหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-139">Report progress</span></span>
- <span data-ttu-id="b042c-140">รายงานของเสีย</span><span class="sxs-lookup"><span data-stu-id="b042c-140">Report scrap</span></span>
- <span data-ttu-id="b042c-141">กิจกรรมทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="b042c-141">Indirect activity</span></span>
- <span data-ttu-id="b042c-142">ตัวแบ่ง</span><span class="sxs-lookup"><span data-stu-id="b042c-142">Break</span></span>
- <span data-ttu-id="b042c-143">รายงานการเสร็จงานและการสำรองสินค้า (คุณยังต้องรันปริมาณงานการรันคลังสินค้าบน scale unit ของคุณ ให้ดูเพิ่มเติมที่ [รายงานการเสร็จงานและการสำรองสินค้าบน scale unit](#RAF))</span><span class="sxs-lookup"><span data-stu-id="b042c-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="b042c-144">การทำงานกับปริมาณงานการดำเนินการผลิตบนฮับ</span><span class="sxs-lookup"><span data-stu-id="b042c-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="b042c-145">โดยทั่วไป กระบวนการที่จำเป็นในการรันปริมาณงานการดำเนินการผลิตจะรันโดยอัตโนมัติเพื่อเก็บฮับและ scale unit ทั้งหมดในการซิงค์ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="b042c-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b042c-146">อย่างไรก็ตาม ถ้าคุณกำลังประสบปัญหา คุณสามารถทริกเกอร์การประมวลผลการลงทะเบียนดิบที่ได้รับจากปริมาณงาน และ/หรือ ตรวจสอบล็อกการประมวลผลการลงทะเบียนด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="b042c-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="b042c-147">ประมวลผลการลงทะเบียนดิบด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b042c-147">Manually process raw registrations</span></span>

<span data-ttu-id="b042c-148">ชุดงานใน Supply Chain Management จะรันโดยอัตโนมัติเพื่อประมวลผลการลงทะเบียนทั้งหมดที่ได้รับมาจากปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="b042c-149">งานนี้จะสร้างสมุดรายวันการผลิตที่จำเป็นและรายการบันทึกเมื่อมีการประมวลผลการลงทะเบียนสำหรับงานที่เสร็จสมบูรณ์แล้วในปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="b042c-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="b042c-150">ถึงแม้ว่างานจะรันโดยอัตโนมัติ คุณสามารถรันด้วยตนเองได้ตลอดเวลาด้วยการล็อกอินเข้าฮับและไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ประมวลผลการลงทะเบียนดิบ**</span><span class="sxs-lookup"><span data-stu-id="b042c-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="b042c-151">ตรวจสอบล็อกการประมวลผลการลงทะเบียนดิบ</span><span class="sxs-lookup"><span data-stu-id="b042c-151">Check the raw registration processing log</span></span>

<span data-ttu-id="b042c-152">เมื่อต้องการตรวจสอบล็อกการประมวลผลการลงทะเบียน ให้ล็อกอินเข้าฮับ และไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ล็อกการประมวลผลการลงทะเบียนดิบ**</span><span class="sxs-lookup"><span data-stu-id="b042c-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="b042c-153">หน้า **ล็อกการประมวลผลการลงทะเบียนดิบ** จะแสดงรายการการลงทะเบียนดิบที่ประมวลผลและสถานะของการลงทะเบียนแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="b042c-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="b042c-154">![หน้าล็อกการประมวลผลการลงทะเบียนดิบ](media/mes-processing-log.png "หน้าล็อกการประมวลผลการลงทะเบียนดิบ")</span><span class="sxs-lookup"><span data-stu-id="b042c-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="b042c-155">คุณสามารถทำงานกับการลงทะเบียนใดก็ได้ในรายการ โดยเลือกการลงทะเบียน แล้วเลือกปุ่มอย่างใดอย่างหนึ่งต่อไปนี้ในบานหน้าต่างการดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="b042c-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b042c-156">**กระบวนการ** – ประมวลผลการลงทะเบียนที่เลือกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b042c-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="b042c-157">การดำเนินการนี้อาจเป็นประโยชน์ถ้างาน _ประมวลผลการลงทะเบียนดิบ_ ไม่ได้รันอยู่ หรือถ้าล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b042c-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="b042c-158">**ยกเลิก** – ยกเลิกการลงทะเบียนที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b042c-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="b042c-159">การทำงานกับปริมาณงานการดำเนินการผลิตบน scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="b042c-160">โดยทั่วไป กระบวนการที่จำเป็นในการรันปริมาณงานการดำเนินการผลิตจะรันโดยอัตโนมัติเพื่อเก็บฮับและ scale unit ทั้งหมดในการซิงค์ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="b042c-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b042c-161">อย่างไรก็ตาม ถ้าคุณกำลังประสบปัญหา คุณสามารถตรวจสอบประวัติของใบสั่งที่มีการประมวลผลไว้ใน scale unit หรือรันงาน _ตัวประมวลผลข้อความของฮับการดำเนินการผลิตไปยัง scale unit_</span><span class="sxs-lookup"><span data-stu-id="b042c-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="b042c-162">ดูประวัติของงานการผลิตที่มีการประมวลผลไว้ใน scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="b042c-163">เมื่อต้องการตรวจสอบประวัติของงานการผลิตที่มีการประมวลผลไว้ใน scale unit ให้ล็อกอินเข้าสู่เครื่องจักร scale unit และไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ประวัติการประมวลผลงานการผลิต**</span><span class="sxs-lookup"><span data-stu-id="b042c-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="b042c-164">หน้า **ประวัติการประมวลผลงานการผลิต** จะแสดงประวัติการประมวลผลของใบสั่งผลิตใน scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="b042c-165">คุณสามารถทำงานกับใบสั่งผลิตใดก็ได้ในรายการ โดยเลือกการลงทะเบียน แล้วเลือกปุ่มอย่างใดอย่างหนึ่งต่อไปนี้ในบานหน้าต่างการดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="b042c-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b042c-166">**กระบวนการ** – ประมวลผลใบสั่งผลิตที่เลือกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b042c-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="b042c-167">**ยกเลิก** – ยกเลิกใบสั่งผลิตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b042c-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="b042c-168">งานตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="b042c-169">งาน _ตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit_ ประมวลผลข้อมูลจากฮับไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="b042c-170">งานนี้จะเริ่มต้นโดยอัตโนมัติเมื่อมีการปรับใช้ปริมาณงานการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="b042c-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="b042c-171">อย่างไรก็ตาม คุณสามารถรันด้วยตนเองได้ตลอดเวลา โดยไปที่ **การควบคุมการผลิต \> งานประจำงวดของ \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit**</span><span class="sxs-lookup"><span data-stu-id="b042c-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="b042c-172">รายงานการเสร็จงานและการสำรองสินค้าบน scale unit</span><span class="sxs-lookup"><span data-stu-id="b042c-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="b042c-173">ในผลิตภัณฑ์ปัจจุบัน ให้รายงานการดําเนินงานเสร็จงานและขั้นตอนการสำรอง (สำหรับผลิตภัณฑ์สำเร็จรูป สินค้าร่วม และสินค้าพลอยได้) ได้รับการสนับสนุนโดย [ปริมาณงานการดําเนินงานของคลังสินค้า](cloud-edge-workload-warehousing.md) (ไม่ใช่ปริมาณงานการดําเนินการผลิต)</span><span class="sxs-lookup"><span data-stu-id="b042c-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="b042c-174">ดังนั้น เมื่อต้องการใช้ฟังก์ชันนี้เมื่อเชื่อมต่อกับ scale unit คุณต้องทำดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b042c-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="b042c-175">ติดตั้งทั้งปริมาณงานการปฏิบัติการของคลังสินค้าและปริมาณงานการปฏิบัติการผลิตบน scale unit ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b042c-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="b042c-176">ใช้แอป Warehouse Management บนมือถือเพื่อรายงานการเสร็จงานและประมวลผลงานการสำรอง</span><span class="sxs-lookup"><span data-stu-id="b042c-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="b042c-177">อินเทอร์เฟสการดำเนินการผลิตไม่สนับสนุนกระบวนการเหล่านี้ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b042c-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
