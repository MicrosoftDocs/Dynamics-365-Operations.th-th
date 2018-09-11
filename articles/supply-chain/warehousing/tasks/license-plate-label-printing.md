--- 
title: "เปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน"
description: "กระบวนงานนี้เปิดใช้งานการพิมพ์ป้ายรหัสรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) โดยอัตโนมัติ หลังจากที่มีการเบิกสินค้าสุดท้ายจากสินค้าคงคลังในกระบวนงานการเบิกสินค้าขาย "
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d562e3a757ed0d8dd0ccc88119cfaadb7d8e1c1f
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="ff574-103">เปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน</span><span class="sxs-lookup"><span data-stu-id="ff574-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff574-104">กระบวนงานนี้เปิดใช้งานการพิมพ์ป้ายรหัสรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) โดยอัตโนมัติ หลังจากที่มีการเบิกสินค้าสุดท้ายจากสินค้าคงคลังในกระบวนงานการเบิกสินค้าขาย </span><span class="sxs-lookup"><span data-stu-id="ff574-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="ff574-105">คุณสามารถรันกระบวนงานนี้ได้ใน บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="ff574-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="ff574-106">ถ้าคุณกำลังดำเนินงานโดยใช้ข้อมูลของคุณเอง คุณต้องมีการตั้งค่าลำดับหมายเลขสำหรับป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="ff574-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="ff574-107">คุณต้องตั้งค่าเครื่องพิมพ์ป้ายชื่อก่อนที่คุณจะเริ่มต้นงานนี้</span><span class="sxs-lookup"><span data-stu-id="ff574-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="ff574-108">ไปที่ การจัดการองค์กร > การตั้งค่า > เครื่องพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="ff574-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="ff574-109">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก และจากนั้นคลิกปุ่มดาวน์โหลดตัวติดตั้งเอเจนต์การกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ff574-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="ff574-110">เรียกใช้ตัวติดตั้ง และตรวจสอบให้แน่ใจว่าคุณมีเครื่องพิมพ์บนเครือข่ายทำงานที่ตั้งค่าเป็น ใช้งานอยู่ ก่อนที่จะดำเนินการกระบวนงานต่อไป</span><span class="sxs-lookup"><span data-stu-id="ff574-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="ff574-111">ตั้งค่าคำนำหน้าบริษัท GS1</span><span class="sxs-lookup"><span data-stu-id="ff574-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="ff574-112">ไปที่การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ff574-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="ff574-113">ในฟิลด์คำนำหน้าบริษัท GS1 ให้ป้อน 7 หมายเลขสำหรับหมายเลขบริษัท GS1 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ff574-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="ff574-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-114">Click Save.</span></span>
4. <span data-ttu-id="ff574-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="ff574-116">ตั้งค่าลำดับหมายเลขป้ายทะเบียน SSCC</span><span class="sxs-lookup"><span data-stu-id="ff574-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="ff574-117">ไปที่จัดการองค์กร > ลำดับหมายเลข > ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ff574-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="ff574-118">ในฟิลด์พื้นที่ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="ff574-119">ในฟิลด์การอ้างอิง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="ff574-120">ในฟิลด์บริษัท ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ff574-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="ff574-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ff574-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ff574-123">ขยายส่วนเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="ff574-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="ff574-124">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ff574-124">Click Edit.</span></span>
9. <span data-ttu-id="ff574-125">ในตารางเซ็กเมนต์ ให้เลือกแถวแรก</span><span class="sxs-lookup"><span data-stu-id="ff574-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="ff574-126">คลิกลบ</span><span class="sxs-lookup"><span data-stu-id="ff574-126">Click Remove.</span></span>
11. <span data-ttu-id="ff574-127">คลิกลบ</span><span class="sxs-lookup"><span data-stu-id="ff574-127">Click Remove.</span></span>
12. <span data-ttu-id="ff574-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-128">Click Save.</span></span>
13. <span data-ttu-id="ff574-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="ff574-130">สร้างโครงร่างการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ff574-130">Create the document route layout</span></span>
1. <span data-ttu-id="ff574-131">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การกำหนดเส้นทางเอกสาร > โครงร่างการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ff574-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="ff574-132">เปิดใช้งานโครงร่าง SSCC</span><span class="sxs-lookup"><span data-stu-id="ff574-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="ff574-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff574-133">Click New.</span></span>
3. <span data-ttu-id="ff574-134">ในฟิลด์รหัสโครงร่าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff574-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="ff574-135">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ff574-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ff574-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ff574-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ff574-137">คลิกแทรกที่ส่วนท้ายของข้อความ</span><span class="sxs-lookup"><span data-stu-id="ff574-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="ff574-138">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-138">Click Save.</span></span>
8. <span data-ttu-id="ff574-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="ff574-140">ตั้งค่าการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ff574-140">Set up the document routing</span></span>
1. <span data-ttu-id="ff574-141">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การกำหนดเส้นทางเอกสาร > การกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ff574-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="ff574-142">ในฟิลด์ชนิดใบสั่งงาน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="ff574-143">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff574-143">Click New.</span></span>
4. <span data-ttu-id="ff574-144">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ff574-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="ff574-145">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="ff574-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="ff574-146">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff574-146">Click New.</span></span>
7. <span data-ttu-id="ff574-147">ในฟิลด์รหัสโครงร่าง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ff574-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="ff574-148">ในฟิลด์ชื่อ ให้ป้อนชื่อเครื่องพิมพ์ที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="ff574-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="ff574-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-149">Click Save.</span></span>
10. <span data-ttu-id="ff574-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="ff574-151">สร้างเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="ff574-151">Create mobile device menu</span></span>
1. <span data-ttu-id="ff574-152">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="ff574-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="ff574-153">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff574-153">Click New.</span></span>
3. <span data-ttu-id="ff574-154">ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ff574-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="ff574-155">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff574-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="ff574-156">ในฟิลด์โหมด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="ff574-157">เลือก ใช่ ในฟิลด์การใช้ค่าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ff574-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="ff574-158">เลือก ใช่ ในฟิลด์การสร้างป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="ff574-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="ff574-159">ขยายส่วนคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="ff574-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="ff574-160">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff574-160">Click New.</span></span>
10. <span data-ttu-id="ff574-161">ในฟิลด์รหัสคลาสงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff574-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="ff574-162">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-162">Click Save.</span></span>
12. <span data-ttu-id="ff574-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-163">Close the page.</span></span>
13. <span data-ttu-id="ff574-164">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="ff574-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="ff574-165">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ff574-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ff574-166">ในแผนภูมิ ให้เลือก 'ในแผนภูมิ ให้เลือกรายการเมนูที่ได้คุณสร้างขึ้นก่อนหน้า'</span><span class="sxs-lookup"><span data-stu-id="ff574-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="ff574-167">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="ff574-167">Click Edit.</span></span>
17. <span data-ttu-id="ff574-168">คลิกที่ลูกศรเพื่อเพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="ff574-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="ff574-169">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-169">Click Save.</span></span>
19. <span data-ttu-id="ff574-170">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="ff574-171">อัพเดตเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="ff574-171">Update a work template</span></span>
1. <span data-ttu-id="ff574-172">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="ff574-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="ff574-173">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ff574-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ff574-174">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ff574-174">Click Edit.</span></span>
4. <span data-ttu-id="ff574-175">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff574-175">Click New.</span></span>
5. <span data-ttu-id="ff574-176">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ff574-177">ในฟิลด์ประเภทงาน ให้เลือก 'พิมพ์'</span><span class="sxs-lookup"><span data-stu-id="ff574-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="ff574-178">ในฟิลด์รหัสคลาสงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff574-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="ff574-179">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff574-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ff574-180">คลิกเลื่อนขึ้น</span><span class="sxs-lookup"><span data-stu-id="ff574-180">Click Move up.</span></span>
10. <span data-ttu-id="ff574-181">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ff574-181">Click Save.</span></span>
11. <span data-ttu-id="ff574-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff574-182">Close the page.</span></span>


