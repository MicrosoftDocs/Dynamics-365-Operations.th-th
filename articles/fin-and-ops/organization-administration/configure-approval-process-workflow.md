---
title: "ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน"
description: "ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับกระบวนการอนุมัติ"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 212e9c32c7bb22b0ee0450e04b4090c540df7b54
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="83f71-103">ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="83f71-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83f71-104">ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="83f71-105">เมื่อต้องการตั้งค่าคอนฟิกกระบวนการอนุมัติในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่องค์ประกอบการอนุมัตินั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดแบบฟอร์ม **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="83f71-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="83f71-106">การตั้งชื่อกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="83f71-107">ทำตามขั้นตอนเหล่านี้เพื่อป้อนชื่อสำหรับกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="83f71-108">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="83f71-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="83f71-109">ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="83f71-110">ระบุเวลาที่จะให้ระบบดำเนินการกับเอกสารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="83f71-111">คุณสามารถตั้งค่าคอนฟิกระบบเพื่อดำเนินการกับเอกสารโดยอัตโนมัติถ้าตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="83f71-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="83f71-112">ตัวอย่างเช่น ระบบสามารถอนุมัติรายงานค่าใช้จ่ายที่มียอดเงินรวมที่น้อยกว่า 100 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="83f71-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="83f71-113">ทำตามขั้นตอนเหล่านี้เพื่อระบุเวลาที่จะให้ระบบดำเนินการกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="83f71-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="83f71-114">ในบานหน้าต่างทางซ้าย ให้คลิก **การดำเนินการโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="83f71-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="83f71-115">เลือกกล่องกาเครื่องหมาย **เปิดใช้งานการดำเนินการโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="83f71-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="83f71-116">คลิก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="83f71-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="83f71-117">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="83f71-117">Enter a condition.</span></span>
5.  <span data-ttu-id="83f71-118">ป้อนเงื่อนไขเพิ่มเติม หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="83f71-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="83f71-119">หากต้องการตรวจสอบว่าเงื่อนไขที่คุณป้อนเข้าไปตั้งค่าคอนฟิกไว้ถูกต้องหรือไม่ ให้ทำตามขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="83f71-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="83f71-120">คลิก **ทดสอบ** เพื่อเปิดแบบฟอร์ม **ทดสอบเงื่อนไขลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="83f71-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="83f71-121">เลือกเรกคอร์ดในพื้นที่ของแบบฟอร์ม **ตรวจสอบเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="83f71-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="83f71-122">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="83f71-122">Click **Test**.</span></span> <span data-ttu-id="83f71-123">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณกำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="83f71-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="83f71-124">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่แบบฟอร์ม **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="83f71-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="83f71-125">ในรายการ **การดำเนินการให้สมบูรณ์โดยอัตโนมัติ** เลือกการดำเนินการที่ระบบควรใช้กับเอกสารนั้น</span><span class="sxs-lookup"><span data-stu-id="83f71-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="83f71-126">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="83f71-126">Specify when notifications are sent</span></span>
<span data-ttu-id="83f71-127">คุณสามารถส่งการแจ้งเตือนไปยังบุคคลต่างๆ เมื่อเอกสารมีการอนุมัติ ถูกปฏิเสธ มอบหมาย หรือเลื่อนระดับ หรือเมื่อมีการร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="83f71-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="83f71-128">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะส่งการแจ้งเตือนเมื่อใดและจะส่งให้ใคร</span><span class="sxs-lookup"><span data-stu-id="83f71-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="83f71-129">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="83f71-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="83f71-130">เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเหตุการณ์เพื่อส่งการแจ้งเตือนสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="83f71-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="83f71-131">**มอบหมาย** – เมื่อมีการกำหนดเอกสารนี้ให้กับผู้ใช้รายอื่นเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="83f71-132">**เลื่อนระดับ** – เมื่อผู้ใช้ที่กำหนดไม่ได้ดำเนินการกับเอกสารในเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="83f71-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="83f71-133">**อนุมัติ** – เมื่อเอกสารได้รับการอนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="83f71-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="83f71-134">**ปฏิเสธ** – เมื่อเอกสารถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="83f71-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="83f71-135">**ร้องขอการเปลี่ยนแปลง** – เมื่อผู้ใช้ที่กำหนดได้ร้องขอการเปลี่ยนแปลงเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="83f71-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="83f71-136">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="83f71-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="83f71-137">คลิกแท็บ **ข้อความการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="83f71-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="83f71-138">ในกล่องข้อความ ให้ป้อนข้อความสำหรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="83f71-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="83f71-139">เมื่อต้องการให้เนื้อหาเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตำแหน่งลงไปได้ ซึ่งจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อแสดงต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="83f71-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="83f71-140">เมื่อต้องการแทรกตัวยึด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="83f71-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="83f71-141">คลิกในกล่องข้อความของที่ตั้งที่ควรปรากฏตัวยึดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="83f71-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="83f71-142">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="83f71-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="83f71-143">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="83f71-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="83f71-144">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="83f71-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="83f71-145">เมื่อต้องการเพิ่มคำแปลของการแจ้งเตือน ให้คลิก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="83f71-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="83f71-146">ในแบบฟอร์มที่แสดง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="83f71-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="83f71-147">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="83f71-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="83f71-148">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณจะป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="83f71-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="83f71-149">ในกล่องข้อความ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="83f71-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="83f71-150">เมื่อต้องการปรับแต่งข้อความ ให้แทรกตัวยึดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="83f71-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="83f71-151">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="83f71-151">Click **Close**.</span></span>

