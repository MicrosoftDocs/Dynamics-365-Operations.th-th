---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 2 - ตั้งค่าคอนฟิกการคำนวณ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อตรวจนับและรวมตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว (ส่วนที่ 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565177"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="b9839-104">ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 2 - ตั้งค่าคอนฟิกการคำนวณ)</span><span class="sxs-lookup"><span data-stu-id="b9839-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9839-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="b9839-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="b9839-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="b9839-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="b9839-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1: สร้างรูปแบบ)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b9839-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="b9839-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="b9839-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="b9839-109">สร้างการตั้งค่าคอนฟิกรูปแบบเพื่อเพิ่มรายละเอียดการตรวจนับและการสรุป</span><span class="sxs-lookup"><span data-stu-id="b9839-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="b9839-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b9839-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b9839-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="b9839-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b9839-112">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="b9839-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="b9839-113">ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'</span><span class="sxs-lookup"><span data-stu-id="b9839-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="b9839-114">สมมติว่าคุณจำเป็นต้องกำหนดรูปแบบที่ระบุโดย Microsoft โดยการเพิ่มบรรทัดพร้อมกับรายละเอียดสรุปที่ส่วนท้ายของรายงานอินทราสแทต </span><span class="sxs-lookup"><span data-stu-id="b9839-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="b9839-115">คุณจะต้องทำเช่นนั้นโดยได้รับอินสแตนซ์ของการตั้งค่าคอนฟิกอินทราสแทตของเราจากอินสแตนซ์ Microsoft เพื่อทำการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="b9839-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="b9839-116">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b9839-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="b9839-117">ในฟิลด์ใหม่ ป้อน 'ได้รับมาจากชื่อ: อินทราสแทต (DE), Microsoft'</span><span class="sxs-lookup"><span data-stu-id="b9839-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="b9839-118">ในฟิลด์ชื่อ พิมพ์ 'อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป'</span><span class="sxs-lookup"><span data-stu-id="b9839-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="b9839-119">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b9839-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="b9839-120">ตั้งค่าคอนฟิกรายงานนี้เพื่อทำการตรวจนับและสรุปตามรายละเอียดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b9839-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="b9839-121">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b9839-121">Click Designer.</span></span>
2. <span data-ttu-id="b9839-122">เลือก ใช่ ในฟิลด์ รวมบรวมรายละเอียดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b9839-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="b9839-123">แฟล็กนี้จะเปิดใช้งานในเวลาที่ใช้ในการผลิตกระบวนการรวบรวมรายละเอียดผลลัพธ์สำหรับการสร้างไฟล์อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="b9839-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="b9839-124">คุณต้องทำการตรวจนับสำหรับทิศทางอินทราสแทตที่แตกต่างกัน ดังนั้น ให้เพิ่มการแจงนับแบบจำลองเฉพาะลงในรายการของแหล่งข้อมูลของการตั้งค่าคอนฟิกรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="b9839-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="b9839-125">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="b9839-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="b9839-126">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b9839-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="b9839-127">ในแผนภูมิ เลือก 'Data model\Enumeration '</span><span class="sxs-lookup"><span data-stu-id="b9839-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="b9839-128">ในฟิลด์ชื่อ ให้พิมพ์ 'ทิศทาง'</span><span class="sxs-lookup"><span data-stu-id="b9839-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="b9839-129">ในฟิลด์การแจงนับแบบจำลอง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b9839-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="b9839-130">เลือกค่า ทิศทาง</span><span class="sxs-lookup"><span data-stu-id="b9839-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="b9839-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b9839-131">Click OK.</span></span>
9. <span data-ttu-id="b9839-132">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b9839-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="b9839-133">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="b9839-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="b9839-134">ในฟิลด์ชื่อ ให้พิมพ์ '$BlockName'</span><span class="sxs-lookup"><span data-stu-id="b9839-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="b9839-135">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b9839-135">Click Edit formula.</span></span>
13. <span data-ttu-id="b9839-136">ในฟิลด์สูตร ให้ป้อน '"บล็อค"'</span><span class="sxs-lookup"><span data-stu-id="b9839-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="b9839-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-137">Click Save.</span></span>
15. <span data-ttu-id="b9839-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-138">Close the page.</span></span>
16. <span data-ttu-id="b9839-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b9839-139">Click OK.</span></span>
17. <span data-ttu-id="b9839-140">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b9839-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="b9839-141">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="b9839-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="b9839-142">ในฟิลด์ชื่อ ให้พิมพ์ '$RecName'</span><span class="sxs-lookup"><span data-stu-id="b9839-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="b9839-143">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b9839-143">Click Edit formula.</span></span>
21. <span data-ttu-id="b9839-144">ในฟิลด์สูตร ให้ป้อน '"เรกคอร์ด"'</span><span class="sxs-lookup"><span data-stu-id="b9839-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="b9839-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-145">Click Save.</span></span>
23. <span data-ttu-id="b9839-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-146">Close the page.</span></span>
24. <span data-ttu-id="b9839-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b9839-147">Click OK.</span></span>
25. <span data-ttu-id="b9839-148">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="b9839-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="b9839-149">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="b9839-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="b9839-150">ในฟิลด์ชื่อ ให้พิมพ์ '$InvName'</span><span class="sxs-lookup"><span data-stu-id="b9839-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="b9839-151">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="b9839-151">Click Edit formula.</span></span>
29. <span data-ttu-id="b9839-152">ในฟิลด์สูตร ให้ป้อน '"InvoicedAmountEUR"'</span><span class="sxs-lookup"><span data-stu-id="b9839-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="b9839-153">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-153">Click Save.</span></span>
31. <span data-ttu-id="b9839-154">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-154">Close the page.</span></span>
32. <span data-ttu-id="b9839-155">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b9839-155">Click OK.</span></span>
33. <span data-ttu-id="b9839-156">ในแผนภูมิ ให้เลือก 'Intrastat\Data'</span><span class="sxs-lookup"><span data-stu-id="b9839-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="b9839-157">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="b9839-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="b9839-158">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9839-158">Click Add data source.</span></span>
    * <span data-ttu-id="b9839-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="b9839-159">$BlockName</span></span>  
