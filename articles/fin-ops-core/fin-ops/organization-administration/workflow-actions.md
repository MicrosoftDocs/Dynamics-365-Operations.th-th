---
title: การดำเนินการในกระบวนการอนุมัติในลำดับงาน
description: บทความนี้อธิบายการดำเนินการที่ผู้เข้าร่วมในกระบวนการอนุมัติลำดับงานสามารถทำได้
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e622f9a0a50cd6c5dbcbaf9cd5d56b691232c849
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797613"
---
# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="3a199-103">การดำเนินการในกระบวนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3a199-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a199-104">บทความนี้อธิบายการดำเนินการที่ผู้เข้าร่วมในกระบวนการอนุมัติลำดับงานสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="3a199-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="3a199-105">ลำดับงานเกี่ยวข้องกับกลุ่มบุคคลหลายกลุ่ม: ผู้ริเริ่ม รับงาน ผู้ทำการตัดสินใจ และผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="3a199-106">ตัวอย่างเช่น ในลำดับงานรายงานค่าใช้จ่ายต่อไปนี้ Sam คือผู้ริเริ่ม สมาชิกของคิวคือผู้รับงาน John คือผู้ตัดสินใจ Frank Sue และAnn คือผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="3a199-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="3a199-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="3a199-108">ส่วนต่อไปนี้อธิบายการดำเนินการของลำดับงานที่สามารถดำเนินการแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3a199-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="3a199-109">การดำเนินการที่ผู้ริเริ่มสามารถดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="3a199-109">Actions that an originator can perform</span></span>

<span data-ttu-id="3a199-110">ผู้ริเริ่มเริ่มต้นอินสแตนซ์ลำดับงาน โดยการส่งเอกสารการเพื่อประมวลผล</span><span class="sxs-lookup"><span data-stu-id="3a199-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="3a199-111">ตัวอย่างเช่น Sam ต้องคลิกปุ่ม **ส่ง** บนหน้า **รายงานค่าใช้จ่าย** เพื่อส่งรายงานค่าใช้จ่ายของเขา</span><span class="sxs-lookup"><span data-stu-id="3a199-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="3a199-112">การดำเนินการที่ผู้รับงานสามารถดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="3a199-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="3a199-113">สามารถมอบหมายงานให้กับหลายบุคคลได้ หรือคิวรายการงานที่ถูกตรวจสอบโดยคนหลายคน</span><span class="sxs-lookup"><span data-stu-id="3a199-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="3a199-114">อย่างไรก็ตาม มีเพียงบุคคลเดียวที่สามารถทำงานให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-114">However, only one person can complete a task.</span></span> <span data-ttu-id="3a199-115">ตัวอย่างเช่น Sam Sam ได้ทำการส่งรายงานค่าใช้จ่ายและเวียนส่งการรับสินค้าไปยังแผนกรายงานค่าใช้จ่ายขององค์กรของเขาเพื่อตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="3a199-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="3a199-116">สมาชิกของแผนกรายงานค่าใช้จ่าย Adventure Works ตรวจสอบคิว</span><span class="sxs-lookup"><span data-stu-id="3a199-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="3a199-117">Julie หนึ่งในสมาชิกของแผนกนั้น ได้ยอมรับงานตรวจทานรายงานค่าใช้จ่ายและใบเสร็จของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3a199-118">เธอสามารถดำเนินการอย่างใดอย่างหนึ่งต่อไปนี้: ทำให้เสร็จสมบูรณ์ ปฏิเสธ มอบหมาย ร้องขอการเปลี่ยนแปลง มอบหมาย หรือนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="3a199-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="3a199-119">การดำเนินการที่พร้อมใช้งานจะแตกต่างกันไป โดยขึ้นอยู่กับวิธีการที่นักพัฒนาซอฟต์แวร์ออกแบบงาน</span><span class="sxs-lookup"><span data-stu-id="3a199-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="3a199-120">ทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3a199-120">Complete</span></span>

<span data-ttu-id="3a199-121">เมื่อผู้ใช้ทำงานเสร็จสมบูรณ์แล้ว ระบบจะมอบหมายเอกสารที่ได้ส่งสำหรับการประมวลผลให้กับผู้ใช้ถัดไปในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3a199-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="3a199-122">ถ้าไม่จำเป็นต้องมีการประมวลผลเพิ่มเติม กระบวนการลำดับงานจะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="3a199-123">ตัวอย่างเช่น Julie หนึ่งในสมาชิกของแผนกรายงานค่าใช้จ่ายAdventure Works ได้ยอมรับงานตรวจทานรายงานค่าใช้จ่ายและใบเสร็จของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3a199-124">หลังจาก Julie ตรวจทานเสร็จสมบูรณ์แล้ว เอกสารจะถูกมอบหมายให้กับ John</span><span class="sxs-lookup"><span data-stu-id="3a199-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="3a199-125">ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="3a199-125">Reject</span></span>

