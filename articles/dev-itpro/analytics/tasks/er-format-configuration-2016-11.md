--- 
title: "สร้างการตั้งค่าคอนฟิกรูปแบบของ ER (พฤศจิกายน 2016)"
description: "ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: th-th
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="dcba4-103">สร้างการตั้งค่าคอนฟิกรูปแบบของ ER (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="dcba4-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dcba4-104">ขั้นตอนต่อไปนี้อธิบายถึงผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="dcba4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="dcba4-105">การตั้งค่าคอนฟิกรูปแบบนี้จะใช้กำหนดรูปแบบของเอกสารทางอิเล็กทรอนิกส์ที่ถูกใช้สำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dcba4-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="dcba4-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "แม็ปแบบจำลองไปยังแหล่งข้อมูลที่เลือก" ก่อน </span><span class="sxs-lookup"><span data-stu-id="dcba4-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="dcba4-107">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="dcba4-107">Create a new format configuration</span></span>
1. <span data-ttu-id="dcba4-108">ไปที่ **การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="dcba4-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="dcba4-109">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="dcba4-110">ในแผนภูมิ เลือก **การชำระเงิน (แบบจำลองอย่างง่าย)**</span><span class="sxs-lookup"><span data-stu-id="dcba4-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="dcba4-111">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dcba4-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="dcba4-112">ถ้าคุณไม่เห็น **สร้างการตั้งค่าคอนฟิก** คุณต้องเปิดใช้งานโหมดการออกแบบในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="dcba4-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="dcba4-113">ในฟิลด์ **สร้าง** ป้อน **รูปแบบตามแบบจำลองข้อมูล PaymentModel**</span><span class="sxs-lookup"><span data-stu-id="dcba4-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="dcba4-114">ในฟิลด์ **ชื่อ** พิมพ์ **BACS (UK แบบสมมติ)**</span><span class="sxs-lookup"><span data-stu-id="dcba4-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="dcba4-115">ในฟิลด์ **คำอธิบาย** พิมพ์ **รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (UK แบบสมมติ)**</span><span class="sxs-lookup"><span data-stu-id="dcba4-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="dcba4-116">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="dcba4-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="dcba4-117">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="dcba4-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="dcba4-118">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="dcba4-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="dcba4-119">รูปแบบเฉพาะของเอกสารทางอิเล็กทรอนิกส์สามารถถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="dcba4-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="dcba4-120">ปล่อยฟิลด์นี้ว่างเปล่า ถ้าคุณต้องการเลือกรูปแบบที่ตรงกับเวลาที่ใช้ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="dcba4-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="dcba4-121">ในฟิลด์ **คำนิยามแบบจำลองข้อมูล** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="dcba4-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="dcba4-122">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="dcba4-122">Click **Create configuration**.</span></span> <span data-ttu-id="dcba4-123">การตั้งค่าคอนฟิกใหม่ถูกสร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="dcba4-123">A new configuration has been created.</span></span> <span data-ttu-id="dcba4-124">รุ่นแบบร่างสามารถใช้เพื่อจัดเก็บรูปแบบการออกแบบสำหรับเอกสารการจัดการทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dcba4-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="dcba4-125">ถ้าคุณไม่เห็น **สร้างการตั้งค่าคอนฟิก** คุณต้องเปิดใช้งานโหมดการออกแบบในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="dcba4-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="dcba4-126">ออกแบบรูปแบบของเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dcba4-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="dcba4-127">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-127">Click **Designer**.</span></span>
2. <span data-ttu-id="dcba4-128">คลิก **เพิ่มราก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dcba4-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="dcba4-129">ในแผนภูมิ เลือก **ทั่วไป\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="dcba4-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="dcba4-130">ในฟิลด์ **ชื่อ** พิมพ์ **Xml**</span><span class="sxs-lookup"><span data-stu-id="dcba4-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="dcba4-131">ในฟิลด์ **การเข้ารหัส** พิมพ์ **UTF-8**</span><span class="sxs-lookup"><span data-stu-id="dcba4-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="dcba4-132">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-132">Click **OK**.</span></span>
7. <span data-ttu-id="dcba4-133">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="dcba4-133">Click **Add**.</span></span>
8. <span data-ttu-id="dcba4-134">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="dcba4-135">ในฟิลด์ **ชือ** พิมพ์ **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="dcba4-136">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-136">Click **OK**.</span></span>
11. <span data-ttu-id="dcba4-137">ในแผนภูมิ ให้เลือก **Xml\ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="dcba4-138">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="dcba4-139">ในฟิลด์ **ชื่อ** พิมพ์ **วันที่ที่ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="dcba4-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="dcba4-140">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-140">Click **OK**.</span></span>
15. <span data-ttu-id="dcba4-141">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="dcba4-142">ในฟิลด์ชือ พิมพ์ **รหัสข้อความ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="dcba4-143">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-143">Click **OK**.</span></span>
18. <span data-ttu-id="dcba4-144">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="dcba4-145">ในฟิลด์ **ชื่อ** ให้พิมพ์ **การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="dcba4-146">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-146">Click **OK**.</span></span>
21. <span data-ttu-id="dcba4-147">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="dcba4-148">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="dcba4-149">ในฟิลด์ **ชื่อ** พิมพ์ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="dcba4-150">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-150">Click **OK**.</span></span>
25. <span data-ttu-id="dcba4-151">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="dcba4-152">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="dcba4-152">Click **Add**.</span></span>
27. <span data-ttu-id="dcba4-153">ในแผนภูมิ เลือก **XML\แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="dcba4-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="dcba4-154">ในฟิลด์ชื่อ พิมพ์ **รหัส**</span><span class="sxs-lookup"><span data-stu-id="dcba4-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="dcba4-155">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-155">Click **OK**.</span></span>
30. <span data-ttu-id="dcba4-156">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="dcba4-156">Click **Add**.</span></span>
31. <span data-ttu-id="dcba4-157">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="dcba4-158">ในฟิลด์ชื่อ พิมพ์ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="dcba4-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="dcba4-159">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-159">Click **OK**.</span></span>
34. <span data-ttu-id="dcba4-160">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="dcba4-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="dcba4-161">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="dcba4-162">ในฟิลด์ชื่อ พิมพ์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="dcba4-163">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-163">Click **OK**.</span></span>
38. <span data-ttu-id="dcba4-164">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="dcba4-165">ในฟิลด์ **ชื่อ** พิมพ์ **ธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="dcba4-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="dcba4-166">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-166">Click **OK**.</span></span>
41. <span data-ttu-id="dcba4-167">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="dcba4-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="dcba4-168">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="dcba4-169">ในฟิลด์ **ชื่อ** พิมพ์ **หมายเลขการกำหนดเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="dcba4-170">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-170">Click **OK**.</span></span>
45. <span data-ttu-id="dcba4-171">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="dcba4-172">ในฟิลด์ **ชื่อ** พิมพ์ **หมายเลขบัญชี**</span><span class="sxs-lookup"><span data-stu-id="dcba4-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="dcba4-173">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-173">Click **OK**.</span></span>
48. <span data-ttu-id="dcba4-174">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="dcba4-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="dcba4-175">คลิก **คัดลอก** </span><span class="sxs-lookup"><span data-stu-id="dcba4-175">Click **Copy**.</span></span>
50. <span data-ttu-id="dcba4-176">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="dcba4-177">คลิก **วาง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-177">Click **Paste**.</span></span>
52. <span data-ttu-id="dcba4-178">ในฟิลด์ **ชื่อ** พิมพ์ **ผู้ชำระ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="dcba4-179">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="dcba4-180">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="dcba4-181">ในฟิลด์ **ชื่อ** ให้พิมพ์ **สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="dcba4-182">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-182">Click **OK**.</span></span>
57. <span data-ttu-id="dcba4-183">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="dcba4-184">ในฟิลด์ **ชื่อ** ให้พิมพ์ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="dcba4-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="dcba4-185">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-185">Click **OK**.</span></span>
60. <span data-ttu-id="dcba4-186">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="dcba4-187">ในฟิลด์ชื่อ พิมพ์ **วันที่ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="dcba4-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="dcba4-188">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-188">Click **OK**.</span></span>
63. <span data-ttu-id="dcba4-189">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="dcba4-190">ในฟิลด์ชื่อ พิมพ์ **จำนวน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="dcba4-191">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="dcba4-192">จัดเตรียมส่วนประกอบรูปแบบสำหรับการแม็ปไปยังองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dcba4-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="dcba4-193">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\วันที่ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="dcba4-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="dcba4-194">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dcba4-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="dcba4-195">ในแผนภูมิ ให้เลือก **ข้อความอักษร\วันที่และเวลา**</span><span class="sxs-lookup"><span data-stu-id="dcba4-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="dcba4-196">ในฟิลด์ **รูปแบบ** พิมพ์ **yyyy-MM-dd**</span><span class="sxs-lookup"><span data-stu-id="dcba4-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="dcba4-197">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-197">Click **OK**.</span></span>
6. <span data-ttu-id="dcba4-198">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\วันที่ทำธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="dcba4-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="dcba4-199">คลิก **เพิ่มวันที่และเวลา**</span><span class="sxs-lookup"><span data-stu-id="dcba4-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="dcba4-200">ในฟิลด์ **รูปแบบ** พิมพ์ **yyyy-MM-dd**</span><span class="sxs-lookup"><span data-stu-id="dcba4-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="dcba4-201">ในฟิลด์ชนิด **วันที่และเวลา** ให้เลือก **วันที่**</span><span class="sxs-lookup"><span data-stu-id="dcba4-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="dcba4-202">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-202">Click **OK**.</span></span>
11. <span data-ttu-id="dcba4-203">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\รหัสข้อความ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="dcba4-204">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dcba4-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="dcba4-205">ในแผนภูมิ ให้เลือก **ข้อความ\สตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="dcba4-206">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-206">Click **OK**.</span></span>
15. <span data-ttu-id="dcba4-207">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="dcba4-208">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-208">Click **Add String**.</span></span>
17. <span data-ttu-id="dcba4-209">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-209">Click **OK**.</span></span>
18. <span data-ttu-id="dcba4-210">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="dcba4-211">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-211">Click **Add String**.</span></span>
20. <span data-ttu-id="dcba4-212">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-212">Click **OK**.</span></span>
21. <span data-ttu-id="dcba4-213">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขบัญชี**</span><span class="sxs-lookup"><span data-stu-id="dcba4-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="dcba4-214">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-214">Click **Add String**.</span></span>
23. <span data-ttu-id="dcba4-215">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-215">Click **OK**.</span></span>
24. <span data-ttu-id="dcba4-216">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="dcba4-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="dcba4-217">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-217">Click **Add String**.</span></span>
26. <span data-ttu-id="dcba4-218">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-218">Click **OK**.</span></span>
27. <span data-ttu-id="dcba4-219">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="dcba4-220">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-220">Click **Add String**.</span></span>
29. <span data-ttu-id="dcba4-221">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-221">Click **OK**.</span></span>
30. <span data-ttu-id="dcba4-222">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขบัญชี**</span><span class="sxs-lookup"><span data-stu-id="dcba4-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="dcba4-223">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-223">Click **Add String**.</span></span>
32. <span data-ttu-id="dcba4-224">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-224">Click **OK**.</span></span>
33. <span data-ttu-id="dcba4-225">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="dcba4-226">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-226">Click **Add String**.</span></span>
35. <span data-ttu-id="dcba4-227">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-227">Click **OK**.</span></span>
36. <span data-ttu-id="dcba4-228">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="dcba4-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="dcba4-229">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-229">Click **Add String**.</span></span>
38. <span data-ttu-id="dcba4-230">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-230">Click **OK**.</span></span>
39. <span data-ttu-id="dcba4-231">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\จำนวนเงิน**</span><span class="sxs-lookup"><span data-stu-id="dcba4-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="dcba4-232">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="dcba4-232">Click **Add String**.</span></span>
41. <span data-ttu-id="dcba4-233">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="dcba4-233">Click **OK**.</span></span>
42. <span data-ttu-id="dcba4-234">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dcba4-234">Click **Save**.</span></span>
43. <span data-ttu-id="dcba4-235">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dcba4-235">Close the page.</span></span>


