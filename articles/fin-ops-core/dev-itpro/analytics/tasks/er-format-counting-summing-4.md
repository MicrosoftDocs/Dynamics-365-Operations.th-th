---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 4 - รันรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อตรวจนับและรวมตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว (ส่วนที่ 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092958"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="ec7da-104">ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 4 - รันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="ec7da-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec7da-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="ec7da-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="ec7da-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="ec7da-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ec7da-107">เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำให้ขั้นตอนในกระบวนงาน "ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 3: ใช้การคำนวณเพื่อสร้างผลลัพธ์)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ec7da-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="ec7da-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="ec7da-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="ec7da-109">ทดสอบการตั้งค่าคอนฟิกนี้สำหรับการสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="ec7da-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="ec7da-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ec7da-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ec7da-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec7da-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ec7da-112">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="ec7da-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="ec7da-113">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="ec7da-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="ec7da-114">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="ec7da-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="ec7da-115">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="ec7da-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="ec7da-116">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ec7da-116">Click User parameters.</span></span>
8. <span data-ttu-id="ec7da-117">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="ec7da-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="ec7da-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ec7da-118">Click OK.</span></span>
10. <span data-ttu-id="ec7da-119">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ec7da-119">Click Edit.</span></span>
11. <span data-ttu-id="ec7da-120">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="ec7da-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="ec7da-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ec7da-121">Click Save.</span></span>
13. <span data-ttu-id="ec7da-122">ไปที่ภาษี > การตั้งค่า > การค้าต่างประเทศ > พารามิเตอร์การค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="ec7da-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="ec7da-123">ขยายส่วนการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ec7da-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="ec7da-124">เลือกการตั้งค่าคอนฟิก "อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป"</span><span class="sxs-lookup"><span data-stu-id="ec7da-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="ec7da-125">เลือกการตั้งค่าคอนฟิก "อินทราสแทต (DE) พร้อมกับการตรวจนับ & การสรุป"</span><span class="sxs-lookup"><span data-stu-id="ec7da-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="ec7da-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ec7da-126">Click Save.</span></span>
18. <span data-ttu-id="ec7da-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec7da-127">Close the page.</span></span>
19. <span data-ttu-id="ec7da-128">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="ec7da-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="ec7da-129">คลิกเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="ec7da-129">Click Output.</span></span>
21. <span data-ttu-id="ec7da-130">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec7da-130">Click Report.</span></span>
    * <span data-ttu-id="ec7da-131">รันกระบวนการสร้างรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="ec7da-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="ec7da-132">ในฟิลด์วันที่เริ่มต้น ตั้งค่าวันที่เป็น ' 2000-01-01'</span><span class="sxs-lookup"><span data-stu-id="ec7da-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="ec7da-133">กำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรอบระยะเวลาการรายงานที่รวมอยู่ในรายการที่มีอยู่ในธุรกรรมแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="ec7da-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="ec7da-134">ในฟิลด์วันที่สิ้นสุด ตั้งค่าวันที่เป็น ' 2022-12-31'</span><span class="sxs-lookup"><span data-stu-id="ec7da-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="ec7da-135">กำหนดวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรอบระยะเวลาการรายงานที่รวมอยู่ในรายการที่มีอยู่ในธุรกรรมแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="ec7da-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="ec7da-136">ในฟิลด์ทิศทาง ให้เลือก 'การมาถึง'</span><span class="sxs-lookup"><span data-stu-id="ec7da-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="ec7da-137">เลือก ใช่ ในฟิลด์สร้างไฟล์</span><span class="sxs-lookup"><span data-stu-id="ec7da-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="ec7da-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ec7da-138">Click OK.</span></span>
    * <span data-ttu-id="ec7da-139">ตรวจทานผลลัพธ์ที่สร้างไว้ที่มีรายการสรุปในส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="ec7da-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="ec7da-140">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ec7da-140">Click New.</span></span>
28. <span data-ttu-id="ec7da-141">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec7da-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="ec7da-142">ในฟิลด์ทิศทาง ให้เลือก 'การจัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="ec7da-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="ec7da-143">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ec7da-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="ec7da-144">ในฟิลด์โภคภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ec7da-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="ec7da-145">ตั้งค่าน้ำหนักเป็น '10'</span><span class="sxs-lookup"><span data-stu-id="ec7da-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="ec7da-146">ตั้งค่าจำนวนเงินในใบแจ้งหนี้เป็น '10000'</span><span class="sxs-lookup"><span data-stu-id="ec7da-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="ec7da-147">ตั้งค่ายอดเงินตามสถิติเป็น '10000'</span><span class="sxs-lookup"><span data-stu-id="ec7da-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="ec7da-148">คลิกเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="ec7da-148">Click Output.</span></span>
36. <span data-ttu-id="ec7da-149">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec7da-149">Click Report.</span></span>
37. <span data-ttu-id="ec7da-150">ในฟิลด์ทิศทาง ให้เลือก 'การจัดส่ง'</span><span class="sxs-lookup"><span data-stu-id="ec7da-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="ec7da-151">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ec7da-151">Click OK.</span></span>
    * <span data-ttu-id="ec7da-152">ตรวจทานผลลัพธ์ที่สร้างไว้ที่มีรายการสรุปในส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="ec7da-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="ec7da-153">โปรดทราบว่าการเปรียบเทียบมีการเปลี่ยนแปลงในการรันครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="ec7da-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="ec7da-154">รันการตั้งค่าคอนฟิกนี้ในโหมดดีบักเพื่อตรวจทานการตรวจนับการรับสินค้า & การรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ec7da-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="ec7da-155">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ec7da-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ec7da-156">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="ec7da-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="ec7da-157">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="ec7da-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="ec7da-158">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="ec7da-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="ec7da-159">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="ec7da-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="ec7da-160">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ec7da-160">Click User parameters.</span></span>
7. <span data-ttu-id="ec7da-161">เลือก ใช่ ในฟิลด์ รันในโหมดดีบัก</span><span class="sxs-lookup"><span data-stu-id="ec7da-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="ec7da-162">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ec7da-162">Click OK.</span></span>
9. <span data-ttu-id="ec7da-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec7da-163">Close the page.</span></span>
10. <span data-ttu-id="ec7da-164">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="ec7da-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="ec7da-165">คลิกเอาท์พุท</span><span class="sxs-lookup"><span data-stu-id="ec7da-165">Click Output.</span></span>
12. <span data-ttu-id="ec7da-166">คลิกรายงาน</span><span class="sxs-lookup"><span data-stu-id="ec7da-166">Click Report.</span></span>
13. <span data-ttu-id="ec7da-167">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ec7da-167">Click OK.</span></span>
14. <span data-ttu-id="ec7da-168">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ec7da-168">Close the page.</span></span>
15. <span data-ttu-id="ec7da-169">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ec7da-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="ec7da-170">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="ec7da-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="ec7da-171">ในแผนภูมิ ขยาย 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)'</span><span class="sxs-lookup"><span data-stu-id="ec7da-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="ec7da-172">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\อินทราสแทต (DE)\อินทราสแทต (DE) ที่มีการตรวจนับ & การรวม'</span><span class="sxs-lookup"><span data-stu-id="ec7da-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="ec7da-173">คลิก ล็อกดีบัก</span><span class="sxs-lookup"><span data-stu-id="ec7da-173">Click Debug logs.</span></span>
    * <span data-ttu-id="ec7da-174">โปรดทราบว่ามีการสร้างเรกคอร์ดล็อกดีบักสำหรับกระบวนการดำเนินการของการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec7da-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="ec7da-175">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="ec7da-175">Click Attach.</span></span>
21. <span data-ttu-id="ec7da-176">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="ec7da-176">Click Open.</span></span>
    * <span data-ttu-id="ec7da-177">ตรวจทานไฟล์ XML ที่สร้างขึ้นที่ประกอบด้วยรายละเอียดการตรวจนับและการสรุปที่ได้รวบรวมในระหว่างการดำเนินการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ec7da-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

