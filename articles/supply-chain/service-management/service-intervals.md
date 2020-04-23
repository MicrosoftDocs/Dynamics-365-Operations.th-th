---
title: ช่วงการบริการ
description: ช่วงการให้บริการบ่งชี้ความถี่พร้อมกับรายการใบสั่งบริการถูกสร้างสำหรับรายการข้อตกลงการให้บริการ เมื่อคุณสร้างใบสั่งบริการ
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5766d8ce1fa382f3f014e160d311b2dfab2bf774
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216286"
---
# <a name="service-intervals"></a><span data-ttu-id="ad8d9-103">ช่วงการบริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad8d9-104">ช่วงข้อตกลงการให้บริการบ่งชี้ความถี่พร้อมกับรายการใบสั่งบริการถูกสร้างสำหรับรายการข้อตกลงการให้บริการ เมื่อคุณสร้างใบสั่งบริการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="ad8d9-105">เมื่อคุณสร้างใบสั่งบริการโดยอัตโนมัติ ระบบจะสร้างรายการใบสั่งบริการขึ้นตามช่วงที่คุณระบุไว้สำหรับรายการข้อตกลงการให้บริการ นับจากวันที่เริ่มต้นของรายการข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="ad8d9-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="ad8d9-106">ถ้าฟิลด์ **ช่วง** ของรายการข้อตกลงการให้บริการในหน้า **ข้อตกลงการให้บริการ** ว่างเปล่า รายการจะเป็นเหตุการณ์ที่เกิดขึ้นเพียงครั้งเดียว และไม่มีการใช้เหตุการณ์นั้นเพื่อสร้างใบสั่งบริการซ้ำอีก</span><span class="sxs-lookup"><span data-stu-id="ad8d9-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="ad8d9-107">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ad8d9-107">Example</span></span>

<span data-ttu-id="ad8d9-108">ตัวอย่างนี้แสดงให้เห็นว่าช่วงการบริการจะมีผลกระทบต่อรายการข้อตกลงการให้บริการและรายการใบสั่งบริการในใบสั่งบริการอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ad8d9-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="ad8d9-109">สร้างข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-109">Create a service agreement</span></span>

<span data-ttu-id="ad8d9-110">ลำดับแรก คุณสร้างข้อตกลงการให้บริการ และตั้งค่าตัวเลือก **รวมใบสั่งบริการ** เป็น **ตามข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="ad8d9-111">คลิก **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="ad8d9-112">ใน **บานหน้าต่างการดำเนินการ** บนแท็บ **ข้อตกลงการให้บริการ** ในกลุ่ม **ใหม่** คลิก **ข้อตกลงการให้บริการ** เพื่อสร้างข้อตกลงการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="ad8d9-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="ad8d9-113">ป้อนคำอธิบาย เลือกโครงการในฟิลด์ **รหัสโครงการ** และป้อนวันที่ในฟิลด์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="ad8d9-114">ในฟิลด์ **รวมใบสั่งบริการ** เลือก **ตามข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="ad8d9-115">ขณะนี้คุณได้สร้างข้อตกลงการให้บริการต่อไปนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="ad8d9-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="ad8d9-116">Project</span><span class="sxs-lookup"><span data-stu-id="ad8d9-116">Project</span></span>      | <span data-ttu-id="ad8d9-117">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ad8d9-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8d9-118">โครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-118">Your project</span></span> | <span data-ttu-id="ad8d9-119">วันที่ที่คุณระบุสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-119">The date you specified for the project.</span></span> <span data-ttu-id="ad8d9-120">ในตัวอย่างนี้ มีการใช้วันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ad8d9-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="ad8d9-121">สร้างรายการข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-121">Create a service agreement line</span></span>

