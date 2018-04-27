--- 
title: "ออกแบบรูปแบบเพื่อใช้ช่วงขยายในแนวนอนเพื่อเพิ่มคอลัมน์ในรายงาน Excel แบบไดนามิก"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9c3cf17cd406a50a9f92e78991289f9139d7c73
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="67640-103">ออกแบบรูปแบบเพื่อใช้ช่วงขยายในแนวนอนเพื่อเพิ่มคอลัมน์ในรายงาน Excel แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="67640-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67640-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน </span><span class="sxs-lookup"><span data-stu-id="67640-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="67640-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="67640-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="67640-106">เพื่อทำตามขั้นตอนเหล่านี้ ก่อนอื่นคุณต้องดำเนินการตามคำแนะนำงานสามรายการนี้:</span><span class="sxs-lookup"><span data-stu-id="67640-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="67640-107">”สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของ ER”</span><span class="sxs-lookup"><span data-stu-id="67640-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="67640-108">”ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: ออกแบบแบบจำลองข้อมูล)”</span><span class="sxs-lookup"><span data-stu-id="67640-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="67640-109">”ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)”</span><span class="sxs-lookup"><span data-stu-id="67640-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="67640-110">นอกจากนี้ คุณยังต้องดาวน์โหลดและบันทึกสำเนาเฉพาะที่ของเท็มเพลตที่มีรายงานตัวอย่างซึ่งดูได้ที่นี่ [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266)</span><span class="sxs-lookup"><span data-stu-id="67640-110">You must also download and save a local copy of the template with a sample report found here, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 


<span data-ttu-id="67640-111">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="67640-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="67640-112">สร้างการตั้งค่าคอนฟิกรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="67640-112">Create a new report configuration</span></span>
1. <span data-ttu-id="67640-113">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="67640-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="67640-114">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="67640-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="67640-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="67640-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="67640-116">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="67640-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="67640-117">ใช้แบบจำลองที่สร้างขึ้นล่วงหน้าเป็นแหล่งข้อมูลสำหรับรายงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="67640-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="67640-118">ในฟิลด์ชื่อ พิมพ์ 'ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน'</span><span class="sxs-lookup"><span data-stu-id="67640-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="67640-119">ตัวอย่างรายงานที่มีช่วงที่สามารถขยายได้ในแนวนอน</span><span class="sxs-lookup"><span data-stu-id="67640-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="67640-120">ในฟิลด์คำอธิบาย พิมพ์ 'เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก'</span><span class="sxs-lookup"><span data-stu-id="67640-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="67640-121">เพื่อสร้างผลลัพธ์ Excel ด้วยการเพิ่มคอลัมน์แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="67640-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="67640-122">ในฟิลด์คำนิยามแบบจำลองข้อมูล ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="67640-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="67640-123">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="67640-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="67640-124">ออกแบบรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="67640-124">Design the report format</span></span>
1. <span data-ttu-id="67640-125">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="67640-125">Click Designer.</span></span>
2. <span data-ttu-id="67640-126">เปิดใช้งานปุ่มสลับ 'แสดงรายละเอียด'</span><span class="sxs-lookup"><span data-stu-id="67640-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="67640-127">ในบานหน้าต่างการดำเนินการ คลิกนำเข้า</span><span class="sxs-lookup"><span data-stu-id="67640-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="67640-128">คลิกนำเข้าจาก Excel</span><span class="sxs-lookup"><span data-stu-id="67640-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="67640-129">คลิกสิ่งที่แนบ</span><span class="sxs-lookup"><span data-stu-id="67640-129">Click Attachments.</span></span>
    * <span data-ttu-id="67640-130">นำเข้าเท็มเพลตของรายงาน </span><span class="sxs-lookup"><span data-stu-id="67640-130">Import the report’s template.</span></span> <span data-ttu-id="67640-131">ใช้ไฟล์ Excel ที่คุณดาวน์โหลดมา</span><span class="sxs-lookup"><span data-stu-id="67640-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="67640-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="67640-132">Click New.</span></span>
7. <span data-ttu-id="67640-133">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="67640-133">Click File.</span></span>
8. <span data-ttu-id="67640-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67640-134">Close the page.</span></span>
9. <span data-ttu-id="67640-135">ในฟิลด์เท็มเพลต ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="67640-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="67640-136">เลือกเท็มเพลตที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="67640-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="67640-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="67640-137">Click OK.</span></span>
    * <span data-ttu-id="67640-138">เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="67640-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="67640-139">แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงชื่อของมิติทางการเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="67640-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="67640-140">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="67640-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="67640-141">ในแผนภูมิ เลือก 'Excel\Range'</span><span class="sxs-lookup"><span data-stu-id="67640-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="67640-142">ในฟิลด์ช่วง Excel พิมพ์ 'DimNames'</span><span class="sxs-lookup"><span data-stu-id="67640-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="67640-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="67640-143">DimNames</span></span>  
