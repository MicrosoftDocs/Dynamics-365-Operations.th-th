---
title: สร้างเซลล์ทำงานที่รับเหมารายย่อยสำหรับ lean manufacturing
description: เมื่อต้องการสร้างแบบจำลองงานที่รับเหมารายย่อยสำหรับ Lean Manufacturing คุณต้องสร้างเซลล์ทำงานที่เกี่ยวข้องกับผู้จัดจำหน่ายที่มีการทำงาน
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e07dde702e3e247ac9312d05724ea307f431937
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210835"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="a2443-103">สร้างเซลล์ทำงานที่รับเหมารายย่อยสำหรับ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="a2443-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2443-104">เมื่อต้องการสร้างแบบจำลองงานที่รับเหมารายย่อยสำหรับ Lean Manufacturing คุณต้องสร้างเซลล์ทำงานที่เกี่ยวข้องกับผู้จัดจำหน่ายที่มีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="a2443-105">เซลล์ทำงานที่รับเหมารายย่อยจะเชื่อมโยงกับผู้จัดจำหน่ายโดยใช้การเชื่อมโยงของทรัพยากรของชนิดผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a2443-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="a2443-106">ถ้าคุณเล่นการบันทึกนี้ในบริษัทสาธิต USMF คุณสามารถเลือกรหัสบัญชีผู้จัดจำหน่าย 1002 และไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="a2443-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="a2443-107">สร้างทรัพยากรผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a2443-107">Create a vendor resource</span></span>
1. <span data-ttu-id="a2443-108">ไปที่ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="a2443-108">Go to Resources.</span></span>
2. <span data-ttu-id="a2443-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a2443-109">Click New.</span></span>
3. <span data-ttu-id="a2443-110">ในฟิลด์ทรัพยากร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a2443-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="a2443-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2443-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a2443-112">ในฟิลด์ชนิด ให้เลือก 'ผู้จัดจำหน่าย'</span><span class="sxs-lookup"><span data-stu-id="a2443-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="a2443-113">ในฟิลด์ผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="a2443-114">สร้างกลุ่มทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="a2443-114">Create the resource group</span></span>
1. <span data-ttu-id="a2443-115">ไปที่กลุ่มทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="a2443-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="a2443-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a2443-116">Click New.</span></span>
3. <span data-ttu-id="a2443-117">ในฟิลด์กลุ่มทรัพยากร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2443-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="a2443-118">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2443-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a2443-119">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a2443-120">เลือกไซต์ที่ควรปันส่วนกับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="a2443-121">ในทฤษฎี ไซต์อาจแสดงถึงไซต์เดียวที่ได้รับการดำเนินการโดยผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a2443-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="a2443-122">อย่างไรก็ตาม ในกรณีส่วนใหญ่ ทรัพยากรที่รับเหมารายย่อยจะถูกปันส่วนไปยังไซต์ที่สั่งงานรับเหมารายย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a2443-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="a2443-123">โปรดทราบว่าคลังสินค้าอินพุทและเอาท์พุทของเซลล์ทำงานที่รับเหมารายย่อยต้องอยู่ในไซต์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a2443-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="a2443-124">ในฟิลด์ไซต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a2443-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="a2443-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="a2443-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="a2443-126">เลือกหรือยกเลิกกล่องกาเครื่องหมายเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="a2443-127">ในฟิลด์คลังสินค้าอินพุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a2443-128">เลือกคลังสินค้าและสถานที่ที่ใช้ระยะวัสดุสำหรับเซลล์ทำงานที่มีจัดการผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a2443-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="a2443-129">ในหลายกรณี คลังสินค้าและสถานที่เก็บจะถูกสร้างแบบจำลองโดยใช้คลังสินค้าที่แยกต่างหากสำหรับแต่ละผู้จัดจำหน่ายและสถานที่เก็บหนึ่งสำหรับแต่ละเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="a2443-130">ในฟิลด์ที่ตั้งอินพุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a2443-131">ในฟิลด์คลังสินค้าเอาท์พุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a2443-132">กำหนดคลังสินค้าและสถานที่เก็บที่ลงรายการบัญชีวัสดุเมื่อมีการลงรายการบัญชีกิจกรรมที่รับเหมารายย่อยของเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="a2443-133">คลังสินค้าและสถานที่เก็บสามารถเป็นที่ไซต์ของผู้จัดจำหน่ายหากผู้จัดจำหน่ายรายงานงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="a2443-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="a2443-134">หรือคลังสินค้าและสถานที่เก็บสามารถเป็นสถานที่รับสินค้าที่เกี่ยวข้องกับขั้นตอนถัดไปของขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="a2443-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="a2443-135">ในฟิลด์ที่ตั้งเอาท์พุท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a2443-136">ขยายหรือยุบส่วนปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="a2443-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="a2443-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a2443-137">Click Add.</span></span>
15. <span data-ttu-id="a2443-138">ในฟิลด์ปฏิทิน คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a2443-139">เชื่อมโยงปฏิทินเวลาการทำงานของเซลล์ทำงานที่มีกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="a2443-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="a2443-140">สำหรับทรัพยากรที่วิกฤติ เราขอแนะนำว่าคุณควรกำหนดปฏิทินเฉพาะที่แสดงถึงเวลาการทำงานที่แน่นอนและกำลังการผลิตที่เกี่ยวข้องของไซต์ของผู้จัดจำหน่ายหรือเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="a2443-141">ขยายหรือยุบส่วนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="a2443-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="a2443-142">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a2443-142">Click Add.</span></span>
    * <span data-ttu-id="a2443-143">กลุ่มทรัพยากรที่รับเหมารายย่อยต้องมีทรัพยากรที่เชื่อมโยงกันของชนิดผู้จัดจำหน่ายที่เชื่อมโยงกับกลุ่มทรัพยากรกับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a2443-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="a2443-144">ในฟิลด์ทรัพยากร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a2443-145">เลือกหรือป้อนทรัพยากรของผู้จัดจำหน่ายที่คุณเพิ่งสร้างในงานย่อยก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a2443-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="a2443-146">ขยายหรือยุบส่วนของกำลังการผลิตของเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a2443-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="a2443-147">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a2443-147">Click Add.</span></span>
    * <span data-ttu-id="a2443-148">เซลล์ทำงานต้องมีกำลังการผลิตที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="a2443-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="a2443-149">ในตัวอย่างนี้ เราจะสร้างกำลังการผลิตปริมาณที่สามารถประมวลผลได้ 100 ชิ้นต่อวันทำงานมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="a2443-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="a2443-150">ในฟิลด์แบบจำลองขั้นตอนการผลิต ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="a2443-151">ในฟิลด์รอบระยะเวลากำลังการผลิต ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a2443-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="a2443-152">ในฟิลด์ปริมาณของปริมาณที่สามารถประมวลผลได้เฉลี่ย ให้ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="a2443-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="a2443-153">ในฟิลด์หน่วย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a2443-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="a2443-154">แก้ไขการเปลี่ยนแปลงของหน่วย</span><span class="sxs-lookup"><span data-stu-id="a2443-154">ResolveChanges the Unit.</span></span>

