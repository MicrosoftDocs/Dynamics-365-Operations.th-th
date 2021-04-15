---
title: ER อัพเกรดรูปแบบของคุณโดยการใช้เวอร์ชันฐานใหม่ของรูปแบบนั้น
description: หัวข้อนี้อธิบายวิธีการรักษาการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05f8562bcab50a303b58174d177c6058f9417294
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744950"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="b6d80-103">ER อัพเกรดรูปแบบของคุณโดยการใช้เวอร์ชันฐานใหม่ของรูปแบบนั้น</span><span class="sxs-lookup"><span data-stu-id="b6d80-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6d80-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถรักษาการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="b6d80-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="b6d80-105">กระบวนงานนี้อธิบายวิธีการสร้างเวอร์ชันที่กำหนดเองของรูปแบบ ซึ่งเป็นไปตามรูปแบบที่ได้รับจากผู้ให้บริการการตั้งค่าคอนฟิก (CP)</span><span class="sxs-lookup"><span data-stu-id="b6d80-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="b6d80-106">นอกจากนี้ ยังอธิบายวิธีการนำเวอร์ชันฐานใหม่ของรูปแบบนั้นไปใช้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="b6d80-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="b6d80-107">เมื่อต้องการดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ลำดับแรกคุณต้องดำเนินงานขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" และกระบวนงาน "ใช้รูปแบบที่สร้างไว้เพื่อสร้างเอกสารอิเล็กทรอนิกส์สำหรับการชำระเงิน" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b6d80-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="b6d80-108">ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัท GBSI</span><span class="sxs-lookup"><span data-stu-id="b6d80-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="b6d80-109">เลือกการตั้งค่าคอนฟิกรูปแบบสำหรับการเลือกกำหนด</span><span class="sxs-lookup"><span data-stu-id="b6d80-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="b6d80-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b6d80-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="b6d80-111">ในตัวอย่างนี้ บริษัทตัวอย่าง Litware, Inc. (https://www.litware.com) จะทำหน้าที่เป็นผู้ให้บริการการตั้งค่าคอนฟิก ซึ่งสนับสนุนการตั้งค่าคอนฟิกรูปแบบสำหรับการชำระเงินทางอิเล็กทรอนิกส์สำหรับประเทศเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b6d80-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="b6d80-112">บริษัทตัวอย่าง Proseware, Inc. (http://www.proseware.com) จะทำหน้าที่เป็นลูกค้าของการตั้งค่าคอนฟิกรูปแบบที่ Litware, Inc. จัดให้</span><span class="sxs-lookup"><span data-stu-id="b6d80-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="b6d80-113">Proseware, Inc. ใช้รูปแบบในภูมิภาคบางแห่งของประเทศนั้น</span><span class="sxs-lookup"><span data-stu-id="b6d80-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="b6d80-114">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b6d80-115">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-115">Click Show filters.</span></span>
4. <span data-ttu-id="b6d80-116">ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรอง "BACS (แบบสมมติของ UK)" ในฟิลด์ "ชื่อ" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="b6d80-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="b6d80-117">BACS (การกำหนดเองแบบสมมติของ UK) ของการตั้งค่าคอนฟิกรูปแบบที่เลือก เป็นเจ้าของโดยผู้ให้บริการ Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b6d80-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="b6d80-118">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-118">Click Show filters.</span></span>
6. <span data-ttu-id="b6d80-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b6d80-120">เวอร์ชันของรูปแบบที่มีสถานะเป็น 'เสร็จสมบูรณ์แล้ว' จะถูกใช้โดย Proseware, Inc. สำหรับการกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="b6d80-121">สร้างการตั้งค่าคอนฟิกใหม่ สำหรับรูปแบบการชำระเงินที่กำหนดเองของเอกสารอิเล็กทรอนิกส์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b6d80-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="b6d80-122">Proseware, Inc. ได้รับการตั้งค่าคอนฟิก BACS (แบบสมมติของ UK) เวอร์ชัน 1.1 ที่ประกอบด้วยรูปแบบเริ่มต้น ในการสร้างเอกสารการชำระเงินทางอิเล็กทรอนิกส์จาก Litware, Inc. ที่สอดคล้องกับการสมัครใช้งานบริการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="b6d80-123">Proseware, Inc. ต้องการเริ่มต้นการใช้ให้เป็นพื้นฐานสำหรับประเทศของพวกเขา แต่การกำหนดค่าเองบางมีความจำเป็นในการสนับสนุนข้อกำหนดเฉพาะส่วนภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="b6d80-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="b6d80-124">Proseware, Inc. ยังต้องการเก็บความสามารถในการอัพเกรดรูปแบบที่กำหนดเอง ทันทีที่เวอร์ชันใหม่ออกมา (ซึ่งมีการเปลี่ยนแปลงเพื่อสนับสนุนข้อกำหนดเฉพาะประเทศ)จาก Litware, Inc. และพวกเขาต้องการที่จะดำเนินการอัพเกรดนี้ด้วยต้นทุนที่ต่ำที่สุด</span><span class="sxs-lookup"><span data-stu-id="b6d80-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="b6d80-125">เพื่อดำเนินการสิ่งนี้ Proseware, Inc. ต้องสร้างการตั้งค่าคอนฟิกโดยใช้ BACS (แบบสมมติของ UK) ของการตั้งค่าคอนฟิก Litware, Inc. เป็นฐาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="b6d80-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b6d80-126">Close the page.</span></span>
2. <span data-ttu-id="b6d80-127">เลือก Proseware, Inc. เพื่อทำให้เป็นผู้ให้บริการที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b6d80-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="b6d80-128">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b6d80-128">Click Set active.</span></span>
4. <span data-ttu-id="b6d80-129">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="b6d80-130">ในแผนภูมิ ขยาย 'การชำระเงิน (แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="b6d80-131">ในแผนภูมิ เลือก 'การชำระเงิน (แบบจำลองอย่างง่าย)\BACS (แบบสมมติ UK)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="b6d80-132">เลือกการตั้งค่าคอนฟิก BACS (แบบสมมติของ UK) จาก Litware, Inc. Proseware, Inc. จะใช้รุ่น 1.1 เป็นฐานสำหรับรุ่นที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="b6d80-133">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b6d80-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="b6d80-134">การดำเนินการนี้ช่วยให้คุณสามารถสร้างการตั้งค่าคอนฟิกใหม่สำหรับรูปแบบการชำระเงินที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="b6d80-135">ในฟิลด์ใหม่ ป้อน ' สืบทอดมาจากชื่อ: BACS (แบบสมมติ UK) Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="b6d80-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="b6d80-136">เลือกตัวเลือก ได้รับมา เพื่อยืนยันการใช้งานของ BACS (แบบสมมติ UK) เป็นฐานสำหรับการสร้างเวอร์ชันที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="b6d80-137">ในฟิลด์ชือ ให้พิมพ์ 'BACS (การกำหนดเองแบบสมมติของ UK)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="b6d80-138">ในฟิลด์คำอธิบาย พิมพ์ 'รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (การกำหนดเองแบบสมมติของ UK)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="b6d80-139">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่ (Proseware, Inc.) จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b6d80-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="b6d80-140">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="b6d80-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="b6d80-141">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="b6d80-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="b6d80-142">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b6d80-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="b6d80-143">กำหนดรูปแบบของคุณสำหรับเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b6d80-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="b6d80-144">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-144">Click Designer.</span></span>
2. <span data-ttu-id="b6d80-145">คลิก ขยาย/ยุบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="b6d80-146">คลิก ขยาย/ยุบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="b6d80-147">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="b6d80-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="b6d80-148">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b6d80-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="b6d80-149">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="b6d80-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="b6d80-150">ในฟิลด์ชื่อ ให้พิมพ์ 'IBAN'</span><span class="sxs-lookup"><span data-stu-id="b6d80-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="b6d80-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b6d80-151">Click OK.</span></span>
9. <span data-ttu-id="b6d80-152">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\IBAN'</span><span class="sxs-lookup"><span data-stu-id="b6d80-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="b6d80-153">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b6d80-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="b6d80-154">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="b6d80-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="b6d80-155">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b6d80-155">Click OK.</span></span>
13. <span data-ttu-id="b6d80-156">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="b6d80-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="b6d80-157">ในฟิลด์ความยาวสูงสุด ให้ป้อน '60'</span><span class="sxs-lookup"><span data-stu-id="b6d80-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="b6d80-158">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="b6d80-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="b6d80-159">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="b6d80-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="b6d80-160">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="b6d80-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="b6d80-161">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="b6d80-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="b6d80-162">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\บัญชี'</span><span class="sxs-lookup"><span data-stu-id="b6d80-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="b6d80-163">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\บัญชี\IBAN'</span><span class="sxs-lookup"><span data-stu-id="b6d80-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="b6d80-164">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ = แบบจำลอง.การชำระเงิน\ผู้จัดจำหน่าย\ธนาคาร\IBAN\สตริง'</span><span class="sxs-lookup"><span data-stu-id="b6d80-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="b6d80-165">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b6d80-165">Click Bind.</span></span>
23. <span data-ttu-id="b6d80-166">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b6d80-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="b6d80-167">ตรวจสอบความถูกต้องของรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-167">Validate the customized format</span></span>
1. <span data-ttu-id="b6d80-168">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b6d80-168">Click Validate.</span></span>

    <span data-ttu-id="b6d80-169">ตรวจสอบโครงร่างรูปแบบที่กำหนดเอง และการเปลี้ยนแปลงการแม็ปของข้อมูล เพื่อให้แน่ใจว่าการผูกข้อมูลทั้งหมดถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b6d80-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="b6d80-170">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b6d80-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="b6d80-171">เปลี่ยนสถานะของเวอร์ชันปัจจุบันของการตั้งค่าคอนฟิกรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="b6d80-172">เปลี่ยนสถานะของการตั้งค่าคอนฟิกรูปแบบที่ออกแบบแล้วจากแบบร่างเป็นแบบที่เสร็จสมบูรณ์ เพื่อทำให้พร้อมใช้งานสำหรับการตั้งค่าคอนฟิกเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b6d80-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="b6d80-173">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="b6d80-173">Click Change status.</span></span>

    <span data-ttu-id="b6d80-174">หมายเหตุว่าเวอร์ชันปัจจุบันของการตั้งค่าคอนฟิกที่เลือกอยู่ในสถานะแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="b6d80-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="b6d80-175">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b6d80-175">Click Complete.</span></span>
