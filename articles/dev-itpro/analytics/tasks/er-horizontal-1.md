--- 
title: "ออกแบบรูปแบบเพื่อใช้ช่วงขยายในแนวนอนเพื่อเพิ่มคอลัมน์ในรายงาน Excel แบบไดนามิกสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน "
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="f772e-103">ออกแบบรูปแบบเพื่อใช้ช่วงขยายในแนวนอนเพื่อเพิ่มคอลัมน์ในรายงาน Excel แบบไดนามิกสำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f772e-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f772e-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน </span><span class="sxs-lookup"><span data-stu-id="f772e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="f772e-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="f772e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f772e-106">เพื่อทำตามขั้นตอนเหล่านี้ ก่อนอื่นคุณต้องดำเนินการตามคำแนะนำงานสามรายการนี้:</span><span class="sxs-lookup"><span data-stu-id="f772e-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="f772e-107">”สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของ ER”</span><span class="sxs-lookup"><span data-stu-id="f772e-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="f772e-108">”ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: ออกแบบแบบจำลองข้อมูล)”</span><span class="sxs-lookup"><span data-stu-id="f772e-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="f772e-109">”ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)”</span><span class="sxs-lookup"><span data-stu-id="f772e-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="f772e-110">นอกจากนี้คุณยังต้องดาวน์โหลดและบันทึกสำเนาเฉพาะที่ของเท็มเพลตที่มีรายงานตัวอย่างซึ่งดูได้ที่นี่: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="f772e-110">You must also download and save a local copy of the template with a sample report found here: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx</span></span>

<span data-ttu-id="f772e-111">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="f772e-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="f772e-112">สร้างการตั้งค่าคอนฟิกรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="f772e-112">Create a new report configuration</span></span>
1. <span data-ttu-id="f772e-113">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f772e-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f772e-114">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f772e-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f772e-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f772e-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f772e-116">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f772e-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="f772e-117">ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f772e-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="f772e-118">ในฟิลด์ชื่อ พิมพ์ 'ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน'</span><span class="sxs-lookup"><span data-stu-id="f772e-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="f772e-119">ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน</span><span class="sxs-lookup"><span data-stu-id="f772e-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="f772e-120">ในฟิลด์คำอธิบาย พิมพ์ 'เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก'</span><span class="sxs-lookup"><span data-stu-id="f772e-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="f772e-121">เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="f772e-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="f772e-122">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="f772e-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="f772e-123">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f772e-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="f772e-124">ออกแบบรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="f772e-124">Design the report format</span></span>
1. <span data-ttu-id="f772e-125">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f772e-125">Click Designer.</span></span>
2. <span data-ttu-id="f772e-126">เปิดใช้งานปุ่มสลับ 'แสดงรายละเอียด'</span><span class="sxs-lookup"><span data-stu-id="f772e-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="f772e-127">ในบานหน้าต่างการดำเนินการ คลิกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="f772e-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="f772e-128">คลิกนำเข้าจาก Excel</span><span class="sxs-lookup"><span data-stu-id="f772e-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="f772e-129">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="f772e-129">Click Attachments.</span></span>
    * <span data-ttu-id="f772e-130">นำเข้าเท็มเพลตของรายงาน </span><span class="sxs-lookup"><span data-stu-id="f772e-130">Import the report’s template.</span></span> <span data-ttu-id="f772e-131">ใช้ไฟล์ Excel ที่คุณดาวน์โหลดมา</span><span class="sxs-lookup"><span data-stu-id="f772e-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="f772e-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f772e-132">Click New.</span></span>
7. <span data-ttu-id="f772e-133">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="f772e-133">Click File.</span></span>
8. <span data-ttu-id="f772e-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f772e-134">Close the page.</span></span>
9. <span data-ttu-id="f772e-135">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f772e-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="f772e-136">เลือกเท็มเพลตที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="f772e-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="f772e-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f772e-137">Click OK.</span></span>
    * <span data-ttu-id="f772e-138">เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="f772e-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="f772e-139">แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงชื่อของมิติทางการเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="f772e-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="f772e-140">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f772e-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="f772e-141">ในแผนภูมิ เลือก 'Excel\Range'</span><span class="sxs-lookup"><span data-stu-id="f772e-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="f772e-142">ในฟิลด์ช่วง Excel พิมพ์ 'DimNames'</span><span class="sxs-lookup"><span data-stu-id="f772e-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="f772e-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="f772e-143">DimNames</span></span>  
