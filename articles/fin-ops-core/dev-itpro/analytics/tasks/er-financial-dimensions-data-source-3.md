---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3 - ออกแบบรายงาน)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกแบบโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลของรายงาน ER (ส่วนที่ 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565249"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="f00c8-104">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3 - ออกแบบรายงาน)</span><span class="sxs-lookup"><span data-stu-id="f00c8-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f00c8-105">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="f00c8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f00c8-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="f00c8-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f00c8-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f00c8-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="f00c8-108">ออกแบบรายงานเพื่อแสดงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="f00c8-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f00c8-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f00c8-110">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f00c8-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f00c8-111">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f00c8-112">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f00c8-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="f00c8-113">ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f00c8-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="f00c8-114">ในฟิลด์ชื่อ ให้พิมพ์ 'รายงานสมุดบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="f00c8-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="f00c8-115">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="f00c8-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="f00c8-116">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f00c8-116">Click Create configuration.</span></span>
8. <span data-ttu-id="f00c8-117">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f00c8-117">Click Designer.</span></span>
9. <span data-ttu-id="f00c8-118">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="f00c8-119">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="f00c8-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="f00c8-120">ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'</span><span class="sxs-lookup"><span data-stu-id="f00c8-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="f00c8-121">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-121">Click OK.</span></span>
13. <span data-ttu-id="f00c8-122">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="f00c8-123">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="f00c8-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="f00c8-124">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f00c8-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="f00c8-125">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-125">Click OK.</span></span>
17. <span data-ttu-id="f00c8-126">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="f00c8-127">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="f00c8-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="f00c8-128">ในฟิลด์ชื่อ ให้พิมพ์ 'สมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="f00c8-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="f00c8-129">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-129">Click OK.</span></span>
21. <span data-ttu-id="f00c8-130">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="f00c8-131">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="f00c8-132">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="f00c8-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="f00c8-133">ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="f00c8-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="f00c8-134">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-134">Click OK.</span></span>
26. <span data-ttu-id="f00c8-135">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="f00c8-136">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="f00c8-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="f00c8-137">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="f00c8-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="f00c8-138">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-138">Click OK.</span></span>
30. <span data-ttu-id="f00c8-139">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="f00c8-140">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="f00c8-141">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="f00c8-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="f00c8-142">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="f00c8-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="f00c8-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-143">Click OK.</span></span>
35. <span data-ttu-id="f00c8-144">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="f00c8-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="f00c8-145">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="f00c8-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="f00c8-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-146">Click OK.</span></span>
38. <span data-ttu-id="f00c8-147">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="f00c8-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="f00c8-148">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="f00c8-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="f00c8-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-149">Click OK.</span></span>
41. <span data-ttu-id="f00c8-150">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="f00c8-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="f00c8-151">ในฟิลด์ ชื่อ ให้พิมพ์ 'Dt'</span><span class="sxs-lookup"><span data-stu-id="f00c8-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="f00c8-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-152">Click OK.</span></span>
44. <span data-ttu-id="f00c8-153">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="f00c8-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="f00c8-154">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Ct'</span><span class="sxs-lookup"><span data-stu-id="f00c8-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="f00c8-155">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-155">Click OK.</span></span>
47. <span data-ttu-id="f00c8-156">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="f00c8-157">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="f00c8-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="f00c8-158">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Dimensions'</span><span class="sxs-lookup"><span data-stu-id="f00c8-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="f00c8-159">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f00c8-159">Click OK.</span></span>
51. <span data-ttu-id="f00c8-160">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="f00c8-161">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f00c8-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="f00c8-162">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="f00c8-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="f00c8-163">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="f00c8-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="f00c8-164">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-164">Click OK.</span></span>
56. <span data-ttu-id="f00c8-165">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="f00c8-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="f00c8-166">ในฟิลด์ ชื่อ ให้พิมพ์ 'Value'</span><span class="sxs-lookup"><span data-stu-id="f00c8-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="f00c8-167">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f00c8-167">Click OK.</span></span>
59. <span data-ttu-id="f00c8-168">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="f00c8-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="f00c8-169">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Desc'</span><span class="sxs-lookup"><span data-stu-id="f00c8-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="f00c8-170">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f00c8-170">Click OK.</span></span>
<span data-ttu-id="f00c8-171">![เพจตัวออกแบบการดำเนินงาน ER](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="f00c8-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="f00c8-172">แม็ปองค์ประกอบของรายงานไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f00c8-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="f00c8-173">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="f00c8-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="f00c8-174">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f00c8-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f00c8-175">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f00c8-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="f00c8-176">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f00c8-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="f00c8-177">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f00c8-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="f00c8-178">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\คำอธิบาย: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="f00c8-179">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\คำอธิบาย: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="f00c8-180">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-180">Click Bind.</span></span>
9. <span data-ttu-id="f00c8-181">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\ค่า: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="f00c8-182">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="f00c8-183">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-183">Click Bind.</span></span>
12. <span data-ttu-id="f00c8-184">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\รหัส: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="f00c8-185">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\ชื่อ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="f00c8-186">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-186">Click Bind.</span></span>
15. <span data-ttu-id="f00c8-187">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f00c8-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="f00c8-188">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="f00c8-189">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-189">Click Bind.</span></span>
18. <span data-ttu-id="f00c8-190">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\Ct: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="f00c8-191">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เครดิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="f00c8-192">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-192">Click Bind.</span></span>
21. <span data-ttu-id="f00c8-193">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\Dt: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="f00c8-194">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เดบิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="f00c8-195">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-195">Click Bind.</span></span>
24. <span data-ttu-id="f00c8-196">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\สกุลเงิน: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="f00c8-197">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\สกุลเงิน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="f00c8-198">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-198">Click Bind.</span></span>
27. <span data-ttu-id="f00c8-199">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\วันที่: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="f00c8-200">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\วันที่: วันที่'</span><span class="sxs-lookup"><span data-stu-id="f00c8-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="f00c8-201">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-201">Click Bind.</span></span>
30. <span data-ttu-id="f00c8-202">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\ใบสำคัญ: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="f00c8-203">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ใบสำคัญ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="f00c8-204">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-204">Click Bind.</span></span>
33. <span data-ttu-id="f00c8-205">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="f00c8-206">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f00c8-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="f00c8-207">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-207">Click Bind.</span></span>
36. <span data-ttu-id="f00c8-208">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ชุดงาน: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="f00c8-209">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="f00c8-210">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-210">Click Bind.</span></span>
39. <span data-ttu-id="f00c8-211">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="f00c8-212">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f00c8-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="f00c8-213">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-213">Click Bind.</span></span>
42. <span data-ttu-id="f00c8-214">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\บริษัท: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="f00c8-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="f00c8-215">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\บริษัท: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f00c8-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="f00c8-216">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f00c8-216">Click Bind.</span></span>
45. <span data-ttu-id="f00c8-217">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f00c8-217">Click Save.</span></span>
46. <span data-ttu-id="f00c8-218">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f00c8-218">Close the page.</span></span>
<span data-ttu-id="f00c8-219">![เพจตัวออกแบบการดำเนินงาน ER](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="f00c8-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]