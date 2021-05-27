---
title: ตัวบันทึกงานและวิธีใช้สำหรับ Retail Modern POS (MPOS) และ Cloud POS
description: หัวข้อนี้อธิบายวิธีการใช้ตัวบันทึกงานใน Retail Modern POS และ Cloud POS
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02e8bb1bfb088a877ef23b7a81982868700f4ae2
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028118"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="5b4bd-103">ตัวบันทึกงานและวิธีใช้สำหรับ Retail Modern POS (MPOS) และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="5b4bd-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b4bd-104">หัวข้อนี้อธิบายวิธีการใช้ตัวบันทึกงานใน Retail Modern POS และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="5b4bd-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="5b4bd-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5b4bd-105">Overview</span></span>

<span data-ttu-id="5b4bd-106">ตัวบันทึกงานใน Retail Modern POS หรือ Cloud POS คือโซลูชันใหม่ที่ถูกสร้างขึ้นโดยเน้นที่การตอบสนองสูง</span><span class="sxs-lookup"><span data-stu-id="5b4bd-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="5b4bd-107">ซึ่งเป็น Application Programming Interface (API) ที่ยืดหยุ่นสำหรับการเพิ่มความสามารถและการรวมที่ต่อเนื่องสำหรับผู้บริโภคในการบันทึกกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="5b4bd-108">นอกจากนี้ การรวมตัวบันทึกงานด้วยเครื่องมือตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM) บน Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) ยังถูกเลื่อนออกไปอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="5b4bd-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="5b4bd-109">ดังนั้น ผู้ใช้สามารถผลิตไดอะแกรมกระบวนการทางธุรกิจที่หลากหลายจากการบันทึกเพื่อวิเคราะห์และออกแบบแอพลิเคชันของตนต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="5b4bd-110">สถาปัตยกรรม</span><span class="sxs-lookup"><span data-stu-id="5b4bd-110">Architecture</span></span>

<span data-ttu-id="5b4bd-111">ตัวบันทึกงานสามารถบันทึกการดำเนินการของผู้ใช้ในไคลเอนต์ที่มีความแม่นยำทุกประการ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="5b4bd-112">แต่ละการควบคุมถูกติดตั้งไว้เพื่อแจ้งให้ตัวบันทึกงานทราบเกี่ยวกับการดำเนินงานของการดำเนินการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="5b4bd-113">การควบคุมจะแจ้งตัวบันทึกงานให้ทราบเกี่ยวกับเหตุการณ์ที่เกิดขึ้นและส่งผ่านตามข้อมูลที่เกี่ยวข้องทั้งหมดเกี่ยวกับการดำเนินการของผู้ใช้ที่สอดคล้องกันในเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="5b4bd-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="5b4bd-114">จากข้อมูลนี้ ตัวบันทึกงานสามารถรวบรวมชนิดของการดำเนินการของผู้ใช้ (เช่น การคลิกปุ่ม การป้อนค่า หรือการนำทาง) และข้อมูลใด ๆ ที่เกี่ยวข้องกับการดำเนินการของผู้ใช้ (เช่น ค่าและชนิดของข้อมูลป้อนเข้า บริบทแบบฟอร์ม หรือบริบทเรกคอร์ด)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="5b4bd-115">ตัวบันทึกงานยังคงมีข้อมูลที่มีรายละเอียดที่เพียงพอที่จะช่วยรับประกันว่าการเล่นการบันทึกสามารถดำเนินการดำเนินการที่บันทึกไว้เช่นเดียวกับที่ผู้ใช้ดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="5b4bd-116">(ลักษณะการทำงานของการเล่นยังไม่ได้นำมาใช้ใน Retail modern POS หรือ Cloud POS)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="5b4bd-117">การจัดโครงแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-117">Basic configuration</span></span>

<span data-ttu-id="5b4bd-118">เมื่อต้องการเปิดใช้งานการบันทึกงานใน POS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="5b4bd-119">คลิก **Retail และ Commerce** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **เครื่องบันทึกเงินสด**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="5b4bd-120">คลิกการลงทะเบียนเพื่อเปิดใช้งานการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="5b4bd-121">บนแท็บ **การลงทะเบียน** บนแท็บด่วน **ทั่วไป** ตั้งค่าตัวเลือก **เปิดใช้งานการบันทึกงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="5b4bd-122">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-122">Click **Save**.</span></span>
5. <span data-ttu-id="5b4bd-123">ไปยัง **การขายปลีกและการค้า** &gt; **การขายปลีกและไอทีเชิงพาณิชย์** &gt; **กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="5b4bd-124">เลือกงาน **การลงทะเบียน (1090)** จากนั้นคลิก **รันทันที**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="5b4bd-125">สร้างการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-125">Create a recording</span></span>

