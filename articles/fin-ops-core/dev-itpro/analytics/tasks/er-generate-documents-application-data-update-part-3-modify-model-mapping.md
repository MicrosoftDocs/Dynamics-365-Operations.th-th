---
title: แก้ไขแบบจำลองและการแมปเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน
description: หัวข้อนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงาน เพื่อสร้างเอกสารอิเล็กทรอนิกส์ส์และอัพเดตข้อมูลแอพลิเคชัน (ส่วนที่ 2 - สร้างเอกสาร)
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751617"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="fa4d5-104">แก้ไขแบบจำลองและการแมปเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa4d5-105">เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน “ER สร้างเอกสารที่มีการปรับปรุงข้อมูลแอพลิเคชัน (ส่วนที่ 2: สร้างเอกสาร)“ ให้เสร็จเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="fa4d5-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="fa4d5-106">ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ส์และอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="fa4d5-107">ในกระบวนงานนี้ คุณจะปรับเปลี่ยนการตั้งค่าคอนฟิก ER เพื่อเริ่มต้นการใช้งานเพื่อสร้างเอกสารอิเล็กทรอนิกส์ และอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="fa4d5-108">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fa4d5-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="fa4d5-109">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF</span><span class="sxs-lookup"><span data-stu-id="fa4d5-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="fa4d5-110">ปรับเปลี่ยนแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fa4d5-110">Modify data model</span></span>
1. <span data-ttu-id="fa4d5-111">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fa4d5-112">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="fa4d5-113">คุณจะขยายวิธีใช้แบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fa4d5-113">You will extend how you use the data model.</span></span> <span data-ttu-id="fa4d5-114">นอกจากการใช้เป็นแหล่งข้อมูลในการสร้างรายงานอินทราสแทต จะมีการใช้แบบจำลองข้อมูลเพื่อรวบรวมรายละเอียดเกี่ยวกับกระบวนการการรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="fa4d5-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="fa4d5-115">จากนั้นจะมีการใช้รายละเอียดเพื่ออัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="fa4d5-116">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fa4d5-116">Click Designer.</span></span>
4. <span data-ttu-id="fa4d5-117">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="fa4d5-118">ในฟิลด์สร้างโหนดใหม่เป็น ให้ป้อน 'รากแบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="fa4d5-119">ในฟิลด์ชื่อ ให้พิมพ์ 'สำหรับการอัพเดตข้อมูลแอพลิเคชัน'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="fa4d5-120">สำหรับการอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-120">For application data update</span></span>  
7. <span data-ttu-id="fa4d5-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-121">Click Add.</span></span>
8. <span data-ttu-id="fa4d5-122">ในแผนภูมิ เลือก 'สำหรับการอัพเดตข้อมูลแอพลิเคชัน'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="fa4d5-123">มีการเพิ่มรายการรากใหม่นี้เพื่อระบุลำดับข้อมูลสำหรับการย้ายข้อมูลจากรายงานอินทราสแทต (ซึ่งใช้เป็นแหล่งข้อมูล) ไปยังตารางแอพลิเคชัน (ปลายทางการอัพเดต)</span><span class="sxs-lookup"><span data-stu-id="fa4d5-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="fa4d5-124">หมายเหตุว่าต้องใช้รายการรากที่แตกต่างกันสำหรับการเรียกข้อมูลที่มีการลงรายการบัญชีเอกสารขาออกและสำหรับการเรียกข้อมูลจากเอกสารที่ใช้เพื่ออัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="fa4d5-125">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="fa4d5-126">ในฟิลด์ชื่อ ให้พิมพ์ 'ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="fa4d5-127">ส่วนหัวที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-127">Archive header</span></span>  
11. <span data-ttu-id="fa4d5-128">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="fa4d5-129">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-129">Click Add.</span></span>
    * <span data-ttu-id="fa4d5-130">เนื่องจากคุณจะสร้างเรกคอร์ดสำหรับแต่ละรายงานอินทราสแทตที่ถูกสร้างขึ้น คุณจะต้องสร้างรายการใหม่สำหรับรายการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="fa4d5-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="fa4d5-131">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="fa4d5-132">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="fa4d5-133">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="fa4d5-133">File name</span></span>  
