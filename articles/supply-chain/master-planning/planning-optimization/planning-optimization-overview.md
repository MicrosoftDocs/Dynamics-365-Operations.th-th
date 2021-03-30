---
title: ภาพรวมการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้แสดงภาพรวมของการวางแผนเพิ่มประสิทธิภาพการทำงานของฟังก์ชันทั่วไป
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: cf64c3dea6fe08c36388f5f7147795221cf85b8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224486"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="c6914-103">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6914-104">การเพิ่มประสิทธิภาพการวางแผน Add-in สำหรับ Microsoft Dynamics 365 Supply Chain Management เปิดใช้งานการคำนวณการวางแผนหลักที่จะเกิดขึ้นภายนอก Dynamics 365 Supply Chain Management และฐานข้อมูล SQL ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c6914-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="c6914-105">สวัสดิการที่เกี่ยวข้องกับฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนรวมถึงประสิทธิภาพที่ดียิ่งขึ้นและผลกระทบน้อยที่สุดบนฐานข้อมูล SQL ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="c6914-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="c6914-106">การรันการวางแผนด่วนสามารถทำได้แม้กระทั่งช่วงเวลาทำงาน เพื่อให้ผู้วางแผนสามารถตอบสนองความต้องการหรือเปลี่ยนแปลงพารามิเตอร์ได้ทันที</span><span class="sxs-lookup"><span data-stu-id="c6914-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="c6914-107">เมื่อต้องการใช้การเพิ่มประสิทธิภาพการวางแผน คุณต้องติดตั้ง Add-in ของการเพิ่มประสิทธิภาพการวางแผนจากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS) และเปิดเพิ่มประสิทธิภาพการวางแผนของฟังก์ชันใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c6914-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="c6914-108">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การเริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="c6914-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="c6914-109">ภาพประกอบต่อไปนี้แสดงข้อดีของการรันการเพิ่มประสิทธิภาพการวางแผนในระหว่างชั่วโมงที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c6914-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![ข้อดีของการรันการเพิ่มประสิทธิภาพการวางแผนในระหว่างชั่วโมงทำงาน](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="c6914-111">ประสิทธิภาพการทำงานเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="c6914-111">Improved performance</span></span>

<span data-ttu-id="c6914-112">การเพิ่มประสิทธิภาพการวางแผนสามารถใช้ในสถานการณ์ที่เกี่ยวข้องกับแผนหลักที่รันเป็นเวลานาน</span><span class="sxs-lookup"><span data-stu-id="c6914-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="c6914-113">ออกแบบมาโดยเฉพาะสำหรับการคำนวณที่รวดเร็วมากซึ่งเกี่ยวข้องกับปริมาณที่มีขนาดใหญ่มากของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6914-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="c6914-114">เนื่องจากได้รับการสร้างขึ้นเป็นบริการเช่าแบบไฮเปอร์ซึ่งจะทำงานกับอินสแตนซ์หลายอินสแตนซ์พร้อมกันเพื่อคำนวณแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="c6914-115">นอกจากนี้บริการวางแผนจะลบจำนวนงานในศูนย์การผลิตหลักออกจากระบบของคุณและทำงานกับสตรีมข้อมูลที่ช่วยลดการโหลดของเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="c6914-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="c6914-116">การเพิ่มประสิทธิภาพการวางแผนสามารถช่วยคุณในการบรรลุเป้าหมายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6914-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="c6914-117">ปรับปรุงประสิทธิภาพการทำงานของการวางแผนผ่านรันไทม์แบบสั้น</span><span class="sxs-lookup"><span data-stu-id="c6914-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="c6914-118">ลดผลกระทบต่อกระบวนการอื่นๆ ในระหว่างการรันการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="c6914-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="c6914-119">ทำงานการวางแผนบ่อยขึ้น</span><span class="sxs-lookup"><span data-stu-id="c6914-119">Do more frequent planning runs.</span></span> <span data-ttu-id="c6914-120">(คุณไม่จำกัดเฉพาะการรันรายวัน)</span><span class="sxs-lookup"><span data-stu-id="c6914-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="c6914-121">มั่นใจว่าการเติบโตของธุรกิจในอนาคตจะไม่เกินระบบการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="c6914-122">ลำดับข้อมูลของสถาปัตยกรรม</span><span class="sxs-lookup"><span data-stu-id="c6914-122">Architecture and data flow</span></span>

