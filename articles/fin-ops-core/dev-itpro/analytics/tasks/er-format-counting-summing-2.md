---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 2 - ตั้งค่าคอนฟิกการคำนวณ)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d785b321037645837dbcbaf28c8ede9b8e97b79
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550613"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="f76ed-103">ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 2 - ตั้งค่าคอนฟิกการคำนวณ)</span><span class="sxs-lookup"><span data-stu-id="f76ed-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f76ed-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="f76ed-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f76ed-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="f76ed-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f76ed-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1: สร้างรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="f76ed-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="f76ed-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="f76ed-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="f76ed-108">สร้างการตั้งค่าคอนฟิกรูปแบบเพื่อเพิ่มรายละเอียดการตรวจนับและการสรุป</span><span class="sxs-lookup"><span data-stu-id="f76ed-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="f76ed-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f76ed-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f76ed-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="f76ed-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f76ed-111">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="f76ed-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="f76ed-112">ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'</span><span class="sxs-lookup"><span data-stu-id="f76ed-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="f76ed-113">สมมติว่าคุณจำเป็นต้องกำหนดรูปแบบที่ระบุโดย Microsoft โดยการเพิ่มบรรทัดพร้อมกับรายละเอียดสรุปที่ส่วนท้ายของรายงานอินทราสแทต </span><span class="sxs-lookup"><span data-stu-id="f76ed-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="f76ed-114">คุณจะต้องทำเช่นนั้นโดยได้รับอินสแตนซ์ของการตั้งค่าคอนฟิกอินทราสแทตของเราจากอินสแตนซ์ Microsoft เพื่อทำการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="f76ed-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="f76ed-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f76ed-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="f76ed-116">ในฟิลด์ใหม่ ป้อน 'ได้รับมาจากชื่อ: อินทราสแทต (DE), Microsoft'</span><span class="sxs-lookup"><span data-stu-id="f76ed-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="f76ed-117">ในฟิลด์ชื่อ พิมพ์ 'อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป'</span><span class="sxs-lookup"><span data-stu-id="f76ed-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="f76ed-118">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f76ed-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="f76ed-119">ตั้งค่าคอนฟิกรายงานนี้เพื่อทำการตรวจนับและสรุปตามรายละเอียดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f76ed-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="f76ed-120">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f76ed-120">Click Designer.</span></span>
2. <span data-ttu-id="f76ed-121">เลือก ใช่ ในฟิลด์ รวมบรวมรายละเอียดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f76ed-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="f76ed-122">แฟล็กนี้จะเปิดใช้งานในเวลาที่ใช้ในการผลิตกระบวนการรวบรวมรายละเอียดผลลัพธ์สำหรับการสร้างไฟล์อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="f76ed-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="f76ed-123">คุณต้องทำการตรวจนับสำหรับทิศทางอินทราสแทตที่แตกต่างกัน ดังนั้น ให้เพิ่มการแจงนับแบบจำลองเฉพาะลงในรายการแหล่งข้อมูลของการตั้งค่าคอนฟิกรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="f76ed-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="f76ed-124">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="f76ed-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="f76ed-125">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f76ed-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="f76ed-126">ในแผนภูมิ เลือก 'Data model\Enumeration '</span><span class="sxs-lookup"><span data-stu-id="f76ed-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="f76ed-127">ในฟิลด์ชื่อ ให้พิมพ์ 'ทิศทาง'</span><span class="sxs-lookup"><span data-stu-id="f76ed-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="f76ed-128">ในฟิลด์การแจงนับแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f76ed-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="f76ed-129">เลือกค่า ทิศทาง</span><span class="sxs-lookup"><span data-stu-id="f76ed-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="f76ed-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f76ed-130">Click OK.</span></span>
9. <span data-ttu-id="f76ed-131">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f76ed-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="f76ed-132">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="f76ed-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="f76ed-133">ในฟิลด์ชื่อ ให้พิมพ์ '$BlockName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="f76ed-134">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="f76ed-134">Click Edit formula.</span></span>
13. <span data-ttu-id="f76ed-135">ในฟิลด์สูตร ให้ป้อน '"บล็อค"'</span><span class="sxs-lookup"><span data-stu-id="f76ed-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="f76ed-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-136">Click Save.</span></span>
15. <span data-ttu-id="f76ed-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-137">Close the page.</span></span>
16. <span data-ttu-id="f76ed-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f76ed-138">Click OK.</span></span>
17. <span data-ttu-id="f76ed-139">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f76ed-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="f76ed-140">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="f76ed-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="f76ed-141">ในฟิลด์ชื่อ ให้พิมพ์ '$RecName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="f76ed-142">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="f76ed-142">Click Edit formula.</span></span>
21. <span data-ttu-id="f76ed-143">ในฟิลด์สูตร ให้ป้อน '"เรกคอร์ด"'</span><span class="sxs-lookup"><span data-stu-id="f76ed-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="f76ed-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-144">Click Save.</span></span>
23. <span data-ttu-id="f76ed-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-145">Close the page.</span></span>
24. <span data-ttu-id="f76ed-146">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f76ed-146">Click OK.</span></span>
25. <span data-ttu-id="f76ed-147">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f76ed-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="f76ed-148">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="f76ed-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="f76ed-149">ในฟิลด์ชื่อ ให้พิมพ์ '$InvName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="f76ed-150">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="f76ed-150">Click Edit formula.</span></span>
29. <span data-ttu-id="f76ed-151">ในฟิลด์สูตร ให้ป้อน '"InvoicedAmountEUR"'</span><span class="sxs-lookup"><span data-stu-id="f76ed-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="f76ed-152">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-152">Click Save.</span></span>
31. <span data-ttu-id="f76ed-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-153">Close the page.</span></span>
32. <span data-ttu-id="f76ed-154">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f76ed-154">Click OK.</span></span>
33. <span data-ttu-id="f76ed-155">ในแผนภูมิ ให้เลือก 'Intrastat\Data'</span><span class="sxs-lookup"><span data-stu-id="f76ed-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="f76ed-156">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="f76ed-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="f76ed-157">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f76ed-157">Click Add data source.</span></span>
    * <span data-ttu-id="f76ed-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="f76ed-158">$BlockName</span></span>  