36. <span data-ttu-id="b9839-160">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-160">Click Save.</span></span>
37. <span data-ttu-id="b9839-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-161">Close the page.</span></span>
38. <span data-ttu-id="b9839-162">คลิกปุ่มแก้ไขสำหรับฟิลด์ ค่าคีย์ข้อมูลที่รวบรวม</span><span class="sxs-lookup"><span data-stu-id="b9839-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="b9839-163">ในฟิลด์สูตร ป้อน 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'</span><span class="sxs-lookup"><span data-stu-id="b9839-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="b9839-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="b9839-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="b9839-165">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-165">Click Save.</span></span>
41. <span data-ttu-id="b9839-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-166">Close the page.</span></span>
    * <span data-ttu-id="b9839-167">ตรวจนับจำนวนบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="b9839-167">Count the lines of this sequence.</span></span> <span data-ttu-id="b9839-168">ผลลัพธ์จะถูกใช้พร้อมกับชื่อ "บล็อค" โดยแยกต่างหากสำหรับทิศทางที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b9839-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="b9839-169">จะมีการใช้ค่า "นำเข้า" สำหรับธุรกรรมอินทราสแทตขาเข้าใดๆ</span><span class="sxs-lookup"><span data-stu-id="b9839-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="b9839-170">ค่า "ส่งออก" จะถูกใช้สำหรับธุกรรมการจัดส่งอินทราสแทตใดๆ</span><span class="sxs-lookup"><span data-stu-id="b9839-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="b9839-171">ให้พิจารณาสิ่งนี้เป็นแผ่นตารางทำการ Excel เสมือน </span><span class="sxs-lookup"><span data-stu-id="b9839-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="b9839-172">สำหรับธุรกรรมแต่ละรายการ แถวที่ซึ่งคอลัมน์แรก "บล็อค" ถูกเติมด้วยค่า "นำเข้า" และ "ส่งออก" อย่างสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b9839-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="b9839-173">ในแผนภูมิ ขยาย 'Intrastat\Data: Sequence'</span><span class="sxs-lookup"><span data-stu-id="b9839-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="b9839-174">ในแผนภูมิ เลือก 'Intrastat\Data: Sequence\Arrivals?'</span><span class="sxs-lookup"><span data-stu-id="b9839-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="b9839-175">คลิกปุ่ม แก้ไข สำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="b9839-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="b9839-176">ตรวจนับจำนวนบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="b9839-176">Count the lines of this sequence.</span></span> <span data-ttu-id="b9839-177">ระบบจะจดจำผลลัพธ์โดยใช้ชื่อ "เรกคอร์ด"</span><span class="sxs-lookup"><span data-stu-id="b9839-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="b9839-178">ในแผนภูมิ ให้เลือก '$RecName'</span><span class="sxs-lookup"><span data-stu-id="b9839-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="b9839-179">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9839-179">Click Add data source.</span></span>