<span data-ttu-id="5b4bd-126">ทำตามขั้นตอนเหล่านี้เพื่อสร้างการบันทึกใหม่โดยใช้ตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="5b4bd-127">เริ่มต้น Retail Modern POS หรือ Cloud POS และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="5b4bd-128">ในหน้า **การตั้งค่า** ในส่วน **ตัวบันทึกงาน** คลิก **เปิดตัวบันทึกงาน**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="5b4bd-129">บานหน้าต่าง **ตัวบันทึกงาน** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b4bd-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="5b4bd-130">คุณสามารถคลิกปุ่ม **ปิด** (**X**) ในมุมด้านขวาบนเพื่อปิดบานหน้าต่าง **ตัวบันทึกงาน** ก่อนที่คุณจะเริ่มต้นการบันทึกใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="5b4bd-131">เมื่อต้องการเปิดบานหน้าต่างอีกครั้ง ให้ทำซ้ำขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="5b4bd-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="5b4bd-132">[![บานหน้าต่างตัวบันทึกงาน](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="5b4bd-133">ป้อนชื่อและคำอธิบายสำหรับการบันทึกเงิน แล้วคลิก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="5b4bd-134">รอบเวลาการบันทึกเริ่มต้นทันทีที่คุณคลิก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b4bd-135">ถ้าคุณคลิกปุ่ม **ปิด** (**X**) ในมุมด้านขวาบน ขณะที่การบันทึกอยู่ในระหว่างดำเนินการ บานหน้าต่าง **ตัวบันทึกงาน** จะถูกปิด แต่รอบเวลาการบันทึกไม่ได้สิ้นสุดลง</span><span class="sxs-lookup"><span data-stu-id="5b4bd-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="5b4bd-136">เมื่อต้องการเปิดบานหน้าต่างตัวบันทึกงาน คลิกปุ่ม **วิธีใช้** (เครื่องหมายคำถาม) ที่ด้านบนของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="5b4bd-137">[![เครื่องหมายคำถาม](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="5b4bd-138">หลังจากที่คุณคลิก **เริ่มต้น** ตัวบันทึกงานเข้าสู่โหมดการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="5b4bd-139">บานหน้าต่าง **ตัวบันทึกงาน** แสดงรายละเอียดและตัวควบคุมที่เกี่ยวข้องกับกระบวนการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="5b4bd-140">ปฏิบัติการดำเนินการที่คุณต้องการดำเนินการในอินเทอร์เฟสผู้ใช้ (UI) ของ Retail Modern POS หรือ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="5b4bd-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="5b4bd-141">เมื่อต้องการสิ้นสุดรอบเวลาการบันทึก คลิก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="5b4bd-142">ตัวเลือกการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="5b4bd-142">Download options</span></span>

