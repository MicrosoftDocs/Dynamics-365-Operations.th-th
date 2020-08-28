---
title: ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของลำดับงาน
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d01a784b0f0cbfce30f1197278f015b236ef0b8
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698155"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="6d80b-103">ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d80b-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="6d80b-105">เมื่อต้องการตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน เปิดลำดับงานในโปรแกรมแก้ไขลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="6d80b-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="6d80b-106">คลิกผ้าของโปรแกรมแก้ไขลำดับงาน แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="6d80b-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="6d80b-107">จากนั้นคุณสามารถใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="6d80b-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="6d80b-108">การตั้งชื่อลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-108">Name the workflow</span></span>

<span data-ttu-id="6d80b-109">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="6d80b-110">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="6d80b-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6d80b-111">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="6d80b-112">เช่น ถ้าคุณสร้างลำดับงานของใบสั่งซื้อสำหรับแต่ละประเทศหรือภูมิภาคที่คุณดำเนินธุรกิจอยู่ คุณสามารถตั้งชื่อลำดับงานของใบสั่งซื้อ **ใบสั่งซื้อเดนมาร์ก** หรือ **ใบสั่งซื้อสเปน**</span><span class="sxs-lookup"><span data-stu-id="6d80b-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="6d80b-113">การระบุเจ้าของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-113">Specify the workflow owner</span></span>

<span data-ttu-id="6d80b-114">เจ้าของลำดับงาน คือบุคคลที่จัดการและรักษาลำดับงานนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="6d80b-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="6d80b-115">ทำตามขั้นตอนต่อไปนี้ในการระบุเจ้าของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="6d80b-116">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="6d80b-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6d80b-117">ในรายการ **เจ้าของ** เลือกชื่อของบุคคลที่จะจัดการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="6d80b-118">เลือกเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="6d80b-118">Select an email template</span></span>

<span data-ttu-id="6d80b-119">ทำตามขั้นตอนเหล่านี้เพื่อเลือกเท็มเพลตอีเมลที่ใช้ในการสร้างข้อความแจ้งเตือนเกี่ยวกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="6d80b-120">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="6d80b-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6d80b-121">ในรายการ **เท็มเพลตอีเมลสำหรับการแจ้งเตือนลำดับงาน** เลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6d80b-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="6d80b-122">การป้อนคำแนะนำสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-122">Enter instructions for users</span></span>

<span data-ttu-id="6d80b-123">คุณสามารถให้คำแนะนำแก่ผู้ใช้ที่ส่งเอกสารสำหรับการประมวลผลและการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="6d80b-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="6d80b-124">ผู้ใช้เหล่านี้จะเรียกว่า *ผู้ริเริ่ม*</span><span class="sxs-lookup"><span data-stu-id="6d80b-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="6d80b-125">ตัวอย่างเช่น คุณกำลังสร้างลำดับงานใบขอซื้อ และคุณป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="6d80b-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="6d80b-126">คำแนะนำเหล่านั้นจะปรากฏแก่ผู้ใช้ที่ป้อนใบขอซื้อในหน้า **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="6d80b-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="6d80b-127">เมื่อต้องการดูคำสั่ง ผู้ริเริ่มจะคลิกไอคอนในแถบข้อความลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="6d80b-128">ทำตามขั้นตอนเหล่านี้ในการป้อนคำแนะนำสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="6d80b-129">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="6d80b-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6d80b-130">ในฟิลด์ **คำแนะนำในการส่ง** ป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="6d80b-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="6d80b-131">เมื่อต้องการปรับแต่งคำแนะนำ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="6d80b-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="6d80b-132">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงคำสั่งแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="6d80b-133">เมื่อต้องการแทรกตัวยึด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6d80b-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="6d80b-134">คลิกในฟิลด์ **คำแนะนำในการส่ง** เพื่อระบุตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="6d80b-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="6d80b-135">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="6d80b-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="6d80b-136">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="6d80b-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="6d80b-137">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="6d80b-137">Click **Insert**.</span></span>