8.  <span data-ttu-id="83f71-152">คลิกแท็บ **ผู้รับ**</span><span class="sxs-lookup"><span data-stu-id="83f71-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="83f71-153">ระบุว่าจะส่งการแจ้งเตือนให้ใคร</span><span class="sxs-lookup"><span data-stu-id="83f71-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="83f71-154">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 10</span><span class="sxs-lookup"><span data-stu-id="83f71-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="83f71-155">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="83f71-155">Option</span></span></th>
    <th><span data-ttu-id="83f71-156">ผู้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="83f71-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="83f71-157">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="83f71-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="83f71-158"><strong>ผู้เข้าร่วม</strong></span><span class="sxs-lookup"><span data-stu-id="83f71-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="83f71-159">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="83f71-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="83f71-160">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>คลิกที่แท็บ <strong>ตามบทบาท</strong></span><span class="sxs-lookup"><span data-stu-id="83f71-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="83f71-161">ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="83f71-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="83f71-162">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="83f71-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="83f71-163"><strong>ผู้ใช้ลำดับงาน</strong></span><span class="sxs-lookup"><span data-stu-id="83f71-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="83f71-164">ผู้ใช้ที่เข้าร่วมในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="83f71-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="83f71-165">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>คลิกแท็บ <strong>ผู้ใช้ลำดับงาน</strong></span><span class="sxs-lookup"><span data-stu-id="83f71-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="83f71-166">ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="83f71-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="83f71-167"><strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="83f71-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="83f71-168">ผู้ใช้ Microsoft Dynamics 365 for Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="83f71-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="83f71-169">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="83f71-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="83f71-170">รายการ <strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Microsoft Dynamics 365 for Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="83f71-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="83f71-171">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong>:</span><span class="sxs-lookup"><span data-stu-id="83f71-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="83f71-172">ทำซ้ำขั้นตอนที่ 3 ถึง 9 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="83f71-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="83f71-173"> ระบุผู้อนุมัติขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="83f71-173">Specify a final approver</span></span>
<span data-ttu-id="83f71-174">คุณอาจต้องการแต่งตั้งผู้อนุมัติขั้นสุดท้ายสำหรับสถานการณ์จำลองที่ผู้อนุมัติเป็นบุคคลที่ส่งเอกสารเพื่อการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="83f71-175">ทำตามขั้นตอนเหล่านี้เพื่อระบุผู้อนุมัติขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="83f71-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="83f71-176">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="83f71-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="83f71-177">เลือกกล่องกาเครื่องหมาย **ใช้ผู้อนุมัติขั้นสุดท้าย**</span><span class="sxs-lookup"><span data-stu-id="83f71-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="83f71-178">ในรายการ เลือกผู้ใช้ที่จะเป็นผู้อนุมัติขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="83f71-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="83f71-179">การกำหนดขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="83f71-179">Set a time limit</span></span>
<span data-ttu-id="83f71-180">ทำตามขั้นตอนเหล่านี้ถ้าต้องดำเนินกระบวนการอนุมัติให้เสร็จสมบูรณ์ในเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="83f71-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

