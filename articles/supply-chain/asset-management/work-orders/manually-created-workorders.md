---
title: ใบสั่งงานที่สร้างด้วยตนเอง
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งงานด้วยตนเองในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017879"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="1c791-103">ใบสั่งงานที่สร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1c791-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1c791-104">คุณสามารถสร้างใบสั่งงานด้วยตนเองได้สองวิธี</span><span class="sxs-lookup"><span data-stu-id="1c791-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="1c791-105">บนหน้า **ใบสั่งทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1c791-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="1c791-106">บนหน้า **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่** หรือ **คำขอการบำรุงรักษาของตำแหน่งที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="1c791-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="1c791-107">สร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-107">Create work order</span></span>

1. <span data-ttu-id="1c791-108">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1c791-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1c791-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1c791-109">Select **New**.</span></span>

3. <span data-ttu-id="1c791-110">ในกล่องโต้ตอบ **สร้างใบสั่งงาน** ให้เลือกชนิดใบสั่งงานในฟิลด์ **ชนิดของใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="1c791-111">หากต้องการ เลือก **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="1c791-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="1c791-112">ในฟิลด์ **สินทรัพย์** เลือกสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1c791-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="1c791-113">เมื่อคุณเลือกสินทรัพย์ แท็บสามแท็บอาจมีอยู่ในรายการแบบหล่นลงของ **สินทรัพย์**:</span><span class="sxs-lookup"><span data-stu-id="1c791-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="1c791-114">**สินทรัพย์ที่ใช้งานอยู่** - แท็บนี้ประกอบด้วยรายการของสินทรัพย์ทั้งหมดที่มีสถานะของวงจรการใช้ของสินทรัพย์เป็น "ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="1c791-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="1c791-115">**มุมมองสินทรัพย์** - แท็บนี้แสดงมุมมองแผนภูมิของตำแหน่งที่ทำงานและสินทรัพย์ที่ติดตั้งอยู่ในนั้น</span><span class="sxs-lookup"><span data-stu-id="1c791-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="1c791-116">**สินทรัพย์ของฉัน** - แท็บนี้มีสินทรัพย์ที่เกี่ยวข้องกับสถานที่ทำงานที่คุณ (ผู้ปฏิบัติงานที่ลงชื่อเข้าสู่ระบบ) อาจได้รับการปันส่วนให้</span><span class="sxs-lookup"><span data-stu-id="1c791-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="1c791-117">(สำหรับข้อมูลเกี่ยวกับการตั้งค่า ให้ดูที่ [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)) ถ้าไม่มีการตั้งค่าสถานที่ทำงานไว้ในผู้ปฏิบัติงานใน [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md) แท็บ **สินทรัพย์ของฉัน** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1c791-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="1c791-118">ในฟิลด์ **ชนิดงานบำรุงรักษา** เลือกชนิดงานบำรุงรักษาสำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="1c791-119">หากจำเป็น เลือก **ตัวแปรชนิดงานบำรุงรักษา** และ **ความเชี่ยวชาญ**</span><span class="sxs-lookup"><span data-stu-id="1c791-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="1c791-120">หากจำเป็น คุณสามารถเปลี่ยนระดับการบริการใบสั่งงานในฟิลด์ **ระดับการบริการ**</span><span class="sxs-lookup"><span data-stu-id="1c791-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="1c791-121">เลือกวันที่ **เริ่มต้นที่คาดไว้** และวันที่ **สิ้นสุดที่คาดไว้** ในฟิลด์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1c791-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="1c791-122">คลิก **ตกลง** เพื่อสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="1c791-123">บนหน้ารายการ **ใบสั่งงานทั้งหมด** คุณสามารถแก้ไขใบสั่งงานได้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="1c791-124">บันทึกคะแนนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c791-124">Note the following points:</span></span>

