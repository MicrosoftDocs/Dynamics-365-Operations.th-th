---
title: การวางแผนงบประมาณ
description: วัตถุประสงค์ของแล็บนี้ คือการให้มุมมองที่แนะนำของการปรับปรุงฟังก์ชัน Microsoft Dynamics 365 Finance ในพื้นที่การวางแผนงบประมาณ จุดประสงค์ของห้องปฏิบัติการนี้คือแสดงตัวอย่างการตั้งค่าคอนฟิกด่วนของโมดูลการวางแผนงบประมาณ และแสดงวิธีวางแผนงบประมาณให้สำเร็จโดยใช้การตั้งค่าคอนฟิกนี้
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9558013236a728e0fb9691f4edd719fe58d5457
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448540"
---
# <a name="budget-planning"></a><span data-ttu-id="9d0cb-104">การวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-104">Budget planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d0cb-105">วัตถุประสงค์ของแล็บนี้ คือการให้มุมมองที่แนะนำของการปรับปรุงฟังก์ชัน Microsoft Dynamics 365 Finance ในพื้นที่การวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-105">The objective of this lab is to provide a guided view of Microsoft Dynamics 365 Finance functionality updates in Budget planning area.</span></span> <span data-ttu-id="9d0cb-106">จุดประสงค์ของห้องปฏิบัติการนี้คือแสดงตัวอย่างการตั้งค่าคอนฟิกด่วนของโมดูลการวางแผนงบประมาณ และแสดงวิธีวางแผนงบประมาณให้สำเร็จโดยใช้การตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-106">The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration.</span></span>  <span data-ttu-id="9d0cb-107">ห้องปฏิบัติการนี้จะโฟกัสเป็นพิเศษในกระบวนการทางธุรกิจหรืองานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d0cb-107">This lab will focus specifically on the following business processes or tasks:</span></span>
- <span data-ttu-id="9d0cb-108">การสร้างลำดับชั้นขององค์กรสำหรับการวางแผนงบประมาณ และการตั้งค่าคอนฟิกความปลอดภัยของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-108">Creating organizational hierarchy for budget planning and configuring user security</span></span>
- <span data-ttu-id="9d0cb-109">การกำหนดสถานการณ์จำลองแผนงบประมาณ คอลัมน์แผนงบประมาณ โครงร่าง และเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="9d0cb-109">Defining budget plan scenarios, budget plan columns, layouts and Excel templates</span></span>
- <span data-ttu-id="9d0cb-110">การสร้างและการเรียกใช้กระบวนการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-110">Creating and activating budget planning process</span></span>
- <span data-ttu-id="9d0cb-111">การสร้างเอกสารแผนงบประมาณโดยการดึงค่าจริงจากบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9d0cb-111">Creating budget plan document by pulling in actuals from General ledger</span></span>
- <span data-ttu-id="9d0cb-112">การใช้การปันส่วนเพื่อปรับปรุงข้อมูลเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-112">Using allocations to adjust budget plan document data</span></span>
- <span data-ttu-id="9d0cb-113">การแก้ไขข้อมูลเอกสารแผนงบประมาณใน Excel</span><span class="sxs-lookup"><span data-stu-id="9d0cb-113">Editing budget plan document data in Excel</span></span> 

<a name="prerequisites"></a><span data-ttu-id="9d0cb-114">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9d0cb-114">Prerequisites</span></span> 
------------------

<span data-ttu-id="9d0cb-115">สำหรับบทสอนนี้ คุณจะต้องเข้าถึงสภาพแวดล้อม Microsoft Dynamics 365 Finance ด้วยข้อมูลสาธิต Contoso และเตรียมใช้งานในฐานะผู้ดูแลบนอินสแตนซ์</span><span class="sxs-lookup"><span data-stu-id="9d0cb-115">For this tutorial, you’ll need to access the Microsoft Dynamics 365 Finance environment with Contoso demo data, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="9d0cb-116">อย่าใช้โหมดเบราเซอร์ส่วนตัวสำหรับห้องปฏิบัติการนี้ - ลงชื่อออกจากบัญชีอื่น ๆ ในเบราเซอร์ถ้าจำเป็น และลงชื่อเข้าใช้ ด้วยข้อมูลประจำตัวของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-116">Do not use In Private browser mode for this lab - sign out from any other account in the browser if needed and sign in with administrator credentials.</span></span> <span data-ttu-id="9d0cb-117">เมื่อลงชื่อเข้าใช้ คุณ **ต้อง** กาเครื่องหมายที่กล่องกาเครื่องหมาย "ให้ฉันลงชื่อเข้าใช้เสมอ"</span><span class="sxs-lookup"><span data-stu-id="9d0cb-117">When signing in, you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="9d0cb-118">วิธีนี้สร้างคุกกี้ถาวรที่แอพลิเคชัน Excel ต้องการ ณ ขณะนี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-118">This creates a persistent cookie that the Excel App currently needs.</span></span> <span data-ttu-id="9d0cb-119">หากคุณเข้าสู่ระบบแอพลิเคชัน โดยใช้เบราเซอร์อื่นนอกเหนือจาก IE คุณจะได้รับพร้อมต์ให้เข้าสู่ระบบภายในแอพ Excel</span><span class="sxs-lookup"><span data-stu-id="9d0cb-119">If you sign in to the application using a browser other than IE, then you’ll be prompted to sign in within the Excel App.</span></span> <span data-ttu-id="9d0cb-120">เมื่อคุณคลิก "ลงชื่อเข้าใช้" ในแอพ Excel หน้าต่างป๊อปอัพ IE จะเปิดและขณะที่คุณกำลังลงชื่อ คุณ **ต้อง** กาเครื่องหมายที่กล่องกาเครื่องหมาย "ให้ฉันลงชื่อเข้าใช้เสมอ"</span><span class="sxs-lookup"><span data-stu-id="9d0cb-120">When you click “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” check box.</span></span> <span data-ttu-id="9d0cb-121">ถ้าคลิก "ลงชื่อข้าใช้" ในแอพลิเคชัน Excel ไม่ดำเนินการใดๆ คุณควรล้างแคชคุกกี้ IE</span><span class="sxs-lookup"><span data-stu-id="9d0cb-121">If clicking “Sign in” in the Excel App doesn’t appear to do anything then you should clear the IE cookie cache.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="9d0cb-122">**ภาพรวมของสถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="9d0cb-122">**Scenario overview**</span></span>
<span data-ttu-id="9d0cb-123">จูเลียทำงานเป็นผู้จัดการฝ่ายการเงินในระบบความบันเทิง Contoso ในเยอรมนี (DEMF)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-123">Julia works as a finance manager in Contoso Entertainment Systems in Germany (DEMF).</span></span> <span data-ttu-id="9d0cb-124">เมื่อ FY2016 ใกล้ถึง เธอจำเป็นต้องทำงานในการตั้งค่างบประมาณของบริษัทสำหรับปีกำลังมาถึง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-124">As FY2016 approaches, she needs to work on setting up the company’s budget for the upcoming year.</span></span> <span data-ttu-id="9d0cb-125">การจัดเตรียมงบประมาณมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="9d0cb-125">Budget preparation looks as follows:</span></span>

