--- 
title: "ใช้การคำนวณเพื่อสร้างผลลัพธ์สำหรับการตรวจนับและการรวม"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว "
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5b7f0cc5b94ab7be11a013ef3e5909d84847e885
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing"></a><span data-ttu-id="7f87b-103">ใช้การคำนวณเพื่อสร้างผลลัพธ์สำหรับการตรวจนับและการรวม</span><span class="sxs-lookup"><span data-stu-id="7f87b-103">Use computations to make the output for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f87b-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="7f87b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="7f87b-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="7f87b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7f87b-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 2: ตั้งค่าการคำนวณ)"</span><span class="sxs-lookup"><span data-stu-id="7f87b-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="7f87b-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="7f87b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="7f87b-108">ตั้งค่าคอนฟิกรายงานนี้เพื่อใช้การตรวจนับและการสรุปข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f87b-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="7f87b-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="7f87b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7f87b-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="7f87b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7f87b-111">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="7f87b-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="7f87b-112">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="7f87b-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="7f87b-113">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="7f87b-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="7f87b-114">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="7f87b-114">Click Designer.</span></span>
7. <span data-ttu-id="7f87b-115">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="7f87b-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="7f87b-116">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7f87b-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="7f87b-117">เพิ่มแหล่งข้อมูลใหม่เพื่อดึงข้อมูลรายการของบล็อคที่จดจำไว้</span><span class="sxs-lookup"><span data-stu-id="7f87b-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="7f87b-118">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="7f87b-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="7f87b-119">ในฟิลด์ชื่อ ให้พิมพ์ '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="7f87b-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="7f87b-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="7f87b-120">$BlocksList</span></span>  
11. <span data-ttu-id="7f87b-121">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="7f87b-121">Click Edit formula.</span></span>
12. <span data-ttu-id="7f87b-122">ในแผนภูมิ ให้เลือก 'ฟังก์ชันการรวบรวมข้อมูล\COLLECTEDLIST'</span><span class="sxs-lookup"><span data-stu-id="7f87b-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="7f87b-123">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="7f87b-123">Click Add function.</span></span>
14. <span data-ttu-id="7f87b-124">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f87b-124">Click Add data source.</span></span>
15. <span data-ttu-id="7f87b-125">ในฟิลด์สูตร ให้ป้อน 'COLLECTEDLIST('$BlockName', '</span><span class="sxs-lookup"><span data-stu-id="7f87b-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="7f87b-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="7f87b-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="7f87b-127">ในฟิลด์สูตร ให้ป้อน 'COLLECTEDLIST('$BlockName', "\*")'</span><span class="sxs-lookup"><span data-stu-id="7f87b-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="7f87b-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="7f87b-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="7f87b-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7f87b-129">Click Save.</span></span>
    * <span data-ttu-id="7f87b-130">รูปแบบ "\*" หมายความว่าบล็อคทั้งหมดจะถูกรวมไว้ในรายการสำหรับเรกคอร์ดนี้</span><span class="sxs-lookup"><span data-stu-id="7f87b-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="7f87b-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f87b-131">Close the page.</span></span>