- <span data-ttu-id="1c791-125">ในมุมมองรายละเอียดบนหน้ารายการ **ใบสั่งงานทั้งหมด** คุณสามารถเพิ่มสินทรัพย์ต่างๆ ลงในใบสั่งงานโดยการเพิ่มรายการบน FastTab **งานการบำรุงรักษาในใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="1c791-126">บนสินทรพัย์ คุณสามารถเลือกได้เฉพาะชนิดงานบำรุงรักษาที่ถูกกำหนดบนชนิดสินทรัพย์ที่ถูกเลือกไว้ในสินทรัพย์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c791-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="1c791-127">ถ้าคุณเปลี่ยนแปลงระดับบริการของสินทรัพย์หรือการวิพากษ์วิจารณ์สินทรัพย์ หลังจากที่คุณได้ใช้สินทรัพย์ในใบสั่งงานแล้ว จะไม่มีการปรับปรุงระดับบริการหรือการวิพากษ์วิจารณ์ในใบสั่งงานให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="1c791-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="1c791-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับระดับบริการและการวิพากษ์วิจารณ์ ให้ดูที่ [ระดับบริการของสินทรัพย์](../setup-for-objects/object-priorities.md) และ [ชนิดการวิพากษ์วิจารณ์สินทรัพย์](../setup-for-objects/object-criticalities.md)</span><span class="sxs-lookup"><span data-stu-id="1c791-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="1c791-129">การวิพากษ์วิจารณ์ในใบสั่งงานจะถูกคำนวณใหม่ทุกครั้งที่มีการเพิ่มหรือลบงานใบสั่งงานจากใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="1c791-130">ในมุมมองรายละเอียด **ใบสั่งงานทั้งหมด** > แท็บ **ส่วนหัว** > FastTab **กำหนดการ** ในฟิลด์ **กลุ่มผู้รับผิดชอบ** หรือ **ผู้รับผิดชอบ** คุณสามารถเลือกกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบได้</span><span class="sxs-lookup"><span data-stu-id="1c791-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="1c791-131">คุณสามารถเปลี่ยนการตั้งค่าเหล่านี้ได้ในขณะที่ใบสั่งงานเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1c791-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="1c791-132">ตัวอย่างเช่น สามารถเปลี่ยนแปลงได้เมื่อสถานะของวงจรการใช้ของใบสั่งงานมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1c791-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="1c791-133">การเลือกอัตโนมัติที่ทำไว้ระหว่างการสร้างใบสั่งงานจะขึ้นอยู่กับการตั้งค่าในหน้า **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ**</span><span class="sxs-lookup"><span data-stu-id="1c791-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="1c791-134">ถ้าคุณเพิ่มหรือลบงานของใบสั่งงานหลังจากที่คุณได้สร้างใบสั่งงานแล้ว และถ้าฟิลด์ **กลุ่มผุ้รับผิดชอบ** และ **ผู้รับผิดชอบ** ว่างเปล่า เมื่อคุณอัพเดตใบสั่งงาน การจัดการสินทรัพย์จะพยายามค้นหากลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบสำหรับการจับคู่ที่เป็นไปได้ในหน้าการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="1c791-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="1c791-135">หากฟิลด์ **กลุ่มผู้รับผิดชอบ** หรือ **ผู้รับผิดชอบ** มีการตั้งค่าแล้ว เมื่อคุณอัพเดตใบสั่งงาน จะไม่มีการเปลี่ยนแปลงใดๆ เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c791-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="1c791-136">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบและกลุ่มผู้ปฏิบัติงาน ดู [เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ](../setup-for-maintenance-requests/responsible-workers.md)</span><span class="sxs-lookup"><span data-stu-id="1c791-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="1c791-137">จากหน้า [สถานะการบำรุงรักษา](../controlling-and-reporting/maintenance-status.md) คุณสามารถทำการคำนวณเพื่อดูภาพรวมของปริมาณงานสำหรับใบสั่งงานที่เข้ามาและที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1c791-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="1c791-138">ในมุมมองรายละเอียดของหน้า **ใบสั่งงานทั้งหมด** บน FastTab **รายละเอียดรายการ** คุณสามารถใช้ฟิลด์ **ละติจูด** และ **ลองจิจูด** เพื่อเพิ่มพิกัดทางภูมิศาสตร์สำหรับสินทรัพย์ที่เลือกในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="1c791-139">สร้างใบสั่งงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1c791-139">Create related work order</span></span>

