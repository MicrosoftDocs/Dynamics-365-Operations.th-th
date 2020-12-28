---
title: สร้างใบขอซื้อที่ใช้ RFQ
description: หัวข้อนี้อธิบายวิธีการเพิ่มข้อมูลราคาและผู้จัดจำหน่ายในใบขอซื้อจากกระบวนการ RFQ
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 205cba2325e76dae9572301e44e0e89cbcfd106e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438352"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="e7ada-103">สร้างใบขอซื้อที่ใช้ RFQ</span><span class="sxs-lookup"><span data-stu-id="e7ada-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7ada-104">หัวข้อนี้อธิบายวิธีการเพิ่มข้อมูลราคาและผู้จัดจำหน่ายในใบขอซื้อจากกระบวนการ RFQ</span><span class="sxs-lookup"><span data-stu-id="e7ada-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="e7ada-105">ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF และคุณต้องล็อกอินเป็นผู้ดูแลระบบเพื่อทำขั้นตอนทั้งหมดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7ada-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="e7ada-106">โดยทั่วไปงานในคู่มือนี้จะดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7ada-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="e7ada-107">สร้างใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7ada-107">Create a requisition</span></span>
1. <span data-ttu-id="e7ada-108">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > ใบขอซื้อ > ใบขอซื้อทั้งหมดที่จัดเตรียมโดยฉัน**</span><span class="sxs-lookup"><span data-stu-id="e7ada-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="e7ada-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e7ada-109">Select **New**.</span></span>
3. <span data-ttu-id="e7ada-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e7ada-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e7ada-111">ในฟิลด์ **วันที่ร้องขอ** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e7ada-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="e7ada-112">ในฟิลด์ **วันที่ลงบัญชี** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e7ada-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="e7ada-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-113">Select **OK**.</span></span>
7. <span data-ttu-id="e7ada-114">ในฟิลด์ **เหตุผล** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e7ada-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="e7ada-115">เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-115">Select **Add line**.</span></span>
9. <span data-ttu-id="e7ada-116">ในฟิลด์ **ประเภทการจัดซื้อ** เลือกประเภทในแผนภูมิ และจากนั้น คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="e7ada-117">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7ada-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="e7ada-118">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="e7ada-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="e7ada-119">ในฟิลด์ **หน่วย** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7ada-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="e7ada-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e7ada-120">Select **Save**.</span></span>
14. <span data-ttu-id="e7ada-121">เลือก **ลำดับงาน** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e7ada-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="e7ada-122">เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-122">Select **Submit**.</span></span>
16. <span data-ttu-id="e7ada-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-123">Close the page.</span></span>
17. <span data-ttu-id="e7ada-124">เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="e7ada-125">กำหนดงานในลำดับงานใหม่</span><span class="sxs-lookup"><span data-stu-id="e7ada-125">Reassign a workflow task</span></span>
<span data-ttu-id="e7ada-126">งานถัดไปคือการสร้าง RFQ เพื่อรับการประมูลจากผู้จัดจำหน่ายสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7ada-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="e7ada-127">ในข้อมูลสาธิต USMF ลำดับงานใบขอซื้อถูกตั้งค่าด้วยกฎเพื่อว่าถ้าไม่มีการเลือกผู้จัดจำหน่าย รือราคาต่อหน่วยเป็น 0 สำหรับรายการ งานจะได้รับมอบหมายให้กับผู้ปฏิบัติงานที่เฉพาะเจาะจงเพื่อสร้าง RFQ</span><span class="sxs-lookup"><span data-stu-id="e7ada-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="e7ada-128">เพื่อดำเนินต่อพร้อมกับคำแนะนำนี้ คุณจะต้องกำหนดงานนั้นใหม่ให้กับผู้ใช้อื่น (ด้วยตนเอง) </span><span class="sxs-lookup"><span data-stu-id="e7ada-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="e7ada-129">คุณสามารถดำเนินการนี้ได้ถ้าคุณเข้าสู่ระบบในฐานะผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="e7ada-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="e7ada-130">เลือก **ลำดับงาน** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e7ada-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="e7ada-131">เลือก **ดูประวัติ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-131">Select **View history**.</span></span>
3. <span data-ttu-id="e7ada-132">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-132">Refresh the page.</span></span>
4. <span data-ttu-id="e7ada-133">ขยายส่วน **รายละเอียดการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="e7ada-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="e7ada-134">ในแผนภูมิ เลือกรายการที่ขึ้นต้นด้วย "เรียกใช้ลำดับงานในรายการบน"</span><span class="sxs-lookup"><span data-stu-id="e7ada-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="e7ada-135">เลือก **ดูรายละเอียดลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="e7ada-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="e7ada-136">ขยายส่วน **รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="e7ada-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="e7ada-137">เลือก **กำหนดอีกครั้ง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="e7ada-138">ในฟิลด์ **ผู้ใช้** ให้เลือก **ผู้ดูแล**</span><span class="sxs-lookup"><span data-stu-id="e7ada-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="e7ada-139">เลือก **กำหนดอีกครั้ง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="e7ada-140">ปิดหน้าสองหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="e7ada-141">สร้าง RFQ</span><span class="sxs-lookup"><span data-stu-id="e7ada-141">Create an RFQ</span></span>

