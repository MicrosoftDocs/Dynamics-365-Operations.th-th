--- 
title: "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 4 - รันรูปแบบ)"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว "
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a><span data-ttu-id="80b41-103">ER ตั้งค่าคอนฟิกรูปปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 4: รันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="80b41-103">ER Configure format to do counting and summing (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80b41-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="80b41-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="80b41-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="80b41-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="80b41-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 3: ใช้การคำนวณเพื่อสร้างผลลัพธ์)"</span><span class="sxs-lookup"><span data-stu-id="80b41-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="80b41-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="80b41-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="80b41-108">ทดสอบการตั้งค่าคอนฟิกนี้สำหรับการสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="80b41-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="80b41-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="80b41-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="80b41-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="80b41-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="80b41-111">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="80b41-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="80b41-112">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="80b41-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="80b41-113">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="80b41-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="80b41-114">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="80b41-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="80b41-115">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="80b41-115">Click User parameters.</span></span>
8. <span data-ttu-id="80b41-116">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="80b41-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="80b41-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="80b41-117">Click OK.</span></span>
10. <span data-ttu-id="80b41-118">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="80b41-118">Click Edit.</span></span>
11. <span data-ttu-id="80b41-119">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="80b41-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="80b41-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="80b41-120">Click Save.</span></span>
13. <span data-ttu-id="80b41-121">ไปที่ภาษี > การตั้งค่า > การค้าต่างประเทศ > พารามิเตอร์การค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="80b41-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="80b41-122">ขยายส่วนการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="80b41-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="80b41-123">เลือกการจัดโครงแบบ "อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป"</span><span class="sxs-lookup"><span data-stu-id="80b41-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="80b41-124">เลือกการจัดโครงแบบ "อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป"</span><span class="sxs-lookup"><span data-stu-id="80b41-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="80b41-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="80b41-125">Click Save.</span></span>
18. <span data-ttu-id="80b41-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="80b41-126">Close the page.</span></span>
19. <span data-ttu-id="80b41-127">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="80b41-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="80b41-128">คลิกเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="80b41-128">Click Output.</span></span>
21. <span data-ttu-id="80b41-129">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="80b41-129">Click Report.</span></span>
    * <span data-ttu-id="80b41-130">รันกระบวนการสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="80b41-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="80b41-131">ในฟิลด์วันที่เริ่มต้น ตั้งค่าวันที่เป็น ' 2000-01-01'</span><span class="sxs-lookup"><span data-stu-id="80b41-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="80b41-132">กำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรอบระยะเวลาการรายงานที่รวมอยู่ในรายการที่มีอยู่ในธุรกรรมแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="80b41-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="80b41-133">ในฟิลด์วันที่สิ้นสุด ตั้งค่าวันที่เป็น ' 2022-12-31'</span><span class="sxs-lookup"><span data-stu-id="80b41-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="80b41-134">กำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรอบระยะเวลาการรายงานที่รวมอยู่ในรายการที่มีอยู่ในธุรกรรมแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="80b41-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="80b41-135">ในฟิลด์ทิศทาง ให้เลือก 'การมาถึง'</span><span class="sxs-lookup"><span data-stu-id="80b41-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="80b41-136">เลือก ใช่ ในฟิลด์สร้างไฟล์</span><span class="sxs-lookup"><span data-stu-id="80b41-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="80b41-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="80b41-137">Click OK.</span></span>
    * <span data-ttu-id="80b41-138">ตรวจทานผลลัพธ์ที่สร้างไว้ที่มีรายการสรุปในส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="80b41-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="80b41-139">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="80b41-139">Click New.</span></span>
28. <span data-ttu-id="80b41-140">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="80b41-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="80b41-141">ในฟิลด์ทิศทาง ให้เลือก 'การจัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="80b41-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="80b41-142">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="80b41-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="80b41-143">ในฟิลด์โภคภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="80b41-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="80b41-144">ตั้งค่าน้ำหนักเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="80b41-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="80b41-145">ตั้งค่าจำนวนเงินในใบแจ้งหนี้เป็น '10000'</span><span class="sxs-lookup"><span data-stu-id="80b41-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="80b41-146">ตั้งค่ายอดเงินตามสถิติเป็น '10000'</span><span class="sxs-lookup"><span data-stu-id="80b41-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="80b41-147">คลิกเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="80b41-147">Click Output.</span></span>
36. <span data-ttu-id="80b41-148">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="80b41-148">Click Report.</span></span>
37. <span data-ttu-id="80b41-149">ในฟิลด์ทิศทาง ให้เลือก 'การจัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="80b41-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="80b41-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="80b41-150">Click OK.</span></span>
    * <span data-ttu-id="80b41-151">ตรวจทานผลลัพธ์ที่สร้างไว้ที่มีรายการสรุปในส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="80b41-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="80b41-152">โปรดทราบว่าการเปรียบเทียบมีการเปลี่ยนแปลงในการรันครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="80b41-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="80b41-153">รันการตั้งค่าคอนฟิกนี้ในโหมดดีบักเพื่อตรวจทานการตรวจนับการรับสินค้า & การรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="80b41-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="80b41-154">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="80b41-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="80b41-155">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="80b41-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="80b41-156">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="80b41-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="80b41-157">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="80b41-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="80b41-158">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="80b41-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="80b41-159">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="80b41-159">Click User parameters.</span></span>
7. <span data-ttu-id="80b41-160">เลือก ใช่ ในฟิลด์ รันในโหมดดีบัก</span><span class="sxs-lookup"><span data-stu-id="80b41-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="80b41-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="80b41-161">Click OK.</span></span>
9. <span data-ttu-id="80b41-162">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="80b41-162">Close the page.</span></span>
10. <span data-ttu-id="80b41-163">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="80b41-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="80b41-164">คลิกเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="80b41-164">Click Output.</span></span>
12. <span data-ttu-id="80b41-165">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="80b41-165">Click Report.</span></span>
13. <span data-ttu-id="80b41-166">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="80b41-166">Click OK.</span></span>
14. <span data-ttu-id="80b41-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="80b41-167">Close the page.</span></span>
15. <span data-ttu-id="80b41-168">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="80b41-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="80b41-169">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="80b41-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="80b41-170">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="80b41-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="80b41-171">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="80b41-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="80b41-172">คลิก ล็อกดีบัก</span><span class="sxs-lookup"><span data-stu-id="80b41-172">Click Debug logs.</span></span>
    * <span data-ttu-id="80b41-173">โปรดทราบว่ามีการสร้างเรกคอร์ดล็อกดีบักสำหรับกระบวนการดำเนินการของการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="80b41-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="80b41-174">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="80b41-174">Click Attach.</span></span>
21. <span data-ttu-id="80b41-175">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="80b41-175">Click Open.</span></span>
    * <span data-ttu-id="80b41-176">ตรวจทานไฟล์ XML ที่สร้างขึ้นที่ประกอบด้วยรายละเอียดการตรวจนับและการสรุปที่ได้รวบรวมในระหว่างการดำเนินการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="80b41-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


