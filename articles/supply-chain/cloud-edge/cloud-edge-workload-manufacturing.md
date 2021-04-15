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
ms.openlocfilehash: a8c263104e209a81e33ea0db9e5fecddff3bc95b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809793"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="0ca52-103">ปริมาณงานการดำเนินการผลิตสำหรับ Cloud และ edge scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="0ca52-104">ฟังก์ชันธุรกิจบางอย่างไม่ได้รับการสนับสนุนอย่างเต็มที่ในตัวอย่างสำหรับสาธารณะเมื่อมีการใช้ปริมาณงาน scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-104">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="0ca52-105">ในการดำเนินการผลิต cloud and edge scale unit จัดส่งความสามารถต่อไปนี้ ถึงแม้ว่า edge unit จะไม่ได้เชื่อมต่อกับฮับ:</span><span class="sxs-lookup"><span data-stu-id="0ca52-105">In manufacturing execution, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the hub:</span></span>

- <span data-ttu-id="0ca52-106">ผู้ปฏิบัติงานเครื่องจักรและหัวหน้างานฝ่ายผลิตสามารถเข้าถึงแผนการผลิตที่มีการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-106">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="0ca52-107">ผู้ปฏิบัติงานในเครื่องสามารถรักษาแผนให้ทันสมัยอยู่เสมอโดยการรันงานการผลิตที่แยกต่างหากและมีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="0ca52-107">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="0ca52-108">หัวหน้างานฝ่ายผลิตสามารถปรับปรุงแผนการดำเนินงานได้</span><span class="sxs-lookup"><span data-stu-id="0ca52-108">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="0ca52-109">ผู้ปฏิบัติงานสามารถเข้าถึงเวลาและการเข้างานสำหรับการตอกบัตรเข้าและการตอกบัตรออกบน edge เพื่อให้มั่นใจว่าการคำนวณการจ่ายค่าจ้างของผู้ปฏิบัติงานถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0ca52-109">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="0ca52-110">หัวข้อนี้จะอธิบายวิธีการทำงานของปริมาณงานการดำเนินการผลิตกับ Cloud และ edge scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-110">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="0ca52-111">วงจรการผลิต</span><span class="sxs-lookup"><span data-stu-id="0ca52-111">The manufacturing lifecycle</span></span>

