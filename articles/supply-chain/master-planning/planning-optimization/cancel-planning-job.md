---
title: ยกเลิกงานการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774064"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="4180b-103">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-103">Cancel a planning job</span></span>

<span data-ttu-id="4180b-104">ใน Microsoft Dynamics 365 Supply Chain Management คุณสามารถยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="4180b-105">การยกเลิกงานการวางแผนที่ใช้งานอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4180b-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="4180b-106">เฉพาะตำแหน่งงานที่เปิดอยู่เท่านั้น ที่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="4180b-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="4180b-107">ไปที่ **การวางแผนหลัก \> ตั้งค่า \> แผน**</span><span class="sxs-lookup"><span data-stu-id="4180b-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="4180b-108">เลือกแผนที่เหมาะสมสำหรับการดำเนินการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="4180b-109">เลือก **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="4180b-109">Select **History**.</span></span>
4. <span data-ttu-id="4180b-110">เลือกงานการวางแผนที่จะยกเลิก</span><span class="sxs-lookup"><span data-stu-id="4180b-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="4180b-111">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="4180b-111">Select **Cancel**.</span></span>

<span data-ttu-id="4180b-112">สถานะของงานจะเป็น **กำลังยกเลิก** จนกว่าบริการการเพิ่มประสิทธิภาพของการวางแผนยืนยันว่างานถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="4180b-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="4180b-113">สถานะจะเปลี่ยนเป็น **ยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="4180b-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="4180b-114">การดูการเปลี่ยนแปลงสถานะ คุณต้องรีเฟรชหน้า โดยเลือกปุ่ม **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="4180b-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="4180b-115">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4180b-115">Related resources</span></span>

[<span data-ttu-id="4180b-116">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="4180b-117">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="4180b-118">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="4180b-119">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="4180b-120">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="4180b-120">Apply filters to a plan</span></span>](plan-filters.md)
