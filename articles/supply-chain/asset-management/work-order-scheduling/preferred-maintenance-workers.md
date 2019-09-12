---
title: ตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887422"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="012b4-103">เจ้าหน้าที่บำรุงรักษาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="012b4-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="012b4-104">คุณสามารถกำหนดลักษณะที่จะมีการปันส่วนเจ้าหน้าที่บำรุงรักษาเพื่อดำเนินการใบสั่งงานให้เสร็จสมบูรณ์ในระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="012b4-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="012b4-105">การใช้ฟังก์ชันนี้ไม่จำเป็นต้องระบุ แต่จะช่วยให้คุณเลือกตัวเลือกสำหรับเจ้าหน้าที่บำรุงรักษาที่มีคุณสมบัติเหมาะสมที่สุดเพื่อทำงานให้เสร็จสมบูรณ์ ตามทักษะและความสามารถของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="012b4-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="012b4-106">ดังนั้น ในระหว่างการจัดกำหนดการใบสั่งงาน การตั้งค่าใน **เจ้าหน้าที่บำรุงรักษาที่ต้องการ** จะใช้ในการกำหนดว่าควรมีการจัดกำหนดการเจ้าหน้าที่บำรุงรักษาเฉพาะหรือกลุ่มเจ้าหน้าที่สำหรับใบสั่งงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="012b4-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="012b4-107">เฉพาะเจ้าหน้าที่บำรุงรักษาที่พร้อมใช้งานในเวลาที่จัดกำหนดการจะได้รับการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="012b4-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="012b4-108">ถ้าการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการตรงกับใบสั่งงานระหว่างการจัดกำหนดการ แต่เจ้าหน้าที่บำรุงรักษาถูกจัดสรรให้กับงานอื่นๆ ใบสั่งงานจะได้รับการจัดกำหนดการให้กับเจ้าหน้าที่บำรุงรักษาที่พร้อมทำงานอีกคนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="012b4-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="012b4-109">ก่อนที่คุณจะสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการได้ คุณต้องตั้งค่ากลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษาที่ควรพร้อมทำงานสำหรับการเลือกก่อน</span><span class="sxs-lookup"><span data-stu-id="012b4-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="012b4-110">อ้างอิงถึง [กลุ่มเจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)</span><span class="sxs-lookup"><span data-stu-id="012b4-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="012b4-111">ตั้งค่าผู้ปฏิบัติงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="012b4-111">Set up preferred workers</span></span>

<span data-ttu-id="012b4-112">เจ้าหน้าที่บำรุงรักษาที่ต้องการหรือกลุ่มผู้ปฏิบัติงานอาจเกี่ยวข้องกับเฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="012b4-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="012b4-113">การค้า</span><span class="sxs-lookup"><span data-stu-id="012b4-113">trade</span></span>  
- <span data-ttu-id="012b4-114">ตัวแปรชนิดงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="012b4-114">maintenance job type variant</span></span>  
- <span data-ttu-id="012b4-115">ชนิดงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="012b4-115">maintenance job type</span></span>  
- <span data-ttu-id="012b4-116">ประเภทชนิดงานบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="012b4-116">maintenance job type category</span></span>  
- <span data-ttu-id="012b4-117">asset / สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="012b4-117">asset</span></span>  
- <span data-ttu-id="012b4-118">ชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="012b4-118">asset type</span></span>  

