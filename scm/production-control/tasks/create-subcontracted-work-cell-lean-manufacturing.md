--- 
title: "สร้างเซลล์ทำงานที่รับเหมารายย่อยสำหรับ lean manufacturing"
description: "เมื่อต้องการสร้างแบบจำลองงานที่รับเหมารายย่อยสำหรับ Lean Manufacturing คุณต้องสร้างเซลล์ทำงานที่เกี่ยวข้องกับผู้จัดจำหน่ายที่มีการทำงาน"
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fc8dc0bc29c6bdb662c46808491abf5395f0be5d
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="875a8-103">สร้างเซลล์ทำงานที่รับเหมารายย่อยสำหรับ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="875a8-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="875a8-104">เมื่อต้องการสร้างแบบจำลองงานที่รับเหมารายย่อยสำหรับ Lean Manufacturing คุณต้องสร้างเซลล์ทำงานที่เกี่ยวข้องกับผู้จัดจำหน่ายที่มีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="875a8-105">เซลล์ทำงานที่รับเหมารายย่อยจะเชื่อมโยงกับผู้จัดจำหน่ายโดยใช้การเชื่อมโยงของทรัพยากรของชนิดผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="875a8-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="875a8-106">ถ้าคุณเล่นการบันทึกนี้ในบริษัทสาธิต USMF คุณสามารถเลือกรหัสบัญชีผู้จัดจำหน่าย 1002 และไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="875a8-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="875a8-107">สร้างทรัพยากรผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="875a8-107">Create a vendor resource</span></span>
1. <span data-ttu-id="875a8-108">ไปที่ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="875a8-108">Go to Resources.</span></span>
2. <span data-ttu-id="875a8-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="875a8-109">Click New.</span></span>
3. <span data-ttu-id="875a8-110">ในฟิลด์ทรัพยากร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="875a8-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="875a8-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="875a8-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="875a8-112">ในฟิลด์ชนิด ให้เลือก 'ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="875a8-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="875a8-113">ในฟิลด์ผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="875a8-114">สร้างกลุ่มทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="875a8-114">Create the resource group</span></span>
1. <span data-ttu-id="875a8-115">ไปที่กลุ่มทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="875a8-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="875a8-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="875a8-116">Click New.</span></span>
3. <span data-ttu-id="875a8-117">ในฟิลด์กลุ่มทรัพยากร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="875a8-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="875a8-118">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="875a8-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="875a8-119">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="875a8-120">เลือกไซต์ที่ควรปันส่วนกับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="875a8-121">ในทฤษฎี ไซต์อาจแสดงถึงไซต์เดียวที่ได้รับการดำเนินการโดยผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="875a8-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="875a8-122">อย่างไรก็ตาม ในกรณีส่วนใหญ่ ทรัพยากรที่รับเหมารายย่อยจะถูกปันส่วนไปยังไซต์ที่สั่งงานรับเหมารายย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="875a8-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="875a8-123">โปรดทราบว่าคลังสินค้าอินพุทและเอาท์พุทของเซลล์ทำงานที่รับเหมารายย่อยต้องอยู่ในไซต์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="875a8-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="875a8-124">ในฟิลด์ไซต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="875a8-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="875a8-125">เลือกหรือยกเลิกกล่องกาเครื่องหมายเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="875a8-126">ในฟิลด์คลังสินค้าอินพุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="875a8-127">เลือกคลังสินค้าและสถานที่ที่ใช้ระยะวัสดุสำหรับเซลล์ทำงานที่มีจัดการผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="875a8-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="875a8-128">ในหลายกรณี คลังสินค้าและสถานที่เก็บจะถูกสร้างแบบจำลองโดยใช้คลังสินค้าที่แยกต่างหากสำหรับแต่ละผู้จัดจำหน่ายและสถานที่เก็บหนึ่งสำหรับแต่ละเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="875a8-129">ในฟิลด์ที่ตั้งอินพุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="875a8-130">ในฟิลด์คลังสินค้าเอาท์พุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="875a8-131">กำหนดคลังสินค้าและสถานที่เก็บที่ลงรายการบัญชีวัสดุเมื่อมีการลงรายการบัญชีกิจกรรมที่รับเหมารายย่อยของเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="875a8-132">คลังสินค้าและสถานที่เก็บสามารถเป็นที่ไซต์ของผู้จัดจำหน่ายหากผู้จัดจำหน่ายรายงานงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="875a8-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="875a8-133">หรือคลังสินค้าและสถานที่เก็บสามารถเป็นสถานที่รับสินค้าที่เกี่ยวข้องกับขั้นตอนถัดไปของขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="875a8-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="875a8-134">ในฟิลด์ที่ตั้งเอาท์พุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="875a8-135">ขยายหรือยุบส่วนปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="875a8-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="875a8-136">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="875a8-136">Click Add.</span></span>
15. <span data-ttu-id="875a8-137">ในฟิลด์ปฏิทิน คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="875a8-138">เชื่อมโยงปฏิทินเวลาการทำงานของเซลล์ทำงานที่มีกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="875a8-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="875a8-139">สำหรับทรัพยากรที่วิกฤติ เราขอแนะนำว่าคุณควรกำหนดปฏิทินเฉพาะที่แสดงถึงเวลาการทำงานที่แน่นอนและกำลังการผลิตที่เกี่ยวข้องของไซต์ของผู้จัดจำหน่ายหรือเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="875a8-140">ขยายหรือยุบส่วนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="875a8-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="875a8-141">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="875a8-141">Click Add.</span></span>
    * <span data-ttu-id="875a8-142">กลุ่มทรัพยากรที่รับเหมารายย่อยต้องมีทรัพยากรที่เชื่อมโยงกันของชนิดผู้จัดจำหน่ายที่เชื่อมโยงกับกลุ่มทรัพยากรกับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="875a8-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="875a8-143">ในฟิลด์ทรัพยากร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="875a8-144">เลือกหรือป้อนทรัพยากรของผู้จัดจำหน่ายที่คุณเพิ่งสร้างในงานย่อยก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="875a8-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="875a8-145">ขยายหรือยุบส่วนของกำลังการผลิตของเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="875a8-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="875a8-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="875a8-146">Click Add.</span></span>
    * <span data-ttu-id="875a8-147">เซลล์ทำงานต้องมีกำลังการผลิตที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="875a8-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="875a8-148">ในตัวอย่างนี้ เราจะสร้างกำลังการผลิตปริมาณที่สามารถประมวลผลได้ 100 ชิ้นต่อวันทำงานมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="875a8-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="875a8-149">ในฟิลด์แบบจำลองขั้นตอนการผลิต ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="875a8-150">ในฟิลด์รอบระยะเวลากำลังการผลิต ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="875a8-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="875a8-151">ในฟิลด์ปริมาณของปริมาณที่สามารถประมวลผลได้เฉลี่ย ให้ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="875a8-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="875a8-152">ในฟิลด์หน่วย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="875a8-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="875a8-153">แก้ไขการเปลี่ยนแปลงของหน่วย</span><span class="sxs-lookup"><span data-stu-id="875a8-153">ResolveChanges the Unit.</span></span>