36. <span data-ttu-id="f76ed-159">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-159">Click Save.</span></span>
37. <span data-ttu-id="f76ed-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-160">Close the page.</span></span>
38. <span data-ttu-id="f76ed-161">คลิกปุ่มแก้ไขสำหรับฟิลด์ ค่าคีย์ข้อมูลที่รวบรวม</span><span class="sxs-lookup"><span data-stu-id="f76ed-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="f76ed-162">ในฟิลด์สูตร ป้อน 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'</span><span class="sxs-lookup"><span data-stu-id="f76ed-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="f76ed-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="f76ed-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="f76ed-164">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-164">Click Save.</span></span>
41. <span data-ttu-id="f76ed-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-165">Close the page.</span></span>
    * <span data-ttu-id="f76ed-166">ตรวจนับจำนวนบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="f76ed-166">Count the lines of this sequence.</span></span> <span data-ttu-id="f76ed-167">ผลลัพธ์จะถูกนำไปใช้พร้อมกับชื่อ "บล็อค" โดยแยกต่างหากสำหรับทิศทางที่แตกต่างกัน </span><span class="sxs-lookup"><span data-stu-id="f76ed-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="f76ed-168">จะมีการใช้ค่า "นำเข้า" สำหรับธุรกรรมอินทราสแทตขาเข้าใดๆ </span><span class="sxs-lookup"><span data-stu-id="f76ed-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="f76ed-169">ค่า "ส่งออก" จะถูกใช้สำหรับธุกรรมการจัดส่งอินทราสแทตใดๆ ให้</span><span class="sxs-lookup"><span data-stu-id="f76ed-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="f76ed-170">ให้พิจารณาสิ่งนี้เป็นแผ่นตารางทำการ Excel เสมือน </span><span class="sxs-lookup"><span data-stu-id="f76ed-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="f76ed-171">สำหรับแต่ละธุรกรรมของแถวที่มีคอลัมน์แรก "บล็อค" จะมีค่า "นำเข้า" และ "ส่งออก" ที่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="f76ed-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="f76ed-172">ในแผนภูมิ ขยาย 'Intrastat\Data: Sequence'</span><span class="sxs-lookup"><span data-stu-id="f76ed-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="f76ed-173">ในแผนภูมิ เลือก 'Intrastat\Data: Sequence\Arrivals?'</span><span class="sxs-lookup"><span data-stu-id="f76ed-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="f76ed-174">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="f76ed-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="f76ed-175">ตรวจนับจำนวนบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="f76ed-175">Count the lines of this sequence.</span></span> <span data-ttu-id="f76ed-176">ระบบจะจดจำผลลัพธ์โดยใช้ชื่อ "เรกคอร์ด"</span><span class="sxs-lookup"><span data-stu-id="f76ed-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="f76ed-177">ในแผนภูมิ ให้เลือก '$RecName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="f76ed-178">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f76ed-178">Click Add data source.</span></span>
47. <span data-ttu-id="f76ed-179">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-179">Click Save.</span></span>
48. <span data-ttu-id="f76ed-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-180">Close the page.</span></span>
49. <span data-ttu-id="f76ed-181">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ค่าคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="f76ed-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="f76ed-182">ในฟิลด์สูตร ให้ป้อน 'Intrastat.CommodityRecord.CommodityCode'</span><span class="sxs-lookup"><span data-stu-id="f76ed-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="f76ed-183">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-183">Click Save.</span></span>
52. <span data-ttu-id="f76ed-184">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-184">Close the page.</span></span>
    * <span data-ttu-id="f76ed-185">ตรวจนับจำนวนบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="f76ed-185">Count the lines of this sequence.</span></span> <span data-ttu-id="f76ed-186">ผลลัพธ์จะถูกนำไปใช้พร้อมกับชื่อ "เรกคอร์ด" โดยแยกต่างหากสำหรับรหัสโภคภัณฑ์ที่แตกต่างกัน </span><span class="sxs-lookup"><span data-stu-id="f76ed-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="f76ed-187">ให้พิจารณาสิ่งนี้เป็นแผ่นตารางทำการ Excel เสมือน </span><span class="sxs-lookup"><span data-stu-id="f76ed-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="f76ed-188">สำหรับแต่ละธุรกรรมของแถวที่มีคอลัมน์แรก "บล็อค" จะมีค่า "นำเข้า" และ "ส่งออก" ที่สอดคล้องกัน และบล็อคที่สอง "เรกคอร์ด" จะมีค่ารหัสโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f76ed-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="f76ed-189">ในแผนภูมิ เลือก 'Intrastat\Data: Sequence\Dispatches?'</span><span class="sxs-lookup"><span data-stu-id="f76ed-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="f76ed-190">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="f76ed-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="f76ed-191">ในแผนภูมิ ให้เลือก '$RecName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="f76ed-192">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f76ed-192">Click Add data source.</span></span>