<span data-ttu-id="ad8d9-122">ถัดไป คุณสร้างรายการข้อตกลงการให้บริการที่มีชนิดธุรกรรม **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="ad8d9-123">เพื่อทำส่วนนี้ของตัวอย่างให้เสร็จสมบูรณ์ คุณต้องสร้างช่วงการบริการเป็น 10 วันในหน้า **ช่วงการบริการ**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="ad8d9-124">เลือกข้อตกลงการให้บริการที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ad8d9-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="ad8d9-125">บน FastTab **รายการ** คลิกปุ่ม **เพิ่ม** เพื่อสร้างรายการใหม่ในบานหน้าต่างด้านล่างของหน้า **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="ad8d9-126">ในฟิลด์ **ชนิดธุรกรรม** เลือก **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="ad8d9-127">ในฟิลด์ **ผู้ปฏิบัติงาน** เลือกผู้ปฏิบัติงานที่จะให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="ad8d9-128">ในฟิลด์ **ช่วงการบริการ** ให้เลือกช่วงเวลา 10 วัน</span><span class="sxs-lookup"><span data-stu-id="ad8d9-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="ad8d9-129">ขณะนี้คุณได้สร้างรายการข้อตกลงการให้บริการที่มีข้อมูลต่อไปนี้แล้ว:</span><span class="sxs-lookup"><span data-stu-id="ad8d9-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="ad8d9-130">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ad8d9-130">Transaction type</span></span> | <span data-ttu-id="ad8d9-131">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ad8d9-131">Start date</span></span>                               | <span data-ttu-id="ad8d9-132">ช่วงการบริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="ad8d9-133">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="ad8d9-133">Hour</span></span>             | <span data-ttu-id="ad8d9-134">วันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ad8d9-134">The current date.</span></span>                        | <span data-ttu-id="ad8d9-135">ทุก 10 วัน</span><span class="sxs-lookup"><span data-stu-id="ad8d9-135">Every 10 days</span></span>    |
| <span data-ttu-id="ad8d9-136">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ad8d9-136">Worker</span></span>           | <span data-ttu-id="ad8d9-137">ผู้ปฏิบัติงานที่จะดำเนินการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="ad8d9-138">ไม่มีหน้าต่างเวลาที่ระบุสำหรับรายการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="ad8d9-139">สร้างแผนการใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-139">Create planned service orders</span></span>

<span data-ttu-id="ad8d9-140">ขณะนี้ คุณสามารถสร้างใบสั่งบริการที่วางแผนไว้และรายการใบสั่งบริการสำหรับเดือนที่กำลังจะมาถึงได้</span><span class="sxs-lookup"><span data-stu-id="ad8d9-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="ad8d9-141">ในหน้า **ข้อตกลงการให้บริการ** บน **บานหน้าต่างการดำเนินการ** บนแท็บ **ส่ง** คลิก **ใบสั่งบริการที่วางแผนไว้**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="ad8d9-142">ในหน้า **สร้างใบสั่งบริการ** ป้อนวันที่ปัจจุบันในฟิลด์ **วันที่เริ่มต้น** และวันที่ที่เป็นหนึ่งเดือนจากวันที่ปัจจุบันในฟิลด์ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="ad8d9-143">ตั้งค่าตัวเลื่อน **ชั่วโมง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="ad8d9-144">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="ad8d9-144">Click **OK**.</span></span>

<span data-ttu-id="ad8d9-145">เนื่องจากไม่มีการจัดกลุ่มในใบสั่งบริการ (ที่กำหนดไว้โดยตัวเลือก **ตามข้อตกลงการให้บริการ** ในฟิลด์ **รวมข้อตกลงการให้บริการ** ) ระบบจะสร้างรายการใบสั่งบริการขึ้นหนึ่งรายการสำหรับใบสั่งบริการแต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="ad8d9-146">ใบสั่งบริการที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ad8d9-146">Service orders created</span></span>

<span data-ttu-id="ad8d9-147">รายการใบสั่งบริการสามรายการที่ได้ถูกสร้างขึ้นภายในกรอบเวลาที่คุณระบุไว้ในกล่องโต้ตอบ **สร้างใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="ad8d9-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="ad8d9-148">คุณสามารถดูรายการใบสั่งบริการได้ในหน้า **ข้อตกลงการให้บริการ** (**บานหน้าต่างการดำเนินการ** \> แท็บ **ส่ง** \>ปุ่ม**ดู** )</span><span class="sxs-lookup"><span data-stu-id="ad8d9-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad8d9-149">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ad8d9-149">Related topics</span></span>

[<span data-ttu-id="ad8d9-150">การตั้งค่าช่วงการบริการ</span><span class="sxs-lookup"><span data-stu-id="ad8d9-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

