---
title: เชื่อมต่อระบบวิธีใช้
description: หัวข้อนี้อธิบายองค์ประกอบของระบบวิธีใช้สำหรับ Microsoft Dynamics 365 for Finance and Operations และให้ภาพรวมของวิธีการเชื่อมต่อและสรุปของวิธีการสร้างวิธีใช้แบบกำหนดเอง
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 929e453987c6e2773d1886d03a4393a68033566b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850912"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="53349-103">เชื่อมต่อระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="53349-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53349-104">หัวข้อนี้อธิบายองค์ประกอบของระบบวิธีใช้สำหรับ Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="53349-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="53349-105">และให้ภาพรวมของวิธีการเชื่อมต่อส่วนประกอบเหล่านี้และสรุปวิธีการสร้างวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="53349-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="53349-106">สถาปัตยกรรมของวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="53349-106">Help architecture</span></span>

<span data-ttu-id="53349-107">ภาพประกอบต่อไปนี้แสดงส่วนประกอบของระบบวิธีใช้ของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="53349-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="53349-108">ระบบวิธีใช้ภายในผลิตภัณฑ์ดึงบทความจากไซต์ Finance and Operations ใน https://docs.microsoft.com ตลอดจนคู่มืองานที่จัดเก็บอยู่ในตัวทำแบบจำลองกระบวนการทางธุรกิจใน Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="53349-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="53349-109">มีการวางแผนลักษณะการทำงานที่แสดงไว้ในไดอะแกรมที่มีเครื่องหมายดอกจัน (\*) แต่ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="53349-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="53349-110">[![สถาปัตยกรรมของวิธีใช้](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="53349-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="53349-111">การเชื่อมต่อระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="53349-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="53349-112">แท็บ **คู่มืองาน** ไม่พร้อมใช้งานในขณะนี้ใน Microsoft Dynamics 365 for Talent และ Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="53349-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="53349-113">เรากำลังดำเนินกรเพื่อเปิดใช้งานฟังก์ชันนี้ในรุ่นต่อไป</span><span class="sxs-lookup"><span data-stu-id="53349-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="53349-114">คู่มืองานในประสบการณ์การเริ่มต้นใช้งานใน Talent ยังคงพร้อมใช้งานเพื่อให้ครอบคลุมฟังก์ชันพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="53349-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="53349-115">นอกจากนี้วิธีใช้ตามขั้นตอนยังพร้อมใช้งานบนไซต์ docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) สำหรับทั้ง Retail และ Talent</span><span class="sxs-lookup"><span data-stu-id="53349-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="53349-116">การใช้หน้า **พารามิเตอร์ระบบ** ผู้ดูแลระบบจะเชื่อมต่อชิ้นส่วนของระบบวิธีใช้สำหรับการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="53349-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="53349-117">[![แบบฟอร์มพารามิเตอร์ระบบพร้อมการตั้งค่าวิธีใช้](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="53349-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="53349-118">ในหน้า **พารามิเตอร์ระบบ** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="53349-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53349-119">ในครั้งแรกที่คุณเปิดแท็บ **วิธีใช้** คุณต้องเชื่อมต่อกับ Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="53349-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="53349-120">ตรวจสอบให้แน่ใจว่าคลิกลิงค์ในกึ่งกลางของแบบฟอร์ม รอการเชื่อมต่อ ปิดกล่องโต้ตอบ และจากนั้นคลิก **ตกลง** เพื่อเข้าถึงหน้า **พารามิเตอร์ระบบ**</span><span class="sxs-lookup"><span data-stu-id="53349-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="53349-121">[![เชื่อมต่อไปยัง LCS](./media/connect-to-lcs-crop-1024x365.png "เชื่อมต่อไปยัง LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="53349-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="53349-122">เลือกโครงการ Lifecycle Services เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="53349-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="53349-123">เลือกไลบรารี BPM (ภายในโครงการที่เลือก) เพื่อดึงข้อมูลการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="53349-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="53349-124">สำหรับ Finance and Operations สำหรับเนื้อหา Microsoft เลือกไลบรารี่โดยรวมของ APQC ล่าสุดสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="53349-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="53349-125">สำหรับ Retail เราจะนำออกใช้ไลบรารีในอนาคตอันใกล้</span><span class="sxs-lookup"><span data-stu-id="53349-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="53349-126">คุณไม่ต้องเลือกไลบรารีสำหรับ Talent — มีการสร้างการเชื่อมต่อกับไลบรารีที่ถูกต้องให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="53349-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="53349-127">ตั้งค่าลำดับการแสดงผลของไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="53349-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="53349-128">ซึ่งจะกำหนดลำดับว่าบันทึกงานใดจะปรากฏขึ้นในบานหน้าต่าง **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="53349-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="53349-129">หลังจากที่คุณเสร็จสิ้นขั้นตอนเหล่านี้ คุณสามารถเปิดบานหน้าต่าง **วิธีใช้** และคลิกแท็บ **คู่มืองาน** คุณจะเห็นคู่มืองานที่ใช้กับหน้าที่คุณกำลังอยู่ใน Finance and Operations ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="53349-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="53349-130">ถ้าไม่พบคู่มืองาน คุณสามารถป้อนคำสำคัญเพื่อจำกัดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="53349-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="53349-131">แสดงคำแปลคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="53349-131">Showing translated task guides</span></span>

<span data-ttu-id="53349-132">คู่มืองานที่แปลแล้วถูกจัดส่งในไลบรารี่โดยรวมของ APQC เดือนพฤษภาคม 2016 และไลบรารีการเริ่มต้นใช้งานก่อน</span><span class="sxs-lookup"><span data-stu-id="53349-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="53349-133">ใน Finance and Operations เมื่อต้องการดูวิธีใช้ของคู่มืองานที่เป็นภาษาท้องถิ่น ให้ตรวจสอบให้แน่ใจว่าคุณได้เชื่อมต่อไปยังไลบรารีเดือนพฤษภาคมแล้ว</span><span class="sxs-lookup"><span data-stu-id="53349-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="53349-134">ภาษาที่ปรากฏในคู่มืองานมีการควบคุมสำหรับผู้ใช้แต่ละรายโดยการตั้งค่าภาษาภายใต้ **ตัวเลือก** &gt; **การกำหนดลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="53349-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="53349-135">แม้ว่าจะมีคู่มืองานจำนวนมากที่ได้รับการแปลแล้ว ในขณะนี้ไคลเอนต์ Finance and Operations ไม่แสดงชื่อคู่มืองานที่แปลแล้ว</span><span class="sxs-lookup"><span data-stu-id="53349-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="53349-136">นอกจากนี้ มีคู่มืองานที่ถูกนำออกใช้ในเดือนกุมภาพันธ์ 2016 เท่านั้นที่พร้อมใช้งานในการแปลในไลบรารีเดือนพฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="53349-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="53349-137">เราจะปล่อยไลบรารีที่ปรับปรุงแล้วพร้อมกับคำแปลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="53349-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="53349-138">ถ้าคู่มืองานได้รับการแปลแล้ว เมื่อคุณเปิดคู่มืองานนั้น ข้อความทั้งหมดของคู่มืองานจะปรากฏในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="53349-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="53349-139">ถ้าคู่มืองานยังไม่ได้รับการแปล เมื่อคุณเปิดคู่มืองานนั้น จะปรากฏข้อความเพียงบางส่วน (ข้อความของการควบคุม) ในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="53349-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="53349-140">การสร้างวิธีใช้ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="53349-140">Creating custom help</span></span>

<span data-ttu-id="53349-141">คุณสามารถใช้คู่มืองานเพื่อสร้างวิธีใช้แบบกำหนดเอง หรือเชื่อมต่อเว็บไซต์ไปยังบานหน้าต่างวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="53349-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="53349-142">สร้างวิธีใช้แบบกำหนดเองด้วยคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="53349-142">Create custom help with task guides</span></span>

<span data-ttu-id="53349-143">คุณสามารถสร้างวิธีใช้ที่กำหนดเองสำหรับการใช้งาน Finance and Operations และสำหรับ Retail โดยการสร้างบันทึกงานที่สะท้อนถึงการใช้งาน และบันทึกวิธีใช้เหล่านั้นลงในไลบรารีกระบวนการทางธุรกิจมี LCS</span><span class="sxs-lookup"><span data-stu-id="53349-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="53349-144">คุณไม่สามารถสร้างคู่มืองานแบบกำหนดเองสำหรับ Talent</span><span class="sxs-lookup"><span data-stu-id="53349-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="53349-145">สำหรับคู่ค้า ถ้าคุณเลื่อนลำดับเป็นไลบรารีของบริษัท และรวมอยู่ในโซลูชัน ไลบรารีนั้นจะพร้อมใช้งานสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="53349-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="53349-146">คุณสามารถทำสำเนาสากล APQC และจากนั้นเปิดสำเนาของคุณ เปิดบันทึกงานจากไลบรารีนั้น ปรับเปลี่ยน และบันทึกบันทึกงานที่ึคุณทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="53349-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="53349-147">สำหรับข้อมูลเพิ่มเติม ดู [วิธีการสร้างบันทึกงานเพื่อใช้เป็นเอกสารหรือการฝึกอบรม](../../dev-itpro/user-interface/task-recorder.md)</span><span class="sxs-lookup"><span data-stu-id="53349-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="53349-148">เชื่อมต่อไซต์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="53349-148">Connect a custom site</span></span>

<span data-ttu-id="53349-149">Microsoft มีเอกสารและรหัสตัวอย่างที่อธิบายถึงวิธีการสร้างและการเชื่อมโยงไซต์วิธีใช้แบบกำหนดเองไปยังบานหน้าต่างวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="53349-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="53349-150">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="53349-150">For more information, see:</span></span>

- [<span data-ttu-id="53349-151">สร้างวิธีใช้แบบกำหนดเองสำหรับ Finance and Operations (เอกสาร)</span><span class="sxs-lookup"><span data-stu-id="53349-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="53349-152">ที่เก็บ GitHub วิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="53349-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="53349-153">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="53349-153">Additional resources</span></span>

[<span data-ttu-id="53349-154">ภาพรวมของวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="53349-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="53349-155">ภาพรวมของตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="53349-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="53349-156">วิธีการสร้างการบันทึกงานเพื่อใช้เป็นเอกสารหรือการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="53349-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