57. <span data-ttu-id="f76ed-193">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-193">Click Save.</span></span>
58. <span data-ttu-id="f76ed-194">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-194">Close the page.</span></span>
59. <span data-ttu-id="f76ed-195">คลิกปุ่มแก้ไขสำหรับฟิลด์ ‘ค่าคีย์ข้อมูลที่รวบรวม‘</span><span class="sxs-lookup"><span data-stu-id="f76ed-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="f76ed-196">ในฟิลด์สูตร ให้ป้อน 'Intrastat.CommodityRecord.CommodityCode'</span><span class="sxs-lookup"><span data-stu-id="f76ed-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="f76ed-197">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-197">Click Save.</span></span>
62. <span data-ttu-id="f76ed-198">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-198">Close the page.</span></span>
63. <span data-ttu-id="f76ed-199">ในแผนภูมิ ขยาย 'Intrastat\Data: Sequence\Dispatches: Sequence?'</span><span class="sxs-lookup"><span data-stu-id="f76ed-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="f76ed-200">ในแผนภูมิ ขยาย 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'</span><span class="sxs-lookup"><span data-stu-id="f76ed-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="f76ed-201">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="f76ed-201">Click the Format tab.</span></span>
66. <span data-ttu-id="f76ed-202">ในแผนภูมิ เลือก ''Intrastat\Data\Dispatches\Record\Invoice amount EUR'</span><span class="sxs-lookup"><span data-stu-id="f76ed-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="f76ed-203">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="f76ed-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="f76ed-204">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="f76ed-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="f76ed-205">ในแผนภูมิ ให้เลือก '$InvName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="f76ed-206">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f76ed-206">Click Add data source.</span></span>
71. <span data-ttu-id="f76ed-207">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-207">Click Save.</span></span>
72. <span data-ttu-id="f76ed-208">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-208">Close the page.</span></span>
    * <span data-ttu-id="f76ed-209">สรุปค่ายอดเงินใบแจ้งหนี้สำหรับบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="f76ed-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="f76ed-210">ผลลัพธ์จะถูกนำไปใช้พร้อมกับชื่อ "InvoicedAmountEUR" โดยแยกต่างหากสำหรับทิศทางอินทราสแทตและรหัสโภคภัณฑ์ที่แตกต่างกัน </span><span class="sxs-lookup"><span data-stu-id="f76ed-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="f76ed-211">ให้พิจารณาสิ่งนี้เป็นการสร้างเสมือนในแผ่นตารางทำการ Excel </span><span class="sxs-lookup"><span data-stu-id="f76ed-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="f76ed-212">สำหรับแต่ละธุรกรรมของแถวที่มีคอลัมน์แรก "บล็อค" จะมีค่า "นำเข้า" และ "ส่งออก" ที่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="f76ed-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="f76ed-213">บล็อคที่สอง "เรกคอร์ด" จะมีค่ารหัสโภคภัณฑ์ และคอลัมน์ที่สาม “InvoicedAmountEUR” จะมีค่ายอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f76ed-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="f76ed-214">ในแผนภูมิ ขยาย 'Intrastat\Data\Arrivals?'</span><span class="sxs-lookup"><span data-stu-id="f76ed-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="f76ed-215">ในแผนภูมิ ขยาย 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'</span><span class="sxs-lookup"><span data-stu-id="f76ed-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="f76ed-216">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="f76ed-216">Click the Format tab.</span></span>
76. <span data-ttu-id="f76ed-217">ในแผนภูมิ เลือก ''Intrastat\Data\Arrivals\Record\Invoice amount EUR'</span><span class="sxs-lookup"><span data-stu-id="f76ed-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="f76ed-218">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="f76ed-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="f76ed-219">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="f76ed-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="f76ed-220">ในแผนภูมิ ให้เลือก '$InvName'</span><span class="sxs-lookup"><span data-stu-id="f76ed-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="f76ed-221">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f76ed-221">Click Add data source.</span></span>
81. <span data-ttu-id="f76ed-222">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-222">Click Save.</span></span>
82. <span data-ttu-id="f76ed-223">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-223">Close the page.</span></span>
83. <span data-ttu-id="f76ed-224">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f76ed-224">Click Save.</span></span>
84. <span data-ttu-id="f76ed-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f76ed-225">Close the page.</span></span>

