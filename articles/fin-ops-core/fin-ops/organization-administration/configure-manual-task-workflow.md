---
title: ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของงานที่กำหนดด้วยตนเอง
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 109c047a35154f6d4c0ebcd71e1c72990d0f4971
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693389"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="84f52-103">ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84f52-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84f52-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="84f52-105">หากต้องการตั้งค่าคอนฟิกงานที่กำหนดด้วยตนเองในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่งานนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="84f52-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="84f52-106">แล้วใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84f52-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="84f52-107">การตั้งชื่องาน</span><span class="sxs-lookup"><span data-stu-id="84f52-107">Name the task</span></span>

<span data-ttu-id="84f52-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับงานที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84f52-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="84f52-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="84f52-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="84f52-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="84f52-111">การป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="84f52-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="84f52-112">คุณต้องระบุบรรทัดชื่อเรื่องและคำแนะนำให้กับผู้ใช้ที่กำหนดงานนี้ให้</span><span class="sxs-lookup"><span data-stu-id="84f52-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="84f52-113">ตัวอย่างเช่น ถ้าคุณกำลังตั้งค่าคอนฟิกงานสำหรับใบขอซื้อ ผู้ใช้ที่กำหนดให้กับงานจะเห็นบรรทัดชื่อเรื่องและคำแนะนำในหน้า **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="84f52-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="84f52-114">บรรทัดชื่อเรื่องจะปรากฏขึ้นในแถบข้อความบนหน้า</span><span class="sxs-lookup"><span data-stu-id="84f52-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="84f52-115">จากนั้นผู้ใช้สามารถคลิกไอคอนในแถบข้อความเพื่อดูคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="84f52-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="84f52-116">ทำตามขั้นตอนเหล่านี้เพื่อป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="84f52-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="84f52-117">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="84f52-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="84f52-118">ในฟิลด์ **ชื่อเรื่องรายการงาน** ป้อนบรรทัดชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="84f52-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="84f52-119">เมื่อต้องการปรับแต่งบรรทัดชื่อเรื่อง คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="84f52-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="84f52-120">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงบรรทัดชื่อเรื่องแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="84f52-121">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="84f52-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="84f52-122">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="84f52-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="84f52-123">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="84f52-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="84f52-124">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="84f52-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="84f52-125">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="84f52-125">Click **Insert**.</span></span>

4. <span data-ttu-id="84f52-126">เมื่อต้องการเพิ่มคำแปลของบรรทัดชื่อเรื่อง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="84f52-127">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="84f52-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="84f52-128">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="84f52-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="84f52-129">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="84f52-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="84f52-130">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="84f52-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="84f52-131">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="84f52-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="84f52-132">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="84f52-132">Click **Close**.</span></span>

5. <span data-ttu-id="84f52-133">ในฟิลด์ **คำแนะนำรายการงาน** ป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="84f52-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="84f52-134">เมื่อต้องการปรับแต่งคำแนะนำ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="84f52-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="84f52-135">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงคำสั่งแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="84f52-136">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="84f52-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="84f52-137">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="84f52-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="84f52-138">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="84f52-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="84f52-139">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="84f52-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="84f52-140">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="84f52-140">Click **Insert**.</span></span>

7. <span data-ttu-id="84f52-141">เมื่อต้องการเพิ่มคำแปลของคำแนะนำ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="84f52-142">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="84f52-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="84f52-143">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="84f52-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="84f52-144">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="84f52-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="84f52-145">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="84f52-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="84f52-146">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 6</span><span class="sxs-lookup"><span data-stu-id="84f52-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="84f52-147">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="84f52-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="84f52-148">การกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-148">Assign the task</span></span>

