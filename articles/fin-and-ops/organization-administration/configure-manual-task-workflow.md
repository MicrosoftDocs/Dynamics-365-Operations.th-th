---
title: ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของงานที่กำหนดด้วยตนเอง
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 669fce3ddade4d6e0a130da2420ab33ca4ff4671
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "309759"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="bd72b-103">ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd72b-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bd72b-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="bd72b-105">หากต้องการตั้งค่าคอนฟิกงานที่กำหนดด้วยตนเองในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่งานนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="bd72b-106">แล้วใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bd72b-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="bd72b-107">การตั้งชื่องาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-107">Name the task</span></span>

<span data-ttu-id="bd72b-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bd72b-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="bd72b-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="bd72b-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="bd72b-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="bd72b-111">การป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bd72b-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="bd72b-112">คุณต้องระบุบรรทัดชื่อเรื่องและคำแนะนำให้กับผู้ใช้ที่กำหนดงานนี้ให้</span><span class="sxs-lookup"><span data-stu-id="bd72b-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="bd72b-113">ตัวอย่างเช่น ถ้าคุณกำลังตั้งค่าคอนฟิกงานสำหรับใบขอซื้อ ผู้ใช้ที่กำหนดให้กับงานจะเห็นบรรทัดชื่อเรื่องและคำแนะนำในหน้า **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="bd72b-114">บรรทัดชื่อเรื่องจะปรากฏขึ้นในแถบข้อความบนหน้า</span><span class="sxs-lookup"><span data-stu-id="bd72b-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="bd72b-115">จากนั้นผู้ใช้สามารถคลิกไอคอนในแถบข้อความเพื่อดูคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bd72b-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="bd72b-116">ทำตามขั้นตอนเหล่านี้เพื่อป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bd72b-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="bd72b-117">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="bd72b-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="bd72b-118">ในฟิลด์ **ชื่อเรื่องรายการงาน** ป้อนบรรทัดชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="bd72b-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="bd72b-119">เมื่อต้องการปรับแต่งบรรทัดชื่อเรื่อง คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="bd72b-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="bd72b-120">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงบรรทัดชื่อเรื่องแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="bd72b-121">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="bd72b-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="bd72b-122">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="bd72b-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="bd72b-123">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="bd72b-124">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="bd72b-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="bd72b-125">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="bd72b-125">Click **Insert**.</span></span>

4. <span data-ttu-id="bd72b-126">เมื่อต้องการเพิ่มคำแปลของบรรทัดชื่อเรื่อง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="bd72b-127">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="bd72b-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="bd72b-128">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bd72b-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="bd72b-129">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd72b-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="bd72b-130">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd72b-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="bd72b-131">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="bd72b-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="bd72b-132">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-132">Click **Close**.</span></span>

5. <span data-ttu-id="bd72b-133">ในฟิลด์ **คำแนะนำรายการงาน** ป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bd72b-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="bd72b-134">เมื่อต้องการปรับแต่งคำแนะนำ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="bd72b-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="bd72b-135">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงคำสั่งแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="bd72b-136">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="bd72b-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="bd72b-137">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="bd72b-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="bd72b-138">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="bd72b-139">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="bd72b-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="bd72b-140">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="bd72b-140">Click **Insert**.</span></span>

7. <span data-ttu-id="bd72b-141">เมื่อต้องการเพิ่มคำแปลของคำแนะนำ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="bd72b-142">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="bd72b-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="bd72b-143">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bd72b-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="bd72b-144">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd72b-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="bd72b-145">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd72b-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="bd72b-146">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 6</span><span class="sxs-lookup"><span data-stu-id="bd72b-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="bd72b-147">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="bd72b-148">การกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-148">Assign the task</span></span>

