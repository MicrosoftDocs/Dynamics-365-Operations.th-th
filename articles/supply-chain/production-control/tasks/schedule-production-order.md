---
title: กำหนดการใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการกำหนดใบสั่งผลิต '
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3fe8f6890c7d8ac8835503091642faa773f7f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438443"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="335ad-103">กำหนดการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="335ad-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="335ad-104">กระบวนงานนี้แสดงวิธีการกำหนดใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="335ad-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="335ad-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="335ad-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="335ad-106">นี่เป็นกระบวนงานที่สามจากเจ็ดกระบวนงานซึ่งอธิบายวงจรชีวิตของใบสั่งการผลิต</span><span class="sxs-lookup"><span data-stu-id="335ad-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="335ad-107">กำหนดการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="335ad-107">Schedule a production order</span></span>
1. <span data-ttu-id="335ad-108">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="335ad-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="335ad-109">เลือกใบสั่งผลิตที่มีสถานะเป็น ประเมินแล้ว</span><span class="sxs-lookup"><span data-stu-id="335ad-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="335ad-110">ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="335ad-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="335ad-111">การจัดส่ง กำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="335ad-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="335ad-112">พารามิเตอร์สำหรับการวางแผนมีการตั้งค่าบนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="335ad-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="335ad-113">คุณสามารถตั้งค่าพารามิเตอร์สำหรับผู้ใช้เฉพาะหรือผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="335ad-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="335ad-114">ในฟิลด์ทิศทางการจัดกำหนดการ ให้เลือก 'ไปข้างหน้าจากวันนี้'</span><span class="sxs-lookup"><span data-stu-id="335ad-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="335ad-115">ในฟิลด์วันที่กำหนดเวลาการดำเนินงาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="335ad-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="335ad-116">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายกำลังการผลิตมีจำกัด</span><span class="sxs-lookup"><span data-stu-id="335ad-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="335ad-117">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายวัตถุดิบมีจำกัด</span><span class="sxs-lookup"><span data-stu-id="335ad-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="335ad-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="335ad-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="335ad-119">ดูผลลัพธ์การจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="335ad-119">View the scheduling results</span></span>
1. <span data-ttu-id="335ad-120">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="335ad-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="335ad-121">คลิกงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="335ad-121">Click All jobs.</span></span>
    * <span data-ttu-id="335ad-122">หน้านี้แสดงงานที่ได้จัดกำหนดการที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="335ad-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="335ad-123">ขยายหรือยุบส่วนการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="335ad-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="335ad-124">บนแท็บด่วนการวางแผน คุณสามารถดูวันที่และเวลาที่จัดกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="335ad-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="335ad-125">คลิกการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="335ad-125">Click Inquiries.</span></span>
5. <span data-ttu-id="335ad-126">คลิกการใช้กำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="335ad-126">Click Capacity load.</span></span>
    * <span data-ttu-id="335ad-127">หน้าการใช้กำลังการผลิตแสดงถึงกำลังการผลิตที่ถูกจองไว้ผ่านการจัดตารางงาน จำนวนรวมของชั่วโมงที่ถูกจองบนทรัพยากรและจำนวนของชั่วโมงที่พร้อมใช้งานสำหรับงานที่จัดกำหนดบนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="335ad-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="335ad-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="335ad-128">Close the page.</span></span>
7. <span data-ttu-id="335ad-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="335ad-129">Close the page.</span></span>