<span data-ttu-id="84f52-149">ทำตามขั้นตอนเหล่านี้เพื่อระบุผู้ที่ควรกำหนดงานที่กำหนดด้วยตนเองให้</span><span class="sxs-lookup"><span data-stu-id="84f52-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="84f52-150">ในบานหน้าต่างทางซ้าย ให้คลิก **การกำหนด**</span><span class="sxs-lookup"><span data-stu-id="84f52-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="84f52-151">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="84f52-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="84f52-152">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="84f52-152">Option</span></span></th>
    <th><span data-ttu-id="84f52-153">ผู้ใช้ที่ได้รับการกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="84f52-154">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="84f52-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="84f52-155">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="84f52-155">Participant</span></span></td>
    <td><span data-ttu-id="84f52-156">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="84f52-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-157">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="84f52-158">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-159">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="84f52-160">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84f52-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-161">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะกำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="84f52-162">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="84f52-163">ชื่อเหล่านี้คือผู้ใช้ที่สามารถกำหนดงานได้</span><span class="sxs-lookup"><span data-stu-id="84f52-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="84f52-164">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="84f52-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="84f52-165">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="84f52-166">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="84f52-167">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="84f52-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="84f52-168">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรกำหนดให้กับผู้ใช้ใดในช่วงงาน:</span><span class="sxs-lookup"><span data-stu-id="84f52-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="84f52-169"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– งานถูกกำหนดให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="84f52-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="84f52-170"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> งานถูกกำหนดให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="84f52-171"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – งานไม่ถูกกำหนดให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="84f52-172">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="84f52-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-173">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-173">Workflow user</span></span></td>
    <td><span data-ttu-id="84f52-174">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="84f52-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="84f52-175">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-176">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-176">User</span></span></td>
    <td><span data-ttu-id="84f52-177">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-178">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="84f52-179">ผู้ใช้ <strong> ที่พร้อมใช้งานรายการ </strong> รวมผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84f52-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="84f52-180">เลือกผู้ใช้ที่จะกำหนดงาน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-181">คิว</span><span class="sxs-lookup"><span data-stu-id="84f52-181">Queue</span></span></td>
    <td><span data-ttu-id="84f52-182">คิวรายการงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-183">หลังจากที่คุณเลือก <strong>คิว</strong>คลิกที่แท็บ <strong>ตามคิว</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="84f52-184">เมื่อต้องการกำหนดงานในคิวเฉพาะ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="84f52-185">ในรายการ <strong>ชนิดของคิว</strong> เลือก <strong>คิวรายการงาน</strong>.</span><span class="sxs-lookup"><span data-stu-id="84f52-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="84f52-186">ในรายการ <strong>ชื่อคิว</strong> เลือกคิว</span><span class="sxs-lookup"><span data-stu-id="84f52-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="84f52-187">ถ้าเงื่อนไขที่ระบุควรกำหนดคิวที่กำหนดงานให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="84f52-188">ในรายการ <strong>ชนิดของคิว</strong> เลือก <strong>คิวรายการงานแบบมีเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="84f52-189">ในรายการ <strong>ชื่อคิว</strong> เลือก <strong>คิวแบบมีเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="84f52-190">ตัวเลือกนี้จะใช้สำหรับลำดับงานเพียงไม่กี่รายการ เช่น การจัดการกรณี</span><span class="sxs-lookup"><span data-stu-id="84f52-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="84f52-191">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="84f52-192">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-192">Select one of the following options:</span></span>

    - <span data-ttu-id="84f52-193">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="84f52-194">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="84f52-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84f52-195">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="84f52-196">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="84f52-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84f52-197">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="84f52-198">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="84f52-199">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="84f52-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="84f52-200">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="84f52-201">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="84f52-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="84f52-202">ถ้าผู้ใช้ไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด งานจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="84f52-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="84f52-203">งานที่เกินกำหนดอาจถูกเลื่อนระดับตามตัวเลือกที่คุณเลือกในพื้นที่ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="84f52-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="84f52-204">การระบุสิ่งที่จะเกิดขึ้นเมื่องานเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="84f52-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="84f52-205">ถ้าผู้ใช้ไม่ทำงานที่กำหนดด้วยตนเองให้เสร็จสมบูรณ์ในเวลาที่กำหนด งานจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="84f52-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="84f52-206">งานที่เกินกำหนดอาจถูกเลื่อนระดับหรือถูกกำหนดให้กับผู้ใช้รายอื่นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84f52-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="84f52-207">ทำตามขั้นตอนเหล่านี้เพื่อเลื่อนระดับงานถ้าเกินกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="84f52-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="84f52-208">ในบานหน้าต่างทางซ้าย ให้คลิก **การเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="84f52-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="84f52-209">เลือกกล่องกาเครื่องหมาย **ใช้พาธการเลื่อนระดับ** เพื่อสร้างพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="84f52-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="84f52-210">ระบบจะกำหนดงานให้กับผู้ใช้ที่อยู่ในพาธการเลื่อนระดับโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84f52-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="84f52-211">ตัวอย่างเช่น ตารางต่อไปนี้แสดงพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="84f52-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="84f52-212">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="84f52-212">Sequence</span></span> | <span data-ttu-id="84f52-213">พาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="84f52-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="84f52-214">1</span><span class="sxs-lookup"><span data-stu-id="84f52-214">1</span></span>        | <span data-ttu-id="84f52-215">กำหนดให้กับ: Donna</span><span class="sxs-lookup"><span data-stu-id="84f52-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="84f52-216">2</span><span class="sxs-lookup"><span data-stu-id="84f52-216">2</span></span>        | <span data-ttu-id="84f52-217">กำหนดให้กับ: Erin</span><span class="sxs-lookup"><span data-stu-id="84f52-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="84f52-218">3</span><span class="sxs-lookup"><span data-stu-id="84f52-218">3</span></span>        | <span data-ttu-id="84f52-219">การดำเนินการขั้นสุดท้าย: ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="84f52-219">Final action: Reject</span></span> |

    <span data-ttu-id="84f52-220">ในตัวอย่างนี้ ระบบจะกำหนดงานที่เกินกำหนดให้กับ Donna</span><span class="sxs-lookup"><span data-stu-id="84f52-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="84f52-221">ถ้า Donna ไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด ระบบจะกำหนดงานให้กับ Erin</span><span class="sxs-lookup"><span data-stu-id="84f52-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="84f52-222">หาก Erin ไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด ระบบจะปฏิเสธเอกสารที่ส่งสำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="84f52-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="84f52-223">เมื่อต้องการเพิ่มผู้ใช้ในพาธการเลื่อนระดับ คลิก **เพิ่มการเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="84f52-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="84f52-224">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 4</span><span class="sxs-lookup"><span data-stu-id="84f52-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="84f52-225">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="84f52-225">Option</span></span></th>
    <th><span data-ttu-id="84f52-226">ผู้ใช้ที่ได้รับการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="84f52-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="84f52-227">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="84f52-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="84f52-228">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="84f52-229">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="84f52-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-230">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะเลื่อนระดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="84f52-231">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="84f52-232">ชื่อเหล่านี้คือผู้ใช้ที่สามารถเลื่อนระดับงานได้</span><span class="sxs-lookup"><span data-stu-id="84f52-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="84f52-233">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="84f52-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="84f52-234">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="84f52-235">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="84f52-236">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="84f52-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="84f52-237">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรเลื่อนระดับให้กับผู้ใช้ใดในช่วงงาน:</span><span class="sxs-lookup"><span data-stu-id="84f52-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="84f52-238"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– งานถูกเลื่อนระดับให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="84f52-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="84f52-239"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> งานถูกเลื่อนระดับให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="84f52-240"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – งานไม่ถูกเลื่อนระดับให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="84f52-241">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="84f52-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-242">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-242">Workflow user</span></span></td>
    <td><span data-ttu-id="84f52-243">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="84f52-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="84f52-244">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-245">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-245">User</span></span></td>
    <td><span data-ttu-id="84f52-246">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-247">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="84f52-248">ผู้ใช้ <strong> ที่พร้อมใช้งานรายการ </strong> รวมผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84f52-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="84f52-249">เลือกผู้ใช้ที่จะเลื่อนระดับงาน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="84f52-250">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="84f52-251">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-251">Select one of the following options:</span></span>

    - <span data-ttu-id="84f52-252">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="84f52-253">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="84f52-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84f52-254">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="84f52-255">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="84f52-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84f52-256">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="84f52-257">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="84f52-258">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="84f52-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="84f52-259">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องใช้ในการทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="84f52-260">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ทำงานให้เสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="84f52-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="84f52-261">ทำซ้ำขั้นตอนที่ 3 ถึง 4 สำหรับแต่ละผู้ใช้ที่ควรจะเพิ่มในพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="84f52-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="84f52-262">คุณสามารถเปลี่ยนลำดับของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="84f52-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="84f52-263">ถ้าผู้ใช้ในพาธการเลื่อนระดับไม่ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนด ระบบจะดำเนินการกับงานเอง</span><span class="sxs-lookup"><span data-stu-id="84f52-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="84f52-264">เมื่อต้องการระบุการดำเนินการที่ระบบจะทำ เลือกแถว **การดำเนินการ** จากนั้น บนแท็บ **สิ้นสุดการดำเนินการ** เลือกการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="84f52-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="84f52-265">ระบุเวลาที่จะให้ระบบดำเนินงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="84f52-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="84f52-266">คุณสามารถตั้งค่าคอนฟิกระบบเพื่อดำเนินการกับงานที่กำหนดด้วยตนเองเมื่อตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="84f52-267">ตัวอย่างเช่น งานถูกกำหนดให้ต้องได้รับการตรวจทานการรับสินค้าที่ส่งมาพร้อมกับรายงานค่าใช้จ่ายจากสมาชิกของแผนกรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="84f52-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="84f52-268">ตามนโยบายของบริษัท งานนี้ต้องถูกดำเนินการถ้ายอดรวมของรายงานค่าใช้จ่ายมีมากกว่า 100 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="84f52-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="84f52-269">ในสถานการณ์นี้ คุณสามารถตั้งค่าคอนฟิกระบบเพื่อทำเครื่องหมายงานเป็น **เสร็จสมบูรณ์** โดยอัตโนมัติเมื่อยอดเงินรวมน้อยกว่า 100 ได้</span><span class="sxs-lookup"><span data-stu-id="84f52-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="84f52-270">ทำตามขั้นตอนเหล่านี้เพื่อระบุเวลาที่จะให้ระบบดำเนินการกับงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="84f52-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="84f52-271">ในบานหน้าต่างทางซ้าย ให้คลิก **การดำเนินการโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="84f52-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="84f52-272">เลือกกล่องกาเครื่องหมาย **เปิดใช้งานการดำเนินการโดยอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="84f52-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="84f52-273">คลิก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="84f52-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="84f52-274">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="84f52-274">Enter a condition.</span></span>