<span data-ttu-id="1c791-140">คุณสามารถสร้างใบสั่งงานที่เกี่ยวข้องกับใบสั่งงานที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="1c791-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="1c791-141">ความสามารถนี้มีประโยชน์ ตัวอย่างเช่น ถ้าคุณต้องการทำงานกับใบสั่งงานหลักและใบสั่งงานรอง</span><span class="sxs-lookup"><span data-stu-id="1c791-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="1c791-142">ใบสั่งงานใหม่จะขึ้นอยู่กับงานของใบสั่งงานจากใบสั่งงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1c791-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="1c791-143">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1c791-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1c791-144">เลือกใบสั่งงานเพื่อสร้างใบสั่งงานที่เกี่ยวข้องให้</span><span class="sxs-lookup"><span data-stu-id="1c791-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="1c791-145">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งงาน** ในกลุ่ม **ใหม่** ให้เลือก **ใบสั่งงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="1c791-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="1c791-146">ในกล่องโต้ตอบ **สร้างใบงานที่เกี่ยวข้อง** ในฟิลด์ **งานใบสั่งงาน** เลือกงานใบสั่งงานเพื่อสร้างใบสั่งงานที่เกี่ยวข้องให้</span><span class="sxs-lookup"><span data-stu-id="1c791-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="1c791-147">ให้เลือกชนิดงานบำรุงรักษาในฟิลด์ **ชนิดงานบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="1c791-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="1c791-148">ให้เลือกตัวแปรและการค้าของชนิดงานบำรุงรักษาที่เกี่ยวข้องในฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา** และฟิลด์ **การค้า** ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="1c791-149">ถ้าใบสั่งงานนี้เป็นใบสั่งงานแรกที่เกี่ยวข้องที่ถูกสร้างขึ้นสำหรับใบสั่งงานที่เลือก ให้ปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="1c791-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="1c791-150">เลือกตัวเลือก **ใบสั่งงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="1c791-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="1c791-151">ในฟิลด์ **ชนิดใบสั่งงาน** เลือกชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="1c791-152">ใน **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c791-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="1c791-153">ในฟิลด์ **ระดับบริการ** ให้เปลี่ยนระดับบริการของใบสั่งงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="1c791-154">ในฟิลด์ **การเริ่มต้นที่คาดไว้** และฟิลด์ **การสิ้นสุดที่คาดไว้** ให้เลือกวันที่เริ่มต้นและวันที่สิ้นสุดที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="1c791-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="1c791-155">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c791-155">Select **OK**.</span></span> <span data-ttu-id="1c791-156">ใบสั่งงานที่เกี่ยวข้องใหม่จะแสดงอยู่ในหน้ารายการ **ใบสั่งงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="1c791-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="1c791-157">ถ้าใบสั่งงานที่คุณกำลังสร้างใบสั่งงานที่เกี่ยวข้องนี้มีใบสั่งงานที่เกี่ยวข้องอยู่แล้ว ให้ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มงานใบสั่งงานใหม่ไปยังใบสั่งงานที่เกี่ยวข้องที่มีอยู่:</span><span class="sxs-lookup"><span data-stu-id="1c791-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="1c791-158">เลือกตัวเลือก **เพิ่มในใบสั่งงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="1c791-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="1c791-159">ในฟิลด์ **ใบสั่งงาน** เลือกใบสั่งงานที่เกี่ยวข้องเพื่อเพิ่มงานใบสั่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="1c791-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="1c791-160">ในฟิลด์ **ระดับบริการ** ให้เปลี่ยนระดับบริการของใบสั่งงานตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="1c791-161">ในฟิลด์ **การเริ่มต้นที่คาดไว้** และฟิลด์ **การสิ้นสุดที่คาดไว้** เปลี่ยนวันที่เริ่มต้นและวันที่สิ้นสุดที่คาดไว้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="1c791-162">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c791-162">Select **OK**.</span></span> <span data-ttu-id="1c791-163">งานใบสั่งงานจะถูกเพิ่มไปยังใบสั่งงานที่เกี่ยวข้องที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1c791-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="1c791-164">ภาพประกอบด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **สร้างใบสั่งงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="1c791-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![รูปที่ 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="1c791-166">หากคุณได้ตั้งค่าตัวพรางใบสั่งงานที่เกี่ยวข้องในฟิลด์ **พารามิเตอร์การจัดการสินทรัพย์** >  แท็บ **ใบสั่งงาน** > **ตัวพรางใบสั่งงานที่เกี่ยวข้อง** รหัสใบสั่งงานจะถูกสร้างขึ้นตามการตั้งค่าตัวพราง</span><span class="sxs-lookup"><span data-stu-id="1c791-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="1c791-167">หากไม่มีการตั้งค่าตัวพรางใบสั่งงานที่เกี่ยวข้อง รหัสใบสั่งงานที่พร้อมใช้งานถัดไปจะถูกใช้สำหรับใบสั่งงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1c791-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="1c791-168">คัดลอกใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c791-168">Copy a work order</span></span>

