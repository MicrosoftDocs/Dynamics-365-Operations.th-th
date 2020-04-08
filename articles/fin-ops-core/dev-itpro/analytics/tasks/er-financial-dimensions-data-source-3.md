---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3 - ออกแบบรายงาน)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbbc81eaf8c13e8d13e30a0276e38453e07ead9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142535"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="bd68b-103">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3 - ออกแบบรายงาน)</span><span class="sxs-lookup"><span data-stu-id="bd68b-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd68b-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="bd68b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="bd68b-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="bd68b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="bd68b-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd68b-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="bd68b-107">ออกแบบรายงานเพื่อแสดงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="bd68b-108">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="bd68b-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bd68b-109">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="bd68b-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bd68b-110">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="bd68b-111">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="bd68b-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="bd68b-112">ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd68b-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="bd68b-113">ในฟิลด์ชื่อ ให้พิมพ์ 'รายงานสมุดบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="bd68b-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="bd68b-114">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="bd68b-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="bd68b-115">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="bd68b-115">Click Create configuration.</span></span>
8. <span data-ttu-id="bd68b-116">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="bd68b-116">Click Designer.</span></span>
9. <span data-ttu-id="bd68b-117">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="bd68b-118">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="bd68b-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="bd68b-119">ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'</span><span class="sxs-lookup"><span data-stu-id="bd68b-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="bd68b-120">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-120">Click OK.</span></span>
13. <span data-ttu-id="bd68b-121">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="bd68b-122">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="bd68b-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="bd68b-123">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="bd68b-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="bd68b-124">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-124">Click OK.</span></span>
17. <span data-ttu-id="bd68b-125">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="bd68b-126">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="bd68b-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="bd68b-127">ในฟิลด์ชื่อ ให้พิมพ์ 'สมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="bd68b-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="bd68b-128">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-128">Click OK.</span></span>
21. <span data-ttu-id="bd68b-129">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="bd68b-130">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="bd68b-131">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="bd68b-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="bd68b-132">ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="bd68b-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="bd68b-133">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-133">Click OK.</span></span>
26. <span data-ttu-id="bd68b-134">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="bd68b-135">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="bd68b-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="bd68b-136">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="bd68b-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="bd68b-137">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-137">Click OK.</span></span>
30. <span data-ttu-id="bd68b-138">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="bd68b-139">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="bd68b-140">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="bd68b-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="bd68b-141">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="bd68b-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="bd68b-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-142">Click OK.</span></span>
35. <span data-ttu-id="bd68b-143">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd68b-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="bd68b-144">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="bd68b-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="bd68b-145">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-145">Click OK.</span></span>
38. <span data-ttu-id="bd68b-146">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd68b-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="bd68b-147">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="bd68b-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="bd68b-148">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-148">Click OK.</span></span>
41. <span data-ttu-id="bd68b-149">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd68b-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="bd68b-150">ในฟิลด์ ชื่อ ให้พิมพ์ 'Dt'</span><span class="sxs-lookup"><span data-stu-id="bd68b-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="bd68b-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-151">Click OK.</span></span>
44. <span data-ttu-id="bd68b-152">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd68b-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="bd68b-153">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Ct'</span><span class="sxs-lookup"><span data-stu-id="bd68b-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="bd68b-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-154">Click OK.</span></span>
47. <span data-ttu-id="bd68b-155">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="bd68b-156">ในแผนภูมิ เลือก 'XML\องค์ประกอบ'</span><span class="sxs-lookup"><span data-stu-id="bd68b-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="bd68b-157">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Dimensions'</span><span class="sxs-lookup"><span data-stu-id="bd68b-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="bd68b-158">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bd68b-158">Click OK.</span></span>
51. <span data-ttu-id="bd68b-159">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="bd68b-160">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bd68b-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="bd68b-161">ในแผนภูมิ เลือก 'XML\แอททริบิวต์'</span><span class="sxs-lookup"><span data-stu-id="bd68b-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="bd68b-162">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="bd68b-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="bd68b-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-163">Click OK.</span></span>
56. <span data-ttu-id="bd68b-164">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd68b-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="bd68b-165">ในฟิลด์ ชื่อ ให้พิมพ์ 'Value'</span><span class="sxs-lookup"><span data-stu-id="bd68b-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="bd68b-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-166">Click OK.</span></span>
59. <span data-ttu-id="bd68b-167">คลิก เพิ่มแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd68b-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="bd68b-168">ในฟิลด์ ชื่อ ให้พิมพ์ชื่อ 'Desc'</span><span class="sxs-lookup"><span data-stu-id="bd68b-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="bd68b-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd68b-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="bd68b-170">แม็ปองค์ประกอบของรายงานไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bd68b-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="bd68b-171">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="bd68b-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="bd68b-172">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="bd68b-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bd68b-173">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="bd68b-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="bd68b-174">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="bd68b-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="bd68b-175">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="bd68b-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="bd68b-176">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\คำอธิบาย: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="bd68b-177">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\คำอธิบาย: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="bd68b-178">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-178">Click Bind.</span></span>
9. <span data-ttu-id="bd68b-179">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\ค่า: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="bd68b-180">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="bd68b-181">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-181">Click Bind.</span></span>
12. <span data-ttu-id="bd68b-182">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML\รหัส: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="bd68b-183">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\ชื่อ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="bd68b-184">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-184">Click Bind.</span></span>
15. <span data-ttu-id="bd68b-185">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="bd68b-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="bd68b-186">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\มิติ: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="bd68b-187">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-187">Click Bind.</span></span>
18. <span data-ttu-id="bd68b-188">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\Ct: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="bd68b-189">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เครดิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="bd68b-190">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-190">Click Bind.</span></span>
21. <span data-ttu-id="bd68b-191">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\Dt: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="bd68b-192">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เดบิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="bd68b-193">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-193">Click Bind.</span></span>
24. <span data-ttu-id="bd68b-194">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\สกุลเงิน: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="bd68b-195">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\สกุลเงิน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="bd68b-196">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-196">Click Bind.</span></span>
27. <span data-ttu-id="bd68b-197">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\วันที่: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="bd68b-198">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\วันที่: วันที่'</span><span class="sxs-lookup"><span data-stu-id="bd68b-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="bd68b-199">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-199">Click Bind.</span></span>
30. <span data-ttu-id="bd68b-200">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML\ใบสำคัญ: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="bd68b-201">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ใบสำคัญ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="bd68b-202">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-202">Click Bind.</span></span>
33. <span data-ttu-id="bd68b-203">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ธุรกรรม: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="bd68b-204">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="bd68b-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="bd68b-205">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-205">Click Bind.</span></span>
36. <span data-ttu-id="bd68b-206">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML\ชุดงาน: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="bd68b-207">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="bd68b-208">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-208">Click Bind.</span></span>
39. <span data-ttu-id="bd68b-209">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\สมุดรายวัน: องค์ประกอบ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="bd68b-210">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="bd68b-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="bd68b-211">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-211">Click Bind.</span></span>
42. <span data-ttu-id="bd68b-212">ในแผนภูมิ เลือก 'ราก: องค์ประกอบ XML\บริษัท: แอททริบิวต์ XML'</span><span class="sxs-lookup"><span data-stu-id="bd68b-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="bd68b-213">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\บริษัท: สตริง'</span><span class="sxs-lookup"><span data-stu-id="bd68b-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="bd68b-214">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bd68b-214">Click Bind.</span></span>
45. <span data-ttu-id="bd68b-215">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bd68b-215">Click Save.</span></span>
46. <span data-ttu-id="bd68b-216">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bd68b-216">Close the page.</span></span>

