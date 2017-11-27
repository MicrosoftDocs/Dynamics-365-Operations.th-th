---
title: "ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติสำหรับงานอัตโนมัติ"
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
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e8189f8d16e9b6dcbc339a23c1af5402c0316ce3
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="924e4-103">ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="924e4-103">Configure an automated task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="924e4-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติสำหรับงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="924e4-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="924e4-105">หากต้องการตั้งค่าคอนฟิกงานอัตโนมัติในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่งานนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="924e4-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="924e4-106">แล้วใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="924e4-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="924e4-107">การตั้งชื่องาน</span><span class="sxs-lookup"><span data-stu-id="924e4-107">Name the task</span></span>
<span data-ttu-id="924e4-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="924e4-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="924e4-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="924e4-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="924e4-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="924e4-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="924e4-111">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="924e4-111">Specify when notifications are sent</span></span>
<span data-ttu-id="924e4-112">คุณสามารถส่งการแจ้งเตือนไปยังบุคคลต่าง ๆ เมื่อมีการรันและยกเลิกงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="924e4-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="924e4-113">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะส่งการแจ้งเตือนเมื่อใดและจะส่งให้ใคร</span><span class="sxs-lookup"><span data-stu-id="924e4-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="924e4-114">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="924e4-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="924e4-115">เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเหตุการณ์เพื่อส่งการแจ้งเตือนสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="924e4-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="924e4-116">**การดำเนินการ**– จะส่งการแจ้งเตือนเมื่อมีการรันงาน</span><span class="sxs-lookup"><span data-stu-id="924e4-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="924e4-117">**ยกเลิกแล้ว**– จะส่งการแจ้งเตือนเมื่อมีการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="924e4-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="924e4-118">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="924e4-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="924e4-119">ในแท็บ **ข้อความแจ้งเตือน** ในกล่องข้อความ ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="924e4-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="924e4-120">เมื่อต้องการปรับแต่งการแจ้งเตือน คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="924e4-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="924e4-121">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงการแจ้งเตือนแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="924e4-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="924e4-122">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="924e4-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="924e4-123">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="924e4-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="924e4-124">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="924e4-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="924e4-125">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="924e4-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="924e4-126">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="924e4-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="924e4-127">เมื่อต้องการเพิ่มคำแปลของการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="924e4-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="924e4-128">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="924e4-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="924e4-129">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="924e4-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="924e4-130">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="924e4-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="924e4-131">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="924e4-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="924e4-132">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="924e4-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="924e4-133">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="924e4-133">Click **Close**.</span></span>

7.  <span data-ttu-id="924e4-134">ในแท็บ **ผู้รับ** ระบุผู้ที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="924e4-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="924e4-135">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="924e4-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="924e4-136">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="924e4-136">Option</span></span></th>
    <th><span data-ttu-id="924e4-137">ผู้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="924e4-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="924e4-138">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="924e4-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="924e4-139">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="924e4-139">Participant</span></span></td>
    <td><span data-ttu-id="924e4-140">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="924e4-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="924e4-141">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="924e4-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="924e4-142">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="924e4-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="924e4-143">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="924e4-143">Workflow user</span></span></td>
    <td><span data-ttu-id="924e4-144">ผู้ใช้ที่เข้าร่วมในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="924e4-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="924e4-145">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="924e4-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="924e4-146">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="924e4-146">User</span></span></td>
    <td><span data-ttu-id="924e4-147">ผู้ใช้ Microsoft Dynamics 365 for Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="924e4-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="924e4-148">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="924e4-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="924e4-149"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="924e4-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="924e4-150">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="924e4-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="924e4-151">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="924e4-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





