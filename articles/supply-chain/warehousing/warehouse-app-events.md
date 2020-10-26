---
title: เหตุการณ์ของแอปคลังสินค้า
description: หัวข้อนี้จะอธิบายถึงการประมวลผลเหตุการณ์ของแอปคลังสินค้าที่ใช้ในการประมวลผลข้อความเหตุการณ์ของแอปคลังสินค้าเป็นส่วนหนึ่งของชุดงาน
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988402"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="0bb1c-103">การประมวลผลเหตุการณ์ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bb1c-104">ชุดงานที่ทำงานใน Supply Chain Management สามารถใช้ข้อมูลจากคิวสำหรับเหตุการณ์การประมวลผลที่ออกโดยแอปคลังสินค้า เพื่อตอบสนองตามที่จำเป็นสำหรับเหตุการณ์ที่ส่งสัญญาณ</span><span class="sxs-lookup"><span data-stu-id="0bb1c-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="0bb1c-105">คุณลักษณะนี้จะเพิ่มเหตุการณ์ที่เกี่ยวข้องลงในคิวเพื่อตอบสนองต่อการดำเนินการบางชนิดที่ใช้โดยผู้ปฏิบัติงานที่ใช้แอป</span><span class="sxs-lookup"><span data-stu-id="0bb1c-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="0bb1c-106">ตัวอย่างเช่น เมื่อใช้คุณลักษณะ **สร้างและประมวลผลใบสั่งโอนย้ายจากแอปคลังสินค้า** ส่วนหัวของใบสั่งโอนย้ายและรายการถูกสร้างและอัพเดตใน back end เมื่อระบบรันชุดงาน **ประมวลผลเหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="0bb1c-107">เปิดใช้งานคุณลักษณะประมวลผลเหตุการณ์ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="0bb1c-108">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ ต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="0bb1c-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="0bb1c-109">ผู้ดูแลระบบสามารถใช้หน้า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="0bb1c-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="0bb1c-110">คุณลักษณะประมวลผลเหตุการณ์ของแอปคลังสินค้าถูกแสดงรายการเป็น:</span><span class="sxs-lookup"><span data-stu-id="0bb1c-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="0bb1c-111">**โมดูล** - การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="0bb1c-112">**ชื่อคุณลักษณะ** - ประมวลผลเหตุการณ์ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="0bb1c-113">ตั้งค่าชุดงานเพื่อประมวลผลเหตุการณ์ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="0bb1c-114">ประมวลผลเหตุการณ์ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-114">Process warehouse app events</span></span>

<span data-ttu-id="0bb1c-115">ตั้งค่าชุดงานที่จัดกำหนดการไว้เพื่อประมวลผลเหตุการณ์ของแอปคลังสินค้าสำหรับการสร้างใบสั่งโอนย้ายและการอัพเดตบรรทัด</span><span class="sxs-lookup"><span data-stu-id="0bb1c-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="0bb1c-116">ไปที่ **การจัดการคลังสินค้า \> งานประจำงวด \> ประมวลผลเหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="0bb1c-117">กล่องโต้ตอบประมวลผลเหตุการณ์ของแอปคลังสินค้าจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0bb1c-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="0bb1c-118">ขยาย FastTab **รันในเบื้องหลัง** และตั้งค่า **การประมวลผลชุดงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="0bb1c-119">บนแท็บด่วน **การรันในส่วนเบื้องหลัง** เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="0bb1c-120">กล่องโต้ตอบ **กำหนดการเกิดซ้ำ** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="0bb1c-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="0bb1c-121">ตั้งค่ากำหนดการรันตามที่จำเป็นสำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="0bb1c-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="0bb1c-122">เลือก **ตกลง** เพื่อกลับไปที่กล่องโต้ตอบ **ประมวลผลเหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="0bb1c-123">เลือก **ตกลง** ในกล่องโต้ตอบ **ประมวลผลเหตุการณ์ของแอปคลังสินค้า** เพื่อเพิ่มชุดงานเข้าในคิวชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0bb1c-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="0bb1c-124">สอบถามเหตุการณ์ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0bb1c-124">Query warehouse app events</span></span>

<span data-ttu-id="0bb1c-125">คุณสามารถดูข้อความคิวเหตุการณ์และข้อความเหตุการณ์ที่สร้างขึ้นโดยแอปคลังสินค้า โดยไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ล็อกอุปกรณ์เคลื่อนที่ \> เหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="0bb1c-126">กระบวนการคิวเหตุการณ์มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="0bb1c-126">The standard event queue process</span></span>