<span data-ttu-id="c6914-123">เมื่อมีการติดตั้ง Add-in การเพิ่มประสิทธิภาพการวางแผนเพิ่มเติมจาก LCS การเชื่อมต่อที่ปลอดภัยไปยังบริการการเพิ่มประสิทธิภาพการวางแผนจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c6914-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="c6914-124">บริการจะอยู่ในประเทศหรือภูมิภาคศูนย์ข้อมูลเดียวกันกับอินสแตนซ์ Supply Chain Management ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c6914-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="c6914-125">หลังจากที่มีการตั้งค่าการเพิ่มประสิทธิภาพการวางแผน เมื่อรันการวางแผนหลัก ข้อมูลหลัก และข้อมูลของทรานแซคชันจะถูกส่งจาก Supply Chain Management ไปยังบริการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="c6914-126">ถ้า Add-in การเพิ่มประสิทธิภาพการวางแผนถูกถอนการติดตั้ง ข้อมูลที่เกี่ยวข้องทั้งหมดในบริการการเพิ่มประสิทธิภาพการวางแผนจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="c6914-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="c6914-127">ลำดับข้อมูลระดับสูงสำหรับการรันการฟื้นฟู</span><span class="sxs-lookup"><span data-stu-id="c6914-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="c6914-128">ไคลเอนต์ Supply Chain Management ส่งสัญญาณเพื่อร้องขอการรันการวางแผนจากการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="c6914-129">การร้องขอการเพิ่มประสิทธิภาพการวางแผนข้อมูลที่จำเป็นผ่านทางการเชื่อมต่อแบบรวม</span><span class="sxs-lookup"><span data-stu-id="c6914-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="c6914-130">ฐานข้อมูล SQL จะส่งข้อมูลที่ร้องขอเกี่ยวกับการตั้งค่าต้นแบบและข้อมูลของทรานแซคชันไปยังการวางแผนการเพิ่มประสิทธิภาพผ่านทางตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c6914-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="c6914-131">ตัวเชื่อมต่อจะแปลข้อมูลระหว่าง Supply Chain Management และบริการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="c6914-132">บริการเพิ่มประสิทธิภาพของการวางแผนมีข้อมูลที่เกี่ยวข้องกับการวางแผนอยู่ในหน่วยความจำ เช่นเดียวกับการคำนวณที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="c6914-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="c6914-133">ผลลัพธ์ของการวางแผนจะถูกส่งไปยังฐานข้อมูล Supply Chain Management ผ่านทางตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c6914-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="c6914-134">ผลลัพธ์รวมถึงข้อมูล เช่น ใบสั่งที่วางแผนไว้ และข้อมูลการจัดจำแนก</span><span class="sxs-lookup"><span data-stu-id="c6914-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="c6914-135">การเพิ่มประสิทธิภาพการวางแผนส่งสัญญาณให้กับ Supply Chain Management เพื่อบ่งชี้ว่าการรันการวางแผนเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6914-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="c6914-136">นอกจากนี้ยังส่งข้อความและคำเตือนที่เกี่ยวข้องใดๆ</span><span class="sxs-lookup"><span data-stu-id="c6914-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="c6914-137">ภาพประกอบต่อไปนี้แสดงโฟลว์ลำดับของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6914-137">The following illustration shows the data flow.</span></span>

![ลำดับข้อมูลระดับสูงสำหรับการรันการฟื้นฟู](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="c6914-139">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c6914-139">Related resources</span></span>

[<span data-ttu-id="c6914-140">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c6914-141">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c6914-142">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c6914-143">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="c6914-144">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c6914-144">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]