---
title: สร้างลำดับงาน
description: หัวข้อนี้อธิบายวิธีการสร้างลำดับงาน
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
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
ms.openlocfilehash: 7d4a3c5e12b226a7d801d8db9abcbd15738c1ce0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "353367"
---
# <a name="create-workflows"></a><span data-ttu-id="34e31-103">สร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-103">Create workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34e31-104">หัวข้อนี้อธิบายวิธีการสร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="34e31-105">เปิดโปรแกรมแก้ไขลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-105">Open the workflow editor</span></span>

<span data-ttu-id="34e31-106">โมดูล Microsoft Dynamics 365 for Finance and Operations ที่คุณกำลังทำงานอยู่ กำหนดประเภทของเวิร์กโฟลว์ที่คุณสามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="34e31-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="34e31-107">ทำตามขั้นตอนเหล่านี้เพื่อเลือกชนิดของลำดับงานที่จะสร้างและเปิดโปรแกรมแก้ไขลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="34e31-108">เปิดโมดูลที่คุณต้องการสร้างลำดับงานใหม่</span><span class="sxs-lookup"><span data-stu-id="34e31-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="34e31-109">ตัวอย่างเช่น ถ้าต้องการสร้างลำดับงานสำหรับใบขอซื้อ คลิก **การจัดซื้อและการจัดหา**</span><span class="sxs-lookup"><span data-stu-id="34e31-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="34e31-110">คลิก **การตั้งค่า** &gt; **ลำดับงาน\[ชื่อโมดูล]\]**</span><span class="sxs-lookup"><span data-stu-id="34e31-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="34e31-111">ในหน้ารายการที่ปรากฏ บนบานหน้าต่างการดำเนินการ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="34e31-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="34e31-112">ในหน้า **สร้างลำดับงาน** เลือกชนิดของลำดับงานที่จะสร้าง แล้วคลิก **สร้างลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="34e31-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="34e31-113">โปรแกรมแก้ไขลำดับงานปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="34e31-113">The workflow editor appears.</span></span> <span data-ttu-id="34e31-114">ขณะนี้คุณสามารถใช้กระบวนงานต่อไปนี้เพื่อออกแบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="34e31-115">ลากองค์ประกอบลำดับงานบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="34e31-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="34e31-116">พื้นที่ **องค์ประกอบลำดับงาน** ของโปรแกรมแก้ไขลำดับงานประกอบด้วยองค์ประกอบที่คุณสามารถเพิ่มไปยังลำดับงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="34e31-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="34e31-117">เมื่อต้องการเพิ่มองค์ประกอบไปยังลำดับงาน ให้ลากรายการเหล่านั้นบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="34e31-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="34e31-118">เชื่อมต่อองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="34e31-118">Connect the elements</span></span>

<span data-ttu-id="34e31-119">เมื่อต้องการเชื่อมต่อองค์ประกอบลำดับงานหนึ่งไปยังอีกรายการหนึ่ง ให้วางตัวชี้ไว้เหนือองค์ประกอบหนึ่งจนกว่าจะปรากฏจุดเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="34e31-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="34e31-120">คลิกจุดเชื่อมต่อ และลากไปยังองค์ประกอบอื่น</span><span class="sxs-lookup"><span data-stu-id="34e31-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="34e31-121">ตรวจสอบให้แน่ใจว่าเชื่อมต่อองค์ประกอบทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="34e31-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="34e31-122">ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="34e31-123">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="34e31-124">คลิกผืนผ้าใบเพื่อให้แน่ใจว่าไม่มีการเลือกองค์ประกอบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="34e31-125">คลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ** สำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="34e31-126">ทำตามกระบวนงานในหัวข้อ [ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน](configure-workflow-properties.md)</span><span class="sxs-lookup"><span data-stu-id="34e31-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="34e31-127">การตั้งค่าคอนฟิกองค์ประกอบของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="34e31-128">ตั้งค่าคอนฟิกแต่ละองค์ประกอบที่คุณลากลงบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="34e31-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="34e31-129">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกแต่ละองค์ประกอบลำดับงาน ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="34e31-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="34e31-130">ตั้งค่าคอนฟิกงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="34e31-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="34e31-131">ตั้งค่าคอนฟิกงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="34e31-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="34e31-132">การตั้งค่าคอนฟิกกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="34e31-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="34e31-133">ตั้งค่าคอนฟิกขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="34e31-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="34e31-134">ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="34e31-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="34e31-135">ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="34e31-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="34e31-136">ตั้งค่าคอนฟิกกิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="34e31-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="34e31-137">ตั้งค่าคอนฟิกสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="34e31-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="34e31-138">ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="34e31-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="34e31-139">แก้ไขข้อผิดพลาดหรือคำเตือน</span><span class="sxs-lookup"><span data-stu-id="34e31-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="34e31-140">บานหน้าต่าง **ข้อผิดพลาดและคำเตือน** ที่ด้านล่างของโปรแกรมแก้ไขลำดับงานแสดงข้อความที่สร้างขึ้นสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="34e31-141">เมื่อต้องการค้นหาองค์ประกอบที่เกิดข้อผิดพลาดหรือคำเตือนขึ้น ดับเบิลคลิกที่ข้อความแจ้งข้อผิดพลาดหรือคำเตือนนั้น</span><span class="sxs-lookup"><span data-stu-id="34e31-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="34e31-142">คุณต้องแก้ไขข้อผิดพลาดและคำเตือนทั้งหมดก่อนคุณจึงจะสามารถเรียกใช้งานลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="34e31-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="34e31-143">บันทึกและเรียกใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="34e31-143">Save and activate the workflow</span></span>

<span data-ttu-id="34e31-144">เมื่อคุณพร้อมบันทึกและเรียกใช้งานลำดับงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="34e31-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="34e31-145">คลิก **บันทึกและปิด** เพื่อปิดโปรแกรมแก้ไขลำดับงาน และเปิดหน้า **บันทึกลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="34e31-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="34e31-146">การป้อนข้อคิดเห็นเกี่ยวกับการเปลี่ยนแปลงที่คุณทำกับลำดับงาน แล้วคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="34e31-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="34e31-147">ถ้าแก้ไขข้อผิดพลาดและคำเตือนทั้งหมดแล้ว หน้า **เรียกใช้ลำดับงาน** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="34e31-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="34e31-148">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="34e31-148">Select one of the following options:</span></span>

    - <span data-ttu-id="34e31-149">เมื่อต้องการเรียกใช้เวอร์ชันนี้ของลำดับงาน คลิก **เรียกใช้เวอร์ชันใหม่**</span><span class="sxs-lookup"><span data-stu-id="34e31-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="34e31-150">เมื่อลำดับงานทำงานอยู่ ผู้ใช้สามารถส่งเอกสารเพื่อการประมวลผลได้</span><span class="sxs-lookup"><span data-stu-id="34e31-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="34e31-151">ถ้าคุณไม่ต้องการเรียกใช้เวอร์ชันนี้ คลิก **ไม่เรียกใช้เวอร์ชันใหม่**</span><span class="sxs-lookup"><span data-stu-id="34e31-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="34e31-152">คุณสามารถเรียกใช้ลำดับงานได้ในภายหลัง </span><span class="sxs-lookup"><span data-stu-id="34e31-152">You can activate the workflow later.</span></span>
