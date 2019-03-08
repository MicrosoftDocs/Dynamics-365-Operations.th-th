---
title: ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของการตัดสินใจด้วยตนเอง
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d09e99a5bf99593a8fa7682f9d4f29eaa4e7c836
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "341407"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="ca14a-103">ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca14a-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณสมบัติต่างๆ ของการตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ca14a-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="ca14a-105">หากต้องการตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่การตัดสินใจด้วยตนเองนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="ca14a-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ca14a-106">แล้วใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับการตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ca14a-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="ca14a-107">กำหนดชื่อการตัดสินใจนั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-107">Name the decision</span></span>

<span data-ttu-id="ca14a-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับการตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ca14a-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="ca14a-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="ca14a-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ca14a-110">ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับการตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ca14a-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="ca14a-111">การป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="ca14a-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="ca14a-112">คุณต้องระบุบรรทัดชื่อเรื่องและคำแนะนำให้กับผู้ใช้ที่กำหนดไว้ในการตัดสินใจด้วยตนเองนี้</span><span class="sxs-lookup"><span data-stu-id="ca14a-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="ca14a-113">ตัวอย่างเช่น ถ้าคุณกำลังตั้งค่าคอนฟิกการตัดสินใจสำหรับใบขอซื้อ ผู้ใช้ที่กำหนดให้กับการตัดสินใจจะเห็นบรรทัดชื่อเรื่องและคำแนะนำในหน้า **ใบขอซื้อ**</span><span class="sxs-lookup"><span data-stu-id="ca14a-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="ca14a-114">บรรทัดชื่อเรื่องจะปรากฏขึ้นในแถบข้อความบนหน้า</span><span class="sxs-lookup"><span data-stu-id="ca14a-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="ca14a-115">จากนั้นผู้ใช้สามารถคลิกไอคอนในแถบข้อความเพื่อดูคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="ca14a-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="ca14a-116">ทำตามขั้นตอนเหล่านี้เพื่อป้อนบรรทัดชื่อเรื่องและคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="ca14a-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="ca14a-117">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="ca14a-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ca14a-118">บนแท็บ **คำแนะนำ** ในฟิลด์ **ชื่อเรื่องรายการงาน** ป้อนบรรทัดชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="ca14a-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="ca14a-119">เมื่อต้องการปรับแต่งบรรทัดชื่อเรื่อง คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca14a-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="ca14a-120">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงบรรทัดชื่อเรื่องแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca14a-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="ca14a-121">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="ca14a-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ca14a-122">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="ca14a-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ca14a-123">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ca14a-124">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="ca14a-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ca14a-125">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="ca14a-125">Click **Insert**.</span></span>

4. <span data-ttu-id="ca14a-126">เมื่อต้องการเพิ่มคำแปลของบรรทัดชื่อเรื่อง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="ca14a-127">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="ca14a-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="ca14a-128">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ca14a-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ca14a-129">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ca14a-130">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ca14a-131">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="ca14a-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="ca14a-132">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-132">Click **Close**.</span></span>

5. <span data-ttu-id="ca14a-133">ในฟิลด์ **คำแนะนำรายการงาน** ป้อนคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="ca14a-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="ca14a-134">เมื่อต้องการปรับแต่งคำแนะนำ คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca14a-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="ca14a-135">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงคำสั่งแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca14a-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="ca14a-136">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="ca14a-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ca14a-137">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="ca14a-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ca14a-138">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ca14a-139">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="ca14a-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ca14a-140">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="ca14a-140">Click **Insert**.</span></span>