3. <span data-ttu-id="b6d80-176">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b6d80-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b6d80-177">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b6d80-177">Click OK.</span></span>
5. <span data-ttu-id="b6d80-178">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b6d80-179">หมายเหตุว่า การตั้งค่าคอนฟิกที่สร้างไว้ถูกบันทึกเป็นเวอร์ชัน 1.1.1 ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b6d80-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="b6d80-180">ซึ่งหมายความว่าเป็นเวอร์ชัน 1 ของรูปแบบ BACS (การกำหนดเองแบบสมมติของ UK) ที่กำหนดเอง ซึ่งเป็นไปตามเวอร์ชัน 1 ของรูปแบบ BACS (แบบสมมติ UK) ซึ่งเป็นไปตามเวอร์ชัน 1 ของแบบจำลองข้อมูลการชำระเงิน (แบบจำลองอย่างง่าย)</span><span class="sxs-lookup"><span data-stu-id="b6d80-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="b6d80-181">ทดสอบรูปแบบที่กำหนดเองเพื่อสร้างไฟล์การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b6d80-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="b6d80-182">ดำเนินการขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "ใช้รูปแบบที่สร้างไว้เพื่อสร้างเอกสารอิเล็กทรอนิกส์สำหรับการชำระเงิน" ในรอบเวลา Finance and Operations แบบขนาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="b6d80-183">เลือกรูปแบบ BACS (การกำหนดเองแบบสมมติของ UK) ในพารามิเตอร์วิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b6d80-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="b6d80-184">ตรวจสอบให้แน่ใจว่าไฟล์การชำระเงินที่สร้างประกอบด้วย โหนด XML ที่นำมาใช้ล่าสุด ซึ่งแสดงรหัส IBAN ที่สอดคล้องกับความต้องการทางภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="b6d80-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="b6d80-185">อัพเดตการตั้งค่าคอนฟิกเฉพาะประเทศที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b6d80-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="b6d80-186">Litware, Inc. ต้องอัพเดตการตั้งค่าคอนฟิก BACS (แบบสมมติ UK) และนำข้อกำหนดใหม่ของประเทศมาใช้สำหรับการจัดการรูปแบบของเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b6d80-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="b6d80-187">ในภายหลัง นี่จะถูกแนบในเวอร์ชันใหม่ของการตั้งค่าคอนฟิกซึ่งจะถูกเสนอสำหรับผู้ติดตามบริการ ซึ่งรวมกึง Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b6d80-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="b6d80-188">ในการเตรียมใช้งานบริการจริงที่เกี่ยวข้องกับกระบวนการ รุ่นใหม่ของ BACS (แบบสมมติของ UK) แต่ละรุ่นสามารถถูกนำเข้าได้โดย Proseware, Inc. จากที่เก็บ LCS ของการตั้งค่าคอนฟิกของ Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b6d80-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="b6d80-189">ในกระบวนงานนี้ เราจะจำลองโดยการอัพเดต BACS (แบบสมมติ UK) ในนามของผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="b6d80-190">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b6d80-190">Close the page.</span></span>
2. <span data-ttu-id="b6d80-191">เลือก Litware, Inc. ผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="b6d80-192">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b6d80-192">Click Set active.</span></span>
4. <span data-ttu-id="b6d80-193">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="b6d80-194">ในแผนภูมิ ขยาย 'การชำระเงิน (แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="b6d80-195">ในแผนภูมิ เลือก 'การชำระเงิน (แบบจำลองอย่างง่าย)\BACS (แบบสมมติ UK)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="b6d80-196">เวอร์ชันแบบร่างที่ครอบครองโดย BACS (แบบสมมติ UK) ของผู้ให้บริการ Litware, Inc. จะถูกเลือกเพื่อนำการเปลี่ยนแปลงไปสนับสนุนข้อกำหนดเฉพาะประเทศใหม่</span><span class="sxs-lookup"><span data-stu-id="b6d80-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="b6d80-197">แปลรูปแบบพื้นฐานของเอกสารทางอิเล็กทรอนิกส์เป็นภาษาท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="b6d80-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="b6d80-198">สมมติว่ามีข้อกำหนดเฉพาะประเทศใหม่ที่ต้องได้รับการสนับสนุนโดย Litware, Inc.:</span><span class="sxs-lookup"><span data-stu-id="b6d80-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="b6d80-199">ค่าสำหรับรหัส SWIFT ของธนาคารเจ้าหนี้ในธุรกรรมการชำระเงินแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="b6d80-200">ขีดจำกัดอักขระ100 ตัวสำหรับความยาวของข้อความสำหรับชื่อผู้จัดจำหน่ายในไฟล์การสร้าง</span><span class="sxs-lookup"><span data-stu-id="b6d80-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="b6d80-201">ข้อกำหนดเฉพาะประเทศใหม่</span><span class="sxs-lookup"><span data-stu-id="b6d80-201">New country-specific requirements</span></span>  
- <span data-ttu-id="b6d80-202">เลือกเวอร์ชันแบบร่างของการตั้งค่าคอนฟิกที่ต้องการเพื่อนำการเปลี่ยนแปลงที่จำเป็นไปใช้</span><span class="sxs-lookup"><span data-stu-id="b6d80-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="b6d80-203">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-203">Click Designer.</span></span>
2. <span data-ttu-id="b6d80-204">คลิก ขยาย/ยุบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="b6d80-205">คลิก ขยาย/ยุบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="b6d80-206">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="b6d80-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="b6d80-207">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b6d80-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="b6d80-208">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="b6d80-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="b6d80-209">ในฟิลด์ชื่อ พิมพ์ 'SWIFT'</span><span class="sxs-lookup"><span data-stu-id="b6d80-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="b6d80-210">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="b6d80-210">Click OK.</span></span>
9. <span data-ttu-id="b6d80-211">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\SWIFT'</span><span class="sxs-lookup"><span data-stu-id="b6d80-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="b6d80-212">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b6d80-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="b6d80-213">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="b6d80-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="b6d80-214">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b6d80-214">Click OK.</span></span>
13. <span data-ttu-id="b6d80-215">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="b6d80-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="b6d80-216">ในฟิลด์ความยาวสูงสุด ให้ป้อน '100'</span><span class="sxs-lookup"><span data-stu-id="b6d80-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="b6d80-217">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="b6d80-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="b6d80-218">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="b6d80-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="b6d80-219">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="b6d80-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="b6d80-220">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="b6d80-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="b6d80-221">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="b6d80-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="b6d80-222">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\ตัวแทน\SWIFT'</span><span class="sxs-lookup"><span data-stu-id="b6d80-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="b6d80-223">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ = แบบจำลอง.การชำระเงิน\ผู้จัดจำหน่าย\ธนาคาร\SWIFT\สตริง'</span><span class="sxs-lookup"><span data-stu-id="b6d80-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="b6d80-224">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b6d80-224">Click Bind.</span></span>
23. <span data-ttu-id="b6d80-225">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b6d80-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="b6d80-226">ตรวจสอบความถูกต้องของรูปแบบที่แปลเป็นภาษาท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="b6d80-226">Validate the localized format</span></span>
1. <span data-ttu-id="b6d80-227">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b6d80-227">Click Validate.</span></span>
2. <span data-ttu-id="b6d80-228">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b6d80-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="b6d80-229">เปลี่ยนสถานะของเวอร์ชันปัจจุบันของการตั้งค่าคอนฟิกรูปแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="b6d80-230">เปลี่ยนสถานะของการตั้งค่าคอนฟิกรูปแบบฐานที่อัพเดต จากแบบร่างเป็นแบบที่เสร็จสมบูรณ์ เพื่อทำให้พร้อมใช้งานสำหรับการสร้างเอกสารการชำระเงิน และอัพเดตการตั้งค่าคอนฟิกรูปแบบที่ได้มา</span><span class="sxs-lookup"><span data-stu-id="b6d80-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="b6d80-231">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="b6d80-231">Click Change status.</span></span>

    <span data-ttu-id="b6d80-232">หมายเหตุว่าเวอร์ชันปัจจุบันของการตั้งค่าคอนฟิกที่เลือกอยู่ในสถานะแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="b6d80-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="b6d80-233">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b6d80-233">Click Complete.</span></span>
