---
title: ใบสั่งงานที่สร้างด้วยตนเอง
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งงานด้วยตนเองในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875923"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="0fa62-103">ใบสั่งงานที่สร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0fa62-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="0fa62-104">คุณสามารถสร้างใบสั่งงานด้วยตนเองได้สองวิธี</span><span class="sxs-lookup"><span data-stu-id="0fa62-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="0fa62-105">ใน **ใบสั่งทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0fa62-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="0fa62-106">ใน **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่** หรือ **คำขอการบำรุงรักษาของตำแหน่งที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="0fa62-107">สร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0fa62-107">Create work order</span></span>

1. <span data-ttu-id="0fa62-108">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0fa62-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0fa62-109">คลิกปุ่ม **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0fa62-109">Click the **New** button.</span></span>

3. <span data-ttu-id="0fa62-110">ในรายการแบบหล่นลง **สร้างใบสั่งงาน** เลือกชนิดของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0fa62-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="0fa62-111">หากต้องการ เลือกคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="0fa62-111">If required, select a description.</span></span>

5. <span data-ttu-id="0fa62-112">เลือกสินทรัพย์สำหรับใบสั่งงานและชนิดงานการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="0fa62-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="0fa62-113">เมื่อคุณเลือกสินทรัพย์ อาจมีสามแท็บที่ใช้งานได้: แท็บ **สินทรัพย์ของฉัน** สินทรัพย์ที่เกี่ยวข้องกับตำแหน่งที่ทำงานซึ่งคุณ (ผู้ปฏิบัติงานที่เข้าสู่ระบบอยู่) อาจถูกจัดสรรให้ (ตั้งค่า ใน [เจ้าหน้าที่บำรุงรักษา และ กลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md))</span><span class="sxs-lookup"><span data-stu-id="0fa62-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="0fa62-114">ถ้าไม่มีการตั้งค่าตำแหน่งที่ทำงานในผู้ปฏิบัติงาน [เจ้าหน้าที่บำรุงรักษา และกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md) แท็บ **สินทรัพย์ของฉัน** จะไม่สามารถมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="0fa62-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="0fa62-115">แท็บ **สินทรัพย์ที่ใช้งานอยู่** ประกอบด้วยรายการของสินทรัพย์ทั้งหมดที่มีสถานะของวงจรการใช้ของสินทรัพย์เป็น "ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="0fa62-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="0fa62-116">แท็บ **มุมมองสินทรัพย์** แสดงมุมมองแผนภูมิของตำแหน่งที่ทำงานและสินทรัพย์ที่ติดตั้งอยู่ในตำแหน่งเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="0fa62-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="0fa62-117">หากจำเป็น เลือก **ตัวแปรชนิดงานบำรุงรักษา** และ **ความเชี่ยวชาญ**</span><span class="sxs-lookup"><span data-stu-id="0fa62-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="0fa62-118">หากจำเป็น คุณสามารถเปลี่ยนระดับการบริการใบสั่งงานในฟิลด์ **ระดับการบริการ**</span><span class="sxs-lookup"><span data-stu-id="0fa62-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="0fa62-119">เลือกวันที่เริ่มต้นและสิ้นสุดที่คาดไว้ในฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0fa62-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="0fa62-120">คลิก **ตกลง** เพื่อสร้างใบสั่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="0fa62-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="0fa62-121">แก้ไขใบสั่งงาน ใน **ใบสั่งงานทั้งหมด**หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="0fa62-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="0fa62-122">ใน **ใบสั่งงานทั้งหมด** คุณสามารถเพิ่มสินทรัพย์ต่างๆ ลงในใบสั่งงานในมุมมองรายละเอียด โดยการเพิ่มรายการบนแท็บด่วน **งานการบำรุงรักษาใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="0fa62-123">บนสินทรพัย์ คุณสามารถเลือกได้เฉพาะชนิดงานการบำรุงรักษาที่ถูกกำหนดบนชนิดสินทรัพย์ที่เลือกไว้ สำหรับสินทรัพย์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0fa62-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="0fa62-124">ถ้าคุณได้เปลี่ยนระดับการบริการของสินทรัพย์ หรือการวิพากษ์วิจารณ์สินทรัพย์หลังจากที่คุณได้ใช้กับใบสั่งงานแล้ว (อ้างถึง [ระดับการบริการของสินทรัพย์](../setup-for-objects/object-priorities.md) และ [การวิพากษ์วิจารณ์สินทรัพย์](../setup-for-objects/object-criticalities.md)) ระดับการบริการหรือการวิพากษ์วิจารณ์บนใบสั่งงานจะไม่ถูกอัพเดตตามนั้น</span><span class="sxs-lookup"><span data-stu-id="0fa62-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="0fa62-125">การวิพากษ์วิจารณ์ในใบสั่งงานจะถูกคำนวณใหม่ทุกครั้งที่มีการเพิ่มหรือลบรายการใบสั่งงานจากใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0fa62-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="0fa62-126">ในมุมมองรายละเอียด **ใบสั่งงานทั้งหมด** > **หัวข้อ** ดู > แท็บด่วน **กำหนดการ** คุณสามารถเลือกกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ ในฟิลด์ **กลุ่มผู้รับผิดชอล** หรือ **ผู้รับผิดชอบ**</span><span class="sxs-lookup"><span data-stu-id="0fa62-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="0fa62-127">การตั้งค่าเหล่านี้สามารถเปลี่ยนแปลงได้ตราบใดที่ใบสั่งงานเปิดใช้งานอยู่ ตัวอย่าง เช่น เมื่อสถานะวงจรของใบสั่งงานมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="0fa62-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="0fa62-128">การเลือกอัตโนมัติที่ทำไว้ระหว่างการสร้างใบสั่งงานจะขึ้นอยู่กับการตั้งค่า **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ**</span><span class="sxs-lookup"><span data-stu-id="0fa62-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="0fa62-129">ถ้าคุณเพิ่มหรือลบงานของใบสั่งงานหลังจากที่คุณได้สร้างใบสั่งงานแล้ว ฟิลด์ **กลุ่มผุ้รับผิดชอบ** และ **ผู้รับผิดชอบ** จะว่างเปล่าเมื่อคุณอัพเดตใบสั่งงาน การค้นหาการจัดการสินทรัพย์ สำหรับการจับคู่ที่เป็นไปได้ในฟอร์มการตั้งค่าสำหรับกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือผู้ปฏิบัติงานบำรุงรักษาที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="0fa62-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="0fa62-130">หากฟิลด์ **กลุ่มผู้รับผิดชอบ** หรือฟิลด์ **ผู้รับผิดชอบ** มีการกรอกข้อมูลแล้ว เมื่อคุณอัพเดตใบสั่งงานจะไม่มีการเปลี่ยนแปลงใดๆเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0fa62-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="0fa62-131">ใน **สถานะการบำรุงรักษา** คุณสามารถทำการคำนวณเพื่อดูภาพรวมของปริมาณงานเกี่ยวกับใบสั่งงานที่เข้ามาและที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0fa62-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="0fa62-132">บนแท็บด่วน **รายละเอียดรายการ** ใช้ฟิลด์ **ละติจูด** และ **ลองจิจูด** เพื่อเพิ่มพิกัดทางภูมิศาสตร์สำหรับสินทรัพย์ที่เลือกในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0fa62-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="0fa62-133">สร้างใบสั่งงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0fa62-133">Create related work order</span></span>

