---
title: "การวางแผนงบประมาณ"
description: "วัตถุประสงค์ของห้องปฏิบัติการนี้คือ แสดงมุมมองที่แนะนำของการอัพเดตฟังก์ชันของ Microsoft Dynamics 365 for Finance and Operations ในพื้นที่การวางแผนงบประมาณ จุดประสงค์ของห้องปฏิบัติการนี้คือแสดงตัวอย่างการตั้งค่าคอนฟิกด่วนของโมดูลการวางแผนงบประมาณ และแสดงวิธีวางแผนงบประมาณให้สำเร็จโดยใช้การตั้งค่าคอนฟิกนี้"
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b8f2f3a33dc19c2ebc941d1a504eae0c276f3cdf
ms.openlocfilehash: ac2e98dbbd45becf06e28b6ea4eb9d0ec15e30f6
ms.contentlocale: th-th
ms.lasthandoff: 06/25/2018

---

# <a name="budget-planning"></a><span data-ttu-id="f6a67-104">การวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-104">Budget planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6a67-105">วัตถุประสงค์ของห้องปฏิบัติการนี้คือ แสดงมุมมองที่แนะนำของการอัพเดตฟังก์ชันของ Microsoft Dynamics 365 for Finance and Operations ในพื้นที่การวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-105">The objective of this lab is to provide a guided view of Microsoft Dynamics 365 for Finance and Operations functionality updates in Budget planning area.</span></span> <span data-ttu-id="f6a67-106">จุดประสงค์ของห้องปฏิบัติการนี้คือแสดงตัวอย่างการตั้งค่าคอนฟิกด่วนของโมดูลการวางแผนงบประมาณ และแสดงวิธีวางแผนงบประมาณให้สำเร็จโดยใช้การตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-106">The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration.</span></span>  <span data-ttu-id="f6a67-107">ห้องปฏิบัติการนี้จะโฟกัสเป็นพิเศษในกระบวนการทางธุรกิจหรืองานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f6a67-107">This lab will focus specifically on the following business processes or tasks:</span></span>
- <span data-ttu-id="f6a67-108">การสร้างลำดับชั้นขององค์กรสำหรับการวางแผนงบประมาณ และการตั้งค่าคอนฟิกความปลอดภัยของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f6a67-108">Creating organizational hierarchy for budget planning and configuring user security</span></span>
- <span data-ttu-id="f6a67-109">การกำหนดสถานการณ์จำลองแผนงบประมาณ คอลัมน์แผนงบประมาณ โครงร่าง และเท็มเพลต Excel</span><span class="sxs-lookup"><span data-stu-id="f6a67-109">Defining budget plan scenarios, budget plan columns, layouts and Excel templates</span></span>
- <span data-ttu-id="f6a67-110">การสร้างและการเรียกใช้กระบวนการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-110">Creating and activating budget planning process</span></span>
- <span data-ttu-id="f6a67-111">การสร้างเอกสารแผนงบประมาณโดยการดึงค่าจริงจากบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="f6a67-111">Creating budget plan document by pulling in actuals from General ledger</span></span>
- <span data-ttu-id="f6a67-112">การใช้การปันส่วนเพื่อปรับปรุงข้อมูลเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-112">Using allocations to adjust budget plan document data</span></span>
- <span data-ttu-id="f6a67-113">การแก้ไขข้อมูลเอกสารแผนงบประมาณใน Excel</span><span class="sxs-lookup"><span data-stu-id="f6a67-113">Editing budget plan document data in Excel</span></span> 

<a name="prerequisites"></a><span data-ttu-id="f6a67-114">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="f6a67-114">Prerequisites</span></span> 
------------------

<span data-ttu-id="f6a67-115">สำหรับบทสอนนี้ คุณจะต้องเข้าถึงสภาพแวดล้อม Finance and Operations ด้วยข้อมูลสาธิต Contoso และเตรียมใช้งานในฐานะผู้ดูแลบนอินสแตนซ์</span><span class="sxs-lookup"><span data-stu-id="f6a67-115">For this tutorial, you’ll need to access the Finance and Operations environment with Contoso demo data, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="f6a67-116">อย่าใช้โหมดเบราเซอร์ส่วนตัวสำหรับห้องปฏิบัติการนี้ - ลงชื่อออกจากบัญชีอื่น ๆ ในเบราเซอร์ถ้าจำเป็น และลงชื่อเข้าใช้ ด้วยข้อมูลประจำตัวของผู้ดูแลระบบ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6a67-116">Do not use In Private browser mode for this lab - sign out from any other account in the browser if needed and sign in with Finance and Operations administrator credentials.</span></span> <span data-ttu-id="f6a67-117">เมื่อลงชื่อเข้าใช้ Finance and Operations คุณ **ต้อง** กาเครื่องหมายที่ "ให้ฉันลงชื่อเข้าใช้" กล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="f6a67-117">When signing into Finance and Operations, you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="f6a67-118">วิธีนี้สร้างคุกกี้ถาวรที่แอพลิเคชัน Excel ต้องการ ณ ขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-118">This creates a persistent cookie that the Excel App currently needs.</span></span> <span data-ttu-id="f6a67-119">ถ้าคุณเข้าสู่ระบบ Finance and Operations โดยใช้เบราเซอร์อื่นนอกเหนือจาก IE แล้วคุณก็จะพร้อมเข้าสู่ระบบภายในแอพลิเคชัน Excel</span><span class="sxs-lookup"><span data-stu-id="f6a67-119">If you sign in to the Finance and Operations using a browser other than IE, then you’ll be prompted to sign in within the Excel App.</span></span> <span data-ttu-id="f6a67-120">เมื่อคุณคลิก "ลงชื่อเข้าใช้" ในแอพลิเคชัน Excel หน้าต่างป๊อปอัพ IE จะเปิดและ ขณะคุณกำลังลงชื่อคุณ **ต้อง** กาเครื่องหมายที่กล่องกาเครื่องหมาย "ให้ฉันลงชื่อเข้าใช้"</span><span class="sxs-lookup"><span data-stu-id="f6a67-120">When you click “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="f6a67-121">ถ้าคลิก "ลงชื่อข้าใช้" ในแอพลิเคชัน Excel ไม่ดำเนินการใดๆ คุณควรล้างแคชคุกกี้ IE</span><span class="sxs-lookup"><span data-stu-id="f6a67-121">If clicking “Sign in” in the Excel App doesn’t appear to do anything then you should clear the IE cookie cache.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="f6a67-122">**ภาพรวมของสถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="f6a67-122">**Scenario overview**</span></span>
<span data-ttu-id="f6a67-123">จูเลียทำงานเป็นผู้จัดการฝ่ายการเงินในระบบความบันเทิง Contoso ในเยอรมนี (DEMF)</span><span class="sxs-lookup"><span data-stu-id="f6a67-123">Julia works as a finance manager in Contoso Entertainment Systems in Germany (DEMF).</span></span> <span data-ttu-id="f6a67-124">เมื่อ FY2016 ใกล้ถึง เธอจำเป็นต้องทำงานในการตั้งค่างบประมาณของบริษัทสำหรับปีกำลังมาถึง</span><span class="sxs-lookup"><span data-stu-id="f6a67-124">As FY2016 approaches, she needs to work on setting up the company’s budget for the upcoming year.</span></span> <span data-ttu-id="f6a67-125">การจัดเตรียมงบประมาณมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f6a67-125">Budget preparation looks as follows:</span></span>