47. <span data-ttu-id="b9839-180">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-180">Click Save.</span></span>
48. <span data-ttu-id="b9839-181">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-181">Close the page.</span></span>
49. <span data-ttu-id="b9839-182">คลิกปุ่ม แก้ไข สำหรับฟิลด์ 'ค่าคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="b9839-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="b9839-183">ในฟิลด์สูตร ให้ป้อน 'Intrastat.CommodityRecord.CommodityCode'</span><span class="sxs-lookup"><span data-stu-id="b9839-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="b9839-184">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-184">Click Save.</span></span>
52. <span data-ttu-id="b9839-185">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-185">Close the page.</span></span>
    * <span data-ttu-id="b9839-186">ตรวจนับจำนวนบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="b9839-186">Count the lines of this sequence.</span></span> <span data-ttu-id="b9839-187">ผลลัพธ์จะถูกนำไปใช้พร้อมกับชื่อ "เรกคอร์ด" โดยแยกต่างหาก สำหรับรหัสโภคภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b9839-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="b9839-188">ให้พิจารณาสิ่งนี้เป็นแผ่นตารางทำการ Excel เสมือน </span><span class="sxs-lookup"><span data-stu-id="b9839-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="b9839-189">สำหรับธุรกรรมแต่ละรายการ แถวที่ซึ่งคอลัมน์แรก "บล็อค" ถูกเติมด้วยค่า "นำเข้า" และ "ส่งออก" อย่างสอดคล้องกัน และบล็อคที่สอง "เรกคอร์ด" ถูกเติมด้วยค่ารหัสโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b9839-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="b9839-190">ในแผนภูมิ เลือก 'Intrastat\Data: Sequence\Dispatches?'</span><span class="sxs-lookup"><span data-stu-id="b9839-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="b9839-191">คลิกปุ่มแก้ไขสำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="b9839-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="b9839-192">ในแผนภูมิ ให้เลือก '$RecName'</span><span class="sxs-lookup"><span data-stu-id="b9839-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="b9839-193">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9839-193">Click Add data source.</span></span>
