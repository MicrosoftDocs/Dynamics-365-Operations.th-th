---
title: ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1 - ออกแบบรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์เวิร์กชีต OPENXML (Excel) (ส่วนที่ 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5119255b119a99f3809d2d75bbfdc7b3bad9932
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569568"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="c2bc3-104">ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1 - ออกแบบรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="c2bc3-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2bc3-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน </span><span class="sxs-lookup"><span data-stu-id="c2bc3-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="c2bc3-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="c2bc3-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="c2bc3-107">เพื่อทำตามขั้นตอนเหล่านี้ ก่อนอื่นคุณต้องดำเนินการตามคำแนะนำงานสามรายการนี้:</span><span class="sxs-lookup"><span data-stu-id="c2bc3-107">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="c2bc3-108">"ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="c2bc3-108">"ER Create a configuration provider and mark it as active"</span></span>

<span data-ttu-id="c2bc3-109">"ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: ออกแบบแบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="c2bc3-109">"ER Use financial dimensions as a data source (Part 1: Design data model)"</span></span>

<span data-ttu-id="c2bc3-110">"ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)"</span><span class="sxs-lookup"><span data-stu-id="c2bc3-110">"ER Use financial dimensions as a data source (Part 2: Model mapping)"</span></span>

<span data-ttu-id="c2bc3-111">นอกจากนี้ คุณยังต้องดาวน์โหลดและบันทึกสำเนาเฉพาะที่ของเท็มเพลตกับรายงานตัวอย่างที่พบที่นี่ [รายงานเว็บเซอร์วิสของมิติทางการเงินตัวอย่าง](https://go.microsoft.com/fwlink/?linkid=862266)</span><span class="sxs-lookup"><span data-stu-id="c2bc3-111">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="c2bc3-112">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="c2bc3-112">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="c2bc3-113">สร้างการตั้งค่าคอนฟิกรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c2bc3-113">Create a new report configuration</span></span>
1. <span data-ttu-id="c2bc3-114">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c2bc3-115">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-115">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c2bc3-116">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-116">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="c2bc3-117">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-117">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="c2bc3-118">ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c2bc3-118">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="c2bc3-119">ในฟิลด์ชื่อ พิมพ์ 'ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-119">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="c2bc3-120">ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน</span><span class="sxs-lookup"><span data-stu-id="c2bc3-120">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="c2bc3-121">ในฟิลด์คำอธิบาย พิมพ์ 'เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-121">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="c2bc3-122">เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-122">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="c2bc3-123">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="c2bc3-123">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="c2bc3-124">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-124">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="c2bc3-125">ออกแบบรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="c2bc3-125">Design the report format</span></span>
1. <span data-ttu-id="c2bc3-126">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c2bc3-126">Click Designer.</span></span>
2. <span data-ttu-id="c2bc3-127">เปิดใช้งานปุ่มสลับ 'แสดงรายละเอียด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-127">Turn on the 'Show details' toggle button.</span></span>
3. <span data-ttu-id="c2bc3-128">ในบานหน้าต่างการดำเนินการ คลิกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="c2bc3-128">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="c2bc3-129">คลิกนำเข้าจาก Excel</span><span class="sxs-lookup"><span data-stu-id="c2bc3-129">Click Import from Excel.</span></span>
5. <span data-ttu-id="c2bc3-130">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="c2bc3-130">Click Attachments.</span></span>
    * <span data-ttu-id="c2bc3-131">นำเข้าเท็มเพลตของรายงาน</span><span class="sxs-lookup"><span data-stu-id="c2bc3-131">Import the report's template.</span></span> <span data-ttu-id="c2bc3-132">ใช้ไฟล์ Excel ที่คุณดาวน์โหลดมา</span><span class="sxs-lookup"><span data-stu-id="c2bc3-132">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="c2bc3-133">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-133">Click New.</span></span>
7. <span data-ttu-id="c2bc3-134">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="c2bc3-134">Click File.</span></span>
8. <span data-ttu-id="c2bc3-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c2bc3-135">Close the page.</span></span>
9. <span data-ttu-id="c2bc3-136">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c2bc3-136">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="c2bc3-137">เลือกเท็มเพลตที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="c2bc3-137">Select the downloaded template.</span></span>  
10. <span data-ttu-id="c2bc3-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-138">Click OK.</span></span>
    * <span data-ttu-id="c2bc3-139">เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="c2bc3-139">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="c2bc3-140">แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงชื่อของมิติทางการเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="c2bc3-140">Each cell for every column will represent a single financial dimension's name.</span></span>  
11. <span data-ttu-id="c2bc3-141">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-141">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="c2bc3-142">ในแผนภูมิ เลือก 'Excel\Range'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-142">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="c2bc3-143">ในฟิลด์ช่วง Excel พิมพ์ 'DimNames'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-143">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="c2bc3-144">DimNames</span><span class="sxs-lookup"><span data-stu-id="c2bc3-144">DimNames</span></span>  
14. <span data-ttu-id="c2bc3-145">ในฟิลด์ทิศทางการจำลอง ให้เลือก 'แนวนอน'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-145">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="c2bc3-146">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2bc3-146">Click OK.</span></span>
16. <span data-ttu-id="c2bc3-147">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-147">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="c2bc3-148">คลิกเลื่อนขึ้น</span><span class="sxs-lookup"><span data-stu-id="c2bc3-148">Click Move up.</span></span>
18. <span data-ttu-id="c2bc3-149">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-149">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="c2bc3-150">คลิก ตัด</span><span class="sxs-lookup"><span data-stu-id="c2bc3-150">Click Cut.</span></span>
20. <span data-ttu-id="c2bc3-151">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-151">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="c2bc3-152">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-152">Click Paste.</span></span>
22. <span data-ttu-id="c2bc3-153">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="c2bc3-154">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="c2bc3-155">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-155">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="c2bc3-156">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-156">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="c2bc3-157">เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="c2bc3-157">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="c2bc3-158">แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงค่าของมิติทางการเงินเดียวสำหรับธุรกรรมการรายงานแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="c2bc3-158">Each cell for every column will represent a single financial dimension's value for each reporting transaction.</span></span>  
26. <span data-ttu-id="c2bc3-159">คลิก เพิ่มช่วง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-159">Click Add Range.</span></span>
27. <span data-ttu-id="c2bc3-160">ในฟิลด์ช่วง Excel พิมพ์ 'DimValues'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-160">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="c2bc3-161">DimValues</span><span class="sxs-lookup"><span data-stu-id="c2bc3-161">DimValues</span></span>  
28. <span data-ttu-id="c2bc3-162">ในฟิลด์ทิศทางการจำลอง ให้เลือก 'แนวนอน'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-162">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="c2bc3-163">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c2bc3-163">Click OK.</span></span>
30. <span data-ttu-id="c2bc3-164">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-164">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="c2bc3-165">คลิก ตัด</span><span class="sxs-lookup"><span data-stu-id="c2bc3-165">Click Cut.</span></span>
32. <span data-ttu-id="c2bc3-166">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-166">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="c2bc3-167">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="c2bc3-167">Click Paste.</span></span>
34. <span data-ttu-id="c2bc3-168">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-168">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="c2bc3-169">แม็ปองค์ประกอบของรูปแบบไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c2bc3-169">Map format elements to data sources</span></span>
1. <span data-ttu-id="c2bc3-170">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="c2bc3-170">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c2bc3-171">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-171">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c2bc3-172">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="c2bc3-173">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="c2bc3-174">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="c2bc3-175">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-175">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="c2bc3-176">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-176">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="c2bc3-177">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-177">Click Bind.</span></span>
9. <span data-ttu-id="c2bc3-178">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-178">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="c2bc3-179">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="c2bc3-180">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-180">Click Bind.</span></span>
12. <span data-ttu-id="c2bc3-181">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-181">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="c2bc3-182">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เครดิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="c2bc3-183">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-183">Click Bind.</span></span>
15. <span data-ttu-id="c2bc3-184">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-184">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="c2bc3-185">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เดบิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="c2bc3-186">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-186">Click Bind.</span></span>
18. <span data-ttu-id="c2bc3-187">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-187">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="c2bc3-188">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\สกุลเงิน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-188">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="c2bc3-189">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-189">Click Bind.</span></span>
21. <span data-ttu-id="c2bc3-190">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-190">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="c2bc3-191">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\วันที่: วันที่'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="c2bc3-192">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-192">Click Bind.</span></span>
24. <span data-ttu-id="c2bc3-193">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-193">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="c2bc3-194">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ใบสำคัญ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="c2bc3-195">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-195">Click Bind.</span></span>
27. <span data-ttu-id="c2bc3-196">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-196">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="c2bc3-197">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="c2bc3-198">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-198">Click Bind.</span></span>
30. <span data-ttu-id="c2bc3-199">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-199">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="c2bc3-200">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="c2bc3-201">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-201">Click Bind.</span></span>
33. <span data-ttu-id="c2bc3-202">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-202">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="c2bc3-203">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="c2bc3-204">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-204">Click Bind.</span></span>
36. <span data-ttu-id="c2bc3-205">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-205">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="c2bc3-206">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="c2bc3-207">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-207">Click Bind.</span></span>
39. <span data-ttu-id="c2bc3-208">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-208">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="c2bc3-209">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-209">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="c2bc3-210">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-210">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="c2bc3-211">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-211">Click Bind.</span></span>
43. <span data-ttu-id="c2bc3-212">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-212">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="c2bc3-213">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-213">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="c2bc3-214">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-214">Click Bind.</span></span>
46. <span data-ttu-id="c2bc3-215">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-215">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="c2bc3-216">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\บริษัท: สตริง'</span><span class="sxs-lookup"><span data-stu-id="c2bc3-216">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="c2bc3-217">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-217">Click Bind.</span></span>
49. <span data-ttu-id="c2bc3-218">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c2bc3-218">Click Save.</span></span>
50. <span data-ttu-id="c2bc3-219">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c2bc3-219">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]