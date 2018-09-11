--- 
title: "สร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์"
description: "กระบวนงานนี้แสดงวิธีการสร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และการป้อนรายละเอียดพื้นฐานเช่น คุณลักษณะและส่วนประกอบย่อย "
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 03dae7a1b068b744ff37199c797ee62bb7dd2ae0
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="e7eb7-103">สร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-103">Create a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7eb7-104">กระบวนงานนี้แสดงวิธีการสร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และการป้อนรายละเอียดพื้นฐานเช่น คุณลักษณะและส่วนประกอบย่อย </span><span class="sxs-lookup"><span data-stu-id="e7eb7-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="e7eb7-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e7eb7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="e7eb7-106">การสร้างรุ่นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-106">Create a product model</span></span>
1. <span data-ttu-id="e7eb7-107">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="e7eb7-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e7eb7-108">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="e7eb7-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e7eb7-109">Click New.</span></span>
4. <span data-ttu-id="e7eb7-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7eb7-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e7eb7-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e7eb7-112">ในฟิลด์กลยุทธ์ของโปรแกรมแก้ปัญหา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e7eb7-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="e7eb7-113">กำหนดกลยุทธวิธีการแก้ปัญหาข้อจำกัดในแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ตามข้อจำกัดมีการประมวลผล </span><span class="sxs-lookup"><span data-stu-id="e7eb7-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="e7eb7-114">ส่วนนี้จะมีผลกระทบในประสิทธิภาพของแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="e7eb7-115">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7eb7-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e7eb7-116">ส่วนประกอบรากแสดงถึงแบบจำลองการตั้งค่าคอนฟิกผลิตภัณ์ แต่ก็ยังสามารถนำมาใช้ในแบบจำลองผลิตภัณฑ์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e7eb7-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="e7eb7-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e7eb7-117">Click OK.</span></span>
9. <span data-ttu-id="e7eb7-118">ในฟิลด์นำโครงแบบมาใช้ใหม่ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="e7eb7-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="e7eb7-119">ถ้าพารามิเตอร์การตั้งค่าคอนฟิกนำกลับมาใช้ใหม่ตั้งค่าเป็น ใช่ ประบบจะเช็คสำหรับการตั้งค่าคอนฟิกที่เหมือนกันหลังจากที่รอบเวลาการตั้งค่าคอนฟิกและนำกลับมาใช้ใหม่ถ้าพบตรงกัน</span><span class="sxs-lookup"><span data-stu-id="e7eb7-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="e7eb7-120">เพิ่มคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e7eb7-120">Add attributes</span></span>
1. <span data-ttu-id="e7eb7-121">ขยายส่วนคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e7eb7-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="e7eb7-122">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7eb7-122">Click Add.</span></span>
3. <span data-ttu-id="e7eb7-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e7eb7-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e7eb7-124">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7eb7-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e7eb7-125">ในฟิลด์ชื่อโปรแกรมแก้ปัญหา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="e7eb7-126">ชื่อโปรแกรมถูกใช้โดยข้อจำกัดการแก้ปัญหาของการตั้งค่าคอนฟิกผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="e7eb7-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="e7eb7-127">ต้องไม่รวมถึงช่องว่างหรืออักขระพิเศษยกเว้น (ขีดเส้นใต้)</span><span class="sxs-lookup"><span data-stu-id="e7eb7-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="e7eb7-128">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e7eb7-129">ข้อความอธิบายจะแสดงถึงผู้ใช้การตั้งค่าคอนฟิกและดั้งนั้นจึงสามารถทำหน้าที่ช่วยเหลือในการเลือกสิทธิ์ค่าแอททริบิวต์ค่าสิทธิ์แอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="e7eb7-130">ในฟิลด์ชนิดคุณลักษณะ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="e7eb7-131">ประเภทแอททริบิวต์มิติซึ่งค่าที่พร้อมใช้งานสำหรับแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="e7eb7-132">เลือกการรวมไว้ในกล่องกาเครื่องหมายการนำมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="e7eb7-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="e7eb7-133">ตัวเลือกนี้จะพร้อมใช้งานเมื่อตัวเลือกการตั้งค่าคอนฟิกนำมาใช้ใหม่ถูกเลือก </span><span class="sxs-lookup"><span data-stu-id="e7eb7-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="e7eb7-134">รวมแอททริบิวต์ในกล่องการเครื่องหมายนำกลับมาใช้ใหม่หมายควาามว่า แอททริบิวต์นี้จะมีการพิจารณาเมื่อระบบค้นหาตรงกัน</span><span class="sxs-lookup"><span data-stu-id="e7eb7-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="e7eb7-135">เพิ่มส่วนประกอบย่อย</span><span class="sxs-lookup"><span data-stu-id="e7eb7-135">Add subcomponents</span></span>
1. <span data-ttu-id="e7eb7-136">ขยายส่วนส่วนประกอบย่อย</span><span class="sxs-lookup"><span data-stu-id="e7eb7-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="e7eb7-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="e7eb7-137">Click Add.</span></span>
3. <span data-ttu-id="e7eb7-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e7eb7-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e7eb7-139">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7eb7-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e7eb7-140">ในฟิลด์ชื่อโปรแกรมแก้ปัญหา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="e7eb7-141">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="e7eb7-142">ในฟิลด์ส่วนประกอบ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e7eb7-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="e7eb7-143">แต่ละส่วนประกอบย่อยต้องอ้างอิงคำนิยามของส่วนประกอบ </span><span class="sxs-lookup"><span data-stu-id="e7eb7-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="e7eb7-144">การออกแบบนี้สนับสนุนส่วนประกอบที่สามารถนำกลับมาใช้ไม่ได้ และช่วยให้มั่นใจว่าเมื่อมีการกำหนดส่วนประกอบ จะสามารถใช้ในรุ่นผลิตภัณฑ์จำนวนมากได้</span><span class="sxs-lookup"><span data-stu-id="e7eb7-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="e7eb7-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e7eb7-145">Click Save.</span></span>
9. <span data-ttu-id="e7eb7-146">คลิกรายละเอียดรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="e7eb7-146">Click BOM line details.</span></span>
    * <span data-ttu-id="e7eb7-147">รายละเอียดรายการ BOM จากผู้ใช้งานที่เปิดใช้งานเพื่อเลือกระบุคุณสมบัติสำหรับแอททริบิวต์ย่อย </span><span class="sxs-lookup"><span data-stu-id="e7eb7-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="e7eb7-148">แต่ละคุณสมบัติสามารถกำหนดค่าหรือแม็ปไปยังแอททริบิวต์ </span><span class="sxs-lookup"><span data-stu-id="e7eb7-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="e7eb7-149">แม็ปไปยังแอททริบิวต์จะส่งผลในรายละเอียดในการรับค่าที่แตกต่างกันขึ้นอยู่กับส่วนของการตั้งค่าคอนฟิกรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="e7eb7-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="e7eb7-150">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e7eb7-151">แต่ละส่วนประกอบย่อยแสดงถึงการตั้งค่าคอนฟิกผลิตภัณฑ์หลักกับเทคโนโลยีการจัดโครงแบบตามข้อจำกัด </span><span class="sxs-lookup"><span data-stu-id="e7eb7-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="e7eb7-152">การอ้างอิงสร้างจากหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="e7eb7-153">เลือกการตั้งค่ากล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e7eb7-153">Select the Set check box.</span></span>
12. <span data-ttu-id="e7eb7-154">เลือก ใช่ ในฟิลด์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e7eb7-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="e7eb7-155">การตั้งค่าตัวเลือกการคำนวณช่วยให้มั่นใจว่า ผลิตภัณฑ์ที่จะถูกรวมอยู่ในการคำนวณต้นทุนสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="e7eb7-156">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="e7eb7-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="e7eb7-157">เลือกการตั้งค่ากล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e7eb7-157">Select the Set check box.</span></span>
15. <span data-ttu-id="e7eb7-158">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="e7eb7-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e7eb7-159">ฟิลด์ปริมาณกำหนดจำนวนของผลิตภัณฑ์ที่จะใช้ในการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7eb7-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="e7eb7-160">เลือกการตั้งค่ากล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e7eb7-160">Select the Set check box.</span></span>
17. <span data-ttu-id="e7eb7-161">ในฟิลด์ต่อชุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="e7eb7-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="e7eb7-162">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e7eb7-162">Click OK.</span></span>