<span data-ttu-id="0fa62-134">คุณสามารถสร้างใบสั่งงานที่เกี่ยวข้องกับใบสั่งงานที่มีอยู่ได้หากว่า ตัวอย่างเช่น คุณต้องการทำงานกับใบสั่งงานหลักและใบสั่งงานรอง</span><span class="sxs-lookup"><span data-stu-id="0fa62-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="0fa62-135">ใบสั่งงานใหม่จะขึ้นอยู่กับงานของใบสั่งงานจากใบสั่งงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0fa62-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="0fa62-136">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0fa62-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0fa62-137">เลือกใบสั่งงานที่คุณต้องการทำใบสั่งงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0fa62-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="0fa62-138">คลิก **ใบสั่งที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="0fa62-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="0fa62-139">ในกล่องโต้ตอบแบบหล่นลง **สร้างใบงานที่เกี่ยวข้อง** เลือกงานใบสั่งงานที่คุณต้องการสร้างใบสั่งงานที่เกี่ยวข้อง ในฟิลด์ **งานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="0fa62-140">เลือกชนิดงานการบำรุงรักษาในฟิลด์ **ชนิดงานการบำรุงรักษา** และเลือกตัวแปรของชนิดงานการบำรุงรักษาที่เกี่ยวข้องในฟิลด์ **ตัวแปรของชนิดงานการบำรุงรักษา** และ **ความเชี่ยวชาญ** หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="0fa62-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="0fa62-141">หากนี่เป็นใบสั่งงานที่เกี่ยวข้องใบแรกที่คุณสร้างขึ้น คลิกปุ่มเรดิโฮ **ใบสั่งงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="0fa62-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="0fa62-142">เลือก **ชนิดของใบสั่งงาน** และ **คำอธิบาย** ในฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0fa62-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="0fa62-143">หากจำเป็น คุณสามารถเปลี่ยนระดับการบริการของใบสั่งงาน ในฟิลด์ **ระดับการบริการ**</span><span class="sxs-lookup"><span data-stu-id="0fa62-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="0fa62-144">ใส่วันที่เริ่มต้นและสิ้นสุดที่คาดไว้ในฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0fa62-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="0fa62-145">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0fa62-145">Click **OK**.</span></span> <span data-ttu-id="0fa62-146">ใบสั่งงานที่เกี่ยวข้องใหม่ จะแสดงอยู่ในรายการ **ใบสั่งงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0fa62-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="0fa62-147">หากคุณสร้างใบสั่งงานที่เกี่ยวข้องบนใบสั่งงานที่มีใบสั่งงานที่เกี่ยวข้องอยู่แล้ว คุณสามารถเพิ่มงานใบสั่งงานไปยังใบสั่งงานที่เกี่ยวข้องอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="0fa62-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="0fa62-148">การดำเนินการนี้ทำได้โดย การคลิกปุ่มเรดิโอ **เพิ่มใบสั่งงานที่เกี่ยวข้อง** ในขั้นตอนที่ 6</span><span class="sxs-lookup"><span data-stu-id="0fa62-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="0fa62-149">จากนั้นให้คุณเลือกใบสั่งงานที่เกี่ยวข้องซึ่งคุณต้องการเพิ่มงานใบสั่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="0fa62-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="0fa62-150">แก้ไขฟิลด์ **ระดับการบริการ** **การเริ่มต้นที่คาดไว้** และ **การสิ้นสุดที่คาดไว้** ตามต้องการ และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0fa62-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="0fa62-151">งานใบสั่งงานจะถูกเพิ่มไปยังใบสั่งงานที่เกี่ยวข้องที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0fa62-151">The work order job is added to the existing related work order.</span></span>


