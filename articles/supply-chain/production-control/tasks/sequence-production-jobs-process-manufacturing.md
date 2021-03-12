---
title: จัดลำดับงานการผลิตสำหรับการผลิตตามกระบวนการ
description: 'กระบวนงานนี้ใช้ผลิตภัณฑ์สีเป็นตัวอย่าง เพื่อแสดงวิธีจัดลำดับใบสั่งที่วางแผนไว้ตามลำดับความสำคัญของสีและขนาดแพคเกจ '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22c767a3de8fd937d9032a5bf285dfb4ced3d55
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981077"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="65fcb-103">จัดลำดับงานการผลิตสำหรับการผลิตตามกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="65fcb-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65fcb-104">กระบวนงานนี้ใช้ผลิตภัณฑ์สีเป็นตัวอย่าง เพื่อแสดงวิธีจัดลำดับใบสั่งที่วางแผนไว้ตามลำดับความสำคัญของสีและขนาดแพคเกจ </span><span class="sxs-lookup"><span data-stu-id="65fcb-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="65fcb-105">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USPI </span><span class="sxs-lookup"><span data-stu-id="65fcb-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="65fcb-106">กระบวนงานนี้มีไว้สำหรับผู้วางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="65fcb-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="65fcb-107">รันการวางแผนหลักสำหรับ USPI</span><span class="sxs-lookup"><span data-stu-id="65fcb-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="65fcb-108">ไปที่การวางแผนหลัก > การวางแผนหลัก > การรัน > การวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="65fcb-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="65fcb-109">ในฟิลด์แผนหลัก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="65fcb-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="65fcb-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="65fcb-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="65fcb-111">เลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="65fcb-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="65fcb-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="65fcb-112">Click OK.</span></span>
    * <span data-ttu-id="65fcb-113">นี่เริ่มต้นแผนหลัก ซึ่งรวมถึงกระบวนการตามลำดับ </span><span class="sxs-lookup"><span data-stu-id="65fcb-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="65fcb-114">กระบวนการนี้ใช้เวลา 2 - 3 นาที</span><span class="sxs-lookup"><span data-stu-id="65fcb-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="65fcb-115">ดูใบสั่งที่วางแผนไว้สำหรับผลิตภัณฑ์สี</span><span class="sxs-lookup"><span data-stu-id="65fcb-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="65fcb-116">ไปที่การวางแผนหลัก > การวางแผนหลัก > ใบสั่งที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="65fcb-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="65fcb-117">ขยายกล่องแสดงข้อมูลย่อรายละเอียดสินค้า</span><span class="sxs-lookup"><span data-stu-id="65fcb-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="65fcb-118">ขยายกล่องแสดงข้อมูลย่อรายละเอียดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="65fcb-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="65fcb-119">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="65fcb-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="65fcb-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="65fcb-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="65fcb-121">เลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="65fcb-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="65fcb-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="65fcb-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="65fcb-123">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์ หมายเลขสินค้าด้วยค่า 'P300'</span><span class="sxs-lookup"><span data-stu-id="65fcb-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="65fcb-124">ปลดล็อคเพื่อเลื่อนลงมาด้านขวา เพื่อดูวันที่ใบสั่งและวันที่การจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="65fcb-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="65fcb-125">สังเกตว่าสินค้าเหล่านี้มีวันที่ใบสั่งเป็นวันนี้ และวันที่การจัดส่งสำหรับใบสั่งที่วางแผนไว้ไม่ได้อยู่ตามลำดับของสีหรือขนาดแพคเกจ ตามที่แสดงในชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="65fcb-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="65fcb-126">คุณสามารถเลื่อนเมาส์ไปที่หมายเลขสินค้า เพื่อดูชื่อผลิตภัณฑ์และความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="65fcb-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="65fcb-127">จัดลำดับใบสั่งที่วางแผนไว้สำหรับสี</span><span class="sxs-lookup"><span data-stu-id="65fcb-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="65fcb-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="65fcb-128">Close the page.</span></span>
2. <span data-ttu-id="65fcb-129">ไปที่การวางแผนหลัก > การวางแผนหลัก > แผนการใบสั่งที่จัดลำดับ</span><span class="sxs-lookup"><span data-stu-id="65fcb-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="65fcb-130">ขยายกล่องแสดงข้อมูลย่อรายละเอียดสินค้า</span><span class="sxs-lookup"><span data-stu-id="65fcb-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="65fcb-131">ขยายกล่องแสดงข้อมูลย่อรายละเอียดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="65fcb-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="65fcb-132">หมายเหตุ: ที่นี่คุณจะเห็นว่าวันที่/เวลาเริ่มต้น สำหรับใบสั่งที่วางแผนไว้ถูกจัดลำดับตามสีและขนาดแพคเกจภายในช่วง 28 วัน</span><span class="sxs-lookup"><span data-stu-id="65fcb-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="65fcb-133">ช่วงเวลาเหล่านี้ถูกกำหนดโดยหมายเลขในการส่งเสริมการขายของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="65fcb-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="65fcb-134">แผนการใบสั่งที่จัดลำดับจากการดำเนินการ เช่น แบบฟอร์มใบสั่งที่วางแผนไว้โดยทั่วไป และผู้วางแผนการผลิตสามารถยืนยันใบสั่งที่วางแผนไว้ได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="65fcb-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="65fcb-135">ทำเครื่องหมายแถวทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="65fcb-135">Mark all rows.</span></span>
6. <span data-ttu-id="65fcb-136">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="65fcb-136">Click Accept.</span></span>
    * <span data-ttu-id="65fcb-137">นี่จะอัพเดตใบสั่งที่วางแผนไว้ ซึ่งมีการดำเนินการตามลำดับที่เลือกของแบบเลื่อนออกไปหรือแบบล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="65fcb-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="65fcb-138">ตรวจสอบความถูกต้องของลำดับใบสั่งที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="65fcb-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="65fcb-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="65fcb-139">Close the page.</span></span>
2. <span data-ttu-id="65fcb-140">ไปที่การวางแผนหลัก > การวางแผนหลัก > ใบสั่งที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="65fcb-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="65fcb-141">ขยายกล่องแสดงข้อมูลย่อรายละเอียดสินค้า</span><span class="sxs-lookup"><span data-stu-id="65fcb-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="65fcb-142">ขยายกล่องแสดงข้อมูลย่อรายละเอียดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="65fcb-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="65fcb-143">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="65fcb-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="65fcb-144">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="65fcb-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="65fcb-145">เลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="65fcb-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="65fcb-146">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="65fcb-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="65fcb-147">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์ หมายเลขสินค้าด้วยค่า 'P300'</span><span class="sxs-lookup"><span data-stu-id="65fcb-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="65fcb-148">สังเกตว่า ขณะนี้ใบสั่งถูกจัดลำดับตามความสำคัญของสีและขนาด และใบสั่งที่วางแผนไว้เริ่มต้นที่วันที่ใบสั่งและวันที่การจัดส่งที่เร็วที่สุด </span><span class="sxs-lookup"><span data-stu-id="65fcb-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="65fcb-149">ตรวจสอบความถูกต้องว่าคอลัมน์วันที่ใบสั่งหรือวันที่เริ่มต้นอยู่ใน FactBbox รายละเอียดที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="65fcb-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