<span data-ttu-id="0bb1c-127">โดยทั่วไปคิวเหตุการณ์ของแอปคลังสินค้าจะถูกใช้กับโฟลว์ที่อธิบายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0bb1c-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="0bb1c-128">เหตุการณ์ที่ได้รับการเพิ่มเข้าในคิวโดยมีข้อความเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="0bb1c-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="0bb1c-129">ข้อความใหม่ในตอนแรกมีสถานะเหตุการณ์เป็น **กำลังรออยู่** ซึ่งหมายความว่าชุดงาน **ประมวลผลเหตุการณ์ของแอปคลังสินค้า** จะไม่มีการเบิกสินค้า และประมวลผลข้อความนี้</span><span class="sxs-lookup"><span data-stu-id="0bb1c-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="0bb1c-130">ทันทีที่สถานะข้อความถูกอัพเดตเป็น **จัดคิวแล้ว** ชุดงานของเหตุการณ์ **ประมวลผลแอปคลังสินค้า** จะเบิกสินค้า และประมวลผลเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="0bb1c-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="0bb1c-131">ชุดงานจะอัพเดตข้อมูลสถานะของเหตุการณ์เป็น **เสร็จสมบูรณ์แล้ว** หรือ **ล้มเหลว** ทั้งนี้ขึ้นอยู่กับว่ากระบวนการที่ร้องขอเป็นไปได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0bb1c-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="0bb1c-132">เมื่อข้อความเหตุการณ์ที่เกี่ยวข้องทั้งหมดเป็น **เสร็จสมบูรณ์แล้ว** เหตุการณ์จะถูกลบออกจากคิว</span><span class="sxs-lookup"><span data-stu-id="0bb1c-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="0bb1c-133">สำหรับตัวอย่างโดยละเอียด ให้ดูที่ [สร้างใบสั่งโอนย้ายจากกระบวนการของแอปคลังสินค้า](create-transfer-order-from-warehouse-app.md)</span><span class="sxs-lookup"><span data-stu-id="0bb1c-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="0bb1c-134">จัดการข้อผิดพลาดของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="0bb1c-134">Handle event errors</span></span>

<span data-ttu-id="0bb1c-135">เนื่องจากเป็นส่วนหนึ่งของการประมวลผลเหตุการณ์ของคลังสินค้า กิจกรรมของข้อความที่ร้องขออาจไม่ได้รับการประมวลผลจากชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0bb1c-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="0bb1c-136">ในกรณีนี้ ข้อความเหตุการณ์จะเปลี่ยนเป็น **ล้มเหลว**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="0bb1c-137">คุณสามารถใช้ข้อมูล **ล็อกชุดงาน** เพื่อเรียนรู้สาเหตุและทำการดำเนินการที่จำเป็นเพื่อแก้ไขปัญหาใดๆ</span><span class="sxs-lookup"><span data-stu-id="0bb1c-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="0bb1c-138">สำหรับตัวอย่างโดยละเอียด ให้ดูที่ [สร้างใบสั่งโอนย้ายจากแอปคลังสินค้า](create-transfer-order-from-warehouse-app.md)</span><span class="sxs-lookup"><span data-stu-id="0bb1c-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="0bb1c-139">เมื่อต้องการรีเซ็ตข้อความเหตุการณ์ของแอปคลังสินค้าที่ล้มเหลว:</span><span class="sxs-lookup"><span data-stu-id="0bb1c-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="0bb1c-140">ไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ล็อกของอุปกรณ์เคลื่อนที่ \> เหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="0bb1c-141">บน FastTab **ข้อความเหตุการณ์ของแอปคลังสินค้า** ให้ค้นหาและเลือกเหตุการณ์ที่เกี่ยวข้องที่แสดง **ล้มเหลว** ในคอลัมน์ **สถานะเหตุการณ์**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="0bb1c-142">เลือก **รีเซ็ต** จากแถบเครื่องมือ **ข้อความเหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="0bb1c-143">ทำงานต่อไปจนกว่าข้อความที่เกี่ยวข้องทั้งหมดจะถูกรีเซ็ต</span><span class="sxs-lookup"><span data-stu-id="0bb1c-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="0bb1c-144">นอกจากนี้ คุณยังสามารถลบข้อความเหตุการณ์ที่ **ล้มเหลว** โดยใช้ตัวเลือก **ลบ** บนแถบเครื่องมือ **ข้อความเหตุการณ์ของแอปคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0bb1c-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
