---
title: ตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ab36d9fde0cc6e864f21f9ebd09834f5098c1913
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021415"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="ebf12-103">ตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ebf12-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ebf12-104">ในระหว่างการจัดกำหนดการใบสั่งงาน คุณสามารถกำหนดลักษณะที่เกี่ยวข้องซึ่งจะมีการปันส่วนเจ้าหน้าที่บำรุงรักษาหรือกลุ่มผู้ปฏิบัติงานเพื่อดำเนินการใบสั่งงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ebf12-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="ebf12-105">การใช้ฟังก์ชันนี้ไม่จำเป็นต้องระบุ แต่จะช่วยให้คุณเลือกตัวเลือกสำหรับเจ้าหน้าที่บำรุงรักษาที่มีคุณสมบัติเหมาะสมที่สุดเพื่อทำงานให้เสร็จสมบูรณ์ ตามทักษะและความสามารถของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ebf12-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="ebf12-106">เฉพาะเจ้าหน้าที่บำรุงรักษาที่พร้อมใช้งานในเวลาที่จัดกำหนดการจะได้รับการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="ebf12-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="ebf12-107">ถ้าการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการตรงกับใบสั่งงานในระหว่างการจัดกำหนดการ แต่เจ้าหน้าที่บำรุงรักษาถูกจัดสรรให้กับงานอื่นๆ ใบสั่งงานจะได้รับการจัดกำหนดการให้กับเจ้าหน้าที่บำรุงรักษาที่พร้อมทำงานอีกคนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ebf12-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="ebf12-108">ก่อนที่คุณจะสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการได้ คุณต้องตั้งค่าเจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงานเป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="ebf12-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="ebf12-109">สำหรับคำอธิบายเกี่ยวกับวิธีการตั้งค่าเจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน ดู [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)</span><span class="sxs-lookup"><span data-stu-id="ebf12-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="ebf12-110">ตั้งค่าผู้ปฏิบัติงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ebf12-110">Set up preferred workers</span></span>

<span data-ttu-id="ebf12-111">เจ้าหน้าที่บำรุงรักษาหรือกลุ่มผู้ปฏิบัติงานที่ต้องการอาจเกี่ยวข้องกับรายการต่อไปนี้อย่างน้อยหนึ่งรายการ:</span><span class="sxs-lookup"><span data-stu-id="ebf12-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="ebf12-112">การค้า</span><span class="sxs-lookup"><span data-stu-id="ebf12-112">trade</span></span>  
- <span data-ttu-id="ebf12-113">ตัวแปรชนิดงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="ebf12-113">maintenance job type variant</span></span>  
- <span data-ttu-id="ebf12-114">ชนิดงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="ebf12-114">maintenance job type</span></span>  
- <span data-ttu-id="ebf12-115">ประเภทชนิดงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="ebf12-115">maintenance job type category</span></span>  
- <span data-ttu-id="ebf12-116">asset / สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ebf12-116">asset</span></span>  
- <span data-ttu-id="ebf12-117">ชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ebf12-117">asset type</span></span>  