1. <span data-ttu-id="e7ada-142">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-142">Refresh the page.</span></span>
2. <span data-ttu-id="e7ada-143">เลือก **คำขอใบเสนอราคา**</span><span class="sxs-lookup"><span data-stu-id="e7ada-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="e7ada-144">ในฟิลด์ **นิติบุคคลที่จัดซื้อ** ให้เลือก **USMF**</span><span class="sxs-lookup"><span data-stu-id="e7ada-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="e7ada-145">คุณต้องเลือกนิติบุคคลเดียวกันที่อยู่ในรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7ada-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="e7ada-146">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e7ada-146">In the list, mark the selected row.</span></span> <span data-ttu-id="e7ada-147">ถ้าคุณมีหลายรายการในใบขอซื้อของคุณ ให้เลือกรายการทั้งหมดที่คุณต้องการเพิ่มไปยัง RFQ</span><span class="sxs-lookup"><span data-stu-id="e7ada-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="e7ada-148">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-148">Select **OK**.</span></span>
6. <span data-ttu-id="e7ada-149">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-149">Refresh the page.</span></span>
7. <span data-ttu-id="e7ada-150">ตรวจสอบให้แน่ใจว่ากล่องแสดงข้อมูลย่อเปิดอยู่ จากนั้น ขยายส่วน **เอกสารที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="e7ada-151">เลือกลิงค์ในฟิลด์ **คำขอใบเสนอราคา** เพื่อเปิด RFQ ที่เพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="e7ada-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="e7ada-152">เลือก **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="e7ada-152">Select **Header**.</span></span>
10. <span data-ttu-id="e7ada-153">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="e7ada-153">Select **Add**.</span></span>
11. <span data-ttu-id="e7ada-154">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e7ada-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="e7ada-155">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="e7ada-155">Select **Add**.</span></span>
13. <span data-ttu-id="e7ada-156">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e7ada-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="e7ada-157">เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-157">Select **Send**.</span></span>
15. <span data-ttu-id="e7ada-158">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-158">Select **OK**.</span></span>
16. <span data-ttu-id="e7ada-159">เลือก **ป้อนการตอบ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="e7ada-160">บนบานหน้าต่างการดำเนินการ เลือก **ตอบ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="e7ada-161">เลือก **คัดลอกข้อมูลไปที่การตอบ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="e7ada-162">ซึ่งจะคัดลอกข้อมูล เช่น ปริมาณและวันที่จาก RFQ ไปยังการตอบกลับ</span><span class="sxs-lookup"><span data-stu-id="e7ada-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="e7ada-163">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e7ada-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="e7ada-164">นี่คือราคาที่คุณได้รับจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e7ada-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="e7ada-165">คุณอาจต้องการป้อนข้อมูลเพิ่มเติมจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e7ada-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="e7ada-166">เลือก **ยอมรับ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-166">Select **Accept**.</span></span>
21. <span data-ttu-id="e7ada-167">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="e7ada-168">ตรวจสอบว่าผู้จัดจำหน่ายและราคามีการโอนย้ายไปที่ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7ada-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="e7ada-169">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-169">Close the page.</span></span>
2. <span data-ttu-id="e7ada-170">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-170">Select **Lines**.</span></span>
3. <span data-ttu-id="e7ada-171">เลือก **ข้อมูลที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="e7ada-171">Select **Related information**.</span></span>
4. <span data-ttu-id="e7ada-172">เลือก **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="e7ada-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="e7ada-173">เลือกบรรทัดที่มีการโอนย้ายไปยัง RFQ</span><span class="sxs-lookup"><span data-stu-id="e7ada-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="e7ada-174">ตรวจสอบว่าราคาและผู้จัดจำหน่ายมีการคัดลอกไปที่ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7ada-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="e7ada-175">เลือก **ลำดับงาน** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="e7ada-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="e7ada-176">เลือกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7ada-176">Select Complete.</span></span>
8. <span data-ttu-id="e7ada-177">เลือกหน้า</span><span class="sxs-lookup"><span data-stu-id="e7ada-177">Select the page.</span></span>
9. <span data-ttu-id="e7ada-178">เลือกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e7ada-178">Select Complete.</span></span>

