--- 
title: "รักษากระบวนการผลิตสำหรับแบบจำลองผลิตภัณฑ์"
description: "การดำเนินกระบวนงานนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ "
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 941ba5e7775f296597a94788c7b70640bdd5a41c
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="bd653-103">รักษากระบวนการผลิตสำหรับแบบจำลองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bd653-103">Maintain a route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd653-104">การดำเนินกระบวนงานนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="bd653-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="bd653-105">กระบวนงานนี้ใช้แบบจำลองลำโพงขั้นสูงในบริษัทสาธิต USMF เพื่อดำเนินกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="bd653-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="bd653-106">เพิ่มขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="bd653-106">Add a route operation</span></span>
1. <span data-ttu-id="bd653-107">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="bd653-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="bd653-108">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bd653-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="bd653-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bd653-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bd653-110">เลือกแบบจำลองลำโพงขั้นสูงสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="bd653-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="bd653-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bd653-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bd653-112">ขยายส่วนดำเนินงานในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="bd653-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="bd653-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="bd653-113">Click Add.</span></span>
7. <span data-ttu-id="bd653-114">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="bd653-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="bd653-115">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bd653-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="bd653-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bd653-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="bd653-117">ป้อนรายละเอียดขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="bd653-117">Enter route operation details</span></span>
1. <span data-ttu-id="bd653-118">คลิกรายละเอียดการดำเนินการในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="bd653-118">Click Route operation details.</span></span>
2. <span data-ttu-id="bd653-119">ในฟิลด์การดำเนินงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bd653-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="bd653-120">ในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="bd653-120">In the Oper.</span></span> <span data-ttu-id="bd653-121">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="bd653-121">No.</span></span> <span data-ttu-id="bd653-122">ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="bd653-122">field, enter a number.</span></span>
    * <span data-ttu-id="bd653-123">หมายเลขการดำเนินงานกำหนดลำดับในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="bd653-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="bd653-124">แต่ละคุณสมบัติในกระบวนการผลิตสามารถมีค่าคงที่หรือถูกแม็ปกับคุณลักษณะ </span><span class="sxs-lookup"><span data-stu-id="bd653-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="bd653-125">การแม็ปไปยังคุณลักษณะจะมีผลกับค่าที่ถูกตั้งค่าเป็นส่วนหนึ่งของการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="bd653-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="bd653-126">ในฟิลด์กลุ่มกระบวนการผลิต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bd653-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="bd653-127">กลุ่มกระบวนการผลิตกำหนดลักษณะการทำงานที่จำเป็นสำหรับการคิดต้นทุน ปริมาณการใช้วัสดุ และการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="bd653-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="bd653-128">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="bd653-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="bd653-129">คลิกแท็บเวลา</span><span class="sxs-lookup"><span data-stu-id="bd653-129">Click the Times tab.</span></span>
7. <span data-ttu-id="bd653-130">ในฟิลด์ปริมาณกระบวนการ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="bd653-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="bd653-131">กำหนดจำนวนที่จะถูกประมวลผลในระหว่างการดำเนินงานหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bd653-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="bd653-132">ในฟิลด์ชั่วโมง/เวลา ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="bd653-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="bd653-133">ป้อนอัตราส่วนเวลา</span><span class="sxs-lookup"><span data-stu-id="bd653-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="bd653-134">เลือกการตั้งค่ากล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="bd653-134">Select the Set check box.</span></span>
10. <span data-ttu-id="bd653-135">ในฟิลด์เวลาที่ใช้ในการผลิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="bd653-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="bd653-136">กำหนดเวลาการประมวลผลสำหรับปริมาณที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="bd653-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="bd653-137">คลิกแท็บความต้องการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bd653-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="bd653-138">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="bd653-138">Click Add.</span></span>
13. <span data-ttu-id="bd653-139">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bd653-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="bd653-140">ในฟิลด์ชนิดความต้องการ ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bd653-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="bd653-141">ตัดสินใจว่าคุณต้องการระบุทรัพยากรที่เฉพาะเจาะจงหรือความสามารถที่ต้องมีอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd653-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="bd653-142">ในฟิลด์ความต้องการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bd653-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="bd653-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd653-143">Click OK.</span></span>


