---
title: สร้างแหล่งปฏิบัติงาน
description: 'ทรัพยากรการดำเนินงานดำเนินการกิจกรรมของโครงการหรือกระบวนการผลิต '
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91f5498bf5a5570c9d3b3f63e0a01b788fa00f35
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838642"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="0b968-103">สร้างแหล่งปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="0b968-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b968-104">ทรัพยากรการดำเนินงานดำเนินการกิจกรรมของโครงการหรือกระบวนการผลิต </span><span class="sxs-lookup"><span data-stu-id="0b968-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="0b968-105">กระบวนงานนี้แสดงถึงวิธีการกำหนดทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="0b968-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="0b968-106">คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="0b968-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="0b968-107">ไปที่ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0b968-107">Go to Resources.</span></span>
2. <span data-ttu-id="0b968-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0b968-108">Click New.</span></span>
3. <span data-ttu-id="0b968-109">ในฟิลด์ทรัพยากร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="0b968-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0b968-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="0b968-111">กำหนดพารามิเตอร์กำลังการผลิตและปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="0b968-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="0b968-112">ขยายส่วนการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="0b968-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="0b968-113">ในฟิลด์เปอร์เซ็นต์ของเสีย ให้ป้อนหมายเลข </span><span class="sxs-lookup"><span data-stu-id="0b968-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="0b968-114">ในฟิลด์ประเภทการตั้งค่า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0b968-115">ระบุประเภทต้นทุนซึ่งกำหนดวิธีตั้งค่าสำหรับการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0b968-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="0b968-116">ในฟิลด์ประเภทเวลาที่ใช้ในการผลิต ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="0b968-117">ระบุประเภทต้นทุนซึ่งกำหนดวิธีการลงบัญชีต้นทุนของเวลาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="0b968-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="0b968-118">ในฟิลด์ประเภทปริมาณ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="0b968-119">ระบุประเภทต้นทุนซึ่งกำหนดวิธีการลงบัญชีสำหรับต้นทุนทรัพยากรที่ขึ้นอยู่กับปริมาณผลผลิต</span><span class="sxs-lookup"><span data-stu-id="0b968-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="0b968-120">ในฟิลด์หน่วยกำลังการผลิต ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="0b968-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="0b968-121">ระบุหน่วยที่แสดงกำลังการผลิตของทรัพยากรการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="0b968-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="0b968-122">ในฟิลด์กำลังการผลิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0b968-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="0b968-123">ในฟิลด์เปอร์เซ็นต์ประสิทธิภาพ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0b968-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="0b968-124">ระบุประสิทธิภาพที่คุณคาดหวังจากทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="0b968-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="0b968-125">เปอร์เซ็นต์ประสิทธิภาพปรับปริมาณที่สามารถประมวลผลได้ของทรัพยากรการดำเนินงาน และมีผลกระทบต่อเวลาที่ถูกจองไว้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0b968-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="0b968-126">ในฟิลด์เปอร์เซ็นต์การจัดตารางการผลิตระดับการดำเนินงาน ให้ป้อนหมายเลข </span><span class="sxs-lookup"><span data-stu-id="0b968-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="0b968-127">ระบุเปอร์เซ็นต์สูงสุดของกำลังการผลิตของทรัพยากรการดำเนินงานที่คุณต้องการใช้ในการจัดตารางการผลิตระดับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="0b968-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="0b968-128">เลือกใช่ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="0b968-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="0b968-129">ตั้งค่าตัวเลือกนี้เป็นใช่ ถ้าทรัพยากรการดำเนินงานควรถูกกำหนดตามกำลังการผลิตที่แท้จริงที่พร้อมใช้งาน และถ้าการจองกำลังการผลิตที่มีอยู่ควรได้รับการพิจารณา </span><span class="sxs-lookup"><span data-stu-id="0b968-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="0b968-130">ถ้าตัวเลือกนี้จะตั้งค่าเป็นไม่ ทรัพยากรการดำเนินงานจะถูกถือว่ามีกำลังการผลิตมีไม่จำกัด และทรัพยากรอาจถูกจองเกินเวลา</span><span class="sxs-lookup"><span data-stu-id="0b968-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="0b968-131">เลือกใช่ในฟิลด์ทรัพยากรที่ติดขัด</span><span class="sxs-lookup"><span data-stu-id="0b968-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="0b968-132">กำหนดเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="0b968-132">Define working times</span></span>
1. <span data-ttu-id="0b968-133">ขยายส่วนปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="0b968-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="0b968-134">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="0b968-134">Click Add.</span></span>
3. <span data-ttu-id="0b968-135">ในฟิลด์ปฏิทิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="0b968-136">ระบุปฏิทินเวลาการทำงานที่กำหนดกำลังการผลิตของทรัพยากร (ในหน่วยชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="0b968-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="0b968-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0b968-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0b968-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0b968-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="0b968-139">กำหนดความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0b968-139">Define resource capabilities</span></span>
1. <span data-ttu-id="0b968-140">ขยายส่วนความสามารถ</span><span class="sxs-lookup"><span data-stu-id="0b968-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="0b968-141">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="0b968-141">Click Add.</span></span>
    * <span data-ttu-id="0b968-142">ความสามารถคือ ความสามารถของทรัพยากรการดำเนินงานในการดำเนินการกิจกรรมที่เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="0b968-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="0b968-143">กลไกจัดการการจัดกำหนดการได้จัดสรรทรัพยากร โดยจัดให้ตรงกับความต้องการทรัพยากรของกิจกรรมแต่ละกิจกรรมกับความสามารถของทรัพยากรการดำเนินงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0b968-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="0b968-144">ในฟิลด์ความสามารถ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="0b968-145">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0b968-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="0b968-146">ระบุระดับของประสิทธิภาพโดยที่ทรัพยากรจะประมวลผลความสามารถ</span><span class="sxs-lookup"><span data-stu-id="0b968-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="0b968-147">ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0b968-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="0b968-148">ระบุระดับความสำคัญของทรัพยากรการดำเนินงานเกี่ยวข้องกับความสามารถ </span><span class="sxs-lookup"><span data-stu-id="0b968-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="0b968-149">เมื่อต้องการจัดกำหนดการตามระดับความสำคัญ ทรัพยากรการดำเนินงานที่มีความสำคัญสูงสุดจะถูกเลือกก่อน (ตัวเลขค่าต่ำสุด)</span><span class="sxs-lookup"><span data-stu-id="0b968-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="0b968-150">กำหนดทรัพยากรให้กับกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0b968-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="0b968-151">ขยายส่วนกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="0b968-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="0b968-152">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="0b968-152">Click Add.</span></span>
    * <span data-ttu-id="0b968-153">กลุ่มทรัพยากรกำหนดไซต์ หน่วยการผลิต และบริบทคลังสินค้าสำหรับทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="0b968-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="0b968-154">สามารถจัดกำหนดการทรัพยากรการดำเนินงานได้เฉพาะเมื่อกำหนดให้กับกลุ่มทรัพยากร และบนไซต์ที่เป็นที่ตั้งของกลุ่มทรัพยากรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0b968-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="0b968-155">ในฟิลด์กลุ่มทรัพยากร ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0b968-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="0b968-156">ในฟิลด์ที่ตั้งอินพุท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0b968-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="0b968-157">ระบุที่ตั้งคลังสินค้าเริ่มต้นจากที่ทรัพยากรการดำเนินงานกำลังใช้งานวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="0b968-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

