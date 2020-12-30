---
title: แก้ไขแบบจำลองและการแมปเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน
description: เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน “ER สร้างเอกสารที่มีการปรับปรุงข้อมูลแอพลิเคชัน (ส่วนที่ 2 - สร้างเอกสาร)“ ให้เสร็จเรียบร้อย
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3401ec98ac1b61572d07fbb30d4465de78473fca
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684582"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="dc100-103">แก้ไขแบบจำลองและการแมปเพื่อสร้างเอกสารที่มีข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc100-104">เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน “ER สร้างเอกสารที่มีการปรับปรุงข้อมูลแอพลิเคชัน (ส่วนที่ 2: สร้างเอกสาร)“ ให้เสร็จเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="dc100-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="dc100-105">ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ส์และอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="dc100-106">ในกระบวนงานนี้ คุณจะปรับเปลี่ยนการตั้งค่าคอนฟิก ER เพื่อเริ่มต้นการใช้งานเพื่อสร้างเอกสารอิเล็กทรอนิกส์ และอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="dc100-107">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="dc100-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="dc100-108">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF</span><span class="sxs-lookup"><span data-stu-id="dc100-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="dc100-109">ปรับเปลี่ยนแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dc100-109">Modify data model</span></span>
1. <span data-ttu-id="dc100-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="dc100-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dc100-111">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="dc100-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="dc100-112">คุณจะขยายวิธีใช้แบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dc100-112">You will extend how you use the data model.</span></span> <span data-ttu-id="dc100-113">นอกจากการใช้เป็นแหล่งข้อมูลในการสร้างรายงานอินทราสแทต จะมีการใช้แบบจำลองข้อมูลเพื่อรวบรวมรายละเอียดเกี่ยวกับกระบวนการการรายงานอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="dc100-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="dc100-114">จากนั้นจะมีการใช้รายละเอียดเพื่ออัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="dc100-115">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="dc100-115">Click Designer.</span></span>
4. <span data-ttu-id="dc100-116">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="dc100-117">ในฟิลด์สร้างโหนดใหม่เป็น ให้ป้อน 'รากแบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="dc100-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="dc100-118">ในฟิลด์ชื่อ ให้พิมพ์ 'สำหรับการอัพเดตข้อมูลแอพลิเคชัน'</span><span class="sxs-lookup"><span data-stu-id="dc100-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="dc100-119">สำหรับการอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-119">For application data update</span></span>  
7. <span data-ttu-id="dc100-120">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-120">Click Add.</span></span>
8. <span data-ttu-id="dc100-121">ในแผนภูมิ เลือก 'สำหรับการอัพเดตข้อมูลแอพลิเคชัน'</span><span class="sxs-lookup"><span data-stu-id="dc100-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="dc100-122">มีการเพิ่มรายการรากใหม่นี้เพื่อระบุลำดับข้อมูลสำหรับการย้ายข้อมูลจากรายงานอินทราสแทต (ซึ่งใช้เป็นแหล่งข้อมูล) ไปยังตารางแอพลิเคชัน (ปลายทางการอัพเดต)</span><span class="sxs-lookup"><span data-stu-id="dc100-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="dc100-123">หมายเหตุว่าต้องใช้รายการรากที่แตกต่างกันสำหรับการเรียกข้อมูลที่มีการลงรายการบัญชีเอกสารขาออกและสำหรับการเรียกข้อมูลจากเอกสารที่ใช้เพื่ออัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="dc100-124">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="dc100-125">ในฟิลด์ชื่อ ให้พิมพ์ 'ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="dc100-126">ส่วนหัวที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-126">Archive header</span></span>  
11. <span data-ttu-id="dc100-127">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="dc100-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="dc100-128">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-128">Click Add.</span></span>
    * <span data-ttu-id="dc100-129">เนื่องจากคุณจะสร้างเรกคอร์ดสำหรับแต่ละรายงานอินทราสแทตที่ถูกสร้างขึ้น คุณจะต้องสร้างรายการใหม่สำหรับรายการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="dc100-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="dc100-130">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="dc100-131">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="dc100-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="dc100-132">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="dc100-132">File name</span></span>  
15. <span data-ttu-id="dc100-133">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="dc100-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="dc100-134">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-134">Click Add.</span></span>
17. <span data-ttu-id="dc100-135">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="dc100-136">ในฟิลด์ชื่อ ให้พิมพ์ 'จำนวนของรายการ'</span><span class="sxs-lookup"><span data-stu-id="dc100-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="dc100-137">จำนวนของรายการ</span><span class="sxs-lookup"><span data-stu-id="dc100-137">Number of lines</span></span>  
19. <span data-ttu-id="dc100-138">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนเต็ม'</span><span class="sxs-lookup"><span data-stu-id="dc100-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="dc100-139">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-139">Click Add.</span></span>
    * <span data-ttu-id="dc100-140">เพิ่มรายการนี้เพื่อแสดงหมายเลขของธุรกรรมอินทราสแทตที่ถูกรายงานในระหว่างกระบวนการรายงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="dc100-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="dc100-141">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="dc100-142">ในฟิลด์ชื่อ ให้พิมพ์ 'รายการที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="dc100-143">รายการที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-143">Archive lines</span></span>  
