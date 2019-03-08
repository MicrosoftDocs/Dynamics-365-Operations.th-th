---
title: สร้างสูตรการผลิตสำหรับผลิตภัณฑ์หลักตามมิติ
description: 'สำหรับกระบวนงานนี้ คุณควรดำเนินงานคู่มือ 4 รายการก่อนหน้าให้เสร็จสมบูรณ์แล้วในลำดับของการบันทึกแปดรายการ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19578f78c11bf0537708e8d516d478f00b13fa95
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "349756"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="33b5d-103">สร้างสูตรการผลิตสำหรับผลิตภัณฑ์หลักตามมิติ</span><span class="sxs-lookup"><span data-stu-id="33b5d-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33b5d-104">สำหรับกระบวนงานนี้ คุณควรดำเนินงานคู่มือ 4 รายการก่อนหน้าให้เสร็จสมบูรณ์แล้วในลำดับของการบันทึกแปดรายการ </span><span class="sxs-lookup"><span data-stu-id="33b5d-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="33b5d-105">การบันทึก 4 รายการแรกจะตั้งค่าข้อมูลที่ต้องการเพื่อดำเนินกระบวนงานนี้ให้สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="33b5d-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="33b5d-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="33b5d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="33b5d-107">โดยทั่วไปงานนี้จะถูกจัดการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="33b5d-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="33b5d-108">เลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="33b5d-108">Select the product</span></span>
1. <span data-ttu-id="33b5d-109">คลิก การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="33b5d-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="33b5d-110">คลิกผลิตภัณฑ์ต่างๆที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="33b5d-110">Click Released products.</span></span>
3. <span data-ttu-id="33b5d-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="33b5d-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="33b5d-112">หาผลิตภัณฑ์หลักที่ได้นำออกใช้ ซึ่งมีเทคโนโลยีการจัดโครงแบบตามมิติ ที่คุณสร้างขึ้นในคู่มืองานแรกในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="33b5d-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="33b5d-113">ในบานหน้าต่างการดำเนินการ คลิกวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="33b5d-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="33b5d-114">คลิกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="33b5d-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="33b5d-115">สร้าง BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="33b5d-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="33b5d-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="33b5d-116">Click New.</span></span>
2. <span data-ttu-id="33b5d-117">คลิก BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="33b5d-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="33b5d-118">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="33b5d-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="33b5d-119">การตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="33b5d-119">Setting a site</span></span>  
    * <span data-ttu-id="33b5d-120">ในกระบวนงานนี้ เราไม่ตั้งค่าไซต์เฉพาะสำหรับ BOM</span><span class="sxs-lookup"><span data-stu-id="33b5d-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="33b5d-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="33b5d-121">Click OK.</span></span>
5. <span data-ttu-id="33b5d-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="33b5d-122">Click New.</span></span>
    * <span data-ttu-id="33b5d-123">ในกระบวนงานนี้ เราจะเพิ่มรายการสี่รายการไปยัง BOM </span><span class="sxs-lookup"><span data-stu-id="33b5d-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="33b5d-124">สองรายการจะแสดงตัวเลือกเคเบิล และอีกสองรายการจะแสดงตัวเลือก cabinet</span><span class="sxs-lookup"><span data-stu-id="33b5d-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="33b5d-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="33b5d-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="33b5d-126">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="33b5d-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-127">เลือกหมายเลขสินค้า เคเบิล A0001 HDMI 6'</span><span class="sxs-lookup"><span data-stu-id="33b5d-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="33b5d-128">ในฟิลด์กลุ่มการตั้งค่าคอนฟิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="33b5d-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-129">เลือกกลุ่มการตั้งค่าคอนฟิกเคเบิลที่สร้างไว้ในคู่มือ 4 ในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="33b5d-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="33b5d-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="33b5d-130">Click New.</span></span>
    * <span data-ttu-id="33b5d-131">เลือกหมายเลขสินค้า เคเบิล A0002 HDMI 12'</span><span class="sxs-lookup"><span data-stu-id="33b5d-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="33b5d-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="33b5d-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="33b5d-133">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="33b5d-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="33b5d-134">ในฟิลด์กลุ่มการตั้งค่าคอนฟิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="33b5d-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-135">เลือกกลุ่มการตั้งค่าคอนฟิกเคเบิลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="33b5d-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="33b5d-136">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="33b5d-136">Click New.</span></span>
14. <span data-ttu-id="33b5d-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="33b5d-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="33b5d-138">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="33b5d-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-139">เลือกหมายเลขสินค้า Cabinet D0002</span><span class="sxs-lookup"><span data-stu-id="33b5d-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="33b5d-140">ในฟิลด์กลุ่มการตั้งค่าคอนฟิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="33b5d-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-141">เลือกกลุ่มการตั้งค่าคอนฟิก Cabinet สำหรับรายการ BOM นี้</span><span class="sxs-lookup"><span data-stu-id="33b5d-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="33b5d-142">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="33b5d-142">Click New.</span></span>
18. <span data-ttu-id="33b5d-143">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="33b5d-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="33b5d-144">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="33b5d-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-145">เลือกหมายเลขสินค้า StandardCabinet M0007 ให้เป็นรายการ BOM สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="33b5d-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="33b5d-146">ในฟิลด์กลุ่มการตั้งค่าคอนฟิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="33b5d-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="33b5d-147">เลือกกลุ่มการตั้งค่าคอนฟิก Cabinet สำหรับรายการ BOM สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="33b5d-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="33b5d-148">อนุมัติและเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="33b5d-148">Approve and activate</span></span>
1. <span data-ttu-id="33b5d-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="33b5d-149">Close the page.</span></span>
2. <span data-ttu-id="33b5d-150">คลิกอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="33b5d-150">Click Approve.</span></span>
3. <span data-ttu-id="33b5d-151">ในฟิลด์อนุมัติโดย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="33b5d-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="33b5d-152">เลือก ใช่ ในฟิลด์คุณยังต้องการอนุมัติสูตรการผลิตอีกด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="33b5d-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="33b5d-153">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="33b5d-153">Click OK.</span></span>
6. <span data-ttu-id="33b5d-154">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="33b5d-154">Click Activate.</span></span>