<span data-ttu-id="3a199-126">เมื่อผู้ใช้ปฏิเสธเอกสาร กระบวนการลำดับงานจะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="3a199-127">ตัวอย่างเช่น Julie หนึ่งในสมาชิกของแผนกรายงานค่าใช้จ่ายAdventure Works ได้ยอมรับงานตรวจทานรายงานค่าใช้จ่ายและใบเสร็จของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3a199-128">ถ้า Julie ปฏิเสธรายงานค่าใช้จ่าย กระบวนการของลำดับงานก็จะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="3a199-129">Sam สามารถส่งรายงานค่าใช้จ่ายอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="3a199-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="3a199-130">เขาสามารถทำการเปลี่ยนแปลงก่อน หรือเขาสามารถส่งเวอร์ชันเดิมอีกครั้งก็ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="3a199-131">ถ้า Sam ส่งรายงานค่าใช้จ่ายอีกครั้ง กระบวนการลำดับงานจะเริ่มต้นที่งานการตรวจทานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3a199-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="3a199-132">มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="3a199-132">Delegate</span></span>

<span data-ttu-id="3a199-133">เมื่อผู้ใช้มอบหมายงาน ระบบจะกำหนดงานให้กับผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="3a199-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="3a199-134">ตัวอย่างเช่น Julie หนึ่งในสมาชิกของแผนกรายงานค่าใช้จ่ายAdventure Works ได้ยอมรับงานตรวจทานรายงานค่าใช้จ่ายและใบเสร็จของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3a199-135">Julie มอบหมายงานนี้กับTim ที่เป็นผู้ช่วยของเธอ</span><span class="sxs-lookup"><span data-stu-id="3a199-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="3a199-136">Tim ทำหน้าที่ในนามของ Julie แล้ว</span><span class="sxs-lookup"><span data-stu-id="3a199-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="3a199-137">ดังนั้น เมื่อTim เสร็จสิ้นการตรวจทานของเขา รายงานค่าใช้จ่ายจะถูกมอบหมายให้กับ John ราวกับว่าJulie ได้ดำเนินการงานนี้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="3a199-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="3a199-138">ร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3a199-138">Request change</span></span>

<span data-ttu-id="3a199-139">เมื่อผู้ใช้ร้องขอการเปลี่ยนแปลงที่เอกสารที่ส่งไปแล้ว เอกสารจะถูกส่งกลับไปที่ผู้ริเริ่ม</span><span class="sxs-lookup"><span data-stu-id="3a199-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="3a199-140">ตัวอย่างเช่น Julie หนึ่งในสมาชิกของแผนกรายงานค่าใช้จ่ายAdventure Works ได้ยอมรับงานตรวจทานรายงานค่าใช้จ่ายและใบเสร็จของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3a199-141">Julie สังเกตพบข้อผิดพลาดบางอย่างในรายงานค่าใช้จ่ายและการร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3a199-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="3a199-142">รายงานค่าใช้จ่ายถูกส่งกลับไปยัง Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="3a199-143">Sam สามารถส่งรายงานค่าใช้จ่ายอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="3a199-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="3a199-144">เขาสามารถทำการเปลี่ยนแปลงที่ร้องขอก่อน หรือเขาสามารถส่งเวอร์ชันเดิมอีกครั้งก็ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="3a199-145">หาก Sam ส่งรายงานค่าใช้จ่ายอีกครั้ง สมาชิกของคิวรายการงานต้องทบทวนรายงานค่าใช้จ่ายและใบเสร็จอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3a199-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="3a199-146">กำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="3a199-146">Reassign</span></span>

<span data-ttu-id="3a199-147">สมาชิกของคิวรายการงานสามารถกำหนดเอกสารที่อยู่ในคิวไปยังคิวอืนอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="3a199-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="3a199-148">ตัวอย่างเช่น Julie หนึ่งในสมาชิกของแผนกรายงานค่าใช้จ่าย Adventure Works กำลังตรวจสอบคิว</span><span class="sxs-lookup"><span data-stu-id="3a199-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="3a199-149">เพื่อรักษาสมดุลของปริมาณงาน เธอสามารถมอบหมายรายงานค่าใช้จ่ายและใบเสร็จที่รวมอยู่ด้วยกัน ให้กับคิวอื่นใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="3a199-150">นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="3a199-150">Release</span></span>

