---
title: "เชื่อมต่อระบบวิธีใช้"
description: "หัวข้อนี้อธิบายถึงส่วนประกอบของระบบวิธีใช้สำหรับ Microsoft Dynamics 365 for Finance and Operations และให้ภาพรวมของวิธีการเชื่อมต่อและสรุปของวิธีการสร้างวิธีใช้ที่กำหนดเอง"
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: a27b21ffcde9bfbb7e6276ef35b2e48bd23af70d
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="a19b0-103">เชื่อมต่อระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="a19b0-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a19b0-104">หัวข้อนี้อธิบายส่วนประกอบของระบบวิธีใช้สำหรับ Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a19b0-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a19b0-105">และให้ภาพรวมของวิธีการเชื่อมต่อส่วนประกอบเหล่านี้และสรุปวิธีการสร้างวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a19b0-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="a19b0-106">สถาปัตยกรรมของวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="a19b0-106">Help architecture</span></span>
<span data-ttu-id="a19b0-107">ภาพประกอบต่อไปนี้แสดงส่วนประกอบของระบบวิธีใช้ของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a19b0-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="a19b0-108">ระบบภายในผลิตภัณฑ์ดึงบทความจากไซต์ Finance and Operations ที่ https://docs.microsoft.com ตลอดจนคู่มืองานที่จัดเก็บอยู่ในบบจำลองกระบวนการทางธุรกิจใน Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a19b0-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="a19b0-109">มีการวางแผนลักษณะการทำงานที่แสดงไว้ในไดอะแกรมที่มีเครื่องหมายดอกจัน (\*) แต่ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a19b0-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="a19b0-110">[![สถาปัตยกรรมของวิธีใช้](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="a19b0-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="a19b0-111">การเชื่อมต่อระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="a19b0-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="a19b0-112">ในขณะนี้แท็บ **คู่มืองาน** ไม่พร้อมใช้งานใน Microsoft Dynamics 365 for Talent และ Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="a19b0-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="a19b0-113">เรากำลังดำเนินกรเพื่อเปิดใช้งานฟังก์ชันนี้ในรุ่นต่อไป</span><span class="sxs-lookup"><span data-stu-id="a19b0-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="a19b0-114">คู่มืองานในประสบการณ์การเริ่มต้นใช้งานใน Talent ยังคงพร้อมใช้งานเพื่อให้ครอบคลุมฟังก์ชันพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="a19b0-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="a19b0-115">นอกจากนี้วิธีใช้ตามขั้นตอนยังพร้อมใช้งานบนไซต์ docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) สำหรับทั้ง Retail และ Talent</span><span class="sxs-lookup"><span data-stu-id="a19b0-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="a19b0-116">การใช้หน้า **พารามิเตอร์ระบบ** ผู้ดูแลระบบจะเชื่อมต่อชิ้นส่วนของระบบวิธีใช้สำหรับการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="a19b0-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="a19b0-117">[![แบบฟอร์มพารามิเตอร์ระบบพร้อมการตั้งค่าวิธีใช้](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) บนหน้า **พารามิเตอร์ระบบ** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a19b0-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a19b0-118">ในครั้งแรกที่คุณเปิดแท็บ **วิธีใช้** คุณต้องเชื่อมต่อกับ Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a19b0-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="a19b0-119">ตรวจสอบให้แน่ใจว่าคลิกลิงค์ในกึ่งกลางของแบบฟอร์ม รอสำหรับการเชื่อมต่อ ปิดกล่องโต้ตอบ และคลิก **ตกลง** เพื่อไปที่หน้า **พารามิเตอร์ระบบ** [![เชื่อมต่อกับ LCS](./media/connect-to-lcs-crop-1024x365.png "เชื่อมต่อกับ LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="a19b0-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="a19b0-120">เลือกโครงการ Lifecycle Services เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="a19b0-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="a19b0-121">เลือกไลบรารี BPM (ภายในโครงการที่เลือก) เพื่อดึงข้อมูลการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="a19b0-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="a19b0-122">สำหรับ Finance and Operations สำหรับเนื้อหา Microsoft เลือกไลบรารี่โดยรวมของ APQC ล่าสุดสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a19b0-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="a19b0-123">สำหรับ Retail เราจะนำออกใช้ไลบรารีในอนาคตอันใกล้</span><span class="sxs-lookup"><span data-stu-id="a19b0-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="a19b0-124">คุณไม่ต้องเลือกไลบรารีสำหรับ Talent — มีการสร้างการเชื่อมต่อกับไลบรารีที่ถูกต้องให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="a19b0-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="a19b0-125">ตั้งค่าลำดับการแสดงผลของไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="a19b0-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="a19b0-126">ซึ่งจะกำหนดลำดับว่าบันทึกงานใดจะปรากฏขึ้นในบานหน้าต่าง **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="a19b0-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="a19b0-127">หลังจากผู้ดูแลระบบเสร็จสิ้นขั้นตอนเหล่านี้ คุณสามารถเปิดบานหน้าต่าง **วิธีใช้** และคลิกแท็บ **คู่มืองาน** คุณจะเห็นคู่มืองานที่ใช้กับหน้าที่คุณกำลังอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a19b0-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="a19b0-128">ถ้าไม่พบคู่มืองาน คุณสามารถป้อนคำสำคัญเพื่อจำกัดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a19b0-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="a19b0-129">แสดงคำแปลคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="a19b0-129">Showing translated task guides</span></span>

