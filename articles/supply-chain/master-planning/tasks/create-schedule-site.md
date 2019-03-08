---
title: สร้างกำหนดการสำหรับไซต์
description: 'กระบวนงานนี้แสดงวิธีจัดกำหนดการใบสั่งผลิตที่ยังไม่ได้เริ่มต้นสำหรับไซต์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54bb2532534d5567239dad4fab7fd74fa50d2826
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "330068"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="a0034-103">สร้างกำหนดการสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="a0034-103">Create a schedule for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0034-104">กระบวนงานนี้แสดงวิธีจัดกำหนดการใบสั่งผลิตที่ยังไม่ได้เริ่มต้นสำหรับไซต์ </span><span class="sxs-lookup"><span data-stu-id="a0034-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="a0034-105">ข้อมูลสาธิตของบริษัท USMF ถูกใช้เพื่อดำเนินกระบวนงานนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a0034-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="a0034-106">ระบุใบสั่งผลิตที่ยังไม่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a0034-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="a0034-107">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="a0034-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="a0034-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="a0034-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a0034-109">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ไซต์ ด้วยค่า '1'</span><span class="sxs-lookup"><span data-stu-id="a0034-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="a0034-110">1 แสดงถึงไซต์ใน USMF</span><span class="sxs-lookup"><span data-stu-id="a0034-110">1 represents a site in USMF.</span></span> <span data-ttu-id="a0034-111">ถ้าคุณไม่ได้กำลังใช้ USMF ให้เลือกไซต์จากบริษัทของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a0034-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="a0034-112">เปิดตัวกรองคอลัมน์สถานะ</span><span class="sxs-lookup"><span data-stu-id="a0034-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="a0034-113">ใช้ตัวกรองในฟิลด์ "สถานะ" ด้วยค่าของ "จัดกำหนดการแล้ว" โดยใช้ตัวดำเนินการตัวกรอง "ตรงทุกประการ"</span><span class="sxs-lookup"><span data-stu-id="a0034-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="a0034-114">สร้างกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="a0034-114">Create a schedule</span></span>
1. <span data-ttu-id="a0034-115">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="a0034-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="a0034-116">ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="a0034-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="a0034-117">คลิกกำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="a0034-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="a0034-118">ในฟิลด์คำสั่งการกำหนดเวลา เลือก 'ย้อนหลังจากวันจัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="a0034-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="a0034-119">เลือก ไม่ใช่ ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="a0034-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="a0034-120">เลือก ไม่ใช่ ในฟิลด์วัตถุดิบที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="a0034-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="a0034-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a0034-121">Click OK.</span></span>
    * <span data-ttu-id="a0034-122">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="a0034-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="a0034-123">ดูผลลัพธ์ของใบสั่งผลิตที่จัดกำหนดการแล้ว</span><span class="sxs-lookup"><span data-stu-id="a0034-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="a0034-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a0034-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a0034-125">คุณสามารถทำเครื่องหมายแถวใดๆก็ได้</span><span class="sxs-lookup"><span data-stu-id="a0034-125">You can mark any row.</span></span>  
2. <span data-ttu-id="a0034-126">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="a0034-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="a0034-127">คลิกงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a0034-127">Click All jobs.</span></span>
    * <span data-ttu-id="a0034-128">ในหน้านี้ คุณสามารถดูรายการของงานได้ </span><span class="sxs-lookup"><span data-stu-id="a0034-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="a0034-129">ในแท็บการจัดกำหนดการ คุณสามารถดูวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับงานได้</span><span class="sxs-lookup"><span data-stu-id="a0034-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="a0034-130">คลิกวัสดุ</span><span class="sxs-lookup"><span data-stu-id="a0034-130">Click Materials.</span></span>
    * <span data-ttu-id="a0034-131">ในหน้านี้ คุณสามารถดูปริมาณการใช้วัสดุที่ประเมินได้ สำหรับการดำเนินการในใบสั่งและสินค้าคงคลังที่พร้อมใช้งานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a0034-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