7. <span data-ttu-id="ca14a-141">เมื่อต้องการเพิ่มคำแปลของคำแนะนำ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="ca14a-142">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="ca14a-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="ca14a-143">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ca14a-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ca14a-144">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ca14a-145">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ca14a-146">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 6</span><span class="sxs-lookup"><span data-stu-id="ca14a-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="ca14a-147">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="ca14a-148">ระบุผลลัพธ์ที่เป็นไปได้ของการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="ca14a-149">โดยทั่วไป เมื่อเอกสารถูกมอบหมายให้ผู้ตัดสินใจ ผู้ตัดสินใจจะถูกถามคำถาม</span><span class="sxs-lookup"><span data-stu-id="ca14a-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="ca14a-150">คำตอบสำหรับคำถามเป็นคำตอบโดยทั่วไป **ใช่** หรือ **ไม่ใช่**หรือ **จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="ca14a-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="ca14a-151">ทำตามขั้นตอนเหล่านี้เพื่อระบุผลลัพธ์ที่เป็นไปได้ของการตัดสินใจด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ca14a-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="ca14a-152">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="ca14a-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ca14a-153">บนแท็บ **ผลลัพธ์** ในฟิลด์ **ผลลัพธ์ 1** ป้อนชื่อของผลลัพธ์หรือตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="ca14a-154">เมื่อต้องการเพิ่มคำแปลของผลลัพธ์ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="ca14a-155">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="ca14a-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="ca14a-156">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ca14a-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ca14a-157">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ca14a-158">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ca14a-159">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-159">Click **Close**.</span></span>

4. <span data-ttu-id="ca14a-160">ในฟิลด์ **ผลลัพธ์ 2** ป้อนชื่อของผลลัพธ์หรือตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="ca14a-161">เมื่อต้องการเพิ่มคำแปลของผลลัพธ์ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="ca14a-162">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="ca14a-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="ca14a-163">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ca14a-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ca14a-164">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ca14a-165">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ca14a-166">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ca14a-167">ระบุว่าจะส่งการแจ้งเตือนเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="ca14a-167">Specify when notifications are sent</span></span>

<span data-ttu-id="ca14a-168">คุณสามารถส่งการแจ้งเตือนไปยังบุคคลต่าง ๆ เมื่อมีการตัดสินใจ มอบหมาย หรือเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="ca14a-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="ca14a-169">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะส่งการแจ้งเตือนเมื่อใดและจะส่งให้ใคร</span><span class="sxs-lookup"><span data-stu-id="ca14a-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="ca14a-170">ในบานหน้าต่างทางซ้าย ให้คลิก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="ca14a-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="ca14a-171">เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเหตุการณ์ที่ควรส่งการแจ้งเตือนสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="ca14a-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="ca14a-172">**\[ตัวเลือก 1\]** – มีการเลือกผู้ใช้ที่กำหนด **\[ตัวเลือก 1\]**</span><span class="sxs-lookup"><span data-stu-id="ca14a-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="ca14a-173">**\[ตัวเลือก 2\]** – มีการเลือกผู้ใช้ที่กำหนด **\[ตัวเลือก 2\]**</span><span class="sxs-lookup"><span data-stu-id="ca14a-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="ca14a-174">**มอบหมาย**– ผู้ใช้ที่กำหนดได้กำหนดการตัดสินใจให้กับผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="ca14a-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="ca14a-175">**เลื่อนระดับ**– ผู้ใช้ที่กำหนดไม่ได้ทำการตัดสินใจในเวลาที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="ca14a-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="ca14a-176">เลือกแถวของเหตุการณ์ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="ca14a-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="ca14a-177">ในแท็บ **ข้อความแจ้งเตือน** ในกล่องข้อความ ป้อนข้อความการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="ca14a-178">เมื่อต้องการปรับแต่งการแจ้งเตือน คุณสามารถแทรกตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca14a-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="ca14a-179">ตัวยึดจะถูกแทนที่ด้วยข้อมูลที่เหมาะสมเมื่อมีการแสดงการแจ้งเตือนแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca14a-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="ca14a-180">ทำตามขั้นตอนเหล่านี้เพื่อแทรกตัวยึด:</span><span class="sxs-lookup"><span data-stu-id="ca14a-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ca14a-181">ในกล่องข้อความ คลิกตำแหน่งที่ต้องการให้ตัวยึดปรากฏ</span><span class="sxs-lookup"><span data-stu-id="ca14a-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ca14a-182">คลิก **แทรกตัวยึด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ca14a-183">ในรายการที่ปรากฏขึ้น ให้เลือกตัวยึดที่จะแทรก</span><span class="sxs-lookup"><span data-stu-id="ca14a-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ca14a-184">คลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="ca14a-184">Click **Insert**.</span></span>

