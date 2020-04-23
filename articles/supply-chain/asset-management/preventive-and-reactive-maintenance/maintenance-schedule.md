---
title: กำหนดการบำรุงรักษา
description: หัวข้อนี้อธิบายถึงกำหนดการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc45dc73073f32db78dc5a8203c661d78437e55f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203307"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="4c07c-103">กำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4c07c-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4c07c-104">กำหนดการบำรุงรักษามีรายการของแผนการบำรุงรักษาเชิงป้องกัน คำขอการบำรุงรักษา และรอบการบำรุงรักษาที่คาดไว้ทั้งหมดที่ต้องดำเนินการ รายการกำหนดการบางรายการอาจถูกแปลงเป็นใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="4c07c-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="4c07c-105">มุมมองกำหนดการบำรุงรักษาสี่มุมมองจะแตกต่างกันเล็กน้อย ขึ้นอยู่กับรายการกำหนดการบำรุงรักษาที่คุณต้องการดู</span><span class="sxs-lookup"><span data-stu-id="4c07c-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="4c07c-106">รายการในเมนู</span><span class="sxs-lookup"><span data-stu-id="4c07c-106">Menu item</span></span>                  | <span data-ttu-id="4c07c-107">คำอธิบายของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4c07c-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c07c-108">กำหนดการบำรุงรักษาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4c07c-108">All maintenance schedule</span></span>       | <span data-ttu-id="4c07c-109">รายการกำหนดการบำรุงรักษาทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="4c07c-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="4c07c-110">กำหนดการของสินทรัพย์ของฉัน</span><span class="sxs-lookup"><span data-stu-id="4c07c-110">My asset schedule</span></span>        | <span data-ttu-id="4c07c-111">รายการกำหนดการบำรุงรักษาทั้งหมดที่มีสินทรัพย์ที่ติดตั้งในตำแหน่งที่ทำงานที่คุณเกี่ยวข้องในฐานะผู้ปฏิบัติงาน (ตั้งค่าใน [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)) จะแสดงอยู่ในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="4c07c-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="4c07c-112">เปิดรายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4c07c-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="4c07c-113">รายการกำหนดการบำรุงรักษาที่มีสถานะ "สร้างแล้ว" หมายความว่ายังไม่ได้ได้รับการแปลงเป็นใบสั่งงานหรือละทิ้ง จะแสดงในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="4c07c-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="4c07c-114">เปิดกลุ่มกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4c07c-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="4c07c-115">รายการกำหนดการบำรุงรักษาที่เกี่ยวข้องกับกลุ่มใบสั่งงานจะแสดงอยู่ในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="4c07c-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="4c07c-116">หากรายการกำหนดการบำรุงรักษารวมอยู่ในกลุ่มใบสั่งงานหลายแห่ง (อ้างถึง [กลุ่มใบสั่งงาน](../work-orders/work-order-pools.md)) แต่ละกลุ่มจะแสดงหนึ่งเรกคอร์ดใน **กลุ่มกำหนดการบำรุงรักษาแบบเปิด**</span><span class="sxs-lookup"><span data-stu-id="4c07c-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="4c07c-117">การดำเนินการนี้จะทำให้ตัวเลือกการกรองข้อมูลบนกลุ่มใบสั่งงานมีประสิทธิภาพมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="4c07c-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="4c07c-118">เมื่อต้องการเปิดกำหนดการบำรุงรักษา:</span><span class="sxs-lookup"><span data-stu-id="4c07c-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="4c07c-119">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **กำหนดการบำรุงรักษา** > **กำหนดการบำรุงรักษาทั้งหมด** หรือ **รายการกำหนดการบำรุงรักษาแบบเปิด** หรือ **กลุ่มกำหนดการบำรุงรักษาแบบเปิด**</span><span class="sxs-lookup"><span data-stu-id="4c07c-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="4c07c-120">เมื่อต้องการอัพเดตกำหนดการบำรุงรักษา คลิก **แผนการบำรุงรักษา** หรือ **รอบการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="4c07c-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="4c07c-121">คุณสามารถแก้ไขรายการกำหนดการบำรุงรักษาได้โดยเลือกและคลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="4c07c-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="4c07c-122">ตัวอย่างเช่น คุณสามารถอัพเดตระดับการบริการหรือผู้ปฏิบัติงานที่รับผิดชอบงานได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="4c07c-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="4c07c-123">คุณสามารถแก้ไขรายการกำหนดการบำรุงรักษาที่ยังไม่ได้เชื่อมต่อกับใบสั่งงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4c07c-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="4c07c-124">คุณสามารถลบรายการกำหนดการบำรุงรักษาได้โดยการเลือกในหน้ารายการและการคลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="4c07c-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="4c07c-125">คุณสามารถละทิ้งรายการกำหนดการบำรุงรักษาได้โดยการเลือกในหน้ารายการและการคลิก **ละทิ้ง**</span><span class="sxs-lookup"><span data-stu-id="4c07c-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="4c07c-126">ฟังก์ชันนี้มีประโยชน์ ตัวอย่างเช่น ถ้าสินทรัพย์มีแผนการบำรุงรักษา 2,000 กิโลเมตร และแผนการบำรุงรักษา 10,000 กิโลเมตร</span><span class="sxs-lookup"><span data-stu-id="4c07c-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="4c07c-127">จากนั้น คุณอาจต้องการละทิ้งรายการที่สร้างขึ้นจากแผนการบำรุงรักษา 2,000 กิโลเมตร เมื่อสอดคล้องกับ 10,000 กิโลเมตร 20,000 กิโลเมตร 30,000 กิโลเมตร และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4c07c-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="4c07c-128">ถ้าคุณละทิ้งรายการกำหนดการบำรุงรักษาที่เกี่ยวข้องกับแผนการบำรุงรักษา รายการดังกล่าวจะไม่ปรากฏขึ้นเมื่อมีการจัดกำหนดการแผนการบำรุงรักษานั้นอีก</span><span class="sxs-lookup"><span data-stu-id="4c07c-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="4c07c-129">คุณสามารถเลือกจำนวนของรายการกำหนดการบำรุงรักษาใน **กำหนดการบำรุงรักษาทั้งหมด** และคลิก **กลุ่มใบสั่งงาน** ถ้าคุณต้องการให้รายการที่เลือกทั้งหมดรวมอยู่ในกลุ่มใบสั่งงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4c07c-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="4c07c-130">คุณสามารถเลือกจำนวนของรายการกำหนดการบำรุงรักษาใน **กำหนดการบำรุงรักษาทั้งหมด** หรือ **รายการกำหนดการบำรุงรักษาแบบเปิด** หรือ **กลุ่มกำหนดการบำรุงรักษาแบบเปิด** และคลิก **ปรับกำหนดการ** ถ้าคุณต้องการทำการปรับปรุงเดียวกันในหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="4c07c-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="4c07c-131">คุณสามารถเปลี่ยนวันที่เริ่มต้นและวันที่สิ้นสุดที่คาดไว้ ระดับบริการ และกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบที่เกี่ยวข้องกับรายการกำหนดการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4c07c-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="4c07c-132">เมื่อรายการกำหนดการบำรุงรักษาเกี่ยวข้องกับใบสั่งงาน รหัสใบสั่งงานจะแสดงอยู่ในฟิลด์ **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="4c07c-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="4c07c-133">ในรายละเอียด **สินทรัพย์ทั้งหมด** ให้ดูที่แท็บด่วน **แผนการบำรุงรักษาสินทรัพย์** คุณสามารถเลือกแผนการบำรุงรักษาสำหรับสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="4c07c-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="4c07c-134">ในภายหลัง ถ้าคุณลบรายการแผนการบำรุงรักษาที่เกี่ยวข้องกับสินทรัพย์ใน **สินทรัพย์ทั้งหมด** นอกจากนี้คุณลบรายการกำหนดการบำรุงรักษาทั้งหมดกับสถานะ "สร้างแล้ว" โดยอัตโนมัติ ซึ่งได้สร้างขึ้นโดยใช้แผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4c07c-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="4c07c-135">ดูเพิ่มเติมที่ [สร้างสินทรัพย์](../objects/create-an-object.md)</span><span class="sxs-lookup"><span data-stu-id="4c07c-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="4c07c-136">ภาพด้านล่างแสดงหน้ารายการ **กำหนดการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4c07c-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![รูปที่ 1](media/16-preventive-maintenance.png)