4. <span data-ttu-id="6d80b-138">เมื่อต้องการเพิ่มคำแปลของคำแนะนำ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6d80b-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="6d80b-139">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="6d80b-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="6d80b-140">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6d80b-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="6d80b-141">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณจะป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="6d80b-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="6d80b-142">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="6d80b-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="6d80b-143">เมื่อต้องการปรับแต่งข้อความ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="6d80b-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="6d80b-144">สำหรับคำแนะนำเกี่ยวกับวิธีการป้อนตัวยึด ดูขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="6d80b-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="6d80b-145">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="6d80b-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="6d80b-146">ระบุเวลาที่ใช้ลำดับงานนี้ผ่านเงื่อนไขการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="6d80b-147">คุณสามารถสร้างลำดับงานหลายรายการโดยใช้ชนิดลำดับงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6d80b-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="6d80b-148">เมื่อคุณมีลำดับงานหลายรายการที่ยึดตามชนิดเดียวกัน คุณต้องระบุว่าใช้ลำดับงานแต่ละรายการโดยใช้เงื่อนไขการใช้งานเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="6d80b-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="6d80b-149">ถ้าไม่เป็นไปตามเงื่อนไขการเรียกใช้งาน จะมีการใช้ลำดับงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6d80b-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="6d80b-150">ในทำนองเดียวกัน ถ้ามีการตั้งค่าคอนฟิกลำดับงานเดียวที่กำหนดไว้สำหรับชนิดลำดับงานเท่านั้น จะมีการใช้การตั้งค่าคอนฟิกลำดับงานโดยไม่คำนึงถึงเงื่อนไขการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="6d80b-151">ตัวอย่างเช่น คุณสามารถสร้างลำดับงานของใบขอซื้อสำหรับแต่ละประเทศ/ภูมิภาคที่คุณดำเนินการ เช่น ใบขอซื้อประเทศเดนมาร์ก และใบสั่งซื้อประเทศสเปน ตามเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="6d80b-152">ใบสั่งซื้อเดนมาร์กถูกนำมาใช้เมื่อ: ประเทศ/ภูมิภาค = DK</span><span class="sxs-lookup"><span data-stu-id="6d80b-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="6d80b-153">ใบสั่งซื้อสเปนถูกนำมาใช้เมื่อ: ประเทศ/ภูมิภาค = ES</span><span class="sxs-lookup"><span data-stu-id="6d80b-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="6d80b-154">ทำตามขั้นตอนเหล่านี้ในการระบุว่าใช้ลำดับงานที่คุณกำลังตั้งค่าคอนฟิกเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="6d80b-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="6d80b-155">ในบานหน้าต่างทางซ้าย ให้คลิก **การเรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="6d80b-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="6d80b-156">เลือกกล่องกาเครื่องหมาย **ตั้งค่าเงื่อนไขสำหรับการรันลำดับงานนี้**</span><span class="sxs-lookup"><span data-stu-id="6d80b-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="6d80b-157">คลิก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="6d80b-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="6d80b-158">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="6d80b-158">Enter a condition.</span></span>
5. <span data-ttu-id="6d80b-159">ป้อนเงื่อนไขเพิ่มเติมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="6d80b-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="6d80b-160">รันลำดับงานด้วยเรกคอร์ดเป้าหมายบางรายการ เพื่อตรวจสอบว่าเงื่อนไขรวมและไม่รวมเรกคอร์ดอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6d80b-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="6d80b-161">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="6d80b-161">Specify when notifications are sent</span></span>

<span data-ttu-id="6d80b-162">เมื่อมีการส่งเอกสารสำหรับการประมวลผล อินสแตนซ์ลำดับงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6d80b-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="6d80b-163">คุณสามารถส่งการแจ้งเตือนให้แก่ผู้ใช้เมื่ออินสแตนซ์ลำดับงานที่ยึดตามลำดับงานเริ่มต้นแล้ว เสร็จสมบูรณ์ หยุดการทำงาน หรือหยุดเนื่องจากมีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="6d80b-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="6d80b-164">ทำตามขั้นตอนเหล่านี้ในการระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="6d80b-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="6d80b-165">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="6d80b-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="6d80b-166">เลือกกล่องกาเครื่องหมายสำหรับแต่ละเหตุการณ์ที่ควรทริกเกอร์การแจ้งเตือน:</span><span class="sxs-lookup"><span data-stu-id="6d80b-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="6d80b-167">**เริ่มต้นแล้ว** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานเริ่มต้นขึ้น</span><span class="sxs-lookup"><span data-stu-id="6d80b-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="6d80b-168">**หยุด** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานหยุดเนื่องจากมีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="6d80b-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="6d80b-169">**เสร็จสมบูรณ์** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6d80b-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="6d80b-170">**ไม่สามารถแก้ไขได้** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานหยุดเนื่องจากมีข้อผิดพลาดที่ไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="6d80b-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="6d80b-171">**หยุดการทำงาน** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานหยุดการทำงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="6d80b-172">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="6d80b-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="6d80b-173">ในแท็บ **ข้อความแจ้งเตือน** ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="6d80b-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="6d80b-174">เมื่อต้องการปรับแต่งข้อความ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="6d80b-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="6d80b-175">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงข้อความแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="6d80b-176">เมื่อต้องการแทรกตัวยึด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6d80b-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="6d80b-177">คลิกในฟิลด์เพื่อระบุตำแหน่งที่ต้องการให้ตัวยึดตำแหน่งปรากฏ</span><span class="sxs-lookup"><span data-stu-id="6d80b-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="6d80b-178">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="6d80b-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="6d80b-179">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="6d80b-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="6d80b-180">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="6d80b-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="6d80b-181">ตัวยึด **ข้อความการแจ้งเตือน** ทั่วไปที่จะจะรวมคือ "บันทึกย่อครั้งล่าสุด: %Workflow.Last note%" ซึ่งแสดงข้อคิดเห็นใดๆ จากขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="6d80b-182">เมื่อต้องการเพิ่มคำแปลของข้อความ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6d80b-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="6d80b-183">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="6d80b-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="6d80b-184">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6d80b-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="6d80b-185">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณจะป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="6d80b-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="6d80b-186">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="6d80b-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="6d80b-187">เมื่อต้องการปรับแต่งข้อความ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="6d80b-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="6d80b-188">สำหรับคำแนะนำเกี่ยวกับวิธีการป้อนตัวยึด ดูขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="6d80b-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="6d80b-189">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="6d80b-189">Click **Close**.</span></span>