![รูปที่ 1](media/03-work-orders.png)

<span data-ttu-id="0fa62-153">**หมายเหตุ:** หากคุณได้ตั้งค่าตัวพรางใบสั่งงานที่เกี่ยวข้อง ในฟิลด์ **พารามิเตอร์การจัดการสินทรัพย์** > **ใบสั่งงาน** ลิงก์ > **ตัวพรางใบสั่งงานที่เกี่ยวข้อง** รหัสใบสั่งงานจะถูกสร้างขึ้นตามการตั้งค่าตัวพราง</span><span class="sxs-lookup"><span data-stu-id="0fa62-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="0fa62-154">หากไม่มีการตั้งค่าตัวพรางใบสั่งงานที่เกี่ยวข้อง รหัสใบสั่งงานที่พร้อมใช้งานถัดไปจะถูกใช้สำหรับใบสั่งงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0fa62-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="0fa62-155">คัดลอกใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0fa62-155">Copy work order</span></span>

<span data-ttu-id="0fa62-156">คุณสามารถสร้างใบสั่งงานใหม่จากใบสั่งงานที่มีอยู่ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="0fa62-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="0fa62-157">วิธีการทำงานกับใบสั่งงานจะแตกต่างจากการสร้างใบสั่งงานตามแผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="0fa62-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="0fa62-158">สิ่งนี้มีประโยชน์หากว่า ตัวอย่างเช่น คุณมีใบสั่งงานที่มีงานของใบสั่งงานหลายอย่างที่ต่างกันในสินทรัพย์ที่ต่างกัน ที่ควรดำเนินการให้เสร็จสมบูรณ์อย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="0fa62-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="0fa62-159">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0fa62-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0fa62-160">เลือกใบสั่งงานที่คุณต้องการคัดลอกเนื้อหาไปไว้</span><span class="sxs-lookup"><span data-stu-id="0fa62-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="0fa62-161">คลิก **คัดลอกใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-161">Click **Copy work order**.</span></span> <span data-ttu-id="0fa62-162">การตั้งค่าใบสั่งงานจากใบสั่งงานที่เลือกจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0fa62-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="0fa62-163">หากจำเป็น คุณสามารถแก้ไขฟิลด์บางฟิลด์ได้</span><span class="sxs-lookup"><span data-stu-id="0fa62-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="0fa62-164">คลิก **ตกลง** เพื่อสร้างใบสั่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="0fa62-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="0fa62-165">แก้ไขใบสั่งงาน ใน **ใบสั่งงานทั้งหมด**หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="0fa62-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="0fa62-166">เมื่อสร้างใบสั่งงานใหม่แล้ว จะมีการคัดลอกข้อมูลบางอย่างโดยตรงจากใบสั่งงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0fa62-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="0fa62-167">ข้อมูลเกี่ยวกับการคาดการณ์ เครื่องมือ รายการการบำรุงรักษา สถานที่ทำงาน ที่อยู่ และการจัดกำหนดการ จะไม่ได้รับการคัดลอก แต่เริ่มต้นจากการตั้งค่าปัจจุบันในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="0fa62-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="0fa62-168">ซึ่งหมายความว่าหากมีการเปลี่ยนแปลงในข้อมูลเหล่านั้นตั้งแต่เวลาที่สร้างใบสั่งงานแรกจนถึงเวลาที่คุณทำการคัดลอกใบสั่งงาน การเปลี่ยนแปลงดังกล่าวจะรวมอยู่ในใบสั่งงานใหม่ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0fa62-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="0fa62-169">ตัวอย่างมีการเปลี่ยนแปลงในการคาดการณ์หรือรายการการบำรุงรักษาที่อัพเดต</span><span class="sxs-lookup"><span data-stu-id="0fa62-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![รูปที่ 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="0fa62-171">สร้างใบสั่งงานตามคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="0fa62-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="0fa62-172">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **คำขอการบำรุงรักษา** > **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่**      </span><span class="sxs-lookup"><span data-stu-id="0fa62-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="0fa62-173">เลือกคำขอบำรุงรักษาที่คุณต้องการสร้างใบสั่งงาน แล้วคลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="0fa62-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="0fa62-174">ใน **คำขอทั้งหมด** คลิก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="0fa62-175">กรอกข้อมูลแบบหล่นลง **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="0fa62-176">หากมีการเลือกชนิดงานการบำรุงรักษาไว้ในคำขอการบำรุงรักษา คุณสามารถเลือกชนิดงานการบำรุงรักษาอื่นได้ถ้าจำเป็น เมื่อคุณสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0fa62-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="0fa62-177">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0fa62-177">Click **OK**.</span></span> <span data-ttu-id="0fa62-178">คุณจะเห็นข้อความที่แจ้งให้คุณทราบว่ามีการสร้างใบสั่งงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="0fa62-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="0fa62-179">หากคุณต้องการดูว่าใบสั่งงานไหนมีการเชื่อมโยงกับคำขอการบำรุงรักษา เลือก คำขอบำรุงรักษา ในรายการ **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่** แล้วคลิกปุ่ม **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0fa62-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![รูปที่ 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="0fa62-181">ใบสั่งงานยังสามารถสร้างขึ้นโดยอัตโนมัติโดยการจัดกำหนดการงานแผนการบำรุงรักษา หรือโดยการตั้งค่า "สร้างอัตโนมัติ" แผนการบำรุงรักษาหรือรอบการบำรุงรักษาในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="0fa62-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="0fa62-182">ใบสั่งงานที่สร้างขึ้นจากคำขอการบำรุงรักษา ใน **กำหนดการบำรุงรักษา** จะถูกสร้างขึ้นโดยใช้ชนิดงานการบำรุงรักษาที่เลือกไว้ในคำขอบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="0fa62-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

