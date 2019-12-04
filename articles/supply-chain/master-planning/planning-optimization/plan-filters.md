---
title: ใช้ตัวกรองกับแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการใช้ตัวกรองบนแผน เมื่อใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774063"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="9ac21-103">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-103">Apply filters to a plan</span></span>

<span data-ttu-id="9ac21-104">เมื่อมีการใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน คุณสามารถใช้ตัวกรองข้อมูลกับแผนได้</span><span class="sxs-lookup"><span data-stu-id="9ac21-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="9ac21-105">ตัวกรองแผนจะถูกนำไปใช้ในระหว่างการรันการวางแผนหลักเสมอ</span><span class="sxs-lookup"><span data-stu-id="9ac21-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="9ac21-106">ตัวกรองแผนมีประโยชน์เมื่อคุณต้องการจำกัดแผนให้กับกลุ่มสินค้าหนึ่ง ๆ และตรวจสอบให้แน่ใจว่าไม่มีสินค้าอื่น ๆ ที่รวมอยู่ในส่วนหนึ่งของการวางแผนหลักที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="9ac21-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="9ac21-107">ถ้ามีการใช้ตัวกรองแผนแล้ว และมีการใช้ตัวกรองข้อมูลรันไทม์ในระหว่างการรันการวางแผนหลัก เฉพาะจุดตัดของตัวกรองทั้งสองเท่านั้นที่จะรวมอยู่ในการรันการวางแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9ac21-108">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="9ac21-108">Example scenario</span></span>

<span data-ttu-id="9ac21-109">มีการตั้งค่าตัวกรองข้อมูลที่รวม A B และ C การรันการวางแผนหลักจะถูกรันสำหรับแผนเดียวกัน แต่มีการใช้ตัวกรองข้อมูลรันไทม์ที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="9ac21-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="9ac21-110">**ตัวกรองข้อมูลรันไทม์ที่รวมรายการ D:** ไม่มีการวางแผนรายการ เนื่องจากไม่มีการแยกระหว่างตัวกรองข้อมูลแผนและตัวกรองข้อมูลรันไทม์</span><span class="sxs-lookup"><span data-stu-id="9ac21-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="9ac21-111">**ตัวกรองข้อมูลรันไทม์ที่รวมรายการ A และ D:** เฉพาะรายการ A เท่านั้นที่จะรวมอยู่ในการวางแผนรัน เนื่องจากรายการ D ไม่ได้เป็นส่วนหนึ่งของตัวกรองข้อมูลของแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="9ac21-112">**ตัวกรองข้อมูลรันไทม์ที่รวมรายการฺ:** เฉพาะรายการ B เท่านั้นที่จะรวมอยู่ในการวางแผนรัน และผลการวางแผนของรายการ A จะถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="9ac21-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="9ac21-113">**ตัวกรองข้อมูลรันไทม์ที่มีรายการทั้งหมด (ตัวกรองเปล่า):** รายการ A B และ C จะรวมอยู่ในการรันการวางแผน และผลของการวางแผนก่อนหน้านี้สำหรับรายการ A และ B ถูกเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="9ac21-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="9ac21-114">คุณควรหลีกเลี่ยงการตั้งค่าตัวกรองข้อมูลแผนบนแผนที่เลือกเป็น **แผนหลักชั่วคราวปัจจุบัน** บนหน้า **พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="9ac21-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="9ac21-115">มิฉะนั้น ฟังก์ชันแผนหลักแบบไดนามิกจะถูกจำกัดให้กับรายการที่กรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ac21-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="9ac21-116">ตัวอย่างเช่น ถ้ามีการอัพเดตความต้องการสุทธิสำหรับสินค้าที่ไม่ได้เป็นส่วนหนึ่งของตัวกรองข้อมูลแผนจะไม่มีการสร้างผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="9ac21-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9ac21-117">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="9ac21-117">Related resources</span></span>

[<span data-ttu-id="9ac21-118">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="9ac21-119">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9ac21-120">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="9ac21-121">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="9ac21-122">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="9ac21-122">Cancel a planning job</span></span>](cancel-planning-job.md)
