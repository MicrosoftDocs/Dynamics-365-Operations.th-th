---
title: ตั้งค่าคอนฟิกประสบการณ์วิธีใช้สำหรับแอป Finance and Operations
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับส่วนประกอบของระบบวิธีใช้สำหรับแอปบาง Microsoft Dynamics 365 บางแอป
author: margoc
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82bb9a09e6d302b0d453ceb5131da039769b58fb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745700"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="223db-103">ตั้งค่าคอนฟิกประสบการณ์วิธีใช้สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="223db-103">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="223db-104">ในหัวข้อนี้ คุณจะพบภาพรวมของส่วนประกอบของระบบวิธีใช้สำหรับแอป Finance and Operations เช่น Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, และ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="223db-104">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="223db-105">หัวข้อนี้ยังอธิบายถึงวิธีการเชื่อมต่อส่วนประกอบเหล่านี้และแสดงสรุปกระบวนการสำหรับการสร้างวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="223db-105">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="223db-106">สถาปัตยกรรมของวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="223db-106">Help architecture</span></span>

<span data-ttu-id="223db-107">แอป Finance and Operations จะรวมภาพรวมแนวคิดและหัวข้ออื่นๆ ที่เผยแพร่ไปยังไซต์ [https://docs.microsoft.com/dynamics365](/dynamics365/)</span><span class="sxs-lookup"><span data-stu-id="223db-107">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="223db-108">คุณสามารถเข้าถึงเนื้อหานี้ได้จากบานหน้าต่าง **วิธีใช้** ในผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="223db-108">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="223db-109">ภาพประกอบต่อไปนี้แสดงส่วนประกอบของระบบให้ความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="223db-109">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="223db-110">[![สถาปัตยกรรมของวิธีใช้](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="223db-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="223db-111">ระบบวิธีใช้ในผลิตภัณฑ์ดึงบทความจาก docs.microsoft.com และเว็บไซต์ที่เชื่อมต่ออื่นๆ</span><span class="sxs-lookup"><span data-stu-id="223db-111">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="223db-112">นอกจากนี้ยังดึงในคู่มืองานที่จัดเก็บไว้ในตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM) ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="223db-112">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="223db-113">การเพิ่มคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="223db-113">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="223db-114">แท็บ **คู่มืองาน** ไม่พร้อมใช้งานในขณะนี้ในทรัพยากรบุคคลหรือ Commerce</span><span class="sxs-lookup"><span data-stu-id="223db-114">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="223db-115">อย่างไรก็ตาม คู่มืองานในประสบการณ์การเริ่มต้นใช้งานในทรัพยากรบุคคลยังคงพร้อมใช้งานเพื่อให้ครอบคลุมฟังก์ชันพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="223db-115">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="223db-116">สำหรับทั้งทรัพยากรบุคคลและ Commerce วิธีใช้ตามขั้นตอนยังมีให้ใช้บนไซต์ [https://docs.microsoft.com/dynamics365](/dynamics365/)</span><span class="sxs-lookup"><span data-stu-id="223db-116">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="223db-117">บนหน้า **พารามิเตอร์ของระบบ** ผู้ดูแลระบบสามารถตั้งค่าคอนฟิกการเข้าถึงไลบรารีของคู่มืองานที่เกี่ยวข้องสำหรับการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="223db-117">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="223db-118">หากต้องการกำหนดค่าวิธีใช้ คุณต้องลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้ในผู้เช่าเดียวกันกับผู้เช่าที่ใช้ในแอป</span><span class="sxs-lookup"><span data-stu-id="223db-118">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="223db-119">คุณจะไม่สามารถเชื่อมต่อไปยังไลบรารี LCS จากอินสแตนซ์ของแอปที่เรียกใช้บนฮาร์ดไดรฟ์เสมือนเฉพาะที่ (VHD)</span><span class="sxs-lookup"><span data-stu-id="223db-119">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="223db-120">[![แบบฟอร์มพารามิเตอร์ระบบพร้อมการตั้งค่าวิธีใช้](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="223db-120">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="223db-121&quot;>เมื่อต้องการตั้งค่าคอนฟิกคู่มืองานสำหรับโซลูชัน ให้ทำตามขั้นตอนต่อไปนี้บนหน้า **พารามิเตอร์ของระบบ**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;223db-121&quot;>To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id=&quot;223db-122&quot;>ในครั้งแรกที่คุณเปิดแท็บ **วิธีใช้** คุณต้องเชื่อมต่อกับ Lifecycle Services</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;223db-122&quot;>The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id=&quot;223db-123&quot;>ตรวจสอบให้แน่ใจว่าเลือกลิงก์ในกึ่งกลางของแบบฟอร์ม รอการเชื่อมต่อ ปิดกล่องโต้ตอบ และจากนั้นเลือก **ตกลง** เพื่อเข้าถึงหน้า **พารามิเตอร์ระบบ**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;223db-123&quot;>Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id=&quot;223db-124&quot;>[![เชื่อมต่อกับ LCS](./media/connect-to-lcs-crop-1024x365.png &quot;เชื่อมต่อกับ LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="223db-124">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="223db-125">เลือกโครงการ Lifecycle Services เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="223db-125">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="223db-126">เลือกไลบรารี BPM (ภายในโครงการที่เลือก) เพื่อดึงข้อมูลการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="223db-126">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="223db-127">ตั้งค่าลำดับการแสดงผลของไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="223db-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="223db-128">ลำดับการแสดงผลจะกำหนดลำดับว่าบันทึกงานใดจากไบรารีที่จะปรากฏขึ้นในบานหน้าต่าง **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="223db-128">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="223db-129">หลังจากที่คุณเสร็จสิ้นขั้นตอนเหล่านี้ คุณสามารถเปิดบานหน้าต่าง **วิธีใช้** และเลือกแท็บ **คู่มืองาน**  คุณจะเห็นคู่มืองานที่ใช้กับหน้าหน้าต่างที่คุณกำลังอยู่ในแอป Finance and Operations ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="223db-129">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="223db-130">ถ้าไม่พบคู่มืองาน คุณสามารถป้อนคำสำคัญเพื่อจำกัดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="223db-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="223db-131">แสดงคำแปลคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="223db-131">Showing translated task guides</span></span>

<span data-ttu-id="223db-132">คู่มืองานที่แปลแล้วถูกปล่อยใช้ในไลบรารี่โดยรวมของ APQC เดือนพฤษภาคม 2016 และไลบรารีการเริ่มต้นใช้งานก่อน</span><span class="sxs-lookup"><span data-stu-id="223db-132">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="223db-133">เมื่อต้องการดูวิธีใช้ของคู่มืองานที่เป็นภาษาท้องถิ่น ให้ตรวจสอบให้แน่ใจว่าโซลูชัน Dynamics 365 ของคุณได้เชื่อมต่อไปยังไลบรารีเดือนพฤษภาคม 2016 แล้ว</span><span class="sxs-lookup"><span data-stu-id="223db-133">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="223db-134">ผู้ใช้สามารถเปลี่ยนภาษาที่ปรากฏในคู่มืองานโดยการตั้งค่าภาษาภายใต้ **ตัวเลือก** &gt; **การกำหนดลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="223db-134">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="223db-135">แม้ว่าจะมีคู่มือการใช้งานจำนวนมากที่ได้รับการแปลแล้ว แต่ตอนนี้ไคลเอนต์ยังไม่ได้แสดงชื่อคู่มือการใช้งานที่แปลแล้ว</span><span class="sxs-lookup"><span data-stu-id="223db-135">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="223db-136">นอกจากนี้ ในไลบรารีเดือนพฤษภาคม 2016 การแปลจะพร้อมใช้งานสำหรับคู่มืองานที่ถูกนำออกใช้ในเดือนกุมภาพันธ์ 2016</span><span class="sxs-lookup"><span data-stu-id="223db-136">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="223db-137">Microsoft จะปล่อยไลบรารีที่ปรับปรุงแล้วพร้อมกับคำแปลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="223db-137">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="223db-138">ถ้าคู่มืองานได้รับการแปลแล้ว เมื่อคุณเปิดคู่มืองานนั้น ข้อความทั้งหมดของคู่มืองานจะปรากฏในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="223db-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="223db-139">ถ้าคู่มืองานยังไม่ได้รับการแปล เมื่อคุณเปิดคู่มืองานนั้น จะปรากฏข้อความเพียงบางส่วน (ข้อความของการควบคุม) ในภาษาที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="223db-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="223db-140">การเพิ่มวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="223db-140">Adding custom Help</span></span>

<span data-ttu-id="223db-141">คุณสามารถใช้คู่มืองานเพื่อสร้างวิธีใช้แบบกำหนดเอง หรือคุณสามารถเชื่อมต่อเว็บไซต์วิธีใช้แบบกำหนดเองไปยังบานหน้าต่าง **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="223db-141">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="223db-142">สร้างวิธีใช้แบบกำหนดเองโดยใช้คู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="223db-142">Create custom Help by using task guides</span></span>

<span data-ttu-id="223db-143">คุณสามารถสร้างวิธีใช้ที่กำหนดเองสำหรับแอปที่สนับสนุนโดยการสร้างบันทึกงานที่สะท้อนถึงการใช้งาน แล้วบันทึกวิธีใช้เหล่านั้นลงในไลบรารีกระบวนการทางธุรกิจใน LCS</span><span class="sxs-lookup"><span data-stu-id="223db-143">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="223db-144">คุณไม่สามารถสร้างคู่มืองานแบบกำหนดเองสำหรับทรัพยากรบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="223db-144">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="223db-145">ถ้าคุณเป็นคู่ค้า และคุณเลื่อนลำดับไลบรารีไปเป็นไลบรารีของบริษัท และรวมไว้ในโซลูชัน ไลบรารีนั้นจะพร้อมใช้งานสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="223db-145">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="223db-146">คุณสามารถทำสำเนาไลบรารี่โดยรวมของ APQC และจากนั้นเปิดบันทึกงานของคุณในสำเนา แก้ไข และบันทึกการเปลี่ยนแปลงที่คุณทำ</span><span class="sxs-lookup"><span data-stu-id="223db-146">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="223db-147">สำหรับข้อมูลเพิ่มเติม ดูที่ [ทรัพยากรตัวบันทึกงาน](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="223db-147">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="223db-148">เชื่อมต่อไซต์วิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="223db-148">Connect a custom Help site</span></span>

<span data-ttu-id="223db-149">แอป Finance and Operations ไม่ค่อยมีการใช้ในแบบฟอร์มสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="223db-149">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="223db-150">อย่างไรก็ตาม โซลูชันมีการกำหนดเองและขยายเพื่อให้ตรงกับความต้องการขององค์กร</span><span class="sxs-lookup"><span data-stu-id="223db-150">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="223db-151">นอกจากนี้คุณยังสามารถเลือกกำหนดและขยายประสบการณ์การใช้งานวิธีใช้ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="223db-151">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="223db-152">ตัวอย่างเช่น คุณสามารถเพิ่มวิธีใช้แบบกำหนดเองให้กับบานหน้าต่าง **วิธีใช้** ในผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="223db-152">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="223db-153">Microsoft มีชุดเครื่องมือเพื่อช่วยให้คุณปรับใช้และเชื่อมต่อวิธีใช้แบบกำหนดเองกับบานหน้าต่าง **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="223db-153">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="223db-154">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการที่คุณสามารถตั้งค่าโซลูชันวิธีใช้แบบกำหนดเองที่เชื่อมต่อกับบานหน้าต่าง **วิธีใช้** ให้ดูที่ [ภาพรวมวิธีใช้แบบกำหนดเอง](../../dev-itpro/help/custom-help-overview.md)</span><span class="sxs-lookup"><span data-stu-id="223db-154">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="223db-155">ถ้าคุณต้องการทำงานร่วมกันกับ Microsoft บนเครื่องมือและกระบวนการสำหรับการเลือกกำหนดวิธีใช้ ให้กรอกข้อมูลในฟอร์มที่ [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback)</span><span class="sxs-lookup"><span data-stu-id="223db-155">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="223db-156">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="223db-156">See also</span></span>

[<span data-ttu-id="223db-157">ระบบวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="223db-157">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="223db-158">ภาพรวมของวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="223db-158">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="223db-159">ทรัพยากรตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="223db-159">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="223db-160">สร้างเอกสารประกอบหรือการฝึกอบรมด้วยการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="223db-160">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="223db-161">ที่เก็บข้อมูล GitHub ของวิธีใช้แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="223db-161">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]