---
title: สร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการสร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และการป้อนรายละเอียดพื้นฐานเช่น คุณลักษณะและส่วนประกอบย่อย '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921376"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="16228-103">สร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="16228-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16228-104">กระบวนงานนี้แสดงวิธีการสร้างแบบจำลองการจัดโครงแบบผลิตภัณฑ์ และการป้อนรายละเอียดพื้นฐานเช่น คุณลักษณะและส่วนประกอบย่อย </span><span class="sxs-lookup"><span data-stu-id="16228-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="16228-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="16228-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="16228-106">การสร้างรุ่นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="16228-106">Create a product model</span></span>

1. <span data-ttu-id="16228-107">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="16228-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="16228-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="16228-108">Select **New**.</span></span>
1. <span data-ttu-id="16228-109">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="16228-110">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="16228-111">ในฟิลด์ **กลยุทธ์ของโปรแกรมแก้ปัญหา** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="16228-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="16228-112">กำหนดกลยุทธวิธีการแก้ปัญหาข้อจำกัดในแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์ตามข้อจำกัดมีการประมวลผล </span><span class="sxs-lookup"><span data-stu-id="16228-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="16228-113">ส่วนนี้จะมีผลกระทบในประสิทธิภาพของแบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="16228-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="16228-114">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="16228-115">ส่วนประกอบรากแสดงถึงแบบจำลองการตั้งค่าคอนฟิกผลิตภัณ์ แต่ก็ยังสามารถนำมาใช้ในแบบจำลองผลิตภัณฑ์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="16228-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="16228-116">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="16228-116">Select **OK**.</span></span>
1. <span data-ttu-id="16228-117">ในฟิลด์ **นำการตั้งค่าคอนฟิกมาใช้ใหม่** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="16228-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="16228-118">ถ้าพารามิเตอร์การตั้งค่าคอนฟิกนำกลับมาใช้ใหม่ตั้งค่าเป็น ใช่ ประบบจะเช็คสำหรับการตั้งค่าคอนฟิกที่เหมือนกันหลังจากที่รอบเวลาการตั้งค่าคอนฟิกและนำกลับมาใช้ใหม่ถ้าพบตรงกัน</span><span class="sxs-lookup"><span data-stu-id="16228-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="16228-119">เพิ่มคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="16228-119">Add attributes</span></span>

1. <span data-ttu-id="16228-120">ขยายส่วน **แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="16228-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="16228-121">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="16228-121">Select **Add**.</span></span>
3. <span data-ttu-id="16228-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16228-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="16228-123">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="16228-124">ในฟิลด์ **ชื่อโปรแกรมแก้ปัญหา** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="16228-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="16228-125">ชื่อโปรแกรมแก้ปัญหาถูกใช้โดยโปรแกรมแก้ปัญหาข้อจำกัดของการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="16228-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="16228-126">ต้องไม่รวมถึงช่องว่างหรืออักขระพิเศษยกเว้น (ขีดเส้นใต้)</span><span class="sxs-lookup"><span data-stu-id="16228-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="16228-127">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="16228-128">ข้อความอธิบายจะแสดงถึงผู้ใช้การตั้งค่าคอนฟิกและดั้งนั้นจึงสามารถทำหน้าที่ช่วยเหลือในการเลือกสิทธิ์ค่าแอททริบิวต์ค่าสิทธิ์แอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="16228-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="16228-129">ในฟิลด์ **ชนิดของแอททริบิวต์** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="16228-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="16228-130">ประเภทแอททริบิวต์มิติซึ่งค่าที่พร้อมใช้งานสำหรับแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="16228-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="16228-131">เลือกกล่องกาเครื่องหมาย **รวมไว้ในการนำมาใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="16228-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="16228-132">ตัวเลือกนี้จะพร้อมใช้งานเมื่อตัวเลือกการตั้งค่าคอนฟิกนำมาใช้ใหม่ถูกเลือก </span><span class="sxs-lookup"><span data-stu-id="16228-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="16228-133">รวมแอททริบิวต์ในกล่องการเครื่องหมายนำกลับมาใช้ใหม่หมายควาามว่า แอททริบิวต์นี้จะมีการพิจารณาเมื่อระบบค้นหาตรงกัน</span><span class="sxs-lookup"><span data-stu-id="16228-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="16228-134">เพิ่มส่วนประกอบย่อย</span><span class="sxs-lookup"><span data-stu-id="16228-134">Add subcomponents</span></span>

1. <span data-ttu-id="16228-135">ขยายส่วน **ส่วนประกอบย่อย**</span><span class="sxs-lookup"><span data-stu-id="16228-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="16228-136">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="16228-136">Select **Add**.</span></span>
3. <span data-ttu-id="16228-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16228-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="16228-138">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="16228-139">ในฟิลด์ **ชื่อโปรแกรมแก้ปัญหา** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="16228-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="16228-140">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="16228-141">ในฟิลด์ **ส่วนประกอบ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="16228-142">แต่ละส่วนประกอบย่อยต้องอ้างอิงคำนิยามของส่วนประกอบ </span><span class="sxs-lookup"><span data-stu-id="16228-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="16228-143">การออกแบบนี้สนับสนุนส่วนประกอบที่สามารถนำกลับมาใช้ไม่ได้ และช่วยให้มั่นใจว่าเมื่อมีการกำหนดส่วนประกอบ จะสามารถใช้ในรุ่นผลิตภัณฑ์จำนวนมากได้</span><span class="sxs-lookup"><span data-stu-id="16228-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="16228-144">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="16228-144">Select **Save**.</span></span>
9. <span data-ttu-id="16228-145">เลือก **รายละเอียดรายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="16228-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="16228-146">รายละเอียดรายการ BOM จากผู้ใช้งานที่เปิดใช้งานเพื่อเลือกระบุคุณสมบัติสำหรับแอททริบิวต์ย่อย </span><span class="sxs-lookup"><span data-stu-id="16228-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="16228-147">แต่ละคุณสมบัติสามารถกำหนดค่าหรือแม็ปไปยังแอททริบิวต์ </span><span class="sxs-lookup"><span data-stu-id="16228-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="16228-148">แม็ปไปยังแอททริบิวต์จะส่งผลในรายละเอียดในการรับค่าที่แตกต่างกันขึ้นอยู่กับส่วนของการตั้งค่าคอนฟิกรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="16228-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="16228-149">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="16228-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="16228-150">แต่ละส่วนประกอบย่อยแสดงถึงการตั้งค่าคอนฟิกผลิตภัณฑ์หลักกับเทคโนโลยีการจัดโครงแบบตามข้อจำกัด </span><span class="sxs-lookup"><span data-stu-id="16228-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="16228-151">การอ้างอิงสร้างจากหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="16228-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="16228-152">เลือกกล่องกาเครื่องหมาย **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="16228-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="16228-153">เลือก **ใช่** ในฟิลด์ **การคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="16228-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="16228-154">การตั้งค่าตัวเลือกการคำนวณช่วยให้มั่นใจว่า ผลิตภัณฑ์ที่จะถูกรวมอยู่ในการคำนวณต้นทุนสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="16228-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="16228-155">เลือกแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="16228-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="16228-156">เลือกกล่องกาเครื่องหมาย **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="16228-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="16228-157">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="16228-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="16228-158">ฟิลด์ปริมาณกำหนดจำนวนของผลิตภัณฑ์ที่จะใช้ในการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="16228-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="16228-159">เลือกกล่องกาเครื่องหมาย **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="16228-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="16228-160">ในฟิลด์ **ต่อชุด** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="16228-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="16228-161">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="16228-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]