6. <span data-ttu-id="ca14a-185">เมื่อต้องการเพิ่มคำแปลของการแจ้งเตือน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="ca14a-186">คลิก **คำแปล**</span><span class="sxs-lookup"><span data-stu-id="ca14a-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="ca14a-187">บนหน้าที่ปรากฏ คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ca14a-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ca14a-188">ในรายการที่ปรากฏ ให้เลือกภาษาที่คุณกำลังป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ca14a-189">ในฟิลด์ **ข้อความที่แปล** ให้ป้อนข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca14a-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ca14a-190">เมื่อต้องการให้ข้อความเป็นแบบส่วนบุคคล คุณสามารถแทรกตัวยึดตามที่อธิบายไว้ในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="ca14a-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="ca14a-191">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-191">Click **Close**.</span></span>

7. <span data-ttu-id="ca14a-192">ในแท็บ **ผู้รับ** ระบุผู้ที่จะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="ca14a-193">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="ca14a-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ca14a-194">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-194">Option</span></span></th>
    <th><span data-ttu-id="ca14a-195">ผู้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="ca14a-196">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ca14a-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ca14a-197">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="ca14a-197">Participant</span></span></td>
    <td><span data-ttu-id="ca14a-198">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="ca14a-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-199">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ca14a-200">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือจะส่งการแจ้งเตือนไปยัง</span><span class="sxs-lookup"><span data-stu-id="ca14a-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-201">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-201">Workflow user</span></span></td>
    <td><span data-ttu-id="ca14a-202">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ca14a-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ca14a-203">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-204">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca14a-204">User</span></span></td>
    <td><span data-ttu-id="ca14a-205">ผู้ใช้ Microsoft Dynamics 365 for Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ca14a-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-206">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ca14a-207"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ca14a-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ca14a-208">เลือกผู้ใช้ที่จะส่งการแจ้งเตือน จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="ca14a-209">ทำซ้ำขั้นตอนที่ 3 ถึง 7 สำหรับแต่ละเหตุการณ์ที่คุณเลือกไว้ในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="ca14a-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="ca14a-210">มอบหมายการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-210">Assign a decision</span></span>