<span data-ttu-id="bd72b-149">ทำตามขั้นตอนเหล่านี้เพื่อระบุผู้ที่ควรกำหนดงานที่กำหนดด้วยตนเองให้</span><span class="sxs-lookup"><span data-stu-id="bd72b-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="bd72b-150">ในบานหน้าต่างทางซ้าย ให้คลิก **การกำหนด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="bd72b-151">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="bd72b-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="bd72b-152">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bd72b-152">Option</span></span></th>
    <th><span data-ttu-id="bd72b-153">ผู้ใช้ที่ได้รับการกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="bd72b-154">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bd72b-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="bd72b-155">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="bd72b-155">Participant</span></span></td>
    <td><span data-ttu-id="bd72b-156">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="bd72b-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-157">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="bd72b-158">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-159">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="bd72b-160">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bd72b-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-161">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="bd72b-162">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="bd72b-163">ชื่อเหล่านี้คือผู้ใช้ที่สามารถกำหนดงานได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="bd72b-164">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="bd72b-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="bd72b-165">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="bd72b-166">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="bd72b-167">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="bd72b-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="bd72b-168">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรกำหนดให้กับผู้ใช้ใดในช่วงงาน:</span><span class="sxs-lookup"><span data-stu-id="bd72b-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="bd72b-169"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– งานถูกกำหนดให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="bd72b-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="bd72b-170"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> งานถูกกำหนดให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="bd72b-171"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – งานไม่ถูกกำหนดให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bd72b-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="bd72b-172">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bd72b-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-173">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-173">Workflow user</span></span></td>
    <td><span data-ttu-id="bd72b-174">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bd72b-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="bd72b-175">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-176">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-176">User</span></span></td>
    <td><span data-ttu-id="bd72b-177">ผู้ใช้ Microsoft Dynamics 365 for Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bd72b-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-178">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="bd72b-179"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bd72b-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="bd72b-180">เลือกผู้ใช้ที่จะกำหนดงาน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-181">คิว</span><span class="sxs-lookup"><span data-stu-id="bd72b-181">Queue</span></span></td>
    <td><span data-ttu-id="bd72b-182">คิวรายการงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-183">หลังจากที่คุณเลือก <strong>คิว</strong>คลิกที่แท็บ <strong>ตามคิว</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="bd72b-184">เมื่อต้องการกำหนดงานในคิวเฉพาะ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="bd72b-185">ในรายการ <strong>ชนิดของคิว</strong> เลือก <strong>คิวรายการงาน</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd72b-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="bd72b-186">ในรายการ <strong>ชื่อคิว</strong> เลือกคิว</span><span class="sxs-lookup"><span data-stu-id="bd72b-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="bd72b-187">ถ้าเงื่อนไขที่ระบุควรกำหนดคิวที่กำหนดงานให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="bd72b-188">ในรายการ <strong>ชนิดของคิว</strong> เลือก <strong>คิวรายการงานแบบมีเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="bd72b-189">ในรายการ <strong>ชื่อคิว</strong> เลือก <strong>คิวแบบมีเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="bd72b-190">ตัวเลือกนี้จะใช้สำหรับลำดับงานเพียงไม่กี่รายการ เช่น การจัดการกรณี</span><span class="sxs-lookup"><span data-stu-id="bd72b-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="bd72b-191">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="bd72b-192">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-192">Select one of the following options:</span></span>

    - <span data-ttu-id="bd72b-193">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="bd72b-194">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd72b-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="bd72b-195">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="bd72b-196">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd72b-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="bd72b-197">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="bd72b-198">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="bd72b-199">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="bd72b-200">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="bd72b-201">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bd72b-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="bd72b-202">ถ้าผู้ใช้ไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด งานจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="bd72b-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="bd72b-203">งานที่เกินกำหนดอาจถูกเลื่อนระดับตามตัวเลือกที่คุณเลือกในพื้นที่ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="bd72b-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="bd72b-204">การระบุสิ่งที่จะเกิดขึ้นเมื่องานเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="bd72b-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="bd72b-205">ถ้าผู้ใช้ไม่ทำงานที่กำหนดด้วยตนเองให้เสร็จสมบูรณ์ในเวลาที่กำหนด งานจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="bd72b-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="bd72b-206">งานที่เกินกำหนดอาจถูกเลื่อนระดับหรือถูกกำหนดให้กับผู้ใช้รายอื่นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bd72b-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="bd72b-207">ทำตามขั้นตอนเหล่านี้เพื่อเลื่อนระดับงานถ้าเกินกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="bd72b-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="bd72b-208">ในบานหน้าต่างทางซ้าย ให้คลิก **การเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="bd72b-209">เลือกกล่องกาเครื่องหมาย **ใช้พาธการเลื่อนระดับ** เพื่อสร้างพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="bd72b-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="bd72b-210">ระบบจะกำหนดงานให้กับผู้ใช้ที่อยู่ในพาธการเลื่อนระดับโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bd72b-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="bd72b-211">ตัวอย่างเช่น ตารางต่อไปนี้แสดงพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="bd72b-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="bd72b-212">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="bd72b-212">Sequence</span></span> | <span data-ttu-id="bd72b-213">พาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="bd72b-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="bd72b-214">1</span><span class="sxs-lookup"><span data-stu-id="bd72b-214">1</span></span>        | <span data-ttu-id="bd72b-215">กำหนดให้กับ: Donna</span><span class="sxs-lookup"><span data-stu-id="bd72b-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="bd72b-216">2</span><span class="sxs-lookup"><span data-stu-id="bd72b-216">2</span></span>        | <span data-ttu-id="bd72b-217">กำหนดให้กับ: Erin</span><span class="sxs-lookup"><span data-stu-id="bd72b-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="bd72b-218">3</span><span class="sxs-lookup"><span data-stu-id="bd72b-218">3</span></span>        | <span data-ttu-id="bd72b-219">การดำเนินการขั้นสุดท้าย: ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="bd72b-219">Final action: Reject</span></span> |

    <span data-ttu-id="bd72b-220">ในตัวอย่างนี้ ระบบจะกำหนดงานที่เกินกำหนดให้กับ Donna</span><span class="sxs-lookup"><span data-stu-id="bd72b-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="bd72b-221">ถ้า Donna ไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด ระบบจะกำหนดงานให้กับ Erin</span><span class="sxs-lookup"><span data-stu-id="bd72b-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="bd72b-222">หาก Erin ไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด ระบบจะปฏิเสธเอกสารที่ส่งสำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="bd72b-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="bd72b-223">เมื่อต้องการเพิ่มผู้ใช้ในพาธการเลื่อนระดับ คลิก **เพิ่มการเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="bd72b-224">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 4</span><span class="sxs-lookup"><span data-stu-id="bd72b-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="bd72b-225">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bd72b-225">Option</span></span></th>
    <th><span data-ttu-id="bd72b-226">ผู้ใช้ที่ได้รับการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="bd72b-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="bd72b-227">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bd72b-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="bd72b-228">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="bd72b-229">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bd72b-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-230">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะเลื่อนระดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="bd72b-231">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="bd72b-232">ชื่อเหล่านี้คือผู้ใช้ที่สามารถเลื่อนระดับงานได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="bd72b-233">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="bd72b-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="bd72b-234">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="bd72b-235">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="bd72b-236">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="bd72b-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="bd72b-237">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรเลื่อนระดับให้กับผู้ใช้ใดในช่วงงาน:</span><span class="sxs-lookup"><span data-stu-id="bd72b-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="bd72b-238"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– งานถูกเลื่อนระดับให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="bd72b-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="bd72b-239"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> งานถูกเลื่อนระดับให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="bd72b-240"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – งานไม่ถูกเลื่อนระดับให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bd72b-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="bd72b-241">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bd72b-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-242">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-242">Workflow user</span></span></td>
    <td><span data-ttu-id="bd72b-243">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bd72b-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="bd72b-244">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-245">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-245">User</span></span></td>
    <td><span data-ttu-id="bd72b-246">ผู้ใช้ Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bd72b-246">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-247">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="bd72b-248"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bd72b-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="bd72b-249">เลือกผู้ใช้ที่จะเลื่อนระดับงาน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="bd72b-250">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="bd72b-251">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-251">Select one of the following options:</span></span>

    - <span data-ttu-id="bd72b-252">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="bd72b-253">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd72b-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="bd72b-254">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="bd72b-255">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd72b-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="bd72b-256">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="bd72b-257">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="bd72b-258">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="bd72b-259">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="bd72b-260">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bd72b-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="bd72b-261">ทำซ้ำขั้นตอนที่ 3 ถึง 4 สำหรับแต่ละผู้ใช้ที่ควรจะเพิ่มในพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="bd72b-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="bd72b-262">คุณสามารถเปลี่ยนลำดับของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="bd72b-263">ถ้าผู้ใช้ในพาธการเลื่อนระดับไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด ระบบจะดำเนินการกับงานเอง</span><span class="sxs-lookup"><span data-stu-id="bd72b-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="bd72b-264">เมื่อต้องการระบุการดำเนินการที่ระบบจะทำ เลือกแถว **การดำเนินการ** จากนั้น บนแท็บ **สิ้นสุดการดำเนินการ** เลือกการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="bd72b-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="bd72b-265">ระบุเวลาที่จะให้ระบบดำเนินงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bd72b-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="bd72b-266">คุณสามารถตั้งค่าคอนฟิกระบบเพื่อดำเนินการกับงานที่กำหนดด้วยตนเองเมื่อตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bd72b-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="bd72b-267">ตัวอย่างเช่น งานถูกกำหนดให้ต้องได้รับการตรวจทานการรับสินค้าที่ส่งมาพร้อมกับรายงานค่าใช้จ่ายจากสมาชิกของแผนกรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="bd72b-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="bd72b-268">ตามนโยบายของบริษัท งานนี้ต้องถูกดำเนินการถ้ายอดรวมของรายงานค่าใช้จ่ายมีมากกว่า 100 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="bd72b-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="bd72b-269">ในสถานการณ์นี้ คุณสามารถตั้งค่าคอนฟิกระบบเพื่อทำเครื่องหมายงานเป็น **เสร็จสมบูรณ์** โดยอัตโนมัติเมื่อยอดเงินรวมน้อยกว่า 100 ได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="bd72b-270">ทำตามขั้นตอนเหล่านี้เพื่อระบุเวลาที่จะให้ระบบดำเนินการกับงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bd72b-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="bd72b-271">ในบานหน้าต่างทางซ้าย ให้คลิก **การดำเนินการโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="bd72b-272">เลือกกล่องกาเครื่องหมาย **เปิดใช้งานการดำเนินการโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="bd72b-273">คลิก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="bd72b-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="bd72b-274">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bd72b-274">Enter a condition.</span></span>