1.  <span data-ttu-id="f6a67-126">Julia ใช้ยอดเงินที่เกิดขึ้นจริงของปีก่อนหน้านี้เป็นจุดเริ่มต้นเพื่อสร้างงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-126">Julia uses previous year actuals amounts as a starting point to create the budget.</span></span>
2.  <span data-ttu-id="f6a67-127">ตามยอดจริงในปีก่อนหน้า เธอสร้างการประเมิน 12 เดือน สำหรับปีกำลังมาถึง</span><span class="sxs-lookup"><span data-stu-id="f6a67-127">Based on the previous year actuals, she creates estimates for 12 months in the upcoming year</span></span>
3.  <span data-ttu-id="f6a67-128">Julia ตรวจทานงบประมาณที่ ด้วย CFO</span><span class="sxs-lookup"><span data-stu-id="f6a67-128">Julia reviews the budget with CFO.</span></span> <span data-ttu-id="f6a67-129">เมื่อเสร็จเรียบร้อย เธอทำการปรับปรุงเท่าที่จำเป็นสำหรับแผนงบประมาณ และ ดำเนินการจัดเตรียมงบประมาณประจำปีขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f6a67-129">Once done she makes necessary adjustments for the budget plan and finalizes budget preparation.</span></span>

<span data-ttu-id="f6a67-130">เค้าร่างการตั้งค่าคอนฟิกการวางแผนงบประมาณสำหรับสถานการณ์จำลองมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f6a67-130">Budget planning configuration schema for the scenario looks as follows:</span></span>

![เค้าร่างการกำหนดค่าการวางแผนงบประมาณ](./media/screenshot1-300x152.png)

<span data-ttu-id="f6a67-132">Julia ใช้เท็มเพลต Excel ต่อไปนี้ในการจัดเตรียมงบประมาณ:</span><span class="sxs-lookup"><span data-stu-id="f6a67-132">Julia uses the following Excel template to prepare the budget:</span></span>