<span data-ttu-id="ca14a-211">ทำตามขั้นตอนเหล่านี้เพื่อระบุผู้ที่ควรกำหนดการตัดสินใจด้วยตนเองให้</span><span class="sxs-lookup"><span data-stu-id="ca14a-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="ca14a-212">ในบานหน้าต่างทางซ้าย ให้คลิก **การกำหนด**</span><span class="sxs-lookup"><span data-stu-id="ca14a-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="ca14a-213">บนแท็บ **ชนิดการกำหนด** เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="ca14a-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ca14a-214">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-214">Option</span></span></th>
    <th><span data-ttu-id="ca14a-215">ผู้ใช้ที่ได้รับการกำหนดการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="ca14a-216">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ca14a-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ca14a-217">ผู้เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="ca14a-217">Participant</span></span></td>
    <td><span data-ttu-id="ca14a-218">ผู้ใช้ที่กำหนดให้กับกลุ่มหรือบทบาทที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="ca14a-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-219">หลังจากที่คุณเลือก <strong>ผู้เข้าร่วม</strong>บนแท็บ <strong>ตามบทบาท</strong>  ในรายการ <strong>ชนิดของผู้เข้าร่วม</strong> เลือกชนิดของกลุ่มหรือบทบาทที่จะกำหนดการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="ca14a-220">ในรายการ <strong>ผู้เข้าร่วม</strong> เลือกกลุ่มหรือบทบาทที่จะกำหนดการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-221">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="ca14a-222">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ca14a-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-223">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะกำหนดการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="ca14a-224">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="ca14a-225">ชื่อเหล่านี้คือผู้ใช้ที่สามารถกำหนดการตัดสินใจได้</span><span class="sxs-lookup"><span data-stu-id="ca14a-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="ca14a-226">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="ca14a-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="ca14a-227">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="ca14a-228">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="ca14a-229">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="ca14a-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ca14a-230">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรกำหนดให้กับผู้ใช้ใดในช่วงการตัดสินใจ:</span><span class="sxs-lookup"><span data-stu-id="ca14a-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="ca14a-231"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– การตัดสินใจถูกกำหนดให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="ca14a-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="ca14a-232"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> การตัดสินใจถูกกำหนดให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="ca14a-233"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – การตัดสินใจไม่ถูกกำหนดให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ca14a-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="ca14a-234">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="ca14a-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-235">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-235">Workflow user</span></span></td>
    <td><span data-ttu-id="ca14a-236">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ca14a-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ca14a-237">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-238">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca14a-238">User</span></span></td>
    <td><span data-ttu-id="ca14a-239">ผู้ใช้ Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ca14a-239">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-240">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ca14a-241"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ca14a-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ca14a-242">เลือกผู้ใช้ที่จะกำหนดการตัดสินใจ จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-243">คิว</span><span class="sxs-lookup"><span data-stu-id="ca14a-243">Queue</span></span></td>
    <td><span data-ttu-id="ca14a-244">คิวรายการงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-245">หลังจากที่คุณเลือก <strong>คิว</strong>คลิกที่แท็บ <strong>ตามคิว</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="ca14a-246">เมื่อต้องการกำหนดการตัดสินใจในคิวเฉพาะ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="ca14a-247">ในรายการ <strong>ชนิดของคิว</strong> เลือก <strong>คิวรายการงาน</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca14a-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="ca14a-248">ในรายการ <strong>ชื่อคิว</strong> เลือกคิว</span><span class="sxs-lookup"><span data-stu-id="ca14a-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ca14a-249">ถ้าเงื่อนไขที่ระบุควรกำหนดคิวที่กำหนดการตัดสินใจ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="ca14a-250">ในรายการ <strong>ชนิดของคิว</strong> เลือก <strong>คิวรายการงานแบบมีเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="ca14a-251">ในรายการ <strong>ชื่อคิว</strong> เลือก <strong>คิวแบบมีเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="ca14a-252">ตัวเลือกนี้จะใช้สำหรับลำดับงานเพียงไม่กี่รายการ เช่น การจัดการกรณี</span><span class="sxs-lookup"><span data-stu-id="ca14a-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="ca14a-253">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="ca14a-254">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-254">Select one of the following options:</span></span>

    - <span data-ttu-id="ca14a-255">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="ca14a-256">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca14a-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ca14a-257">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="ca14a-258">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca14a-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ca14a-259">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="ca14a-260">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="ca14a-261">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตัดสินใจภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ca14a-262">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="ca14a-263">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตัดสินใจภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="ca14a-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="ca14a-264">ถ้าผู้ใช้ไม่ทำการตัดสินใจในเวลาที่กำหนด การตัดสินใจจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="ca14a-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="ca14a-265">การตัดสินใจที่เกินกำหนดจะถูกเลื่อนระดับตามตัวเลือกที่คุณเลือกในพื้นที่ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="ca14a-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="ca14a-266">การระบุสิ่งที่จะเกิดขึ้นเมื่อการตัดสินใจเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="ca14a-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="ca14a-267">ถ้าผู้ใช้ไม่ทำการตัดสินใจในเวลาที่กำหนด การตัดสินใจจะเกินกำหนด</span><span class="sxs-lookup"><span data-stu-id="ca14a-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="ca14a-268">การตัดสินใจที่เกินกำหนดอาจถูกเลื่อนระดับหรือถูกกำหนดให้กับผู้ใช้รายอื่นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ca14a-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="ca14a-269">ทำตามขั้นตอนเหล่านี้เพื่อเลื่อนระดับการตัดสินใจถ้าเกินกำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="ca14a-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="ca14a-270">ในบานหน้าต่างทางซ้าย ให้คลิก **การเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="ca14a-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="ca14a-271">เลือกกล่องกาเครื่องหมาย **ใช้พาธการเลื่อนระดับ** เพื่อสร้างพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="ca14a-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="ca14a-272">ระบบจะกำหนดการตัดสินใจให้กับผู้ใช้ที่อยู่ในพาธการเลื่อนระดับโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ca14a-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="ca14a-273">ตัวอย่างเช่น ตารางต่อไปนี้แสดงพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="ca14a-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="ca14a-274">ลำดับ</span><span class="sxs-lookup"><span data-stu-id="ca14a-274">Sequence</span></span> | <span data-ttu-id="ca14a-275">พาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="ca14a-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="ca14a-276">1</span><span class="sxs-lookup"><span data-stu-id="ca14a-276">1</span></span>        | <span data-ttu-id="ca14a-277">กำหนดให้กับ: Donna</span><span class="sxs-lookup"><span data-stu-id="ca14a-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="ca14a-278">2</span><span class="sxs-lookup"><span data-stu-id="ca14a-278">2</span></span>        | <span data-ttu-id="ca14a-279">กำหนดให้กับ: Erin</span><span class="sxs-lookup"><span data-stu-id="ca14a-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="ca14a-280">3</span><span class="sxs-lookup"><span data-stu-id="ca14a-280">3</span></span>        | <span data-ttu-id="ca14a-281">การดำเนินการขั้นสุดท้าย: \[ตัวเลือก 1\]</span><span class="sxs-lookup"><span data-stu-id="ca14a-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="ca14a-282">ในตัวอย่างนี้ ระบบจะกำหนดการตัดสินใจที่เกินกำหนดให้กับ Donna</span><span class="sxs-lookup"><span data-stu-id="ca14a-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="ca14a-283">ถ้า Donna ไม่ทำการตัดสินใจในเวลาที่กำหนด ระบบจะกำหนดการตัดสินใจให้กับ Erin</span><span class="sxs-lookup"><span data-stu-id="ca14a-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="ca14a-284">ถ้า Erin ไม่ทำการตัดสินใจในเวลาที่กำหนด ระบบจะเลือก **\[ตัวเลือก 1\]** เป็นการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="ca14a-285">เมื่อต้องการเพิ่มผู้ใช้ในพาธการเลื่อนระดับ คลิก **เพิ่มการเลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="ca14a-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="ca14a-286">เลือกหนึ่งในตัวเลือกในตารางต่อไปนี้ และทำตามขั้นตอนเพิ่มเติมสำหรับตัวเลือกนั้นก่อนที่คุณจะไปยังขั้นตอนที่ 4</span><span class="sxs-lookup"><span data-stu-id="ca14a-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ca14a-287">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-287">Option</span></span></th>
    <th><span data-ttu-id="ca14a-288">ผู้ใช้ที่ได้รับการเลื่อนระดับการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="ca14a-289">ขั้นตอนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ca14a-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ca14a-290">ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="ca14a-291">ผู้ใช้ในลำดับชั้นขององค์กรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ca14a-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-292">หลังจากที่คุณเลือก <strong>ลำดับชั้น</strong>บนแท็บ <strong>การเลือกลำดับชั้น</strong>  ในรายการ <strong>ชนิดของลำดับชั้น</strong> เลือกชนิดของลำดับชั้นที่จะเลื่อนระดับการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="ca14a-293">ระบบต้องดึงข้อมูลช่วงชื่อผู้ใช้จากลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="ca14a-294">ชื่อเหล่านี้คือผู้ใช้ที่สามารถเลื่อนระดับการตัดสินใจได้</span><span class="sxs-lookup"><span data-stu-id="ca14a-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="ca14a-295">ทำตามขั้นตอนเหล่านี้เพื่อระบุจุดเริ่มต้นและจุดสิ้นสุดของช่วงดังกล่าวของชื่อผู้ใช้ที่ระบบดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="ca14a-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="ca14a-296">หากต้องการระบุจุดเริ่มต้น ให้เลือกบุคคลในรายการ <strong>เริ่มต้นจาก</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="ca14a-297">หากต้องการระบุจุดสิ้นสุด ให้คลิก <strong>เพิ่มเงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="ca14a-298">จากนั้นป้อนเงื่อนไขที่กำหนดตำแหน่งในลำดับชั้นที่ระบบจะหยุดดึงข้อมูลชื่อ</span><span class="sxs-lookup"><span data-stu-id="ca14a-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ca14a-299">บนแท็บ <strong>ตัวเลือกลำดับชั้น</strong> ระบุว่าควรเลื่อนระดับให้กับผู้ใช้ใดในช่วงการตัดสินใจ:</span><span class="sxs-lookup"><span data-stu-id="ca14a-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="ca14a-300"><strong>กำหนดให้กับผู้ใช้ทั้งหมดที่ดึงข้อมูล</strong>– การตัดสินใจถูกเลื่อนระดับให้กับผู้ใช้ทั้งหมดในช่วง</span><span class="sxs-lookup"><span data-stu-id="ca14a-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="ca14a-301"><strong>กำหนดให้กับผู้ใช้คนสุดท้ายที่ถูกดึงข้อมูลเท่านั้น</strong> การตัดสินใจถูกเลื่อนระดับให้กับผู้ใช้คนสุดท้ายที่อยู่ในช่วงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ca14a-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="ca14a-302"><strong>ไม่รวมผู้ใช้ที่มีเงื่อนไขต่อไปนี้</strong> – การตัดสินใจไม่ถูกเลื่อนระดับให้กับผู้ใช้ใด ๆ ในช่วงที่ตรงตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ca14a-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="ca14a-303">คลิก <strong>เพิ่มเงื่อนไข</strong> เพื่อระบุเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="ca14a-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-304">ผู้ใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-304">Workflow user</span></span></td>
    <td><span data-ttu-id="ca14a-305">ผู้ใช้ในลำดับงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ca14a-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ca14a-306">หลังจากที่คุณเลือก <strong>ผู้ใช้ลำดับงาน</strong>บนแท็บ <strong>ผู้ใช้ลำดับงาน</strong> ในรายการ <strong>ผู้ใช้ลำดับงาน</strong> เลือกผู้ใช้ที่เข้าร่วมในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ca14a-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ca14a-307">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca14a-307">User</span></span></td>
    <td><span data-ttu-id="ca14a-308">ผู้ใช้ Finance and Operations เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ca14a-308">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ca14a-309">หลังจากที่คุณเลือก <strong>ผู้ใช้</strong>คลิกแท็บ <strong>ผู้ใช้</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ca14a-310"><strong>ผู้ใช้ที่พร้อมใช้งาน</strong> ประกอบด้วยผู้ใช้ Finance and Operations ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ca14a-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ca14a-311">เลือกผู้ใช้ที่จะเลื่อนระดับการตัดสินใจ จากนั้นย้ายผู้ใช้เหล่านั้นไปยังรายการ <strong>ผู้ใช้ที่เลือก</strong></span><span class="sxs-lookup"><span data-stu-id="ca14a-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="ca14a-312">บนแท็บ **ขีดจำกัดเวลา** ในฟิลด์ **ระยะเวลา** ระบุระยะเวลาที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="ca14a-313">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-313">Select one of the following options:</span></span>

    - <span data-ttu-id="ca14a-314">**ชั่วโมง**– ป้อนจำนวนชั่วโมงที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="ca14a-315">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca14a-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ca14a-316">**วัน**– ป้อนจำนวนวันที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="ca14a-317">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca14a-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ca14a-318">**สัปดาห์**– ป้อนจำนวนสัปดาห์ที่ผู้ใช้ต้องตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="ca14a-319">**เดือน**– เลือกวันและสัปดาห์ที่ผู้ใช้ต้องใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="ca14a-320">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตัดสินใจภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ca14a-321">**ปี**– เลือกวัน สัปดาห์และเดือนที่ผู้ใช้ต้องใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="ca14a-322">ตัวอย่างเช่น คุณอาจต้องการให้ผู้ใช้ตัดสินใจภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="ca14a-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="ca14a-323">ทำซ้ำขั้นตอนที่ 3 ถึง 4 สำหรับแต่ละผู้ใช้ที่ควรจะเพิ่มในพาธการเลื่อนระดับ</span><span class="sxs-lookup"><span data-stu-id="ca14a-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="ca14a-324">คุณสามารถเปลี่ยนลำดับของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="ca14a-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="ca14a-325">ถ้าผู้ใช้ในพาธการเลื่อนระดับไม่ทำการตัดสินใจในเวลาที่กำหนด ระบบจะทำการตัดสินใจเอง</span><span class="sxs-lookup"><span data-stu-id="ca14a-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="ca14a-326">เมื่อต้องการระบุตัวเลือกที่ระบบเลือก เลือกแถว **การดำเนินการ** จากนั้น บนแท็บ **สิ้นสุดการดำเนินการ** เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="ca14a-327">การกำหนดขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="ca14a-327">Set a time limit</span></span>

