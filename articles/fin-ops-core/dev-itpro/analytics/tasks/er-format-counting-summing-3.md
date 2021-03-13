---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 3 - ใช้การคำนวณในการสร้างผลลัพธ์)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อตรวจนับและรวมตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว (ส่วนที่ 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092983"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="4bbee-104">ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 3 - ใช้การคำนวณในการสร้างผลลัพธ์)</span><span class="sxs-lookup"><span data-stu-id="4bbee-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bbee-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="4bbee-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="4bbee-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="4bbee-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4bbee-107">เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 2: ตั้งค่าคอนฟิกการคำนวณ)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bbee-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="4bbee-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="4bbee-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="4bbee-109">ตั้งค่าคอนฟิกรายงานนี้เพื่อใช้การตรวจนับและการสรุปข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4bbee-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="4bbee-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4bbee-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4bbee-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="4bbee-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4bbee-112">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="4bbee-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="4bbee-113">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="4bbee-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="4bbee-114">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="4bbee-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="4bbee-115">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="4bbee-115">Click Designer.</span></span>
7. <span data-ttu-id="4bbee-116">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="4bbee-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="4bbee-117">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4bbee-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="4bbee-118">เพิ่มแหล่งข้อมูลใหม่เพื่อดึงข้อมูลรายการของบล็อคที่จดจำไว้</span><span class="sxs-lookup"><span data-stu-id="4bbee-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="4bbee-119">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="4bbee-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="4bbee-120">ในฟิลด์ชื่อ ให้พิมพ์ '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="4bbee-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="4bbee-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="4bbee-121">$BlocksList</span></span>  
11. <span data-ttu-id="4bbee-122">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="4bbee-122">Click Edit formula.</span></span>
12. <span data-ttu-id="4bbee-123">ในแผนภูมิ ให้เลือก 'ฟังก์ชันการรวบรวมข้อมูล\COLLECTEDLIST'</span><span class="sxs-lookup"><span data-stu-id="4bbee-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="4bbee-124">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4bbee-124">Click Add function.</span></span>
14. <span data-ttu-id="4bbee-125">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4bbee-125">Click Add data source.</span></span>
15. <span data-ttu-id="4bbee-126">ในฟิลด์สูตร ให้ป้อน 'COLLECTEDLIST('$BlockName', '</span><span class="sxs-lookup"><span data-stu-id="4bbee-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="4bbee-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4bbee-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="4bbee-128">ในฟิลด์สูตร ให้ป้อน 'COLLECTEDLIST('$BlockName', "\*")'</span><span class="sxs-lookup"><span data-stu-id="4bbee-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="4bbee-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="4bbee-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="4bbee-130">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4bbee-130">Click Save.</span></span>
    * <span data-ttu-id="4bbee-131">รูปแบบ "\*" หมายความว่าบล็อคทั้งหมดจะถูกรวมไว้ในรายการสำหรับเรกคอร์ดนี้</span><span class="sxs-lookup"><span data-stu-id="4bbee-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="4bbee-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bbee-132">Close the page.</span></span>
19. <span data-ttu-id="4bbee-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bbee-133">Click OK.</span></span>
20. <span data-ttu-id="4bbee-134">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4bbee-134">Click the Format tab.</span></span>
21. <span data-ttu-id="4bbee-135">ในแผนภูมิ ให้เลือก 'Intrastat\Data'</span><span class="sxs-lookup"><span data-stu-id="4bbee-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="4bbee-136">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4bbee-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="4bbee-137">ในแผนภูมิ ให้เลือก 'ข้อความ\ลำดับ'</span><span class="sxs-lookup"><span data-stu-id="4bbee-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="4bbee-138">ในฟิลด์ชื่อ ให้พิมพ์ 'ผลรวมโดยเรียงตามบล็อค'</span><span class="sxs-lookup"><span data-stu-id="4bbee-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="4bbee-139">ผลรวมโดยเรียงตามบล็อค</span><span class="sxs-lookup"><span data-stu-id="4bbee-139">Totals by blocks</span></span>  
25. <span data-ttu-id="4bbee-140">ในฟิลด์อักขระพิเศษ ให้เลือก 'รายการใหม่ - Windows (CR LF)'</span><span class="sxs-lookup"><span data-stu-id="4bbee-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="4bbee-141">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4bbee-141">Click OK.</span></span>
27. <span data-ttu-id="4bbee-142">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks'</span><span class="sxs-lookup"><span data-stu-id="4bbee-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="4bbee-143">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="4bbee-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="4bbee-144">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="4bbee-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="4bbee-145">ในฟิลด์ชื่อ พิมพ์ 'รหัสบล็อค'</span><span class="sxs-lookup"><span data-stu-id="4bbee-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="4bbee-146">รหัสบล็อค</span><span class="sxs-lookup"><span data-stu-id="4bbee-146">Block code</span></span>  
31. <span data-ttu-id="4bbee-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bbee-147">Click OK.</span></span>
32. <span data-ttu-id="4bbee-148">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="4bbee-148">Click Add String.</span></span>
33. <span data-ttu-id="4bbee-149">ในฟิลด์ชื่อ ให้พิมพ์ 'การตรวจนับจำนวนบรรทัด'</span><span class="sxs-lookup"><span data-stu-id="4bbee-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="4bbee-150">การตรวจนับจำนวนบรรทัด</span><span class="sxs-lookup"><span data-stu-id="4bbee-150">Lines counting</span></span>  
34. <span data-ttu-id="4bbee-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bbee-151">Click OK.</span></span>
35. <span data-ttu-id="4bbee-152">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="4bbee-152">Click Add String.</span></span>
36. <span data-ttu-id="4bbee-153">ในฟิลด์ชื่อ พิมพ์ 'จำนวนเงินรวม'</span><span class="sxs-lookup"><span data-stu-id="4bbee-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="4bbee-154">ยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="4bbee-154">Total amount</span></span>  
37. <span data-ttu-id="4bbee-155">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bbee-155">Click OK.</span></span>
38. <span data-ttu-id="4bbee-156">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="4bbee-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="4bbee-157">ในแผนภูมิ ให้เลือก '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="4bbee-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="4bbee-158">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="4bbee-158">Click Bind.</span></span>
    * <span data-ttu-id="4bbee-159">สร้างบรรทัดสรุปสำหรับแต่ละบล็อคที่จดจำไว้</span><span class="sxs-lookup"><span data-stu-id="4bbee-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="4bbee-160">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4bbee-160">Click the Format tab.</span></span>