15. <span data-ttu-id="fa4d5-134">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="fa4d5-135">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-135">Click Add.</span></span>
17. <span data-ttu-id="fa4d5-136">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="fa4d5-137">ในฟิลด์ชื่อ ให้พิมพ์ 'จำนวนของรายการ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="fa4d5-138">จำนวนของรายการ</span><span class="sxs-lookup"><span data-stu-id="fa4d5-138">Number of lines</span></span>  
19. <span data-ttu-id="fa4d5-139">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนเต็ม'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="fa4d5-140">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-140">Click Add.</span></span>
    * <span data-ttu-id="fa4d5-141">เพิ่มรายการนี้เพื่อแสดงหมายเลขของธุรกรรมอินทราสแทตที่ถูกรายงานในระหว่างกระบวนการรายงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="fa4d5-142">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="fa4d5-143">ในฟิลด์ชื่อ ให้พิมพ์ 'รายการที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="fa4d5-144">รายการที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-144">Archive lines</span></span>  
23. <span data-ttu-id="fa4d5-145">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="fa4d5-146">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-146">Click Add.</span></span>
    * <span data-ttu-id="fa4d5-147">เพิ่มรายการนี้เพื่อแสดงรายการของธุรกรรมอินทราสแทตที่ถูกรายงานในระหว่างกระบวนการรายงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="fa4d5-148">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="fa4d5-149">ในฟิลด์ชื่อ พิมพ์ 'จำนวน'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="fa4d5-150">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-150">Amount</span></span>  
27. <span data-ttu-id="fa4d5-151">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="fa4d5-152">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-152">Click Add.</span></span>
29. <span data-ttu-id="fa4d5-153">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="fa4d5-154">ในฟิลด์ชื่อ พิมพ์ 'รหัสเรกคอร์ดโภคภัณฑ์'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="fa4d5-155">รหัสเรกคอร์ดโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fa4d5-155">Commodity rec id</span></span>  
31. <span data-ttu-id="fa4d5-156">ในฟิลด์ประเภทสินค้า ให้เลือก 'Int64'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="fa4d5-157">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-157">Click Add.</span></span>
33. <span data-ttu-id="fa4d5-158">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="fa4d5-159">ในฟิลด์ชื่อ ให้พิมพ์ 'หมายเลขสินค้า'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="fa4d5-160">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="fa4d5-160">Item number</span></span>  
35. <span data-ttu-id="fa4d5-161">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="fa4d5-162">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-162">Click Add.</span></span>
37. <span data-ttu-id="fa4d5-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-163">Click Save.</span></span>
38. <span data-ttu-id="fa4d5-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fa4d5-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="fa4d5-165">ปรับปรุงการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-165">Modify model mapping</span></span>
1. <span data-ttu-id="fa4d5-166">ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="fa4d5-167">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (การแม็ป)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="fa4d5-168">ปรับเปลี่ยนการแม็ปแบบจำลองที่มีอยู่เพื่อเริ่มต้นการใช้สำหรับการอัพเดตข้อมูลแอพลิเคชัน และเพื่อเก็บรายละเอียดการรายงานอินทราสแทตถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="fa4d5-169">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fa4d5-169">Click Designer.</span></span>
4. <span data-ttu-id="fa4d5-170">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-170">Click New.</span></span>
5. <span data-ttu-id="fa4d5-171">ในฟิลด์ชื่อ ให้พิมพ์ 'อัพเดตที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="fa4d5-172">อัพเดตที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-172">Update archive</span></span>  
6. <span data-ttu-id="fa4d5-173">ในฟิลด์ทิศทาง ให้เลือก 'ไปยังปลายทาง'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="fa4d5-174">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-174">Click Save.</span></span>
    * <span data-ttu-id="fa4d5-175">การแม็ปใหม่นี้จะระบุลำดับข้อมูลสำหรับการย้ายข้อมูล (รายละเอียดการรายงานอินทราสแทต) จากแบบจำลองข้อมูลไปยังตารางแอพลิเคชัน (ปลายทางการอัพเดต)</span><span class="sxs-lookup"><span data-stu-id="fa4d5-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="fa4d5-176">หมายเหตุว่าต้องใช้รายการรากของแบบจำลองที่แตกต่างกันเพื่อเรียกข้อมูลจากแอพลิเคชันสำหรับกระบวนการรายงาน แล้วจึงใช้ข้อมูลจากแบบจำลองข้อมูลสำหรับการปรับปรุงข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="fa4d5-177">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fa4d5-177">Click Designer.</span></span>
