---
title: การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการตรวจสอบการตั้งค่าปัจจุบันและข้อมูลของคุณ กับความสามารถของฟังก์ชันการเพิ่มประสิทธิภาพของการวางแผน
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
ms.openlocfilehash: 25f3b39d0e6e88eb3f042ab93773e9724528ab0f
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076189"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="6133b-103">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="6133b-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6133b-104">เมื่อต้องการดูว่าการตั้งค่าและข้อมูลปัจจุบันของคุณเข้ากันได้อย่างไรกับฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนให้ไปที่ **การวางแผนหลัก** \> **ตั้งค่า** \> **การตั้งค่าการเพิ่มประสิทธิภาพการวางแผนหลัก** แล้วเลือก **เรียกใช้การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="6133b-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="6133b-105">ถ้าการวิเคราะห์พบความไม่สอดคล้องกัน จะแสดงรายการอยู่บนหน้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6133b-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="6133b-106">(การวิเคราะห์อาจใช้เวลาสักครู่ในการรัน)</span><span class="sxs-lookup"><span data-stu-id="6133b-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="6133b-107">ถ้าพบความไม่สอดคล้องกัน คุณยังคงสามารถใช้การเพิ่มประสิทธิภาพการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="6133b-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="6133b-108">ผลลัพธ์ของการวิเคราะห์การปรับให้เหมาะสม แสดงเฉพาะสถานที่ที่บริการการวางแผนจะไม่เป็นไปตามการตั้งค่าปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="6133b-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="6133b-109">กล่าวอีกอย่างหนึ่งคือแสดงสถานที่ที่กระบวนการบางอย่างอาจถูกละเว้นหรืออาจไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="6133b-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="6133b-110">ผลการวิเคราะห์: ตัวอย่าง 1</span><span class="sxs-lookup"><span data-stu-id="6133b-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="6133b-111">**คุณลักษณะ:** การผลิต</span><span class="sxs-lookup"><span data-stu-id="6133b-111">**Feature:** Production</span></span>
- <span data-ttu-id="6133b-112">**ปัญหา:** สินค้าที่มีระดับ BOM มากกว่าศูนย์: 56</span><span class="sxs-lookup"><span data-stu-id="6133b-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="6133b-113">**คำอธิบาย:** การวิเคราะห์การปรับให้เหมาะสม พบสินค้า 56 รายการ ที่มีการตั้งค่ารายการวัสดุและส่วนประกอบ (BOM) สำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="6133b-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="6133b-114">เนื่องจากเวอร์ชันปัจจุบันของการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนการผลิต การเพิ่มประสิทธิภาพการวางแผนจะสร้างแผนการใบสั่งซื้อ แทนแผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="6133b-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="6133b-115">นอกจากนี้ยังจะแสดงคำเตือนที่แสดงรายการสินค้าที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="6133b-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="6133b-116">ผลการวิเคราะห์: ตัวอย่าง 2</span><span class="sxs-lookup"><span data-stu-id="6133b-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="6133b-117">**คุณลักษณะ:** การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6133b-117">**Feature:** Actions</span></span>
- <span data-ttu-id="6133b-118">**ปัญหา:** กลุ่มความครอบคลุมที่มีการคำนวณการดำเนินการที่เปิดใช้งาน: 6</span><span class="sxs-lookup"><span data-stu-id="6133b-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="6133b-119">**คำอธิบาย:** การวิเคราะห์การปรับให้เหมาะสม พบกลุ่มความครอบคลุม 6 กลุ่มที่มีการเปิดใช้งานการคำนวณการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6133b-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="6133b-120">เนื่องจากการเพิ่มประสิทธิภาพการวางแผนเวอร์ชันปัจจุบันไม่สนับสนุนการดำเนินการ จะไม่มีการสร้างการดำเนินการในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="6133b-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="6133b-121">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6133b-121">Related resources</span></span>

[<span data-ttu-id="6133b-122">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="6133b-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="6133b-123">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="6133b-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="6133b-124">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="6133b-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="6133b-125">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="6133b-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="6133b-126">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="6133b-126">Cancel a planning job</span></span>](cancel-planning-job.md)