1.  <span data-ttu-id="9d0cb-126">Julia ใช้ยอดเงินที่เกิดขึ้นจริงของปีก่อนหน้านี้เป็นจุดเริ่มต้นเพื่อสร้างงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-126">Julia uses previous year actuals amounts as a starting point to create the budget.</span></span>
2.  <span data-ttu-id="9d0cb-127">ตามยอดจริงในปีก่อนหน้า เธอสร้างการประเมิน 12 เดือน สำหรับปีกำลังมาถึง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-127">Based on the previous year actuals, she creates estimates for 12 months in the upcoming year</span></span>
3.  <span data-ttu-id="9d0cb-128">Julia ตรวจทานงบประมาณที่ ด้วย CFO</span><span class="sxs-lookup"><span data-stu-id="9d0cb-128">Julia reviews the budget with CFO.</span></span> <span data-ttu-id="9d0cb-129">เมื่อเสร็จเรียบร้อย เธอทำการปรับปรุงเท่าที่จำเป็นสำหรับแผนงบประมาณ และ ดำเนินการจัดเตรียมงบประมาณประจำปีขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="9d0cb-129">Once done she makes necessary adjustments for the budget plan and finalizes budget preparation.</span></span>

<span data-ttu-id="9d0cb-130">เค้าร่างการตั้งค่าคอนฟิกการวางแผนงบประมาณสำหรับสถานการณ์จำลองมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="9d0cb-130">Budget planning configuration schema for the scenario looks as follows:</span></span>

![เค้าร่างการกำหนดค่าการวางแผนงบประมาณ](./media/screenshot1-300x152.png)

<span data-ttu-id="9d0cb-132">Julia ใช้เท็มเพลต Excel ต่อไปนี้ในการจัดเตรียมงบประมาณ:</span><span class="sxs-lookup"><span data-stu-id="9d0cb-132">Julia uses the following Excel template to prepare the budget:</span></span>