<span data-ttu-id="ebf12-118">การเลือกที่มากขึ้นที่คุณสร้างสำหรับเรกคอร์ดเดียวกัน การตั้งค่าของคุณจะเฉพาะเจาะจงมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="ebf12-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="ebf12-119">คลิก **การจัดการสินทรัพย์** > **ตั้งค่า** > **ผู้ปฏิบัติงาน** > **เจ้าหน้าที่บำรุงรักษาที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="ebf12-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="ebf12-120">คลิก **สร้าง** เพื่อสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="ebf12-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="ebf12-121">เริ่มต้นโดยการสร้างผู้ปฏิบัติงานบำรุงรักษาหรือกลุ่มผู้ปฏิบัติงาน "เริ่มต้น"</span><span class="sxs-lookup"><span data-stu-id="ebf12-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="ebf12-122">ซึ่งหมายความว่าคุณสามารถเลือกได้เฉพาะในฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษาที่ต้องการ** หรือฟิลด์ **เจ้าหน้าที่บำรุงรักษาที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="ebf12-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="ebf12-123">ในภาพหน้าจอด้านล่าง คุณจะเห็นตัวอย่างในเรกคอร์ดแรกที่ "การร้องขอ" ถูกเลือกเป็น **กลุ่มเจ้าหน้าที่บำรุงรักษาที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="ebf12-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="ebf12-124">การตั้งค่าเริ่มต้นจะใช้ในระหว่างการจัดกำหนดการใบสั่งงาน ถ้าไม่มีรายการอื่น การรวมกันที่เฉพาะเจาะจงมากขึ้นจะจับคู่เนื้อหาของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ebf12-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="ebf12-125">ทำซ้ำขั้นตอนที่ 2 เพื่อสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="ebf12-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="ebf12-126">ทำการเลือกที่ต้องการ ทั้งนี้ขึ้นอยู่กับระดับรายละเอียดสำหรับกลุ่มผู้ปฏิบัติงานหรือผู้ปฏิบัติงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ebf12-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="ebf12-127">*ตัวอย่าง* ในภาพหน้าจอด้านล่าง ในเรกคอร์ดที่หก เจ้าหน้าที่บำรุงรักษา Shawn Richardson ถูกเลือกเป็นผู้ปฏิบัติงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ebf12-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="ebf12-128">เขาจะถูกเลือกโดยอัตโนมัติในระหว่างการจัดกำหนดการของใบสั่งงานที่รวมสินทรัพย์ "CH-BP1-03-02 และชนิดงานบำรุงรักษา "การประเมินสิ่งอำนวยความสะดวก" ถ้าเขาพร้อมทำงานในเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="ebf12-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="ebf12-129">โดยทั่วไป เมื่อเจ้าหน้าที่บำรุงรักษาที่ต้องการถูกเลือกระหว่างการจัดกำหนดการใบสั่ง การจัดการสินทรัพย์จะผ่านเรกคอร์ด **เจ้าหน้าที่บำรุงรักษาที่ต้องการ** ทั้งหมด เพื่อตรวจสอบการจับคู่ที่เป็นไปได้ ให้ตรวจสอบการรวมกันที่เฉพาะเจาะจงที่สุดก่อนเสมอ</span><span class="sxs-lookup"><span data-stu-id="ebf12-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="ebf12-130">ถ้าไม่พบข้อมูลที่ตรงกัน เรกคอร์ด "เริ่มต้น" ที่มีการเลือกในฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษาที่ต้องการ** หริอ **เจ้าหน้าที่บำรุงรักษาที่ต้องการ** จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="ebf12-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![รูปที่ 1](media/02-work-order-scheduling.png)

<span data-ttu-id="ebf12-132">นอกจากนี้ คุณยังสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษา *ที่รับผิดชอบ* ที่สามารถถูกเลือกได้ เมื่อมีการสร้างคำขอบำรุงรักษาหรือมีการสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ebf12-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="ebf12-133">คุณสามารถแก้ไขการเลือกได้ใน **ใบสั่งงานทั้งหมด** และ **คำขอการบำรุงรักษาทั้งหมด** ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ebf12-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="ebf12-134">สำหรับข้อมูลเพิ่มเติม ดู [เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ](../setup-for-maintenance-requests/responsible-workers.md)</span><span class="sxs-lookup"><span data-stu-id="ebf12-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="ebf12-135">ในระหว่างการจัดกำหนดการใบสั่งงาน คะแนนต่างๆจะถูกคำนวณเพื่อระบุว่าผู้ปฏิบัติงานคนใดควรจะทำงานที่เกี่ยวข้องกับใบสั่งงาน (คะแนนเหล่านั้นมีการตั้งค่าในลิงค์ **พารามิเตอร์การจัดการสินทรัพย์** > **การจัดกำหนดการใบสั่งงาน** )</span><span class="sxs-lookup"><span data-stu-id="ebf12-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="ebf12-136">ถ้าเจ้าหน้าที่บำรุงรักษาที่ต้องการอย่างน้อยสองคนหรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบได้คะแนนเดียวกันระหว่างการจัดกำหนดการใบสั่งงาน ผู้ปฏิบัติงานหนึ่งคนจะได้รับเลือกโดยการสุ่ม</span><span class="sxs-lookup"><span data-stu-id="ebf12-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="ebf12-137">อย่างไรก็ตาม ผู้ปฏิบัติงานที่มีคะแนนสูงสุดเสมอที่ได้รับการจัดสรรให้ทำใบสั่งงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ebf12-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

