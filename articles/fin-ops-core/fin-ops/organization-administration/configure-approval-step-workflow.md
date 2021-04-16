---
title: ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของขั้นตอนการอนุมัติ
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86e8787320721a58f449abcfba21c2c4c6b4caf9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751787"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="3fac5-103">ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3fac5-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fac5-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="3fac5-105">หากต้องการตั้งค่าคอนฟิกขั้นตอนการอนุมัติในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่ขั้นตอนการอนุมัตินั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3fac5-106">แล้วใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="3fac5-107">การตั้งชื่อขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="3fac5-107">Name the step</span></span>
<span data-ttu-id="3fac5-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="3fac5-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="3fac5-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3fac5-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="3fac5-111">การป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="3fac5-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="3fac5-112">คุณต้องระบุบรรทัดชื่อเรื่องและคำแนะนำให้กับผู้ใช้ที่กำหนดไว้ในขั้นตอนการอนุมัตินี้</span><span class="sxs-lookup"><span data-stu-id="3fac5-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="3fac5-113">ตัวอย่างเช่น ถ้าคุณกำลังตั้งค่าคอนฟิกขั้นตอนการอนุมัติสำหรับใบขอซื้อ ผู้ใช้ที่กำหนดให้กับขั้นตอนจะเห็นบรรทัดชื่อเรื่องและคำแนะนำในหน้า **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="3fac5-114">บรรทัดชื่อเรื่องจะปรากฏขึ้นในแถบข้อความบนหน้า</span><span class="sxs-lookup"><span data-stu-id="3fac5-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="3fac5-115">จากนั้นผู้ใช้สามารถคลิกไอคอนในแถบข้อความเพื่อดูคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="3fac5-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="3fac5-116">ทำตามขั้นตอนเหล่านี้เพื่อป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="3fac5-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="3fac5-117">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="3fac5-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3fac5-118">ในฟิลด์ **ชื่อเรื่องรายการงาน** ป้อนบรรทัดชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="3fac5-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="3fac5-119">เมื่อต้องการปรับแต่งบรรทัดชื่อเรื่อง คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="3fac5-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="3fac5-120">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงบรรทัดชื่อเรื่องแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3fac5-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="3fac5-121">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="3fac5-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3fac5-122">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="3fac5-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3fac5-123">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="3fac5-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3fac5-124">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="3fac5-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3fac5-125">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="3fac5-125">Click **Insert**.</span></span>

4. <span data-ttu-id="3fac5-126">เมื่อต้องการเพิ่มคำแปลของบรรทัดชื่อเรื่อง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3fac5-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="3fac5-127">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="3fac5-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="3fac5-128">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3fac5-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3fac5-129">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="3fac5-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3fac5-130">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="3fac5-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3fac5-131">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="3fac5-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="3fac5-132">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="3fac5-132">Click **Close**.</span></span>

5. <span data-ttu-id="3fac5-133">ในฟิลด์ **คำแนะนำรายการงาน** ป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="3fac5-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="3fac5-134">เมื่อต้องการปรับแต่งคำแนะนำ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="3fac5-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="3fac5-135">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงคำสั่งแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3fac5-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="3fac5-136">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="3fac5-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3fac5-137">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="3fac5-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3fac5-138">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="3fac5-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3fac5-139">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="3fac5-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3fac5-140">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="3fac5-140">Click **Insert**.</span></span>

7. <span data-ttu-id="3fac5-141">เมื่อต้องการเพิ่มคำแปลของคำแนะนำ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3fac5-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="3fac5-142">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="3fac5-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="3fac5-143">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3fac5-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3fac5-144">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="3fac5-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3fac5-145">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="3fac5-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3fac5-146">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 6</span><span class="sxs-lookup"><span data-stu-id="3fac5-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="3fac5-147">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="3fac5-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="3fac5-148">การกำหนดขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-148">Assign the approval step</span></span>

