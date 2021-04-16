---
title: สร้างแหล่งปฏิบัติงาน
description: 'ทรัพยากรการดำเนินงานดำเนินการกิจกรรมของโครงการหรือกระบวนการผลิต '
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ab91c449293338469fa2832156a85c4c32301fd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829053"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="6592b-103">สร้างแหล่งปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="6592b-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6592b-104">ทรัพยากรการดำเนินงานดำเนินการกิจกรรมของโครงการหรือกระบวนการผลิต </span><span class="sxs-lookup"><span data-stu-id="6592b-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="6592b-105">กระบวนงานนี้แสดงถึงวิธีการกำหนดทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="6592b-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="6592b-106">คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="6592b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="6592b-107">ไปที่ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6592b-107">Go to Resources.</span></span>
2. <span data-ttu-id="6592b-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6592b-108">Click New.</span></span>
3. <span data-ttu-id="6592b-109">ในฟิลด์ทรัพยากร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="6592b-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6592b-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="6592b-111">กำหนดพารามิเตอร์กำลังการผลิตและปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="6592b-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="6592b-112">ขยายส่วนการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6592b-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="6592b-113">ในฟิลด์เปอร์เซ็นต์ของเสีย ให้ป้อนหมายเลข </span><span class="sxs-lookup"><span data-stu-id="6592b-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="6592b-114">ในฟิลด์ประเภทการตั้งค่า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="6592b-115">ระบุประเภทต้นทุนซึ่งกำหนดวิธีตั้งค่าสำหรับการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6592b-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="6592b-116">ในฟิลด์ประเภทเวลาที่ใช้ในการผลิต ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="6592b-117">ระบุประเภทต้นทุนซึ่งกำหนดวิธีการลงบัญชีต้นทุนของเวลาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6592b-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="6592b-118">ในฟิลด์ประเภทปริมาณ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="6592b-119">ระบุประเภทต้นทุนซึ่งกำหนดวิธีการลงบัญชีสำหรับต้นทุนทรัพยากรที่ขึ้นอยู่กับปริมาณผลผลิต</span><span class="sxs-lookup"><span data-stu-id="6592b-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="6592b-120">ในฟิลด์หน่วยกำลังการผลิต ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6592b-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="6592b-121">ระบุหน่วยที่แสดงกำลังการผลิตของทรัพยากรการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6592b-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="6592b-122">ในฟิลด์กำลังการผลิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6592b-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="6592b-123">ในฟิลด์เปอร์เซ็นต์ประสิทธิภาพ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6592b-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="6592b-124">ระบุประสิทธิภาพที่คุณคาดหวังจากทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="6592b-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="6592b-125">เปอร์เซ็นต์ประสิทธิภาพปรับปริมาณที่สามารถประมวลผลได้ของทรัพยากรการดำเนินงาน และมีผลกระทบต่อเวลาที่ถูกจองไว้สำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6592b-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="6592b-126">ในฟิลด์เปอร์เซ็นต์การจัดตารางการผลิตระดับการดำเนินงาน ให้ป้อนหมายเลข </span><span class="sxs-lookup"><span data-stu-id="6592b-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="6592b-127">ระบุเปอร์เซ็นต์สูงสุดของกำลังการผลิตของทรัพยากรการดำเนินงานที่คุณต้องการใช้ในการจัดตารางการผลิตระดับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6592b-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="6592b-128">เลือกใช่ในฟิลด์กำลังการผลิตที่มีจำกัด</span><span class="sxs-lookup"><span data-stu-id="6592b-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="6592b-129">ตั้งค่าตัวเลือกนี้เป็นใช่ ถ้าทรัพยากรการดำเนินงานควรถูกกำหนดตามกำลังการผลิตที่แท้จริงที่พร้อมใช้งาน และถ้าการจองกำลังการผลิตที่มีอยู่ควรได้รับการพิจารณา </span><span class="sxs-lookup"><span data-stu-id="6592b-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="6592b-130">ถ้าตัวเลือกนี้จะตั้งค่าเป็นไม่ ทรัพยากรการดำเนินงานจะถูกถือว่ามีกำลังการผลิตมีไม่จำกัด และทรัพยากรอาจถูกจองเกินเวลา</span><span class="sxs-lookup"><span data-stu-id="6592b-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="6592b-131">เลือกใช่ในฟิลด์ทรัพยากรที่ติดขัด</span><span class="sxs-lookup"><span data-stu-id="6592b-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="6592b-132">กำหนดเวลาทำงาน</span><span class="sxs-lookup"><span data-stu-id="6592b-132">Define working times</span></span>
1. <span data-ttu-id="6592b-133">ขยายส่วนปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="6592b-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="6592b-134">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6592b-134">Click Add.</span></span>
3. <span data-ttu-id="6592b-135">ในฟิลด์ปฏิทิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="6592b-136">ระบุปฏิทินเวลาการทำงานที่กำหนดกำลังการผลิตของทรัพยากร (ในหน่วยชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="6592b-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="6592b-137">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6592b-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6592b-138">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6592b-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="6592b-139">กำหนดความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6592b-139">Define resource capabilities</span></span>
1. <span data-ttu-id="6592b-140">ขยายส่วนความสามารถ</span><span class="sxs-lookup"><span data-stu-id="6592b-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="6592b-141">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6592b-141">Click Add.</span></span>
    * <span data-ttu-id="6592b-142">ความสามารถคือ ความสามารถของทรัพยากรการดำเนินงานในการดำเนินการกิจกรรมที่เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="6592b-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="6592b-143">กลไกจัดการการจัดกำหนดการได้จัดสรรทรัพยากร โดยจัดให้ตรงกับความต้องการทรัพยากรของกิจกรรมแต่ละกิจกรรมกับความสามารถของทรัพยากรการดำเนินงานที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6592b-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="6592b-144">ในฟิลด์ความสามารถ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="6592b-145">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6592b-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="6592b-146">ระบุระดับของประสิทธิภาพโดยที่ทรัพยากรจะประมวลผลความสามารถ</span><span class="sxs-lookup"><span data-stu-id="6592b-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="6592b-147">ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6592b-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="6592b-148">ระบุระดับความสำคัญของทรัพยากรการดำเนินงานเกี่ยวข้องกับความสามารถ </span><span class="sxs-lookup"><span data-stu-id="6592b-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="6592b-149">เมื่อต้องการจัดกำหนดการตามระดับความสำคัญ ทรัพยากรการดำเนินงานที่มีความสำคัญสูงสุดจะถูกเลือกก่อน (ตัวเลขค่าต่ำสุด)</span><span class="sxs-lookup"><span data-stu-id="6592b-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="6592b-150">กำหนดทรัพยากรให้กับกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6592b-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="6592b-151">ขยายส่วนกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6592b-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="6592b-152">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6592b-152">Click Add.</span></span>
    * <span data-ttu-id="6592b-153">กลุ่มทรัพยากรกำหนดไซต์ หน่วยการผลิต และบริบทคลังสินค้าสำหรับทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="6592b-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="6592b-154">สามารถจัดกำหนดการทรัพยากรการดำเนินงานได้เฉพาะเมื่อกำหนดให้กับกลุ่มทรัพยากร และบนไซต์ที่เป็นที่ตั้งของกลุ่มทรัพยากรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6592b-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="6592b-155">ในฟิลด์กลุ่มทรัพยากร ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6592b-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="6592b-156">ในฟิลด์ที่ตั้งอินพุท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6592b-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="6592b-157">ระบุที่ตั้งคลังสินค้าเริ่มต้นจากที่ทรัพยากรการดำเนินงานกำลังใช้งานวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="6592b-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]