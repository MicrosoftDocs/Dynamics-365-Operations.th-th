---
title: "ภาพรวมของลำดับงาน"
description: "หัวข้อนี้อธิบายถึงระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations"
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6622f0e5ed6c38bb8131d13aa02061968862678b
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-overview"></a><span data-ttu-id="18de2-103">ภาพรวมของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-103">Workflow overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="18de2-104">หัวข้อนี้อธิบายถึงระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18de2-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="18de2-105">ลำดับงานคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="18de2-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="18de2-106">คำว่า *ลำดับงาน* สามารถกำหนดได้ในสองวิธี: เป็นระบบ และเป็นกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="18de2-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="18de2-107">ลำดับงานคือระบบ</span><span class="sxs-lookup"><span data-stu-id="18de2-107">Workflow is a system</span></span>

<span data-ttu-id="18de2-108">Workflow คือ ระบบที่ถูกติดตั้งด้วย Finance and Operations และที่ทำงานบน Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="18de2-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="18de2-109">ระบบลำดับงานมีฟังก์ชันที่คุณสามารถใช้สร้างลำดับงานหรือกระบวนการทางธุรกิจแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="18de2-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="18de2-110">Workflow คือ กระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="18de2-110">Workflow is a business process</span></span>

<span data-ttu-id="18de2-111">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="18de2-111">A workflow represents a business process.</span></span> <span data-ttu-id="18de2-112">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="18de2-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="18de2-113">ตัวอย่างเช่น แผนภาพต่อไปนี้แสดงลำดับงานสำหรับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="18de2-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![ลำดับงานที่มีองค์ประกอบที่กำหนดให้กับผู้ใช้](./media/workflow_user.gif) 

<span data-ttu-id="18de2-115">เพื่อให้เข้าใจลำดับงานนี้ได้ดีขึ้น สมมติว่า Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 7,000 เหรียญสหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="18de2-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="18de2-116">ในสถานการณ์จำลองนี้ Ivan ต้องตรวจสอบใบเสร็จรับเงินที่ Sam ส่งไปให้</span><span class="sxs-lookup"><span data-stu-id="18de2-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="18de2-117">จากนั้น Frank และ Sue ต้องเป็นผู้อนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="18de2-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="18de2-118">ตอนนี้ สมมติว่า Sam ส่งรายงานค่าใช้จ่ายจำนวนเงินเป็นจำนวนเงิน 11,000 เหรียญสหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="18de2-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="18de2-119">ในสถานการณ์นี้ Ivan ต้องทบทวนการรับสินค้า Frank Sue และ Ann ต้องทำการอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="18de2-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="18de2-120"> ประโยชน์ของการใช้ระบบ Workflow</span><span class="sxs-lookup"><span data-stu-id="18de2-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="18de2-121">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังเช่นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="18de2-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="18de2-122">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="18de2-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="18de2-123">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="18de2-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="18de2-124">**การติดตามกระบวนการ** — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="18de2-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="18de2-125">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="18de2-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="18de2-126">**รายการงานจากส่วนกลาง** — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="18de2-127">บริบทลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-127">Workflow content</span></span>

+ [<span data-ttu-id="18de2-128">สถาปัตยกรรมลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="18de2-129">องค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="18de2-130">การดำเนินการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="18de2-131">สร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="18de2-132">ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="18de2-133">ตั้งค่าคอนฟิกงานที่กำหนดด้วยตนเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="18de2-134">ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="18de2-135">ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="18de2-136">ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="18de2-137">ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="18de2-138">ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="18de2-139">ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="18de2-140">ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="18de2-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="18de2-141">ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="18de2-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

