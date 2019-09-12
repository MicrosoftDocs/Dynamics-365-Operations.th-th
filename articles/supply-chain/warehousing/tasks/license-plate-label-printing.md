---
title: เปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน
description: หัวข้อนี้แสดงวิธีการเปิดใช้งานการพิมพ์ป้ายรหัสรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) โดยอัตโนมัติ หลังจากที่มีการเบิกสินค้าสุดท้ายจากสินค้าคงคลังในกระบวนงานการเบิกสินค้าขาย
author: perlynne
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed4fa28039c9320998f6524c9c9edb0a0301b7b0
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866837"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="89909-103">เปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน</span><span class="sxs-lookup"><span data-stu-id="89909-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89909-104">หัวข้อนี้แสดงวิธีการเปิดใช้งานการพิมพ์ป้ายรหัสรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) โดยอัตโนมัติ หลังจากที่มีการเบิกสินค้าสุดท้ายจากสินค้าคงคลังในกระบวนงานการเบิกสินค้าขาย</span><span class="sxs-lookup"><span data-stu-id="89909-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="89909-105">คุณสามารถรันกระบวนงานนี้ได้ใน บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="89909-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="89909-106">ถ้าคุณกำลังดำเนินงานโดยใช้ข้อมูลของคุณเอง คุณต้องมีการตั้งค่าลำดับหมายเลขสำหรับป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="89909-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="89909-107">คุณต้องตั้งค่าเครื่องพิมพ์ป้ายชื่อก่อนที่คุณจะเริ่มต้นงานนี้</span><span class="sxs-lookup"><span data-stu-id="89909-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="89909-108">ไปที่ การจัดการองค์กร > การตั้งค่า > เครื่องพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="89909-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="89909-109">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก และจากนั้นคลิกปุ่มดาวน์โหลดตัวติดตั้งเอเจนต์การกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="89909-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="89909-110">เรียกใช้ตัวติดตั้ง และตรวจสอบให้แน่ใจว่าคุณมีเครื่องพิมพ์บนเครือข่ายทำงานที่ตั้งค่าเป็น ใช้งานอยู่ ก่อนที่จะดำเนินการกระบวนงานต่อไป</span><span class="sxs-lookup"><span data-stu-id="89909-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="89909-111">ตั้งค่าคำนำหน้าบริษัท GS1</span><span class="sxs-lookup"><span data-stu-id="89909-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="89909-112">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="89909-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="89909-113">ในฟิลด์ **คำนำหน้าบริษัท GS1** ให้ป้อน 7 หมายเลขสำหรับหมายเลขบริษัท GS1 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="89909-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="89909-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-114">Select **Save**.</span></span>
4. <span data-ttu-id="89909-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="89909-116">ตั้งค่าลำดับหมายเลขป้ายทะเบียน SSCC</span><span class="sxs-lookup"><span data-stu-id="89909-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="89909-117">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการองค์กร > ลำดับหมายเลข > ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="89909-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="89909-118">ในฟิลด์ **พื้นที่** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89909-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="89909-119">ในฟิลด์ **การอ้างอิง** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89909-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="89909-120">ในฟิลด์ **บริษัท** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="89909-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="89909-121">ขยายส่วน **เซ็กเมนต์**</span><span class="sxs-lookup"><span data-stu-id="89909-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="89909-122">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="89909-122">Select **Edit**.</span></span>
7. <span data-ttu-id="89909-123">ในตาราง **เซ็กเมนต์** ให้เลือกแถวแรก</span><span class="sxs-lookup"><span data-stu-id="89909-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="89909-124">เลือก **ลบออก**</span><span class="sxs-lookup"><span data-stu-id="89909-124">Select **Remove**.</span></span>
9. <span data-ttu-id="89909-125">เลือก **ลบออก**</span><span class="sxs-lookup"><span data-stu-id="89909-125">Select **Remove**.</span></span>
10. <span data-ttu-id="89909-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-126">Select **Save**.</span></span>
11. <span data-ttu-id="89909-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="89909-128">สร้างโครงร่างการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="89909-128">Create the document route layout</span></span>
1. <span data-ttu-id="89909-129">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > การกำหนดเส้นทางเอกสาร > โครงร่างการกำหนดเส้นทางเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="89909-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="89909-130">เปิดใช้งานโครงร่าง SSCC</span><span class="sxs-lookup"><span data-stu-id="89909-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="89909-131">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89909-131">Select **New**.</span></span>
3. <span data-ttu-id="89909-132">ในฟิลด์ **รหัสโครงร่าง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89909-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="89909-133">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89909-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="89909-134">เลือก **แทรกที่ส่วนท้ายของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="89909-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="89909-135">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-135">Select **Save**.</span></span>
7. <span data-ttu-id="89909-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="89909-137">ตั้งค่าการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="89909-137">Set up the document routing</span></span>
1. <span data-ttu-id="89909-138">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > การกำหนดเส้นทางเอกสาร > การกำหนดเส้นทางเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="89909-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="89909-139">ในฟิลด์ **ชนิดใบสั่งงาน** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89909-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="89909-140">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89909-140">Select **New**.</span></span>
4. <span data-ttu-id="89909-141">ในฟิลด์ **คลังสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="89909-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="89909-142">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89909-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="89909-143">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89909-143">Select **New**.</span></span>
7. <span data-ttu-id="89909-144">ในฟิลด์ **รหัสโครงร่าง** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="89909-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="89909-145">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเครื่องพิมพ์ที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="89909-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="89909-146">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-146">Select **Save**.</span></span>
10. <span data-ttu-id="89909-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="89909-148">สร้างเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="89909-148">Create mobile device menu</span></span>
1. <span data-ttu-id="89909-149">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="89909-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="89909-150">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89909-150">Select **New**.</span></span>
3. <span data-ttu-id="89909-151">ในฟิลด์ **ชื่อรายการในเมนู** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="89909-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="89909-152">ในฟิลด์ **หัวข้อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89909-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="89909-153">ในฟิลด์ **โหมด** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="89909-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="89909-154">เลือก **ใช่** ในฟิลด์ **ใช้งานที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="89909-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="89909-155">เลือก **ใช่** ในฟิลด์ **สร้างป้ายทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="89909-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="89909-156">ขยายส่วน **คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="89909-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="89909-157">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89909-157">Select **New**.</span></span>
10. <span data-ttu-id="89909-158">ในฟิลด์ **รหัสคลาสงาน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89909-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="89909-159">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-159">Select **Save**.</span></span>
12. <span data-ttu-id="89909-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-160">Close the page.</span></span>
13. <span data-ttu-id="89909-161">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="89909-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="89909-162">ในแผนภูมิ เลือกรายการเมนูที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="89909-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="89909-163">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="89909-163">Select **Edit**.</span></span>
16. <span data-ttu-id="89909-164">เลือกลูกศรเพื่อเพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="89909-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="89909-165">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-165">Select **Save**.</span></span>
18. <span data-ttu-id="89909-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="89909-167">อัพเดตเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="89909-167">Update a work template</span></span>
1. <span data-ttu-id="89909-168">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="89909-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="89909-169">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="89909-169">Select **Edit**.</span></span>
3. <span data-ttu-id="89909-170">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89909-170">Select **New**.</span></span>
4. <span data-ttu-id="89909-171">ในฟิลด์ **ประเภทงาน** ให้เลือก **พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="89909-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="89909-172">ในฟิลด์ **รหัสคลาสงาน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="89909-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="89909-173">เลือก **เลื่อนขึ้น**</span><span class="sxs-lookup"><span data-stu-id="89909-173">Select **Move up**.</span></span>
7. <span data-ttu-id="89909-174">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="89909-174">Select **Save**.</span></span>
8. <span data-ttu-id="89909-175">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89909-175">Close the page.</span></span>

