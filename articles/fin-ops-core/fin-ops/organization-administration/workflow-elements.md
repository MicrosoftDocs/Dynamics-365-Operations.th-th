---
title: องค์ประกอบลำดับงาน
description: หัวข้อนี้อธิบายองค์ประกอบต่างๆ ที่ประกอบลำดับงาน
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6df767c2db6d5d9addce5f91544686628ab064dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180234"
---
# <a name="workflow-elements"></a><span data-ttu-id="cc87e-103">องค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="cc87e-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc87e-104">หัวข้อนี้อธิบายองค์ประกอบต่างๆ ที่ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="cc87e-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="cc87e-105">ลำดับงานประกอบด้วย องค์ประกอบ </span><span class="sxs-lookup"><span data-stu-id="cc87e-105">A workflow consists of elements.</span></span> <span data-ttu-id="cc87e-106">ส่วนต่อไปนี้อธิบายถึงองค์ประกอบแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="cc87e-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="cc87e-107">งาน</span><span class="sxs-lookup"><span data-stu-id="cc87e-107">Tasks</span></span>

<span data-ttu-id="cc87e-108">หนึ่ง *งาน* คือหน่วยของงานที่ต้องดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="cc87e-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="cc87e-109">งานสองชนิดสามารถถูกเพิ่มไปที่ลำดับงาน: งานด้วยตนเองและงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cc87e-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="cc87e-110">งานที่ทำด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cc87e-110">Manual task</span></span>

<span data-ttu-id="cc87e-111">หนึ่ง *งานที่กำหนดด้วยตนเอง* คือหน่วยของงานที่ต้องดำเนินการโดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cc87e-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="cc87e-112">ตัวอย่างเช่น ลำดับงานรายงานค่าใช้จ่ายสามารถมีงานที่กำหนดด้วยตนเองที่ต้องการให้ผู้ใช้กำหนดเพื่อดำเนินการต่อไปนี้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="cc87e-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="cc87e-113">ทบทวนการรับสินค้าที่ถูกส่งมาพร้อมกับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="cc87e-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="cc87e-114">เรียกผู้จัดการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="cc87e-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="cc87e-115">งานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cc87e-115">Automated task</span></span>

<span data-ttu-id="cc87e-116">หนึ่ง *งานอัตโนมัติ* คือหน่วยของงานที่ต้องดำเนินการโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="cc87e-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="cc87e-117">ไม่มีการโต้ตอบของบุคคลที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="cc87e-117">No human interaction is required.</span></span> <span data-ttu-id="cc87e-118">ตัวอย่างเช่น ลำดับงานใบสั่งขายสามารถมีงานอัตโนมัติที่ต้องการให้ระบบเพื่อดำเนินการต่อไปนี้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="cc87e-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="cc87e-119">ดำเนินการตรวจสอบเครดิต</span><span class="sxs-lookup"><span data-stu-id="cc87e-119">Perform a credit check.</span></span>
- <span data-ttu-id="cc87e-120">สร้างเรกคอร์ดลูกค้าสำหรับลูกค้า ถ้าเรกคอร์ดยังไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="cc87e-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="cc87e-121">กระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="cc87e-121">Approval processes</span></span>

<span data-ttu-id="cc87e-122">*กระบวนการอนุมัติ* คือกระบวนการที่ประกอบด้วยขั้นตอนแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="cc87e-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="cc87e-123">ในแต่ละขั้นตอนการอนุมัติ ผู้ใช้สามารถดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cc87e-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="cc87e-124">อนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="cc87e-124">Approve the document.</span></span>
- <span data-ttu-id="cc87e-125">ปฏิเสธเอกสาร</span><span class="sxs-lookup"><span data-stu-id="cc87e-125">Reject the document.</span></span>
- <span data-ttu-id="cc87e-126">ร้องขอการเปลี่ยนแปลงที่เอกสาร</span><span class="sxs-lookup"><span data-stu-id="cc87e-126">Request a change to the document.</span></span>
- <span data-ttu-id="cc87e-127">กำหนดเอกสารให้กับผู้ใช้รายอื่นสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="cc87e-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="cc87e-128">องค์ประกอบลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="cc87e-128">Line-item workflow elements</span></span>

