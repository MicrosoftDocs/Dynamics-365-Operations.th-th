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
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935886"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="23765-103">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="23765-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="23765-104">เมื่อต้องการดูว่าการตั้งค่าและข้อมูลปัจจุบันของคุณเข้ากันได้อย่างไรกับฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนให้ไปที่ **การวางแผนหลัก** \> **ตั้งค่า** \> **การตั้งค่าการเพิ่มประสิทธิภาพการวางแผนหลัก** แล้วเลือก **เรียกใช้การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="23765-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="23765-105">ถ้าการวิเคราะห์พบความไม่สอดคล้องกัน จะแสดงรายการอยู่บนหน้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="23765-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="23765-106">(การวิเคราะห์อาจใช้เวลาสักครู่ในการรัน)</span><span class="sxs-lookup"><span data-stu-id="23765-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="23765-107">ถ้าพบความไม่สอดคล้องกัน คุณยังคงสามารถใช้การเพิ่มประสิทธิภาพการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="23765-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="23765-108">ผลลัพธ์ของการวิเคราะห์การปรับให้เหมาะสม แสดงเฉพาะสถานที่ที่บริการการวางแผนจะไม่เป็นไปตามการตั้งค่าปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="23765-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="23765-109">กล่าวอีกอย่างหนึ่งคือแสดงสถานที่ที่กระบวนการบางอย่างอาจถูกละเว้นหรืออาจไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="23765-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="23765-110">ผลการวิเคราะห์: ตัวอย่าง 1</span><span class="sxs-lookup"><span data-stu-id="23765-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="23765-111">**คุณลักษณะ:** การผลิต</span><span class="sxs-lookup"><span data-stu-id="23765-111">**Feature:** Production</span></span>
- <span data-ttu-id="23765-112">**ปัญหา:** สินค้าที่มีระดับ BOM มากกว่าศูนย์: 56</span><span class="sxs-lookup"><span data-stu-id="23765-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="23765-113">**คำอธิบาย:** การวิเคราะห์การปรับให้เหมาะสม พบสินค้า 56 รายการ ที่มีการตั้งค่ารายการวัสดุและส่วนประกอบ (BOM) สำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="23765-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="23765-114">เนื่องจากเวอร์ชันปัจจุบันของการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนการผลิต การเพิ่มประสิทธิภาพการวางแผนจะสร้างแผนการใบสั่งซื้อ แทนแผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="23765-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="23765-115">นอกจากนี้ยังจะแสดงคำเตือนที่แสดงรายการสินค้าที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="23765-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="23765-116">ผลการวิเคราะห์: ตัวอย่าง 2</span><span class="sxs-lookup"><span data-stu-id="23765-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="23765-117">**คุณลักษณะ:** การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="23765-117">**Feature:** Actions</span></span>
- <span data-ttu-id="23765-118">**ปัญหา:** กลุ่มความครอบคลุมที่มีการคำนวณการดำเนินการที่เปิดใช้งาน: 6</span><span class="sxs-lookup"><span data-stu-id="23765-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="23765-119">**คำอธิบาย:** การวิเคราะห์การปรับให้เหมาะสม พบกลุ่มความครอบคลุม 6 กลุ่มที่มีการเปิดใช้งานการคำนวณการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="23765-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="23765-120">เนื่องจากการเพิ่มประสิทธิภาพการวางแผนเวอร์ชันปัจจุบันไม่สนับสนุนการดำเนินการ จะไม่มีการสร้างการดำเนินการในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="23765-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="23765-121">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="23765-121">Related resources</span></span>

[<span data-ttu-id="23765-122">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="23765-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="23765-123">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="23765-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="23765-124">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="23765-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="23765-125">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="23765-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="23765-126">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="23765-126">Cancel a planning job</span></span>](cancel-planning-job.md)