23. <span data-ttu-id="dc100-144">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="dc100-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="dc100-145">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-145">Click Add.</span></span>
    * <span data-ttu-id="dc100-146">เพิ่มรายการนี้เพื่อแสดงรายการของธุรกรรมอินทราสแทตที่ถูกรายงานในระหว่างกระบวนการรายงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="dc100-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="dc100-147">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="dc100-148">ในฟิลด์ชื่อ พิมพ์ 'จำนวน'</span><span class="sxs-lookup"><span data-stu-id="dc100-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="dc100-149">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dc100-149">Amount</span></span>  
27. <span data-ttu-id="dc100-150">ในฟิลด์ประเภทสินค้า ให้เลือก 'จำนวนจริง'</span><span class="sxs-lookup"><span data-stu-id="dc100-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="dc100-151">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-151">Click Add.</span></span>
29. <span data-ttu-id="dc100-152">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="dc100-153">ในฟิลด์ชื่อ พิมพ์ 'รหัสเรกคอร์ดโภคภัณฑ์'</span><span class="sxs-lookup"><span data-stu-id="dc100-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="dc100-154">รหัสเรกคอร์ดโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dc100-154">Commodity rec id</span></span>  
31. <span data-ttu-id="dc100-155">ในฟิลด์ประเภทสินค้า ให้เลือก 'Int64'</span><span class="sxs-lookup"><span data-stu-id="dc100-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="dc100-156">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-156">Click Add.</span></span>
33. <span data-ttu-id="dc100-157">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dc100-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="dc100-158">ในฟิลด์ชื่อ ให้พิมพ์ 'หมายเลขสินค้า'</span><span class="sxs-lookup"><span data-stu-id="dc100-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="dc100-159">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="dc100-159">Item number</span></span>  
35. <span data-ttu-id="dc100-160">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="dc100-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="dc100-161">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-161">Click Add.</span></span>
37. <span data-ttu-id="dc100-162">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dc100-162">Click Save.</span></span>
38. <span data-ttu-id="dc100-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dc100-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="dc100-164">ปรับปรุงการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="dc100-164">Modify model mapping</span></span>
1. <span data-ttu-id="dc100-165">ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="dc100-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="dc100-166">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (การแม็ป)'</span><span class="sxs-lookup"><span data-stu-id="dc100-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="dc100-167">ปรับเปลี่ยนการแม็ปแบบจำลองที่มีอยู่เพื่อเริ่มต้นการใช้สำหรับการอัพเดตข้อมูลแอพลิเคชัน และเพื่อเก็บรายละเอียดการรายงานอินทราสแทตถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="dc100-168">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="dc100-168">Click Designer.</span></span>
4. <span data-ttu-id="dc100-169">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dc100-169">Click New.</span></span>
5. <span data-ttu-id="dc100-170">ในฟิลด์ชื่อ ให้พิมพ์ 'อัพเดตที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="dc100-171">อัพเดตที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-171">Update archive</span></span>  
6. <span data-ttu-id="dc100-172">ในฟิลด์ทิศทาง ให้เลือก 'ไปยังปลายทาง'</span><span class="sxs-lookup"><span data-stu-id="dc100-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="dc100-173">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dc100-173">Click Save.</span></span>
    * <span data-ttu-id="dc100-174">การแม็ปใหม่นี้จะระบุลำดับข้อมูลสำหรับการย้ายข้อมูล (รายละเอียดการรายงานอินทราสแทต) จากแบบจำลองข้อมูลไปยังตารางแอพลิเคชัน (ปลายทางการอัพเดต)</span><span class="sxs-lookup"><span data-stu-id="dc100-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="dc100-175">หมายเหตุว่าต้องใช้รายการรากของแบบจำลองที่แตกต่างกันเพื่อเรียกข้อมูลจากแอพลิเคชันสำหรับกระบวนการรายงาน แล้วจึงใช้ข้อมูลจากแบบจำลองข้อมูลสำหรับการปรับปรุงข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-175">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="dc100-176">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="dc100-176">Click Designer.</span></span>
