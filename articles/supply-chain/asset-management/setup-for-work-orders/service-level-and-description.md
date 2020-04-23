---
title: ระดับและคำอธิบายของบริการ
description: หัวข้อนี้จะอธิบายถึงระดับ เเละคำอธิบายการบริการสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0aa23e7fe10e684e110126bd58bd761348e44700
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215504"
---
# <a name="service-level-and-description"></a><span data-ttu-id="96cfb-103">ระดับและคำอธิบายของบริการ</span><span class="sxs-lookup"><span data-stu-id="96cfb-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="96cfb-104">เมื่อคุณสร้างใบสั่งงาน คุณอาจต้องการกำหนดระดับการให้บริการสำหรับฟิลด์นี้ และเพิ่มคำอธิบายทั่วไปลงในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="96cfb-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="96cfb-105">คุณสามารถสร้างระดับการบริการใบสั่งงานบนหน้า **ระดับการบริการใบสั่งงาน** และคำอธิบายบนหน้า **คำอธิบายใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="96cfb-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="96cfb-106">การสร้างระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="96cfb-106">Create a service level</span></span>

1. <span data-ttu-id="96cfb-107">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ใบสั่งงาน** \> **ระดับการบริการ**</span><span class="sxs-lookup"><span data-stu-id="96cfb-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="96cfb-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="96cfb-108">Select **New**.</span></span>
3. <span data-ttu-id="96cfb-109">ในฟิลด์ **ระดับการบริการ** ป้อนระดับการบริการ (ตัวอย่างเช่น หมายเลข)</span><span class="sxs-lookup"><span data-stu-id="96cfb-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="96cfb-110">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="96cfb-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="96cfb-111">บนแท็บด่วน **ใบสั่งงาน** คุณสามารถกำหนดวันที่เริ่มต้น และสิ้นสุด เเละเวลาที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="96cfb-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="96cfb-112">ฟิลด์บนแท็บด่วนนี้กำหนดรอบระยะเวลาที่ใบสั่งงานควรมีการเริ่มต้น และสิ้นสุดในระหว่าง</span><span class="sxs-lookup"><span data-stu-id="96cfb-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="96cfb-113">ใช้สำหรับใบสั่งงานที่สร้างขึ้นด้วยตนเอง และใบสั่งงานที่สร้างขึ้นตามคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="96cfb-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="96cfb-114">ในฟิลด์ **วันที่เริ่มต้น** ป้อนจำนวนของวันเพื่อกำหนดรอบระยะเวลาที่ใบสั่งงานควรเริ่มต้นในระหว่าง</span><span class="sxs-lookup"><span data-stu-id="96cfb-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="96cfb-115">จำนวนของวันที่ถูกคำนวณจากวันที่สร้างของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="96cfb-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="96cfb-116">ตัวอย่างเช่น ถ้าใบสั่งงานควรเริ่มต้นเมื่อสร้างใบสั่งงาน ป้อน **0**</span><span class="sxs-lookup"><span data-stu-id="96cfb-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="96cfb-117">ถ้าใบสั่งงานควรเริ่มต้นภายในหนึ่งอาทิตย์หลังจากสร้างใบสั่งงาน ป้อน **7**</span><span class="sxs-lookup"><span data-stu-id="96cfb-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="96cfb-118">เมื่อต้องการตั้งค่าเวลาเริ่มต้นสำหรับใบสั่งงาน เพิ่มเติมจากวันที่เริ่มต้น ให้ตั้งค่าตัวเลือก **การตั้งค่าเวลาเริ่มต้น** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="96cfb-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="96cfb-119">จากนั้นป้อนเวลาเริ่มต้นในฟิลด์ **เวลาเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="96cfb-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="96cfb-120">ถ้าคุณตั้งค่าตัวเลือกเป็น **ไม่** เวลาปัจจุบันของวันจะถูกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="96cfb-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="96cfb-121">ในฟิลด์ **วันที่สิ้นสุด** ป้อนจำนวนของวันเพื่อกำหนดรอบระยะเวลาที่ใบสั่งงานควรสิ้นสุดในระหว่าง</span><span class="sxs-lookup"><span data-stu-id="96cfb-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="96cfb-122">จำนวนของวันที่ถูกคำนวณจากวันที่เริ่มต้นของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="96cfb-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="96cfb-123">ตัวอย่างเช่น ถ้าใบสั่งงานควรสิ้นสุดภายในหนึ่งสัปดาห์ของวันที่เริ่มต้น ป้อน **7**</span><span class="sxs-lookup"><span data-stu-id="96cfb-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="96cfb-124">เมื่อต้องการตั้งค่าเวลาสิ้นสุดสำหรับใบสั่งงาน เพิ่มเติมจากวันที่สิ้นสุด ให้ตั้งค่าตัวเลือก **การตั้งค่าเวลาสิ้นสุด** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="96cfb-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="96cfb-125">จากนั้นป้อนเวลาสิ้นสุดในฟิลด์ **เวลาสิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="96cfb-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="96cfb-126">ถ้าคุณตั้งค่าตัวเลือกเป็น **ไม่** เวลาปัจจุบันของวันจะถูกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="96cfb-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="96cfb-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="96cfb-127">Select **Save**.</span></span>

![หน้าระดับการบริการของใบสั่งงาน](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="96cfb-129">สร้างคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="96cfb-129">Create a description</span></span>

1. <span data-ttu-id="96cfb-130">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ใบสั่งงาน** \> **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="96cfb-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="96cfb-131">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="96cfb-131">Select **New**.</span></span>
3. <span data-ttu-id="96cfb-132">ในฟิลด์ **คำอธิบาย** ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="96cfb-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="96cfb-133">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="96cfb-133">Select **Save**.</span></span>
