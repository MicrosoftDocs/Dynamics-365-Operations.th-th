---
title: สร้างใบขอซื้อที่ใช้ RFQ
description: 'คำแนะนำนี้แสดงวิธีการเพิ่มข้อมูลราคาและผู้จัดจำหน่ายในใบขอซื้อจากกระบวนการ RFQ '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547416"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="6ec2b-103">สร้างใบขอซื้อที่ใช้ RFQ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ec2b-104">คำแนะนำนี้แสดงวิธีการเพิ่มข้อมูลราคาและผู้จัดจำหน่ายในใบขอซื้อจากกระบวนการ RFQ </span><span class="sxs-lookup"><span data-stu-id="6ec2b-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="6ec2b-105">ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF และคุณต้องล็อกอินเป็นผู้ดูแลระบบเพื่อทำขั้นตอนทั้งหมดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6ec2b-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="6ec2b-106">โดยทั่วไปงานในคู่มือนี้จะดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="6ec2b-107">สร้างใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-107">Create a requisition</span></span>
1. <span data-ttu-id="6ec2b-108">ไปที่การจัดซื้อและการจัดหา > ใบขอซื้อ > ใบขอซื้อที่ฉันจัดเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="6ec2b-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="6ec2b-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-109">Click New.</span></span>
3. <span data-ttu-id="6ec2b-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6ec2b-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6ec2b-111">ในฟิลด์วันที่ร้องขอ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6ec2b-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="6ec2b-112">ในฟิลด์วันที่ลงบัญชี ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6ec2b-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="6ec2b-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-113">Click OK.</span></span>
7. <span data-ttu-id="6ec2b-114">ในฟิลด์เหตุผล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="6ec2b-115">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-115">Click Add line.</span></span>
9. <span data-ttu-id="6ec2b-116">ในฟิลด์ประเภทการจัดซื้อ เลือกประเภทในแผนภูมิ และจากนั้น คลิกตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="6ec2b-117">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="6ec2b-118">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6ec2b-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="6ec2b-119">ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="6ec2b-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ec2b-120">Click Save.</span></span>
14. <span data-ttu-id="6ec2b-121">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="6ec2b-122">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="6ec2b-122">Click Submit.</span></span>
16. <span data-ttu-id="6ec2b-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-123">Close the page.</span></span>
17. <span data-ttu-id="6ec2b-124">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="6ec2b-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="6ec2b-125">กำหนดงานในลำดับงานใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec2b-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="6ec2b-126">งานถัดไปคือการสร้าง RFQ เพื่อรับการประมูลจากผู้จัดจำหน่ายสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6ec2b-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="6ec2b-127">ในข้อมูลสาธิต USMF ลำดับงานใบขอซื้อถูกตั้งค่าด้วยกฎเพื่อว่าถ้าไม่มีการเลือกผู้จัดจำหน่าย รือราคาต่อหน่วยเป็น 0 สำหรับรายการ งานจะได้รับมอบหมายให้กับผู้ปฏิบัติงานที่เฉพาะเจาะจงเพื่อสร้าง RFQ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="6ec2b-128">เพื่อดำเนินต่อพร้อมกับคำแนะนำนี้ คุณจะต้องกำหนดงานนั้นใหม่ให้กับผู้ใช้อื่น (ด้วยตนเอง) </span><span class="sxs-lookup"><span data-stu-id="6ec2b-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="6ec2b-129">คุณสามารถดำเนินการนี้ได้ถ้าคุณเข้าสู่ระบบในฐานะผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="6ec2b-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="6ec2b-130">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="6ec2b-131">คลิกดูประวัติ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-131">Click View history.</span></span>
3. <span data-ttu-id="6ec2b-132">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-132">Refresh the page.</span></span>
4. <span data-ttu-id="6ec2b-133">ขยายส่วนรายละเอียดการติดตาม</span><span class="sxs-lookup"><span data-stu-id="6ec2b-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="6ec2b-134">ในแผนภูมิ เลือก 'รายการที่ขึ้นต้นด้วย "เรียกใช้ลำดับงานในรายการบน"'</span><span class="sxs-lookup"><span data-stu-id="6ec2b-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="6ec2b-135">คลิกดูรายละเอียดลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6ec2b-135">Click View workflow details.</span></span>
7. <span data-ttu-id="6ec2b-136">ขยายส่วนรายการงาน</span><span class="sxs-lookup"><span data-stu-id="6ec2b-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="6ec2b-137">คลิกกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec2b-137">Click Reassign.</span></span>
9. <span data-ttu-id="6ec2b-138">ในฟิลด์ผู้ใช้ ให้เลือกผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="6ec2b-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="6ec2b-139">คลิกกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec2b-139">Click Reassign.</span></span>
11. <span data-ttu-id="6ec2b-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-140">Close the page.</span></span>
12. <span data-ttu-id="6ec2b-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="6ec2b-142">สร้าง RFQ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-142">Create an RFQ</span></span>
1. <span data-ttu-id="6ec2b-143">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-143">Refresh the page.</span></span>
2. <span data-ttu-id="6ec2b-144">คลิกคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6ec2b-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="6ec2b-145">ในฟิลด์นิติบุคคลที่จัดซื้อ ให้เลือก USMF</span><span class="sxs-lookup"><span data-stu-id="6ec2b-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="6ec2b-146">คุณต้องเลือกนิติบุคคลเดียวกันที่อยู่ในรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="6ec2b-147">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6ec2b-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6ec2b-148">ถ้าคุณมีหลายรายการในใบขอซื้อของคุณ ให้เลือกรายการทั้งหมดที่คุณต้องการเพิ่มไปยัง RFQ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="6ec2b-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-149">Click OK.</span></span>
6. <span data-ttu-id="6ec2b-150">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-150">Refresh the page.</span></span>
7. <span data-ttu-id="6ec2b-151">เปิดกล่องแสดงข้อมูลย่อ และขยายส่วนเอกสารที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="6ec2b-152">คุณอาจเปิดกล่องแสดงข้อมูลย่ออยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="6ec2b-152">You may already have the FactBox open.</span></span> <span data-ttu-id="6ec2b-153">ให้ค้นหาไอคอนที่มีลูกศรอยู่ทางด้านขวาของปุ่มเปิดปิดรายการ/ส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="6ec2b-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="6ec2b-154">หากลูกศรชี้ทางขวาแสดงว่าเปิดกล่องแสดงข้อมูลย่ออยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="6ec2b-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="6ec2b-155">หากลูกศรชี้ไปทางซ้าย ให้คลิกเพื่อเปิดกล่องแสดงข้อมูลย่อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="6ec2b-156">คลิกลิงค์ในฟิลด์คำขอใบเสนอราคาเพื่อเปิด RFQ ที่เพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6ec2b-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="6ec2b-157">คลิกหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-157">Click Header.</span></span>
10. <span data-ttu-id="6ec2b-158">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6ec2b-158">Click Add.</span></span>
11. <span data-ttu-id="6ec2b-159">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="6ec2b-160">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6ec2b-160">Click Add.</span></span>
13. <span data-ttu-id="6ec2b-161">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="6ec2b-162">คลิก ส่ง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-162">Click Send.</span></span>
15. <span data-ttu-id="6ec2b-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-163">Click OK.</span></span>
16. <span data-ttu-id="6ec2b-164">คลิกป้อนการตอบ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-164">Click Enter reply.</span></span>
17. <span data-ttu-id="6ec2b-165">ในบานหน้าต่างการดำเนินการ คลิกตอบ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="6ec2b-166">คลิกคัดลอกข้อมูลเพื่อตอบ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="6ec2b-167">ซึ่งจะคัดลอกข้อมูล เช่น ปริมาณและวันที่จาก RFQ ไปยังการตอบกลับ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="6ec2b-168">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6ec2b-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="6ec2b-169">นี่คือราคาที่คุณได้รับจากผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="6ec2b-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="6ec2b-170">คุณอาจต้องการป้อนข้อมูลเพิ่มเติมจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="6ec2b-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="6ec2b-171">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-171">Click Accept.</span></span>
21. <span data-ttu-id="6ec2b-172">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="6ec2b-173">ตรวจสอบว่าผู้จัดจำหน่ายและราคามีการโอนย้ายไปที่ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="6ec2b-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-174">Close the page.</span></span>
2. <span data-ttu-id="6ec2b-175">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-175">Click Lines.</span></span>
3. <span data-ttu-id="6ec2b-176">คลิก ข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-176">Click Related information.</span></span>
4. <span data-ttu-id="6ec2b-177">คลิกใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="6ec2b-178">เลือกบรรทัดที่มีการโอนย้ายไปยัง RFQ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="6ec2b-179">ตรวจสอบว่าราคาและผู้จัดจำหน่ายมีการคัดลอกไปที่ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6ec2b-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="6ec2b-180">คลิกลำดับงานเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec2b-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="6ec2b-181">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6ec2b-181">Click Complete.</span></span>
8. <span data-ttu-id="6ec2b-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec2b-182">Close the page.</span></span>
9. <span data-ttu-id="6ec2b-183">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6ec2b-183">Click Complete.</span></span>