9. <span data-ttu-id="dc100-177">ในแผนภูมิ เลือก 'แบบจำลองข้อมูล\แบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="dc100-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="dc100-178">เพิ่มแหล่งข้อมูลที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="dc100-178">Add the required data source.</span></span> <span data-ttu-id="dc100-179">นี่คือแบบจำลองข้อมูลที่ประกอบด้วยรายละเอียดเกี่ยวกับธุรกรรมอินทราสแทตที่รายงานที่จะต้องถูกเก็บไว้ถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="dc100-180">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="dc100-180">Click Add root.</span></span>
11. <span data-ttu-id="dc100-181">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลอง'</span><span class="sxs-lookup"><span data-stu-id="dc100-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="dc100-182">แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="dc100-182">model</span></span>  
12. <span data-ttu-id="dc100-183">ในฟิลด์คำนิยาม ป้อนหรือเลือกค่า 'สำหรับการปรับปรุงข้อมูลแอพลิเคชัน'</span><span class="sxs-lookup"><span data-stu-id="dc100-183">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="dc100-184">สำหรับการอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-184">For application data update</span></span>  
13. <span data-ttu-id="dc100-185">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="dc100-185">Click OK.</span></span>
14. <span data-ttu-id="dc100-186">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="dc100-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="dc100-187">ในแผนภูมิ เลือก 'ฟิลด์ที่คำนวณ\ฟังก์ชันได้'</span><span class="sxs-lookup"><span data-stu-id="dc100-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="dc100-188">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="dc100-189">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-189">Click Add.</span></span>
    * <span data-ttu-id="dc100-190">เนื่องจากคุณต้องการระบุธุรกรรมอินทราสแทตที่มีการรายงานสำหรับการเก็บถาวร คุณจะต้องเพิ่มแหล่งข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="dc100-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="dc100-191">ในฟิลด์ชื่อ ให้พิมพ์ 'รายการที่ระบุ'</span><span class="sxs-lookup"><span data-stu-id="dc100-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="dc100-192">รายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="dc100-192">Enumerated lines</span></span>  
19. <span data-ttu-id="dc100-193">คลิก แก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="dc100-193">Click Edit formula.</span></span>
20. <span data-ttu-id="dc100-194">ในแผนภูมิ ให้เลือก 'รายการ\แจงนับ'</span><span class="sxs-lookup"><span data-stu-id="dc100-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="dc100-195">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-195">Click Add function.</span></span>
22. <span data-ttu-id="dc100-196">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="dc100-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="dc100-197">ในแผนภูมิ ให้ขยาย 'แบบจำลอง\ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="dc100-198">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="dc100-199">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dc100-199">Click Add data source.</span></span>
26. <span data-ttu-id="dc100-200">ในฟิลด์สูตร ให้ป้อน 'ENUMERATE(model.'Archive header'.'Archive lines')'</span><span class="sxs-lookup"><span data-stu-id="dc100-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="dc100-201">แจงนับ (แบบจำลอง 'ส่วนหัวที่เก็บถาวร' 'รายการที่เก็บถาวร')</span><span class="sxs-lookup"><span data-stu-id="dc100-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="dc100-202">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dc100-202">Click Save.</span></span>
28. <span data-ttu-id="dc100-203">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dc100-203">Close the page.</span></span>
29. <span data-ttu-id="dc100-204">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dc100-204">Click OK.</span></span>
30. <span data-ttu-id="dc100-205">คลิก เพิ่มปลายทาง</span><span class="sxs-lookup"><span data-stu-id="dc100-205">Click Add destination.</span></span>
    * <span data-ttu-id="dc100-206">เพิ่มตารางแอพลิเคชันเป็นปลายทางจำเป็นที่จำเป็นต้องอัพเดตเพื่อเก็บถาวรรายละเอียดของธุรกรรมอินทราสแทตที่มีการรายงาน</span><span class="sxs-lookup"><span data-stu-id="dc100-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="dc100-207">ในฟิลด์ชื่อ ให้พิมพ์ 'ที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="dc100-208">เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-208">Archive</span></span>  
