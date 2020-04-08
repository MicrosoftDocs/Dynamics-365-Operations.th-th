---
title: สร้างการตั้งค่าคอนฟิกรูปแบบของ ER (พฤศจิกายน 2016)
description: หัวข้อนี้อธิบายถึงวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af2899da843967bfaaa8f3c66906fc8e3765b573
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142512"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="5b57e-103">สร้างการตั้งค่าคอนฟิกรูปแบบของ ER (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="5b57e-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b57e-104">หัวข้อนี้อธิบายถึงวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="5b57e-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="5b57e-105">การตั้งค่าคอนฟิกรูปแบบนี้จะใช้กำหนดรูปแบบของเอกสารทางอิเล็กทรอนิกส์ที่ถูกใช้สำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="5b57e-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="5b57e-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกรูปแบบสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "แม็ปแบบจำลองไปยังแหล่งข้อมูลที่เลือก"</span><span class="sxs-lookup"><span data-stu-id="5b57e-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="5b57e-107">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="5b57e-107">Create a new format configuration</span></span>
1. <span data-ttu-id="5b57e-108">ไปที่ **การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="5b57e-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="5b57e-109">คลิก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="5b57e-110">ในแผนภูมิ เลือก **การชำระเงิน (แบบจำลองอย่างง่าย)**</span><span class="sxs-lookup"><span data-stu-id="5b57e-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="5b57e-111">คลิก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5b57e-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="5b57e-112">ถ้าคุณไม่เห็น **สร้างการตั้งค่าคอนฟิก** คุณต้องเปิดใช้งานโหมดการออกแบบในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="5b57e-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="5b57e-113">ในฟิลด์ **สร้าง** ป้อน **รูปแบบตามแบบจำลองข้อมูล PaymentModel**</span><span class="sxs-lookup"><span data-stu-id="5b57e-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="5b57e-114">ในฟิลด์ **ชื่อ** พิมพ์ **BACS (UK แบบสมมติ)**</span><span class="sxs-lookup"><span data-stu-id="5b57e-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="5b57e-115">ในฟิลด์ **คำอธิบาย** พิมพ์ **รูปแบบการชำระเงินของผู้จัดจำหน่าย BACS (UK แบบสมมติ)**</span><span class="sxs-lookup"><span data-stu-id="5b57e-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="5b57e-116">ผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่จะถูกป้อนไว้ที่นี่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5b57e-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5b57e-117">ผู้ให้บริการนี้จะสามารถรักษาการตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="5b57e-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5b57e-118">ผู้ให้บริการอื่นๆสามารถใช้การตั้งค่าคอนฟิกนี้ แต่จะไม่สามารถรักษาค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="5b57e-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="5b57e-119">รูปแบบเฉพาะของเอกสารทางอิเล็กทรอนิกส์สามารถถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="5b57e-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="5b57e-120">ปล่อยฟิลด์นี้ว่างเปล่า ถ้าคุณต้องการเลือกรูปแบบที่ตรงกับเวลาที่ใช้ในการผลิต</span><span class="sxs-lookup"><span data-stu-id="5b57e-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="5b57e-121">ในฟิลด์ **คำนิยามแบบจำลองข้อมูล** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5b57e-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="5b57e-122">คลิก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="5b57e-122">Click **Create configuration**.</span></span> <span data-ttu-id="5b57e-123">การตั้งค่าคอนฟิกใหม่ถูกสร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="5b57e-123">A new configuration has been created.</span></span> <span data-ttu-id="5b57e-124">รุ่นแบบร่างสามารถใช้เพื่อจัดเก็บรูปแบบการออกแบบสำหรับเอกสารการจัดการทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5b57e-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="5b57e-125">ออกแบบรูปแบบของเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5b57e-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="5b57e-126">คลิก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-126">Click **Designer**.</span></span>
2. <span data-ttu-id="5b57e-127">คลิก **เพิ่มราก** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5b57e-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="5b57e-128">ในแผนภูมิ เลือก **ทั่วไป\ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="5b57e-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="5b57e-129">ในฟิลด์ **ชื่อ** พิมพ์ **Xml**</span><span class="sxs-lookup"><span data-stu-id="5b57e-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="5b57e-130">ในฟิลด์ **การเข้ารหัส** พิมพ์ **UTF-8**</span><span class="sxs-lookup"><span data-stu-id="5b57e-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="5b57e-131">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-131">Click **OK**.</span></span>
7. <span data-ttu-id="5b57e-132">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5b57e-132">Click **Add**.</span></span>
8. <span data-ttu-id="5b57e-133">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="5b57e-134">ในฟิลด์ **ชือ** พิมพ์ **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="5b57e-135">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-135">Click **OK**.</span></span>
11. <span data-ttu-id="5b57e-136">ในแผนภูมิ ให้เลือก **Xml\ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="5b57e-137">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="5b57e-138">ในฟิลด์ **ชื่อ** พิมพ์ **วันที่ที่ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="5b57e-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="5b57e-139">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-139">Click **OK**.</span></span>
15. <span data-ttu-id="5b57e-140">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="5b57e-141">ในฟิลด์ชือ พิมพ์ **รหัสข้อความ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="5b57e-142">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-142">Click **OK**.</span></span>
18. <span data-ttu-id="5b57e-143">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="5b57e-144">ในฟิลด์ **ชื่อ** ให้พิมพ์ **การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="5b57e-145">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-145">Click **OK**.</span></span>
21. <span data-ttu-id="5b57e-146">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="5b57e-147">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="5b57e-148">ในฟิลด์ **ชื่อ** พิมพ์ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="5b57e-149">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-149">Click **OK**.</span></span>
25. <span data-ttu-id="5b57e-150">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="5b57e-151">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5b57e-151">Click **Add**.</span></span>
27. <span data-ttu-id="5b57e-152">ในแผนภูมิ เลือก **XML\แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="5b57e-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="5b57e-153">ในฟิลด์ชื่อ พิมพ์ **รหัส**</span><span class="sxs-lookup"><span data-stu-id="5b57e-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="5b57e-154">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-154">Click **OK**.</span></span>
30. <span data-ttu-id="5b57e-155">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5b57e-155">Click **Add**.</span></span>
31. <span data-ttu-id="5b57e-156">ในแผนภูมิ เลือก **XML\องค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="5b57e-157">ในฟิลด์ชื่อ พิมพ์ **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="5b57e-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="5b57e-158">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-158">Click **OK**.</span></span>
34. <span data-ttu-id="5b57e-159">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="5b57e-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="5b57e-160">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="5b57e-161">ในฟิลด์ชื่อ พิมพ์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="5b57e-162">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-162">Click **OK**.</span></span>
38. <span data-ttu-id="5b57e-163">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="5b57e-164">ในฟิลด์ **ชื่อ** พิมพ์ **ธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="5b57e-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="5b57e-165">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-165">Click **OK**.</span></span>
41. <span data-ttu-id="5b57e-166">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="5b57e-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="5b57e-167">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="5b57e-168">ในฟิลด์ **ชื่อ** พิมพ์ **หมายเลขการกำหนดเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="5b57e-169">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-169">Click **OK**.</span></span>
45. <span data-ttu-id="5b57e-170">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="5b57e-171">ในฟิลด์ **ชื่อ** พิมพ์ **หมายเลขบัญชี**</span><span class="sxs-lookup"><span data-stu-id="5b57e-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="5b57e-172">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-172">Click **OK**.</span></span>
48. <span data-ttu-id="5b57e-173">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="5b57e-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="5b57e-174">คลิก **คัดลอก** </span><span class="sxs-lookup"><span data-stu-id="5b57e-174">Click **Copy**.</span></span>
50. <span data-ttu-id="5b57e-175">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="5b57e-176">คลิก **วาง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-176">Click **Paste**.</span></span>
52. <span data-ttu-id="5b57e-177">ในฟิลด์ **ชื่อ** พิมพ์ **ผู้ชำระ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="5b57e-178">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="5b57e-179">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="5b57e-180">ในฟิลด์ **ชื่อ** ให้พิมพ์ **สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="5b57e-181">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-181">Click **OK**.</span></span>
57. <span data-ttu-id="5b57e-182">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="5b57e-183">ในฟิลด์ **ชื่อ** ให้พิมพ์ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="5b57e-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="5b57e-184">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-184">Click **OK**.</span></span>
60. <span data-ttu-id="5b57e-185">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="5b57e-186">ในฟิลด์ชื่อ พิมพ์ **วันที่ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="5b57e-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="5b57e-187">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-187">Click **OK**.</span></span>
63. <span data-ttu-id="5b57e-188">คลิก **เพิ่มองค์ประกอบ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="5b57e-189">ในฟิลด์ชื่อ พิมพ์ **จำนวน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="5b57e-190">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="5b57e-191">จัดเตรียมส่วนประกอบรูปแบบสำหรับการแม็ปไปยังองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5b57e-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="5b57e-192">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\วันที่ประมวลผล**</span><span class="sxs-lookup"><span data-stu-id="5b57e-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="5b57e-193">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5b57e-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="5b57e-194">ในแผนภูมิ ให้เลือก **ข้อความอักษร\วันที่และเวลา**</span><span class="sxs-lookup"><span data-stu-id="5b57e-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="5b57e-195">ในฟิลด์ **รูปแบบ** พิมพ์ **yyyy-MM-dd**</span><span class="sxs-lookup"><span data-stu-id="5b57e-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="5b57e-196">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-196">Click **OK**.</span></span>
6. <span data-ttu-id="5b57e-197">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\วันที่ทำธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="5b57e-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="5b57e-198">คลิก **เพิ่มวันที่และเวลา**</span><span class="sxs-lookup"><span data-stu-id="5b57e-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="5b57e-199">ในฟิลด์ **รูปแบบ** พิมพ์ **yyyy-MM-dd**</span><span class="sxs-lookup"><span data-stu-id="5b57e-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="5b57e-200">ในฟิลด์ชนิด **วันที่และเวลา** ให้เลือก **วันที่**</span><span class="sxs-lookup"><span data-stu-id="5b57e-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="5b57e-201">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-201">Click **OK**.</span></span>
11. <span data-ttu-id="5b57e-202">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\รหัสข้อความ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="5b57e-203">คลิก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="5b57e-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="5b57e-204">ในแผนภูมิ ให้เลือก **ข้อความ\สตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="5b57e-205">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-205">Click **OK**.</span></span>
15. <span data-ttu-id="5b57e-206">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="5b57e-207">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-207">Click **Add String**.</span></span>
17. <span data-ttu-id="5b57e-208">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-208">Click **OK**.</span></span>
18. <span data-ttu-id="5b57e-209">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="5b57e-210">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-210">Click **Add String**.</span></span>
20. <span data-ttu-id="5b57e-211">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-211">Click **OK**.</span></span>
21. <span data-ttu-id="5b57e-212">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขบัญชี**</span><span class="sxs-lookup"><span data-stu-id="5b57e-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="5b57e-213">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-213">Click **Add String**.</span></span>
23. <span data-ttu-id="5b57e-214">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-214">Click **OK**.</span></span>
24. <span data-ttu-id="5b57e-215">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="5b57e-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="5b57e-216">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-216">Click **Add String**.</span></span>
26. <span data-ttu-id="5b57e-217">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-217">Click **OK**.</span></span>
27. <span data-ttu-id="5b57e-218">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขเส้นทาง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="5b57e-219">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-219">Click **Add String**.</span></span>
29. <span data-ttu-id="5b57e-220">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-220">Click **OK**.</span></span>
30. <span data-ttu-id="5b57e-221">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขบัญชี**</span><span class="sxs-lookup"><span data-stu-id="5b57e-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="5b57e-222">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-222">Click **Add String**.</span></span>
32. <span data-ttu-id="5b57e-223">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-223">Click **OK**.</span></span>
33. <span data-ttu-id="5b57e-224">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="5b57e-225">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-225">Click **Add String**.</span></span>
35. <span data-ttu-id="5b57e-226">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-226">Click **OK**.</span></span>
36. <span data-ttu-id="5b57e-227">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="5b57e-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="5b57e-228">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-228">Click **Add String**.</span></span>
38. <span data-ttu-id="5b57e-229">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-229">Click **OK**.</span></span>
39. <span data-ttu-id="5b57e-230">ในแผนภูมิ ให้เลือก **Xml\ข้อความ\การชำระเงิน\รายการ\จำนวนเงิน**</span><span class="sxs-lookup"><span data-stu-id="5b57e-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="5b57e-231">คลิก **เพิ่มสตริง**</span><span class="sxs-lookup"><span data-stu-id="5b57e-231">Click **Add String**.</span></span>
41. <span data-ttu-id="5b57e-232">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="5b57e-232">Click **OK**.</span></span>
42. <span data-ttu-id="5b57e-233">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5b57e-233">Click **Save**.</span></span>
43. <span data-ttu-id="5b57e-234">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5b57e-234">Close the page.</span></span>

