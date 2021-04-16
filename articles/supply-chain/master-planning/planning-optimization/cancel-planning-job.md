---
title: ยกเลิกงานการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833340"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="0637f-103">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0637f-104">ใน Microsoft Dynamics 365 Supply Chain Management คุณสามารถยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="0637f-105">เมื่อคุณเลือก **ยกเลิก** ในกล่องโต้ตอบ เมื่องานการเพิ่มประสิทธิภาพการวางแผนถูกทริกเกอร์โดยตรงจากอินเทอร์เฟสผู้ใช้ (ไม่ได้อยู่ในพื้นหลัง) นี่จะไม่ยกเลิกงานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="0637f-106">แม้ว่าคุณจะได้รับคำเตือน เช่น "ยกเลิกการดำเนินงานแล้ว" คุณจะยังคงต้องใช้ขั้นตอนต่อไปนี้เพื่อยกเลิกงานการวางแผนที่มีการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="0637f-107">การยกเลิกงานการวางแผนที่ใช้งานอยู่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0637f-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="0637f-108">เฉพาะตำแหน่งงานที่เปิดอยู่เท่านั้น ที่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="0637f-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="0637f-109">ไปที่ **การวางแผนหลัก \> ตั้งค่า \> แผน**</span><span class="sxs-lookup"><span data-stu-id="0637f-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="0637f-110">เลือกแผนที่เหมาะสมสำหรับการดำเนินการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="0637f-111">เลือก **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="0637f-111">Select **History**.</span></span>
4. <span data-ttu-id="0637f-112">เลือกงานการวางแผนที่จะยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0637f-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="0637f-113">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="0637f-113">Select **Cancel**.</span></span>

<span data-ttu-id="0637f-114">สถานะของงานจะเป็น **กำลังยกเลิก** จนกว่าบริการการเพิ่มประสิทธิภาพของการวางแผนยืนยันว่างานถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="0637f-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="0637f-115">สถานะจะเปลี่ยนเป็น **ยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="0637f-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="0637f-116">การดูการเปลี่ยนแปลงสถานะ คุณต้องรีเฟรชหน้า โดยเลือกปุ่ม **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="0637f-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0637f-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0637f-117">Additional resources</span></span>

[<span data-ttu-id="0637f-118">ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0637f-119">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="0637f-120">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="0637f-121">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0637f-122">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="0637f-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]