5. <span data-ttu-id="bd72b-275">ป้อนเงื่อนไขเพิ่มเติมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bd72b-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="bd72b-276">หากต้องการตรวจสอบว่าเงื่อนไขที่คุณป้อนเข้าไปตั้งค่าคอนฟิกไว้ถูกต้องหรือไม่ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="bd72b-277">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-277">Click **Test**.</span></span>
    2. <span data-ttu-id="bd72b-278">ในหน้า **ทดสอบเงื่อนไขลำดับงาน** ในพื้นที่ **ตรวจสอบความถูกต้องของเงื่อนไข** เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="bd72b-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="bd72b-279">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-279">Click **Test**.</span></span> <span data-ttu-id="bd72b-280">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณกำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd72b-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="bd72b-281">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่หน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="bd72b-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="bd72b-282">ในรายการ **การดำเนินการให้สมบูรณ์โดยอัตโนมัติ** เลือกการดำเนินการที่ระบบควรใช้กับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="bd72b-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="bd72b-283">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="bd72b-283">Specify when notifications are sent</span></span>

<span data-ttu-id="bd72b-284">คุณสามารถส่งการแจ้งเตือนไปยังบุคคลต่างๆ เมื่องานที่กำหนดด้วยตนเองมีการมอบหมาย มีการเลื่อนระดับ เสร็จสมบูรณ์หรือถูกปฏิเสธ หรือเมื่อมีการร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="bd72b-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="bd72b-285">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะส่งการแจ้งเตือนเมื่อใดและจะส่งให้ใคร</span><span class="sxs-lookup"><span data-stu-id="bd72b-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="bd72b-286">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="bd72b-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="bd72b-287">เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเหตุการณ์ที่ควรส่งการแจ้งเตือนสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="bd72b-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="bd72b-288">**มอบหมาย** – มีการกำหนดภารกิจนี้ให้กับผู้ใช้รายอื่นแล้ว</span><span class="sxs-lookup"><span data-stu-id="bd72b-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="bd72b-289">**เลื่อนระดับ**– ผู้ใช้ที่กำหนดไม่ได้ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="bd72b-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="bd72b-290">**เสร็จสมบูรณ์**– ผู้ใช้ที่กำหนดได้ทำงานให้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="bd72b-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="bd72b-291">**ปฏิเสธ**– ผู้ใช้ที่กำหนดได้ปฏิเสธเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="bd72b-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="bd72b-292">**ร้องขอการเปลี่ยนแปลง**– ผู้ใช้ที่กำหนดได้ร้องขอการเปลี่ยนแปลงเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="bd72b-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="bd72b-293">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="bd72b-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="bd72b-294">ในแท็บ **ข้อความแจ้งเตือน** ในกล่องข้อความ ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="bd72b-295">เมื่อต้องการปรับแต่งการแจ้งเตือน คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="bd72b-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="bd72b-296">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงการแจ้งเตือนแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="bd72b-297">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="bd72b-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="bd72b-298">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="bd72b-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="bd72b-299">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="bd72b-300">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="bd72b-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="bd72b-301">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="bd72b-301">Click **Insert**.</span></span>

