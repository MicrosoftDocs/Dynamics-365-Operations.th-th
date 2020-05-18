---
title: ยกเลิกงานการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323473"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="46005-103">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46005-104">ใน Microsoft Dynamics 365 Supply Chain Management คุณสามารถยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="46005-105">เมื่อคุณเลือก **ยกเลิก** ในกล่องโต้ตอบ เมื่องานการเพิ่มประสิทธิภาพการวางแผนถูกทริกเกอร์โดยตรงจากอินเทอร์เฟสผู้ใช้ (ไม่ได้อยู่ในพื้นหลัง) นี่จะไม่ยกเลิกงานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="46005-106">แม้ว่าคุณจะได้รับคำเตือน เช่น "ยกเลิกการดำเนินงานแล้ว" คุณจะยังคงต้องใช้ขั้นตอนต่อไปนี้เพื่อยกเลิกงานการวางแผนที่มีการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="46005-107">การยกเลิกงานการวางแผนที่ใช้งานอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="46005-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="46005-108">เฉพาะตำแหน่งงานที่เปิดอยู่เท่านั้น ที่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="46005-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="46005-109">ไปที่ **การวางแผนหลัก \> ตั้งค่า \> แผน**</span><span class="sxs-lookup"><span data-stu-id="46005-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="46005-110">เลือกแผนที่เหมาะสมสำหรับการดำเนินการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="46005-111">เลือก **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="46005-111">Select **History**.</span></span>
4. <span data-ttu-id="46005-112">เลือกงานการวางแผนที่จะยกเลิก</span><span class="sxs-lookup"><span data-stu-id="46005-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="46005-113">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="46005-113">Select **Cancel**.</span></span>

<span data-ttu-id="46005-114">สถานะของงานจะเป็น **กำลังยกเลิก** จนกว่าบริการการเพิ่มประสิทธิภาพของการวางแผนยืนยันว่างานถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="46005-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="46005-115">สถานะจะเปลี่ยนเป็น **ยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="46005-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="46005-116">การดูการเปลี่ยนแปลงสถานะ คุณต้องรีเฟรชหน้า โดยเลือกปุ่ม **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="46005-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46005-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="46005-117">Additional resources</span></span>

[<span data-ttu-id="46005-118">ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="46005-119">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="46005-120">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="46005-121">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="46005-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="46005-122">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="46005-122">Apply filters to a plan</span></span>](plan-filters.md)