19. <span data-ttu-id="7f87b-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7f87b-132">Click OK.</span></span>
20. <span data-ttu-id="7f87b-133">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="7f87b-133">Click the Format tab.</span></span>
21. <span data-ttu-id="7f87b-134">ในแผนภูมิ ให้เลือก 'Intrastat\Data'</span><span class="sxs-lookup"><span data-stu-id="7f87b-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="7f87b-135">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7f87b-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="7f87b-136">ในแผนภูมิ ให้เลือก 'ข้อความ\ลำดับ'</span><span class="sxs-lookup"><span data-stu-id="7f87b-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="7f87b-137">ในฟิลด์ชื่อ ให้พิมพ์ 'ผลรวมโดยเรียงตามบล็อค'</span><span class="sxs-lookup"><span data-stu-id="7f87b-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="7f87b-138">ผลรวมโดยเรียงตามบล็อค</span><span class="sxs-lookup"><span data-stu-id="7f87b-138">Totals by blocks</span></span>  
25. <span data-ttu-id="7f87b-139">ในฟิลด์อักขระพิเศษ ให้เลือก 'รายการใหม่ - Windows (CR LF)'</span><span class="sxs-lookup"><span data-stu-id="7f87b-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="7f87b-140">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7f87b-140">Click OK.</span></span>
27. <span data-ttu-id="7f87b-141">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks'</span><span class="sxs-lookup"><span data-stu-id="7f87b-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="7f87b-142">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7f87b-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="7f87b-143">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="7f87b-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="7f87b-144">ในฟิลด์ชื่อ พิมพ์ 'รหัสบล็อค'</span><span class="sxs-lookup"><span data-stu-id="7f87b-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="7f87b-145">รหัสบล็อค</span><span class="sxs-lookup"><span data-stu-id="7f87b-145">Block code</span></span>  
31. <span data-ttu-id="7f87b-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7f87b-146">Click OK.</span></span>
32. <span data-ttu-id="7f87b-147">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="7f87b-147">Click Add String.</span></span>
33. <span data-ttu-id="7f87b-148">ในฟิลด์ชื่อ ให้พิมพ์ 'การตรวจนับจำนวนบรรทัด'</span><span class="sxs-lookup"><span data-stu-id="7f87b-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="7f87b-149">การตรวจนับจำนวนบรรทัด</span><span class="sxs-lookup"><span data-stu-id="7f87b-149">Lines counting</span></span>  
34. <span data-ttu-id="7f87b-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7f87b-150">Click OK.</span></span>
35. <span data-ttu-id="7f87b-151">คลิกเพิ่มสตริง</span><span class="sxs-lookup"><span data-stu-id="7f87b-151">Click Add String.</span></span>
36. <span data-ttu-id="7f87b-152">ในฟิลด์ชื่อ พิมพ์ 'จำนวนเงินรวม'</span><span class="sxs-lookup"><span data-stu-id="7f87b-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="7f87b-153">ยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="7f87b-153">Total amount</span></span>  
37. <span data-ttu-id="7f87b-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7f87b-154">Click OK.</span></span>
38. <span data-ttu-id="7f87b-155">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="7f87b-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="7f87b-156">ในแผนภูมิ ให้เลือก '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="7f87b-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="7f87b-157">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="7f87b-157">Click Bind.</span></span>
    * <span data-ttu-id="7f87b-158">สร้างบรรทัดสรุปสำหรับแต่ละบล็อคที่จดจำไว้</span><span class="sxs-lookup"><span data-stu-id="7f87b-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="7f87b-159">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="7f87b-159">Click the Format tab.</span></span>
42. <span data-ttu-id="7f87b-160">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks\Block code'</span><span class="sxs-lookup"><span data-stu-id="7f87b-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="7f87b-161">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="7f87b-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="7f87b-162">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="7f87b-162">Click Edit formula.</span></span>
45. <span data-ttu-id="7f87b-163">ในฟิลด์สูตร ให้ป้อน '"รหัสบล็อค: " & '</span><span class="sxs-lookup"><span data-stu-id="7f87b-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="7f87b-164">"รหัสบล็อค: " &</span><span class="sxs-lookup"><span data-stu-id="7f87b-164">"Block id: " &</span></span>  
46. <span data-ttu-id="7f87b-165">ในแผนภูมิ ให้ขยาย '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="7f87b-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="7f87b-166">ในแผนภูมิ ให้เลือก '$BlocksList\Value'</span><span class="sxs-lookup"><span data-stu-id="7f87b-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="7f87b-167">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f87b-167">Click Add data source.</span></span>
49. <span data-ttu-id="7f87b-168">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7f87b-168">Click Save.</span></span>
50. <span data-ttu-id="7f87b-169">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f87b-169">Close the page.</span></span>
51. <span data-ttu-id="7f87b-170">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="7f87b-170">Click the Format tab.</span></span>
52. <span data-ttu-id="7f87b-171">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks\Lines counting'</span><span class="sxs-lookup"><span data-stu-id="7f87b-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="7f87b-172">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="7f87b-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="7f87b-173">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="7f87b-173">Click Edit formula.</span></span>
    * <span data-ttu-id="7f87b-174">สร้างผลลัพธ์สำหรับจำนวนของบรรทัดของแต่ละบล็อคที่แสดงอยู่ในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="7f87b-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="7f87b-175">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & '</span><span class="sxs-lookup"><span data-stu-id="7f87b-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="7f87b-176">"จำนวนบรรทัดในบล็อคนี้: " &</span><span class="sxs-lookup"><span data-stu-id="7f87b-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="7f87b-177">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT('</span><span class="sxs-lookup"><span data-stu-id="7f87b-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="7f87b-178">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="7f87b-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="7f87b-179">ในแผนภูมิ ให้เลือก 'Data collection functions\COUNTIFS'</span><span class="sxs-lookup"><span data-stu-id="7f87b-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="7f87b-180">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="7f87b-180">Click Add function.</span></span>