42. <span data-ttu-id="4bbee-161">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks\Block code'</span><span class="sxs-lookup"><span data-stu-id="4bbee-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="4bbee-162">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="4bbee-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="4bbee-163">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="4bbee-163">Click Edit formula.</span></span>
45. <span data-ttu-id="4bbee-164">ในฟิลด์สูตร ให้ป้อน '"รหัสบล็อค: " & '</span><span class="sxs-lookup"><span data-stu-id="4bbee-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="4bbee-165">"รหัสบล็อค: " &</span><span class="sxs-lookup"><span data-stu-id="4bbee-165">"Block id: " &</span></span>  
46. <span data-ttu-id="4bbee-166">ในแผนภูมิ ให้ขยาย '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="4bbee-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="4bbee-167">ในแผนภูมิ ให้เลือก '$BlocksList\Value'</span><span class="sxs-lookup"><span data-stu-id="4bbee-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="4bbee-168">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4bbee-168">Click Add data source.</span></span>
49. <span data-ttu-id="4bbee-169">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4bbee-169">Click Save.</span></span>
50. <span data-ttu-id="4bbee-170">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bbee-170">Close the page.</span></span>
51. <span data-ttu-id="4bbee-171">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4bbee-171">Click the Format tab.</span></span>
52. <span data-ttu-id="4bbee-172">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks\Lines counting'</span><span class="sxs-lookup"><span data-stu-id="4bbee-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="4bbee-173">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="4bbee-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="4bbee-174">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="4bbee-174">Click Edit formula.</span></span>
    * <span data-ttu-id="4bbee-175">สร้างผลลัพธ์สำหรับจำนวนของบรรทัดของแต่ละบล็อคที่แสดงอยู่ในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="4bbee-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="4bbee-176">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & '</span><span class="sxs-lookup"><span data-stu-id="4bbee-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="4bbee-177">"จำนวนบรรทัดในบล็อคนี้: " &</span><span class="sxs-lookup"><span data-stu-id="4bbee-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="4bbee-178">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT('</span><span class="sxs-lookup"><span data-stu-id="4bbee-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="4bbee-179">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="4bbee-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="4bbee-180">ในแผนภูมิ ให้เลือก 'Data collection functions\COUNTIFS'</span><span class="sxs-lookup"><span data-stu-id="4bbee-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="4bbee-181">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4bbee-181">Click Add function.</span></span>
59. <span data-ttu-id="4bbee-182">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4bbee-182">Click Add data source.</span></span>
60. <span data-ttu-id="4bbee-183">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '</span><span class="sxs-lookup"><span data-stu-id="4bbee-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="4bbee-184">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4bbee-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="4bbee-185">ในแผนภูมิ ให้ขยาย '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="4bbee-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="4bbee-186">ในแผนภูมิ ให้เลือก '$BlocksList\Value'</span><span class="sxs-lookup"><span data-stu-id="4bbee-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="4bbee-187">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4bbee-187">Click Add data source.</span></span>
64. <span data-ttu-id="4bbee-188">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '</span><span class="sxs-lookup"><span data-stu-id="4bbee-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="4bbee-189">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="4bbee-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="4bbee-190">ในแผนภูมิ ให้เลือก '$RecName'</span><span class="sxs-lookup"><span data-stu-id="4bbee-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="4bbee-191">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4bbee-191">Click Add data source.</span></span>
67. <span data-ttu-id="4bbee-192">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'</span><span class="sxs-lookup"><span data-stu-id="4bbee-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="4bbee-193">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="4bbee-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="4bbee-194">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4bbee-194">Click Save.</span></span>
69. <span data-ttu-id="4bbee-195">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bbee-195">Close the page.</span></span>
70. <span data-ttu-id="4bbee-196">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4bbee-196">Click the Format tab.</span></span>
71. <span data-ttu-id="4bbee-197">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks\Total amount'</span><span class="sxs-lookup"><span data-stu-id="4bbee-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="4bbee-198">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="4bbee-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="4bbee-199">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="4bbee-199">Click Edit formula.</span></span>
    * <span data-ttu-id="4bbee-200">สร้างผลลัพธ์ที่จะเป็นผลรวมของยอดเงินที่ออกใบแจ้งหนี้สำหรับแต่ละบล็อคที่แสดงอยู่ในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="4bbee-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="4bbee-201">ในฟิลด์สูตร ให้ป้อน '"ผลรวมของยอดเงินที่ออกใบแจ้งหนี้: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'</span><span class="sxs-lookup"><span data-stu-id="4bbee-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="4bbee-202">"ผลรวมของยอดเงินที่ออกใบแจ้งหนี้: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="4bbee-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="4bbee-203">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4bbee-203">Click Save.</span></span>
76. <span data-ttu-id="4bbee-204">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bbee-204">Close the page.</span></span>
77. <span data-ttu-id="4bbee-205">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4bbee-205">Click Save.</span></span>
78. <span data-ttu-id="4bbee-206">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bbee-206">Close the page.</span></span>