9. <span data-ttu-id="fa4d5-178">ในแผนภูมิ เลือก 'แบบจำลองข้อมูล\แบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="fa4d5-179">เพิ่มแหล่งข้อมูลที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="fa4d5-179">Add the required data source.</span></span> <span data-ttu-id="fa4d5-180">นี่คือแบบจำลองข้อมูลที่ประกอบด้วยรายละเอียดเกี่ยวกับธุรกรรมอินทราสแทตที่รายงานที่จะต้องถูกเก็บไว้ถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="fa4d5-181">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-181">Click Add root.</span></span>
11. <span data-ttu-id="fa4d5-182">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="fa4d5-183">แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-183">model</span></span>  
12. <span data-ttu-id="fa4d5-184">ในฟิลด์คำนิยาม ป้อนหรือเลือกค่า 'สำหรับการปรับปรุงข้อมูลแอพลิเคชัน'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="fa4d5-185">สำหรับการอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-185">For application data update</span></span>  
13. <span data-ttu-id="fa4d5-186">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="fa4d5-186">Click OK.</span></span>
14. <span data-ttu-id="fa4d5-187">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="fa4d5-188">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="fa4d5-189">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="fa4d5-190">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-190">Click Add.</span></span>
    * <span data-ttu-id="fa4d5-191">เนื่องจากคุณต้องการระบุธุรกรรมอินทราสแทตที่มีการรายงานสำหรับการเก็บถาวร คุณจะต้องเพิ่มแหล่งข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="fa4d5-192">ในฟิลด์ชื่อ ให้พิมพ์ 'รายการที่ระบุ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="fa4d5-193">รายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fa4d5-193">Enumerated lines</span></span>  
19. <span data-ttu-id="fa4d5-194">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-194">Click Edit formula.</span></span>
20. <span data-ttu-id="fa4d5-195">ในแผนภูมิ ให้เลือก 'รายการ\แจงนับ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="fa4d5-196">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-196">Click Add function.</span></span>
22. <span data-ttu-id="fa4d5-197">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="fa4d5-198">ในแผนภูมิ ให้ขยาย 'แบบจำลอง\ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="fa4d5-199">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="fa4d5-200">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fa4d5-200">Click Add data source.</span></span>
26. <span data-ttu-id="fa4d5-201">ในฟิลด์สูตร ให้ป้อน 'ENUMERATE(model.'Archive header'.'Archive lines')'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="fa4d5-202">แจงนับ (แบบจำลอง 'ส่วนหัวที่เก็บถาวร' 'รายการที่เก็บถาวร')</span><span class="sxs-lookup"><span data-stu-id="fa4d5-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="fa4d5-203">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-203">Click Save.</span></span>
28. <span data-ttu-id="fa4d5-204">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fa4d5-204">Close the page.</span></span>
29. <span data-ttu-id="fa4d5-205">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-205">Click OK.</span></span>
30. <span data-ttu-id="fa4d5-206">คลิก เพิ่มปลายทาง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-206">Click Add destination.</span></span>
    * <span data-ttu-id="fa4d5-207">เพิ่มตารางแอพลิเคชันเป็นปลายทางจำเป็นที่จำเป็นต้องอัพเดตเพื่อเก็บถาวรรายละเอียดของธุรกรรมอินทราสแทตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="fa4d5-208">ในฟิลด์ชื่อ ให้พิมพ์ 'ที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="fa4d5-209">เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-209">Archive</span></span>  