57. <span data-ttu-id="b9839-194">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-194">Click Save.</span></span>
58. <span data-ttu-id="b9839-195">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-195">Close the page.</span></span>
59. <span data-ttu-id="b9839-196">คลิกปุ่ม แก้ไข สำหรับฟิลด์ ‘ค่าคีย์ข้อมูลที่รวบรวม‘</span><span class="sxs-lookup"><span data-stu-id="b9839-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="b9839-197">ในฟิลด์สูตร ให้ป้อน 'Intrastat.CommodityRecord.CommodityCode'</span><span class="sxs-lookup"><span data-stu-id="b9839-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="b9839-198">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-198">Click Save.</span></span>
62. <span data-ttu-id="b9839-199">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-199">Close the page.</span></span>
63. <span data-ttu-id="b9839-200">ในแผนภูมิ ขยาย 'Intrastat\Data: Sequence\Dispatches: Sequence?'</span><span class="sxs-lookup"><span data-stu-id="b9839-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="b9839-201">ในแผนภูมิ ขยาย 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'</span><span class="sxs-lookup"><span data-stu-id="b9839-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="b9839-202">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b9839-202">Click the Format tab.</span></span>
66. <span data-ttu-id="b9839-203">ในแผนภูมิ เลือก ''Intrastat\Data\Dispatches\Record\Invoice amount EUR'</span><span class="sxs-lookup"><span data-stu-id="b9839-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="b9839-204">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="b9839-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="b9839-205">คลิกปุ่ม แก้ไข สำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="b9839-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="b9839-206">ในแผนภูมิ ให้เลือก '$InvName'</span><span class="sxs-lookup"><span data-stu-id="b9839-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="b9839-207">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9839-207">Click Add data source.</span></span>
71. <span data-ttu-id="b9839-208">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-208">Click Save.</span></span>
72. <span data-ttu-id="b9839-209">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-209">Close the page.</span></span>
    * <span data-ttu-id="b9839-210">สรุปค่ายอดเงินใบแจ้งหนี้สำหรับบรรทัดของลำดับนี้ </span><span class="sxs-lookup"><span data-stu-id="b9839-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="b9839-211">ผลลัพธ์จะถูกใช้พร้อมกับชื่อ "InvoicedAmountEUR" โดยแยกต่างหาก สำหรับทิศทางอินทราสแทตและรหัสโภคภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b9839-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="b9839-212">ให้พิจารณาสิ่งนี้เป็นการสร้างเสมือนในแผ่นตารางทำการ Excel </span><span class="sxs-lookup"><span data-stu-id="b9839-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="b9839-213">สำหรับธุรกรรมแต่ละรายการ แถวที่ซึ่งคอลัมน์แรก "บล็อค" ถูกเติมด้วยค่า "นำเข้า" และ "ส่งออก" อย่างสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b9839-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="b9839-214">บล็อคที่สอง "เรกคอร์ด" ถูกเติมด้วยค่ารหัสโภคภัณฑ์ และคอลัมน์ที่สาม “InvoicedAmountEUR” ถูกเติมด้วยค่ายอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b9839-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="b9839-215">ในแผนภูมิ ขยาย 'Intrastat\Data\Arrivals?'</span><span class="sxs-lookup"><span data-stu-id="b9839-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="b9839-216">ในแผนภูมิ ขยาย 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'</span><span class="sxs-lookup"><span data-stu-id="b9839-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="b9839-217">คลิกแท็บรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b9839-217">Click the Format tab.</span></span>
76. <span data-ttu-id="b9839-218">ในแผนภูมิ เลือก ''Intrastat\Data\Arrivals\Record\Invoice amount EUR'</span><span class="sxs-lookup"><span data-stu-id="b9839-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="b9839-219">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="b9839-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="b9839-220">คลิกปุ่ม แก้ไข สำหรับฟิลด์ 'ชื่อคีย์ข้อมูลที่รวบรวม'</span><span class="sxs-lookup"><span data-stu-id="b9839-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="b9839-221">ในแผนภูมิ ให้เลือก '$InvName'</span><span class="sxs-lookup"><span data-stu-id="b9839-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="b9839-222">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9839-222">Click Add data source.</span></span>
81. <span data-ttu-id="b9839-223">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-223">Click Save.</span></span>
82. <span data-ttu-id="b9839-224">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-224">Close the page.</span></span>
83. <span data-ttu-id="b9839-225">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b9839-225">Click Save.</span></span>
84. <span data-ttu-id="b9839-226">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b9839-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]