3. <span data-ttu-id="b6d80-234">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b6d80-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b6d80-235">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b6d80-235">Click OK.</span></span>
5. <span data-ttu-id="b6d80-236">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="b6d80-237">เปลี่ยนเวอร์ชันฐานสำหรับการตั้งค่าคอนฟิกรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="b6d80-238"> Proseware, Inc. ได้รับรายงานว่า เวอร์ชันใหม่ 1.2 ของการตั้งค่าคอนฟิก BACS (แบบสมมติ UK) พร้อมใช้งานในการสร้างเอกสารการชำระเงินอิเล็กทรอนิกส์ ที่สอดคล้องกับข้อกำหนดเฉพาะประเทศที่เพิ่งได้ประกาศมาไม่นานนี้ </span><span class="sxs-lookup"><span data-stu-id="b6d80-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="b6d80-239">Proseware, Inc. ต้องการเริ่มต้นการใช้ให้เป็นพื้นฐานสำหรับประเทศ</span><span class="sxs-lookup"><span data-stu-id="b6d80-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="b6d80-240">เพื่อดำเนินการนี้ Proseware, Inc. ต้องการเปลี่ยนแปลงเวอร์ชันการตั้งค่าคอนฟิกพื้นฐานสำหรับ BACS (การกำหนดเองแบบสมมติของ UK) ของการตั้งค่าคอนฟิกที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="b6d80-241">แทนที่เวอร์ชัน 1.1 ของ BACS (แบบสมมติ UK) ใช้เวอร์ชันใหม่ 1.2</span><span class="sxs-lookup"><span data-stu-id="b6d80-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="b6d80-242">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b6d80-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b6d80-243">เลือก ผู้ให้บริการ Proseware, Inc. เพื่อทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b6d80-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="b6d80-244">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b6d80-244">Click Set active.</span></span>
4. <span data-ttu-id="b6d80-245">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="b6d80-246">ในแผนภูมิ ขยาย 'การชำระเงิน (แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="b6d80-247">ในแผนภูมิ ขยาย 'การชำระเงิน (แบบจำลองอย่างง่าย)\BACS (แบบสมมติ UK)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="b6d80-248">ในแผนภูมิ เลือก 'การชำระเงิน (แบบจำลองอย่างง่าย)\BACS (แบบสมมติ UK)\BACS (การกำหนดเองแบบสมมติของ UK)'</span><span class="sxs-lookup"><span data-stu-id="b6d80-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="b6d80-249">เลือกการตั้งค่าคอนฟิก BACS (การกำหนดเองแบบสมมติของ UK) ซึ่งเป็นเจ้าของโดย Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b6d80-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="b6d80-250">ใช้เวอร์ชันแบบร่างของการตั้งค่าคอนฟิกที่เลือก เพื่อนำการเปลี่ยนแปลงที่จำเป็นไปใช้</span><span class="sxs-lookup"><span data-stu-id="b6d80-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="b6d80-251">คลิกปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="b6d80-251">Click Rebase.</span></span>

    <span data-ttu-id="b6d80-252">เลือกเวอร์ชันใหม่ 1.2 เป็นการตั้งค่าคอนฟิกพื้นฐาน เพื่อนำไปใช้เป็นฐานใหม่สำหรับการอัพเดตการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b6d80-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="b6d80-253">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b6d80-253">Click OK.</span></span>

    <span data-ttu-id="b6d80-254">หมายเหตุว่า ความขัดแย้งบางอย่างได้ถูกพบระหว่างการผสานรุ่นที่กำหนดเองและรุ่นฐานใหม่ ซึ่งแสดงการเปลี่ยนแปลงรูปแบบบางอย่างที่ไม่สามารถผสานได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b6d80-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="b6d80-255">แก้ไขความขัดแย้งของการปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="b6d80-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="b6d80-256">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b6d80-256">Click Designer.</span></span>
    
    <span data-ttu-id="b6d80-257">หมายเหตุว่า การเปลี่ยนแปลงไปยังขีดจำกัดความยาวข้อความของชื่อผู้จัดจำหน่ายไม่สามารถถูกแก้ไขได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b6d80-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="b6d80-258">ดังนั้น จะถูกแสดงในรายการความขัดแย้ง</span><span class="sxs-lookup"><span data-stu-id="b6d80-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="b6d80-259">สำหรับความขัดแย้งของชนิดการอัพเดตแต่ละชนิด ตัวเลือกต่อไปนี้จะพร้อมใช้งาน: - ใช้ค่าฐานก่อนหน้า (ปุ่มบนสุดของกริด) เพื่อนำค่าเวอร์ชันฐานก่อนหน้ามาใช้ (0 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="b6d80-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="b6d80-260">- ใช้ค่าฐานก่อนหน้า (ปุ่มบนสุดของกริด) เพื่อนำค่าเวอร์ชันฐานใหม่มา (100 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="b6d80-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="b6d80-261">- คงค่า (ที่กำหนดเอง) ของคุณ (60 ในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="b6d80-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="b6d80-262">คลิก ใช้งานค่าฐาน เพื่อใช้งานขีดจำกัดเฉพาะประเทศที่เป็น 100 อักขระ สำหรับความยาวข้อความของชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b6d80-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="b6d80-263">โปรดทราบว่า Proseware, Inc. และ Litware, Inc. มีเวอร์ชันที่กำหนดเองเฉพาะของรูปแบบนี้ โดยใช้รหัส IBAN และ SWIFT ที่มีส่วนประกอบที่สัมพันธ์กัน ซึ่งถูกผสานโดยอัตโนมัติในรูปแบบการจัดการ</span><span class="sxs-lookup"><span data-stu-id="b6d80-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="b6d80-264">คลิกใช้ค่าฐาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-264">Click Apply base value.</span></span>

    <span data-ttu-id="b6d80-265">คลิกใช้ค่าฐาน เพื่อใช้งานขีดจำกัดเฉพาะประเทศเป็น 100 อักขระสำหรับชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b6d80-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="b6d80-266">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b6d80-266">Click Save.</span></span>

    <span data-ttu-id="b6d80-267">การบันทึกรูปแบบจะลบความขัดแย้งที่แก้ไขแล้วจากรายการความขัดแย้ง</span><span class="sxs-lookup"><span data-stu-id="b6d80-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="b6d80-268">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b6d80-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="b6d80-269">เปลี่ยนสถานะของเวอร์ชันใหม่ของการตั้งค่าคอนฟิกรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b6d80-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="b6d80-270">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="b6d80-270">Click Change status.</span></span>

    <span data-ttu-id="b6d80-271">เปลี่ยนสถานะจากการตั้งค่าคอนฟิกรูปแบบด้วยตนเองที่อัพเดตแล้วจากแบบร่างเป็นเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="b6d80-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="b6d80-272">การดำเนินการนี้จะทำให้การตั้งค่าคอนฟิกรูปแบบพร้อมใช้งานสำหรับการสร้างเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b6d80-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="b6d80-273">หมายเหตุว่าเวอร์ชันปัจจุบันของการตั้งค่าคอนฟิกที่เลือกอยู่ในสถานะแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="b6d80-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="b6d80-274">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b6d80-274">Click Complete.</span></span>
3. <span data-ttu-id="b6d80-275">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b6d80-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b6d80-276">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b6d80-276">Click OK.</span></span>

    <span data-ttu-id="b6d80-277">หมายเหตุว่า การตั้งค่าคอนฟิกที่สร้างไว้ถูกบันทึกเป็นเวอร์ชัน 1.2.2 ที่สมบูรณ์: เวอร์ชัน 2 ของรูปแบบ BACS (การกำหนดเองแบบสมมติของ UK) พื้นฐาน ซึ่งเป็นไปตามเวอร์ชัน 2 ของรูปแบบ BACS (แบบสมมติ UK) พื้นฐาน ซึ่งเป็นไปตามเวอร์ชัน 1 ของแบบจำลองข้อมูลการชำระเงิน (แบบจำลองอย่างง่าย)</span><span class="sxs-lookup"><span data-stu-id="b6d80-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="b6d80-278">ทดสอบรูปแบบที่กำหนดเองสำหรับการสร้างไฟล์การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b6d80-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="b6d80-279">ดำเนินการขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "ใช้รูปแบบที่สร้างไว้เพื่อสร้างเอกสารอิเล็กทรอนิกส์สำหรับการชำระเงิน" ในรอบเวลา Finance and Operations แบบขนาน</span><span class="sxs-lookup"><span data-stu-id="b6d80-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="b6d80-280">เลือกรูปแบบ 'BACS (การกำหนดเองแบบสมมติของ UK)' ในพารามิเตอร์วิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b6d80-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="b6d80-281">ตรวจสอบให้แน่ใจว่าไฟล์การชำระเงินที่สร้างประกอบด้วยข้อมูลที่นำมาใช้ล่าสุดโดยโหนด XML ของ Proseware, Inc. ซึ่งแสดงรหัส IBAN ที่สอดคล้องกับความต้องการทางภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="b6d80-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="b6d80-282">ไฟล์นี้ยังควรประกอบด้วยข้อมูลที่นำมาใช้ล่าสุดโดยโหนด XML ของ Litware, Inc. ซึ่งแสดงรหัส SWIFT ที่สอดคล้องกับความต้องการของประเทศ</span><span class="sxs-lookup"><span data-stu-id="b6d80-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]