<span data-ttu-id="3a199-151">บางครั้ง สมาชิกของคิวรายการงานอาจยอมรับงาน แต่จากนั้นตัดสินใจได้ว่าเขาหรือเธอไม่สามารถทำงานให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="3a199-152">ในกรณีนี้ บุคคลที่ยอมรับงานสามารถนำเอกสารกลับสู่คิวรายการงานอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="3a199-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="3a199-153">ตัวอย่างเช่น Julie หนึ่งในสมาชิกของแผนกรายงานค่าใช้จ่ายAdventure Works ได้ยอมรับงานตรวจทานรายงานค่าใช้จ่ายและใบเสร็จของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3a199-154">ถ้า Julie ตัดสินใจได้ว่าเธอไม่สามารถทำงานให้เสร็จสมบูรณ์ได้ เธอสามารถนำเอกสารออกได้</span><span class="sxs-lookup"><span data-stu-id="3a199-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="3a199-155">รายงานค่าใช้จ่ายจะถูกส่งกลับไปยังคิว เพื่อให้สมาชิกคนอื่นๆของแผนกรายงานค่าใช้จ่าย Adventure Works สามารถทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3a199-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="3a199-156">การดำเนินการที่ผู้ตัดสินใจสามารถดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="3a199-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="3a199-157">โดยทั่วไป เอกสารถูกมอบหมายให้ผู้ตัดสินใจ เนื่องจากมีคำถามทีผู้ตัดสินใจต้องตอบ</span><span class="sxs-lookup"><span data-stu-id="3a199-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="3a199-158">คำตอบสำหรับคำถามเป็นคำตอบโดยทั่วไป **ใช่** หรือ **ไม่ใช่** หรือ **จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3a199-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="3a199-159">ถ้าผู้ตัดสินใจไม่เลือกตัวเลือกใดๆ เขาหรือเธอสามารถมอบสิทธิ์การตัดสินใจได้</span><span class="sxs-lookup"><span data-stu-id="3a199-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="3a199-160">\[ตัวเลือก 1\] หรือ \[ตัวเลือก 2\]</span><span class="sxs-lookup"><span data-stu-id="3a199-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="3a199-161">ผู้ตัดสินใจต้องตอบคำถามที่เกี่ยวข้องกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3a199-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="3a199-162">คำตอบสำหรับคำถามเป็นคำตอบโดยทั่วไป **ใช่** หรือ **ไม่ใช่** หรือ **จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="3a199-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="3a199-163">คำตอบที่ผู้ตัดสินใจที่เลือกจะกำหนดสาขาของลำดับงานที่ใช้ในกระบวนการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3a199-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="3a199-164">ตัวอย่างเช่น รายงานค่าใช้จ่ายของ Sam ถูกมอบหมายให้กับ John</span><span class="sxs-lookup"><span data-stu-id="3a199-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="3a199-165">จอห์นต้องตัดสินใจว่า ข้อมูลในเอกสารจำเป็นต้องมีการโทรไปหาผู้จัดการของ Sam หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3a199-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="3a199-166">ถ้า John ตัดสินใจว่าการโทรจำเป็น รายงานค่าใช้จ่ายจะถูกมอบหมายให้กับ Aretha ผู้ที่ต้องโทรหาผู้จัดการของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="3a199-167">หาก John ตัดสินใจว่าการโทรไม่จำเป็น รายงานค่าใช้จ่ายจะถูกมอบหมายให้กับ Frank เพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="3a199-168">มอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="3a199-168">Delegate</span></span>

<span data-ttu-id="3a199-169">เมื่อผู้ตัดสินใจมอบสิทธิ์การตัดสินใจ เอกสารถูกกำหนดให้กับผู้ใช้อื่นที่ต้องทำการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="3a199-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="3a199-170">ตัวอย่างเช่น รายงานค่าใช้จ่ายของ Sam ถูกมอบหมายให้กับ John</span><span class="sxs-lookup"><span data-stu-id="3a199-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="3a199-171">จอห์นมอบสิทธิ์การตัดสินใจให้ Maria ที่ผู้ช่วยของเขา</span><span class="sxs-lookup"><span data-stu-id="3a199-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="3a199-172">Maria ทำหน้าที่ในนามของ Johnแล้ว</span><span class="sxs-lookup"><span data-stu-id="3a199-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="3a199-173">ถ้า Maria ตัดสินใจว่าการโทรไปหาผู้จัดการของ Sam จำเป็น รายงานค่าใช้จ่ายจะถูกมอบหมายให้กับ Aretha ผู้ที่ต้องโทรหาผู้จัดการของ Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="3a199-174">หาก Maria ตัดสินใจว่าการโทรไม่จำเป็น รายงานค่าใช้จ่ายจะถูกมอบหมายให้กับ Frank เพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="3a199-175">การดำเนินการที่ผู้อนุมัติสามารถดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="3a199-175">Actions that an approver can perform</span></span>

<span data-ttu-id="3a199-176">เมื่อเอกสารถูกกำหนดให้กับผู้อนุมัติ ผู้อนุมัติสามารถดำเนินการอย่างใดอย่างหนึ่งต่อไปนี้: อนุมัติ ปฏิเสธ มอบสิทธิ์์ หรือร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3a199-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="3a199-177">อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-177">Approve</span></span>