<span data-ttu-id="9d0cb-133">[![เท็มเพลต Excel](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-133">[![Excel template](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span></span>

## <a name="exercise-1-configuration"></a><span data-ttu-id="9d0cb-134">แบบฝึกหัดที่ 1: ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="9d0cb-134">Exercise 1: Configuration</span></span>

### <a name="task-1-create-organizational-hierarchy"></a><span data-ttu-id="9d0cb-135">**งานที่ 1: สร้างลำดับชั้นองค์กร**</span><span class="sxs-lookup"><span data-stu-id="9d0cb-135">**Task 1: Create organizational hierarchy**</span></span>
<span data-ttu-id="9d0cb-136">เมื่อกระบวนการจัดทำงบประมาณทั้งหมดเกิดขึ้นในแผนกการเงิน ดังนั้น Julia จึงจำเป็นต้องสร้างลำดับชั้นองค์กรที่เรียบง่ายมากๆ – ประกอบด้วยแผนกการเงินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9d0cb-136">As all the budgeting process happens in the Finance department, therefore Julia needs to create a very simple organizational hierarchy – consisting of Finance department only.</span></span> 

<span data-ttu-id="9d0cb-137">1.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-137">1.1.</span></span> <span data-ttu-id="9d0cb-138">นำไปยังลำดับชั้นขององค์กร (การจัดการองค์กร &gt; องค์กร &gt; ลำดับชั้นขององค์กร) และคลิกปุ่ม ใหม่</span><span class="sxs-lookup"><span data-stu-id="9d0cb-138">Navigate to Organization hierarchies (Organization administration &gt; Organizations &gt; Organization hierarchies) and click the New button.</span></span>

![ลำดับชั้นขององค์กร](./media/screenshot3.png) 

<span data-ttu-id="9d0cb-140">1.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-140">1.2.</span></span> <span data-ttu-id="9d0cb-141">พิมพ์ชื่อสำหรับลำดับชั้นขององค์กรในกล่อง ชื่อ แล้วคลิกปุ่มกำหนดวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="9d0cb-141">Type the name for the organizational hierarchy in the Name box and click Assign purpose.</span></span>

<span data-ttu-id="9d0cb-142">1.3</span><span class="sxs-lookup"><span data-stu-id="9d0cb-142">1.3.</span></span> <span data-ttu-id="9d0cb-143">เลือกวัตถุประสงค์ในการวางแผนงบประมาณ คลิกปุ่ม เพิ่ม และกำหนดลำดับชั้นขององค์กรที่สร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="9d0cb-143">Select the Budget planning purpsose, click Add, and assign the newly created organizational hierarchy.</span></span> 

<span data-ttu-id="9d0cb-144">[![กำหนดวัตถุประสงค์](./media/screenshot5.png)](./media/screenshot5.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-144">[![Assign purpose](./media/screenshot5.png)](./media/screenshot5.png)</span></span>

<span data-ttu-id="9d0cb-145">1.4</span><span class="sxs-lookup"><span data-stu-id="9d0cb-145">1.4.</span></span> <span data-ttu-id="9d0cb-146">ทำซ้ำขั้นตอนข้างต้นสำหรับวัตถุประสงค์ด้านความปลอดภัยขององค์กร</span><span class="sxs-lookup"><span data-stu-id="9d0cb-146">Repeat the step above for the Security organizational purpose.</span></span> <span data-ttu-id="9d0cb-147">ปิดแบบฟอร์ม เมื่อเสร้จสิ้น</span><span class="sxs-lookup"><span data-stu-id="9d0cb-147">Close the form when done.</span></span>

<span data-ttu-id="9d0cb-148">1.5</span><span class="sxs-lookup"><span data-stu-id="9d0cb-148">1.5.</span></span> <span data-ttu-id="9d0cb-149">ในฟอร์มลำดับชั้นขององค์กร คลิกปุ่ม มุมมอง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-149">In the Organizational Hierarchies form, click View.</span></span> <span data-ttu-id="9d0cb-150">คลิก แก้ไข ในโปรแกรมออกแบบลำดับชั้น และสร้างลำดับชั้น โดยการคลิกปุ่ม แทรก</span><span class="sxs-lookup"><span data-stu-id="9d0cb-150">Click Edit in the Hierarchy designer, and create a hierarchy by clicking Insert.</span></span>

<span data-ttu-id="9d0cb-151">[![แทรก](./media/screenshot7.png)](./media/screenshot7.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-151">[![Insert](./media/screenshot7.png)](./media/screenshot7.png)</span></span> 

<span data-ttu-id="9d0cb-152">1.6</span><span class="sxs-lookup"><span data-stu-id="9d0cb-152">1.6.</span></span> <span data-ttu-id="9d0cb-153">เลือกแผนกการเงินสำหรับลำดับชั้นการจัดทำงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-153">Select Finance department for the budgeting hierarchy.</span></span> 

<span data-ttu-id="9d0cb-154">[![การเงิน](./media/screenshot8.png)](./media/screenshot8.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-154">[![Finance](./media/screenshot8.png)](./media/screenshot8.png)</span></span>

<span data-ttu-id="9d0cb-155">1.7</span><span class="sxs-lookup"><span data-stu-id="9d0cb-155">1.7.</span></span> <span data-ttu-id="9d0cb-156">เมื่อทำเสร็จแล้ว ให้คลิกปุ่ม เผยแพร่ และ ปิด</span><span class="sxs-lookup"><span data-stu-id="9d0cb-156">When done, click Publish and Close.</span></span> <span data-ttu-id="9d0cb-157">เลือกวันที่ 1 มกราคม 2015 เป็นวันที่มีผลบังคับใช้ สำหรับการเผยแพร่ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="9d0cb-157">Select 1/1/2015 as the effective date for hierarchy publishing.</span></span>

<span data-ttu-id="9d0cb-158">[![วันที่มีผลบังคับใช้](./media/screenshot9.png)](./media/screenshot9.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-158">[![Effective date](./media/screenshot9.png)](./media/screenshot9.png)</span></span>

### <a name="task-2-configure-user-security"></a><span data-ttu-id="9d0cb-159">งานที่ 2: ตั้งค่าคอนฟิกความปลอดภัยของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-159">Task 2: Configure user security</span></span>
<span data-ttu-id="9d0cb-160">การวางแผนงบประมาณใช้นโยบายความปลอดภัยพิเศษเพื่อกำหนดค่าคอนฟิกให้กับข้อมูลแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-160">Budget planning uses special security policies to configure access to budget plans data.</span></span> <span data-ttu-id="9d0cb-161">จูเลียจำเป็นต้องให้สิทธิ์ในการเข้าถึงแผนงบประมาณทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9d0cb-161">Julia needs to give access to Finance budget plans for herself.</span></span> 

<span data-ttu-id="9d0cb-162">2.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-162">2.1.</span></span> <span data-ttu-id="9d0cb-163">สลับไปที่บริบทของนิติบุคคล DEMF</span><span class="sxs-lookup"><span data-stu-id="9d0cb-163">Switch to DEMF legal entity context.</span></span> 


<span data-ttu-id="9d0cb-164">2.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-164">2.2.</span></span> <span data-ttu-id="9d0cb-165">นำทางไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-165">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="9d0cb-166">ในแท็บพารามิเตอร์ ตั้งค่าแบบจำลองความปลอดภัย ตามองค์กรความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="9d0cb-166">In the Parameters tab, set the Security model value to Based on security organizations.</span></span> 

<span data-ttu-id="9d0cb-167">[![พารามิเตอร์](./media/screenshot11.png)](./media/screenshot11.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-167">[![Parameters](./media/screenshot11.png)](./media/screenshot11.png)</span></span> 

<span data-ttu-id="9d0cb-168">2.3</span><span class="sxs-lookup"><span data-stu-id="9d0cb-168">2.3.</span></span> <span data-ttu-id="9d0cb-169">ไปยังการดูแลระบบ &gt; ผู้ใช้ &gt; ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-169">Navigate to System administration &gt; Users &gt; Users.</span></span> <span data-ttu-id="9d0cb-170">กำหนดบทบาทผู้จัดการงบประมาณการบริหารให้แก่ผู้ใช้ที่ดูแลระบบ (Julia Funderburk)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-170">Give user Admin (Julia Funderburk) Budget manager role.</span></span> 

<span data-ttu-id="9d0cb-171">[![ผู้จัดการงบประมาณ](./media/screenshot12.png)](./media/screenshot12.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-171">[![Budget manager](./media/screenshot12.png)](./media/screenshot12.png)</span></span> 

<span data-ttu-id="9d0cb-172">2.4</span><span class="sxs-lookup"><span data-stu-id="9d0cb-172">2.4.</span></span> <span data-ttu-id="9d0cb-173">เลือกบทบาทผู้ใช้ แล้วคลิกกำหนดองค์กร</span><span class="sxs-lookup"><span data-stu-id="9d0cb-173">Pick user role and click Assign organizations.</span></span> 

<span data-ttu-id="9d0cb-174">[![กำหนดองค์กร](./media/screenshot13.png)](./media/screenshot13.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-174">[![Assign organizations](./media/screenshot13.png)](./media/screenshot13.png)</span></span>

<span data-ttu-id="9d0cb-175">2.5</span><span class="sxs-lookup"><span data-stu-id="9d0cb-175">2.5.</span></span> <span data-ttu-id="9d0cb-176">เลือก "อนุญาตให้เข้าถึงองค์กรที่ระบุ"</span><span class="sxs-lookup"><span data-stu-id="9d0cb-176">Select “Grant access to specific organizations”.</span></span> <span data-ttu-id="9d0cb-177">เลือกลำดับชั้นขององค์กรที่สร้างขึ้นในขั้นตอนแรก</span><span class="sxs-lookup"><span data-stu-id="9d0cb-177">Pick the Organizational hierarchy created in the first step.</span></span> <span data-ttu-id="9d0cb-178">เลือกโหนดการเงิน แล้วคลิกเงินช่วยเหลือ ด้วยปุ่มรอง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-178">Pick Finance node, and click the Grant with children button.</span></span> 

<span data-ttu-id="9d0cb-179">***ข้อสำคัญ!***</span><span class="sxs-lookup"><span data-stu-id="9d0cb-179">***Important!***</span></span> <span data-ttu-id="9d0cb-180">*ตรวจสอบให้แน่ใจว่าว่าคุณอยู่ในบริบทนิติบุคคล DEMF ขณะดำเนินการกับงานนี้ เมื่อได้ใช้ความปลอดภัยขององค์กรสำหรับแต่ละนิติบุคคล*</span><span class="sxs-lookup"><span data-stu-id="9d0cb-180">*Make sure you are in DEMF legal entity context when performing this task, as Organizational security is applied per legal entity*</span></span> 

### <a name="task-3-create-scenarios"></a><span data-ttu-id="9d0cb-181">งานที่ 3: สร้างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-181">Task 3: Create scenarios</span></span>
<span data-ttu-id="9d0cb-182">3.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-182">3.1.</span></span> <span data-ttu-id="9d0cb-183">นำทางไปยังการจัดทำงบประมาณ&gt;การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-183">Navigate to Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="9d0cb-184">ในหน้าสถานการณ์จำลองสังเกตสถานการณ์เรากำลังจะใช้ห้องปฏิบัติการนี้เพิ่มเติม: ยอดที่เกิดขึ้นจริงและงบประมาณปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-184">In the Scenarios page note the scenarios we are going to use further in this lab: Previous year actuals and Budgeted.</span></span> 

<span data-ttu-id="9d0cb-185">*หมายเหตุ: คุณสามารถสร้างสถานการณ์จำลองใหม่สำหรับแบบฝึกหัดนี้ ตามประสงค์และ และใช้เหล่านั้นแทน*</span><span class="sxs-lookup"><span data-stu-id="9d0cb-185">*Note: You can create new scenarios for this exercise if desired and use those instead.*</span></span> 

<span data-ttu-id="9d0cb-186">[![สถานการณ์จำลองใหม่](./media/screenshot15.png)](./media/screenshot15.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-186">[![New scenarios](./media/screenshot15.png)](./media/screenshot15.png)</span></span> 

<span data-ttu-id="9d0cb-187">*หมายเหตุ: Julia ไม่ได้ใช้กระบวนการอนุมัติอย่างเป็นทางการสำหรับการจัดเตรียมงบประมาณ เราจะข้ามลำดับงาน ขั้น และตั้งค่าขั้นตอนลำดับงานในห้องปฏิบัติการนี้ และจะใช้การตั้งค่าที่มีอยู่สำหรับการลำดับงานอนุมัติอัตโนมัติ โปรดดูภาคผนวกสำหรับการตั้งค่าคอนฟิกลำดับงานนี้*</span><span class="sxs-lookup"><span data-stu-id="9d0cb-187">*Note: as Julia is not using formal approval process for budget preparation, we will skip Workflows, Stages and Workflow stages setup in this lab and will use existing setup for Auto – approve workflow. See appendix for this workflow configuration.*</span></span>

### <a name="task-4-create-budget-plan-columns"></a><span data-ttu-id="9d0cb-188">งานที่ 4: สร้างคอลัมน์แผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-188">Task 4: Create budget plan columns</span></span>
<span data-ttu-id="9d0cb-189">แผนงบประมาณที่มีคอลัมน์ยอดเงินหรือปริมาณตามคอลัมน์ที่สามารถใช้ในโครงร่างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-189">Budget plan columns are either Monetary or quantity based columns that can be used in budget plan document layout.</span></span> <span data-ttu-id="9d0cb-190">ในตัวอย่างของเรา เราต้องสร้างคอลัมน์สำหรับค่าจริงของปีก่อนหน้านี้และ คอลัมน์ 12 คอลัมน์เพื่อแสดงยอดแต่ละเดือนในปีงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-190">In our example we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year.</span></span> <span data-ttu-id="9d0cb-191">คอลัมน์สามารถสร้างได้ โดยการคลิกปุ่มเพิ่ม และการกรอกมูลค่า หรือโดยการใช้ของเอนทิตี้ข้อมูลก็ได้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-191">Columns can be created either by simply clicking Add button and filling in the values, or with a help of Data entity.</span></span> <span data-ttu-id="9d0cb-192">ในห้องปฏิบัติการนี้ เราจะใช้เอนทิตีข้อมูลเพื่อเติมค่า</span><span class="sxs-lookup"><span data-stu-id="9d0cb-192">In this lab we will use Data entity to fill in the values.</span></span> 

<span data-ttu-id="9d0cb-193">4.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-193">4.1.</span></span> <span data-ttu-id="9d0cb-194">ในการจัดงบประมาณ&gt;ตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ เปิดหน้าคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="9d0cb-194">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration, open the Columns page.</span></span> <span data-ttu-id="9d0cb-195">คลิกปุ่ม Office มุมบนขวาของฟอร์ม และเลือกคอลัมน์ (ยังไม่ได้กรอง)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-195">Click the Office button on the top right corner of the form, and pick Columns (unfiltered).</span></span> 

<span data-ttu-id="9d0cb-196">[![คอลัมน์ที่ยังไม่ได้กรอง](./media/screenshot16.png)](./media/screenshot16.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-196">[![Columns unfiltered](./media/screenshot16.png)](./media/screenshot16.png)</span></span> 

<span data-ttu-id="9d0cb-197">4.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-197">4.2.</span></span> <span data-ttu-id="9d0cb-198">ระบบจะเปิดสมุดงาน Excel ที่จะใช้สำหรับการเติมค่า</span><span class="sxs-lookup"><span data-stu-id="9d0cb-198">The system will open an Excel workbook to be used for filling in the values.</span></span> <span data-ttu-id="9d0cb-199">ถ้าได้รับพร้อมท์ ให้คลิกเปิดใช้งานการแก้ไขและเชื่อถือแอปนี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-199">If prompted, click Enable Editing and Trust this app.</span></span> 

<span data-ttu-id="9d0cb-200">4.3</span><span class="sxs-lookup"><span data-stu-id="9d0cb-200">4.3.</span></span> <span data-ttu-id="9d0cb-201">เราจะต้องการคอลัมน์เพิ่มเติมเพื่อเติมค่า</span><span class="sxs-lookup"><span data-stu-id="9d0cb-201">We will need more columns to fill the values in.</span></span> <span data-ttu-id="9d0cb-202">คลิก การออกแบบในบานหน้าต่างด้านขวา เพื่อเพิ่มคอลัมน์ลงในกริด</span><span class="sxs-lookup"><span data-stu-id="9d0cb-202">Click Design on the right side pane to add the columns to the grid.</span></span> 

<span data-ttu-id="9d0cb-203">[![การออกแบบ](./media/screenshot19.png)](./media/screenshot19.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-203">[![Design](./media/screenshot19.png)](./media/screenshot19.png)</span></span> 

<span data-ttu-id="9d0cb-204">4.4</span><span class="sxs-lookup"><span data-stu-id="9d0cb-204">4.4.</span></span> <span data-ttu-id="9d0cb-205">คลิก ปุ่มดินสอถัดจาก PlanColumns เพื่อดูคอลัมน์ที่มีอยู่ เพื่อเพิ่มลงในกริด</span><span class="sxs-lookup"><span data-stu-id="9d0cb-205">Click the pencil button next to PlanColumns to see available columns to add to the grid.</span></span> 

<span data-ttu-id="9d0cb-206">[![แก้ไข](./media/screenshot20.png)](./media/screenshot20.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-206">[![Edit](./media/screenshot20.png)](./media/screenshot20.png)</span></span> 

<span data-ttu-id="9d0cb-207">4.5</span><span class="sxs-lookup"><span data-stu-id="9d0cb-207">4.5.</span></span> <span data-ttu-id="9d0cb-208">ดับเบิลคลิกในแต่ละฟิลด์ที่พร้อมใช้งาน เพื่อเพิ่มไปยังฟิลด์ที่เลือก และคลิก อัพเดต</span><span class="sxs-lookup"><span data-stu-id="9d0cb-208">Double click on each available field to add them to Selected fields, and click Update.</span></span> 

<span data-ttu-id="9d0cb-209">4.6</span><span class="sxs-lookup"><span data-stu-id="9d0cb-209">4.6.</span></span> <span data-ttu-id="9d0cb-210">ในตาราง Excel ให้เพิ่มคอลัมน์ทั้งหมดที่จำเป็นที่ต้องสร้าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-210">In the Excel table, add all the columns that need to be created.</span></span> <span data-ttu-id="9d0cb-211">ใช้คุณลักษณะการเติมอัตโนมัติใน Excel เพื่อเพิ่มบรรทัดอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="9d0cb-211">Use the AutoFill feature in Excel to add the lines quickly.</span></span> <span data-ttu-id="9d0cb-212">ตรวจสอบให้แน่ใจว่า ได้เพิ่มบรรทัดที่เป็นส่วนหนึ่งของตาราง (เมื่อใช้เลื่อนแนวตั้ง คุณควรจะสามารถมองเห็นส่วนหัวของคอลัมน์ที่ด้านบนของกริด)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-212">Make sure the lines are added as a part of the table (when using vertical scroll, you should be able to see column headers on the top of the grid).</span></span> 

<span data-ttu-id="9d0cb-213">4.7</span><span class="sxs-lookup"><span data-stu-id="9d0cb-213">4.7.</span></span> <span data-ttu-id="9d0cb-214">ย้อนกลับไปยังโปรแกรมประยุกต์ และรีเฟรชเพจ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-214">Return to the application, and refresh the page.</span></span> <span data-ttu-id="9d0cb-215">ค่าที่เผยแพร่จะปรากฏ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-215">Published values will appear.</span></span> 

<span data-ttu-id="9d0cb-216">[![รีเฟรช](./media/screenshot23.png)](./media/screenshot23.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-216">[![Refresh](./media/screenshot23.png)](./media/screenshot23.png)</span></span>

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a><span data-ttu-id="9d0cb-217">งานที่ 5: สร้างแม่แบบและโครงร่างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-217">Task 5: Create budget plan document layouts and templates</span></span>
<span data-ttu-id="9d0cb-218">โครงร่างกำหนดวิธีตารางบรรทัดเอกสารของแผนงบประมาณที่จะดูคล้ายกันเมื่อผู้ใช้เปิดเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-218">Layout defines how budget plan document lines grid is going to look like when user opens budget plan document.</span></span> <span data-ttu-id="9d0cb-219">จึงจะสามารถสลับโครงร่างสำหรับเอกสารแผนงบประมาณเมื่อต้องการดูข้อมูลเดียวกันในมุมที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="9d0cb-219">It is also possible to switch the layout for budget plan document to see the same data in different angles.</span></span> <span data-ttu-id="9d0cb-220">ตอนนี้ ขณะเธอยังได้รับคอลัมน์ที่กำหนดไว้เพื่อใช้กับเอกสารแผนงบประมาณของเรา Julia จำเป็นต้องสร้างโครงร่างเอกสารแผนงบประมาณ ที่มีลักษณะคล้ายกับตาราง Excel เธอใช้ในการสร้างข้อมูลงบประมาณ (ดูภาพรวมของส่วนสถานการณ์จำลองในห้องปฏิบัติการนี้)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-220">Now, as she’s got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data (see section Scenario overview in this lab)</span></span> 

<span data-ttu-id="9d0cb-221">5.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-221">5.1.</span></span> <span data-ttu-id="9d0cb-222">ใน การจัดงบประมาณ&gt;ตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ เปิดหน้าโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-222">In the Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration, open the Layouts page.</span></span> <span data-ttu-id="9d0cb-223">สร้างโครงร่างใหม่สำหรับรายการบัญชีงบประมาณรายเดือน:</span><span class="sxs-lookup"><span data-stu-id="9d0cb-223">Create a new layout for Monthly budget entry:</span></span>

-   <span data-ttu-id="9d0cb-224">เลือกเซ็ตมิติ MA+BU ที่จะรวมบัญชีหลักและหน่วยธุรกิจจนถึงโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-224">Pick MA+BU dimension set to include Main accounts and Business units to the layout.</span></span>
-   <span data-ttu-id="9d0cb-225">แสดงรายการคอลัมน์แผนงบประมาณทั้งหมดที่สร้างขึ้นในขั้นตอนก่อนหน้านี้ในส่วนขององค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-225">List all budget plan columns created in the previous step in the Elements section.</span></span> <span data-ttu-id="9d0cb-226">สร้างทั้งหมดแต่ก่อนหน้าปีที่เกิดขึ้นจริงสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-226">Make all but Previous year actuals editable.</span></span>
-   <span data-ttu-id="9d0cb-227">คลิกปุ่มคำอธิบายเกี่ยวกับการเลือกมิติทางการเงินที่ควรแสดงคำอธิบายในกริด</span><span class="sxs-lookup"><span data-stu-id="9d0cb-227">Click Descriptions button to select which financial dimensions should display Descriptions in the grid.</span></span>

<span data-ttu-id="9d0cb-228">[![คำอธิบาย](./media/screenshot24.png)](./media/screenshot24.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-228">[![Descriptions](./media/screenshot24.png)](./media/screenshot24.png)</span></span> 

<span data-ttu-id="9d0cb-229">ยึดตามงบประมาณของแผนคำนิยามโครงร่างที่เราสามารถสร้างเท็มเพลต Excel เพื่อใช้เป็นทางเลือกที่จะแก้ไขข้อมูลงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-229">Based on the budget plan layout definition we can create an Excel template to be used as an alternative way to edit Budget data.</span></span> <span data-ttu-id="9d0cb-230">ตามที่มีเท็มเพลต Excel เพื่อให้ตรงกับคำนิยามโครงร่างของแผนงบประมาณ คุณจะไม่สามารถแก้ไขโครงร่างของแผนงบประมาณหลังจากการสร้างเท็มเพลต Excel ดังนั้น งานนี้ควรทำหลังจากที่มีกำหนดส่วนประกอบทั้งหมดของโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-230">As Excel template has to match budget plan layout definition, you won’t be able to edit budget plan layout after generating Excel template, therefore this task should be done after all layout components are defined.</span></span> 

<span data-ttu-id="9d0cb-231">5.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-231">5.2.</span></span> <span data-ttu-id="9d0cb-232">สำหรับโครงร่างที่สร้างใน 5.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-232">For the layout created in the 5.1.</span></span> <span data-ttu-id="9d0cb-233">ขั้นตอน คลิกปุ่มเท็มเพลต &gt; สร้าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-233">step, click button Template &gt; Generate.</span></span> <span data-ttu-id="9d0cb-234">ยืนยันข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="9d0cb-234">Confirm the warning message.</span></span> <span data-ttu-id="9d0cb-235">เพื่อดูเท็มเพลต คลิกเท็มเพลต &gt; มุมมอง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-235">To view the template, click Template &gt; View.</span></span> 

<span data-ttu-id="9d0cb-236">*หมายเหตุ: ตรวจสอบให้แน่ใจว่าได้เลือก "บันทึกเป็น" แล้วเลือกตำแหน่งที่จะจัดเก็บเท็มเพลตเพื่อที่จะแก้ไข ถ้าผู้ใช้เลือก "เปิด" ในกล่องโต้ตอบโดยไม่ได้บันทึก การเปลี่ยนแปลงไฟล์นั้นจะไม่ถูกเก็บไว้เมื่อไฟล์ถูกปิด* 
[![มุมมองเท็มเพลต](./media/screenshot25.png)](./media/screenshot25.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-236">*Note: Make sure to select “Save as” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png)</span></span> 

<span data-ttu-id="9d0cb-237">5.3</span><span class="sxs-lookup"><span data-stu-id="9d0cb-237">5.3.</span></span> <span data-ttu-id="9d0cb-238">&lt; ขั้นตอนเพิ่มเติม&gt; ปรับเปลี่ยนเท็มเพลต Excel เพื่อทำให้ผู้ใช้ใช้งานได้ง่ายขึ้น – เพิ่มสูตรรวม ฟิลด์หัวข้อ การจัดรูปแบบ เป็นต้น บันทึกการเปลี่ยนแปลง และอัพโหลดไฟล์ไปยังโครงร่างของแผนงบประมาณ โดยคลิกที่โครงร่าง &gt; อัพโหลด</span><span class="sxs-lookup"><span data-stu-id="9d0cb-238">&lt; Optional step&gt; Modify Excel template to make it look more user friendly – add total formulas, header fields, formatting, etc. Save the changes and upload the file to budget plan layout by clicking Layout &gt; Upload.</span></span> 


### <a name="task-6-create-a-budget-planning-process"></a><span data-ttu-id="9d0cb-239">งานที่ 6: สร้างกระบวนการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-239">Task 6: Create a budget planning process</span></span>
<span data-ttu-id="9d0cb-240">Julia จำเป็นต้องสร้าง และเรียกใช้กระบวนการวางแผนงบประมาณใหม่รวมกับการตั้งค่าข้างต้นเพื่อเริ่มป้อนการวางแผนงบประมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="9d0cb-240">Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans.</span></span> <span data-ttu-id="9d0cb-241">กระบวนการวางแผนงบประมาณกำหนดจัดทำงบประมาณองค์กร ลำดับงาน โครงร่าง และเท็มเพจจะใช้สำหรับการสร้างแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-241">Budget planning process defines what budgeting organizations, workflow, layouts and templates will be used for creating budget plans.</span></span> 

<span data-ttu-id="9d0cb-242">6.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-242">6.1.</span></span> <span data-ttu-id="9d0cb-243">นำไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; กระบวนการวางแผนงบประมาณ และสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="9d0cb-243">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process, and create a new record.</span></span>

-   <span data-ttu-id="9d0cb-244">กระบวนการวางแผนงบประมาณ – DEMF budgeting FY2016</span><span class="sxs-lookup"><span data-stu-id="9d0cb-244">Budget planning process – DEMF budgeting FY2016</span></span>
-   <span data-ttu-id="9d0cb-245">วงจรงบประมาณ – FY2016</span><span class="sxs-lookup"><span data-stu-id="9d0cb-245">Budget cycle – FY2016</span></span>
-   <span data-ttu-id="9d0cb-246">บัญชีแยกประเภท– DEMF</span><span class="sxs-lookup"><span data-stu-id="9d0cb-246">Ledger – DEMF</span></span>
-   <span data-ttu-id="9d0cb-247">โครงสร้างทางบัญชีเริ่มต้น – Manufacturing P&L</span><span class="sxs-lookup"><span data-stu-id="9d0cb-247">Default account structure – Manufacturing P&L</span></span>
-   <span data-ttu-id="9d0cb-248">ลำดับชั้นขององค์กร – เลือกลำดับชั้นสร้างขึ้นตั้งแต่ขั้นเริ่มต้นในห้องปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-248">Organization hierarchy – pick the hierarchy created in the beginning of the lab</span></span>
-   <span data-ttu-id="9d0cb-249">ลำดับงานของการวางแผนงบประมาณ –มอบหมายอัตโนมัติ – อนุมัติลำดับงานสำหรับแผนกการเงิน</span><span class="sxs-lookup"><span data-stu-id="9d0cb-249">Budget planning workflow – assign Auto – Approve workflow for Finance department</span></span>
-   <span data-ttu-id="9d0cb-250">ในกฎขั้นการวางแผนงบประมาณและเท็มเพลต เลือกสำหรับแต่ละลำดับงานงบประมาณ ถ้าได้อนุญาตการเพิ่มรายการ และแก้ไขรายการ และสิ่งที่โครงร่างควรจะใช้โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9d0cb-250">In budget planning stage rules and templates, for each workflow Budget planning stage pick if Adding lines and Modifying lines is allowed and what Layout should be used by default</span></span>

<span data-ttu-id="9d0cb-251">*หมายเหตุ: คุณสามารถสร้างโครงร่างเอกสารเพิ่มเติม และกำหนดค่าให้พร้อมใช้งานในขั้นลำดับงานของการวางแผนงบประมาณ ด้วยการคลิกปุ่มเค้าโครงสำรอง*</span><span class="sxs-lookup"><span data-stu-id="9d0cb-251">*Note: You can create additional document layouts and assign them to be available in budget planning workflow stage by clicking Alternate layouts button.*</span></span> 

<span data-ttu-id="9d0cb-252">[![โครงร่างรอง](./media/screenshot27.png)](./media/screenshot27.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-252">[![Alternate layouts](./media/screenshot27.png)](./media/screenshot27.png)</span></span> 

<span data-ttu-id="9d0cb-253">6.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-253">6.2.</span></span> <span data-ttu-id="9d0cb-254">เลือกการดำเนินการ &gt; เปิดใช้งานเพื่อเรียกใช้ลำดับงานของแผนงบประมาณนี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-254">Select Actions &gt; Activate to activate this budget planning workflow.</span></span> 

<span data-ttu-id="9d0cb-255">[![เรียกใช้](./media/screenshot28.png)](./media/screenshot28.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-255">[![Activate](./media/screenshot28.png)](./media/screenshot28.png)</span></span>

## <a name="exercise-2-process-simulation"></a><span data-ttu-id="9d0cb-256">แบบฝึกหัดที่ 2: การจำลองกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-256">Exercise 2: Process simulation</span></span>

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a><span data-ttu-id="9d0cb-257">งานที่ 7: สร้างข้อมูลเริ่มต้นสำหรับแผนงบประมาณจากรายการบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9d0cb-257">Task 7: Generate initial data for budget plan from General ledger</span></span>
<span data-ttu-id="9d0cb-258">7.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-258">7.1.</span></span> <span data-ttu-id="9d0cb-259">นำไปยังการจัดทำงบประมาณ &gt; งานประจำงวด &gt; สร้างรายการแผนงบประมาณจากบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9d0cb-259">Navigate to Budgeting &gt; Periodic &gt; Generate budget plan from General ledger.</span></span> <span data-ttu-id="9d0cb-260">กรอกข้อมูลพารามิเตอร์กระบวนการเป็นครั้งคราว และคลิกปุ่ม สร้าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-260">Fill in the periodic process parameters, and click Generate.</span></span> 

<span data-ttu-id="9d0cb-261">7.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-261">7.2.</span></span> <span data-ttu-id="9d0cb-262">นำทางไปยังการจัดทำงบประมาณ &gt; แผนงบประมาณ เพื่อหาแผนงบประมาณที่สร้างขึ้นโดยกระบวนการสร้าง</span><span class="sxs-lookup"><span data-stu-id="9d0cb-262">Navigate to Budgeting &gt; Budget plans to find a budget plan created by the Generate process.</span></span> 

<span data-ttu-id="9d0cb-263">[![แผนงบประมาณ](./media/screenshot30.png)](./media/screenshot30.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-263">[![Budget plan](./media/screenshot30.png)](./media/screenshot30.png)</span></span> 

<span data-ttu-id="9d0cb-264">7.3</span><span class="sxs-lookup"><span data-stu-id="9d0cb-264">7.3.</span></span> <span data-ttu-id="9d0cb-265">เปิดรายละเอียดเอกสาร โดยคลิกที่ไฮเปอร์ลิงค์หมายเลขเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9d0cb-265">Open document details by clicking on Document number hyperlink.</span></span> <span data-ttu-id="9d0cb-266">แผนงบประมาณจะแสดงขึ้นตามที่กำหนดไว้ในโครงร่างที่สร้างขึ้นในห้องปฏิบัติการนี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-266">Budget plan is displayed as defined in the layout created during this lab.</span></span> 

<span data-ttu-id="9d0cb-267">[![การแสดงแผนงบประมาณ](./media/screenshot31.png)](./media/screenshot31.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-267">[![Budget plan display](./media/screenshot31.png)](./media/screenshot31.png)</span></span>

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a><span data-ttu-id="9d0cb-268">งานที่ 8: สร้างงบประมาณปีปัจจุบันตามจริงของปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9d0cb-268">Task 8: Create current year budget based on previous year actuals</span></span>
<span data-ttu-id="9d0cb-269">สามารถใช้วิธีการปันส่วนในแผนงบประมาณเพื่อคัดลอกข้อมูลสำหรับแผนงบประมาณได้โดยง่ายจากสถานการณ์จำลองหนึ่งไปอีกสถานการณ์จำลองหนึ่ง/ กระจายเหล่านั้นข้ามรอบระยะเวลา /ปันส่วนไปยังกับมิติ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-269">Allocation methods can be used in budget plan to easily copy information for budget plans from one scenario to another/ spread them across periods/ allocate to dimensions.</span></span> <span data-ttu-id="9d0cb-270">เราจะใช้การปันส่วนเพื่อสร้างงบประมาณปีปัจจุบันจากยอดจริงในปีก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="9d0cb-270">We will use allocations to create current year budget from previous year actuals.</span></span> 

<span data-ttu-id="9d0cb-271">8.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-271">8.1.</span></span> <span data-ttu-id="9d0cb-272">เลือกรายการทั้งหมดในกริดเอกสารแผนงบประมาณ และคลิก ปันส่วนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-272">Pick all lines in the budget plan document grid and click Allocate budget.</span></span> 

<span data-ttu-id="9d0cb-273">[![รายการทั้งหมด](./media/screenshot32.png)](./media/screenshot32.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-273">[![All lines](./media/screenshot32.png)](./media/screenshot32.png)</span></span> 

<span data-ttu-id="9d0cb-274">8.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-274">8.2.</span></span> <span data-ttu-id="9d0cb-275">เลือกวิธีการปันส่วน คีย์รอบระยะเวลา สถานการณ์จำลองต้นทางและปลายทาง และคลิก ปันส่วน</span><span class="sxs-lookup"><span data-stu-id="9d0cb-275">Select allocation method, Period key, Source and destination scenarios, and click Allocate.</span></span> 

<span data-ttu-id="9d0cb-276">[![ปันส่วน](./media/screenshot33.png)](./media/screenshot33.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-276">[![Allocate](./media/screenshot33.png)](./media/screenshot33.png)</span></span>

<span data-ttu-id="9d0cb-277">ยอดเงินจริงของปีก่อนหน้านี้จะถูกคัดลอกไปยังงบประมาณปีปัจจุบัน และปันส่วนให้รอบระยะเวลาต่างๆ โดยใช้คีย์รอบระยะเวลาของเส้นโค้งการขาย</span><span class="sxs-lookup"><span data-stu-id="9d0cb-277">The previous year actual amounts will be copied to the current year budget and allocate them across periods using the Sales curve period key.</span></span> 

<span data-ttu-id="9d0cb-278">[![เส้นโค้งการขาย](./media/screenshot34.png)](./media/screenshot34.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-278">[![Sales curve](./media/screenshot34.png)](./media/screenshot34.png)</span></span>

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a><span data-ttu-id="9d0cb-279">งานที่ 9: การปรับปรุงเอกสารแผนงบประมาณโดยใช้ Excel และเอกสารขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="9d0cb-279">Task 9: Adjust budget plan document using Excel and finalize the document</span></span>
<span data-ttu-id="9d0cb-280">9.1</span><span class="sxs-lookup"><span data-stu-id="9d0cb-280">9.1.</span></span> <span data-ttu-id="9d0cb-281">คลิกปุ่มแผ่นงานเพื่อเปิดเนื้อหาเอกสารใน Excel</span><span class="sxs-lookup"><span data-stu-id="9d0cb-281">Click the Worksheet button to open document contents in Excel.</span></span>

<span data-ttu-id="9d0cb-282">9.2</span><span class="sxs-lookup"><span data-stu-id="9d0cb-282">9.2.</span></span> <span data-ttu-id="9d0cb-283">เมื่อสมุดงาน Excel เปิดขึ้น ปรับปรุงหมายเลขในเอกสารแผนงบประมาณ และคลิกปุ่ม เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="9d0cb-283">When the Excel workbook opens, adjust the numbers in the budget plan document, and click the Publish button.</span></span>

<span data-ttu-id="9d0cb-284">9.3</span><span class="sxs-lookup"><span data-stu-id="9d0cb-284">9.3.</span></span> <span data-ttu-id="9d0cb-285">ย้อนกลับไปยังเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-285">Return to budget plan document.</span></span> <span data-ttu-id="9d0cb-286">คลิกลำดับงาน &gt; ส่งเอกสารเพื่ออนุมัติเอกสารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-286">Click Workflow &gt; Submit to Auto-approve the document.</span></span>

<span data-ttu-id="9d0cb-287">[![การอนุมัติอัตโนมัติ](./media/screenshot37.png)](./media/screenshot37.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-287">[![Auto-approve](./media/screenshot37.png)](./media/screenshot37.png)</span></span> 

<span data-ttu-id="9d0cb-288">เมื่อลำดับงานเสร็จสมบูรณ์ ขั้นเอกสารแผนงบประมาณจะเปลี่ยนเป็น อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="9d0cb-288">Once workflow completes, the budget plan document stage changes to Approved.</span></span> <span data-ttu-id="9d0cb-289">[![อนุมัติแล้ว](./media/screenshot38.png)](./media/screenshot38.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-289">[![Approved](./media/screenshot38.png)](./media/screenshot38.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="9d0cb-290">ภาคผนวก</span><span class="sxs-lookup"><span data-stu-id="9d0cb-290">Appendix</span></span>

### <a name="auto-approve-workflow-configuration"></a><span data-ttu-id="9d0cb-291">การตั้งค่าคอนฟิกลำดับงานอนุมัติอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-291">Auto-Approve workflow configuration</span></span>

<span data-ttu-id="9d0cb-292">A.</span><span class="sxs-lookup"><span data-stu-id="9d0cb-292">A.</span></span> <span data-ttu-id="9d0cb-293">การจัดงบประมาณ &gt; ตั้งค่า &gt; การวางแผนงบประมาณ &gt; ลำดับงานการจัดงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-293">Budgeting &gt; Setup &gt; Budget planning &gt; Budgeting workflows.</span></span> <span data-ttu-id="9d0cb-294">สร้างลำดับงานใหม่โดยใช้ลำดับงานการวางแผนงบประมาณเท็มเพลต:</span><span class="sxs-lookup"><span data-stu-id="9d0cb-294">Create a new workflow using template Budget planning workflows:</span></span>

<span data-ttu-id="9d0cb-295">[![สร้างลำดับงานใหม่](./media/screenshot39.png)](./media/screenshot39.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-295">[![Create a new workflow](./media/screenshot39.png)](./media/screenshot39.png)</span></span>

<span data-ttu-id="9d0cb-296">ลำดับงานนี้จะประกอบด้วยงานเพียงหนึ่งรายการ – การเปลี่ยนขั้นของแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-296">This workflow will contain only one task – Stage transition budget plan.</span></span> 

<span data-ttu-id="9d0cb-297">[![การเปลี่ยนขั้นของแผนงบประมาณ](./media/screenshot40.png)](./media/screenshot40.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-297">[![Stage transition budget plan](./media/screenshot40.png)](./media/screenshot40.png)</span></span> 

<span data-ttu-id="9d0cb-298">บันทึกและเรียกใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9d0cb-298">Save and activate the workflow.</span></span> 

<span data-ttu-id="9d0cb-299">B.</span><span class="sxs-lookup"><span data-stu-id="9d0cb-299">B.</span></span> <span data-ttu-id="9d0cb-300">นำทางไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-300">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="9d0cb-301">ในแท็บขั้น สร้าง 2 ขั้น – เริ่มต้น และส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="9d0cb-301">In the Stages tab, create 2 stages – Initial and Submitted.</span></span> 

<span data-ttu-id="9d0cb-302">[![เริ่มต้นและขั้นส่ง](./media/screenshot41.png)](./media/screenshot41.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-302">[![Initial and submitted](./media/screenshot41.png)](./media/screenshot41.png)</span></span>

<span data-ttu-id="9d0cb-303">C.</span><span class="sxs-lookup"><span data-stu-id="9d0cb-303">C.</span></span> <span data-ttu-id="9d0cb-304">นำทางไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9d0cb-304">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="9d0cb-305">ในแท็บขั้นลำดับงาน เชื่อมโยงลำดับงานอนุมัติอัตโนมัติที่สร้างขึ้นในขั้นตอน A ด้วยขั้นเริ่มต้นและส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="9d0cb-305">In the Workflow Stages tab, associate the workflow Auto–approve created in step A with the stages Initial and Submitted.</span></span>

<span data-ttu-id="9d0cb-306">[![การจัดงบประมาณและการวางแผนงบประมาณ](./media/screenshot42.png)](./media/screenshot42.png)</span><span class="sxs-lookup"><span data-stu-id="9d0cb-306">[![Budgeting and budget planning](./media/screenshot42.png)](./media/screenshot42.png)</span></span>  



