---
title: สร้างกฎคัมบังสำหรับหลายกิจกรรม
description: 'กระบวนงานนี้แสดงวิธีการสร้างกฎคัมบังที่ประกอบด้วยกิจกรรมหลายรายการจากขั้นตอนการผลิต '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c25d47a78d1cc91ee2625ef628d7b9ba345b097
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977924"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="8087d-103">สร้างกฎคัมบังสำหรับหลายกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="8087d-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8087d-104">กระบวนงานนี้แสดงวิธีการสร้างกฎคัมบังที่ประกอบด้วยกิจกรรมหลายรายการจากขั้นตอนการผลิต </span><span class="sxs-lookup"><span data-stu-id="8087d-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="8087d-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8087d-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="8087d-106">งานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เนื่องจากเป็นผู้จัดเตรียมการผลิตผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยนในสภาพแวดล้อมแบบลีน</span><span class="sxs-lookup"><span data-stu-id="8087d-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="8087d-107">สร้างกฎคัมบังใหม่</span><span class="sxs-lookup"><span data-stu-id="8087d-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="8087d-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8087d-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="8087d-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8087d-109">Click New.</span></span>
3. <span data-ttu-id="8087d-110">ในฟิลด์กลยุทธ์การเติมสินค้า ให้เลือก 'จัดกำหนดการแล้ว'</span><span class="sxs-lookup"><span data-stu-id="8087d-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="8087d-111">ในฟิลด์กิจกรรมการวางแผนแรก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8087d-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="8087d-112">เลือก SpeakerAssemblyAndPolish</span><span class="sxs-lookup"><span data-stu-id="8087d-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="8087d-113">เลือกกล่องกาเครื่องหมายกิจกรรมหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="8087d-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="8087d-114">วัตถุประสงค์คือเพื่อรวมกิจกรรมหนึ่งรายการขึ้นไปในกฎคัมบัง </span><span class="sxs-lookup"><span data-stu-id="8087d-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="8087d-115">คุณสามารถเลือกเส้นทางในขั้นตอนการผลิตเมื่อคุณเลือกกิจกรรมแผนล่าสุด</span><span class="sxs-lookup"><span data-stu-id="8087d-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="8087d-116">ในฟิลด์กิจกรรมการวางแผนสุดท้าย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8087d-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="8087d-117">เลือก SpeakerTestAndPackaging </span><span class="sxs-lookup"><span data-stu-id="8087d-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="8087d-118">หลังจากที่คุณเลือกค่า หน้าจะเปิดโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="8087d-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="8087d-119">เลือกขั้นตอนคัมบัง SpeakerAssemblyAndPolish > SpeakerTestAndPackaging</span><span class="sxs-lookup"><span data-stu-id="8087d-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="8087d-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8087d-120">Click OK.</span></span>  
7. <span data-ttu-id="8087d-121">ขยายส่วนรายละเอียด </span><span class="sxs-lookup"><span data-stu-id="8087d-121">Expand the Details section.</span></span>
8. <span data-ttu-id="8087d-122">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8087d-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="8087d-123">เลือก สินค้า L0006</span><span class="sxs-lookup"><span data-stu-id="8087d-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="8087d-124">สร้างคัมบังและดูงาน</span><span class="sxs-lookup"><span data-stu-id="8087d-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="8087d-125">ขยายส่วนคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8087d-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="8087d-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="8087d-126">Click Add.</span></span>
3. <span data-ttu-id="8087d-127">ในฟิลด์จำนวนคัมบังใหม่ ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="8087d-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="8087d-128">นี่จะสร้างหนึ่งคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8087d-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="8087d-129">ตั้งค่าปริมาณผลิตภัณฑ์เป็น 3</span><span class="sxs-lookup"><span data-stu-id="8087d-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="8087d-130">คัมบังจะประมวลผลผลิตภัณฑ์ 3 รายการ</span><span class="sxs-lookup"><span data-stu-id="8087d-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="8087d-131">ในฟิลด์วันที่/เวลาที่ครบกำหนด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="8087d-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="8087d-132">คุณสามารถป้อน วันนี้</span><span class="sxs-lookup"><span data-stu-id="8087d-132">You can enter Today.</span></span>  
6. <span data-ttu-id="8087d-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8087d-133">Click Create.</span></span>
7. <span data-ttu-id="8087d-134">คลิก รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="8087d-134">Click Details.</span></span>
    * <span data-ttu-id="8087d-135">โปรดสังเกตว่าคัมบังมีงานกระบวนการสองรายการจากขั้นตอนการผลิต </span><span class="sxs-lookup"><span data-stu-id="8087d-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="8087d-136">รายการแรกคือ SpeakerAssemblyAndPolish และรายการที่สองเป็คือ SpeakerTestAndPackaging</span><span class="sxs-lookup"><span data-stu-id="8087d-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="8087d-137">นี่เป็นขั้นตอนสุดท้าย!</span><span class="sxs-lookup"><span data-stu-id="8087d-137">This is the last step!</span></span>  