5. <span data-ttu-id="84f52-275">ป้อนเงื่อนไขเพิ่มเติมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="84f52-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="84f52-276">หากต้องการตรวจสอบว่าเงื่อนไขที่คุณป้อนเข้าไปตั้งค่าคอนฟิกไว้ถูกต้องหรือไม่ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="84f52-277">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="84f52-277">Click **Test**.</span></span>
    2. <span data-ttu-id="84f52-278">ในหน้า **ทดสอบเงื่อนไขลำดับงาน** ในพื้นที่ **ตรวจสอบความถูกต้องของเงื่อนไข** เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="84f52-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="84f52-279">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="84f52-279">Click **Test**.</span></span> <span data-ttu-id="84f52-280">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณกำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="84f52-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="84f52-281">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่หน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="84f52-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="84f52-282">ในรายการ **การดำเนินการให้สมบูรณ์โดยอัตโนมัติ** เลือกการดำเนินการที่ระบบควรใช้กับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="84f52-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="84f52-283">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="84f52-283">Specify when notifications are sent</span></span>

<span data-ttu-id="84f52-284">คุณสามารถส่งการแจ้งเตือนไปยังบุคคลต่างๆ เมื่องานที่กำหนดด้วยตนเองมีการมอบหมาย มีการเลื่อนระดับ เสร็จสมบูรณ์หรือถูกปฏิเสธ หรือเมื่อมีการร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="84f52-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="84f52-285">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะส่งการแจ้งเตือนเมื่อใดและจะส่งให้ใคร</span><span class="sxs-lookup"><span data-stu-id="84f52-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="84f52-286">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="84f52-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="84f52-287">เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเหตุการณ์ที่ควรส่งการแจ้งเตือนสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="84f52-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="84f52-288">**มอบหมาย** – มีการกำหนดภารกิจนี้ให้กับผู้ใช้รายอื่นแล้ว</span><span class="sxs-lookup"><span data-stu-id="84f52-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="84f52-289">**เลื่อนระดับ**– ผู้ใช้ที่กำหนดไม่ได้ทำงานให้เสร็จสมบูรณ์ในเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="84f52-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="84f52-290">**เสร็จสมบูรณ์**– ผู้ใช้ที่กำหนดได้ทำงานให้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="84f52-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="84f52-291">**ปฏิเสธ**– ผู้ใช้ที่กำหนดได้ปฏิเสธเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="84f52-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="84f52-292">**ร้องขอการเปลี่ยนแปลง**– ผู้ใช้ที่กำหนดได้ร้องขอการเปลี่ยนแปลงเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="84f52-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="84f52-293">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="84f52-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="84f52-294">ในแท็บ **ข้อความแจ้งเตือน** ในกล่องข้อความ ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="84f52-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="84f52-295">เมื่อต้องการปรับแต่งการแจ้งเตือน คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="84f52-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="84f52-296">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงการแจ้งเตือนแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="84f52-297">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="84f52-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="84f52-298">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="84f52-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="84f52-299">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="84f52-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="84f52-300">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="84f52-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="84f52-301">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="84f52-301">Click **Insert**.</span></span>