<span data-ttu-id="5b4bd-143">หลังจากที่คุณสิ้นสุดรอบเวลาการบันทึกแล้ว ตัวเลือกหลายรายการจะปรากฏขึ้น เพื่อให้คุณสามารถดาวน์โหลดการบันทึกของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="5b4bd-144">[![ตัวเลือกการดาวน์โหลด](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="5b4bd-145">บันทึกไปยังพีซีนี้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-145">Save to this PC</span></span>

<span data-ttu-id="5b4bd-146">คุณสามารถใช้แพคเกจการบันทึกเพื่อเล่นคู่มืองาน รักษาการบันทึก หรือแก้ไขคำอธิบายประกอบในการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="5b4bd-147">(ลักษณะการทำงานนี้ยังไม่ได้นำมาใช้ใน Retail Modern POS และ Cloud POS)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="5b4bd-148">ส่งออกเป็นเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="5b4bd-148">Export as Word document</span></span>

<span data-ttu-id="5b4bd-149">คุณสามารถบันทึกการบันทึกเป็นเอกสาร Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="5b4bd-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="5b4bd-150">เอกสารจะประกอบด้วยขั้นตอนที่บันทึกไว้และภาพหน้าจอที่รวบรวมไว้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="5b4bd-151">บันทึกเป็นการบันทึกของนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="5b4bd-151">Save as developer recording</span></span>

<span data-ttu-id="5b4bd-152">ไฟล์บันทึกดิบจะเป็นประโยชน์สำหรับการใช้ในสภาพแวดล้อมของผู้พัฒนา เช่น การสร้างโค้ดทดสอบ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="5b4bd-153">(ลักษณะการทำงานนี้ยังไม่ได้นำมาใช้)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="5b4bd-154">ตัวควบคุมการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-154">Recording controls</span></span>

<span data-ttu-id="5b4bd-155">[![ตัวควบคุมการบันทึก](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="5b4bd-156">หยุด</span><span class="sxs-lookup"><span data-stu-id="5b4bd-156">Stop</span></span>

<span data-ttu-id="5b4bd-157">คลิก **หยุด** เพื่อสิ้นสุดรอบเวลาการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="5b4bd-158">โปรดทราบว่าคุณไม่สามารถเริ่มต้นรอบเวลาหลังจากที่คุณสิ้นสุดรอบเวลานั้นแล้วได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="5b4bd-159">ดังนั้น ตรวจสอบให้แน่ใจว่าการบันทึกเสร็จสมบูรณ์แล้วก่อนที่คุณจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="5b4bd-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="5b4bd-160">หยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b4bd-160">Pause</span></span>

<span data-ttu-id="5b4bd-161">คลิก **หยุดชั่วคราว** เพื่อหยุด (หยุดชั่วคราว) รอบเวลาการบันทึกชั่วขณะ และดำเนินการต่อไป</span><span class="sxs-lookup"><span data-stu-id="5b4bd-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="5b4bd-162">ขั้นตอนที่คุณดำเนินการหลังจากที่คุณคลิก **หยุดชั่วคราว** จะไม่ถูกบันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="5b4bd-163">ดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-163">Continue</span></span>

<span data-ttu-id="5b4bd-164">เมื่อต้องการดำเนินการรอบเวลาการบันทึกต่อหลังจากที่คุณหยุดชั่วคราว คลิก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="5b4bd-165">จับภาพหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-165">Capture screenshots</span></span>

<span data-ttu-id="5b4bd-166">ตัวบันทึกงานสามารถจับภาพหน้าจอของ Retail Modern POS UI ขณะที่คุณบันทึกกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="5b4bd-167">เมื่อต้องการเปิดใช้งานคุณลักษณะการจับภาพหน้าจอ ตั้งค่าตัวเลือก **จับภาพหน้าจอ** เป็น **ใช่** และจากนั้นทำการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="5b4bd-168">หลังจากที่การบันทึกเสร็จสมบูรณ์ คลิก **หยุด** และดาวน์โหลดเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="5b4bd-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="5b4bd-169">เอกสารจะประกอบด้วยขั้นตอนต่างๆ ที่มีภาพหน้าจอที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5b4bd-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="5b4bd-170">ฟังก์ชันการจับภาพหน้าจอไม่ได้รับการสนับสนุนใน Cloud POS</span><span class="sxs-lookup"><span data-stu-id="5b4bd-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="5b4bd-171">เริ่มต้นงานและสิ้นสุดงาน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-171">Start task and End task</span></span>

<span data-ttu-id="5b4bd-172">คุณสามารถระบุจุดเริ่มต้นและจุดสิ้นสุดของชุดของขั้นตอนที่มีการจัดกลุ่มโดยการใช้ปุ่ม **เริ่มต้นงาน** และ **สิ้นสุด** **งาน**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="5b4bd-173">คลิก **เริ่มต้นงาน** เพื่อเพิ่มขั้นตอน "เริ่มต้นงาน" และจากนั้น ทำตามขั้นตอนที่ควรรวมไว้ในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="5b4bd-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="5b4bd-174">หลังจากที่คุณเสร็จสิ้นการดำเนินการขั้นตอนต่าง ๆ สำหรับกลุ่ม คลิก **สิ้นสุดงาน**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="5b4bd-175">งานช่วยให้คุณสามารถจัดระเบียบขั้นตอนต่าง ๆ ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="5b4bd-176">คุณสามารถซ้อนงานในงานอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="5b4bd-177">ด้วยวิธีนี้ คุณสามารถจัดระเบียบกระบวนการทางธุรกิจจำนวนมากและซับซ้อนได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b4bd-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="5b4bd-178">การเพิ่มคำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-178">Adding annotations</span></span>

<span data-ttu-id="5b4bd-179">คำอธิบายประกอบเป็นข้อความเพิ่มเติมที่คุณเพิ่มไปยังขั้นตอนในการบันทึก</span><span class="sxs-lookup"><span data-stu-id="5b4bd-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="5b4bd-180">ตัวอย่างเช่น คุณสามารถใช้คำอธิบายประกอบเพื่อให้บริบทหรือคำแนะนำเพิ่มเติมแก่ผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="5b4bd-181">คุณสามารถเพิ่มคำอธิบายประกอบก่อนหรือหลังขั้นตอนได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="5b4bd-182">คุณสามารถเพิ่มคำอธิบายประกอบสำหรับขั้นตอนใด ๆ ได้โดยการคลิกปุ่ม **แก้ไข** (สัญลักษณ์ดินสอ) ทางด้านขวาของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="5b4bd-183">[![ปุ่มแก้ไขสำหรับขั้นตอน](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="5b4bd-184">ข้อความและหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-184">Texts and notes</span></span>

<span data-ttu-id="5b4bd-185">คุณสามารถใช้ฟิลด์ **ข้อความ** และ **หมายเหตุ** เพื่อเพิ่มข้อความที่ควรจะเชื่อมโยงกับขั้นตอนในคู่มืองานได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="5b4bd-186">[![ฟิลด์ข้อความและหมายเหตุ](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="5b4bd-187">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-187">Text</span></span>

<span data-ttu-id="5b4bd-188">ข้อความที่คุณป้อนในฟิลด์ **ข้อความ** จะปรากฏขึ้น *เหนือ* ข้อความขั้นตอนในคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="5b4bd-189">ตำแหน่งที่ตั้งนี้เหมาะสมสำหรับข้อความที่คุณต้องการให้ผู้ใช้อ่านก่อนที่ผู้ใช้จะดำเนินขั้นตอนเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="5b4bd-189">This location is appropriate for text that you want the user to read before the user completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="5b4bd-190">บันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-190">Notes</span></span>

<span data-ttu-id="5b4bd-191">ข้อความที่คุณป้อนในฟิลด์ **หมายเหตุ** จะปรากฏขึ้น *ใต้* ข้อความขั้นตอนในคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="5b4bd-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="5b4bd-192">เมื่อต้องการอ่านข้อความหมายเหตุ ผู้ใช้ต้องขยายข้อความขั้นตอนในหน้าต่างป๊อปอัพ</span><span class="sxs-lookup"><span data-stu-id="5b4bd-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="5b4bd-193">ตำแหน่งที่ตั้งนี้เหมาะสมสำหรับเอกสารเพื่อนการอ่านที่ไม่จำเป็นหรือข้อมูลอื่น ๆ ที่อาจเป็นประโยชน์กับผู้ใช้ แต่ผู้ใช้ยังไม่จำเป็นต้องใช้เพื่อดำเนินการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="5b4bd-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="5b4bd-194">วิธีใช้ใน Retail Modern POS และ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="5b4bd-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="5b4bd-195">เพื่อแสดงการบันทึกงานแบบกำหนดเองของคุณเองในบานหน้าต่างวิธีใช้ของ Retail Modern POS และ Cloud POS เพื่อให้สามารถดูเป็นข้อความได้ คุณต้องบันทึกการบันทึกงานของคุณไปยังไลบรารี BPM ของคุณเอง และจากนั้น ปรับปรุงพารามิเตอร์ระบบวิธีใช้ของคุณเพื่อชี้ไปยังไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="5b4bd-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="5b4bd-196">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การติดต่อระบบช่วยเหลือ](../fin-ops-core/fin-ops/get-started/help-connect.md)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-196">For more information, see [Connecting the Help system](../fin-ops-core/fin-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="5b4bd-197">Retail Modern POS และวิธีใช้ของ Cloud POS ค้นหา LCS ในเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="5b4bd-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="5b4bd-198">โดยจะค้นหาในไลบรารี BPM ทั้งหมดที่เลือกไว้ในพารามิเตอร์ระบบวิธีใช้ Commerce และแสดงผลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5b4bd-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="5b4bd-199">เมื่อต้องการเข้าถึงเมนู **วิธีใช้** คลิกปุ่ม **วิธีใช้** (เครื่องหมายคำถาม) ที่ด้านบนของหน้าจอ และจากนั้น ในกล่องค้นหา ให้พิมพ์ชื่อกระบวนการของคุณ และกดปุ่มค้นหา</span><span class="sxs-lookup"><span data-stu-id="5b4bd-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="5b4bd-200">[![ปุ่มวิธีใช้](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="5b4bd-201">เมื่อคุณคลิกคู่มืองานในผลการค้นหา คุณสามารถดูขั้นตอนเป็นหัวข้อวิธีใช้หรือขั้นตอนการส่งออกไปยังเอกสาร Word ได้</span><span class="sxs-lookup"><span data-stu-id="5b4bd-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="5b4bd-202">วิธีใช้ใน Retail Modern POS และ Cloud POS จะไม่เรียกคู่มืองานตามแบบฟอร์มที่คุณกำลังทำหรือการดำเนินงานที่คุณกำลังทำอยู่</span><span class="sxs-lookup"><span data-stu-id="5b4bd-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="5b4bd-203">คุณต้องพิมพ์ชื่อกระบวนการในกล่องค้นหา และคลิก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="5b4bd-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]