6. <span data-ttu-id="bd72b-302">เมื่อต้องการเพิ่มคำแปลของการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="bd72b-303">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="bd72b-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="bd72b-304">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bd72b-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="bd72b-305">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd72b-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="bd72b-306">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd72b-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="bd72b-307">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="bd72b-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="bd72b-308">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bd72b-308">Click **Close**.</span></span>

7. <span data-ttu-id="bd72b-309">ในแท็บ **ผู้รับ** ระบุผู้ที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="bd72b-310">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="bd72b-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="bd72b-311">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bd72b-311">Option</span></span></th>
    <th><span data-ttu-id="bd72b-312">ผู้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="bd72b-313">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bd72b-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="bd72b-314">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="bd72b-314">Participant</span></span></td>
    <td><span data-ttu-id="bd72b-315">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="bd72b-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-316">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="bd72b-317">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-318">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-318">Workflow user</span></span></td>
    <td><span data-ttu-id="bd72b-319">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bd72b-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="bd72b-320">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="bd72b-321">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-321">User</span></span></td>
    <td><span data-ttu-id="bd72b-322">ผู้ใช้ Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bd72b-322">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="bd72b-323">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="bd72b-324"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bd72b-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="bd72b-325">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="bd72b-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="bd72b-326">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="bd72b-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="bd72b-327">การกำหนดขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="bd72b-327">Set a time limit</span></span>