6. <span data-ttu-id="84f52-302">เมื่อต้องการเพิ่มคำแปลของการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="84f52-303">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="84f52-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="84f52-304">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="84f52-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="84f52-305">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="84f52-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="84f52-306">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="84f52-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="84f52-307">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="84f52-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="84f52-308">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="84f52-308">Click **Close**.</span></span>

7. <span data-ttu-id="84f52-309">ในแท็บ **ผู้รับ** ระบุผู้ที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="84f52-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="84f52-310">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="84f52-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="84f52-311">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="84f52-311">Option</span></span></th>
    <th><span data-ttu-id="84f52-312">ผู้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="84f52-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="84f52-313">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="84f52-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="84f52-314">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="84f52-314">Participant</span></span></td>
    <td><span data-ttu-id="84f52-315">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="84f52-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-316">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="84f52-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="84f52-317">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="84f52-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-318">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-318">Workflow user</span></span></td>
    <td><span data-ttu-id="84f52-319">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="84f52-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="84f52-320">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="84f52-321">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-321">User</span></span></td>
    <td><span data-ttu-id="84f52-322">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="84f52-323">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="84f52-324">ผู้ใช้ <strong> ที่พร้อมใช้งานรายการ </strong> รวมผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="84f52-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="84f52-325">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="84f52-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="84f52-326">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="84f52-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="84f52-327">การกำหนดขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="84f52-327">Set a time limit</span></span>