32. <span data-ttu-id="fa4d5-210">ในฟิลด์ชื่อตาราง ให้พิมพ์ 'IntrastatArchiveGeneral'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="fa4d5-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="fa4d5-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="fa4d5-212">รักษาการดำเนินการเรกคอร์ด 'แทรก' เพื่อให้คุณสามารถเพิ่มเรกคอร์ดในระหว่างการเก็บรายละเอียดของแต่ละกระบวนการรายงานอินทราสแทตโดยถาวร</span><span class="sxs-lookup"><span data-stu-id="fa4d5-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="fa4d5-213">เลือก ใช่ ในฟิลด์ infolog เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="fa4d5-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="fa4d5-214">เลือก ใช่ เพื่อเรียกดูข้อมูลของปัญหาเกี่ยวกับการอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fa4d5-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="fa4d5-215">เลือก ใช่ ในฟิลด์ ข้ามการตรวจสอบความถูกต้องในการดำเนินการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="fa4d5-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="fa4d5-216">เลือก ใช่ เพื่อระงับข้อผิดพลาดเกี่ยวกับการตรวจสอบความถูกต้องเกี่ยวกับฟิลด์ 'รหัสที่เก็บถาวรของอินทราสแทต' ที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="fa4d5-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="fa4d5-217">ซึ่งจะสามารถทำได้หลังจากที่มีการเพิ่มเรกคอร์ดตามการตั้งค่าหมายเลขลำดับที่ถูกตั้งค่าคอนฟิกสำหรับตารางนี้ในแบบฟอร์มพารามิเตอร์การค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="fa4d5-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="fa4d5-218">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fa4d5-218">Click OK.</span></span>
    * <span data-ttu-id="fa4d5-219">ผูกองค์ประกอบของแหล่งข้อมูลที่เพิ่มเข้ามา (แบบจำลองที่มีการกรองข้อมูลตามรายการรากที่เลือก) ด้วยองค์ประกอบจากปลายทางที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fa4d5-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="fa4d5-220">ในแผนภูมิ ให้ขยาย 'ที่เก็บถาวระ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="fa4d5-221">ในแผนภูมิ ให้ขยาย 'ที่เก็บถาวร\<ความสัมพันธ์'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="fa4d5-222">ในแผนภูมิ ขยาย 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetail'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="fa4d5-223">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailAmount(AmountMST)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="fa4d5-224">ในแผนภูมิ ให้ขยาย 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="fa4d5-225">ในแผนภูมิ ให้ขยาย 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\ค่า'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="fa4d5-226">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\ค่า\ยอดเงิน'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="fa4d5-227">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-227">Click Bind.</span></span>
44. <span data-ttu-id="fa4d5-228">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailCommodity(IntrastatCommodity)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="fa4d5-229">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุค่า\รหัสเรกคอร์ดโภคภัณฑ์'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="fa4d5-230">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-230">Click Bind.</span></span>
47. <span data-ttu-id="fa4d5-231">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailItem number(ItemId)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="fa4d5-232">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\ค่า\หมายเลขสินค้า'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="fa4d5-233">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-233">Click Bind.</span></span>
50. <span data-ttu-id="fa4d5-234">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailLine number(LineNumber)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="fa4d5-235">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="fa4d5-236">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-236">Click Bind.</span></span>
53. <span data-ttu-id="fa4d5-237">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetail'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="fa4d5-238">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="fa4d5-239">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-239">Click Bind.</span></span>
56. <span data-ttu-id="fa4d5-240">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\ชื่อไฟล์(FileName)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="fa4d5-241">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="fa4d5-242">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-242">Click Bind.</span></span>
59. <span data-ttu-id="fa4d5-243">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\จำนวนของรายการ(NumberOfLines)'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="fa4d5-244">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\จำนวนของรายการ'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="fa4d5-245">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-245">Click Bind.</span></span>
62. <span data-ttu-id="fa4d5-246">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="fa4d5-247">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="fa4d5-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="fa4d5-248">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-248">Click Bind.</span></span>
65. <span data-ttu-id="fa4d5-249">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fa4d5-249">Click Save.</span></span>
66. <span data-ttu-id="fa4d5-250">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fa4d5-250">Close the page.</span></span>
67. <span data-ttu-id="fa4d5-251">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fa4d5-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]