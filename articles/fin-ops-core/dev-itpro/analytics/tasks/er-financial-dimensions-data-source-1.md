---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1 - ออกแบบแบบจำลองข้อมูล)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกแบบโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลของรายงาน ER (ส่วนที่ 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570203"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="f1596-104">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1 - ออกแบบแบบจำลองข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="f1596-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1596-105">ขั้นตอนต่อไปนี้อธิบายว่าผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER ได้อย่างไร </span><span class="sxs-lookup"><span data-stu-id="f1596-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f1596-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="f1596-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f1596-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์ "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="f1596-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="f1596-108">สร้างแบบจำลองข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="f1596-108">Create a new data model</span></span>
1. <span data-ttu-id="f1596-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f1596-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f1596-110">ตรวจสอบให้แน่ใจว่า "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="f1596-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="f1596-111">พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f1596-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f1596-112">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="f1596-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f1596-113">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f1596-114">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f1596-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="f1596-115">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f1596-115">Click Create configuration.</span></span>
6. <span data-ttu-id="f1596-116">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f1596-116">Click Designer.</span></span>
7. <span data-ttu-id="f1596-117">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="f1596-118">ในฟิลด์ชื่อ ให้พิมพ์ 'รายการ'</span><span class="sxs-lookup"><span data-stu-id="f1596-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="f1596-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-119">Click Add.</span></span>
10. <span data-ttu-id="f1596-120">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="f1596-121">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f1596-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="f1596-122">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-122">Click Add.</span></span>
    * <span data-ttu-id="f1596-123">เราจะเพิ่มรายการเรกคอร์ดใหม่ไปยังแบบจำลองของเรา </span><span class="sxs-lookup"><span data-stu-id="f1596-123">We will add to our model a new record list.</span></span> <span data-ttu-id="f1596-124">รายการนี้จะแสดงถึง (สำหรับรายงาน ER ใดๆ โดยใช้แบบจำลองนี้เป็นแหล่งข้อมูล) การตั้งค่าของมิติทางการเงินที่เลือก </span><span class="sxs-lookup"><span data-stu-id="f1596-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="f1596-125">มิติทางการเงินแต่ละรายการจะปรากฏในรายการนี้โดยเป็นเรกคอร์ดที่มีฟิลด์ที่เหมาะสมซึ่งแสดงถึงการตั้งค่าของมิติ</span><span class="sxs-lookup"><span data-stu-id="f1596-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="f1596-126">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="f1596-127">ในฟิลด์ ชื่อ ให้พิมพ์ 'การตั้งค่ามิติ'</span><span class="sxs-lookup"><span data-stu-id="f1596-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="f1596-128">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="f1596-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="f1596-129">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-129">Click Add.</span></span>
17. <span data-ttu-id="f1596-130">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="f1596-131">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="f1596-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="f1596-132">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="f1596-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="f1596-133">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-133">Click Add.</span></span>
21. <span data-ttu-id="f1596-134">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="f1596-135">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="f1596-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="f1596-136">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-136">Click Add.</span></span>
24. <span data-ttu-id="f1596-137">ในแผนภูมิ ให้เลือก 'รายการ'</span><span class="sxs-lookup"><span data-stu-id="f1596-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="f1596-138">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="f1596-139">ในฟิลด์ชื่อ ให้พิมพ์ 'สมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="f1596-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="f1596-140">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="f1596-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="f1596-141">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-141">Click Add.</span></span>
29. <span data-ttu-id="f1596-142">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="f1596-143">ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="f1596-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="f1596-144">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="f1596-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="f1596-145">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-145">Click Add.</span></span>
33. <span data-ttu-id="f1596-146">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="f1596-147">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="f1596-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="f1596-148">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="f1596-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="f1596-149">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-149">Click Add.</span></span>
37. <span data-ttu-id="f1596-150">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="f1596-151">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="f1596-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="f1596-152">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="f1596-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="f1596-153">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-153">Click Add.</span></span>
41. <span data-ttu-id="f1596-154">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="f1596-155">ในฟิลด์ชื่อ ให้พิมพ์ 'เดบิต'</span><span class="sxs-lookup"><span data-stu-id="f1596-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="f1596-156">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="f1596-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="f1596-157">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-157">Click Add.</span></span>
45. <span data-ttu-id="f1596-158">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="f1596-159">ในฟิลด์ชื่อ ให้พิมพ์ 'เครดิต'</span><span class="sxs-lookup"><span data-stu-id="f1596-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="f1596-160">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-160">Click Add.</span></span>
48. <span data-ttu-id="f1596-161">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="f1596-162">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="f1596-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="f1596-163">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="f1596-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="f1596-164">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-164">Click Add.</span></span>
52. <span data-ttu-id="f1596-165">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="f1596-166">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="f1596-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="f1596-167">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-167">Click Add.</span></span>
55. <span data-ttu-id="f1596-168">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="f1596-169">ในฟิลด์ ชื่อ ให้พิมพ์ 'ข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="f1596-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="f1596-170">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="f1596-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="f1596-171">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-171">Click Add.</span></span>
    * <span data-ttu-id="f1596-172">เราได้เพิ่มรายการเรกคอร์ดใหม่ไปยังแบบจำลองของเราแล้ว </span><span class="sxs-lookup"><span data-stu-id="f1596-172">We added to our model a new record list.</span></span> <span data-ttu-id="f1596-173">รายการนี้จะแสดงถึง (สำหรับรายงาน ER ใดๆ โดยใช้แบบจำลองนี้เป็นแหล่งข้อมูล) ค่าของมิติทางการเงินที่เลือก </span><span class="sxs-lookup"><span data-stu-id="f1596-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="f1596-174">มิติทางการเงินแต่ละรายการจะปรากฏในรายการนี้โดยเป็นเรกคอร์ดที่มีฟิลด์ที่เหมาะสมซึ่งแสดงถึงค่าของมิติ</span><span class="sxs-lookup"><span data-stu-id="f1596-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="f1596-175">และชื่อมิติจะปรากฏในเรกคอร์ดนี้โดยเป็นฟิลด์ที่จะใช้ ถ้าจำเป็น สำหรับวัตถุประสงค์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f1596-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="f1596-176">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="f1596-177">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="f1596-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="f1596-178">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="f1596-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="f1596-179">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-179">Click Add.</span></span>
63. <span data-ttu-id="f1596-180">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="f1596-181">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="f1596-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="f1596-182">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-182">Click Add.</span></span>
66. <span data-ttu-id="f1596-183">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f1596-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="f1596-184">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="f1596-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="f1596-185">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f1596-185">Click Add.</span></span>
69. <span data-ttu-id="f1596-186">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f1596-186">Click Save.</span></span>
70. <span data-ttu-id="f1596-187">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f1596-187">Close the page.</span></span>

![เพจตัวออกแบบแบบจำลองข้อมูล ER](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]