<span data-ttu-id="3a199-178">เมื่อผู้อนุมัติอนุมัติเอกสาร เอกสารที่จะถูกกำหนดให้กับผู้ใช้ถัดไปในลำดับงาน ถ้ามีผู้ใช้ถัดไป</span><span class="sxs-lookup"><span data-stu-id="3a199-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="3a199-179">ถ้าไม่จำเป็นต้องมีการประมวลผลเพิ่มเติม กระบวนการลำดับงานจะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="3a199-180">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 6,000 เหรียญสหรัฐฯ และรายงานถูกมอบหมายให้กับ Frank</span><span class="sxs-lookup"><span data-stu-id="3a199-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="3a199-181">เมื่อ Frank อนุมัติเอกสาร เอกสารนี้จะถูกกำหนดให้กับ Sue เพื่อการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="3a199-182">เมื่อ Sue อนุมัติรายงานค่าใช้จ่ายแล้ว กระบวนการของลำดับงานก็จะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="3a199-183">ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="3a199-183">Reject</span></span>

<span data-ttu-id="3a199-184">เมื่อผู้อนุมัติปฏิเสธเอกสาร กระบวนการลำดับงานจะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="3a199-185">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 12,000 เหรียญสหรัฐฯ และรายงานถูกมอบหมายให้กับ Sue</span><span class="sxs-lookup"><span data-stu-id="3a199-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="3a199-186">ถ้า Sue ปฏิเสธรายงานค่าใช้จ่าย กระบวนการของลำดับงานก็จะสิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="3a199-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="3a199-187">Sam สามารถส่งรายงานค่าใช้จ่ายอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="3a199-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="3a199-188">เขาสามารถทำการเปลี่ยนแปลงก่อน หรือเขาสามารถส่งเวอร์ชันเดิมของรายงานค่าใช้จ่ายอีกครั้งก็ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="3a199-189">ถ้า Sam ส่งรายงานค่าใช้จ่ายอีกครั้ง กระบวนการลำดับงานจะเริ่มต้นที่กระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="3a199-190">มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="3a199-190">Delegate</span></span>

<span data-ttu-id="3a199-191">เมื่อผู้อนุมัติมอบหมายเอกสาร ระบบจะกำหนดเอกสารให้กับผู้ใช้รายอื่นเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="3a199-192">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 12,000 เหรียญสหรัฐฯ และรายงานถูกมอบหมายให้กับ Frank</span><span class="sxs-lookup"><span data-stu-id="3a199-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="3a199-193">Frank มอบหมายรายงานค่าใช้จ่ายให้กับ Ann</span><span class="sxs-lookup"><span data-stu-id="3a199-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="3a199-194">Ann ทำหน้าที่ในนามของ Frank แล้ว</span><span class="sxs-lookup"><span data-stu-id="3a199-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="3a199-195">ดังนั้น เมื่อ Ann อนุมัติเอกสาร จะกำหนดให้กับ Sue สำหรับการอนุมัติ ราวกับว่า Frank ได้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="3a199-196">หลังจาก Sue อนุมัติเอกสาร เอกสารนี้จะถูกส่งให้กับ Ann เพื่อการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="3a199-197">ร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3a199-197">Request change</span></span>

<span data-ttu-id="3a199-198">เมื่อผู้อนุมัติร้องขอการเปลี่ยนแปลงที่เอกสาร เอกสารจะถูกส่งกลับไปที่ผู้ริเริ่ม</span><span class="sxs-lookup"><span data-stu-id="3a199-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="3a199-199">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 12,000 เหรียญสหรัฐฯ และรายงานถูกมอบหมายให้กับ Sue</span><span class="sxs-lookup"><span data-stu-id="3a199-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="3a199-200">ถ้า Sue ร้องขอการเปลี่ยนแปลง รายงานค่าใช้จ่ายจะถูกส่งกลับไปยัง Sam</span><span class="sxs-lookup"><span data-stu-id="3a199-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="3a199-201">Sam สามารถส่งรายงานค่าใช้จ่ายอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="3a199-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="3a199-202">เขาสามารถทำการเปลี่ยนแปลงที่ร้องขอก่อน หรือเขาสามารถส่งเวอร์ชันเดิมของรายงานค่าใช้จ่ายอีกครั้งก็ได้</span><span class="sxs-lookup"><span data-stu-id="3a199-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="3a199-203">ถ้า Sam ส่งรายงานค่าใช้จ่ายอีกครั้ง รายงานนี้จะส่งไปยัง Frank เพื่อทำการอนุมัติเนื่องจาก Frank เป็นผู้อนุมัติคนแรกในกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3a199-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>