<span data-ttu-id="ca14a-328">ทำตามขั้นตอนเหล่านี้ถ้าต้องทำการตัดสินใจในเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ca14a-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="ca14a-329">ตัวเลือกที่คุณเลือกในกระบวนงานนี้จะแทนที่ตัวเลือกที่คุณเลือกไว้ในพื้นที่ **การกำหนด** และ **การเลื่อนระดับ** ของหน้า</span><span class="sxs-lookup"><span data-stu-id="ca14a-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="ca14a-330">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="ca14a-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="ca14a-331">เลือกกล่องกาเครื่องหมาย **ตั้งค่าขีดจำกัดเวลาสำหรับองค์ประกอบลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="ca14a-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="ca14a-332">ในฟิลด์ **ระยะเวลา** ระบุเวลาที่ต้องทำการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="ca14a-333">เลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ca14a-333">Select one of the following options:</span></span>

    - <span data-ttu-id="ca14a-334">**ชั่วโมง** – ป้อนจำนวนชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="ca14a-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="ca14a-335">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca14a-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ca14a-336">**วัน** – ป้อนจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="ca14a-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="ca14a-337">แล้วเลือกปฏิทินที่องค์กรของคุณใช้ และป้อนข้อมูลเกี่ยวกับสัปดาห์ทำงานขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca14a-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ca14a-338">**สัปดาห์** – ป้อนจำนวนสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="ca14a-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="ca14a-339">**เดือน**– เลือกวันและสัปดาห์ที่ต้องใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="ca14a-340">ตัวอย่างเช่น คุณอาจต้องการให้ทำการตัดสินใจภายในวันศุกร์ของสัปดาห์ที่สามของเดือน</span><span class="sxs-lookup"><span data-stu-id="ca14a-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ca14a-341">**ปี**– เลือกวัน สัปดาห์และเดือนที่ต้องใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="ca14a-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="ca14a-342">ตัวอย่างเช่น คุณอาจต้องการให้ทำการตัดสินใจภายในวันศุกร์ของสัปดาห์ที่สามของเดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="ca14a-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="ca14a-343">ระบบจะทำการตัดสินใจเองหากเกินขอบเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="ca14a-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="ca14a-344">ในรายการ **การดำเนินการ** เลือกตัวเลือกที่ระบบควรเลือก</span><span class="sxs-lookup"><span data-stu-id="ca14a-344">In the **Action** list, select the option that the system should select.</span></span>