<span data-ttu-id="cc87e-129">ลำดับงานสามารถสร้างเพื่อประมวลผลเอกสารหรือสินค้าในรายการบนเอกสาร</span><span class="sxs-lookup"><span data-stu-id="cc87e-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="cc87e-130">ตัวอย่างเช่น คุณสร้างลำดับงานการอนุมัติสำหรับแผ่นเวลาแล้ว</span><span class="sxs-lookup"><span data-stu-id="cc87e-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="cc87e-131">(เราจะอ้างอิงไปที่ลำดับงานนี้เป็น *ลำดับงานเอกสา*) คุณสามารถเพิ่มองค์ประกอบ *ลำดับงานของสินค้าในรายการ* ไปที่ลำดับงานของเอกสารนั้นได้</span><span class="sxs-lookup"><span data-stu-id="cc87e-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="cc87e-132">เมื่อการองค์ประกอบของสินค้าในรายการถูกรัน สินค้าแต่รายการในเอกสารถูกส่งสำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="cc87e-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="cc87e-133">คุณอาจต้องการสินค้าในรายการทั้งหมดที่จะประมวลผล โดยลำดับงานของสินค้าในรายการเดียวกัน หรือคุณอาจต้องการสินค้าแต่ละรายการที่จะประมวลผล โดยลำดับงานของสินค้าในรายการต่างๆ</span><span class="sxs-lookup"><span data-stu-id="cc87e-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="cc87e-134">สมมติว่า พนักงานส่งแผ่นเวลาที่คล้ายคลึงกับรูปต่อไปนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="cc87e-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![ลำดับงานที่มีสินค้าในรายการ](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="cc87e-136">ในสถานการณ์นี้ คุณอาจต้องการสร้างลำดับงานของสินค้าในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cc87e-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="cc87e-137">**ลำดับงานของสินค้าในรายการ 1** – ลำดับงานของสินค้าในรายการนี้ถูกใช้เพื่อประมวลผลสินค้าในรายการที่รหัสโครงการเป็น 1111</span><span class="sxs-lookup"><span data-stu-id="cc87e-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="cc87e-138">**ลำดับงานของสินค้าในรายการ 2** – ลำดับงานของสินค้าในรายการนี้ถูกใช้เพื่อประมวลผลสินค้าในรายการที่รหัสโครงการเป็น 2222</span><span class="sxs-lookup"><span data-stu-id="cc87e-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="cc87e-139">**ลำดับงานของสินค้าในรายการ 3** – ลำดับงานของสินค้าในรายการนี้ถูกใช้เพื่อประมวลผลสินค้าในรายการที่รหัสโครงการเป็น 3333</span><span class="sxs-lookup"><span data-stu-id="cc87e-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="cc87e-140">องค์ประกอบของการควบคุมขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="cc87e-140">Flow-control elements</span></span>

<span data-ttu-id="cc87e-141">องค์ประกอบต่อไปนี้ให้คุณออกแบบลำดับงานที่มีสาขารองหรือสาขาที่รันพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="cc87e-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="cc87e-142">การตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cc87e-142">Manual decision</span></span>

<span data-ttu-id="cc87e-143">หนึ่ง *การตัดสินใจด้วยตนเอง* เป็นจุดที่ลำดับงานแบ่งออกเป็นสองสาขา</span><span class="sxs-lookup"><span data-stu-id="cc87e-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="cc87e-144">ผู้ใช้ต้องตัดสินใจ และการตัดสินใจนี้กำหนดว่าสาขาใดถูกใช้เพื่อประมวลผลเอกสารที่ถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="cc87e-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="cc87e-145">การตัดสินใจแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="cc87e-145">Conditional decision</span></span>

<span data-ttu-id="cc87e-146">หนึ่ง *การตัดสินใจแบบมีเงื่อนไข* ยังเป็นจุดที่ลำดับงานแบ่งออกเป็นสองสาขา</span><span class="sxs-lookup"><span data-stu-id="cc87e-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="cc87e-147">อย่างไรก็ตาม ระบบกำหนดว่าสาขาใดถูกใช้เพื่อประมวลผลเอกสารที่ถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="cc87e-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="cc87e-148">เพื่อทำการตัดสินใจนี้ ระบบจะประเมินเอกสารเพื่อกำหนดว่า เป็นไปตามเงื่อนไขที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cc87e-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="cc87e-149">กิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="cc87e-149">Parallel activity</span></span>

<span data-ttu-id="cc87e-150">หนึ่ง *กิจกรรมคู่ขนาน* เป็นองค์ประกอบลำดับงานที่รวมสาขาลำดับงานสองสาขาขึ้นไปที่รันพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="cc87e-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="cc87e-151">ลำดับงานย่อย</span><span class="sxs-lookup"><span data-stu-id="cc87e-151">Subworkflow</span></span>

<span data-ttu-id="cc87e-152">หนึ่ง *ลำดับงานย่อย* เป็นลำดับงานที่รันภายในบริบทของลำดับงานอื่น</span><span class="sxs-lookup"><span data-stu-id="cc87e-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