59. <span data-ttu-id="7f87b-181">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f87b-181">Click Add data source.</span></span>
60. <span data-ttu-id="7f87b-182">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '</span><span class="sxs-lookup"><span data-stu-id="7f87b-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="7f87b-183">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="7f87b-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="7f87b-184">ในแผนภูมิ ให้ขยาย '$BlocksList'</span><span class="sxs-lookup"><span data-stu-id="7f87b-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="7f87b-185">ในแผนภูมิ ให้เลือก '$BlocksList\Value'</span><span class="sxs-lookup"><span data-stu-id="7f87b-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="7f87b-186">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f87b-186">Click Add data source.</span></span>
64. <span data-ttu-id="7f87b-187">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '</span><span class="sxs-lookup"><span data-stu-id="7f87b-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="7f87b-188">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="7f87b-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="7f87b-189">ในแผนภูมิ ให้เลือก '$RecName'</span><span class="sxs-lookup"><span data-stu-id="7f87b-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="7f87b-190">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f87b-190">Click Add data source.</span></span>
67. <span data-ttu-id="7f87b-191">ในฟิลด์สูตร ป้อน '"จำนวนของรายการในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'</span><span class="sxs-lookup"><span data-stu-id="7f87b-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="7f87b-192">"จำนวนบรรทัดในบล็อคนี้: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="7f87b-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="7f87b-193">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7f87b-193">Click Save.</span></span>
69. <span data-ttu-id="7f87b-194">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f87b-194">Close the page.</span></span>
70. <span data-ttu-id="7f87b-195">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="7f87b-195">Click the Format tab.</span></span>
71. <span data-ttu-id="7f87b-196">ในแผนภูมิ เลือก 'Intrastat\Data\Totals by blocks\Total amount'</span><span class="sxs-lookup"><span data-stu-id="7f87b-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="7f87b-197">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="7f87b-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="7f87b-198">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="7f87b-198">Click Edit formula.</span></span>
    * <span data-ttu-id="7f87b-199">สร้างผลลัพธ์ที่จะเป็นผลรวมของยอดเงินที่ออกใบแจ้งหนี้สำหรับแต่ละบล็อคที่แสดงอยู่ในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="7f87b-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="7f87b-200">ในฟิลด์สูตร ให้ป้อน '"ผลรวมของยอดเงินที่ออกใบแจ้งหนี้: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'</span><span class="sxs-lookup"><span data-stu-id="7f87b-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="7f87b-201">"ผลรวมของยอดเงินที่ออกใบแจ้งหนี้: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="7f87b-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="7f87b-202">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7f87b-202">Click Save.</span></span>
76. <span data-ttu-id="7f87b-203">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f87b-203">Close the page.</span></span>
77. <span data-ttu-id="7f87b-204">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7f87b-204">Click Save.</span></span>
78. <span data-ttu-id="7f87b-205">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7f87b-205">Close the page.</span></span>