| <span data-ttu-id="83f71-181">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="83f71-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f71-182">ตัวเลือกที่คุณเลือกในขั้นตอนเหล่านี้จะแทนที่ตัวเลือกที่คุณเลือกในพื้นที่ **การกำหนด** และ **การเลื่อนระดับ** ของขั้นตอนการอนุมัติต่างๆ</span><span class="sxs-lookup"><span data-stu-id="83f71-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="83f71-183">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="83f71-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="83f71-184">เลือกกล่องกาเครื่องหมาย **ตั้งค่าขีดจำกัดเวลาสำหรับ** **องค์ประกอบลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="83f71-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="83f71-185">ในฟิลด์ **ระยะเวลา** ระบุเวลาที่ต้องดำเนินกระบวนการอนุมัติให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f71-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="83f71-186">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="83f71-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="83f71-187">**ชั่วโมง** – ป้อนจำนวนชั่วโมงที่กระบวนการอนุมัติจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f71-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="83f71-188">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="83f71-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="83f71-189">**วัน** – ป้อนจำนวนวันที่กระบวนการอนุมัติจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f71-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="83f71-190">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="83f71-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="83f71-191">**สัปดาห์** – ป้อนจำนวนสัปดาห์ที่กระบวนการอนุมัติจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f71-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="83f71-192">**เดือน** – เลือกวันและสัปดาห์ที่กระบวนการอนุมัติจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f71-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="83f71-193">ตัวอย่างเช่น คุณอาจต้องการดำเนินกระบวนการอนุมัติให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="83f71-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="83f71-194">**ปี** – เลือกวัน สัปดาห์ และเดือนที่กระบวนการอนุมัติจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="83f71-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="83f71-195">ตัวอย่างเช่น คุณอาจต้องการดำเนินกระบวนการอนุมัติให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="83f71-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="83f71-196">ระบบจะดำเนินการกับเอกสารหากเกินขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="83f71-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="83f71-197">ในรายการ **การดำเนินการ** เลือกการดำเนินการที่ระบบควรใช้</span><span class="sxs-lookup"><span data-stu-id="83f71-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="83f71-198">ระบุการดำเนินการที่ผู้ใช้ใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="83f71-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="83f71-199">เมื่อมีการกำหนดเอกสารให้กับผู้ใช้รายอื่นเป็นผู้อนุมัติ ผู้อนุมัติจะต้องดำเนินการกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="83f71-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="83f71-200">ทำตามขั้นตอนเหล่านี้เพื่อระบุการดำเนินการที่ผู้ใช้สามารถใช้กับเอกสารที่ส่งได้</span><span class="sxs-lookup"><span data-stu-id="83f71-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="83f71-201">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="83f71-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="83f71-202">เลือกกล่องกาเครื่องหมาย **อนุมัติ** ถ้าผู้ใช้สามารถอนุมัติเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="83f71-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="83f71-203">เลือกกล่องกาเครื่องหมาย **ปฏิเสธ** ถ้าผู้ใช้สามารถปฏิเสธเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="83f71-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="83f71-204">เลือกกล่องกาเครื่องหมาย  **ร้องขอการเปลี่ยนแปลง** ถ้าผู้ใช้สามารถร้องขอการเปลี่ยนแปลงเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="83f71-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="83f71-205">เลือกกล่องกาเครื่องหมาย **มอบหมาย** ถ้าผู้ใช้สามารถมอบหมายเอกสารให้กับผู้ใช้รายอื่นเพื่อขออนุมัติได้</span><span class="sxs-lookup"><span data-stu-id="83f71-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="83f71-206">**หมายเหตุ**: กล่องกาเครื่องหมาย **เปิดใช้งานการดำเนินการจากรายการงานในเว็บไซต์องค์กร** ไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="83f71-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="83f71-207"> ตั้งค่าคอนฟิกขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-207">Configure the approval steps</span></span>
<span data-ttu-id="83f71-208">กระบวนการอนุมัติประกอบด้วยขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="83f71-209">ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มขั้นตอนกระบวนการอนุมัติและขั้นตอนการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="83f71-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="83f71-210">ในโปรแกรมแก้ไขลำดับงาน ดับเบิลคลิกที่กระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="83f71-211">โปรแกรมแก้ไขลำดับงานแสดงขั้นตอนกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="83f71-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="83f71-212">เมื่อต้องการเพิ่มขั้นตอนการอนุมัติ ลากขั้นตอนจากพื้นที่ **องค์ประกอบลำดับงาน** ไปที่ผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="83f71-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="83f71-213">เมื่อต้องการตั้งค่าคอนฟิกขั้นตอนการอนุมัติ ให้ดูที่ [ตั้งค่าคอนฟิกขั้นตอนการอนุมัติ](configure-approval-step-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="83f71-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