<span data-ttu-id="bd72b-328">ทำตามขั้นตอนเหล่านี้ถ้าต้องทำงานที่กำหนดด้วยตนเองให้เสร็จสมบูรณ์ในเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bd72b-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="bd72b-329">ตัวเลือกที่คุณเลือกในกระบวนงานนี้จะแทนที่ตัวเลือกที่คุณเลือกไว้ในพื้นที่ **การกำหนด** และ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="bd72b-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="bd72b-330">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="bd72b-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="bd72b-331">เลือกกล่องกาเครื่องหมาย **ตั้งค่าขีดจำกัดเวลาสำหรับองค์ประกอบลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="bd72b-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="bd72b-332">ในฟิลด์ **ระยะเวลา** ระบุเวลาที่ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="bd72b-333">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bd72b-333">Select one of the following options:</span></span>

    - <span data-ttu-id="bd72b-334">**ชั่วโมง** – ป้อนจำนวนชั่วโมงที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="bd72b-335">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd72b-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="bd72b-336">**วัน**– ป้อนจำนวนวันที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="bd72b-337">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd72b-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="bd72b-338">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="bd72b-339">**เดือน**– เลือกวันและสัปดาห์ที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="bd72b-340">ตัวอย่างเช่น คุณอาจต้องการให้งานเสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="bd72b-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="bd72b-341">**ปี**– เลือกวัน สัปดาห์และเดือนที่งานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bd72b-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="bd72b-342">ตัวอย่างเช่น คุณอาจต้องการให้งานเสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bd72b-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="bd72b-343">ระบบจะดำเนินการกับงานโดยอัตโนมัติหากเกินขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="bd72b-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="bd72b-344">ในรายการ **การดำเนินการ** เลือกการดำเนินการที่ระบบควรใช้</span><span class="sxs-lookup"><span data-stu-id="bd72b-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="bd72b-345">ระบุการดำเนินการที่ผู้ใช้ใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="bd72b-346">เมื่อมีกำหนดงานที่กำหนดด้วยตนเองให้กับผู้ใช้ ผู้ใช้จะต้องดำเนินการกับงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="bd72b-347">ทำตามขั้นตอนเหล่านี้เพื่อระบุการดำเนินการที่ผู้ใช้สามารถใช้กับงานได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="bd72b-348">การดำเนินการที่พร้อมใช้งานจะแตกต่างกันไป โดยขึ้นอยู่กับการออกแบบของงาน</span><span class="sxs-lookup"><span data-stu-id="bd72b-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="bd72b-349">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="bd72b-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="bd72b-350">เลือกกล่องกาเครื่องหมาย **เสร็จสมบูรณ์** หากผู้ใช้ควรสามารถทำเครื่องหมายงานนี้ว่า **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="bd72b-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="bd72b-351">เลือกกล่องกาเครื่องหมาย **ปฏิเสธ** หากผู้ใช้ควรสามารถปฏิเสธเอกสารที่ส่งได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="bd72b-352">เลือกกล่องกาเครื่องหมาย **ร้องขอการเปลี่ยนแปลง** หากผู้ใช้ควรสามารถร้องขอทำการเปลี่ยนแปลงเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="bd72b-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="bd72b-353">เลือกกล่องกาเครื่องหมาย **มอบหมาย** หากผู้ใช้ควรสามารถกำหนดงานนี้ให้ผู้ใช้รายอื่นได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="bd72b-354">เลือกกล่องกาเครื่องหมาย **กำหนดใหม่** หากผู้ใช้ควรสามารถกำหนดงานนี้ใหม่ให้ผู้ใช้รายอื่นในคิวรายการงานได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="bd72b-355">เลือกกล่องกาเครื่องหมาย **นำออกใช้** หากผู้ใช้ควรสามารถกำหนดงานนี้ใหม่ในคิวรายการงานได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="bd72b-356">จากนั้นผู้ใช้รายอื่นจึงจะสามารถทำงานให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="bd72b-356">Another user can then complete the task.</span></span>