<span data-ttu-id="f6a67-133">[![เท็มเพลต Excel](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-133">[![Excel template](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span></span>

## <a name="exercise-1-configuration"></a><span data-ttu-id="f6a67-134">แบบฝึกหัดที่ 1: ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f6a67-134">Exercise 1: Configuration</span></span>

### <a name="task-1-create-organizational-hierarchy"></a><span data-ttu-id="f6a67-135">**งานที่ 1: สร้างลำดับชั้นองค์กร**</span><span class="sxs-lookup"><span data-stu-id="f6a67-135">**Task 1: Create organizational hierarchy**</span></span>
<span data-ttu-id="f6a67-136">เมื่อกระบวนการจัดทำงบประมาณทั้งหมดเกิดขึ้นในแผนกการเงิน ดังนั้น Julia จึงจำเป็นต้องสร้างลำดับชั้นองค์กรที่เรียบง่ายมากๆ – ประกอบด้วยแผนกการเงินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f6a67-136">As all the budgeting process happens in the Finance department, therefore Julia needs to create a very simple organizational hierarchy – consisting of Finance department only.</span></span> <span data-ttu-id="f6a67-137">1.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-137">1.1.</span></span> <span data-ttu-id="f6a67-138">นำไปยังลำดับชั้นขององค์กร (การจัดการองค์กร &gt; องค์กร &gt; ลำดับชั้นขององค์กร) และคลิกปุ่มใหม่</span><span class="sxs-lookup"><span data-stu-id="f6a67-138">Navigate to Organization hierarchies (Organization administration &gt; Organizations &gt; Organization hierarchies) and click New button</span></span>

![ลำดับชั้นขององค์กร](./media/screenshot3.png) 

<span data-ttu-id="f6a67-140">1.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-140">1.2.</span></span> <span data-ttu-id="f6a67-141">พิมพ์ชื่อสำหรับลำดับชั้นขององค์กร แล้วคลิกปุ่มกำหนดวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="f6a67-141">Type the name for the organizational hierarchy and click button Assign purpose</span></span>

<span data-ttu-id="f6a67-142">[![ชื่อ](./media/screenshot4.png)](./media/screenshot4.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-142">[![Name](./media/screenshot4.png)](./media/screenshot4.png)</span></span> 

<span data-ttu-id="f6a67-143">1.3</span><span class="sxs-lookup"><span data-stu-id="f6a67-143">1.3.</span></span> <span data-ttu-id="f6a67-144">เลือกวัตถุประสงค์ในการวางแผนงบประมาณ คลิกปุ่มเพิ่ม และกำหนดลำดับชั้นขององค์กรที่สร้างขึ้นใหม่:</span><span class="sxs-lookup"><span data-stu-id="f6a67-144">Select Budget planning purpose, click button Add and assign newly created organizational hierarchy:</span></span> 

<span data-ttu-id="f6a67-145">[![กำหนดวัตถุประสงค์](./media/screenshot5.png)](./media/screenshot5.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-145">[![Assign purpose](./media/screenshot5.png)](./media/screenshot5.png)</span></span>

<span data-ttu-id="f6a67-146">1.4</span><span class="sxs-lookup"><span data-stu-id="f6a67-146">1.4.</span></span> <span data-ttu-id="f6a67-147">ทำซ้ำขั้นตอนข้างต้นเพื่อความมุ่งหมายด้านความปลอดภัยขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f6a67-147">Repeat the step above for Security organizational purpose.</span></span> <span data-ttu-id="f6a67-148">ปิดแบบฟอร์ม เมื่อเสร้จสิ้น</span><span class="sxs-lookup"><span data-stu-id="f6a67-148">Close the form when done.</span></span>

<span data-ttu-id="f6a67-149">[![องค์กรการรักษาความปลอดภัย](./media/screenshot6.png)](./media/screenshot6.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-149">[![Security org](./media/screenshot6.png)](./media/screenshot6.png)</span></span>

<span data-ttu-id="f6a67-150">1.5</span><span class="sxs-lookup"><span data-stu-id="f6a67-150">1.5.</span></span> <span data-ttu-id="f6a67-151">ในแบบฟอร์มลำดับชั้นขององค์กรคลิกปุ่มมุมมอง</span><span class="sxs-lookup"><span data-stu-id="f6a67-151">In the Organizational Hierarchies form click button View.</span></span> <span data-ttu-id="f6a67-152">คลิกแก้ไขในโปรแกรมออกแบบลำดับชั้น และสร้างลำดับชั้น โดยการคลิกปุ่มแทรก</span><span class="sxs-lookup"><span data-stu-id="f6a67-152">Click Edit in the Hierarchy designer and create a hierarchy by clicking button Insert.</span></span>

<span data-ttu-id="f6a67-153">[![แทรก](./media/screenshot7.png)](./media/screenshot7.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-153">[![Insert](./media/screenshot7.png)](./media/screenshot7.png)</span></span> 

<span data-ttu-id="f6a67-154">1.6</span><span class="sxs-lookup"><span data-stu-id="f6a67-154">1.6.</span></span> <span data-ttu-id="f6a67-155">เลือกแผนกการเงินสำหรับลำดับชั้นการจัดทำงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-155">Select Finance department for the budgeting hierarchy.</span></span> 

<span data-ttu-id="f6a67-156">[![การเงิน](./media/screenshot8.png)](./media/screenshot8.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-156">[![Finance](./media/screenshot8.png)](./media/screenshot8.png)</span></span>

<span data-ttu-id="f6a67-157">1.7</span><span class="sxs-lookup"><span data-stu-id="f6a67-157">1.7.</span></span> <span data-ttu-id="f6a67-158">เมื่อทำเสร็จแล้ว ให้คลิกปุ่มเผยแพร่ และปิด</span><span class="sxs-lookup"><span data-stu-id="f6a67-158">When done, click button Publish and Close.</span></span> <span data-ttu-id="f6a67-159">เลือกวันที่ 1 มกราคม 2015 เป็นวันที่มีผลบังคับใช้สำหรับการเผยแพร่ลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f6a67-159">Select 1/1/2015 as effective date for hierarchy publishing.</span></span>

<span data-ttu-id="f6a67-160">[![วันที่มีผลบังคับใช้](./media/screenshot9.png)](./media/screenshot9.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-160">[![Effective date](./media/screenshot9.png)](./media/screenshot9.png)</span></span>

### <a name="task-2-configure-user-security"></a><span data-ttu-id="f6a67-161">งานที่ 2: ตั้งค่าคอนฟิกความปลอดภัยของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f6a67-161">Task 2: Configure user security</span></span>
<span data-ttu-id="f6a67-162">การวางแผนงบประมาณใช้นโยบายความปลอดภัยพิเศษเพื่อกำหนดค่าคอนฟิกให้กับข้อมูลแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-162">Budget planning uses special security policies to configure access to budget plans data.</span></span> <span data-ttu-id="f6a67-163">จูเลียจำเป็นต้องให้สิทธิ์ในการเข้าถึงแผนงบประมาณทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6a67-163">Julia needs to give access to Finance budget plans for herself.</span></span> 

<span data-ttu-id="f6a67-164">2.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-164">2.1.</span></span> <span data-ttu-id="f6a67-165">สลับไปที่บริบทของนิติบุคคล DEMF</span><span class="sxs-lookup"><span data-stu-id="f6a67-165">Switch to DEMF legal entity context.</span></span> 


<span data-ttu-id="f6a67-166">2.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-166">2.2.</span></span> <span data-ttu-id="f6a67-167">นำทางไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-167">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="f6a67-168">ในแท็บพารามิเตอร์ ตั้งค่ารูปแบบความปลอดภัยตามองค์กรความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="f6a67-168">In Parameters tab, set the Security model value to Based on security organizations</span></span> 

<span data-ttu-id="f6a67-169">[![พารามิเตอร์](./media/screenshot11.png)](./media/screenshot11.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-169">[![Parameters](./media/screenshot11.png)](./media/screenshot11.png)</span></span> 

<span data-ttu-id="f6a67-170">2.3</span><span class="sxs-lookup"><span data-stu-id="f6a67-170">2.3.</span></span> <span data-ttu-id="f6a67-171">ไปยังการดูแลระบบ &gt; ผู้ใช้ &gt; ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f6a67-171">Navigate to System administration &gt; Users &gt; Users.</span></span> <span data-ttu-id="f6a67-172">กำหนดบทบาทผู้จัดการงบประมาณการบริหารให้แก่ผู้ใช้ที่ดูแลระบบ (Julia Funderburk)</span><span class="sxs-lookup"><span data-stu-id="f6a67-172">Give user Admin (Julia Funderburk) Budget manager role.</span></span> 

<span data-ttu-id="f6a67-173">[![ผู้จัดการงบประมาณ](./media/screenshot12.png)](./media/screenshot12.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-173">[![Budget manager](./media/screenshot12.png)](./media/screenshot12.png)</span></span> 

<span data-ttu-id="f6a67-174">2.4</span><span class="sxs-lookup"><span data-stu-id="f6a67-174">2.4.</span></span> <span data-ttu-id="f6a67-175">เลือกบทบาทผู้ใช้ แล้วคลิกกำหนดองค์กร</span><span class="sxs-lookup"><span data-stu-id="f6a67-175">Pick user role and click Assign organizations</span></span> 

<span data-ttu-id="f6a67-176">[![กำหนดองค์กร](./media/screenshot13.png)](./media/screenshot13.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-176">[![Assign org](./media/screenshot13.png)](./media/screenshot13.png)</span></span>

<span data-ttu-id="f6a67-177">2.5</span><span class="sxs-lookup"><span data-stu-id="f6a67-177">2.5.</span></span> <span data-ttu-id="f6a67-178">เลือก "อนุญาตให้เข้าถึงองค์กรที่ระบุ"</span><span class="sxs-lookup"><span data-stu-id="f6a67-178">Select “Grant access to specific organizations”.</span></span> <span data-ttu-id="f6a67-179">เลือกลำดับชั้นขององค์กรที่สร้างขึ้นในขั้นตอนแรก</span><span class="sxs-lookup"><span data-stu-id="f6a67-179">Pick Organizational hierarchy created in the first step.</span></span> <span data-ttu-id="f6a67-180">เลือกโหนดการเงิน แล้วคลิกเงินช่วยเหลือ ด้วยปุ่มรอง</span><span class="sxs-lookup"><span data-stu-id="f6a67-180">Pick Finance node and click Grant with children button</span></span> 

<span data-ttu-id="f6a67-181">***ข้อสำคัญ!***</span><span class="sxs-lookup"><span data-stu-id="f6a67-181">***Important!***</span></span> <span data-ttu-id="f6a67-182">*ตรวจสอบให้แน่ใจว่าว่าคุณอยู่ในบริบทนิติบุคคล DEMF ขณะดำเนินการกับงานนี้ เมื่อได้ใช้ความปลอดภัยขององค์กรสำหรับแต่ละนิติบุคคล*</span><span class="sxs-lookup"><span data-stu-id="f6a67-182">*Make sure you are in DEMF legal entity context when performing this task, as Organizational security is applied per legal entity*</span></span> 

### <a name="task-3-create-scenarios"></a><span data-ttu-id="f6a67-183">งานที่ 3: สร้างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="f6a67-183">Task 3: Create scenarios</span></span>
<span data-ttu-id="f6a67-184">3.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-184">3.1.</span></span> <span data-ttu-id="f6a67-185">นำทางไปยังการจัดทำงบประมาณ&gt;การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-185">Navigate to Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="f6a67-186">ในหน้าสถานการณ์จำลองสังเกตสถานการณ์เรากำลังจะใช้ห้องปฏิบัติการนี้เพิ่มเติม: ยอดที่เกิดขึ้นจริงและงบประมาณปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-186">In the Scenarios page note the scenarios we are going to use further in this lab: Previous year actuals and Budgeted.</span></span> 

<span data-ttu-id="f6a67-187">*หมายเหตุ: คุณสามารถสร้างสถานการณ์จำลองใหม่สำหรับแบบฝึกหัดนี้ ตามประสงค์และ และใช้เหล่านั้นแทน*</span><span class="sxs-lookup"><span data-stu-id="f6a67-187">*Note: You can create new scenarios for this exercise if desired and use those instead.*</span></span> 

<span data-ttu-id="f6a67-188">[![สถานการณ์จำลองใหม่](./media/screenshot15.png)](./media/screenshot15.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-188">[![New scenarios](./media/screenshot15.png)](./media/screenshot15.png)</span></span> 

<span data-ttu-id="f6a67-189">*หมายเหตุ: Julia ไม่ได้ใช้กระบวนการอนุมัติอย่างเป็นทางการสำหรับการจัดเตรียมงบประมาณ เราจะข้ามลำดับงาน ขั้น และตั้งค่าขั้นตอนลำดับงานในห้องปฏิบัติการนี้ และจะใช้การตั้งค่าที่มีอยู่สำหรับการลำดับงานอนุมัติอัตโนมัติ โปรดดูภาคผนวกสำหรับการตั้งค่าคอนฟิกลำดับงานนี้*</span><span class="sxs-lookup"><span data-stu-id="f6a67-189">*Note: as Julia is not using formal approval process for budget preparation, we will skip Workflows, Stages and Workflow stages setup in this lab and will use existing setup for Auto – approve workflow. See appendix for this workflow configuration.*</span></span>

### <a name="task-4-create-budget-plan-columns"></a><span data-ttu-id="f6a67-190">งานที่ 4: สร้างคอลัมน์แผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-190">Task 4: Create budget plan columns</span></span>
<span data-ttu-id="f6a67-191">แผนงบประมาณที่มีคอลัมน์ยอดเงินหรือปริมาณตามคอลัมน์ที่สามารถใช้ในโครงร่างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-191">Budget plan columns are either Monetary or quantity based columns that can be used in budget plan document layout.</span></span> <span data-ttu-id="f6a67-192">ในตัวอย่างของเรา เราต้องสร้างคอลัมน์สำหรับค่าจริงของปีก่อนหน้านี้และ คอลัมน์ 12 คอลัมน์เพื่อแสดงยอดแต่ละเดือนในปีงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-192">In our example we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year.</span></span> <span data-ttu-id="f6a67-193">คอลัมน์สามารถสร้างได้ โดยการคลิกปุ่มเพิ่ม และการกรอกมูลค่า หรือโดยการใช้ของเอนทิตี้ข้อมูลก็ได้</span><span class="sxs-lookup"><span data-stu-id="f6a67-193">Columns can be created either by simply clicking Add button and filling in the values, or with a help of Data entity.</span></span> <span data-ttu-id="f6a67-194">ในห้องปฏิบัติการนี้ เราจะใช้เอนทิตีข้อมูลเพื่อเติมค่า</span><span class="sxs-lookup"><span data-stu-id="f6a67-194">In this lab we will use Data entity to fill in the values.</span></span> 

<span data-ttu-id="f6a67-195">4.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-195">4.1.</span></span> <span data-ttu-id="f6a67-196">ในการจัดงบประมาณ&gt;ตั้งค่า &gt; การวางแผนงบประมาณ &gt;  การตั้งค่าคอนฟิกการวางแผนงบประมาณเปิดหน้าคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="f6a67-196">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Columns page.</span></span> <span data-ttu-id="f6a67-197">คลิกปุ่ม Office มุมบนขวาของแบบฟอร์ม และเลือกคอลัมน์ (ยังไม่ได้กรอง)</span><span class="sxs-lookup"><span data-stu-id="f6a67-197">Click Office button on the top right corner of the form and pick Columns (unfiltered)</span></span> 

<span data-ttu-id="f6a67-198">[![คอลัมน์ที่ยังไม่ได้กรอง](./media/screenshot16.png)](./media/screenshot16.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-198">[![Columns unfiltered](./media/screenshot16.png)](./media/screenshot16.png)</span></span> 

<span data-ttu-id="f6a67-199">4.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-199">4.2.</span></span> <span data-ttu-id="f6a67-200">ระบบจะเปิดสมุดงาน Excel ที่จะใช้สำหรับการเติมค่า</span><span class="sxs-lookup"><span data-stu-id="f6a67-200">System will open Excel workbook to be used for filling in the values.</span></span> <span data-ttu-id="f6a67-201">ถ้าได้รับพร้อมท์ ให้คลิกเปิดใช้งานการแก้ไขและเชื่อถือแอพนี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-201">If prompted, click Enable Editing and Trust this app</span></span> 

<span data-ttu-id="f6a67-202">[![เปิดใช้งานการแก้ไข](./media/screenshot18.png)](./media/screenshot18.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-202">[![Enable editing](./media/screenshot18.png)](./media/screenshot18.png)</span></span> 

<span data-ttu-id="f6a67-203">[![เชื่อถือแอพนี้](./media/screenshot17.png)](./media/screenshot17.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-203">[![Trust this app](./media/screenshot17.png)](./media/screenshot17.png)</span></span>

<span data-ttu-id="f6a67-204">4.3</span><span class="sxs-lookup"><span data-stu-id="f6a67-204">4.3.</span></span> <span data-ttu-id="f6a67-205">เราจะต้องการคอลัมน์เพิ่มเติมเพื่อเติมค่า</span><span class="sxs-lookup"><span data-stu-id="f6a67-205">We will need more columns to fill the values in.</span></span> <span data-ttu-id="f6a67-206">คลิกการออกแบบในบานหน้าต่างด้านขวาเพื่อเพิ่มคอลัมน์ลงในกริด:</span><span class="sxs-lookup"><span data-stu-id="f6a67-206">Click Design on the right side pane to add the columns to the grid:</span></span> 

<span data-ttu-id="f6a67-207">[![การออกแบบ](./media/screenshot19.png)](./media/screenshot19.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-207">[![Design](./media/screenshot19.png)](./media/screenshot19.png)</span></span> 

<span data-ttu-id="f6a67-208">4.4</span><span class="sxs-lookup"><span data-stu-id="f6a67-208">4.4.</span></span> <span data-ttu-id="f6a67-209">คลิกปุ่มดินสอน้อยถัดจาก PlanColumns เพื่อดูคอลัมน์ที่มีอยู่เพื่อเพิ่มลงในกริด</span><span class="sxs-lookup"><span data-stu-id="f6a67-209">Click little pencil button next to PlanColumns to see available columns to add to the grid</span></span> 

<span data-ttu-id="f6a67-210">[![แก้ไข](./media/screenshot20.png)](./media/screenshot20.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-210">[![Edit](./media/screenshot20.png)](./media/screenshot20.png)</span></span> 

<span data-ttu-id="f6a67-211">4.5</span><span class="sxs-lookup"><span data-stu-id="f6a67-211">4.5.</span></span> <span data-ttu-id="f6a67-212">ดับเบิลคลิกในแต่ละฟิลด์ที่พร้อมใช้งานเพื่อเพิ่มไปยังฟิลด์ที่เลือก และคลิกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="f6a67-212">Double click on each available field to add them to Selected fields and click Update</span></span> 

![อัพเดต](./media/screenshot21.png)<span data-ttu-id="f6a67-214">](./media/screenshot21.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-214">](./media/screenshot21.png)</span></span> 

<span data-ttu-id="f6a67-215">4.6</span><span class="sxs-lookup"><span data-stu-id="f6a67-215">4.6.</span></span> <span data-ttu-id="f6a67-216">ในตาราง Excel ให้เพิ่มคอลัมน์ทั้งหมดที่จำเป็นที่จะสร้าง</span><span class="sxs-lookup"><span data-stu-id="f6a67-216">In Excel table add all the columns that need to be created.</span></span> <span data-ttu-id="f6a67-217">ใช้คุณลักษณะการเติมอัตโนมัติใน Excel เพื่อเพิ่มบรรทัดอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="f6a67-217">Use AutoFill feature in Excel to add the lines quickly.</span></span> <span data-ttu-id="f6a67-218">ตรวจสอบให้แน่ใจว่า ได้เพิ่มบรรทัดที่เป็นส่วนหนึ่งของตาราง (เมื่อใช้เลื่อนแนวตั้ง คุณควรจะสามารถมองเห็นส่วนหัวของคอลัมน์ในตารางด้านบน)</span><span class="sxs-lookup"><span data-stu-id="f6a67-218">Make sure the lines are added as a part of the table (when using vertical scroll, you should be able to see column headers on the top of the grid)</span></span> 

<span data-ttu-id="f6a67-219">[![เติมอัตโนมัติ](./media/screenshot22.png)](./media/screenshot22.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-219">[![Autofill](./media/screenshot22.png)](./media/screenshot22.png)</span></span> 

<span data-ttu-id="f6a67-220">4.7</span><span class="sxs-lookup"><span data-stu-id="f6a67-220">4.7.</span></span> <span data-ttu-id="f6a67-221">กลับไปยัง Finance and Operations และรีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="f6a67-221">Return to Finance and Operations and refresh the page.</span></span> <span data-ttu-id="f6a67-222">ค่าที่เผยแพร่แล้วจะปรากฏขึ้นใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6a67-222">Published values will appear in Finance and Operations.</span></span> 

<span data-ttu-id="f6a67-223">[![รีเฟรช](./media/screenshot23.png)](./media/screenshot23.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-223">[![Refresh](./media/screenshot23.png)](./media/screenshot23.png)</span></span>

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a><span data-ttu-id="f6a67-224">งานที่ 5: สร้างแม่แบบและโครงร่างเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-224">Task 5: Create budget plan document layouts and templates</span></span>
<span data-ttu-id="f6a67-225">โครงร่างกำหนดวิธีตารางบรรทัดเอกสารของแผนงบประมาณที่จะดูคล้ายกันเมื่อผู้ใช้เปิดเอกสารแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-225">Layout defines how budget plan document lines grid is going to look like when user opens budget plan document.</span></span> <span data-ttu-id="f6a67-226">จึงจะสามารถสลับโครงร่างสำหรับเอกสารแผนงบประมาณเมื่อต้องการดูข้อมูลเดียวกันในมุมที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f6a67-226">It is also possible to switch the layout for budget plan document to see the same data in different angles.</span></span> <span data-ttu-id="f6a67-227">ตอนนี้ ขณะเธอยังได้รับคอลัมน์ที่กำหนดไว้เพื่อใช้กับเอกสารแผนงบประมาณของเรา Julia จำเป็นต้องสร้างโครงร่างเอกสารแผนงบประมาณ ที่มีลักษณะคล้ายกับตาราง Excel เธอใช้ในการสร้างข้อมูลงบประมาณ (ดูภาพรวมของส่วนสถานการณ์จำลองในห้องปฏิบัติการนี้)</span><span class="sxs-lookup"><span data-stu-id="f6a67-227">Now, as she’s got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data (see section Scenario overview in this lab)</span></span> 

<span data-ttu-id="f6a67-228">5.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-228">5.1.</span></span> <span data-ttu-id="f6a67-229">ในการจัดงบประมาณ&gt;ตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณเปิดหน้าโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="f6a67-229">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Layouts page.</span></span> <span data-ttu-id="f6a67-230">สร้างโครงร่างใหม่สำหรับรายการบัญชีงบประมาณรายเดือน:</span><span class="sxs-lookup"><span data-stu-id="f6a67-230">Create a new layout for Monthly budget entry:</span></span>

-   <span data-ttu-id="f6a67-231">เลือกเซ็ตมิติ MA+BU ที่จะรวมบัญชีหลักและหน่วยธุรกิจจนถึงโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="f6a67-231">Pick MA+BU dimension set to include Main accounts and Business units to the layout.</span></span>
-   <span data-ttu-id="f6a67-232">แสดงรายการคอลัมน์แผนงบประมาณทั้งหมดที่สร้างขึ้นในขั้นตอนก่อนหน้านี้ในส่วนขององค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6a67-232">List all budget plan columns created in the previous step in the Elements section.</span></span> <span data-ttu-id="f6a67-233">สร้างทั้งหมดแต่ก่อนหน้าปีที่เกิดขึ้นจริงสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="f6a67-233">Make all but Previous year actuals editable.</span></span>
-   <span data-ttu-id="f6a67-234">คลิกปุ่มคำอธิบายเกี่ยวกับการเลือกมิติทางการเงินที่ควรแสดงคำอธิบายในกริด</span><span class="sxs-lookup"><span data-stu-id="f6a67-234">Click Descriptions button to select which financial dimensions should display Descriptions in the grid.</span></span>

<span data-ttu-id="f6a67-235">[![คำอธิบาย](./media/screenshot24.png)](./media/screenshot24.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-235">[![Descriptions](./media/screenshot24.png)](./media/screenshot24.png)</span></span> 

<span data-ttu-id="f6a67-236">ยึดตามงบประมาณของแผนคำนิยามโครงร่างที่เราสามารถสร้างเท็มเพลต Excel เพื่อใช้เป็นทางเลือกที่จะแก้ไขข้อมูลงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-236">Based on the budget plan layout definition we can create an Excel template to be used as an alternative way to edit Budget data.</span></span> <span data-ttu-id="f6a67-237">ตามที่มีเท็มเพลต Excel เพื่อให้ตรงกับคำนิยามโครงร่างของแผนงบประมาณ คุณจะไม่สามารถแก้ไขโครงร่างของแผนงบประมาณหลังจากการสร้างเท็มเพลต Excel ดังนั้น งานนี้ควรทำหลังจากที่มีกำหนดส่วนประกอบทั้งหมดของโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="f6a67-237">As Excel template has to match budget plan layout definition, you won’t be able to edit budget plan layout after generating Excel template, therefore this task should be done after all layout components are defined.</span></span> 

<span data-ttu-id="f6a67-238">5.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-238">5.2.</span></span> <span data-ttu-id="f6a67-239">สำหรับโครงร่างที่สร้างใน 5.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-239">For the layout created in the 5.1.</span></span> <span data-ttu-id="f6a67-240">ขั้นตอน คลิกปุ่มเท็มเพลต &gt; สร้าง</span><span class="sxs-lookup"><span data-stu-id="f6a67-240">step, click button Template &gt; Generate.</span></span> <span data-ttu-id="f6a67-241">ยืนยันข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="f6a67-241">Confirm the warning message.</span></span> <span data-ttu-id="f6a67-242">เพื่อดูเท็มเพลต คลิกเท็มเพลต &gt; มุมมอง</span><span class="sxs-lookup"><span data-stu-id="f6a67-242">To view the template, click Template &gt; View.</span></span> 

<span data-ttu-id="f6a67-243">*หมายเหตุ: ตรวจสอบให้แน่ใจว่าได้เลือก "บันทึกเป็น" แล้วเลือกตำแหน่งที่จะจัดเก็บเท็มเพลตเพื่อที่จะแก้ไข ถ้าผู้ใช้เลือก "เปิด" ในกล่องโต้ตอบโดยไม่ได้บันทึก การเปลี่ยนแปลงไฟล์นั้นจะไม่ถูกเก็บไว้เมื่อไฟล์ถูกปิด* 
[![มุมมองเท็มเพลต](./media/screenshot25.png)](./media/screenshot25.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-243">*Note: Make sure to select “Save as” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png)</span></span> 

<span data-ttu-id="f6a67-244">5.3</span><span class="sxs-lookup"><span data-stu-id="f6a67-244">5.3.</span></span> <span data-ttu-id="f6a67-245">&lt; ขั้นตอนเพิ่มเติม&gt; เท็มเพลต Excel ปรับเปลี่ยนเพื่อทำให้ผู้ใช้ใช้งานได้ง่ายขึ้น – ดูเพิ่มสูตรรวม ฟิลด์หัวข้อ การจัดรูปแบบ เป็นต้น บันทึกการเปลี่ยนแปลง และอัพโหลดไฟล์โครงร่างของแผนงบประมาณ โดยคลิกที่โครงร่าง &gt; อัพโหลด [![อัพโหลด](./media/screenshot26.png)](./media/screenshot26.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-245">&lt; Optional step&gt; Modify Excel template to make it look more user friendly – add total formulas, header fields, formatting, etc. Save the changes and upload the file to budget plan layout by clicking Layout &gt; Upload [![Upload](./media/screenshot26.png)](./media/screenshot26.png)</span></span>

### <a name="task-6-create-a-budget-planning-process"></a><span data-ttu-id="f6a67-246">งานที่ 6: สร้างกระบวนการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-246">Task 6: Create a budget planning process</span></span>
<span data-ttu-id="f6a67-247">Julia จำเป็นต้องสร้าง และเรียกใช้กระบวนการวางแผนงบประมาณใหม่รวมกับการตั้งค่าข้างต้นเพื่อเริ่มป้อนการวางแผนงบประมาณใหม่</span><span class="sxs-lookup"><span data-stu-id="f6a67-247">Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans.</span></span> <span data-ttu-id="f6a67-248">กระบวนการวางแผนงบประมาณกำหนดจัดทำงบประมาณองค์กร ลำดับงาน โครงร่าง และเท็มเพจจะใช้สำหรับการสร้างแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-248">Budget planning process defines what budgeting organizations, workflow, layouts and templates will be used for creating budget plans.</span></span> 

<span data-ttu-id="f6a67-249">6.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-249">6.1.</span></span> <span data-ttu-id="f6a67-250">นำไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; กระบวนการวางแผนงบประมาณ และสร้างเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="f6a67-250">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process and create a new record.</span></span>

-   <span data-ttu-id="f6a67-251">กระบวนการวางแผนงบประมาณ – DEMF budgeting FY2016</span><span class="sxs-lookup"><span data-stu-id="f6a67-251">Budget planning process – DEMF budgeting FY2016</span></span>
-   <span data-ttu-id="f6a67-252">วงจรงบประมาณ – FY2016</span><span class="sxs-lookup"><span data-stu-id="f6a67-252">Budget cycle – FY2016</span></span>
-   <span data-ttu-id="f6a67-253">บัญชีแยกประเภท– DEMF</span><span class="sxs-lookup"><span data-stu-id="f6a67-253">Ledger – DEMF</span></span>
-   <span data-ttu-id="f6a67-254">โครงสร้างทางบัญชีเริ่มต้น – Manufacturing P&L</span><span class="sxs-lookup"><span data-stu-id="f6a67-254">Default account structure – Manufacturing P&L</span></span>
-   <span data-ttu-id="f6a67-255">ลำดับชั้นขององค์กร – เลือกลำดับชั้นสร้างขึ้นตั้งแต่ขั้นเริ่มต้นในห้องปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="f6a67-255">Organization hierarchy – pick the hierarchy created in the beginning of the lab</span></span>
-   <span data-ttu-id="f6a67-256">ลำดับงานของการวางแผนงบประมาณ –มอบหมายอัตโนมัติ – อนุมัติลำดับงานสำหรับแผนกการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6a67-256">Budget planning workflow – assign Auto – Approve workflow for Finance department</span></span>
-   <span data-ttu-id="f6a67-257">ในกฎขั้นการวางแผนงบประมาณและเท็มเพลต เลือกสำหรับแต่ละลำดับงานงบประมาณ ถ้าได้อนุญาตการเพิ่มรายการ และแก้ไขรายการ และสิ่งที่โครงร่างควรจะใช้โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6a67-257">In budget planning stage rules and templates, for each workflow Budget planning stage pick if Adding lines and Modifying lines is allowed and what Layout should be used by default</span></span>

<span data-ttu-id="f6a67-258">*หมายเหตุ: คุณสามารถสร้างโครงร่างเอกสารเพิ่มเติม และกำหนดค่าให้พร้อมใช้งานในขั้นลำดับงานของการวางแผนงบประมาณ ด้วยการคลิกปุ่มเค้าโครงสำรอง*</span><span class="sxs-lookup"><span data-stu-id="f6a67-258">*Note: You can create additional document layouts and assign them to be available in budget planning workflow stage by clicking Alternate layouts button.*</span></span> 

<span data-ttu-id="f6a67-259">[![โครงร่างรอง](./media/screenshot27.png)](./media/screenshot27.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-259">[![Alternate layouts](./media/screenshot27.png)](./media/screenshot27.png)</span></span> 

<span data-ttu-id="f6a67-260">6.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-260">6.2.</span></span> <span data-ttu-id="f6a67-261">เลือกการดำเนินการ &gt; เปิดใช้งานเพื่อเรียกใช้ลำดับงานของแผนงบประมาณนี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-261">Select Actions &gt; Activate to activate this budget planning workflow</span></span> 

<span data-ttu-id="f6a67-262">[![เปิดใช้งาน](./media/screenshot28.png)](./media/screenshot28.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-262">[![Activate](./media/screenshot28.png)](./media/screenshot28.png)</span></span>

## <a name="exercise-2-process-simulation"></a><span data-ttu-id="f6a67-263">แบบฝึกหัดที่ 2: การจำลองกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="f6a67-263">Exercise 2: Process simulation</span></span>

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a><span data-ttu-id="f6a67-264">งานที่ 7: สร้างข้อมูลเริ่มต้นสำหรับแผนงบประมาณจากรายการบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="f6a67-264">Task 7: Generate initial data for budget plan from General ledger</span></span>
<span data-ttu-id="f6a67-265">7.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-265">7.1.</span></span> <span data-ttu-id="f6a67-266">นำไปยังการจัดทำงบประมาณ &gt; งานประจำงวด &gt; สร้างรายการแผนงบประมาณจากบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="f6a67-266">Navigate to Budgeting &gt; Periodic &gt; Generate budget plan from General ledger.</span></span> <span data-ttu-id="f6a67-267">กรอกข้อมูลพารามิเตอร์กระบวนการเป็นครั้งคราว และคลิกปุ่มสร้าง</span><span class="sxs-lookup"><span data-stu-id="f6a67-267">Fill in the periodic process parameters and click button Generate.</span></span> 

<span data-ttu-id="f6a67-268">[![สร้าง](./media/screenshot29.png)](./media/screenshot29.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-268">[![Generate](./media/screenshot29.png)](./media/screenshot29.png)</span></span> 

<span data-ttu-id="f6a67-269">7.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-269">7.2.</span></span> <span data-ttu-id="f6a67-270">ไปยังการจัดทำงบประมาณ &gt; แผนงบประมาณเพื่อหาแผนงบประมาณที่สร้างขึ้นโดยการสร้างกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="f6a67-270">Navigate to Budgeting &gt; Budget plans to find a budget plan created by Generate process.</span></span> 

<span data-ttu-id="f6a67-271">[![แผนงบประมาณ](./media/screenshot30.png)](./media/screenshot30.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-271">[![Budget plan](./media/screenshot30.png)](./media/screenshot30.png)</span></span> 

<span data-ttu-id="f6a67-272">7.3</span><span class="sxs-lookup"><span data-stu-id="f6a67-272">7.3.</span></span> <span data-ttu-id="f6a67-273">เปิดรายละเอียดเอกสาร โดยคลิกที่ไฮเปอร์ลิงค์หมายเลขเอกสาร</span><span class="sxs-lookup"><span data-stu-id="f6a67-273">Open document details by clicking on Document number hyperlink.</span></span> <span data-ttu-id="f6a67-274">แผนงบประมาณจะแสดงขึ้นตามที่กำหนดไว้ในโครงร่างที่สร้างขึ้นในห้องปฏิบัติการนี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-274">Budget plan is displayed as defined in the layout created during this lab</span></span> 

<span data-ttu-id="f6a67-275">[![การแสดงแผนงบประมาณ](./media/screenshot31.png)](./media/screenshot31.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-275">[![Budget plan display](./media/screenshot31.png)](./media/screenshot31.png)</span></span>

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a><span data-ttu-id="f6a67-276">งานที่ 8: สร้างงบประมาณปีปัจจุบันตามจริงของปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f6a67-276">Task 8: Create current year budget based on previous year actuals</span></span>
<span data-ttu-id="f6a67-277">สามารถใช้วิธีการปันส่วนในแผนงบประมาณเพื่อคัดลอกข้อมูลสำหรับแผนงบประมาณได้โดยง่ายจากสถานการณ์จำลองหนึ่งไปอีกสถานการณ์จำลองหนึ่ง/ กระจายเหล่านั้นข้ามรอบระยะเวลา /ปันส่วนไปยังกับมิติ</span><span class="sxs-lookup"><span data-stu-id="f6a67-277">Allocation methods can be used in budget plan to easily copy information for budget plans from one scenario to another/ spread them across periods/ allocate to dimensions.</span></span> <span data-ttu-id="f6a67-278">เราจะใช้การปันส่วนเพื่อสร้างงบประมาณปีปัจจุบันจากยอดจริงในปีก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="f6a67-278">We will use allocations to create current year budget from previous year actuals.</span></span> 

<span data-ttu-id="f6a67-279">8.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-279">8.1.</span></span> <span data-ttu-id="f6a67-280">เลือกรายการทั้งหมดในกริดเอกสารแผนงบประมาณ และคลิกปุ่มปันส่วนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-280">Pick all lines in the budget plan document grid and click button allocate budget</span></span> 

<span data-ttu-id="f6a67-281">[![รายการทั้งหมด](./media/screenshot32.png)](./media/screenshot32.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-281">[![All lines](./media/screenshot32.png)](./media/screenshot32.png)</span></span> 

<span data-ttu-id="f6a67-282">8.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-282">8.2.</span></span> <span data-ttu-id="f6a67-283">เลือกวิธีการปันส่วน คีย์รอบระยะเวลา สถานการณ์จำลองต้นทางและปลายทาง และคลิกปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6a67-283">Select allocation method, Period key, Source and destination scenarios and click Allocate</span></span> 

<span data-ttu-id="f6a67-284">[![ปันส่วน](./media/screenshot33.png)](./media/screenshot33.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-284">[![Allocate](./media/screenshot33.png)](./media/screenshot33.png)</span></span>

<span data-ttu-id="f6a67-285">ยอดเงินจริงของปีก่อนหน้านี้จะถูกคัดลอกไปยังงบประมาณปีปัจจุบัน และปันส่วนให้รอบระยะเวลาต่าง ๆ โดยใช้คีย์รอบระยะเวลาของเส้นขาย</span><span class="sxs-lookup"><span data-stu-id="f6a67-285">The previous year actual amounts will be copied to current year budget and allocate them across periods using Sales curve period key.</span></span> 

<span data-ttu-id="f6a67-286">[![เส้นโค้งการขาย](./media/screenshot34.png)](./media/screenshot34.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-286">[![Sales curve](./media/screenshot34.png)](./media/screenshot34.png)</span></span>

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a><span data-ttu-id="f6a67-287">งานที่ 9: การปรับปรุงเอกสารแผนงบประมาณโดยใช้ Excel และเอกสารขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f6a67-287">Task 9: Adjust budget plan document using Excel and finalize the document</span></span>
<span data-ttu-id="f6a67-288">9.1</span><span class="sxs-lookup"><span data-stu-id="f6a67-288">9.1.</span></span> <span data-ttu-id="f6a67-289">คลิกปุ่มแผ่นงานเพื่อเปิดเนื้อหาเอกสารใน Excel</span><span class="sxs-lookup"><span data-stu-id="f6a67-289">Click Button worksheet to open document contents in Excel</span></span>

<span data-ttu-id="f6a67-290">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-290">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span></span>

<span data-ttu-id="f6a67-291">9.2</span><span class="sxs-lookup"><span data-stu-id="f6a67-291">9.2.</span></span> <span data-ttu-id="f6a67-292">เมื่อเปิดสมุดงาน Excel ปรับปรุงหมายเลขในเอกสารแผนงบประมาณและคลิกปุ่มเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f6a67-292">When Excel workbook opens, adjust the numbers in budget plan document and click button Publish.</span></span>

<span data-ttu-id="f6a67-293">[![เผยแพร่](./media/screenshot36.png)](./media/screenshot36.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-293">[![Publish](./media/screenshot36.png)](./media/screenshot36.png)</span></span>

<span data-ttu-id="f6a67-294">9.3</span><span class="sxs-lookup"><span data-stu-id="f6a67-294">9.3.</span></span> <span data-ttu-id="f6a67-295">กลับไปยังเอกสารแผนงบประมาณใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6a67-295">Return to budget plan document in Finance and Operations.</span></span> <span data-ttu-id="f6a67-296">คลิกลำดับงาน &gt; ส่งเอกสารเพื่ออนุมัติอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f6a67-296">Click Workflow &gt; Submit to Auto-approve the document</span></span>

<span data-ttu-id="f6a67-297">[![การอนุมัติอัตโนมัติ](./media/screenshot37.png)](./media/screenshot37.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-297">[![Auto-approve](./media/screenshot37.png)](./media/screenshot37.png)</span></span> 

<span data-ttu-id="f6a67-298">หลังจากที่ลำดับงานเสร็จสมบูรณ์ ขั้นเอกสารแผนงบประมาณจะเปลี่ยนเป็น อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="f6a67-298">Once workflow completes, budget plan document stage changes to Approved.</span></span> <span data-ttu-id="f6a67-299">[![อนุมัติแล้ว](./media/screenshot38.png)](./media/screenshot38.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-299">[![Approved](./media/screenshot38.png)](./media/screenshot38.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="f6a67-300">ภาคผนวก</span><span class="sxs-lookup"><span data-stu-id="f6a67-300">Appendix</span></span>

### <a name="auto-approve-workflow-configuration"></a><span data-ttu-id="f6a67-301">การตั้งค่าคอนฟิกลำดับงานอนุมัติอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f6a67-301">Auto-Approve workflow configuration</span></span>

<span data-ttu-id="f6a67-302">A.</span><span class="sxs-lookup"><span data-stu-id="f6a67-302">A.</span></span> <span data-ttu-id="f6a67-303">การจัดงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; ลำดับงานของการวางแผนสร้างลำดับงานใหม่โดยใช้ลำดับงานการวางแผนงบประมาณเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f6a67-303">Budgeting &gt; Setup &gt; Budget planning &gt; Budgeting workflows Create a new workflow using template Budget planning workflows:</span></span>

<span data-ttu-id="f6a67-304">[![สร้างลำดับงานใหม่](./media/screenshot39.png)](./media/screenshot39.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-304">[![Create a new workflow](./media/screenshot39.png)](./media/screenshot39.png)</span></span>

<span data-ttu-id="f6a67-305">ลำดับงานนี้จะประกอบด้วยงานเพียงหนึ่งรายการ – การเปลี่ยนขั้นของแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-305">This workflow will contain only one task – Stage transition budget plan</span></span> 

<span data-ttu-id="f6a67-306">[![การเปลี่ยนขั้นของแผนงบประมาณ](./media/screenshot40.png)](./media/screenshot40.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-306">[![Stage transition budget plan](./media/screenshot40.png)](./media/screenshot40.png)</span></span> 

<span data-ttu-id="f6a67-307">บันทึกและเรียกใช้ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f6a67-307">Save and activate the workflow.</span></span> 

<span data-ttu-id="f6a67-308">B.</span><span class="sxs-lookup"><span data-stu-id="f6a67-308">B.</span></span> <span data-ttu-id="f6a67-309">นำทางไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-309">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="f6a67-310">ในแท็บขั้น สร้าง 2 ขั้น – เริ่มต้นและส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="f6a67-310">In Stages tab create 2 stages – Initial and Submitted</span></span> 

<span data-ttu-id="f6a67-311">[![เริ่มต้นและขั้นส่ง](./media/screenshot41.png)](./media/screenshot41.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-311">[![Initial and submitted](./media/screenshot41.png)](./media/screenshot41.png)</span></span>

<span data-ttu-id="f6a67-312">C.</span><span class="sxs-lookup"><span data-stu-id="f6a67-312">C.</span></span> <span data-ttu-id="f6a67-313">นำทางไปยังการจัดทำงบประมาณ &gt; การตั้งค่า &gt; การวางแผนงบประมาณ &gt; การตั้งค่าคอนฟิกการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f6a67-313">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="f6a67-314">ในแท็บขั้นลำดับงานเชื่อมโยงลำดับงานอนุมัติอัตโนมัติสร้างขึ้นในขั้นเริ่มต้นและขั้นส่ง</span><span class="sxs-lookup"><span data-stu-id="f6a67-314">In Workflow Stages tab Associate the workflow Auto – approve created in A step with the stages Initial and Submitted</span></span> 

<span data-ttu-id="f6a67-315">[![การจัดงบประมาณและการวางแผนงบประมาณ](./media/screenshot42.png)](./media/screenshot42.png)</span><span class="sxs-lookup"><span data-stu-id="f6a67-315">[![Budgeting and budget planning](./media/screenshot42.png)](./media/screenshot42.png)</span></span>  