14. <span data-ttu-id="f772e-144">ในฟิลด์ทิศทางการจำลอง ให้เลือก 'แนวนอน'</span><span class="sxs-lookup"><span data-stu-id="f772e-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="f772e-145">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f772e-145">Click OK.</span></span>
16. <span data-ttu-id="f772e-146">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="f772e-147">คลิกเลื่อนขึ้น</span><span class="sxs-lookup"><span data-stu-id="f772e-147">Click Move up.</span></span>
18. <span data-ttu-id="f772e-148">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'</span><span class="sxs-lookup"><span data-stu-id="f772e-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="f772e-149">คลิก ตัด</span><span class="sxs-lookup"><span data-stu-id="f772e-149">Click Cut.</span></span>
20. <span data-ttu-id="f772e-150">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="f772e-151">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="f772e-151">Click Paste.</span></span>
22. <span data-ttu-id="f772e-152">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="f772e-153">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="f772e-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="f772e-154">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="f772e-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="f772e-155">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="f772e-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="f772e-156">เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="f772e-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="f772e-157">แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงค่าของมิติทางการเงินเดียวสำหรับแต่ละธุรกรรมการรายงาน</span><span class="sxs-lookup"><span data-stu-id="f772e-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="f772e-158">คลิก เพิ่มช่วง</span><span class="sxs-lookup"><span data-stu-id="f772e-158">Click Add Range.</span></span>
27. <span data-ttu-id="f772e-159">ในฟิลด์ช่วง Excel พิมพ์ 'DimValues'</span><span class="sxs-lookup"><span data-stu-id="f772e-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="f772e-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="f772e-160">DimValues</span></span>  
28. <span data-ttu-id="f772e-161">ในฟิลด์ทิศทางการจำลอง ให้เลือก 'แนวนอน'</span><span class="sxs-lookup"><span data-stu-id="f772e-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="f772e-162">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f772e-162">Click OK.</span></span>
30. <span data-ttu-id="f772e-163">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'</span><span class="sxs-lookup"><span data-stu-id="f772e-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="f772e-164">คลิก ตัด</span><span class="sxs-lookup"><span data-stu-id="f772e-164">Click Cut.</span></span>
32. <span data-ttu-id="f772e-165">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="f772e-166">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="f772e-166">Click Paste.</span></span>
34. <span data-ttu-id="f772e-167">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="f772e-168">แม็ปองค์ประกอบของรูปแบบไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f772e-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="f772e-169">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="f772e-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="f772e-170">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="f772e-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f772e-171">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="f772e-172">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="f772e-173">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="f772e-174">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'</span><span class="sxs-lookup"><span data-stu-id="f772e-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="f772e-175">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="f772e-176">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-176">Click Bind.</span></span>
9. <span data-ttu-id="f772e-177">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="f772e-178">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="f772e-179">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-179">Click Bind.</span></span>
12. <span data-ttu-id="f772e-180">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'</span><span class="sxs-lookup"><span data-stu-id="f772e-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="f772e-181">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เครดิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="f772e-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-182">Click Bind.</span></span>
15. <span data-ttu-id="f772e-183">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'</span><span class="sxs-lookup"><span data-stu-id="f772e-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="f772e-184">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เดบิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="f772e-185">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-185">Click Bind.</span></span>
18. <span data-ttu-id="f772e-186">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'</span><span class="sxs-lookup"><span data-stu-id="f772e-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="f772e-187">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\สกุลเงิน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="f772e-188">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-188">Click Bind.</span></span>
21. <span data-ttu-id="f772e-189">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'</span><span class="sxs-lookup"><span data-stu-id="f772e-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="f772e-190">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\วันที่: วันที่'</span><span class="sxs-lookup"><span data-stu-id="f772e-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="f772e-191">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-191">Click Bind.</span></span>
24. <span data-ttu-id="f772e-192">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'</span><span class="sxs-lookup"><span data-stu-id="f772e-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="f772e-193">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ใบสำคัญ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="f772e-194">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-194">Click Bind.</span></span>
27. <span data-ttu-id="f772e-195">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'</span><span class="sxs-lookup"><span data-stu-id="f772e-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="f772e-196">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="f772e-197">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-197">Click Bind.</span></span>
30. <span data-ttu-id="f772e-198">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="f772e-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="f772e-199">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="f772e-200">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-200">Click Bind.</span></span>
33. <span data-ttu-id="f772e-201">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'</span><span class="sxs-lookup"><span data-stu-id="f772e-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="f772e-202">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="f772e-203">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-203">Click Bind.</span></span>
36. <span data-ttu-id="f772e-204">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="f772e-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="f772e-205">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="f772e-206">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-206">Click Bind.</span></span>
39. <span data-ttu-id="f772e-207">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="f772e-208">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="f772e-209">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'</span><span class="sxs-lookup"><span data-stu-id="f772e-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="f772e-210">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-210">Click Bind.</span></span>
43. <span data-ttu-id="f772e-211">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="f772e-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="f772e-212">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="f772e-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="f772e-213">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-213">Click Bind.</span></span>
46. <span data-ttu-id="f772e-214">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'</span><span class="sxs-lookup"><span data-stu-id="f772e-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="f772e-215">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\บริษัท: สตริง'</span><span class="sxs-lookup"><span data-stu-id="f772e-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="f772e-216">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f772e-216">Click Bind.</span></span>
49. <span data-ttu-id="f772e-217">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f772e-217">Click Save.</span></span>
50. <span data-ttu-id="f772e-218">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f772e-218">Close the page.</span></span>