<span data-ttu-id="84f52-328">ทำตามขั้นตอนเหล่านี้ถ้าต้องทำงานที่กำหนดด้วยตนเองให้เสร็จสมบูรณ์ในเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="84f52-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="84f52-329">ตัวเลือกที่คุณเลือกในกระบวนงานนี้จะแทนที่ตัวเลือกที่คุณเลือกไว้ในพื้นที่ **การกำหนด** และ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="84f52-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="84f52-330">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="84f52-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="84f52-331">เลือกกล่องกาเครื่องหมาย **ตั้งค่าขีดจำกัดเวลาสำหรับองค์ประกอบลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="84f52-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="84f52-332">ในฟิลด์ **ระยะเวลา** ระบุเวลาที่ต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="84f52-333">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="84f52-333">Select one of the following options:</span></span>

    - <span data-ttu-id="84f52-334">**ชั่วโมง** – ป้อนจำนวนชั่วโมงที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="84f52-335">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="84f52-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84f52-336">**วัน**– ป้อนจำนวนวันที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="84f52-337">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="84f52-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="84f52-338">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="84f52-339">**เดือน**– เลือกวันและสัปดาห์ที่งานต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="84f52-340">ตัวอย่างเช่น คุณอาจต้องการให้งานเสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="84f52-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="84f52-341">**ปี**– เลือกวัน สัปดาห์และเดือนที่งานเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="84f52-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="84f52-342">ตัวอย่างเช่น คุณอาจต้องการให้งานเสร็จสมบูรณ์ภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="84f52-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="84f52-343">ระบบจะดำเนินการกับงานโดยอัตโนมัติหากเกินขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="84f52-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="84f52-344">ในรายการ **การดำเนินการ** เลือกการดำเนินการที่ระบบควรใช้</span><span class="sxs-lookup"><span data-stu-id="84f52-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="84f52-345">ระบุการดำเนินการที่ผู้ใช้ใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="84f52-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="84f52-346">เมื่อมีกำหนดงานที่กำหนดด้วยตนเองให้กับผู้ใช้ ผู้ใช้จะต้องดำเนินการกับงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="84f52-347">ทำตามขั้นตอนเหล่านี้เพื่อระบุการดำเนินการที่ผู้ใช้สามารถใช้กับงานได้</span><span class="sxs-lookup"><span data-stu-id="84f52-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="84f52-348">การดำเนินการที่พร้อมใช้งานจะแตกต่างกันไป โดยขึ้นอยู่กับการออกแบบของงาน</span><span class="sxs-lookup"><span data-stu-id="84f52-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="84f52-349">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="84f52-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="84f52-350">เลือกกล่องกาเครื่องหมาย **เสร็จสมบูรณ์** หากผู้ใช้ควรสามารถทำเครื่องหมายงานนี้ว่า **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="84f52-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="84f52-351">เลือกกล่องกาเครื่องหมาย **ปฏิเสธ** หากผู้ใช้ควรสามารถปฏิเสธเอกสารที่ส่งได้</span><span class="sxs-lookup"><span data-stu-id="84f52-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="84f52-352">เลือกกล่องกาเครื่องหมาย **ร้องขอการเปลี่ยนแปลง** หากผู้ใช้ควรสามารถร้องขอทำการเปลี่ยนแปลงเอกสารที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="84f52-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="84f52-353">เลือกกล่องกาเครื่องหมาย **มอบหมาย** หากผู้ใช้ควรสามารถกำหนดงานนี้ให้ผู้ใช้รายอื่นได้</span><span class="sxs-lookup"><span data-stu-id="84f52-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="84f52-354">เลือกกล่องกาเครื่องหมาย **กำหนดใหม่** หากผู้ใช้ควรสามารถกำหนดงานนี้ใหม่ให้ผู้ใช้รายอื่นในคิวรายการงานได้</span><span class="sxs-lookup"><span data-stu-id="84f52-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="84f52-355">เลือกกล่องกาเครื่องหมาย **นำออกใช้** หากผู้ใช้ควรสามารถกำหนดงานนี้ใหม่ในคิวรายการงานได้</span><span class="sxs-lookup"><span data-stu-id="84f52-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="84f52-356">จากนั้นผู้ใช้รายอื่นจึงจะสามารถทำงานให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="84f52-356">Another user can then complete the task.</span></span>