14. <span data-ttu-id="67640-144">ในฟิลด์ทิศทางการจำลอง ให้เลือก 'แนวนอน'</span><span class="sxs-lookup"><span data-stu-id="67640-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="67640-145">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="67640-145">Click OK.</span></span>
16. <span data-ttu-id="67640-146">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="67640-147">คลิกเลื่อนขึ้น</span><span class="sxs-lookup"><span data-stu-id="67640-147">Click Move up.</span></span>
18. <span data-ttu-id="67640-148">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'</span><span class="sxs-lookup"><span data-stu-id="67640-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="67640-149">คลิก ตัด</span><span class="sxs-lookup"><span data-stu-id="67640-149">Click Cut.</span></span>
20. <span data-ttu-id="67640-150">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="67640-151">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="67640-151">Click Paste.</span></span>
22. <span data-ttu-id="67640-152">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="67640-153">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="67640-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="67640-154">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="67640-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="67640-155">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="67640-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="67640-156">เพิ่มช่วงใหม่เพื่อสร้างแบบผลลัพธ์ Excel แบบไดนามิกด้วยจำนวนคอลัมน์ที่มากเท่ากับที่คุณเลือก (ในแบบฟอร์มกล่องโต้ตอบผู้ใช้) สำหรับมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="67640-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="67640-157">แต่ละเซลล์สำหรับทุกคอลัมน์จะแสดงถึงค่าของมิติทางการเงินเดียวสำหรับแต่ละธุรกรรมการรายงาน</span><span class="sxs-lookup"><span data-stu-id="67640-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="67640-158">คลิก เพิ่มช่วง</span><span class="sxs-lookup"><span data-stu-id="67640-158">Click Add Range.</span></span>
27. <span data-ttu-id="67640-159">ในฟิลด์ช่วง Excel พิมพ์ 'DimValues'</span><span class="sxs-lookup"><span data-stu-id="67640-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="67640-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="67640-160">DimValues</span></span>  
28. <span data-ttu-id="67640-161">ในฟิลด์ทิศทางการจำลอง ให้เลือก 'แนวนอน'</span><span class="sxs-lookup"><span data-stu-id="67640-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="67640-162">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="67640-162">Click OK.</span></span>
30. <span data-ttu-id="67640-163">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'</span><span class="sxs-lookup"><span data-stu-id="67640-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="67640-164">คลิก ตัด</span><span class="sxs-lookup"><span data-stu-id="67640-164">Click Cut.</span></span>
32. <span data-ttu-id="67640-165">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="67640-166">คลิก วาง</span><span class="sxs-lookup"><span data-stu-id="67640-166">Click Paste.</span></span>
34. <span data-ttu-id="67640-167">ในแผนภูมิ ขยาย 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="67640-168">แม็ปองค์ประกอบของรูปแบบไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="67640-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="67640-169">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="67640-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="67640-170">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="67640-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="67640-171">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="67640-172">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="67640-173">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="67640-174">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'</span><span class="sxs-lookup"><span data-stu-id="67640-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="67640-175">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="67640-176">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-176">Click Bind.</span></span>
9. <span data-ttu-id="67640-177">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="67640-178">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ข้อมูลมิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="67640-179">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-179">Click Bind.</span></span>
12. <span data-ttu-id="67640-180">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'</span><span class="sxs-lookup"><span data-stu-id="67640-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="67640-181">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เครดิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="67640-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="67640-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-182">Click Bind.</span></span>
15. <span data-ttu-id="67640-183">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'</span><span class="sxs-lookup"><span data-stu-id="67640-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="67640-184">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\เดบิต: จริง'</span><span class="sxs-lookup"><span data-stu-id="67640-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="67640-185">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-185">Click Bind.</span></span>
18. <span data-ttu-id="67640-186">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'</span><span class="sxs-lookup"><span data-stu-id="67640-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="67640-187">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\สกุลเงิน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="67640-188">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-188">Click Bind.</span></span>
21. <span data-ttu-id="67640-189">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'</span><span class="sxs-lookup"><span data-stu-id="67640-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="67640-190">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\วันที่: วันที่'</span><span class="sxs-lookup"><span data-stu-id="67640-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="67640-191">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-191">Click Bind.</span></span>
24. <span data-ttu-id="67640-192">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'</span><span class="sxs-lookup"><span data-stu-id="67640-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="67640-193">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด\ใบสำคัญ: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="67640-194">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-194">Click Bind.</span></span>
27. <span data-ttu-id="67640-195">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'</span><span class="sxs-lookup"><span data-stu-id="67640-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="67640-196">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="67640-197">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-197">Click Bind.</span></span>
30. <span data-ttu-id="67640-198">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="67640-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="67640-199">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ธุรกรรม: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="67640-200">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-200">Click Bind.</span></span>
33. <span data-ttu-id="67640-201">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'</span><span class="sxs-lookup"><span data-stu-id="67640-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="67640-202">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด\ชุดงาน: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="67640-203">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-203">Click Bind.</span></span>
36. <span data-ttu-id="67640-204">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'</span><span class="sxs-lookup"><span data-stu-id="67640-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="67640-205">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\สมุดรายวัน: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="67640-206">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-206">Click Bind.</span></span>
39. <span data-ttu-id="67640-207">ในแผนภูมิ ขยาย 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="67640-208">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด\รหัส: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="67640-209">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'</span><span class="sxs-lookup"><span data-stu-id="67640-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="67640-210">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-210">Click Bind.</span></span>
43. <span data-ttu-id="67640-211">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\การตั้งค่ามิติ: รายการเรกคอร์ด'</span><span class="sxs-lookup"><span data-stu-id="67640-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="67640-212">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'</span><span class="sxs-lookup"><span data-stu-id="67640-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="67640-213">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-213">Click Bind.</span></span>
46. <span data-ttu-id="67640-214">ในแผนภูมิ เลือก 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'</span><span class="sxs-lookup"><span data-stu-id="67640-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="67640-215">ในแผนภูมิ เลือก 'แบบจำลอง: แบบจำลองข้อมูลแบบจำลองตัวอย่างมิติทางการเงิน\บริษัท: สตริง'</span><span class="sxs-lookup"><span data-stu-id="67640-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="67640-216">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="67640-216">Click Bind.</span></span>
49. <span data-ttu-id="67640-217">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="67640-217">Click Save.</span></span>
50. <span data-ttu-id="67640-218">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67640-218">Close the page.</span></span>


