---
title: ให้คำแนะนำผสมความเป็นจริงสำหรับผู้ปฏิบัติงานในการผลิต
description: หัวข้อนี้อธิบายถึงวิธีการรวมโมดูลการจัดการการผลิตใน Microsoft Dynamics 365 Supply Chain Management ด้วย Dynamics 365 Guides
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 14645f592275d07a6b633146bb6da35b89c1bf77
ms.sourcegitcommit: 6d2fc497c8a7f49c48e7662995e27b5f8cc10296
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000989"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="8064c-103">ให้คำแนะนำผสมความเป็นจริงสำหรับผู้ปฏิบัติงานในการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="8064c-104">ผู้ปฏิบัติงานในกระบวนการผลิตจะได้รับประโยชน์จากคำแนะนำที่เกี่ยวข้อง ซึ่งมีให้ในเวลาที่เหมาะสมในบริบทของงานพวกเขา</span><span class="sxs-lookup"><span data-stu-id="8064c-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="8064c-105">*คำแนะนำ* นำไปใช้ในโดเมนต่างๆ ของงานได้ รวมถึง: แอสเซมบลี การบริการ การดำเนินงาน ใบรับรอง และความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="8064c-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="8064c-106">ฟังก์ชันธุรกิจหลักเหล่านี้ทั้งหมดในอีกด้าน คำแนะนำในการฝึกอบรมที่ต่อเนื่องจะช่วยให้ผู้ปฏิบัติงานสามารถทำงานได้อย่างมีประสิทธิภาพมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="8064c-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="8064c-107">คำนำ</span><span class="sxs-lookup"><span data-stu-id="8064c-107">Introduction</span></span>

