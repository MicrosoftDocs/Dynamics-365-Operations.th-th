--- 
title: "สร้างใบขอซื้อที่ใช้ RFQ"
description: "คำแนะนำนี้แสดงวิธีการเพิ่มข้อมูลราคาและผู้จัดจำหน่ายในใบขอซื้อจากกระบวนการ RFQ "
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1bb831c1e6e4f148307b6546c1fb63af217f07ed
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="aafb0-103">สร้างใบขอซื้อที่ใช้ RFQ</span><span class="sxs-lookup"><span data-stu-id="aafb0-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aafb0-104">คำแนะนำนี้แสดงวิธีการเพิ่มข้อมูลราคาและผู้จัดจำหน่ายในใบขอซื้อจากกระบวนการ RFQ </span><span class="sxs-lookup"><span data-stu-id="aafb0-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="aafb0-105">ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF และคุณต้องล็อกอินเป็นผู้ดูแลระบบเพื่อทำขั้นตอนทั้งหมดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aafb0-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="aafb0-106">โดยทั่วไปงานในคู่มือนี้จะดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="aafb0-107">สร้างใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-107">Create a requisition</span></span>
1. <span data-ttu-id="aafb0-108">ไปที่การจัดซื้อและการจัดหา > ใบขอซื้อ > ใบขอซื้อที่ฉันจัดเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="aafb0-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="aafb0-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="aafb0-109">Click New.</span></span>
3. <span data-ttu-id="aafb0-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="aafb0-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="aafb0-111">ในฟิลด์วันที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="aafb0-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="aafb0-112">ในฟิลด์วันที่ลงบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="aafb0-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="aafb0-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aafb0-113">Click OK.</span></span>
7. <span data-ttu-id="aafb0-114">ในฟิลด์เหตุผล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="aafb0-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="aafb0-115">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="aafb0-115">Click Add line.</span></span>
9. <span data-ttu-id="aafb0-116">ในฟิลด์ประเภทการจัดซื้อ เลือกประเภทในแผนภูมิ และจากนั้น คลิกตกลง</span><span class="sxs-lookup"><span data-stu-id="aafb0-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="aafb0-117">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="aafb0-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="aafb0-118">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="aafb0-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="aafb0-119">ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="aafb0-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="aafb0-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="aafb0-120">Click Save.</span></span>
14. <span data-ttu-id="aafb0-121">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aafb0-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="aafb0-122">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="aafb0-122">Click Submit.</span></span>
16. <span data-ttu-id="aafb0-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-123">Close the page.</span></span>
17. <span data-ttu-id="aafb0-124">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="aafb0-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="aafb0-125">กำหนดงานในลำดับงานใหม่</span><span class="sxs-lookup"><span data-stu-id="aafb0-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="aafb0-126">งานถัดไปคือการสร้าง RFQ เพื่อรับการประมูลจากผู้จัดจำหน่ายสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="aafb0-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="aafb0-127">ในข้อมูลสาธิต USMF ลำดับงานใบขอซื้อถูกตั้งค่าด้วยกฎเพื่อว่าถ้าไม่มีการเลือกผู้จัดจำหน่าย รือราคาต่อหน่วยเป็น 0 สำหรับรายการ งานจะได้รับมอบหมายให้กับผู้ปฏิบัติงานที่เฉพาะเจาะจงเพื่อสร้าง RFQ</span><span class="sxs-lookup"><span data-stu-id="aafb0-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="aafb0-128">เพื่อดำเนินต่อพร้อมกับคำแนะนำนี้ คุณจะต้องกำหนดงานนั้นใหม่ให้กับผู้ใช้อื่น (ด้วยตนเอง) </span><span class="sxs-lookup"><span data-stu-id="aafb0-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="aafb0-129">คุณสามารถดำเนินการนี้ได้ถ้าคุณเข้าสู่ระบบในฐานะผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="aafb0-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="aafb0-130">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aafb0-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="aafb0-131">คลิกดูประวัติ</span><span class="sxs-lookup"><span data-stu-id="aafb0-131">Click View history.</span></span>
3. <span data-ttu-id="aafb0-132">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-132">Refresh the page.</span></span>
4. <span data-ttu-id="aafb0-133">ขยายส่วนรายละเอียดการติดตาม</span><span class="sxs-lookup"><span data-stu-id="aafb0-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="aafb0-134">ในแผนภูมิ เลือก 'รายการที่ขึ้นต้นด้วย "เรียกใช้ลำดับงานในรายการบน"'</span><span class="sxs-lookup"><span data-stu-id="aafb0-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="aafb0-135">คลิกดูรายละเอียดลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="aafb0-135">Click View workflow details.</span></span>
7. <span data-ttu-id="aafb0-136">ขยายส่วนรายการงาน</span><span class="sxs-lookup"><span data-stu-id="aafb0-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="aafb0-137">คลิกกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="aafb0-137">Click Reassign.</span></span>
9. <span data-ttu-id="aafb0-138">ในฟิลด์ผู้ใช้ ให้เลือกผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="aafb0-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="aafb0-139">คลิกกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="aafb0-139">Click Reassign.</span></span>
11. <span data-ttu-id="aafb0-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-140">Close the page.</span></span>
12. <span data-ttu-id="aafb0-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="aafb0-142">สร้าง RFQ</span><span class="sxs-lookup"><span data-stu-id="aafb0-142">Create an RFQ</span></span>
1. <span data-ttu-id="aafb0-143">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-143">Refresh the page.</span></span>
2. <span data-ttu-id="aafb0-144">คลิกคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="aafb0-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="aafb0-145">ในฟิลด์นิติบุคคลที่จัดซื้อ ให้เลือก USMF</span><span class="sxs-lookup"><span data-stu-id="aafb0-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="aafb0-146">คุณต้องเลือกนิติบุคคลเดียวกันที่อยู่ในรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="aafb0-147">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="aafb0-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="aafb0-148">ถ้าคุณมีหลายรายการในใบขอซื้อของคุณ ให้เลือกรายการทั้งหมดที่คุณต้องการเพิ่มไปยัง RFQ</span><span class="sxs-lookup"><span data-stu-id="aafb0-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="aafb0-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aafb0-149">Click OK.</span></span>
6. <span data-ttu-id="aafb0-150">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-150">Refresh the page.</span></span>
7. <span data-ttu-id="aafb0-151">เปิดกล่องแสดงข้อมูลย่อ และขยายส่วนเอกสารที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="aafb0-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="aafb0-152">คุณอาจเปิดกล่องแสดงข้อมูลย่ออยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="aafb0-152">You may already have the FactBox open.</span></span> <span data-ttu-id="aafb0-153">ให้ค้นหาไอคอนที่มีลูกศรอยู่ทางด้านขวาของปุ่มเปิดปิดรายการ/ส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="aafb0-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="aafb0-154">หากลูกศรชี้ทางขวาแสดงว่าเปิดกล่องแสดงข้อมูลย่ออยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="aafb0-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="aafb0-155">หากลูกศรชี้ไปทางซ้าย ให้คลิกเพื่อเปิดกล่องแสดงข้อมูลย่อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="aafb0-156">คลิกลิงค์ในฟิลด์คำขอใบเสนอราคาเพื่อเปิด RFQ ที่เพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="aafb0-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="aafb0-157">คลิกหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-157">Click Header.</span></span>
10. <span data-ttu-id="aafb0-158">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="aafb0-158">Click Add.</span></span>
11. <span data-ttu-id="aafb0-159">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="aafb0-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="aafb0-160">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="aafb0-160">Click Add.</span></span>
13. <span data-ttu-id="aafb0-161">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="aafb0-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="aafb0-162">คลิก ส่ง</span><span class="sxs-lookup"><span data-stu-id="aafb0-162">Click Send.</span></span>
15. <span data-ttu-id="aafb0-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aafb0-163">Click OK.</span></span>
16. <span data-ttu-id="aafb0-164">คลิกป้อนการตอบ</span><span class="sxs-lookup"><span data-stu-id="aafb0-164">Click Enter reply.</span></span>
17. <span data-ttu-id="aafb0-165">ในบานหน้าต่างการดำเนินการ คลิกตอบ</span><span class="sxs-lookup"><span data-stu-id="aafb0-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="aafb0-166">คลิกคัดลอกข้อมูลเพื่อตอบ</span><span class="sxs-lookup"><span data-stu-id="aafb0-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="aafb0-167">ซึ่งจะคัดลอกข้อมูล เช่น ปริมาณและวันที่จาก RFQ ไปยังการตอบกลับ</span><span class="sxs-lookup"><span data-stu-id="aafb0-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="aafb0-168">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="aafb0-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="aafb0-169">นี่คือราคาที่คุณได้รับจากผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="aafb0-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="aafb0-170">คุณอาจต้องการป้อนข้อมูลเพิ่มเติมจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="aafb0-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="aafb0-171">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="aafb0-171">Click Accept.</span></span>
21. <span data-ttu-id="aafb0-172">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aafb0-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="aafb0-173">ตรวจสอบว่าผู้จัดจำหน่ายและราคามีการโอนย้ายไปที่ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="aafb0-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-174">Close the page.</span></span>
2. <span data-ttu-id="aafb0-175">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="aafb0-175">Click Lines.</span></span>
3. <span data-ttu-id="aafb0-176">คลิก ข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="aafb0-176">Click Related information.</span></span>
4. <span data-ttu-id="aafb0-177">คลิกใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="aafb0-178">เลือกบรรทัดที่มีการโอนย้ายไปยัง RFQ</span><span class="sxs-lookup"><span data-stu-id="aafb0-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="aafb0-179">ตรวจสอบว่าราคาและผู้จัดจำหน่ายมีการคัดลอกไปที่ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="aafb0-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="aafb0-180">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="aafb0-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="aafb0-181">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aafb0-181">Click Complete.</span></span>
8. <span data-ttu-id="aafb0-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="aafb0-182">Close the page.</span></span>
9. <span data-ttu-id="aafb0-183">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="aafb0-183">Click Complete.</span></span>


