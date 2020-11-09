---
title: เปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน
description: หัวข้อนี้แสดงวิธีการเปิดใช้งานการพิมพ์ป้ายรหัสรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) โดยอัตโนมัติ หลังจากที่มีการเบิกสินค้าสุดท้ายจากสินค้าคงคลังในกระบวนงานการเบิกสินค้าขาย
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e548e5e5528733412d47478dd740b87217cdac2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016113"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="1ce57-103">เปิดใช้งานการพิมพ์ป้ายชื่อทะเบียน</span><span class="sxs-lookup"><span data-stu-id="1ce57-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ce57-104">หัวข้อนี้แสดงวิธีการเปิดใช้งานการพิมพ์ป้ายรหัสรหัสคอนเทนเนอร์ประจำสินค้า (SSCC) โดยอัตโนมัติ หลังจากที่มีการเบิกสินค้าสุดท้ายจากสินค้าคงคลังในกระบวนงานการเบิกสินค้าขาย</span><span class="sxs-lookup"><span data-stu-id="1ce57-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="1ce57-105">คุณสามารถรันกระบวนงานนี้ได้ใน บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="1ce57-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="1ce57-106">ถ้าคุณกำลังดำเนินงานโดยใช้ข้อมูลของคุณเอง คุณต้องมีการตั้งค่าลำดับหมายเลขสำหรับป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="1ce57-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="1ce57-107">คุณต้องตั้งค่าเครื่องพิมพ์ป้ายชื่อก่อนที่คุณจะเริ่มต้นงานนี้</span><span class="sxs-lookup"><span data-stu-id="1ce57-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="1ce57-108">ไปที่ การจัดการองค์กร > การตั้งค่า > เครื่องพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="1ce57-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="1ce57-109">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก และจากนั้นคลิกปุ่มดาวน์โหลดตัวติดตั้งเอเจนต์การกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="1ce57-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="1ce57-110">เรียกใช้ตัวติดตั้ง และตรวจสอบให้แน่ใจว่าคุณมีเครื่องพิมพ์บนเครือข่ายทำงานที่ตั้งค่าเป็น ใช้งานอยู่ ก่อนที่จะดำเนินการกระบวนงานต่อไป</span><span class="sxs-lookup"><span data-stu-id="1ce57-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="1ce57-111">ตั้งค่าคำนำหน้าบริษัท GS1</span><span class="sxs-lookup"><span data-stu-id="1ce57-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="1ce57-112">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="1ce57-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="1ce57-113">ในฟิลด์ **คำนำหน้าบริษัท GS1** ให้ป้อน 7 หมายเลขสำหรับหมายเลขบริษัท GS1 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1ce57-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="1ce57-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-114">Select **Save**.</span></span>
4. <span data-ttu-id="1ce57-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="1ce57-116">ตั้งค่าลำดับหมายเลขป้ายทะเบียน SSCC</span><span class="sxs-lookup"><span data-stu-id="1ce57-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="1ce57-117">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการองค์กร > ลำดับหมายเลข > ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="1ce57-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="1ce57-118">ในฟิลด์ **พื้นที่** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1ce57-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="1ce57-119">ในฟิลด์ **การอ้างอิง** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1ce57-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="1ce57-120">ในฟิลด์ **บริษัท** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1ce57-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="1ce57-121">ขยายส่วน **เซ็กเมนต์**</span><span class="sxs-lookup"><span data-stu-id="1ce57-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="1ce57-122">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1ce57-122">Select **Edit**.</span></span>
7. <span data-ttu-id="1ce57-123">ในตาราง **เซ็กเมนต์** ให้เลือกแถวแรก</span><span class="sxs-lookup"><span data-stu-id="1ce57-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="1ce57-124">เลือก **ลบออก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-124">Select **Remove**.</span></span>
9. <span data-ttu-id="1ce57-125">เลือก **ลบออก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-125">Select **Remove**.</span></span>
10. <span data-ttu-id="1ce57-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-126">Select **Save**.</span></span>
11. <span data-ttu-id="1ce57-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="1ce57-128">สร้างโครงร่างการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="1ce57-128">Create the document route layout</span></span>
1. <span data-ttu-id="1ce57-129">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > การกำหนดเส้นทางเอกสาร > โครงร่างการกำหนดเส้นทางเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="1ce57-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="1ce57-130">เปิดใช้งานโครงร่าง SSCC</span><span class="sxs-lookup"><span data-stu-id="1ce57-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="1ce57-131">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-131">Select **New**.</span></span>
3. <span data-ttu-id="1ce57-132">ในฟิลด์ **รหัสโครงร่าง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ce57-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="1ce57-133">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ce57-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1ce57-134">เลือก **แทรกที่ส่วนท้ายของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="1ce57-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="1ce57-135">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-135">Select **Save**.</span></span>
7. <span data-ttu-id="1ce57-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="1ce57-137">ตั้งค่าการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="1ce57-137">Set up the document routing</span></span>
1. <span data-ttu-id="1ce57-138">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > การกำหนดเส้นทางเอกสาร > การกำหนดเส้นทางเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="1ce57-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="1ce57-139">ในฟิลด์ **ชนิดใบสั่งงาน** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1ce57-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="1ce57-140">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-140">Select **New**.</span></span>
4. <span data-ttu-id="1ce57-141">ในฟิลด์ **คลังสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1ce57-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="1ce57-142">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ce57-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="1ce57-143">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-143">Select **New**.</span></span>
7. <span data-ttu-id="1ce57-144">ในฟิลด์ **รหัสโครงร่าง** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1ce57-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="1ce57-145">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเครื่องพิมพ์ที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="1ce57-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="1ce57-146">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-146">Select **Save**.</span></span>
10. <span data-ttu-id="1ce57-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="1ce57-148">สร้างเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1ce57-148">Create mobile device menu</span></span>
1. <span data-ttu-id="1ce57-149">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="1ce57-150">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-150">Select **New**.</span></span>
3. <span data-ttu-id="1ce57-151">ในฟิลด์ **ชื่อรายการในเมนู** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1ce57-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="1ce57-152">ในฟิลด์ **หัวข้อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ce57-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="1ce57-153">ในฟิลด์ **โหมด** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1ce57-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="1ce57-154">เลือก **ใช่** ในฟิลด์ **ใช้งานที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="1ce57-155">เลือก **ใช่** ในฟิลด์ **สร้างป้ายทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="1ce57-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="1ce57-156">ขยายส่วน **คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="1ce57-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="1ce57-157">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-157">Select **New**.</span></span>
10. <span data-ttu-id="1ce57-158">ในฟิลด์ **รหัสคลาสงาน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ce57-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="1ce57-159">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-159">Select **Save**.</span></span>
12. <span data-ttu-id="1ce57-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-160">Close the page.</span></span>
13. <span data-ttu-id="1ce57-161">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > เมนูของอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="1ce57-162">ในแผนภูมิ เลือกรายการเมนูที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="1ce57-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="1ce57-163">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1ce57-163">Select **Edit**.</span></span>
16. <span data-ttu-id="1ce57-164">เลือกลูกศรเพื่อเพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="1ce57-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="1ce57-165">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-165">Select **Save**.</span></span>
18. <span data-ttu-id="1ce57-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="1ce57-167">อัพเดตเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="1ce57-167">Update a work template</span></span>
1. <span data-ttu-id="1ce57-168">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การตั้งค่า > งาน > เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="1ce57-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="1ce57-169">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="1ce57-169">Select **Edit**.</span></span>
3. <span data-ttu-id="1ce57-170">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="1ce57-170">Select **New**.</span></span>
4. <span data-ttu-id="1ce57-171">ในฟิลด์ **ประเภทงาน** ให้เลือก **พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="1ce57-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="1ce57-172">ในฟิลด์ **รหัสคลาสงาน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1ce57-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="1ce57-173">เลือก **เลื่อนขึ้น**</span><span class="sxs-lookup"><span data-stu-id="1ce57-173">Select **Move up**.</span></span>
7. <span data-ttu-id="1ce57-174">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1ce57-174">Select **Save**.</span></span>
8. <span data-ttu-id="1ce57-175">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1ce57-175">Close the page.</span></span>

