---
title: ใช้ตัวกรองกับแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการใช้ตัวกรองบนแผน เมื่อใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
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
ms.openlocfilehash: ca28953846b4f1978a453d2ab2aa9759e4f45221
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076120"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="305b6-103">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="305b6-104">เมื่อมีการใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน คุณสามารถใช้ตัวกรองข้อมูลกับแผนได้</span><span class="sxs-lookup"><span data-stu-id="305b6-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="305b6-105">**ตัวกรองแผน** จะถูกนำไปใช้ในระหว่างการรันการวางแผนหลักเสมอ</span><span class="sxs-lookup"><span data-stu-id="305b6-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="305b6-106">**ตัวกรองแผน** มีประโยชน์เมื่อคุณต้องการจำกัดแผนให้กับกลุ่มสินค้าหนึ่งๆ และตรวจสอบให้แน่ใจว่าไม่มีสินค้าอื่นๆ ที่รวมอยู่ในส่วนหนึ่งของการวางแผนหลักที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="305b6-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="305b6-107">ถ้ามีการใช้ **ตัวกรองแผน** แล้ว และยังมีการใช้ตัวกรองข้อมูลรันไทม์ในระหว่างการรันการวางแผนหลักด้วย เฉพาะจุดตัดของตัวกรองทั้งสองเท่านั้นที่จะรวมอยู่ในการรันการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="305b6-108">**ตัวกรองแผน** สามารถเข้าถึงได้จาก **แผนหลัก** เมื่อมีการใช้การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="305b6-109">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="305b6-109">Example scenario</span></span>

<span data-ttu-id="305b6-110">มีการตั้งค่าตัวกรองข้อมูลที่รวม A B และ C การรันการวางแผนหลักจะถูกรันสำหรับแผนเดียวกัน แต่มีการใช้ตัวกรองข้อมูลรันไทม์ที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="305b6-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="305b6-111">**ตัวกรองข้อมูลรันไทม์ที่รวมรายการ D:** ไม่มีการวางแผนรายการ เนื่องจากไม่มีการแยกระหว่างตัวกรองข้อมูลแผนและตัวกรองข้อมูลรันไทม์</span><span class="sxs-lookup"><span data-stu-id="305b6-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="305b6-112">**ตัวกรองข้อมูลรันไทม์ที่รวมรายการ A และ D:** เฉพาะรายการ A เท่านั้นที่จะรวมอยู่ในการวางแผนรัน เนื่องจากรายการ D ไม่ได้เป็นส่วนหนึ่งของตัวกรองข้อมูลของแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="305b6-113">**ตัวกรองข้อมูลรันไทม์ที่รวมรายการฺ:** เฉพาะรายการ B เท่านั้นที่จะรวมอยู่ในการวางแผนรัน และผลการวางแผนของรายการ A จะถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="305b6-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="305b6-114">**ตัวกรองข้อมูลรันไทม์ที่มีรายการทั้งหมด (ตัวกรองเปล่า):** รายการ A B และ C จะรวมอยู่ในการรันการวางแผน และผลของการวางแผนก่อนหน้านี้สำหรับรายการ A และ B ถูกเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="305b6-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="305b6-115">คุณควรหลีกเลี่ยงการตั้งค่าตัวกรองข้อมูลแผนบนแผนที่เลือกเป็น **แผนหลักชั่วคราวปัจจุบัน** บนหน้า **พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="305b6-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="305b6-116">มิฉะนั้น ฟังก์ชันแผนหลักแบบไดนามิกจะถูกจำกัดให้กับรายการที่กรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="305b6-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="305b6-117">ตัวอย่างเช่น ถ้ามีการอัพเดตความต้องการสุทธิสำหรับสินค้าที่ไม่ได้เป็นส่วนหนึ่งของตัวกรองข้อมูลแผนจะไม่มีการสร้างผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="305b6-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="305b6-118">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="305b6-118">Related resources</span></span>

[<span data-ttu-id="305b6-119">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="305b6-120">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="305b6-121">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="305b6-122">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="305b6-123">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="305b6-123">Cancel a planning job</span></span>](cancel-planning-job.md)
