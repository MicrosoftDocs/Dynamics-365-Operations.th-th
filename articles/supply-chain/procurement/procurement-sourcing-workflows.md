---
title: ลำดับงานการจัดซื้อและการจัดหา
description: องค์กรบางองค์กรต้องการให้ใบขอซื้อและใบสั่งซื้อ ได้รับการอนุมัติโดยผู้ใช้อื่นที่ไม่ใช่บุคคลที่ป้อนธุรกรรม เพื่อตั้งค่ากระบวนการอนุมัติ คุณสามารถสร้างลำดับงานได้
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af614b7f29144d02a853ef15b008f2a21d3d3aa5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019765"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="b7e8b-104">ลำดับงานการจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="b7e8b-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7e8b-105">องค์กรบางองค์กรต้องการให้ใบขอซื้อและใบสั่งซื้อ ได้รับการอนุมัติโดยผู้ใช้อื่นที่ไม่ใช่บุคคลที่ป้อนธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b7e8b-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="b7e8b-106">เพื่อตั้งค่ากระบวนการอนุมัติ คุณสามารถสร้างลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="b7e8b-107">ลำดับงานแสดงถึงกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-107">A workflow represents a business process.</span></span> <span data-ttu-id="b7e8b-108">โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร</span><span class="sxs-lookup"><span data-stu-id="b7e8b-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b7e8b-109">มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="b7e8b-110">**กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b7e8b-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b7e8b-111">การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="b7e8b-112">**การติดตามกระบวนการ** — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b7e8b-113">ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b7e8b-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="b7e8b-114">**รายการงานส่วนกลาง**— ผู้ใช้สามารถดูรายการงานส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้ลำดับงานทั้งหมดที่จะเข้าร่วมในระหว่างนั้น</span><span class="sxs-lookup"><span data-stu-id="b7e8b-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="b7e8b-115">ซึ่งพร้อมใช้งานในหน้ารายการงาน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="b7e8b-116">ชนิดของลำดับงานที่คุณสามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-116">The types of workflows that you can create</span></span>

<span data-ttu-id="b7e8b-117">ชนิดลำดับงานต่อไปนี้จะพร้อมใช้งานสำหรับการจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="b7e8b-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="b7e8b-118">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b7e8b-118">Type</span></span> | <span data-ttu-id="b7e8b-119">ใช้ชนิดนี้กับ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="b7e8b-120">การตรวจทานใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-120">Purchase requisition review</span></span> | <span data-ttu-id="b7e8b-121">สร้างการทบทวนและลำดับงานการอนุมัติสำหรับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="b7e8b-122">การตรวจทานรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-122">Purchase requisition line review</span></span> | <span data-ttu-id="b7e8b-123">สร้างการทบทวนและลำดับงานการอนุมัติสำหรับรายการใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="b7e8b-124">ลำดับงานใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-124">Purchase order workflow</span></span> | <span data-ttu-id="b7e8b-125">สร้างลำดับงานการตรวจทานและการอนุมัติสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="b7e8b-126">ลำดับงานรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-126">Purchase order line workflow</span></span> | <span data-ttu-id="b7e8b-127">สร้างลำดับงานการตรวจทานและการอนุมัติสำหรับรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="b7e8b-128">ลำดับงานการเพิ่มใบสมัครของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b7e8b-128">Vendor add application workflow</span></span> | <span data-ttu-id="b7e8b-129">สร้างการทบทานและลำดับงานการอนุมัติสำหรับการเพิ่มผู้จัดจำหน่ายใหม่ โดยใช้คำขอของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b7e8b-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="b7e8b-130">เมื่อคุณกำลังเพิ่มลำดับงานใหม่ คุณอาจจะเห็นลำดับงานที่ล้าสมัยต่อไปนี้แสดงรายการอยู่ในกล่องโต้ตอบ **สร้างลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="b7e8b-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="b7e8b-131">ข้อมูลเหล่านี้เกี่ยวข้องกับฟังก์ชัน *การยืนยันการรับสินค้า* ที่พร้อมใช้งานใน [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows) แต่ขณะนี้ไม่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="b7e8b-132">ลำดับงานเหล่านี้ไม่ได้รับการสนับสนุนในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="b7e8b-133">ลำดับงานการแจ้งเตือนวันที่ครบกำหนดจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b7e8b-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="b7e8b-134">ลำดับงานการแจ้งเตือนใบแจ้งหนี้ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="b7e8b-135">ลำดับงานการแจ้งเตือนใบรับสินค้าล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b7e8b-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="b7e8b-136">ลำดับงานการแจ้งเตือนการปฏิเสธใบรับสินค้าที่ยังไม่ได้ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="b7e8b-137">การสร้างแผนงาน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-137">Creating a workflow</span></span>

<span data-ttu-id="b7e8b-138">เมื่อต้องการสร้างลำดับงาน ให้ไปที่การจัดซื้อและการจัดหา &gt; การตั้งค่า &gt; การจัดซื้อและการจัดหาลำดับงาน และสร้างลำดับงานใหม่โดยการเลือกชนิดของลำดับงานที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="b7e8b-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="b7e8b-139">ในผืนผ้าใบลำดับงาน คุณสามารถลากองค์ประกอบลำดับงานลงในโปรแกรมออกแบบ และลิงค์องค์ประกอบไปยังขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="b7e8b-140">ควรตั้งค่าคอนฟิกองค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-140">The workflow elements should be configured.</span></span> <span data-ttu-id="b7e8b-141">สำหรับการอนุมัติและองค์ประกอบลำดับงาน คุณสามารถตั้งค่าคอนฟิกที่ผู้เข้าร่วมควรดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="b7e8b-142">ชนิดของผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="b7e8b-142">Types of participants</span></span>

<span data-ttu-id="b7e8b-143">คุณสามารถกำหนดขั้นตอนการอนุมัติให้กลุ่มหรือผู้เข้าร่วมต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="b7e8b-144">กลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-144">User group</span></span> | <span data-ttu-id="b7e8b-145">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b7e8b-145">Description</span></span> |
|---|---|
| <span data-ttu-id="b7e8b-146">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="b7e8b-146">Participant</span></span> | <span data-ttu-id="b7e8b-147">กำหนดขั้นตอนการอนุมัติให้กับสมาชิกของกลุ่มหรือบทบาท</span><span class="sxs-lookup"><span data-stu-id="b7e8b-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="b7e8b-148">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="b7e8b-148">Hierarchy</span></span> | <span data-ttu-id="b7e8b-149">กำหนดขั้นตอนการอนุมัติให้กับผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="b7e8b-150">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-150">Workflow user</span></span> | <span data-ttu-id="b7e8b-151">กำหนดขั้นตอนการอนุมัติให้กับผู้ใช้ของลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="b7e8b-152">คิว</span><span class="sxs-lookup"><span data-stu-id="b7e8b-152">Queue</span></span> | <span data-ttu-id="b7e8b-153">กำหนดขั้นตอนการอนุมัติให้กับคิวรายการงาน</span><span class="sxs-lookup"><span data-stu-id="b7e8b-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="b7e8b-154">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b7e8b-154">User</span></span> | <span data-ttu-id="b7e8b-155">กำหนดขั้นตอนการอนุมัติให้กับผู้ใช้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b7e8b-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b7e8b-156">Additional resources</span></span>

- [<span data-ttu-id="b7e8b-157">การกำหนดลำดับงานของกระบวนการทางธุรกิจสำหรับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="b7e8b-158">ลำดับงานของใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="b7e8b-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="b7e8b-159">เตรียมความพร้อมผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b7e8b-159">Onboard vendors</span></span>](vendor-onboarding.md)