<span data-ttu-id="a19b0-130">คู่มืองานที่แปลแล้วถูกจัดส่งในไลบรารี่โดยรวมของ APQC เดือนพฤษภาคม 2016 และไลบรารีการเริ่มต้นใช้งานก่อน</span><span class="sxs-lookup"><span data-stu-id="a19b0-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="a19b0-131">ใน Finance and Operations เมื่อต้องการดูวิธีใช้ของคู่มืองานที่เป็นภาษาท้องถิ่น ให้ตรวจสอบให้แน่ใจว่าคุณได้เชื่อมต่อไปยังไลบรารีเดือนพฤษภาคมแล้ว</span><span class="sxs-lookup"><span data-stu-id="a19b0-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="a19b0-132">ภาษาที่ปรากฏในคู่มืองานมีการควบคุมสำหรับผู้ใช้แต่ละรายโดยการตั้งค่าภาษาภายใต้ **ตัวเลือก** &gt; **การกำหนดลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="a19b0-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a19b0-133">แม้ว่าจะมีคู่มืองานจำนวนมากที่ได้รับการแปลแล้ว ในขณะนี้ไคลเอนต์ Finance and Operations ไม่แสดงชื่อคู่มืองานที่แปลแล้ว</span><span class="sxs-lookup"><span data-stu-id="a19b0-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="a19b0-134">นอกจากนี้ มีคู่มืองานที่ถูกนำออกใช้ในเดือนกุมภาพันธ์ 2016 เท่านั้นที่พร้อมใช้งานในการแปลในไลบรารีเดือนพฤษภาคม</span><span class="sxs-lookup"><span data-stu-id="a19b0-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="a19b0-135">เราจะปล่อยไลบรารีที่ปรับปรุงแล้วพร้อมกับคำแปลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a19b0-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="a19b0-136">ถ้าคู่มืองานได้รับการแปลแล้ว เมื่อคุณเปิดคู่มืองานนั้น ข้อความทั้งหมดของคู่มืองานจะปรากฏในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a19b0-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="a19b0-137">ถ้าคู่มืองานยังไม่ได้รับการแปล เมื่อคุณเปิดคู่มืองานนั้น จะปรากฏข้อความเพียงบางส่วน (ข้อความของการควบคุม) ในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a19b0-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="a19b0-138">การสร้างวิธีใช้ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a19b0-138">Creating custom help</span></span>
<span data-ttu-id="a19b0-139">คุณสามารถสร้างวิธีใช้ที่กำหนดเองสำหรับการใช้งาน Finance and Operations และสำหรับ Retail โดยการสร้างบันทึกงานที่สะท้อนถึงการใช้งาน และบันทึกวิธีใช้เหล่านั้นลงในไลบรารีกระบวนการทางธุรกิจมี LCS</span><span class="sxs-lookup"><span data-stu-id="a19b0-139">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="a19b0-140">คุณไม่สามารถสร้างคู่มืองานแบบกำหนดเองสำหรับ Talent</span><span class="sxs-lookup"><span data-stu-id="a19b0-140">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="a19b0-141">สำหรับคู่ค้า ถ้าคุณเลื่อนลำดับเป็นไลบรารีของบริษัท และรวมอยู่ในโซลูชัน ไลบรารีนั้นจะพร้อมใช้งานสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="a19b0-141">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="a19b0-142">คุณสามารถทำสำเนาสากล APQC และจากนั้นเปิดสำเนาของคุณ เปิดบันทึกงานจากไลบรารีนั้น ปรับเปลี่ยน และบันทึกบันทึกงานที่ึคุณทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a19b0-142">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="a19b0-143">สำหรับข้อมูลเพิ่มเติม ดู [วิธีการสร้างบันทึกงานเพื่อใช้เป็นเอกสารหรือการฝึกอบรม](../../dev-itpro/user-interface/task-recorder.md)</span><span class="sxs-lookup"><span data-stu-id="a19b0-143">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="a19b0-144">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="a19b0-144">See also</span></span>
--------

[<span data-ttu-id="a19b0-145">ภาพรวมของวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="a19b0-145">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="a19b0-146">ภาพรวมของตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="a19b0-146">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="a19b0-147">วิธีการสร้างการบันทึกงานเพื่อใช้เป็นเอกสารหรือการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="a19b0-147">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





