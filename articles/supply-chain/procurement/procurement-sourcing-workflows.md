---
title: "ลำดับงานการจัดซื้อและการจัดหา"
description: "องค์กรบางองค์กรต้องการให้ใบขอซื้อและใบสั่งซื้อ ได้รับการอนุมัติโดยผู้ใช้อื่นที่ไม่ใช่บุคคลที่ป้อนธุรกรรม เพื่อตั้งค่ากระบวนการอนุมัติ คุณสามารถสร้างลำดับงานได้"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="2288f-104">ลำดับงานการจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="2288f-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2288f-105">องค์กรบางองค์กรต้องการให้ใบขอซื้อและใบสั่งซื้อ ได้รับการอนุมัติโดยผู้ใช้อื่นที่ไม่ใช่บุคคลที่ป้อนธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="2288f-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="2288f-106">เพื่อตั้งค่ากระบวนการอนุมัติ คุณสามารถสร้างลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="2288f-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="2288f-107">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="2288f-107">A workflow represents a business process.</span></span> <span data-ttu-id="2288f-108">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="2288f-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="2288f-109">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2288f-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="2288f-110">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2288f-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="2288f-111">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="2288f-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="2288f-112">**การติดตามกระบวนการ** — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2288f-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="2288f-113">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2288f-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="2288f-114">**รายการงานส่วนกลาง**— ผู้ใช้สามารถดูรายการงานส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้ลำดับงานทั้งหมดที่จะเข้าร่วมในระหว่างนั้น</span><span class="sxs-lookup"><span data-stu-id="2288f-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="2288f-115">ซึ่งพร้อมใช้งานในหน้ารายการงาน</span><span class="sxs-lookup"><span data-stu-id="2288f-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="2288f-116">ชนิดของลำดับงานที่คุณสามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="2288f-116">The types of workflows that you can create</span></span>
<span data-ttu-id="2288f-117">ชนิดลำดับงานต่อไปนี้จะพร้อมใช้งานสำหรับการจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="2288f-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2288f-118">**ชนิด**</span><span class="sxs-lookup"><span data-stu-id="2288f-118">**Type**</span></span>                         | <span data-ttu-id="2288f-119">**ใช้ชนิดนี้กับ**</span><span class="sxs-lookup"><span data-stu-id="2288f-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="2288f-120">การตรวจทานใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-120">Purchase requisition review</span></span>      | <span data-ttu-id="2288f-121">สร้างลำดับลำดับงานการตรวจทานสำหรับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="2288f-122">การตรวจทานรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-122">Purchase requisition line review</span></span> | <span data-ttu-id="2288f-123">สร้างลำดับลำดับงานการตรวจทานสำหรับรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="2288f-124">ลำดับงานใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-124">Purchase order workflow</span></span>          | <span data-ttu-id="2288f-125">สร้างลำดับงานการตรวจทานและการอนุมัติสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="2288f-126">ลำดับงานรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-126">Purchase order line workflow</span></span>     | <span data-ttu-id="2288f-127">สร้างลำดับงานการตรวจทานและการอนุมัติสำหรับรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="2288f-128">การสร้างแผนงาน</span><span class="sxs-lookup"><span data-stu-id="2288f-128">Creating a workflow</span></span>
<span data-ttu-id="2288f-129">เมื่อต้องการสร้างลำดับงาน ให้ไปที่การจัดซื้อและการจัดหา &gt; การตั้งค่า &gt; การจัดซื้อและการจัดหาลำดับงาน และสร้างลำดับงานใหม่โดยการเลือกชนิดของลำดับงานที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="2288f-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="2288f-130">ในผืนผ้าใบลำดับงาน คุณสามารถลากองค์ประกอบลำดับงานลงในโปรแกรมออกแบบ และลิงค์องค์ประกอบไปยังขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="2288f-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="2288f-131">ควรตั้งค่าคอนฟิกองค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="2288f-131">The workflow elements should be configured.</span></span> <span data-ttu-id="2288f-132">สำหรับการอนุมัติและองค์ประกอบลำดับงาน คุณสามารถตั้งค่าคอนฟิกที่ผู้เข้าร่วมควรดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="2288f-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="2288f-133">ชนิดของผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="2288f-133">Types of participants</span></span>
----------------------

<span data-ttu-id="2288f-134">คุณสามารถกำหนดขั้นตอนการอนุมัติให้กลุ่มหรือผู้เข้าร่วมต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2288f-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="2288f-135">กลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2288f-135">User group</span></span>    | <span data-ttu-id="2288f-136">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2288f-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="2288f-137">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="2288f-137">Participant</span></span>   | <span data-ttu-id="2288f-138">กำหนดขั้นตอนการอนุมัติให้กับสมาชิกของกลุ่มหรือบทบาท</span><span class="sxs-lookup"><span data-stu-id="2288f-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="2288f-139">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="2288f-139">Hierarchy</span></span>     | <span data-ttu-id="2288f-140">กำหนดขั้นตอนการอนุมัติให้กับผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2288f-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="2288f-141">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="2288f-141">Workflow user</span></span> | <span data-ttu-id="2288f-142">กำหนดขั้นตอนการอนุมัติให้กับผู้ใช้ของลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="2288f-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="2288f-143">คิว</span><span class="sxs-lookup"><span data-stu-id="2288f-143">Queue</span></span>         | <span data-ttu-id="2288f-144">กำหนดขั้นตอนการอนุมัติให้กับคิวรายการงาน</span><span class="sxs-lookup"><span data-stu-id="2288f-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="2288f-145">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2288f-145">User</span></span>          | <span data-ttu-id="2288f-146">กำหนดขั้นตอนการอนุมัติให้กับผู้ใช้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2288f-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="2288f-147">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="2288f-147">See also</span></span>
--------

[<span data-ttu-id="2288f-148">การกำหนดลำดับงานของกระบวนการทางธุรกิจสำหรับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="2288f-149">ลำดับงานใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="2288f-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




