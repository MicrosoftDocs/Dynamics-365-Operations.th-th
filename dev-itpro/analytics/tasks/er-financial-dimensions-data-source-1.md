--- 
title: "ออกแบบแบบจำลองข้อมูลเพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายว่าผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER ได้อย่างไร "
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0953ffb3a98d4f2852caecc3a59792698d1c9d9b
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="adecc-103">ออกแบบแบบจำลองข้อมูลเพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="adecc-103">Design data model to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="adecc-104">ขั้นตอนต่อไปนี้อธิบายว่าผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER ได้อย่างไร </span><span class="sxs-lookup"><span data-stu-id="adecc-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="adecc-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="adecc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="adecc-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์ "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="adecc-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="adecc-107">สร้างแบบจำลองข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="adecc-107">Create a new data model</span></span>
1. <span data-ttu-id="adecc-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="adecc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="adecc-109">ตรวจสอบให้แน่ใจว่า "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="adecc-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="adecc-110">พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="adecc-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="adecc-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="adecc-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="adecc-112">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="adecc-113">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="adecc-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="adecc-114">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="adecc-114">Click Create configuration.</span></span>
6. <span data-ttu-id="adecc-115">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="adecc-115">Click Designer.</span></span>
7. <span data-ttu-id="adecc-116">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="adecc-117">ในฟิลด์ชื่อ ให้พิมพ์ 'รายการ'</span><span class="sxs-lookup"><span data-stu-id="adecc-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="adecc-118">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-118">Click Add.</span></span>
10. <span data-ttu-id="adecc-119">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="adecc-120">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="adecc-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="adecc-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-121">Click Add.</span></span>
    * <span data-ttu-id="adecc-122">เราจะเพิ่มรายการเรกคอร์ดใหม่ไปยังแบบจำลองของเรา </span><span class="sxs-lookup"><span data-stu-id="adecc-122">We will add to our model a new record list.</span></span> <span data-ttu-id="adecc-123">รายการนี้จะแสดงถึง (สำหรับรายงาน ER ใดๆ โดยใช้แบบจำลองนี้เป็นแหล่งข้อมูล) การตั้งค่าของมิติทางการเงินที่เลือก </span><span class="sxs-lookup"><span data-stu-id="adecc-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="adecc-124">แต่ละมิติทางการเงินจะปรากฏในรายการนี้โดยเป็นเรกคอร์ดที่มีฟิลด์ที่เหมาะสมที่แสดงถึงการตั้งค่าของมิติ</span><span class="sxs-lookup"><span data-stu-id="adecc-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="adecc-125">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="adecc-126">ในฟิลด์ ชื่อ ให้พิมพ์ 'การตั้งค่ามิติ'</span><span class="sxs-lookup"><span data-stu-id="adecc-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="adecc-127">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="adecc-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="adecc-128">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-128">Click Add.</span></span>
17. <span data-ttu-id="adecc-129">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="adecc-130">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="adecc-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="adecc-131">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="adecc-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="adecc-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-132">Click Add.</span></span>
21. <span data-ttu-id="adecc-133">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="adecc-134">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="adecc-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="adecc-135">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-135">Click Add.</span></span>
24. <span data-ttu-id="adecc-136">ในแผนภูมิ ให้เลือก 'รายการ'</span><span class="sxs-lookup"><span data-stu-id="adecc-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="adecc-137">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="adecc-138">ในฟิลด์ชื่อ ให้พิมพ์ 'สมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="adecc-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="adecc-139">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="adecc-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="adecc-140">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-140">Click Add.</span></span>
29. <span data-ttu-id="adecc-141">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="adecc-142">ในฟิลด์ชื่อ ให้พิมพ์ชื่อ 'ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="adecc-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="adecc-143">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="adecc-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="adecc-144">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-144">Click Add.</span></span>
33. <span data-ttu-id="adecc-145">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="adecc-146">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="adecc-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="adecc-147">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="adecc-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="adecc-148">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-148">Click Add.</span></span>
37. <span data-ttu-id="adecc-149">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="adecc-150">ในฟิลด์ชื่อ ให้พิมพ์ 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="adecc-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="adecc-151">ในฟิลด์ประเภทสินค้า ให้เลือก 'วันที่'</span><span class="sxs-lookup"><span data-stu-id="adecc-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="adecc-152">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-152">Click Add.</span></span>
41. <span data-ttu-id="adecc-153">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="adecc-154">ในฟิลด์ชื่อ ให้พิมพ์ 'เดบิต'</span><span class="sxs-lookup"><span data-stu-id="adecc-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="adecc-155">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="adecc-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="adecc-156">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-156">Click Add.</span></span>
45. <span data-ttu-id="adecc-157">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="adecc-158">ในฟิลด์ชื่อ ให้พิมพ์ 'เครดิต'</span><span class="sxs-lookup"><span data-stu-id="adecc-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="adecc-159">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-159">Click Add.</span></span>
48. <span data-ttu-id="adecc-160">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="adecc-161">ในฟิลด์ชื่อ ให้พิมพ์ 'สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="adecc-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="adecc-162">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="adecc-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="adecc-163">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-163">Click Add.</span></span>
52. <span data-ttu-id="adecc-164">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="adecc-165">ในฟิลด์ชื่อ ให้พิมพ์ 'ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="adecc-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="adecc-166">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-166">Click Add.</span></span>
55. <span data-ttu-id="adecc-167">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="adecc-168">ในฟิลด์ ชื่อ ให้พิมพ์ 'ข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="adecc-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="adecc-169">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="adecc-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="adecc-170">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-170">Click Add.</span></span>
    * <span data-ttu-id="adecc-171">เราได้เพิ่มรายการเรกคอร์ดใหม่ไปยังแบบจำลองของเราแล้ว </span><span class="sxs-lookup"><span data-stu-id="adecc-171">We added to our model a new record list.</span></span> <span data-ttu-id="adecc-172">รายการนี้จะแสดงถึง (สำหรับรายงาน ER ใดๆ โดยใช้แบบจำลองนี้เป็นแหล่งข้อมูล) ค่าของมิติทางการเงินที่เลือก </span><span class="sxs-lookup"><span data-stu-id="adecc-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="adecc-173">แต่ละมิติทางการเงินจะปรากฏในรายการนี้โดยเป็นเรกคอร์ดที่มีฟิลด์ที่เหมาะสมที่แสดงถึงการตั้งค่าของมิติ </span><span class="sxs-lookup"><span data-stu-id="adecc-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="adecc-174">และชื่อมิติจะปรากฏในเรกคอร์ดนี้โดยเป็นฟิลด์ที่จะใช้ ถ้าจำเป็น สำหรับวัตถุประสงค์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="adecc-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="adecc-175">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="adecc-176">ในฟิลด์ชื่อ ให้พิมพ์ 'รหัส'</span><span class="sxs-lookup"><span data-stu-id="adecc-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="adecc-177">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="adecc-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="adecc-178">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-178">Click Add.</span></span>
63. <span data-ttu-id="adecc-179">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="adecc-180">ในฟิลด์ชื่อ ให้พิมพ์ 'คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="adecc-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="adecc-181">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-181">Click Add.</span></span>
66. <span data-ttu-id="adecc-182">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="adecc-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="adecc-183">ในฟิลด์ชื่อ พิมพ์ 'ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="adecc-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="adecc-184">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="adecc-184">Click Add.</span></span>
69. <span data-ttu-id="adecc-185">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="adecc-185">Click Save.</span></span>
70. <span data-ttu-id="adecc-186">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="adecc-186">Close the page.</span></span>