<span data-ttu-id="8064c-108">คุณสามารถจัดเตรียมคำแนะนำได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="8064c-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="8064c-109">ระบบที่มีประสิทธิภาพหนึ่งที่จัดส่งนอกกรอบใช้ [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/)</span><span class="sxs-lookup"><span data-stu-id="8064c-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="8064c-110">Dynamics 365 Guides ช่วยเพิ่มศักยภาพพนักงานของคุณด้วยการเรียนรู้เชิงปฏิบัติได้</span><span class="sxs-lookup"><span data-stu-id="8064c-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="8064c-111">คุณสามารถกำหนดกระบวนการมาตรฐานที่มีคำแนะนำทีละขั้นตอน ที่แนะนำเครื่องมือและส่วนที่จำเป็นต้องใช้ให้กับพนักงานของคุณ และแสดงให้พนักงานทราบวิธีการใช้เครื่องมือเหล่านี้ในสถานการณ์การทำงานจริง</span><span class="sxs-lookup"><span data-stu-id="8064c-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="8064c-112">คุณสามารถแนบคู่มือกับแง่มุมต่างๆ ของการควบคุมการผลิต รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="8064c-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="8064c-113">ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-113">Resources</span></span>](#resources)
- [<span data-ttu-id="8064c-114">กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="8064c-115">ผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="8064c-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="8064c-116">สูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="8064c-117">เวอร์ชันสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="8064c-118">รายการวัสดุและส่วนประกอบ (BOM)</span><span class="sxs-lookup"><span data-stu-id="8064c-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="8064c-119">เวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="8064c-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="8064c-120">กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-120">Routes</span></span>](#routes)
- [<span data-ttu-id="8064c-121">เวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="8064c-122">ความสัมพันธ์ของการดำเนินงานกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="8064c-123">นอกจากนี้ คุณยังสามารถแนบคู่มือกับการจัดการสินทรัพย์ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8064c-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="8064c-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวเลือกนั้น ให้ดูที่ [รวม Dynamics 365 Supply Chain Management (การจัดการสินทรัพย์) ด้วย Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md)</span><span class="sxs-lookup"><span data-stu-id="8064c-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="8064c-125">เมื่อผู้ปฏิบัติงานแถวแรกเลือกงานของการผลิตผ่าน Supply Chain Management ผู้ปฏิบัติงานจะสามารถเห็น [คู่มือที่เกี่ยวข้อง](#logic) บนบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="8064c-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="8064c-126">เมื่อผู้ปฏิบัติงานเลือกคู่มือเฉพาะ รหัส QR สำหรับคู่มือนั้นจะแสดงขึ้นบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="8064c-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="8064c-127">จากนั้นผู้ปฏิบัติงานใช้ HoloLens เพื่อสแกนรหัส QR ซึ่งเปิดใช้งานคู่มือ และแสดงคำแนะนำที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8064c-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="8064c-128">ส่วนย่อยต่อไปนี้อธิบายสถานการณ์จำลองบางประการที่บริษัทในอุตสาหกรรมต่างๆ สามารถดูค่าที่ใหญ่ที่สุด เมื่อใช้คู่มือในการนำเสนอคำแนะนำในการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="8064c-129">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8064c-129">Assembly</span></span>

<span data-ttu-id="8064c-130">![การใช้คู่มือในงานแอสเซมบลี](media/instruction-guides-hero-assembly.png "การใช้คู่มือในงานการบริการ")</span><span class="sxs-lookup"><span data-stu-id="8064c-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="8064c-131">คำแนะนำในการดำเนินงานของแอสเซมบลีแสดงผู้ปฏิบัติงานเครื่องมือและส่วนที่จำเป็นต้องใช้ และวิธีการใช้งานในสถานการณ์งานจริง</span><span class="sxs-lookup"><span data-stu-id="8064c-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="8064c-132">ผู้จัดการฝ่ายผลิตสามารถสร้างและกำหนดคู่มือนำ ตัวอย่างเช่น สำหรับ [กระบวนการผลิต](routes-operations.md) [ความสัมพันธ์ของการดำเนินงาน](routes-operations.md#operation-relations) หรือ [รายการวัสดุและส่วนประกอบ](bill-of-material-bom.md)</span><span class="sxs-lookup"><span data-stu-id="8064c-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="8064c-133">ผู้ปฏิบัติงานจะพบคำแนะนำที่เกี่ยวข้องกับการดำเนินการที่เกี่ยวข้องกับการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="8064c-134">บริการ</span><span class="sxs-lookup"><span data-stu-id="8064c-134">Service</span></span>

<span data-ttu-id="8064c-135">![การใช้คู่มือในงานการบริการ](media/instruction-guides-hero-service.png "การใช้คู่มือในงานการบริการ")</span><span class="sxs-lookup"><span data-stu-id="8064c-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="8064c-136">จัดให้ช่างเทคนิคมีคำแนะนำที่แนะนำบนเว็บไซต์ของงาน ตัดความจำเป็นในการจัดกำหนดการเยี่ยมชมเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8064c-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="8064c-137">ผู้จัดการฝ่ายบริการสามารถกำหนดคู่มือได้ ตัวอย่างเช่น ระบุ [ผลิตภัณฑ์](../../commerce/product.md) ที่แนะนำขั้นตอนกิจวัตรการประเมินคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="8064c-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="8064c-138">คุณภาพ</span><span class="sxs-lookup"><span data-stu-id="8064c-138">Quality</span></span>

<span data-ttu-id="8064c-139">![ใช้คู่มือในงานการรับรองคุณภาพ](media/instruction-guides-hero-quality.png "ใช้คู่มือในงานการรับรองคุณภาพ")</span><span class="sxs-lookup"><span data-stu-id="8064c-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="8064c-140">เปิดตัวกระบวนการใหม่ และตรวจสอบให้แน่ใจว่ามีความสอดคล้องกันเพิ่มขึ้นด้วยการเปลี่ยนความรู้ของพนักงานเป็นเครื่องมือทำซ้ำ</span><span class="sxs-lookup"><span data-stu-id="8064c-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="8064c-141">ผู้จัดการการรับรองคุณภาพสามารถกำหนดคู่มือได้ ตัวอย่างเช่น ให้กับ [ผลิตภัณฑ์](../../commerce/product.md) ที่แนะนำขั้นตอนกิจวัตรการประเมินคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="8064c-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="8064c-142">ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="8064c-142">Certifications</span></span>

<span data-ttu-id="8064c-143">![ใช้คู่มือสำหรับงานที่เกี่ยวข้องกับใบรับรอง](media/instruction-guides-hero-certification.png "ใช้คู่มือสำหรับงานที่เกี่ยวข้องกับใบรับรอง")</span><span class="sxs-lookup"><span data-stu-id="8064c-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="8064c-144">ตรวจสอบให้แน่ใจว่าพนักงานทุกคนตรงตามมาตรฐานระดับสูงโดยการระบุว่าใครต้องการความช่วยเหลืออย่างไรและเมื่อใดอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="8064c-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="8064c-145">ด้านความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="8064c-145">Safety</span></span>

<span data-ttu-id="8064c-146">![ใช้คู่มือการทำงานในคำแนะนำด้านความปลอดภัยของงาน](media/instruction-guides-hero-safety.png "ใช้คู่มือการทำงานในคำแนะนำด้านความปลอดภัยของงาน")</span><span class="sxs-lookup"><span data-stu-id="8064c-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="8064c-147">ให้คำแนะนำที่แนะนำขั้นตอนที่เป็นอันตรายแบบเสมือนก่อนที่จะพยายามในสภาพแวดล้อมจริง</span><span class="sxs-lookup"><span data-stu-id="8064c-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="8064c-148">ด้วยวิธีการความจริงแบบผสม ผู้ปฏิบัติงานสามารถประสบขั้นตอนที่เป็นอันตรายได้แบบเสมือน</span><span class="sxs-lookup"><span data-stu-id="8064c-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="8064c-149">ผู้จัดการฝ่ายผลิตสามารถให้คำแนะนำการจัดการโดยเฉพาะสำหรับการจัดการวัสดุที่เป็นอันตราย หรือขั้นตอนการจัดการที่ละเอียดอ่อน โดยการกำหนดคำสั่งสำหรับ [รายการผลิตภัณฑ์](../../commerce/product.md) [กระบวนการผลิต](routes-operations.md) และ [การดำเนินงาน](routes-operations.md#operation-relations)</span><span class="sxs-lookup"><span data-stu-id="8064c-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="8064c-150">เริ่มต้นใช้งานด้วยคำแนะนำและคู่มือ</span><span class="sxs-lookup"><span data-stu-id="8064c-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="8064c-151">เมื่อต้องการเปิดใช้งานคำแนะนำในกระบวนการผลิต Supply Chain Management จะมีการรวมสำเร็จรูปด้วย Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="8064c-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="8064c-152">อินสแตนซ์ของโปรแกรมประยุกต์ที่ได้รับอนุญาตและติดตั้งแล้วของ Guides จำเป็นต้องใช้ เพื่อสร้าง รักษา และกำหนดคำแนะนำความจริงผสมให้กับสินทรัพย์และการทำงานของการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8064c-153">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8064c-153">Prerequisites</span></span>

<span data-ttu-id="8064c-154">เมื่อต้องการใช้คุณลักษณะนี้ ระบบของคุณต้องรวมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8064c-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="8064c-155">Dynamics 365 Supply Chain Management รุ่น 10.0.15 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="8064c-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="8064c-156">[การรวมแบบสองทิศทาง](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) สำหรับแอป Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8064c-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="8064c-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) รุ่น 400.0.1.48 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="8064c-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="8064c-158">เปิดคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="8064c-158">Turn on the feature</span></span>

<span data-ttu-id="8064c-159">คุณต้องเปิดใช้งานคีย์การตั้งค่าคอนฟิกเพื่อให้สามารถใช้คุณลักษณะได้ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="8064c-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="8064c-160">คุณจำเป็นต้องดำเนินการนี้ครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8064c-160">You only need to do this once.</span></span> <span data-ttu-id="8064c-161">เมื่อต้องการดำเนินการดังกล่าว ผู้ดูแลระบบต้องทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8064c-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="8064c-162">วางระบบของคุณให้เข้าสู่โหมดการบำรุงรักษาตามที่อธิบายไว้ใน [โหมดการบำรุงรักษา](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)</span><span class="sxs-lookup"><span data-stu-id="8064c-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="8064c-163">ไปที่ **การจัดการระบบ \> การตั้งค่า \> การตั้งค่าคอนฟิกลิขสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="8064c-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="8064c-164">ขยายส่วนของ **ความเป็นจริงผสม** แล้วเลือกกล่องกาเครื่องหมาย **คู่มือความเป็นจริงผสม**</span><span class="sxs-lookup"><span data-stu-id="8064c-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="8064c-165">ขยายส่วนของ **การจัดการการผลิต** แล้วเลือกกล่องกาเครื่องหมาย **คำแนะนำการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="8064c-166">ปิดโหมดการบำรุงรักษาตามที่อธิบายไว้ใน [โหมดการบำรุงรักษา](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)</span><span class="sxs-lookup"><span data-stu-id="8064c-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="8064c-167">ตั้งค่าคอนฟิกแนวทางที่คู่มือจะปรากฏในการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="8064c-168">หากต้องการตั้งค่าคอนฟิกคู่มือให้ปรากฏในการผลิต ให้ไปที่ **ความเป็นจริงผสม \> Dynamics 365 Guides \> ตั้งค่าคอนฟิกการรวมคู่มือ**</span><span class="sxs-lookup"><span data-stu-id="8064c-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="8064c-169">![ตั้งค่าคอนฟิกการรวมคู่มือสำหรับการผลิต](media/instruction-guides-configure-integration.png "ตั้งค่าคอนฟิกการรวมคู่มือสำหรับการผลิต")</span><span class="sxs-lookup"><span data-stu-id="8064c-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="8064c-170">ตั้งค่าฟิลด์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8064c-170">Set the following fields:</span></span>

- <span data-ttu-id="8064c-171">**โดเมนย่อยของ Common Data Service**  - ฟิลด์นี้ควรแสดงค่าอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="8064c-171">**Common Data Service subdomain** - This field should already show a value.</span></span> <span data-ttu-id="8064c-172">ฟิลด์นี้จัดเก็บโดเมนย่อยสำหรับสภาพแวดล้อม Common Data Service ที่คุณสร้างคู่มือของคุณ</span><span class="sxs-lookup"><span data-stu-id="8064c-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="8064c-173">โดเมนย่อยเป็นส่วนแรกของ URL และโดยทั่วไปจะมีการตั้งชื่อตามองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="8064c-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="8064c-174">ตัวอย่าง เช่นถ้า URL ของคุณ Common Data Service เป็น "contoso.crm4.dynamics.com" คุณควรป้อน *contoso* ที่นี่</span><span class="sxs-lookup"><span data-stu-id="8064c-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="8064c-175">ค่านี้จะใช้ในการสร้างที่อยู่สำหรับคู่มือของคุณ และจะถูกเข้ารหัสเป็นรหัส QR</span><span class="sxs-lookup"><span data-stu-id="8064c-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="8064c-176">**ขนาดรหัส QR** - ตั้งค่าขนาดของรหัส QR ที่แสดง</span><span class="sxs-lookup"><span data-stu-id="8064c-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="8064c-177">เราขอแนะนำให้คุณเลือกขนาดที่จะเต็มหน้าจอการแสดงผลส่วนใหญ่ของคุณ แต่ไม่มากกว่า</span><span class="sxs-lookup"><span data-stu-id="8064c-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="8064c-178">โดยทั่วไป *15* เป็นค่าที่ดี</span><span class="sxs-lookup"><span data-stu-id="8064c-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="8064c-179">**ระดับการแก้ไขข้อผิดพลาดของรหัส QR** - ตั้งค่าส่วนประกอบของรหัส QR</span><span class="sxs-lookup"><span data-stu-id="8064c-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="8064c-180">ส่วนประกอบที่สูงขึ้นสามารถช่วยเพิ่มความน่าเชื่อถือของรหัสได้ แต่ **ขนาดของรหัส QR** ของคุณต้องมีขนาดใหญ่พอที่จะรองรับระดับของรายละเอียดที่จำเป็นต้องใช้โดยระดับการแก้ไขที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="8064c-181">ขนาดของรหัส QR ที่มีขนาดใหญ่เกินกว่าที่จะแสดงผลของคุณจะใช้เวลานานกว่าในการแสดงผล และปรับสเกลให้พอดีกับจอแสดงผลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8064c-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="8064c-182">สิ่งเหล่านี้ไม่ได้ให้ผลประโยชน์</span><span class="sxs-lookup"><span data-stu-id="8064c-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="8064c-183">ขนาดรหัส QR ที่เล็กเกินไปอาจลดความสามารถในการอ่านรหัสของ HoloLens อย่างถูกต้องในบางสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8064c-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="8064c-184">เราขอแนะนำให้คุณทดสอบการตั้งค่าสำหรับอุปกรณ์แต่ละรายการที่จะแสดงรหัส QR สำหรับผู้ใช้ HoloLens</span><span class="sxs-lookup"><span data-stu-id="8064c-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="8064c-185">เลือกการตั้งค่าที่ให้การอ่านได้เพียงพอในสภาพแวดล้อมการผลิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="8064c-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="8064c-186">เรียกดูภาพรวมของการกำหนดคู่มือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8064c-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="8064c-187">ใช้หน้า **คู่มือทั้งหมด** เพื่อดูรายการของคู่มือทั้งหมดที่มีอยู่ในองค์กรของคุณ และการกำหนดทั้งหมดให้กับกระบวนการผลิตและทรัพยากรของคุณ</span><span class="sxs-lookup"><span data-stu-id="8064c-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="8064c-188">เมื่อต้องการเปิด ให้ไปที่ **ความเป็นจริงผสม \> คู่มือ \> คู่มือทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8064c-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="8064c-189">รายการที่อยู่ด้านบนจะแสดงคู่มือที่มีอยู่ทั้งหมด และคุณสามารถใช้ฟิลด์นี้เพื่อกรองข้อมูลรายการได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="8064c-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="8064c-190">รายการที่อยู่ด้านล่างแสดงการกำหนดคู่มือทั้งหมด และแสดงแถบเครื่องมือสำหรับการจัดการ</span><span class="sxs-lookup"><span data-stu-id="8064c-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="8064c-191">![จัดการคู่มือ](media/instruction-guides-allguides.png "จัดการคู่มือ")</span><span class="sxs-lookup"><span data-stu-id="8064c-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="8064c-192">หัวข้อต่อไปนี้อธิบายถึงชนิดของออบเจ็กต์ที่คุณสามารถกำหนดคู่มือให้ได้</span><span class="sxs-lookup"><span data-stu-id="8064c-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="8064c-193">คำแนะนำที่กำหนดแต่ละรายการจะให้คำแนะนำที่แนบกับงานการผลิตที่เกี่ยวข้องโดยอัตโนมัติ และจะพร้อมใช้งานในการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="8064c-194">เชื่อมโยงคู่มือกับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="8064c-195">เพิ่มคู่มือให้กับ [ทรัพยากร](operations-resources.md) เพื่อให้คู่มือในบริบทของงานการผลิตที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8064c-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="8064c-196">สถานการณ์จำลองทั่วไปโดยใช้ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-196">Typical scenario using resources</span></span>

<span data-ttu-id="8064c-197">ตัวอย่างเช่น คุณสามารถแนบคู่มือกับความปลอดภัยของเครื่องจักรทั่วไป หรือขั้นตอนการจัดการกับทรัพยากรชนิดเครื่องจักรได้</span><span class="sxs-lookup"><span data-stu-id="8064c-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="8064c-198">คู่มือจะพร้อมใช้งานในทุกงานที่ดำเนินการบนเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="8064c-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="8064c-199">เพื่มคู่มือให้ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-199">Add a Guide to a resource</span></span>

<span data-ttu-id="8064c-200">หากต้องการเพื่มคู่มือให้ทรัพยากร:</span><span class="sxs-lookup"><span data-stu-id="8064c-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="8064c-201">ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> ทรัพยากร \> ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8064c-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="8064c-202">จากบานหน้าต่างแสดงรายการ ให้เลือกทรัพยากรที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-203">ขยายแท็บด่วน **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="8064c-204">เลือก **เพิ่ม** จากแถบเครื่องมือ **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="8064c-205">มีการเพิ่มบรรทัดใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="8064c-206">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="8064c-207">ถ้าคุณมีคู่มือจำนวนมาก คุณก็สามารถกรองรายการนั้นเพื่อค้นหารายการที่คุณกำลังค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="8064c-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="8064c-208">![จัดการคู่มือ](media/instruction-guides-allguides.png "จัดการคู่มือ")</span><span class="sxs-lookup"><span data-stu-id="8064c-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="8064c-209">เชื่อมโยงคู่มือกับกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="8064c-210">คุณสามารถเพิ่มคู่มือให้กับ [กลุ่มทรัพยากร](tasks/define-discrete-manufacturing-resource-group.md) ถ้าคุณใช้เพื่อจัดการกลุ่มของเครื่องจักร สายการผลิต หรือเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8064c-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="8064c-211">สถานการณ์จำลองทั่วไปโดยใช้กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="8064c-212">**ตัวอย่างที่ 1:** คุณได้กำหนดกลุ่มทรัพยากรสำหรับหลายเครื่องจักรของแบบจำลองเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8064c-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="8064c-213">แทนที่จะกำหนดคู่มือแนะนำการจัดการที่เกี่ยวข้องสำหรับแบบจำลองเครื่องจักรให้กับทรัพยากรที่เกี่ยวข้องทั้งหมด คุณสามารถกำหนดคู่มือให้กับกลุ่มทรัพยากรที่แสดงถึงแบบจำลองเครื่องจักรแทนได้</span><span class="sxs-lookup"><span data-stu-id="8064c-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="8064c-214">**ตัวอย่างที่ 2:** คุณได้กำหนดกลุ่มทรัพยากรสำหรับเซลล์ทำงานที่มีเครื่องจักรแตกต่างกัน และคุณมีคู่มือที่จะให้คำแนะนำโดยทั่วไปเกี่ยวกับวิธีการรักษาเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8064c-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="8064c-215">คู่มือสามารถนำไปใช้กับกิจกรรมการผลิตใดๆ ในเซลล์ทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="8064c-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="8064c-216">เพิ่มคู่มือให้กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="8064c-217">หากต้องการเพิ่มคู่มือให้กลุ่มทรัพยากร:</span><span class="sxs-lookup"><span data-stu-id="8064c-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="8064c-218">ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> ทรัพยากร \> กลุ่มทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8064c-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="8064c-219">จากบานหน้าต่างแสดงรายการ ให้เลือกกลุ่มทรัพยากรที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-220">ขยายแท็บด่วน **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="8064c-221">เลือก **เพิ่ม** จากแถบเครื่องมือ **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="8064c-222">มีการเพิ่มบรรทัดใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="8064c-223">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="8064c-224">ถ้าคุณมีคู่มือจำนวนมาก คุณก็สามารถกรองรายการนั้นเพื่อค้นหารายการที่คุณกำลังค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="8064c-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="8064c-225">![การเพิ่มคู่มือกับกลุ่มทรัพยากร](media/instruction-guides-resourcegroup.png "การเพิ่มคู่มือกับกลุ่มทรัพยากร")</span><span class="sxs-lookup"><span data-stu-id="8064c-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="8064c-226">เชื่อมโยงคู่มือกับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="8064c-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="8064c-227">คุณสามารถเพิ่มคู่มือให้กับ [ผลิตภัณฑ์ที่นำออกใช้](../pim/tasks/create-released-product-single-company.md) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="8064c-228">สถานการณ์จำลองทั่วไปโดยใช้ผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="8064c-228">Typical scenario using released products</span></span>

<span data-ttu-id="8064c-229">คู่มือระดับผลิตภัณฑ์ให้คำแนะนำแก่ผู้ปฏิบัติงานเกี่ยวข้องกับการดำเนินงาน หรือการจัดการผลิตภัณฑ์หรือสินค้าที่นำออกใช้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8064c-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="8064c-230">เพิ่มคู่มือกับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="8064c-230">Add a Guide to a released product</span></span>

<span data-ttu-id="8064c-231">หากต้องการเพิ่มคู่มือกับผลิตภัณฑ์ที่นำออกใช้:</span><span class="sxs-lookup"><span data-stu-id="8064c-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="8064c-232">ไปยัง **การจัดการข้อมูลการผลิต \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="8064c-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8064c-233">เปิดผลิตภัณฑ์ที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-234">ในบานหน้าต่างการดำเนินการ ให้เปิดแท็บ **วิศวกรรม** และ จากกลุ่ม **ดู** ให้เลือก **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="8064c-235">หน้า **คู่มือที่เชื่อมโยง** เปิดขึ้นสำหรับผลิตภัณฑ์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="8064c-236">ให้เลือก **เพิ่ม** ในบานหน้าต่างการดำเนินการ เพื่อเพิ่มรายการใหม่ไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="8064c-237">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-238">![การเพิ่มคู่มือกับผลิตภัณฑ์ที่นำออกใช้](media/instruction-guides-ReleasedProduct-AddGuides.png "การเพิ่มคู่มือกับผลิตภัณฑ์ที่นำออกใช้")</span><span class="sxs-lookup"><span data-stu-id="8064c-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="8064c-239">เชื่อมโยงคู่มือกับสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="8064c-240">คุณสามารถเพิ่มคู่มือให้กับ [สูตร](bill-of-material-bom.md#formulas-co-products-and-by-products) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="8064c-241">สถานการณ์จำลองทั่วไปโดยใช้สูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="8064c-242">คู่มือระดับสูตรช่วยให้คำแนะนำแก่ผู้ปฏิบัติงานเกี่ยวข้องกับการดำเนินงาน หรือการจัดการในบริบทของสูตรหรือสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="8064c-243">นอกจากนี้คู่มือยังสามารถกำหนดให้กับรุ่นของสูตรได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8064c-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="8064c-244">คุณสามารถกำหนดคำแนะนำที่เกี่ยวข้องกับกระบวนการผลิตตามสูตรกับกระบวนการผลิต รุ่นกระบวนการผลิต หรือความสัมพันธ์ของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="8064c-245">คู่มือไม่สามารถแนบกับรายการสูตรแต่ละรายการได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8064c-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="8064c-246">เพื่มคู่มือให้สูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-246">Add a Guide to a formula</span></span>

<span data-ttu-id="8064c-247">หากต้องการเพื่มคู่มือให้สูตร:</span><span class="sxs-lookup"><span data-stu-id="8064c-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="8064c-248">ไปที่ **การจัดการข้อมูลการผลิต \> สูตรและสูตรการผลิต \> สูตร**</span><span class="sxs-lookup"><span data-stu-id="8064c-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="8064c-249">เปิดสูตรที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-250">เปิดแท็บ **ส่วนหัว** ด้านบนแท็บด่วน</span><span class="sxs-lookup"><span data-stu-id="8064c-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="8064c-251">ขยายแท็บด่วน **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="8064c-252">เลือก **เพิ่ม** จากแถบเครื่องมือ **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="8064c-253">มีการเพิ่มบรรทัดใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="8064c-254">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-255">![การเพิ่มคู่มือให้สูตร](media/instruction-guides-Formula.png "การเพิ่มคู่มือให้สูตร")</span><span class="sxs-lookup"><span data-stu-id="8064c-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="8064c-256">เชื่อมโยงคู่มือกับรุ่นของสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="8064c-257">คุณสามารถเพิ่มคู่มือให้กับ [รุ่นของสูตร](bill-of-material-bom.md#bom-and-formula-versions) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="8064c-258">สถานการณ์จำลองทั่วไปโดยใช้รุ่นของสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="8064c-259">คู่มือที่แนบมากับสูตรแต่ละรุ่นให้คำแนะนำแก่ผู้ปฏิบัติงานเกี่ยวกับการผลิตของรุ่นของสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="8064c-260">คุณสามารถกำหนดคำแนะนำที่เกี่ยวข้องกับกระบวนการผลิตตามรุ่นของสูตรนี้กับกระบวนการผลิต รุ่นกระบวนการผลิต หรือความสัมพันธ์ของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="8064c-261">คู่มือไม่สามารถแนบกับรายการสูตรแต่ละรายการได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8064c-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="8064c-262">เพิ่มคู่มือให้รุ่นของสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="8064c-263">หากต้องการเพิ่มคู่มือให้รุ่นของสูตร:</span><span class="sxs-lookup"><span data-stu-id="8064c-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="8064c-264">ไปที่ **การจัดการข้อมูลการผลิต \> สูตรและสูตรการผลิต \> สูตร**</span><span class="sxs-lookup"><span data-stu-id="8064c-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="8064c-265">เปิดสูตรที่มีรุ่นที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-266">เปิดแท็บ **ส่วนหัว** ด้านบนแท็บด่วน</span><span class="sxs-lookup"><span data-stu-id="8064c-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="8064c-267">บนแท็บด่วน **รุ่นของสูตร** ให้เลือกรุ่นที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-268">บนแถบเครื่องมือ **รุ่นของสูตร** ให้เลือก **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="8064c-269">![เปิดคู่มือที่เชื่อมโยงกับรุ่นของสูตรที่เลือก](media/instruction-guides-FormulaVersion.png "เปิดคู่มือที่เชื่อมโยงกับรุ่นของสูตรที่เลือก")</span><span class="sxs-lookup"><span data-stu-id="8064c-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="8064c-270">หน้า **คู่มือที่เชื่อมโยง** เปิดขึ้นสำหรับรุ่นของสูตรที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="8064c-271">ให้เลือก **เพิ่ม** ในบานหน้าต่างการดำเนินการ เพื่อเพิ่มรายการใหม่ไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="8064c-272">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-273">![การเพิ่มคู่มือให้รุ่นของสูตร](media/instruction-guides-FormulaVersionAddGuide.png "การเพิ่มคู่มือให้รุ่นของสูตร")</span><span class="sxs-lookup"><span data-stu-id="8064c-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="8064c-274">เชื่อมโยงคู่มือกับสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="8064c-275">คุณสามารถเพิ่มคู่มือให้กับ [สูตรการผลิต](bill-of-material-bom.md) (BOM) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="8064c-276">สถานการณ์จำลองทั่วไปโดยใช้สูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="8064c-277">คู่มือที่แนบกับ BOM ให้คำแนะนำแก่ผู้ปฏิบัติงานที่อธิบายวิธีการจัดเตรียมและจัดการวัสดุจาก BOM</span><span class="sxs-lookup"><span data-stu-id="8064c-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="8064c-278">นอกจากนี้คู่มือยังสามารถกำหนดให้กับรุ่นของ BOM ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8064c-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="8064c-279">คู่มือไม่สามารถแนบกับรายการสูตรแต่ละรายการ BOM ได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8064c-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="8064c-280">เพิ่มคู่มือกับสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="8064c-281">หากต้องการเพิ่มคู่มือกับสูตรการผลิต:</span><span class="sxs-lookup"><span data-stu-id="8064c-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="8064c-282">ไปที่ **การจัดการข้อมูลการผลิต \> สูตรและสูตรการผลิต \> สูตรการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="8064c-283">เปิดสูตรการผลิตที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-284">เปิดแท็บ **ส่วนหัว** ด้านบนแท็บด่วน</span><span class="sxs-lookup"><span data-stu-id="8064c-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="8064c-285">ขยายแท็บด่วน **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="8064c-286">เลือก **เพิ่ม** จากแถบเครื่องมือ **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="8064c-287">มีการเพิ่มบรรทัดใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="8064c-288">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-289">![การเพิ่มคู่มือให้ BOM](media/instruction-guides-BOM.png "การเพิ่มคู่มือให้ BOM")</span><span class="sxs-lookup"><span data-stu-id="8064c-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="8064c-290">เชื่อมโยงคู่มือกับรุ่นของสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="8064c-291">คุณสามารถเพิ่มคู่มือให้กับ [รุ่นของสูตรการผลิต](bill-of-material-bom.md#bom-and-formula-versions) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="8064c-292">สถานการณ์จำลองทั่วไปโดยใช้รุ่นของสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="8064c-293">คู่มือที่แนบกับรุ่นของ BOM แต่ละรายการจะให้คำแนะนำแก่ผู้ปฏิบัติงานที่อธิบายวิธีการจัดเตรียมและจัดการวัสดุสำหรับรุ่นของ BOM ที่แตกต่างจาก BOM ทั่วไป หรือรุ่นอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="8064c-294">คู่มือไม่สามารถแนบกับรายการสูตรแต่ละรายการ BOM ได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8064c-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="8064c-295">เพิ่มคู่มือกับรุ่นของสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="8064c-296">หากต้องการเพิ่มคู่มือกับรุ่นของสูตรการผลิต:</span><span class="sxs-lookup"><span data-stu-id="8064c-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="8064c-297">ไปที่ **การจัดการข้อมูลการผลิต \> สูตรและสูตรการผลิต \> สูตรการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="8064c-298">เปิด BOM ที่มีรุ่นที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-299">เปิดแท็บ **ส่วนหัว** ด้านบนแท็บด่วน</span><span class="sxs-lookup"><span data-stu-id="8064c-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="8064c-300">บนแท็บด่วน **รุ่นของ BOM** ให้เลือกรุ่นที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-301">บนแถบเครื่องมือ **รุ่นของ BOM** ให้เลือก **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="8064c-302">![เปิดคู่มือที่เชื่อมโยงกับรุ่นของ BOM ที่เลือก](media/instruction-guides-BOMVersion.png "เปิดคู่มือที่เชื่อมโยงกับรุ่นของ BOM ที่เลือก")</span><span class="sxs-lookup"><span data-stu-id="8064c-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="8064c-303">หน้า **คู่มือที่เชื่อมโยง** เปิดขึ้นสำหรับรุ่นของ BOM ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="8064c-304">ให้เลือก **เพิ่ม** ในบานหน้าต่างการดำเนินการ เพื่อเพิ่มรายการใหม่ไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="8064c-305">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-306">![การเพิ่มคู่มือให้รุ่นของ BOM](media/instruction-guides-BOMVersionAddGuide.png "การเพิ่มคู่มือให้รุ่นของ BOM")</span><span class="sxs-lookup"><span data-stu-id="8064c-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="8064c-307">เชื่อมโยงคู่มือกับกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-307">Associate a Guide to a route</span></span>

<span data-ttu-id="8064c-308">คุณสามารถเพิ่มคู่มือให้กับ [กระบวนการผลิต](routes-operations.md) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="8064c-309">สถานการณ์จำลองทั่วไปโดยใช้กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-309">Typical scenario using routes</span></span>

<span data-ttu-id="8064c-310">โดยทั่วไปแล้วกระบวนการผลิตจะใช้ในการระบุว่าผลิตภัณฑ์ที่นำออกใช้จะมีการผลิตตาม BOM หรือรุ่นของ BOM อย่างไร และด้วยชุดทรัพยากรหรือกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="8064c-311">กำหนดคู่มือให้กับกระบวนการผลิตเพื่อให้คำแนะนำทีละขั้นตอนสำหรับกระบวนการผลิตที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8064c-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="8064c-312">เพื่มคู่มือให้กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-312">Add a Guide to a route</span></span>

<span data-ttu-id="8064c-313">หากต้องการเพิ่มคู่มือให้กระบวนการผลิต:</span><span class="sxs-lookup"><span data-stu-id="8064c-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="8064c-314">ไปที่การ **การควบคุมการผลิต \> ทั้งหมดกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="8064c-315">เปิดกระบวนการผลิตที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-316">ขยายแท็บด่วน **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="8064c-317">เลือก **เพิ่ม** จากแถบเครื่องมือ **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="8064c-318">มีการเพิ่มบรรทัดใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="8064c-319">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-320">![การเพิ่มคู่มือให้กระบวนการผลิต](media/instruction-guides-Route.png "การเพิ่มคู่มือให้กระบวนการผลิต")</span><span class="sxs-lookup"><span data-stu-id="8064c-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="8064c-321">เชื่อมโยงคู่มือกับรุ่นของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="8064c-322">คุณสามารถเพิ่มคู่มือให้กับ [รุ่นของกระบวนการผลิต](routes-operations.md#route-versions) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="8064c-323">สถานการณ์จำลองทั่วไปโดยใช้รุ่นของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-323">Typical scenario using route versions</span></span>

<span data-ttu-id="8064c-324">โดยทั่วไปจะใช้รุ่นของกระบวนการผลิตเพื่อระบุตัวแปรของกระบวนการผลิตตามกระบวนการผลิตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8064c-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="8064c-325">คุณสามารถกำหนดคู่มือต่างๆ ให้กับรุ่นของกระบวนการผลิตแต่ละรุ่นได้</span><span class="sxs-lookup"><span data-stu-id="8064c-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="8064c-326">เพิ่มคู่มือให้รุ่นของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-326">Add a Guide to a route version</span></span>

<span data-ttu-id="8064c-327">หากต้องการเพิ่มคู่มือให้รุ่นของกระบวนการผลิต:</span><span class="sxs-lookup"><span data-stu-id="8064c-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="8064c-328">ไปที่การ **การควบคุมการผลิต \> ทั้งหมดกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="8064c-329">เปิดกระบวนการผลิตที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-330">บนแท็บด่วน **รุ่น** ให้เลือกรุ่นที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-331">บนแถบเครื่องมือ **รุ่น** ให้เลือก **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="8064c-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="8064c-332">![เปิดคู่มือที่เชื่อมโยงกับรุ่นของกระบวนการผลิตที่เลือก](media/instruction-guides-RouteVersion.png "เปิดคู่มือที่เชื่อมโยงกับรุ่นของกระบวนการผลิตที่เลือก")</span><span class="sxs-lookup"><span data-stu-id="8064c-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="8064c-333">หน้า **คู่มือที่เชื่อมโยง** เปิดขึ้นสำหรับรุ่นของ BOM ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="8064c-334">ให้เลือก **เพิ่ม** ในบานหน้าต่างการดำเนินการ เพื่อเพิ่มรายการใหม่ไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="8064c-335">สำหรับรายการใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="8064c-336">![การเพิ่มคู่มือให้รุ่นของกระบวนการผลิต](media/instruction-guides-RouteVersionAddGuide.png "การเพิ่มคู่มือให้รุ่นของกระบวนการผลิต")</span><span class="sxs-lookup"><span data-stu-id="8064c-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="8064c-337">เชื่อมโยงคู่มือกับความสัมพันธ์ของการดำเนินงานกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="8064c-338">คุณสามารถเพิ่มคู่มือให้กับ [ความสัมพันธ์ของการดำเนินงานกระบวนการผลิต](routes-operations.md#operation-relations) ใดๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="8064c-339">สถานการณ์ปกติโดยใช้ความสัมพันธ์ของการดำเนินงานของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="8064c-340">ความสัมพันธ์ของการดำเนินงานเป็นวิธีการที่เฉพาะเจาะจงที่สุดในการเพิ่มคำแนะนำให้กับกระบวนการผลิตและการดำเนินงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8064c-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="8064c-341">คุณสามารถระบุคำแนะนำสำหรับแต่ละการดำเนินงานในกระบวนการผลิต และระบุคำแนะนำต่างๆ สำหรับบริบทความสัมพันธ์ชนิดใดๆ ที่ระบุไว้สำหรับกระบวนการผลิต เช่น สำหรับสินค้าเฉพาะ การตั้งค่าคอนฟิก และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8064c-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="8064c-342">นอกจากนี้คุณยังสามารถระบุถึงระยะที่อยู่ในการดำเนินงานที่จะใช้คำแนะนำ (เช่น การตั้งค่า คิว ประมวลผล หรือการขนส่ง)</span><span class="sxs-lookup"><span data-stu-id="8064c-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="8064c-343">ถ้าคุณระบุคู่มือสำหรับความสัมพันธ์ของการดำเนินงานหลายอย่างของกระบวนการผลิต ในระหว่างคู่มือดังกล่าว เฉพาะคำแนะนำจากความสัมพันธ์เฉพาะที่สุดเท่านั้นจะแสดงในการผลิตสำหรับงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8064c-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="8064c-344">เพิ่มคู่มือกับความสัมพันธ์ของการดำเนินงานกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="8064c-345">หากต้องการเพิ่มคู่มือกับความสัมพันธ์ของการดำเนินงานกระบวนการผลิต:</span><span class="sxs-lookup"><span data-stu-id="8064c-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="8064c-346">ไปที่การ **การควบคุมการผลิต \> ทั้งหมดกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="8064c-347">เปิดกระบวนการผลิตที่คุณต้องการกำหนดคู่มือให้</span><span class="sxs-lookup"><span data-stu-id="8064c-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="8064c-348">ในบานหน้าต่างการดำเนินการ ให้เปิดแท็บ **กระบวนการผลิต** และ จากกลุ่ม **รักษา** ให้เลือก **รายละเอียดกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8064c-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="8064c-349">หน้า **รายละเอียดกระบวนการผลิต** จะเปิดขึ้นสำหรับกระบวนการผลิตที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="8064c-350">ในกริดบนสุด ให้เลือกการดำเนินงานที่คุณต้องการให้คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="8064c-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="8064c-351">ในกริดด้านล่าง ให้เลือกความสัมพันธ์เฉพาะ (หรือความสัมพันธ์ **ทั้งหมด** แบบทั่วไป)</span><span class="sxs-lookup"><span data-stu-id="8064c-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="8064c-352">![เลือกการดำเนินงานและความสัมพันธ์](media/instruction-guides-RouteOperationRelation.png "เลือกการดำเนินงานและความสัมพันธ์")</span><span class="sxs-lookup"><span data-stu-id="8064c-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="8064c-353">ด้านบนกริดด้านล่าง ให้เปิดแท็บ **คู่มือที่เชื่อมโยง** ![แท็บคู่มือที่เชื่อมโยง](media/instruction-guides-RouteOperationRelation-AddGuide.png "แท็บคู่มือที่เชื่อมโยง")</span><span class="sxs-lookup"><span data-stu-id="8064c-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="8064c-354">เลือก **เพิ่ม** จากแถบเครื่องมือที่ด้านบนของกริดด้านล่างเพื่อเพิ่มรายการใหม่ลงในกริด</span><span class="sxs-lookup"><span data-stu-id="8064c-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="8064c-355">สำหรับแถวใหม่ ให้ใช้รายการแบบหล่นลงในคอลัมน์ **ชื่อ** เพื่อเลือกคู่มือที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="8064c-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="8064c-356">ในส่วนที่เหลือของแถว ให้เลือกกล่องกาเครื่องหมายสำหรับแต่ละบริบทที่ควรมีคู่มือที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8064c-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="8064c-357">คุณสามารถเพิ่มคู่มือหนึ่งรายการขึ้นไปสำหรับแต่ละขั้นตอนของการดำเนินงานแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="8064c-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="8064c-358">เลือกคู่มือจากส่วนติดต่อการดําเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="8064c-359">เมื่อผู้ปฏิบัติงานเปิดรายการงานบนส่วนติดต่อการดําเนินการผลิต Supply Chain Management พบคู่มือที่เกี่ยวข้องสำหรับงานที่แสดง</span><span class="sxs-lookup"><span data-stu-id="8064c-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="8064c-360">ใช้ปุ่ม **คู่มือ** เพื่อดูคู่มือที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8064c-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="8064c-361">![ปุ่มคู่มือในส่วนติดต่อการดําเนินการผลิต](media/instruction-guides-Shopfloor1.png "ปุ่มคู่มือในส่วนติดต่อการดําเนินการผลิต")</span><span class="sxs-lookup"><span data-stu-id="8064c-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="8064c-362">จากนั้นให้วาง HoloLens และเข้าถึงคู่มือที่เกี่ยวข้องโดยมองที่รหัส QR และเปิดใช้งานคู่มือที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8064c-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="8064c-363">![รหัส QR เพื่อเข้าถึงคู่มือโดยใช้ HoloLens](media/instruction-guides-Shopfloor2.png "รหัส QR เพื่อเข้าถึงคู่มือโดยใช้ HoloLens")</span><span class="sxs-lookup"><span data-stu-id="8064c-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="8064c-364">การแก้ไขตรรกะสำหรับการเลือกคู่มือ</span><span class="sxs-lookup"><span data-stu-id="8064c-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="8064c-365">คุณสามารถเพิ่มคู่มือไปยังข้อมูลการผลิตต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8064c-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="8064c-366">ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-366">Resources</span></span>](#resources)
- [<span data-ttu-id="8064c-367">กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8064c-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="8064c-368">ผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="8064c-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="8064c-369">สูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="8064c-370">เวอร์ชันสูตร</span><span class="sxs-lookup"><span data-stu-id="8064c-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="8064c-371">รายการวัสดุและส่วนประกอบ (BOM)</span><span class="sxs-lookup"><span data-stu-id="8064c-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="8064c-372">เวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="8064c-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="8064c-373">กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-373">Routes</span></span>](#routes)
- [<span data-ttu-id="8064c-374">เวอร์ชันกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="8064c-375">ความสัมพันธ์ของการดำเนินงานกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8064c-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="8064c-376">เมื่อ Supply Chain Management สร้างงานสำหรับพื้นที่การผลิต จะมีการรวบรวมคู่มือที่เกี่ยวข้องจากแหล่งที่มาดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8064c-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="8064c-377">จดบันทึกกฎสำคัญต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8064c-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="8064c-378">ถ้าคุณแนบรุ่นของ BOM หรือรุ่นของสูตรกับกระบวนการผลิตหรือใบสั่งผลิต คู่มือใดๆ จะที่แนบอยู่กับรุ่นนี้ และคู่มือที่แนบกับ BOM หรือสูตรของรุ่นนั้นจะแสดงขึ้นในงานด้วย</span><span class="sxs-lookup"><span data-stu-id="8064c-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="8064c-379">ถ้าคุณแนบรุ่นของกระบวนการผลิตหรือใบสั่งผลิต คู่มือใดๆ จะที่แนบอยู่กับรุ่นนี้ และคู่มือที่แนบกับกระบวนการผลิตของรุ่นนั้นจะแสดงขึ้นในงานด้วย</span><span class="sxs-lookup"><span data-stu-id="8064c-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="8064c-380">ถ้าคุณกำหนดความสัมพันธ์ของการดำเนินงานของกระบวนการผลิตต่างๆ ที่รวมความสัมพันธ์ *ทั้งหมด* และกำหนดคู่มือให้กับผู้ปฏิบัติงาน เฉพาะคู่มือจากความสัมพันธ์เฉพาะเท่านั้นจะแสดงสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="8064c-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="8064c-381">![แผนภาพในการแก้ไขคู่มือที่เกี่ยวข้อง](media/instruction-guides-Resolve.png "แผนภาพในการแก้ไขคู่มือที่เกี่ยวข้อง")</span><span class="sxs-lookup"><span data-stu-id="8064c-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
