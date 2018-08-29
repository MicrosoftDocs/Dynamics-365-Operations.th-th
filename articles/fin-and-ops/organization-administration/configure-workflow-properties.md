---
title: "ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของลำดับงาน"
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba03473dd6fc31d51fd4e890acac1cd1494ef5a3
ms.openlocfilehash: a327b85f18f03294a237c3795ae2e1f4a97095f0
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="configure-workflow-properties"></a><span data-ttu-id="757bc-103">ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="757bc-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="757bc-105">เมื่อต้องการตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน เปิดลำดับงานในโปรแกรมแก้ไขลำดับงาน </span><span class="sxs-lookup"><span data-stu-id="757bc-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="757bc-106">คลิกผ้าของโปรแกรมแก้ไขลำดับงาน แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="757bc-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="757bc-107">จากนั้นคุณสามารถใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="757bc-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="757bc-108">การตั้งชื่อลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-108">Name the workflow</span></span>
<span data-ttu-id="757bc-109">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="757bc-110">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="757bc-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="757bc-111">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="757bc-112">เช่น ถ้าคุณสร้างลำดับงานของใบสั่งซื้อสำหรับแต่ละประเทศหรือภูมิภาคที่คุณดำเนินธุรกิจอยู่ คุณสามารถตั้งชื่อลำดับงานของใบสั่งซื้อ **ใบสั่งซื้อเดนมาร์ก** หรือ **ใบสั่งซื้อสเปน**</span><span class="sxs-lookup"><span data-stu-id="757bc-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="757bc-113">การระบุเจ้าของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-113">Specify the workflow owner</span></span>
<span data-ttu-id="757bc-114">เจ้าของลำดับงาน คือบุคคลที่จัดการและรักษาลำดับงานนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="757bc-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="757bc-115">ทำตามขั้นตอนต่อไปนี้ในการระบุเจ้าของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="757bc-116">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="757bc-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="757bc-117">ในรายการ **เจ้าของ** เลือกชื่อของบุคคลที่จะจัดการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="757bc-118">เลือกเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="757bc-118">Select an email template</span></span>
<span data-ttu-id="757bc-119">ทำตามขั้นตอนเหล่านี้เพื่อเลือกเท็มเพลตอีเมลที่ใช้ในการสร้างข้อความแจ้งเตือนเกี่ยวกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="757bc-120">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="757bc-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="757bc-121">ในรายการ **เท็มเพลตอีเมลสำหรับการแจ้งเตือนลำดับงาน** เลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="757bc-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="757bc-122">การป้อนคำแนะนำสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="757bc-122">Enter instructions for users</span></span>
<span data-ttu-id="757bc-123">คุณสามารถให้คำแนะนำแก่ผู้ใช้ที่ส่งเอกสารสำหรับการประมวลผลและการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="757bc-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="757bc-124">ผู้ใช้เหล่านี้จะเรียกว่า *ผู้ริเริ่ม*</span><span class="sxs-lookup"><span data-stu-id="757bc-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="757bc-125">ตัวอย่างเช่น คุณกำลังสร้างลำดับงานใบขอซื้อ และคุณป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="757bc-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="757bc-126">คำแนะนำเหล่านั้นจะปรากฏแก่ผู้ใช้ที่ป้อนใบขอซื้อในหน้า **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="757bc-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="757bc-127">เมื่อต้องการดูคำสั่ง ผู้ริเริ่มจะคลิกไอคอนในแถบข้อความลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="757bc-128">ทำตามขั้นตอนเหล่านี้ในการป้อนคำแนะนำสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="757bc-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="757bc-129">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="757bc-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="757bc-130">ในฟิลด์ **คำแนะนำในการส่ง** ป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="757bc-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="757bc-131">เมื่อต้องการปรับแต่งคำแนะนำ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="757bc-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="757bc-132">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงคำสั่งแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="757bc-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="757bc-133">เมื่อต้องการแทรกตัวยึด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="757bc-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="757bc-134">คลิกในฟิลด์ **คำแนะนำในการส่ง** เพื่อระบุตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="757bc-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="757bc-135">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="757bc-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="757bc-136">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="757bc-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="757bc-137">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="757bc-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="757bc-138">เมื่อต้องการเพิ่มคำแปลของคำแนะนำ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="757bc-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="757bc-139">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="757bc-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="757bc-140">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="757bc-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="757bc-141">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณจะป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="757bc-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="757bc-142">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="757bc-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="757bc-143">เมื่อต้องการปรับแต่งข้อความ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="757bc-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="757bc-144">สำหรับคำแนะนำเกี่ยวกับวิธีการป้อนตัวยึด ดูขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="757bc-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="757bc-145">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="757bc-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="757bc-146">ระบุว่าใช้ลำดับงานนี้เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="757bc-146">Specify when this workflow is used</span></span>
<span data-ttu-id="757bc-147">คุณสามารถสร้างลำดับงานหลายรายการที่ยึดตามชนิดเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="757bc-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="757bc-148">เช่น คุณสามารถสร้างลำดับงานของใบสั่งซื้อสำหรับแต่ละประเทศหรือภูมิภาคที่คุณดำเนินธุรกิจอยู่ เช่น ใบสั่งซื้อเดนมาร์ก และ ใบสั่งซื้อสเปน</span><span class="sxs-lookup"><span data-stu-id="757bc-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="757bc-149">เมื่อคุณมีลำดับงานหลายรายการที่ยึดตามชนิดเดียวกัน คุณต้องระบุว่าใช้ลำดับงานแต่ละรายการเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="757bc-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="757bc-150">สำหรับตัวอย่างข้างต้น คุณระบุเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="757bc-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="757bc-151">ใบสั่งซื้อเดนมาร์กถูกนำมาใช้เมื่อ: ประเทศ/ภูมิภาค = DK</span><span class="sxs-lookup"><span data-stu-id="757bc-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="757bc-152">ใบสั่งซื้อสเปนถูกนำมาใช้เมื่อ: ประเทศ/ภูมิภาค = ES</span><span class="sxs-lookup"><span data-stu-id="757bc-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="757bc-153">ทำตามขั้นตอนเหล่านี้ในการระบุว่าใช้ลำดับงานที่คุณกำลังตั้งค่าคอนฟิกเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="757bc-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="757bc-154">ในบานหน้าต่างทางซ้าย ให้คลิก **การเรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="757bc-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="757bc-155">เลือกกล่องกาเครื่องหมาย **ตั้งค่าเงื่อนไขสำหรับการรันลำดับงานนี้**</span><span class="sxs-lookup"><span data-stu-id="757bc-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="757bc-156">คลิก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="757bc-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="757bc-157">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="757bc-157">Enter a condition.</span></span>
5.  <span data-ttu-id="757bc-158">ป้อนเงื่อนไขเพิ่มเติมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="757bc-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="757bc-159">หากต้องการตรวจสอบว่าเงื่อนไขที่คุณป้อนเข้าไปกำหนดไว้ถูกต้องหรือไม่ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="757bc-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="757bc-160">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="757bc-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="757bc-161">ในหน้า **ทดสอบเงื่อนไขลำดับงาน** ในพื้นที่ **ตรวจสอบความถูกต้องของเงื่อนไข** เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="757bc-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="757bc-162">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="757bc-162">Click **Test**.</span></span> <span data-ttu-id="757bc-163">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณระบุไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="757bc-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="757bc-164">ตัวอย่างเช่น ถ้าคุณกำลังสร้างลำดับงานใบขอซื้อสำหรับสเปน พื้นที่ **ตรวจสอบความถูกต้องของเงื่อนไข** ของหน้าจะแสดงรายการของใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="757bc-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="757bc-165">เมื่อคุณคลิก **ทดสอบ**ระบบจะประเมินใบสั่งซื้อที่เลือกเพื่อกำหนดว่าประเทศ/ภูมิภาคคือ ES หรือไม่</span><span class="sxs-lookup"><span data-stu-id="757bc-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="757bc-166">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่หน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="757bc-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="757bc-167">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="757bc-167">Specify when notifications are sent</span></span>
<span data-ttu-id="757bc-168">เมื่อมีการส่งเอกสารสำหรับการประมวลผล อินสแตนซ์ลำดับงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="757bc-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="757bc-169">คุณสามารถส่งการแจ้งเตือนให้แก่ผู้ใช้เมื่ออินสแตนซ์ลำดับงานที่ยึดตามลำดับงานเริ่มต้นแล้ว เสร็จสมบูรณ์ หยุดการทำงาน หรือหยุดเนื่องจากมีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="757bc-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="757bc-170">ทำตามขั้นตอนเหล่านี้ในการระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="757bc-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="757bc-171">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="757bc-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="757bc-172">เลือกกล่องกาเครื่องหมายสำหรับแต่ละเหตุการณ์ที่ควรทริกเกอร์การแจ้งเตือน:</span><span class="sxs-lookup"><span data-stu-id="757bc-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="757bc-173">**เริ่มต้นแล้ว** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานเริ่มต้นขึ้น</span><span class="sxs-lookup"><span data-stu-id="757bc-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="757bc-174">**หยุด** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานหยุดเนื่องจากมีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="757bc-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="757bc-175">**เสร็จสมบูรณ์** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="757bc-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="757bc-176">**ไม่สามารถแก้ไขได้** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานหยุดเนื่องจากมีข้อผิดพลาดที่ไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="757bc-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="757bc-177">**หยุดการทำงาน** — ส่งการแจ้งเตือนเมื่ออินสแตนซ์ลำดับงานหยุดการทำงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="757bc-178">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="757bc-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="757bc-179">ในแท็บ **ข้อความแจ้งเตือน** ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="757bc-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="757bc-180">เมื่อต้องการปรับแต่งข้อความ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="757bc-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="757bc-181">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงข้อความแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="757bc-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="757bc-182">เมื่อต้องการแทรกตัวยึด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="757bc-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="757bc-183">คลิกในฟิลด์เพื่อระบุตำแหน่งที่ต้องการให้ตัวยึดตำแหน่งปรากฏ</span><span class="sxs-lookup"><span data-stu-id="757bc-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="757bc-184">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="757bc-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="757bc-185">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="757bc-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="757bc-186">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="757bc-186">Click **Insert**.</span></span>
    5.  <span data-ttu-id="757bc-187">ตัวยึด **ข้อความแจ้งเตือน** ทั่วไปที่จะจะรวมเป็น "บันทึกย่อครั้งล่าสุด: %Workflow.Last note%" ซึ่งแสดงข้อคิดเห็นใดๆ จากขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="757bc-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6.  <span data-ttu-id="757bc-188">เมื่อต้องการเพิ่มคำแปลของข้อความ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="757bc-188">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="757bc-189">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="757bc-189">Click **Translations**.</span></span>
    2.  <span data-ttu-id="757bc-190">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="757bc-190">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="757bc-191">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณจะป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="757bc-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="757bc-192">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="757bc-192">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="757bc-193">เมื่อต้องการปรับแต่งข้อความ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="757bc-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="757bc-194">สำหรับคำแนะนำเกี่ยวกับวิธีการป้อนตัวยึด ดูขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="757bc-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="757bc-195">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="757bc-195">Click **Close**.</span></span>

