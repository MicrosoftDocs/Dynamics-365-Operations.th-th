---
title: ภาพรวมของระบบลำดับงาน
description: หัวข้อนี้อธิบายระบบลำดับงาน
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef77a5d81d12ec92eea86b1dd9902d9e3d80b33
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812374"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="7556a-103">ภาพรวมของระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7556a-104">หัวข้อนี้อธิบายระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="7556a-105">ลำดับงานคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="7556a-105">What is workflow?</span></span>

<span data-ttu-id="7556a-106">คำว่า *ลำดับงาน* สามารถกำหนดได้ในสองวิธี: เป็นระบบ และเป็นกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7556a-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="7556a-107">ลำดับงานคือระบบ</span><span class="sxs-lookup"><span data-stu-id="7556a-107">Workflow is a system</span></span>

<span data-ttu-id="7556a-108">การลำดับงานคือระบบที่ปฏิบัติการบน Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="7556a-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="7556a-109">ระบบลำดับงานมีฟังก์ชันที่คุณสามารถใช้สร้างลำดับงานหรือกระบวนการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="7556a-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="7556a-110">Workflow คือ กระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7556a-110">Workflow is a business process</span></span>

<span data-ttu-id="7556a-111">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7556a-111">A workflow represents a business process.</span></span> <span data-ttu-id="7556a-112">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="7556a-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="7556a-113">ตัวอย่างเช่น แผนภาพต่อไปนี้แสดงลำดับงานสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7556a-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![ลำดับงานที่มีองค์ประกอบที่กำหนดให้กับผู้ใช้](./media/workflow_user.gif)

<span data-ttu-id="7556a-115">เพื่อให้เข้าใจลำดับงานนี้ได้ดีขึ้น สมมติว่า Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 7,000 เหรียญสหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="7556a-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="7556a-116">ในสถานการณ์จำลองนี้ Ivan ต้องตรวจสอบใบเสร็จรับเงินที่ Sam ส่งไปให้</span><span class="sxs-lookup"><span data-stu-id="7556a-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="7556a-117">จากนั้น Frank และ Sue ต้องเป็นผู้อนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7556a-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="7556a-118">ตอนนี้ สมมติว่า Sam ส่งรายงานค่าใช้จ่ายจำนวนเงินเป็นจำนวนเงิน 11,000 เหรียญสหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="7556a-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="7556a-119">ในสถานการณ์นี้ Ivan ต้องทบทวนการรับสินค้า Frank Sue และ Ann ต้องทำการอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7556a-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="7556a-120"> ประโยชน์ของการใช้ระบบ Workflow</span><span class="sxs-lookup"><span data-stu-id="7556a-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="7556a-121">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังเช่นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7556a-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="7556a-122">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7556a-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="7556a-123">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="7556a-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="7556a-124">**การติดตามกระบวนการ** — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7556a-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="7556a-125">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7556a-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="7556a-126">**รายการงานจากส่วนกลาง** — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="7556a-127">บริบทลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-127">Workflow content</span></span>

+ [<span data-ttu-id="7556a-128">สถาปัตยกรรมระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="7556a-129">องค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="7556a-130">การดำเนินการในกระบวนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="7556a-131">ภาพรวมของการสร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="7556a-132">ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="7556a-133">ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="7556a-134">ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="7556a-135">ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="7556a-136">ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="7556a-137">ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="7556a-138">ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="7556a-139">ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="7556a-140">ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="7556a-141">ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="7556a-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="7556a-142">FAQ เกี่ยวกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7556a-142">Workflow FAQ</span></span>](workflow-FAQ.md)
