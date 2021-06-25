---
title: ดูประวัติการวางแผนและล็อกการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการดูประวัติของงานการวางแผน ซึ่งทริกเกอร์โดยฟังก์ชันการเพิ่มประสิทธิภาพของการวางแผน
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187258"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="b4e0a-103">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4e0a-104">หัวข้อนี้จะอธิบายถึงวิธีการดูประวัติของงานการวางแผน ซึ่งทริกเกอร์โดยฟังก์ชันการเพิ่มประสิทธิภาพของการวางแผนใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4e0a-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b4e0a-105">เมื่อต้องการดูประวัติสำหรับแผนให้เปิดแผนโดยไปที่ **การวางแผนหลัก** \> **การตั้งค่าแผน** \> **แผน** \> **แผนหลัก** และเลือก **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="b4e0a-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="b4e0a-106">ประวัติแสดงรายการงานทั้งหมดสำหรับแผนที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b4e0a-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="b4e0a-107">รายการรวมงานที่เสร็จสมบูรณ์และงานที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b4e0a-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="b4e0a-108">ประวัติของงานเกี่ยวกับการวางแผนหลักในการเพิ่มประสิทธิภาพการวางแผนจะรักษาไว้เพียง 60 เรกคอร์ดต่อแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="b4e0a-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="b4e0a-109">เมื่อใดก็ตามที่คุณรันการคํานวณการวางแผนหลักใหม่ เรกคอร์ดประวัติแรกสุดของแผนนั้นจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="b4e0a-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="b4e0a-110">นอกจากการดูเวลาเริ่มต้นและสถานะของงานแล้วคุณยังสามารถดูล็อกของงานที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="b4e0a-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="b4e0a-111">ล็อกรวมถึงข้อมูลเพิ่มเติมและคำเตือน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="b4e0a-112">ไม่ใช่ทุกงานที่จะมีล็อก</span><span class="sxs-lookup"><span data-stu-id="b4e0a-112">Not all jobs have a log.</span></span> <span data-ttu-id="b4e0a-113">เมื่อต้องการดูล็อกของงานให้เลือก **ล็อก**</span><span class="sxs-lookup"><span data-stu-id="b4e0a-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="b4e0a-114">รายการบันทึกจะจัดเก็บไว้เฉพาะเมื่อ 30 วันหลังจากวันที่งานเสร็จสิ้น หลังจากนั้นจะถูกลบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b4e0a-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b4e0a-115">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b4e0a-115">Related resources</span></span>

- [<span data-ttu-id="b4e0a-116">ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="b4e0a-117">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="b4e0a-118">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="b4e0a-119">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="b4e0a-120">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="b4e0a-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]