<span data-ttu-id="3fac5-149">ทำตามขั้นตอนเหล่านี้เพื่อระบุผู้ที่ควรกำหนดขั้นตอนการอนุมัติให้</span><span class="sxs-lookup"><span data-stu-id="3fac5-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="3fac5-150">ในบานหน้าต่างทางซ้าย ให้คลิก **การกำหนด**</span><span class="sxs-lookup"><span data-stu-id="3fac5-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="3fac5-151">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="3fac5-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3fac5-152">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3fac5-152">Option</span></span></th>
    <th><span data-ttu-id="3fac5-153">ผู้ใช้ที่ได้รับการกำหนดขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="3fac5-154">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3fac5-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3fac5-155">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="3fac5-155">Participant</span></span></td>
    <td><span data-ttu-id="3fac5-156">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="3fac5-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3fac5-157">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะกำหนดขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="3fac5-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="3fac5-158">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะกำหนดขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="3fac5-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3fac5-159">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="3fac5-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="3fac5-160">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3fac5-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3fac5-161">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะกำหนดขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="3fac5-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="3fac5-162">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="3fac5-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="3fac5-163">ชื่อเหล่านี้คือผู้ใช้ที่สามารถกำหนดขั้นตอนได้</span><span class="sxs-lookup"><span data-stu-id="3fac5-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="3fac5-164">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="3fac5-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="3fac5-165">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="3fac5-166">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="3fac5-167">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="3fac5-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3fac5-168">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรกำหนดให้กับผู้ใช้ใดในช่วงขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="3fac5-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="3fac5-169"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– ขั้นตอนถูกกำหนดให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="3fac5-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="3fac5-170"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> ขั้นตอนถูกกำหนดให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fac5-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="3fac5-171"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – ขั้นตอนไม่ถูกกำหนดให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3fac5-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="3fac5-172">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="3fac5-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3fac5-173">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3fac5-173">Workflow user</span></span></td>
    <td><span data-ttu-id="3fac5-174">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3fac5-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3fac5-175">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3fac5-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3fac5-176">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3fac5-176">User</span></span></td>
    <td><span data-ttu-id="3fac5-177">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3fac5-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3fac5-178">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3fac5-179">ผู้ใช้ <strong> ที่พร้อมใช้งานรายการ </strong> จะมีผู้ใช้ระบบทุกคน</span><span class="sxs-lookup"><span data-stu-id="3fac5-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="3fac5-180">เลือกผู้ใช้ที่จะกำหนดขั้นตอน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="3fac5-181">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องดำเนินการ หรือตอบสนองเอกสารที่มาถึงขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="3fac5-182">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3fac5-182">Select one of the following options:</span></span>

    - <span data-ttu-id="3fac5-183">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="3fac5-184">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fac5-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3fac5-185">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="3fac5-186">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fac5-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3fac5-187">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="3fac5-188">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="3fac5-189">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตอบสนองภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="3fac5-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3fac5-190">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="3fac5-191">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตอบสนองภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="3fac5-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="3fac5-192">ถ้าผู้ใช้ไม่ดำเนินการกับเอกสารในเวลาที่กำหนด เอกสารจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="3fac5-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="3fac5-193">เอกสารที่เกินกำหนดจะถูกเลื่อนระดับตามตัวเลือกที่คุณเลือกในพื้นที่ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="3fac5-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="3fac5-194">ถ้าคุณกำหนดขั้นตอนการอนุมัติให้กับผู้ใช้หรือกลุ่มผู้ใช้หลายราย บนแท็บ **นโยบายฉบับสมบูรณ์** เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3fac5-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="3fac5-195">**ผู้อนุมัติรายเดียว** – การดำเนินการที่ใช้กับเอกสารจะเป็นไปตามบุคคลแรกที่ตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="3fac5-196">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายมูลค่า 15000 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="3fac5-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="3fac5-197">ในขณะนี้รายงานค่าใช้จ่ายถูกกำหนดให้กับ Sue, Jo และ Bill</span><span class="sxs-lookup"><span data-stu-id="3fac5-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="3fac5-198">หาก Sue เป็นบุคคลแรกที่ตอบสนองเอกสารนี้ การดำเนินการของ Sue จะถูกนำไปใช้กับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3fac5-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="3fac5-199">หาก Sue ปฏิเสธเอกสารนี้ เอกสารจะถูกปฏิเสธและส่งกลับไปยัง Sam</span><span class="sxs-lookup"><span data-stu-id="3fac5-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="3fac5-200">ถ้า Sue อนุมัติเอกสาร เอกสารนี้จะถูกส่งให้กับ Ann เพื่อขอการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![ลำดับงานที่มีกระบวนการอนุมัติ](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="3fac5-202">**ผู้อนุมัติส่วนใหญ่** –การดำเนินการที่ใช้กับเอกสารนี้จะเป็นไปตามเสียงตอบสนองส่วนใหญ่ของผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="3fac5-203">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายมูลค่า 15000 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="3fac5-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="3fac5-204">ในขณะนี้รายงานค่าใช้จ่ายถูกกำหนดให้กับ Sue, Jo และ Bill</span><span class="sxs-lookup"><span data-stu-id="3fac5-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="3fac5-205">หาก Sue และ Jo เป็นผู้อนุมัติสองคนแรกที่ตอบสนอง การดำเนินการของทั้งสองคนจะถูกนำไปใช้กับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3fac5-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="3fac5-206">หาก Sue อนุมัติเอกสารนี้แต่ Jo ปฏิเสธ เอกสารจะถูกปฏิเสธและส่งกลับไปยัง Sam</span><span class="sxs-lookup"><span data-stu-id="3fac5-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="3fac5-207">หากทั้ง Sue และ Jo อนุมัติเอกสารนี้ เอกสารจะส่งไปยัง Ann เพื่อทำการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="3fac5-208">**เปอร์เซ็นต์ของผู้อนุมัติ** – การดำเนินการที่ใช้กับเอกสารจะเป็นไปตามเปอร์เซ็นต์เฉพาะของผู้อนุมัติที่ตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="3fac5-209">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายมูลค่า 15000 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="3fac5-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="3fac5-210">ในขณะนี้ รายงานค่าใช้จ่ายถูกมอบหมายให้กับ Sue, Jo และ Bill และคุณได้ป้อนเปอร์เซ็นต์เป็น **50**</span><span class="sxs-lookup"><span data-stu-id="3fac5-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="3fac5-211">หาก Sue และ Jo เป็นผู้อนุมัติสองคนแรกที่ตอบสนอง การดำเนินการของทั้งสองคนจะถูกนำไปใช้กับเอกสาร เนื่องจากพวกเขาตรงตามข้อกำหนดของผู้อนุมัติ 50 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="3fac5-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="3fac5-212">หาก Sue อนุมัติเอกสารนี้แต่ Jo ปฏิเสธ เอกสารจะถูกปฏิเสธและส่งกลับไปยัง Sam</span><span class="sxs-lookup"><span data-stu-id="3fac5-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="3fac5-213">หากทั้ง Sue และ Jo อนุมัติเอกสารนี้ เอกสารจะส่งไปยัง Ann เพื่อทำการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="3fac5-214">**ผู้อนุมัติทั้งหมด**– ผู้อนุมัติทั้งหมดต้องอนุมัติเอกสารนี้</span><span class="sxs-lookup"><span data-stu-id="3fac5-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="3fac5-215">มิฉะนั้น จะไม่สามารถดำเนินลำดับงานต่อได้</span><span class="sxs-lookup"><span data-stu-id="3fac5-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="3fac5-216">ตัวอย่างเช่น Sam ส่งรายงานค่าใช้จ่ายมูลค่า 15000 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="3fac5-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="3fac5-217">ในขณะนี้รายงานค่าใช้จ่ายถูกกำหนดให้กับ Sue, Jo และ Bill</span><span class="sxs-lookup"><span data-stu-id="3fac5-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="3fac5-218">หาก Sue และ Joe อนุมัติเอกสารนี้แต่ Bill ปฏิเสธ เอกสารจะถูกปฏิเสธและส่งกลับไปยัง Sam</span><span class="sxs-lookup"><span data-stu-id="3fac5-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="3fac5-219">หาก Sue, Jo และ Bill อนุมัติเอกสารนี้ เอกสารจะส่งไปยัง Ann เพื่อทำการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="3fac5-220">ระบุว่าขั้นตอนการอนุมัตินี้จำเป็นเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="3fac5-220">Specify when the approval step is required</span></span>

<span data-ttu-id="3fac5-221">คุณสามารถระบุว่าขั้นตอนการอนุมัตินี้จำเป็นเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="3fac5-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="3fac5-222">อาจจำเป็นต้องใช้ขั้นตอนการอนุมัติทุกครั้ง หรืออาจจำเป็นเฉพาะเมื่อเป็นไปตามเงื่อนไขเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3fac5-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="3fac5-223">จำเป็นต้องใช้ขั้นตอนการอนุมัติทุกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3fac5-223">The approval step is always required</span></span>

<span data-ttu-id="3fac5-224">ทำตามขั้นตอนเหล่านี้หากจำเป็นต้องใช้ขั้นตอนการอนุมัติทุกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3fac5-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="3fac5-225">ในบานหน้าต่างทางซ้าย ให้คลิก **เงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="3fac5-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="3fac5-226">เลือกตัวเลือก **รันขั้นตอนนี้ทุกครั้ง**</span><span class="sxs-lookup"><span data-stu-id="3fac5-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="3fac5-227">จำเป็นต้องใช้ขั้นตอนการอนุมัติภายใต้เงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3fac5-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="3fac5-228">ขั้นตอนการอนุมัติที่คุณกำลังตั้งค่าคอนฟิกอาจจำเป็นเฉพาะเมื่อเป็นไปตามเงื่อนไขเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3fac5-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="3fac5-229">ตัวอย่างเช่น ถ้าคุณกำลังตั้งค่าคอนฟิกขั้นตอนการอนุมัติสำหรับลำดับงานใบขอซื้อ คุณอาจต้องการให้ใช้ขั้นตอนการอนุมัติเฉพาะเมื่อถ้ายอดเงินของใบสั่งซื้อมากกว่า 10000 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="3fac5-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="3fac5-230">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าเมื่อใดจึงจำเป็นต้องใช้ขั้นตอนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="3fac5-231">ในบานหน้าต่างทางซ้าย ให้คลิก **เงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="3fac5-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="3fac5-232">เลือกตัวเลือก **รันขั้นตอนนี้เมื่อเป็นไปตามเงื่อนไขต่อไปนี้เท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="3fac5-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="3fac5-233">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="3fac5-233">Enter a condition.</span></span>
4. <span data-ttu-id="3fac5-234">ป้อนเงื่อนไขเพิ่มเติมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3fac5-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="3fac5-235">หากต้องการตรวจสอบว่าเงื่อนไขที่คุณป้อนเข้าไปตั้งค่าคอนฟิกไว้ถูกต้องหรือไม่ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3fac5-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="3fac5-236">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-236">Click **Test**.</span></span>
    2. <span data-ttu-id="3fac5-237">ในหน้า **ทดสอบเงื่อนไขลำดับงาน** ในพื้นที่ **ตรวจสอบความถูกต้องของเงื่อนไข** เลือกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="3fac5-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="3fac5-238">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-238">Click **Test**.</span></span> <span data-ttu-id="3fac5-239">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณกำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fac5-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="3fac5-240">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่หน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="3fac5-241">การระบุสิ่งที่จะเกิดขึ้นเมื่อเอกสารเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="3fac5-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="3fac5-242">ถ้าผู้ใช้ไม่ดำเนินการกับเอกสารในเวลาที่กำหนด เอกสารจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="3fac5-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="3fac5-243">เอกสารที่เกินกำหนดอาจถูกเลื่อนระดับหรือถูกกำหนดให้กับผู้ใช้รายอื่นโดยอัตโนมัติสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="3fac5-244">ทำตามขั้นตอนเหล่านี้เพื่อเลื่อนระดับเอกสารถ้าเกินกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="3fac5-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="3fac5-245">ในบานหน้าต่างทางซ้าย ให้คลิก **การเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="3fac5-246">เลือกกล่องกาเครื่องหมาย **ใช้พาธการเลื่อนระดับ** เพื่อสร้างพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="3fac5-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="3fac5-247">ระบบจะกำหนดเอกสารให้กับผู้ใช้ที่อยู่ในพาธการเลื่อนระดับโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="3fac5-248">ตัวอย่างเช่น ตารางต่อไปนี้แสดงพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="3fac5-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="3fac5-249">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="3fac5-249">Sequence</span></span> | <span data-ttu-id="3fac5-250">พาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="3fac5-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="3fac5-251">1</span><span class="sxs-lookup"><span data-stu-id="3fac5-251">1</span></span>        | <span data-ttu-id="3fac5-252">กำหนดให้กับ: Donna</span><span class="sxs-lookup"><span data-stu-id="3fac5-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="3fac5-253">2</span><span class="sxs-lookup"><span data-stu-id="3fac5-253">2</span></span>        | <span data-ttu-id="3fac5-254">กำหนดให้กับ: Erin</span><span class="sxs-lookup"><span data-stu-id="3fac5-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="3fac5-255">3</span><span class="sxs-lookup"><span data-stu-id="3fac5-255">3</span></span>        | <span data-ttu-id="3fac5-256">การดำเนินการขั้นสุดท้าย: ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="3fac5-256">Final action: Reject</span></span> |

    <span data-ttu-id="3fac5-257">ในตัวอย่างนี้ ระบบจะกำหนดเอกสารที่เกินกำหนดให้กับ Donna</span><span class="sxs-lookup"><span data-stu-id="3fac5-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="3fac5-258">ถ้า Donna ไม่ตอบสนองในเวลาที่กำหนด ระบบจะกำหนดเอกสารให้กับ Erin</span><span class="sxs-lookup"><span data-stu-id="3fac5-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="3fac5-259">ถ้า Erin ไม่ตอบสนองในเวลาที่กำหนด ระบบจะปฏิเสธเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3fac5-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="3fac5-260">เมื่อต้องการเพิ่มผู้ใช้ในพาธการเลื่อนระดับ คลิก **เพิ่มการเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="3fac5-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="3fac5-261">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 4</span><span class="sxs-lookup"><span data-stu-id="3fac5-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3fac5-262">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3fac5-262">Option</span></span></th>
    <th><span data-ttu-id="3fac5-263">ผู้ใช้ที่ได้รับการเลื่อนระดับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3fac5-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="3fac5-264">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3fac5-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3fac5-265">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="3fac5-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="3fac5-266">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3fac5-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3fac5-267">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะเลื่อนระดับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3fac5-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="3fac5-268">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="3fac5-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="3fac5-269">ชื่อเหล่านี้คือผู้ใช้ที่สามารถเลื่อนระดับเอกสารได้</span><span class="sxs-lookup"><span data-stu-id="3fac5-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="3fac5-270">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="3fac5-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="3fac5-271">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="3fac5-272">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="3fac5-273">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="3fac5-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3fac5-274">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรเลื่อนระดับให้กับผู้ใช้ใดในช่วงเอกสาร:</span><span class="sxs-lookup"><span data-stu-id="3fac5-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="3fac5-275"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– เอกสารถูกเลื่อนระดับให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="3fac5-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="3fac5-276"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> เอกสารถูกเลื่อนระดับให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fac5-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="3fac5-277"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – เอกสารไม่ถูกเลื่อนระดับให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3fac5-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="3fac5-278">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="3fac5-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3fac5-279">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3fac5-279">Workflow user</span></span></td>
    <td><span data-ttu-id="3fac5-280">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3fac5-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3fac5-281">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="3fac5-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3fac5-282">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3fac5-282">User</span></span></td>
    <td><span data-ttu-id="3fac5-283">ผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3fac5-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3fac5-284">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3fac5-285">ผู้ใช้ <strong> ที่พร้อมใช้งานรายการ </strong> รวมผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3fac5-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3fac5-286">เลือกผู้ใช้ที่จะเลื่อนระดับเอกสาร จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="3fac5-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="3fac5-287">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องดำเนินการ หรือตอบสนองเอกสาร</span><span class="sxs-lookup"><span data-stu-id="3fac5-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="3fac5-288">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3fac5-288">Select one of the following options:</span></span>

    - <span data-ttu-id="3fac5-289">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="3fac5-290">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fac5-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3fac5-291">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="3fac5-292">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fac5-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3fac5-293">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="3fac5-294">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="3fac5-295">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตอบสนองภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="3fac5-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3fac5-296">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="3fac5-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="3fac5-297">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตอบสนองภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="3fac5-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="3fac5-298">ทำซ้ำขั้นตอนที่ 3 ถึง 4 สำหรับแต่ละผู้ใช้ที่ควรจะเพิ่มในพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="3fac5-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="3fac5-299">คุณสามารถเปลี่ยนลำดับของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="3fac5-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="3fac5-300">ถ้าผู้ใช้ในพาธการเลื่อนระดับไม่ตอบสนองในเวลาที่กำหนด ระบบจะดำเนินการกับเอกสารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3fac5-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="3fac5-301">เมื่อต้องการระบุการดำเนินการที่ระบบจะทำ เลือกแถว **การดำเนินการ** จากนั้น บนแท็บ **สิ้นสุดการดำเนินการ** เลือกการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3fac5-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]