<span data-ttu-id="0ca52-112">ดังภาพที่แสดงต่อไปนี้ วงจรการผลิตจะถูกแบ่งออกเป็นสามระยะ ได้แก่ *วางแผน* *ดำเนินการ* และ *จบการทำงาน*</span><span class="sxs-lookup"><span data-stu-id="0ca52-112">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="0ca52-113">[![ระยะการดำเนินการผลิตเมื่อมีการใช้สภาพแวดล้อมเดียว](media/mes-phases.png "ระยะการดำเนินการผลิตเมื่อมีการใช้สภาพแวดล้อมเดียว")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="0ca52-113">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="0ca52-114">ระยะของ _แผน_ รวมถึงข้อกำหนดผลิตภัณฑ์ การวางแผน การสร้างใบสั่งและการจัดกำหนดการ และการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="0ca52-114">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="0ca52-115">ขั้นตอนการนำออกใช้บ่งชี้การเปลี่ยนจากระยะ _แผน_ ไปยังระยะ _ดำเนินการ_</span><span class="sxs-lookup"><span data-stu-id="0ca52-115">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="0ca52-116">เมื่อมีการนำใบสั่งผลิตออกใช้ งานใบสั่งผลิตจะมองเห็นได้บนชั้นการผลิตและพร้อมสำหรับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0ca52-116">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="0ca52-117">เมื่องานการผลิตถูกทำเครื่องหมายเป็นเสร็จสมบูรณ์แล้ว จะย้ายระยะ _การดำเนินการ_ ไปยังระยะ _การเสร็จสิ้น_</span><span class="sxs-lookup"><span data-stu-id="0ca52-117">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="0ca52-118">ในระยะ _การเสร็จสิ้น_ การลงทะเบียนจากระยะ *การดำเนินการ* จะเป็นไปตามลำดับงานการอนุมัติ ซึ่งถูกคำนวณ อนุมัติ และโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="0ca52-118">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="0ca52-119">ในจุดนั้น ใบสั่งผลิตจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0ca52-119">At that point, the production order is completed.</span></span> <span data-ttu-id="0ca52-120">ดังนั้น เกณฑ์สำหรับการจ่ายค่าจ้างของผู้ปฏิบัติงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0ca52-120">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="0ca52-121">การแบ่งระยะดำเนินการเป็นปริมาณงานที่แยกกัน</span><span class="sxs-lookup"><span data-stu-id="0ca52-121">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="0ca52-122">ดังภาพที่แสดงต่อไปนี้ เมื่อมีการใช้ scale unit ระยะ _การดำเนินการ_ จะถูกแบ่งออกเป็นปริมาณงานที่แยกกัน</span><span class="sxs-lookup"><span data-stu-id="0ca52-122">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="0ca52-123">[![ระยะการดำเนินการผลิตเมื่อมีการใช้ scale unit](media/mes-phases-workloads.png "ระยะการดำเนินการผลิตเมื่อมีการใช้ scale unit")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="0ca52-123">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="0ca52-124">แบบจำลองเดี๋ยวนี้จะมาจากการติดตั้งอินสแตนซ์เดียวกับแบบจำลองที่ยึดตามฮับและ scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-124">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="0ca52-125">ระยะ _แผน_ และ _การเสร็จสิ้น_ จะรันเป็นการดำเนินงานของฝ่ายสนับสนุนบนฮับ และปริมาณงานการดำเนินการผลิตจะรันบน scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-125">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="0ca52-126">ข้อมูลจะถูกโอนย้ายแบบอะซิงโครนัสระหว่างฮับและ scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-126">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="0ca52-127">เมื่อมีการนำใบสั่งผลิตออกใช้บนฮับ ข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการประมวลผลงานการผลิตจะถูกโอนย้ายไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-127">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="0ca52-128">ข้อมูลนี้รวมถึง ใบสั่งผลิต กระบวนการผลิต รายการวัสดุ และผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="0ca52-128">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="0ca52-129">ข้อมูลที่ไม่เกี่ยวข้องกับใบสั่งผลิต (เช่น กิจกรรมทางอ้อม รหัสการขาดงาน และพารามิเตอร์การผลิต) จะถูกโอนย้ายจากฮับไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-129">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="0ca52-130">ในฐานะที่เป็นกฎ ข้อมูลที่มีต้นกำเนิดมาจากฮับและมีการโอนย้ายไปยัง scale unit. สามารถสร้างหรืออัปเดตได้บนฮับเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ca52-130">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="0ca52-131">ตัวอย่างเช่น รหัสการขาดงานใหม่หรือกิจกรรมทางอ้อมไม่สามารถสร้างขึ้นบน scale unit&mdash;สามารถใช้สำหรับการลงทะเบียนได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0ca52-131">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="0ca52-132">การลงทะเบียนที่ทำบน scale unit ระหว่างการดำเนินการจะถูกโอนย้ายไปยังฮับ ซึ่งจะมีการประมวลผลการอนุมัติเวลาและการเข้างาน สินค้าคงคลัง และการอัปเดตทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="0ca52-132">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="0ca52-133">งานการดำเนินการผลิตที่สามารถรันบนปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-133">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="0ca52-134">สามารถรันงานการดำเนินการผลิตต่อไปนี้บนปริมาณงานเมื่อมีการใช้ scale unit:</span><span class="sxs-lookup"><span data-stu-id="0ca52-134">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="0ca52-135">การตอกบัตรเข้า ล็อกอิน การตอกบัตรออก และการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-135">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="0ca52-136">เริ่มต้นงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-136">Start job</span></span>
- <span data-ttu-id="0ca52-137">การรวมกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-137">Bundle jobs</span></span>
- <span data-ttu-id="0ca52-138">ความคืบหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-138">Report progress</span></span>
- <span data-ttu-id="0ca52-139">รายงานของเสีย</span><span class="sxs-lookup"><span data-stu-id="0ca52-139">Report scrap</span></span>
- <span data-ttu-id="0ca52-140">กิจกรรมทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="0ca52-140">Indirect activity</span></span>
- <span data-ttu-id="0ca52-141">ตัวแบ่ง</span><span class="sxs-lookup"><span data-stu-id="0ca52-141">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="0ca52-142">การทำงานกับปริมาณงานการดำเนินการผลิตบนฮับ</span><span class="sxs-lookup"><span data-stu-id="0ca52-142">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="0ca52-143">โดยทั่วไป กระบวนการที่จำเป็นในการรันปริมาณงานการดำเนินการผลิตจะรันโดยอัตโนมัติเพื่อเก็บฮับและ scale unit ทั้งหมดในการซิงค์ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ca52-143">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="0ca52-144">อย่างไรก็ตาม ถ้าคุณกำลังประสบปัญหา คุณสามารถทริกเกอร์การประมวลผลการลงทะเบียนดิบที่ได้รับจากปริมาณงาน และ/หรือ ตรวจสอบล็อกการประมวลผลการลงทะเบียนด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="0ca52-144">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="0ca52-145">ประมวลผลการลงทะเบียนดิบด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0ca52-145">Manually process raw registrations</span></span>

<span data-ttu-id="0ca52-146">ชุดงานใน Supply Chain Management จะรันโดยอัตโนมัติเพื่อประมวลผลการลงทะเบียนทั้งหมดที่ได้รับมาจากปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-146">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="0ca52-147">งานนี้จะสร้างสมุดรายวันการผลิตที่จำเป็นและรายการบันทึกเมื่อมีการประมวลผลการลงทะเบียนสำหรับงานที่เสร็จสมบูรณ์แล้วในปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="0ca52-147">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="0ca52-148">ถึงแม้ว่างานจะรันโดยอัตโนมัติ คุณสามารถรันด้วยตนเองได้ตลอดเวลาด้วยการล็อกอินเข้าฮับและไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ประมวลผลการลงทะเบียนดิบ**</span><span class="sxs-lookup"><span data-stu-id="0ca52-148">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="0ca52-149">ตรวจสอบล็อกการประมวลผลการลงทะเบียนดิบ</span><span class="sxs-lookup"><span data-stu-id="0ca52-149">Check the raw registration processing log</span></span>

<span data-ttu-id="0ca52-150">เมื่อต้องการตรวจสอบล็อกการประมวลผลการลงทะเบียน ให้ล็อกอินเข้าฮับ และไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ล็อกการประมวลผลการลงทะเบียนดิบ**</span><span class="sxs-lookup"><span data-stu-id="0ca52-150">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="0ca52-151">หน้า **ล็อกการประมวลผลการลงทะเบียนดิบ** จะแสดงรายการการลงทะเบียนดิบที่ประมวลผลและสถานะของการลงทะเบียนแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="0ca52-151">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="0ca52-152">![หน้าล็อกการประมวลผลการลงทะเบียนดิบ](media/mes-processing-log.png "หน้าล็อกการประมวลผลการลงทะเบียนดิบ")</span><span class="sxs-lookup"><span data-stu-id="0ca52-152">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="0ca52-153">คุณสามารถทำงานกับการลงทะเบียนใดก็ได้ในรายการ โดยเลือกการลงทะเบียน แล้วเลือกปุ่มอย่างใดอย่างหนึ่งต่อไปนี้ในบานหน้าต่างการดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="0ca52-153">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="0ca52-154">**กระบวนการ** – ประมวลผลการลงทะเบียนที่เลือกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0ca52-154">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="0ca52-155">การดำเนินการนี้อาจเป็นประโยชน์ถ้างาน _ประมวลผลการลงทะเบียนดิบ_ ไม่ได้รันอยู่ หรือถ้าล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="0ca52-155">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="0ca52-156">**ยกเลิก** – ยกเลิกการลงทะเบียนที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ca52-156">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="0ca52-157">การทำงานกับปริมาณงานการดำเนินการผลิตบน scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-157">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="0ca52-158">โดยทั่วไป กระบวนการที่จำเป็นในการรันปริมาณงานการดำเนินการผลิตจะรันโดยอัตโนมัติเพื่อเก็บฮับและ scale unit ทั้งหมดในการซิงค์ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="0ca52-158">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="0ca52-159">อย่างไรก็ตาม ถ้าคุณกำลังประสบปัญหา คุณสามารถตรวจสอบประวัติของใบสั่งที่มีการประมวลผลไว้ใน scale unit หรือรันงาน _ตัวประมวลผลข้อความของฮับการดำเนินการผลิตไปยัง scale unit_</span><span class="sxs-lookup"><span data-stu-id="0ca52-159">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="0ca52-160">ดูประวัติของงานการผลิตที่มีการประมวลผลไว้ใน scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-160">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="0ca52-161">เมื่อต้องการตรวจสอบประวัติของงานการผลิตที่มีการประมวลผลไว้ใน scale unit ให้ล็อกอินเข้าสู่เครื่องจักร scale unit และไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ประวัติการประมวลผลงานการผลิต**</span><span class="sxs-lookup"><span data-stu-id="0ca52-161">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="0ca52-162">หน้า **ประวัติการประมวลผลงานการผลิต** จะแสดงประวัติการประมวลผลของใบสั่งผลิตใน scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-162">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="0ca52-163">คุณสามารถทำงานกับใบสั่งผลิตใดก็ได้ในรายการ โดยเลือกการลงทะเบียน แล้วเลือกปุ่มอย่างใดอย่างหนึ่งต่อไปนี้ในบานหน้าต่างการดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="0ca52-163">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="0ca52-164">**กระบวนการ** – ประมวลผลใบสั่งผลิตที่เลือกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0ca52-164">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="0ca52-165">**ยกเลิก** – ยกเลิกใบสั่งผลิตที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ca52-165">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="0ca52-166">งานตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-166">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="0ca52-167">งาน _ตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit_ ประมวลผลข้อมูลจากฮับไปยัง scale unit</span><span class="sxs-lookup"><span data-stu-id="0ca52-167">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="0ca52-168">งานนี้จะเริ่มต้นโดยอัตโนมัติเมื่อมีการปรับใช้ปริมาณงานการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="0ca52-168">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="0ca52-169">อย่างไรก็ตาม คุณสามารถรันด้วยตนเองได้ตลอดเวลา โดยไปที่ **การควบคุมการผลิต \> งานประจำงวดของ \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit**</span><span class="sxs-lookup"><span data-stu-id="0ca52-169">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]