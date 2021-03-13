---
title: สร้างกำหนดการสำหรับไซต์
description: 'กระบวนงานนี้แสดงวิธีจัดกำหนดการใบสั่งผลิตที่ยังไม่ได้เริ่มต้นสำหรับไซต์ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 442826d6611ea4aaedee2e9bae5649ada1cc846d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007902"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="fae5a-103">สร้างกำหนดการสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="fae5a-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fae5a-104">กระบวนงานนี้แสดงวิธีจัดกำหนดการใบสั่งผลิตที่ยังไม่ได้เริ่มต้นสำหรับไซต์ </span><span class="sxs-lookup"><span data-stu-id="fae5a-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="fae5a-105">ข้อมูลสาธิตของบริษัท USMF ถูกใช้เพื่อดำเนินกระบวนงานนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fae5a-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="fae5a-106">ระบุใบสั่งผลิตที่ยังไม่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fae5a-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="fae5a-107">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="fae5a-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="fae5a-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="fae5a-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fae5a-109">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ไซต์ ด้วยค่า '1'</span><span class="sxs-lookup"><span data-stu-id="fae5a-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="fae5a-110">1 แสดงถึงไซต์ใน USMF</span><span class="sxs-lookup"><span data-stu-id="fae5a-110">1 represents a site in USMF.</span></span> <span data-ttu-id="fae5a-111">ถ้าคุณไม่ได้กำลังใช้ USMF ให้เลือกไซต์จากบริษัทของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="fae5a-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="fae5a-112">เปิดตัวกรองคอลัมน์สถานะ</span><span class="sxs-lookup"><span data-stu-id="fae5a-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="fae5a-113">ใช้ตัวกรองในฟิลด์ "สถานะ" ด้วยค่าของ "จัดกำหนดการแล้ว" โดยใช้ตัวดำเนินการตัวกรอง "ตรงทุกประการ"</span><span class="sxs-lookup"><span data-stu-id="fae5a-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="fae5a-114">สร้างกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="fae5a-114">Create a schedule</span></span>
1. <span data-ttu-id="fae5a-115">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="fae5a-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="fae5a-116">ในบานหน้าต่างการดำเนินการ คลิก กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="fae5a-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="fae5a-117">คลิกกำหนดเวลางาน</span><span class="sxs-lookup"><span data-stu-id="fae5a-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="fae5a-118">ในฟิลด์คำสั่งการกำหนดเวลา เลือก 'ย้อนหลังจากวันจัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="fae5a-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="fae5a-119">เลือก ไม่ใช่ ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="fae5a-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="fae5a-120">เลือก ไม่ใช่ ในฟิลด์วัตถุดิบที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="fae5a-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="fae5a-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fae5a-121">Click OK.</span></span>
    * <span data-ttu-id="fae5a-122">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="fae5a-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="fae5a-123">ดูผลลัพธ์ของใบสั่งผลิตที่จัดกำหนดการแล้ว</span><span class="sxs-lookup"><span data-stu-id="fae5a-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="fae5a-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fae5a-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fae5a-125">คุณสามารถทำเครื่องหมายแถวใดๆก็ได้</span><span class="sxs-lookup"><span data-stu-id="fae5a-125">You can mark any row.</span></span>  
2. <span data-ttu-id="fae5a-126">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="fae5a-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="fae5a-127">คลิกงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fae5a-127">Click All jobs.</span></span>
    * <span data-ttu-id="fae5a-128">ในหน้านี้ คุณสามารถดูรายการของงานได้ </span><span class="sxs-lookup"><span data-stu-id="fae5a-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="fae5a-129">ในแท็บการจัดกำหนดการ คุณสามารถดูวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับงานได้</span><span class="sxs-lookup"><span data-stu-id="fae5a-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="fae5a-130">คลิกวัสดุ</span><span class="sxs-lookup"><span data-stu-id="fae5a-130">Click Materials.</span></span>
    * <span data-ttu-id="fae5a-131">ในหน้านี้ คุณสามารถดูปริมาณการใช้วัสดุที่ประเมินได้ สำหรับการดำเนินการในใบสั่งและสินค้าคงคลังที่พร้อมใช้งานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="fae5a-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