32. <span data-ttu-id="dc100-209">ในฟิลด์ชื่อตาราง ให้พิมพ์ 'IntrastatArchiveGeneral'</span><span class="sxs-lookup"><span data-stu-id="dc100-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="dc100-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="dc100-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="dc100-211">รักษาการดำเนินการเรกคอร์ด 'แทรก' เพื่อให้คุณสามารถเพิ่มเรกคอร์ดในระหว่างการเก็บรายละเอียดของแต่ละกระบวนการรายงานอินทราสแทตโดยถาวร</span><span class="sxs-lookup"><span data-stu-id="dc100-211">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="dc100-212">เลือก ใช่ ในฟิลด์ infolog เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="dc100-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="dc100-213">เลือก ใช่ เพื่อเรียกดูข้อมูลของปัญหาเกี่ยวกับการอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="dc100-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="dc100-214">เลือก ใช่ ในฟิลด์ ข้ามการตรวจสอบความถูกต้องในการดำเนินการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="dc100-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="dc100-215">เลือก ใช่ เพื่อระงับข้อผิดพลาดเกี่ยวกับการตรวจสอบความถูกต้องเกี่ยวกับฟิลด์ 'รหัสที่เก็บถาวรของอินทราสแทต' ที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="dc100-215">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="dc100-216">ซึ่งจะสามารถทำได้หลังจากที่มีการเพิ่มเรกคอร์ดตามการตั้งค่าหมายเลขลำดับที่ถูกตั้งค่าคอนฟิกสำหรับตารางนี้ในแบบฟอร์มพารามิเตอร์การค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="dc100-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="dc100-217">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dc100-217">Click OK.</span></span>
    * <span data-ttu-id="dc100-218">ผูกองค์ประกอบของแหล่งข้อมูลที่เพิ่มเข้ามา (แบบจำลองที่มีการกรองข้อมูลตามรายการรากที่เลือก) ด้วยองค์ประกอบจากปลายทางที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="dc100-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="dc100-219">ในแผนภูมิ ให้ขยาย 'ที่เก็บถาวระ'</span><span class="sxs-lookup"><span data-stu-id="dc100-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="dc100-220">ในแผนภูมิ ให้ขยาย 'ที่เก็บถาวร\<ความสัมพันธ์'</span><span class="sxs-lookup"><span data-stu-id="dc100-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="dc100-221">ในแผนภูมิ ขยาย 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetail'</span><span class="sxs-lookup"><span data-stu-id="dc100-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="dc100-222">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailAmount(AmountMST)'</span><span class="sxs-lookup"><span data-stu-id="dc100-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="dc100-223">ในแผนภูมิ ให้ขยาย 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ'</span><span class="sxs-lookup"><span data-stu-id="dc100-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="dc100-224">ในแผนภูมิ ให้ขยาย 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\ค่า'</span><span class="sxs-lookup"><span data-stu-id="dc100-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="dc100-225">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\ค่า\ยอดเงิน'</span><span class="sxs-lookup"><span data-stu-id="dc100-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="dc100-226">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-226">Click Bind.</span></span>
44. <span data-ttu-id="dc100-227">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailCommodity(IntrastatCommodity)'</span><span class="sxs-lookup"><span data-stu-id="dc100-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="dc100-228">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุค่า\รหัสเรกคอร์ดโภคภัณฑ์'</span><span class="sxs-lookup"><span data-stu-id="dc100-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="dc100-229">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-229">Click Bind.</span></span>
47. <span data-ttu-id="dc100-230">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailItem number(ItemId)'</span><span class="sxs-lookup"><span data-stu-id="dc100-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="dc100-231">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\ค่า\หมายเลขสินค้า'</span><span class="sxs-lookup"><span data-stu-id="dc100-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="dc100-232">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-232">Click Bind.</span></span>
50. <span data-ttu-id="dc100-233">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetailLine number(LineNumber)'</span><span class="sxs-lookup"><span data-stu-id="dc100-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="dc100-234">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="dc100-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="dc100-235">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-235">Click Bind.</span></span>
53. <span data-ttu-id="dc100-236">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\<ความสัมพันธ์IntrastatArchiveDetail'</span><span class="sxs-lookup"><span data-stu-id="dc100-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="dc100-237">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\รายการที่ระบุ'</span><span class="sxs-lookup"><span data-stu-id="dc100-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="dc100-238">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-238">Click Bind.</span></span>
56. <span data-ttu-id="dc100-239">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\ชื่อไฟล์(FileName)'</span><span class="sxs-lookup"><span data-stu-id="dc100-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="dc100-240">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="dc100-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="dc100-241">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-241">Click Bind.</span></span>
59. <span data-ttu-id="dc100-242">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร\จำนวนของรายการ(NumberOfLines)'</span><span class="sxs-lookup"><span data-stu-id="dc100-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="dc100-243">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร\จำนวนของรายการ'</span><span class="sxs-lookup"><span data-stu-id="dc100-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="dc100-244">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-244">Click Bind.</span></span>
62. <span data-ttu-id="dc100-245">ในแผนภูมิ ให้เลือก 'ที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="dc100-246">ในแผนภูมิ ให้เลือก 'แบบจำลอง\ส่วนหัวที่เก็บถาวร'</span><span class="sxs-lookup"><span data-stu-id="dc100-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="dc100-247">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="dc100-247">Click Bind.</span></span>
65. <span data-ttu-id="dc100-248">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dc100-248">Click Save.</span></span>
66. <span data-ttu-id="dc100-249">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dc100-249">Close the page.</span></span>
67. <span data-ttu-id="dc100-250">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dc100-250">Close the page.</span></span>

