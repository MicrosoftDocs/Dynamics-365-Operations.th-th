---
title: เชื่อมต่อระบบวิธีใช้
description: หัวข้อนี้อธิบายองค์ประกอบของระบบวิธีใช้สำหรับแอป Finance and Operations และให้ภาพรวมของวิธีการเชื่อมต่อและบทสรุปของวิธีการสร้างวิธีใช้แบบกำหนดเอง
author: margoc
manager: AnnBe
ms.date: 10/02/2019
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
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006183"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="0eb5e-103">เชื่อมต่อระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0eb5e-104">หัวข้อนี้จะอธิบายเกี่ยวกับส่วนประกอบของระบบวิธีใช้สำหรับแอป Finance and Operations เช่น Dynamics 365 Finance Supply Chain Management Commerce และ Human Resources</span><span class="sxs-lookup"><span data-stu-id="0eb5e-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="0eb5e-105">และให้ภาพรวมของวิธีการเชื่อมต่อส่วนประกอบเหล่านี้และสรุปวิธีการสร้างวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0eb5e-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="0eb5e-106">สถาปัตยกรรมของวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-106">Help architecture</span></span>

<span data-ttu-id="0eb5e-107">ภาพประกอบต่อไปนี้แสดงส่วนประกอบของระบบให้ความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="0eb5e-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="0eb5e-108">ระบบให้ความช่วยเหลือภายในผลิตภัณฑ์ดึงบทความจาก https://docs.microsoft.com ตลอดจนคู่มืองานที่จัดเก็บอยู่ในแบบจำลองกระบวนการทางธุรกิจใน Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="0eb5e-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="0eb5e-109">มีการวางแผนลักษณะการทำงานที่แสดงไว้ในไดอะแกรมที่มีเครื่องหมายดอกจัน (\*) แต่ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="0eb5e-110">[![สถาปัตยกรรมของวิธีใช้](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="0eb5e-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="0eb5e-111">การเชื่อมต่อระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="0eb5e-112">แท็บ **คู่มืองาน** ไม่พร้อมใช้งานในขณะนี้ใน Dynamics 365 Human Resources หรือ Commerce</span><span class="sxs-lookup"><span data-stu-id="0eb5e-112">The **Task guides** tab is currently not available in Dynamics 365 Human Resources or Commerce.</span></span> <span data-ttu-id="0eb5e-113">เรากำลังดำเนินกรเพื่อเปิดใช้งานฟังก์ชันนี้ในรุ่นต่อไป</span><span class="sxs-lookup"><span data-stu-id="0eb5e-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="0eb5e-114">คู่มืองานในประสบการณ์การเริ่มต้นใช้งานในทรัพยากรบุคคลยังคงพร้อมใช้งานเพื่อให้ครอบคลุมฟังก์ชันพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-114">The Task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="0eb5e-115">วิธีใช้ตามขั้นตอนยังมีอยู่บนไซต์ docs.microsoft.com สำหรับทรัพยากรบุคคลและ Commerce</span><span class="sxs-lookup"><span data-stu-id="0eb5e-115">Procedural help is also available on the docs.microsoft.com site for both Human Resources and Commerce.</span></span>

<span data-ttu-id="0eb5e-116">การใช้หน้า **พารามิเตอร์ระบบ** ผู้ดูแลระบบจะเชื่อมต่อชิ้นส่วนของระบบวิธีใช้สำหรับการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="0eb5e-117">[![แบบฟอร์มพารามิเตอร์ระบบพร้อมการตั้งค่าวิธีใช้](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="0eb5e-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="0eb5e-118">ในหน้า **พารามิเตอร์ระบบ** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0eb5e-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0eb5e-119">ในครั้งแรกที่คุณเปิดแท็บ **วิธีใช้** คุณต้องเชื่อมต่อกับ Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0eb5e-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="0eb5e-120">ตรวจสอบให้แน่ใจว่าคลิกลิงค์ในกึ่งกลางของแบบฟอร์ม รอการเชื่อมต่อ ปิดกล่องโต้ตอบ และจากนั้นคลิก **ตกลง** เพื่อเข้าถึงหน้า **พารามิเตอร์ระบบ**</span><span class="sxs-lookup"><span data-stu-id="0eb5e-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="0eb5e-121">[![เชื่อมต่อกับ LCS](./media/connect-to-lcs-crop-1024x365.png "เชื่อมต่อกับ LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="0eb5e-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="0eb5e-122">เลือกโครงการ Lifecycle Services เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="0eb5e-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="0eb5e-123">เลือกไลบรารี BPM (ภายในโครงการที่เลือก) เพื่อดึงข้อมูลการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="0eb5e-124">ตั้งค่าลำดับการแสดงผลของไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="0eb5e-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="0eb5e-125">ซึ่งจะกำหนดลำดับว่าบันทึกงานใดจะปรากฏขึ้นในบานหน้าต่าง **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="0eb5e-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="0eb5e-126">หลังจากที่คุณเสร็จสิ้นขั้นตอนเหล่านี้ คุณสามารถเปิดบานหน้าต่าง **วิธีใช้** และคลิกแท็บ **คู่มืองาน**  คุณจะเห็นคู่มืองานที่ใช้กับหน้าหน้าต่างที่คุณกำลังอยู่ในแอป Finance and Operations ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="0eb5e-127">ถ้าไม่พบคู่มืองาน คุณสามารถป้อนคำสำคัญเพื่อจำกัดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0eb5e-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="0eb5e-128">แสดงคำแปลคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-128">Showing translated task guides</span></span>

<span data-ttu-id="0eb5e-129">คู่มืองานที่แปลแล้วถูกจัดส่งในไลบรารี่โดยรวมของ APQC เดือนพฤษภาคม 2016 และไลบรารีการเริ่มต้นใช้งานก่อน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="0eb5e-130">ในแอป Finance and Operations เมื่อต้องการดูวิธีใช้ของคู่มืองานที่เป็นภาษาท้องถิ่น ให้ตรวจสอบให้แน่ใจว่าคุณได้เชื่อมต่อไปยังไลบรารีเดือนพฤษภาคมแล้ว</span><span class="sxs-lookup"><span data-stu-id="0eb5e-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="0eb5e-131">ภาษาที่ปรากฏในคู่มืองานมีการควบคุมสำหรับผู้ใช้แต่ละรายโดยการตั้งค่าภาษาภายใต้ **ตัวเลือก** &gt; **การกำหนดลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="0eb5e-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="0eb5e-132">แม้ว่าจะมีคู่มือการใช้งานจำนวนมากที่ได้รับการแปลแล้ว แต่ตอนนี้ไคลเอนต์ยังไม่ได้แสดงชื่อคู่มือการใช้งานที่แปลแล้ว</span><span class="sxs-lookup"><span data-stu-id="0eb5e-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="0eb5e-133">นอกจากนี้ มีคู่มืองานที่ถูกนำออกใช้ในเดือนกุมภาพันธ์ 2016 เท่านั้นที่พร้อมใช้งานในการแปลในไลบรารีเดือนพฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="0eb5e-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="0eb5e-134">เราจะปล่อยไลบรารีที่ปรับปรุงแล้วพร้อมกับคำแปลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0eb5e-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="0eb5e-135">ถ้าคู่มืองานได้รับการแปลแล้ว เมื่อคุณเปิดคู่มืองานนั้น ข้อความทั้งหมดของคู่มืองานจะปรากฏในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="0eb5e-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="0eb5e-136">ถ้าคู่มืองานยังไม่ได้รับการแปล เมื่อคุณเปิดคู่มืองานนั้น จะปรากฏข้อความเพียงบางส่วน (ข้อความของการควบคุม) ในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="0eb5e-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="0eb5e-137">การสร้างวิธีใช้ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0eb5e-137">Creating custom help</span></span>

<span data-ttu-id="0eb5e-138">คุณสามารถใช้คู่มืองานเพื่อสร้างวิธีใช้แบบกำหนดเอง หรือเชื่อมต่อเว็บไซต์ไปยังบานหน้าต่างวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="0eb5e-139">สร้างวิธีใช้แบบกำหนดเองด้วยคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-139">Create custom help with task guides</span></span>

<span data-ttu-id="0eb5e-140">คุณสามารถกำหนดวิธีใช้เองสำหรับ Finance Supply Chain Management และ Commerce โดยการสร้างการบันทึกงานที่สะท้อนถึงการดำเนินงานของคุณและบันทึกวิธีใช้เหล่านั้นลงในไลบรารีกระบวนการ LCS Business</span><span class="sxs-lookup"><span data-stu-id="0eb5e-140">You can create custom help for Finance, Supply Chain Management, and Commerce by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="0eb5e-141">คุณไม่สามารถสร้างคู่มืองานแบบกำหนดเองสำหรับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-141">You cannot create custom task guides for Human Resources.</span></span>

<span data-ttu-id="0eb5e-142">สำหรับคู่ค้า ถ้าคุณเลื่อนลำดับเป็นไลบรารีของบริษัท และรวมอยู่ในโซลูชัน ไลบรารีนั้นจะพร้อมใช้งานสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="0eb5e-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="0eb5e-143">คุณสามารถทำสำเนาสากล APQC และจากนั้นเปิดสำเนาของคุณ เปิดบันทึกงานจากไลบรารีนั้น ปรับเปลี่ยน และบันทึกบันทึกงานที่ึคุณทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="0eb5e-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="0eb5e-144">สำหรับข้อมูลเพิ่มเติม ดูที่ [ทรัพยากรตัวบันทึกงาน](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="0eb5e-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="0eb5e-145">เชื่อมต่อไซต์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0eb5e-145">Connect a custom site</span></span>

<span data-ttu-id="0eb5e-146">Microsoft มีเอกสารและรหัสตัวอย่างที่อธิบายถึงวิธีการสร้างและการเชื่อมโยงไซต์วิธีใช้แบบกำหนดเองไปยังบานหน้าต่างวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="0eb5e-147">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ </span><span class="sxs-lookup"><span data-stu-id="0eb5e-147">For more information, see:</span></span>

- [<span data-ttu-id="0eb5e-148">สร้างวิธีใช้ที่กำหนดเองสำหรับแอป Finance and Operations (กระดาษขาว)</span><span class="sxs-lookup"><span data-stu-id="0eb5e-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="0eb5e-149">ที่เก็บ GitHub วิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="0eb5e-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="0eb5e-150">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0eb5e-150">Additional resources</span></span>

[<span data-ttu-id="0eb5e-151">ระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="0eb5e-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="0eb5e-152">ทรัพยากรตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="0eb5e-153">สร้างเอกสารหรือการฝึกอบรมด้วยการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="0eb5e-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
