---
title: ภาพรวมของการสร้างลำดับงาน
description: หัวข้อนี้อธิบายวิธีการสร้างลำดับงาน
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a643be553f3fcdfbe53f2024982a596e498830a8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811322"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="c21c5-103">ภาพรวมของการสร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c21c5-104">หัวข้อนี้อธิบายวิธีการสร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="c21c5-105">เปิดโปรแกรมแก้ไขลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-105">Open the workflow editor</span></span>

<span data-ttu-id="c21c5-106">โมดูลที่คุณกำลังทำงานอยู่ จะกำหนดประเภทของลำดับงานที่คุณสามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="c21c5-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="c21c5-107">ทำตามขั้นตอนเหล่านี้เพื่อเลือกชนิดของลำดับงานที่จะสร้างและเปิดโปรแกรมแก้ไขลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="c21c5-108">เปิดโมดูลที่คุณต้องการสร้างลำดับงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c21c5-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="c21c5-109">ตัวอย่างเช่น ถ้าต้องการสร้างลำดับงานสำหรับใบขอซื้อ คลิก **การจัดซื้อและการจัดหา**</span><span class="sxs-lookup"><span data-stu-id="c21c5-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="c21c5-110">คลิก **การตั้งค่า** &gt; **ลำดับงาน\[ชื่อโมดูล]\]**</span><span class="sxs-lookup"><span data-stu-id="c21c5-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="c21c5-111">ในหน้ารายการที่ปรากฏ บนบานหน้าต่างการดำเนินการ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c21c5-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="c21c5-112">ในหน้า **สร้างลำดับงาน** เลือกชนิดของลำดับงานที่จะสร้าง แล้วคลิก **สร้างลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="c21c5-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="c21c5-113">โปรแกรมแก้ไขลำดับงานปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c21c5-113">The workflow editor appears.</span></span> <span data-ttu-id="c21c5-114">ขณะนี้คุณสามารถใช้กระบวนงานต่อไปนี้เพื่อออกแบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="c21c5-115">ลากองค์ประกอบลำดับงานบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="c21c5-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="c21c5-116">พื้นที่ **องค์ประกอบลำดับงาน** ของโปรแกรมแก้ไขลำดับงานประกอบด้วยองค์ประกอบที่คุณสามารถเพิ่มไปยังลำดับงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c21c5-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="c21c5-117">เมื่อต้องการเพิ่มองค์ประกอบไปยังลำดับงาน ให้ลากรายการเหล่านั้นบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="c21c5-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="c21c5-118">เชื่อมต่อองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="c21c5-118">Connect the elements</span></span>

<span data-ttu-id="c21c5-119">เมื่อต้องการเชื่อมต่อองค์ประกอบลำดับงานหนึ่งไปยังอีกรายการหนึ่ง ให้วางตัวชี้ไว้เหนือองค์ประกอบหนึ่งจนกว่าจะปรากฏจุดเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c21c5-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="c21c5-120">คลิกจุดเชื่อมต่อ และลากไปยังองค์ประกอบอื่น</span><span class="sxs-lookup"><span data-stu-id="c21c5-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="c21c5-121">ตรวจสอบให้แน่ใจว่าเชื่อมต่อองค์ประกอบทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="c21c5-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="c21c5-122">ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="c21c5-123">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="c21c5-124">คลิกผืนผ้าใบเพื่อให้แน่ใจว่าไม่มีการเลือกองค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="c21c5-125">คลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ** สำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="c21c5-126">ทำตามกระบวนงานในหัวข้อ [ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน](configure-workflow-properties.md)</span><span class="sxs-lookup"><span data-stu-id="c21c5-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="c21c5-127">การตั้งค่าคอนฟิกองค์ประกอบของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="c21c5-128">ตั้งค่าคอนฟิกแต่ละองค์ประกอบที่คุณลากลงบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="c21c5-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="c21c5-129">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกแต่ละองค์ประกอบลำดับงาน ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c21c5-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="c21c5-130">ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="c21c5-131">ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="c21c5-132">ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="c21c5-133">ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="c21c5-134">ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="c21c5-135">ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="c21c5-136">ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="c21c5-137">ตั้งค่าคอนฟิกสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="c21c5-138">ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="c21c5-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="c21c5-139">แก้ไขข้อผิดพลาดหรือคำเตือน</span><span class="sxs-lookup"><span data-stu-id="c21c5-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="c21c5-140">บานหน้าต่าง **ข้อผิดพลาดและคำเตือน** ที่ด้านล่างของโปรแกรมแก้ไขลำดับงานแสดงข้อความที่สร้างขึ้นสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="c21c5-141">เมื่อต้องการค้นหาองค์ประกอบที่เกิดข้อผิดพลาดหรือคำเตือนขึ้น ดับเบิลคลิกที่ข้อความแจ้งข้อผิดพลาดหรือคำเตือนนั้น</span><span class="sxs-lookup"><span data-stu-id="c21c5-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="c21c5-142">คุณต้องแก้ไขข้อผิดพลาดและคำเตือนทั้งหมดก่อนคุณจึงจะสามารถเรียกใช้งานลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="c21c5-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="c21c5-143">บันทึกและเรียกใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c21c5-143">Save and activate the workflow</span></span>

<span data-ttu-id="c21c5-144">เมื่อคุณพร้อมบันทึกและเรียกใช้งานลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c21c5-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="c21c5-145">คลิก **บันทึกและปิด** เพื่อปิดโปรแกรมแก้ไขลำดับงาน และเปิดหน้า **บันทึกลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="c21c5-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="c21c5-146">การป้อนข้อคิดเห็นเกี่ยวกับการเปลี่ยนแปลงที่คุณทำกับลำดับงาน แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c21c5-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="c21c5-147">ถ้าแก้ไขข้อผิดพลาดและคำเตือนทั้งหมดแล้ว หน้า **เรียกใช้ลำดับงาน** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c21c5-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="c21c5-148">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c21c5-148">Select one of the following options:</span></span>

    - <span data-ttu-id="c21c5-149">เมื่อต้องการเรียกใช้เวอร์ชันนี้ของลำดับงาน คลิก **เรียกใช้เวอร์ชันใหม่**</span><span class="sxs-lookup"><span data-stu-id="c21c5-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="c21c5-150">เมื่อลำดับงานทำงานอยู่ ผู้ใช้สามารถส่งเอกสารเพื่อการประมวลผลได้</span><span class="sxs-lookup"><span data-stu-id="c21c5-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="c21c5-151">ถ้าคุณไม่ต้องการเรียกใช้เวอร์ชันนี้ คลิก **ไม่เรียกใช้เวอร์ชันใหม่**</span><span class="sxs-lookup"><span data-stu-id="c21c5-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="c21c5-152">คุณสามารถเรียกใช้ลำดับงานได้ในภายหลัง </span><span class="sxs-lookup"><span data-stu-id="c21c5-152">You can activate the workflow later.</span></span>