<span data-ttu-id="1c791-169">คุณสามารถสร้างใบสั่งงานใหม่จากใบสั่งงานที่มีอยู่ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="1c791-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="1c791-170">วิธีการทำงานนี้กับใบสั่งงานจะแตกต่างจากการสร้างใบสั่งงานตาม [แผนการบำรุงรักษา](../preventive-and-reactive-maintenance/maintenance-plans.md)</span><span class="sxs-lookup"><span data-stu-id="1c791-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="1c791-171">สิ่งนี้มีประโยชน์หากว่า ตัวอย่างเช่น ใบสั่งงานมีงานใบสั่งงานหลายอย่าง และงานที่ต่างกันควรถูกดำเนินการให้เสร็จสมบูรณ์ในสินทรัพย์ที่ต่างกันอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="1c791-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="1c791-172">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1c791-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="1c791-173">เลือกใบสั่งงานที่คุณต้องการคัดลอกเนื้อหามา</span><span class="sxs-lookup"><span data-stu-id="1c791-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="1c791-174">บนบานหน้าต่างการดำเนินการ > แท็บ **ใบสั่งงาน** > กลุ่ม **ใหม่** ให้เลือก **คัดลอกใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="1c791-175">การตั้งค่าใบสั่งงานจากใบสั่งงานที่เลือกจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c791-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="1c791-176">คุณสามารถแก้ไขฟิลด์บางฟิลด์ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="1c791-177">เลือก **ตกลง** เพื่อสร้างใบสั่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="1c791-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="1c791-178">บนหน้ารายการ **ใบสั่งงานทั้งหมด** คุณสามารถแก้ไขใบสั่งงานได้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="1c791-179">เมื่อสร้างใบสั่งงานใหม่แล้ว จะมีการคัดลอกข้อมูลบางอย่างโดยตรงจากใบสั่งงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1c791-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="1c791-180">ข้อมูลเกี่ยวกับการคาดการณ์ เครื่องมือ รายการตรวจสอบการบำรุงรักษา สถานที่ทำงาน ที่อยู่ และการจัดกำหนดการ จะไม่ถูกคัดลอก</span><span class="sxs-lookup"><span data-stu-id="1c791-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="1c791-181">แต่จะมีการเริ่มต้นจากการตั้งค่าปัจจุบันในการจัดการสินทรัพย์แทน</span><span class="sxs-lookup"><span data-stu-id="1c791-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="1c791-182">ดังนั้น ถ้ามีการเปลี่ยนแปลงข้อมูลดังกล่าวระหว่างเวลาที่สร้างใบสั่งงานแรกและเวลาที่คุณทำสำเนาของใบสั่งงาน การเปลี่ยนแปลงจะถูกรวมอยู่ในใบสั่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="1c791-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="1c791-183">ตัวอย่างประกอบด้วยการเปลี่ยนแปลงไปยังการคาดการณ์และการอัพเดตไปยังรายการการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1c791-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="1c791-184">ภาพประกอบด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **คัดลอกใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![รูปที่ 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="1c791-186">สร้างใบสั่งงานตามคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1c791-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="1c791-187">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **คำขอการบำรุงรักษา** > **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="1c791-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="1c791-188">เลือกคำขอบำรุงรักษาเพื่อสร้างใบสั่งงานให้ และคลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1c791-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="1c791-189">บนบานหน้าต่างการดำเนินการ > แท็บ **คำขอการบำรุงรักษา** > กลุ่ม **ใหม่** ให้เลือก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="1c791-190">ในกล่องโต้ตอบ **ใบสั่งงาน** ให้ตั้งค่าฟิลด์</span><span class="sxs-lookup"><span data-stu-id="1c791-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="1c791-191">หากมีการเลือกชนิดงานบำรุงรักษาไว้ในคำขอการบำรุงรักษา คุณสามารถเลือกชนิดงานบำรุงรักษาอื่นได้ เมื่อคุณสร้างใบสั่งงาน ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c791-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="1c791-192">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c791-192">Select **OK**.</span></span> <span data-ttu-id="1c791-193">ข้อความแจ้งให้คุณทราบว่าใบสั่งงานถูกสร้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="1c791-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="1c791-194">หากคุณต้องการดูใบสั่งงานที่มีการเชื่อมโยงกับคำขอการบำรุงรักษา บนหน้ารายการ **คำขอการบำรุงรักษาทั้งหมด** หรือ **คำขอการบำรุงรักษาที่ใช้งานอยู่** เลือกคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1c791-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="1c791-195">จากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **คำขอการบำรุงรักษา** ในกลุ่ม **มุมมอง** ให้เลือก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="1c791-196">ภาพประกอบด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **สร้างใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1c791-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![รูปที่ 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="1c791-198">ถ้าคุณต้องการให้ใบสั่งงานถูกสร้างขึ้นโดยอัตโนมัติ คุณสามารถจัดกำหนดการงานแผนการบำรุงรักษา หรือคุณสามารถตั้งค่า "สร้างอัตโนมัติ" [แผนการบำรุงรักษาs](../preventive-and-reactive-maintenance/maintenance-plans.md) หรือ [รอบการบำรุงรักษา](../preventive-and-reactive-maintenance/maintenance-rounds.md) ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1c791-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="1c791-199">ใบสั่งงานที่ถูกสร้างขึ้นจากคำขอการบำรุงรักษาบนหน้ารายการ **กำหนดการบำรุงรักษาทั้งหมด** มีชนิดงานบำรุงรักษาที่ถูกเลือกไว้ในคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1c791-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