7. <span data-ttu-id="6d80b-190">บนแท็บ **ผู้รับ** ใช้ตัวเลือกต่อไปนี้เพื่อระบุบุคคลที่ควรได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="6d80b-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="6d80b-191">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6d80b-191">Option</span></span></th>
    <th><span data-ttu-id="6d80b-192">ส่งการแจ้งเตือนให้แก่ผู้ใช้เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="6d80b-193">เมื่อต้องการส่งการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="6d80b-194">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="6d80b-194">Participant</span></span></td>
    <td><span data-ttu-id="6d80b-195">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="6d80b-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="6d80b-196">บนแท็บ <strong>ผู้รับ</strong> คลิก <strong>ผู้เข้าร่วม</strong></span><span class="sxs-lookup"><span data-stu-id="6d80b-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="6d80b-197">บนแท็บ <strong>ตามบทบาท</strong> ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="6d80b-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="6d80b-198">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="6d80b-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="6d80b-199">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-199">Workflow user</span></span></td>
    <td><span data-ttu-id="6d80b-200">ผู้ใช้ที่เป็นผู้เข้าร่วมในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="6d80b-201">บนแท็บ <strong>ผู้รับ</strong> คลิก <strong>ผู้ใช้ลำดับงาน</strong></span><span class="sxs-lookup"><span data-stu-id="6d80b-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="6d80b-202">บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้เข้าร่วมในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="6d80b-203">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6d80b-203">User</span></span></td>
    <td><span data-ttu-id="6d80b-204">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="6d80b-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="6d80b-205">บนแท็บ <strong>ผู้รับ</strong> คลิก <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="6d80b-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="6d80b-206">บนแท็บผู้ใช้ <strong>แท็บ</strong> ผู้ใช้ที่พร้อมใช้งาน <strong>รายการ</strong> ประกอบด้วยผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6d80b-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="6d80b-207">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน แล้วย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="6d80b-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="6d80b-208">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="6d80b-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="6d80b-209">การป้อนข้อคิดเห็นเกี่ยวกับการเปลี่ยนแปลงที่คุณทำกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6d80b-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="6d80b-210">หากต้องการป้อนข้อคิดเห็นเกี่ยวกับการเปลี่ยนแปลงที่คุณทำกับลำดับงานนี้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6d80b-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="6d80b-211">ในบานหน้าต่างทางซ้าย ให้คลิก **หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="6d80b-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="6d80b-212">ในฟิลด์ **ป้อนข้อคิดเห็นเกี่ยวกับลำดับงาน** ป้อนข้อคิดเห็นของคุณ</span><span class="sxs-lookup"><span data-stu-id="6d80b-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="6d80b-213">ตรวจทานข้อคิดเห็นของคุณ</span><span class="sxs-lookup"><span data-stu-id="6d80b-213">Review your comments.</span></span> <span data-ttu-id="6d80b-214">หลังจากที่คุณเพิ่มข้อคิดเห็นแล้ว คุณไม่สามารถปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="6d80b-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="6d80b-215">คลิก **เพิ่ม** เพื่อเพิ่มข้อคิดเห็นของคุณลงในพื้นที่ **ประวัติข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="6d80b-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
