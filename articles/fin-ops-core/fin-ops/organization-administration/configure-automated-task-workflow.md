---
title: ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติสำหรับงานอัตโนมัติ
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f02b128036ebc0bd8789ecafd1e72e26fe31436
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747966"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="f160d-103">ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f160d-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f160d-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติสำหรับงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f160d-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="f160d-105">หากต้องการตั้งค่าคอนฟิกงานอัตโนมัติในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่งานนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="f160d-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f160d-106">แล้วใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f160d-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="f160d-107">การตั้งชื่องาน</span><span class="sxs-lookup"><span data-stu-id="f160d-107">Name the task</span></span>

<span data-ttu-id="f160d-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f160d-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="f160d-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="f160d-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f160d-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="f160d-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f160d-111">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="f160d-111">Specify when notifications are sent</span></span>

<span data-ttu-id="f160d-112">คุณสามารถส่งการแจ้งเตือนไปยังบุคคลต่าง ๆ เมื่อมีการรันและยกเลิกงานอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f160d-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="f160d-113">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะส่งการแจ้งเตือนเมื่อใดและจะส่งให้ใคร</span><span class="sxs-lookup"><span data-stu-id="f160d-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="f160d-114">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="f160d-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="f160d-115">เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเหตุการณ์เพื่อส่งการแจ้งเตือนสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="f160d-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="f160d-116">**การดำเนินการ**– จะส่งการแจ้งเตือนเมื่อมีการรันงาน</span><span class="sxs-lookup"><span data-stu-id="f160d-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="f160d-117">**ยกเลิกแล้ว**– จะส่งการแจ้งเตือนเมื่อมีการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="f160d-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="f160d-118">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="f160d-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="f160d-119">ในแท็บ **ข้อความแจ้งเตือน** ในกล่องข้อความ ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="f160d-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="f160d-120">เมื่อต้องการปรับแต่งการแจ้งเตือน คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="f160d-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="f160d-121">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงการแจ้งเตือนแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f160d-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="f160d-122">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="f160d-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="f160d-123">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="f160d-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f160d-124">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="f160d-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f160d-125">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="f160d-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f160d-126">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="f160d-126">Click **Insert**.</span></span>

6. <span data-ttu-id="f160d-127">เมื่อต้องการเพิ่มคำแปลของการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f160d-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="f160d-128">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="f160d-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="f160d-129">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f160d-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f160d-130">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="f160d-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="f160d-131">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="f160d-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f160d-132">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="f160d-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="f160d-133">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="f160d-133">Click **Close**.</span></span>

7. <span data-ttu-id="f160d-134">ในแท็บ **ผู้รับ** ระบุผู้ที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="f160d-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="f160d-135">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="f160d-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f160d-136">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f160d-136">Option</span></span></th>
    <th><span data-ttu-id="f160d-137">ผู้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="f160d-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="f160d-138">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f160d-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f160d-139">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="f160d-139">Participant</span></span></td>
    <td><span data-ttu-id="f160d-140">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="f160d-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f160d-141">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="f160d-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f160d-142">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="f160d-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f160d-143">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f160d-143">Workflow user</span></span></td>
    <td><span data-ttu-id="f160d-144">ผู้ใช้ที่เข้าร่วมในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f160d-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="f160d-145">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f160d-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f160d-146">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f160d-146">User</span></span></td>
    <td><span data-ttu-id="f160d-147">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f160d-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f160d-148">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="f160d-149">ผู้ใช้ <strong> ที่พร้อมใช้งานรายการ </strong> รวมผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f160d-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f160d-150">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="f160d-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="f160d-151">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="f160d-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]