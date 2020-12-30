---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3 - ออกแบบรายงาน)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER '
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684798"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="aa37a-103">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3 - ออกแบบรายงาน)</span><span class="sxs-lookup"><span data-stu-id="aa37a-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa37a-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="aa37a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="aa37a-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="aa37a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="aa37a-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aa37a-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="aa37a-107">ออกแบบรายงานเพื่อแสดงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="aa37a-108">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="aa37a-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="aa37a-109">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="aa37a-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="aa37a-110">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="aa37a-111">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="aa37a-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="aa37a-112">ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="aa37a-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="aa37a-113">ในฟิลด์ชื่อ ให้พิมพ์ 'รายงานสมุดบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="aa37a-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="aa37a-114">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="aa37a-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="aa37a-115">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="aa37a-115">Click Create configuration.</span></span>
8. <span data-ttu-id="aa37a-116">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="aa37a-116">Click Designer.</span></span>
9. <span data-ttu-id="aa37a-117">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="aa37a-118">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="aa37a-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="aa37a-119">ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'</span><span class="sxs-lookup"><span data-stu-id="aa37a-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="aa37a-120">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-120">Click OK.</span></span>
13. <span data-ttu-id="aa37a-121">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="aa37a-122">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="aa37a-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="aa37a-123">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="aa37a-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="aa37a-124">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-124">Click OK.</span></span>
17. <span data-ttu-id="aa37a-125">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="aa37a-126">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="aa37a-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="aa37a-127">ในฟิลด์ชื่อ ให้พิมพ์ 'สมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="aa37a-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="aa37a-128">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-128">Click OK.</span></span>
21. <span data-ttu-id="aa37a-129">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="aa37a-130">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="aa37a-131">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="aa37a-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="aa37a-132">ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="aa37a-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="aa37a-133">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-133">Click OK.</span></span>
26. <span data-ttu-id="aa37a-134">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="aa37a-135">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="aa37a-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="aa37a-136">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="aa37a-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="aa37a-137">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-137">Click OK.</span></span>
30. <span data-ttu-id="aa37a-138">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="aa37a-139">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="aa37a-140">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="aa37a-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="aa37a-141">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="aa37a-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="aa37a-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-142">Click OK.</span></span>
35. <span data-ttu-id="aa37a-143">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="aa37a-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="aa37a-144">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="aa37a-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="aa37a-145">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-145">Click OK.</span></span>
38. <span data-ttu-id="aa37a-146">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="aa37a-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="aa37a-147">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="aa37a-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="aa37a-148">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-148">Click OK.</span></span>
41. <span data-ttu-id="aa37a-149">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="aa37a-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="aa37a-150">ในฟิลด์ ชื่อ ให้พิมพ์ 'Dt'</span><span class="sxs-lookup"><span data-stu-id="aa37a-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="aa37a-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-151">Click OK.</span></span>
44. <span data-ttu-id="aa37a-152">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="aa37a-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="aa37a-153">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Ct'</span><span class="sxs-lookup"><span data-stu-id="aa37a-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="aa37a-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-154">Click OK.</span></span>
47. <span data-ttu-id="aa37a-155">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="aa37a-156">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="aa37a-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="aa37a-157">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Dimensions'</span><span class="sxs-lookup"><span data-stu-id="aa37a-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="aa37a-158">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="aa37a-158">Click OK.</span></span>
51. <span data-ttu-id="aa37a-159">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="aa37a-160">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aa37a-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="aa37a-161">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="aa37a-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="aa37a-162">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="aa37a-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="aa37a-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-163">Click OK.</span></span>
56. <span data-ttu-id="aa37a-164">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="aa37a-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="aa37a-165">ในฟิลด์ ชื่อ ให้พิมพ์ 'Value'</span><span class="sxs-lookup"><span data-stu-id="aa37a-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="aa37a-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aa37a-166">Click OK.</span></span>
59. <span data-ttu-id="aa37a-167">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="aa37a-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="aa37a-168">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Desc'</span><span class="sxs-lookup"><span data-stu-id="aa37a-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="aa37a-169">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="aa37a-169">Click OK.</span></span>
<span data-ttu-id="aa37a-170">![เพจตัวออกแบบการดำเนินงาน ER](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="aa37a-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="aa37a-171">แม็ปองค์ประกอบของรายงานไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="aa37a-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="aa37a-172">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="aa37a-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="aa37a-173">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="aa37a-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="aa37a-174">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="aa37a-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="aa37a-175">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="aa37a-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="aa37a-176">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="aa37a-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="aa37a-177">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\คำอธิบาย: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="aa37a-178">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\คำอธิบาย: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="aa37a-179">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-179">Click Bind.</span></span>
9. <span data-ttu-id="aa37a-180">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\ค่า: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="aa37a-181">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="aa37a-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-182">Click Bind.</span></span>
12. <span data-ttu-id="aa37a-183">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\รหัส: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="aa37a-184">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\ชื่อ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="aa37a-185">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-185">Click Bind.</span></span>
15. <span data-ttu-id="aa37a-186">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="aa37a-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="aa37a-187">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="aa37a-188">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-188">Click Bind.</span></span>
18. <span data-ttu-id="aa37a-189">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\Ct: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="aa37a-190">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เครดิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="aa37a-191">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-191">Click Bind.</span></span>
21. <span data-ttu-id="aa37a-192">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\Dt: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="aa37a-193">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เดบิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="aa37a-194">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-194">Click Bind.</span></span>
24. <span data-ttu-id="aa37a-195">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\สกุลเงิน: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="aa37a-196">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\สกุลเงิน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="aa37a-197">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-197">Click Bind.</span></span>
27. <span data-ttu-id="aa37a-198">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\วันที่: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="aa37a-199">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\วันที่: วันที่'</span><span class="sxs-lookup"><span data-stu-id="aa37a-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="aa37a-200">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-200">Click Bind.</span></span>
30. <span data-ttu-id="aa37a-201">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\ใบสำคัญ: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="aa37a-202">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ใบสำคัญ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="aa37a-203">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-203">Click Bind.</span></span>
33. <span data-ttu-id="aa37a-204">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="aa37a-205">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="aa37a-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="aa37a-206">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-206">Click Bind.</span></span>
36. <span data-ttu-id="aa37a-207">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ชุดงาน: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="aa37a-208">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="aa37a-209">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-209">Click Bind.</span></span>
39. <span data-ttu-id="aa37a-210">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="aa37a-211">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="aa37a-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="aa37a-212">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-212">Click Bind.</span></span>
42. <span data-ttu-id="aa37a-213">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\บริษัท: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="aa37a-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="aa37a-214">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\บริษัท: สตริง'</span><span class="sxs-lookup"><span data-stu-id="aa37a-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="aa37a-215">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="aa37a-215">Click Bind.</span></span>
45. <span data-ttu-id="aa37a-216">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="aa37a-216">Click Save.</span></span>
46. <span data-ttu-id="aa37a-217">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aa37a-217">Close the page.</span></span>
<span data-ttu-id="aa37a-218">![เพจตัวออกแบบการดำเนินงาน ER](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="aa37a-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