<span data-ttu-id="012b4-119">หรือชุดข้อมูลของการเลือกเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="012b4-119">or a combination of those selections.</span></span> <span data-ttu-id="012b4-120">การเลือกที่มากขึ้นที่คุณสร้างสำหรับเรกคอร์ดเดียวกัน การตั้งค่าของคุณจะเฉพาะเจาะจงมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="012b4-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="012b4-121">คลิก **การจัดการสินทรัพย์** > **ตั้งค่า** > **ผู้ปฏิบัติงาน** > **เจ้าหน้าที่บำรุงรักษาที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="012b4-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="012b4-122">คลิก **สร้าง** เพื่อสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="012b4-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="012b4-123">เริ่มต้นด้วยการสร้างการตั้งค่ากลุ่มผู้ปฏิบัติงานหรือเจ้าหน้าที่บำรุงรักษา "เริ่มต้น" ที่ไม่มีการเลือกในฟิลด์ที่แสดงในรายการแสดงหัวข้อย่อยข้างบน</span><span class="sxs-lookup"><span data-stu-id="012b4-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="012b4-124">ซึ่งหมายความว่าคุณสามารถเลือกได้เฉพาะในฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษาที่ต้องการ** หรือฟิลด์ **เจ้าหน้าที่บำรุงรักษาที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="012b4-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="012b4-125">ในรูปด้านล่าง คุณจะเห็นตัวอย่างในเรกคอร์ดแรกที่ "การร้องขอ" ถูกเลือกเป็นกลุ่มเจ้าหน้าที่บำรุงรักษาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="012b4-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="012b4-126">การตั้งค่าเริ่มต้นจะใช้ในระหว่างการจัดกำหนดการใบสั่งงาน ในกรณีที่ไม่มีรายการอื่น การรวมกันที่เฉพาะเจาะจงมากขึ้นจับคู่เนื้อหาของใบสั่งงานในระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="012b4-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="012b4-127">ทำซ้ำขั้นตอนที่ 2 เพื่อสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="012b4-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="012b4-128">ทำการเลือกที่ต้องการ ทั้งนี้ขึ้นอยู่กับระดับรายละเอียดสำหรับกลุ่มผู้ปฏิบัติงานหรือผู้ปฏิบัติงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="012b4-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="012b4-129">*ตัวอย่าง* ในรูปด้านล่าง ในเรกคอร์ดที่หก เจ้าหน้าที่บำรุงรักษา Shawn Richardson ถูกเลือกเป็นผู้ปฏิบัติงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="012b4-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="012b4-130">เขาจะได้รับการเลือกโดยอัตโนมัติในระหว่างการจัดกำหนดการของใบสั่งงานที่รวมสินทรัพย์ "CH-BP1-03-02 และชนิดงานบำรุงรักษา "การประเมินสิ่งอำนวยความสะดวก" ถ้าเขาพร้อมทำงานในเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="012b4-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="012b4-131">โดยทั่วไป เมื่อเจ้าหน้าที่บำรุงรักษาที่ต้องการถูกเลือกระหว่างการจัดกำหนดการใบสั่ง การจัดการสินทรัพย์จะผ่านเรกคอร์ด **เจ้าหน้าที่บำรุงรักษาที่ต้องการ** ทั้งหมด เพื่อตรวจสอบการจับคู่ที่เป็นไปได้ ให้ตรวจสอบการรวมกันที่เฉพาะเจาะจงที่สุดก่อนเสมอ</span><span class="sxs-lookup"><span data-stu-id="012b4-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="012b4-132">ถ้าไม่พบข้อมูลที่ตรงกัน เรกคอร์ด "เริ่มต้น" ที่มีการเลือกในฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษาที่ต้องการ** หริอ **เจ้าหน้าที่บำรุงรักษาที่ต้องการ** จะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="012b4-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![รูปที่ 1](media/02-work-order-scheduling.png)

<span data-ttu-id="012b4-134">คุณยังสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบที่สามารถเลือกได้เมื่อมีการสร้างคำขอบำรุงรักษาหรือมีการสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="012b4-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="012b4-135">ใน **ใบสั่งงานทั้งหมด** และ **คำขอการบำรุงรักษาทั้งหมด** คุณสามารถแก้ไขการเลือกได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="012b4-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="012b4-136">อ้างอิงถึง [เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ](../setup-for-maintenance-requests/responsible-workers.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="012b4-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="012b4-137">ในระหว่างการจัดกำหนดการใบสั่งงาน คะแนนต่างๆจะถูกคำนวณเพื่อระบุว่าผู้ปฏิบัติงานคนใดควรจะทำงานที่เกี่ยวข้องกับใบสั่งงาน (คะแนนเหล่านั้นมีการตั้งค่าในลิงค์ **พารามิเตอร์การจัดการสินทรัพย์** > **การจัดกำหนดการใบสั่งงาน** )</span><span class="sxs-lookup"><span data-stu-id="012b4-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="012b4-138">ถ้าเจ้าหน้าที่บำรุงรักษาที่ต้องการอย่างน้อยสองคนหรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบได้คะแนนเดียวกันระหว่างการจัดกำหนดการใบสั่งงาน ผู้ปฏิบัติงานหนึ่งคนจะได้รับเลือกโดยการสุ่ม</span><span class="sxs-lookup"><span data-stu-id="012b4-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="012b4-139">อย่างไรก็ตาม ผู้ปฏิบัติงานที่มีคะแนนสูงสุดเสมอที่ได้รับการจัดสรรให้ทำใบสั่งงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="012b4-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