7.  <span data-ttu-id="757bc-196">บนแท็บ **ผู้รับ** ใช้ตัวเลือกต่อไปนี้เพื่อระบุบุคคลที่ควรได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="757bc-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="757bc-197">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="757bc-197">Option</span></span></th>
    <th><span data-ttu-id="757bc-198">ส่งการแจ้งเตือนให้แก่ผู้ใช้เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="757bc-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="757bc-199">เมื่อต้องการส่งการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="757bc-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="757bc-200">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="757bc-200">Participant</span></span></td>
    <td><span data-ttu-id="757bc-201">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="757bc-201">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="757bc-202">บนแท็บ <strong>ผู้รับ</strong> คลิก <strong>ผู้เข้าร่วม</strong></span><span class="sxs-lookup"><span data-stu-id="757bc-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="757bc-203">บนแท็บ <strong>ตามบทบาท</strong> ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="757bc-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="757bc-204">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="757bc-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="757bc-205">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-205">Workflow user</span></span></td>
    <td><span data-ttu-id="757bc-206">ผู้ใช้ที่เป็นผู้เข้าร่วมในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="757bc-206">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="757bc-207">บนแท็บ <strong>ผู้รับ</strong> คลิก <strong>ผู้ใช้ลำดับงาน</strong></span><span class="sxs-lookup"><span data-stu-id="757bc-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="757bc-208">บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้เข้าร่วมในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="757bc-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="757bc-209">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="757bc-209">User</span></span></td>
    <td><span data-ttu-id="757bc-210">ผู้ใช้ Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="757bc-210">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="757bc-211">บนแท็บ <strong>ผู้รับ</strong> คลิก <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="757bc-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="757bc-212">บนแท็บ <strong>ผู้ใช้</strong> รายการ <strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Dynamics 365 for Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="757bc-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="757bc-213">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน แล้วย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="757bc-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="757bc-214">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="757bc-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="757bc-215">การป้อนข้อคิดเห็นเกี่ยวกับการเปลี่ยนแปลงที่คุณทำกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="757bc-215">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="757bc-216">หากต้องการป้อนข้อคิดเห็นเกี่ยวกับการเปลี่ยนแปลงที่คุณทำกับลำดับงานนี้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="757bc-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="757bc-217">ในบานหน้าต่างทางซ้าย ให้คลิก **หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="757bc-217">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="757bc-218">ในฟิลด์ **ป้อนข้อคิดเห็นเกี่ยวกับลำดับงาน** ป้อนข้อคิดเห็นของคุณ</span><span class="sxs-lookup"><span data-stu-id="757bc-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="757bc-219">ตรวจทานข้อคิดเห็นของคุณ</span><span class="sxs-lookup"><span data-stu-id="757bc-219">Review your comments.</span></span> <span data-ttu-id="757bc-220">หลังจากที่คุณเพิ่มข้อคิดเห็นแล้ว คุณไม่สามารถปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="757bc-220">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="757bc-221">คลิก **เพิ่ม** เพื่อเพิ่มข้อคิดเห็นของคุณลงในพื้นที่ **ประวัติข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="757bc-221">Click **Add** to add your comments to the **Comment history** area.</span></span>





