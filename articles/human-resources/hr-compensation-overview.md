---
title: แผนค่าตอบแทน
description: ค่าตอบแทนและสวัสดิการผู้จัดการสามารถใช้การจัดการค่าตอบแทนเพื่อรักษาและประมวลผลแผนค่าตอบแทนคงที่และผันแปรสำหรับพนักงานขององค์กร
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: d683b0b140592e4c93a68f7f58c7d13475b4c2a5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189612"
---
# <a name="compensation-plans"></a><span data-ttu-id="5f951-103">แผนค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-103">Compensation plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5f951-104">ค่าตอบแทนและสวัสดิการผู้จัดการสามารถใช้การจัดการค่าตอบแทนเพื่อรักษาและประมวลผลแผนค่าตอบแทนคงที่และผันแปรสำหรับพนักงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5f951-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="5f951-105">คำนำ</span><span class="sxs-lookup"><span data-stu-id="5f951-105">Introduction</span></span>

<span data-ttu-id="5f951-106">การจัดการค่าตอบแทนจะใช้ควบคุมการจัดส่งของค่าจ้างพื้นฐานและเงินรางวัล</span><span class="sxs-lookup"><span data-stu-id="5f951-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="5f951-107">ค่าจ้างพื้นฐานคงที่ของพนักงานและการขึ้นค่าตอบแทนตามผลงานจะถูกควบคุมโดยใช้แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5f951-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="5f951-108">ค่าจ้างจูงใจเช่นการชำระเงินโบนัส รางวัลตามผลการปฏิบัติงาน สิทธิในการซื้อหุ้น การให้หุ้น รางวัลที่จ่ายครั้งเดียว โดยใช้แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5f951-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="5f951-109">พนักงานสามารถลงทะเบียนในแผนทั้งสองชนิดได้หนึ่งแผนขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="5f951-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="5f951-110">พนักงานต้องต้องมีคุณสมบัติตามข้อกำหนดต่อไปนี้เพื่อให้มีสิทธิ์สำหรับการลงทะเบียนในแผนค่าตอบแทน:</span><span class="sxs-lookup"><span data-stu-id="5f951-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="5f951-111">พนักงานต้องมีการมอบหมายตำแหน่งที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="5f951-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="5f951-112">พนักงานต้องตรงกับเงื่อนไขกำหนดไว้โดยกฎการมีสิทธิ์สำหรับแผนค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="5f951-113"> การตั้งค่าค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-113">Compensation setup</span></span>
<span data-ttu-id="5f951-114">ตารางต่อไปนี้แสดงรายการส่วนประกอบของกระบวนการค่าตอบแทนที่สามารถรวมในการตั้งค่าแผนค่าตอบแทนของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="5f951-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5f951-115">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5f951-115">Component</span></span></th>
<th><span data-ttu-id="5f951-116">ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5f951-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f951-117">การดำเนินการเกี่ยวกับค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5f951-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="5f951-118">การดำเนินการเกี่ยวกับค่าตอบแทนคงที่ ซึ่งมีวัตถุประสงค์สองประการคือ:</span><span class="sxs-lookup"><span data-stu-id="5f951-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="5f951-119">การดำเนินการสามารถระบุชนิดของข้อมูลที่จะต้องบันทึกเมื่อมีการเปลี่ยนแปลงของค่าตอบแทนของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="5f951-120">ตัวอย่างเช่น คุณสามารถกำหนดว่าเหตุผลที่เปลี่ยนแปลง เช่นการเลื่อนตำแหน่งหรือลดตำแหน่งจะถูกบันทึกเป็นต้น</span><span class="sxs-lookup"><span data-stu-id="5f951-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="5f951-121">การดำเนินการสามารถให้แน่ใจว่าการคำนวณจะถูกใช้เมื่อแผนค่าตอบแทนคงที่มีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="5f951-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="5f951-122">ตัวอย่างเช่น การดำเนินการของชนิดหุ้นทุนจะเปรียบเทียบค่าจ้างพนักงานกับจุดอ้างอิงต่ำสุดสำหรับระดับในพนักงาน&#39;และให้แน่ใจว่าพนักงานได้รับการจ่ายเงินขั้นต่ำเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="5f951-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-123">ระดับ</span><span class="sxs-lookup"><span data-stu-id="5f951-123">Levels</span></span></td>
<td><span data-ttu-id="5f951-124">ระดับจะสัมพันธ์กับงานและตำแหน่งงานใดๆที่เกี่ยวข้องกับการอ้างอิงงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="5f951-125">คุณสามารถสร้างระดับที่ไม่ต่อเนื่องสำหรับแผนค่าตอบแทนทั้งสามชนิด: ระดับ แถบ และขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="5f951-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-126">เมทริกซ์การใช้ช่วงค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5f951-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="5f951-127">เมทริกซ์การใช้ช่วงค่าจ้างช่วยคุณเปลี่ยนพนักงานไปยังจุดควบคุมสำหรับงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="5f951-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="5f951-128">นอกจากนี้ คุณยังสามารถใช้การใช้ประโยชน์ของช่วงเพื่อควบคุมหุ้นทุนของอัตราค่าจ้างในบริษัท โดยไม่คำนึงถึงประสิทธิภาพของ&#39;พนักงานแต่ละราย หรือประสิทธิภาพโดยรวมของบริษัท</span><span class="sxs-lookup"><span data-stu-id="5f951-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="5f951-129">ตัวอย่างเช่น พนักงานที่ได้รับค่าจ้างต่ำกว่าในช่วงของตนได้เพิ่มเปอร์เซ็นต์ที่สูงกว่าพนักงานที่ได้รับค่าจ้างสูงกว่าในช่วงนั้น</span><span class="sxs-lookup"><span data-stu-id="5f951-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="5f951-130">ในลักษณะนี้ คุณสามารถออฟเซ็ตความแตกต่างของผู้ถือหุ้นอย่างเป็นระบบ</span><span class="sxs-lookup"><span data-stu-id="5f951-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="5f951-131">การใช้ช่วงค่าจ้างมีคำนวณดังนี้: (อัตราค่าจ้างคงที่ - ค่าต่ำสุดของช่วง ) ÷ (ค่าสูงสุดของช่วง - ค่าต่ำสุดของช่วง)</span><span class="sxs-lookup"><span data-stu-id="5f951-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-132">การตั้งค่าจุดอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="5f951-132">Reference point setups</span></span></td>
<td><span data-ttu-id="5f951-133">สร้างการตั้งค่าจุดอ้างอิงรวมถึงชุดของจุดอ้างอิงที่แสดงถึงช่วงในเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="5f951-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="5f951-134">แต่ละช่วงสามารถเชื่อมโยงกับอัตราค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5f951-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="5f951-135">ตัวอย่างเช่น ระดับแผนมักจะมีจุดอ้างอิงค่าต่ำสุด จุดกึ่งกลาง และสูงสุด</span><span class="sxs-lookup"><span data-stu-id="5f951-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-136">เมทริกซ์ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="5f951-137">เมทริกซ์ค่าตอบแทนคือชุดของจุดอ้างอิงและระดับที่คุณใช้เพื่อสร้างโครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-138">โครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-138">Compensation structure</span></span></td>
<td><span data-ttu-id="5f951-139">โครงสร้างแผนค่าตอบแทนเป็นเมทริกซ์ค่าตอบแทนที่มีอัตราการชำระค่าจ้างที่สัมพันธ์กับจุดอ้างอิงสำหรับแต่ละระดับ</span><span class="sxs-lookup"><span data-stu-id="5f951-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-140">กฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="5f951-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="5f951-141">กฎการมีคุณสมบัติเหมาะสมจะใช้เพื่อระบุถึงพนักงานในงานเฉพาะ ฟังก์ชันงาน ชนิดงาน แผนก สหภาพแรงงาน หรือภูมิภาคของค่าตอบแทนที่ครอบคลุมโดยแผนค่าตอบแทนที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="5f951-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="5f951-142">คุณต้องสร้างกฎการมีคุณสมบัติเหมาะสมสำหรับทั้งแผนค่าตอบแทนคงที่และผันแปรเพื่อลงทะเบียนพนักงานในแผน</span><span class="sxs-lookup"><span data-stu-id="5f951-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="5f951-143">หลังจากที่คุณระบุกฎการมีคุณสมบัติเหมาะสมสำหรับแผนค่าตอบแทนแล้ว คุณสามารถกำหนดระดับที่ควรใช้กับงานที่ครอบคลุมโดยแผนนั้นได้</span><span class="sxs-lookup"><span data-stu-id="5f951-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-144">ความถี่ในการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5f951-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="5f951-145">ความถี่ในการชำระค่าจ้างจะใช้เพื่อกำหนดรอบระยะเวลาสำหรับค่าตอบแทนที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5f951-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="5f951-146">ตัวอย่างเช่น ความถี่ในการชำระค่าจ้างช่วยให้คุณเข้าใจถ้ายอดเงินค่าตอบแทนที่มีการระบุตามเงินเดือนต่อปี เทียบกับอัตราค่าจ้างต่อชัวโมง</span><span class="sxs-lookup"><span data-stu-id="5f951-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="5f951-147">ความถี่ในการชำระค่าจ้างยังใช้ในการตั้งค่าตัวคูณการแปลงเพื่อแปลงยอดเงินค่าตอบแทนจาก รายเดือน รายสัปดาห์ รายสองสัปดาห์ และรายชั่วโมง ไปเป็นความถี่ในการชำระค่าจ้างรายปี</span><span class="sxs-lookup"><span data-stu-id="5f951-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-148">ภูมิภาคของค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-148">Compensation regions</span></span></td>
<td><span data-ttu-id="5f951-149">ภูมิภาคของค่าตอบแทนใช้ระบุค่าตอบแทนของพนักงานตามสถานที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-150">จุดควบคุม</span><span class="sxs-lookup"><span data-stu-id="5f951-150">Control point</span></span></td>
<td><span data-ttu-id="5f951-151">จุดควบคุมกำหนดสิ่งที่ควรพิจารณาเป็นอัตราค่าจ้างที่เหมาะสมที่สุดสำหรับพนักงานทุกคนในระดับค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="5f951-152">สำหรับโครงสร้างแผนระดับ โดยทั่วไปจุดควบคุมคือจุดกึ่งกลางของช่วง</span><span class="sxs-lookup"><span data-stu-id="5f951-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="5f951-153">โครงสร้างแถบไม่ค่อยใช้จุดควบคุม</span><span class="sxs-lookup"><span data-stu-id="5f951-153">Band structures rarely use control points.</span></span> <span data-ttu-id="5f951-154">คุณสามารถระบุจุดควบคุมสำหรับแผนค่าตอบแทนคงที่ในแบบฟอร์มแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5f951-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-155">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-155">Job functions</span></span></td>
<td><span data-ttu-id="5f951-156">ฟังก์ชันงานจะใช้เพื่อจัดประเภทและกรองข้อมูลแผนค่าตอบแทนสำหรับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="5f951-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-157">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-157">Job types</span></span></td>
<td><span data-ttu-id="5f951-158">ชนิดงานจะใช้เพื่อจัดประเภทและกรองข้อมูลแผนค่าตอบแทนสำหรับงานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="5f951-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-159">ชนิดของค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5f951-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="5f951-160">ชนิดค่าตอบแทนผันแปร เช่นรางวัลหุ้นสามัญหรือโบนัสเงินสด มีตั้งค่าในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5f951-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-161">กริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-161">Compensation grids</span></span></td>
<td><span data-ttu-id="5f951-162">กริดค่าตอบแทนประกอบด้วยโครงสร้างค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="5f951-163">สามารถใช้กริดค่าตอบแทนโดยแผนค่าตอบแทนหนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="5f951-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f951-164">แผนการปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-164">Performance plans</span></span></td>
<td><span data-ttu-id="5f951-165">แผนการปฏิบัติงานจะใช้เชื่อมโยงการปฏิบัติงานกับเมทริกซ์การปันส่วน ดังนั้นคุณสามารถใช้แผนนั้นในกลยุทธ์การจ่ายค่าจ้างตามผลการปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5f951-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f951-166">การจัดอันดับประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="5f951-166">Performance ratings</span></span></td>
<td><span data-ttu-id="5f951-167">การประเมินผลการปฏิบัติงานจะใช้ในแผนการปฏิบัติงานเพื่อกำหนดยอดเงินรางวัลสำหรับการปฏิบัติงานดีหรือรางวัลสำหรับประสิทธิภาพการทำงานยอดเยี่ยม</span><span class="sxs-lookup"><span data-stu-id="5f951-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="5f951-168">เหตุการณ์กระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5f951-168">Process events</span></span>
<span data-ttu-id="5f951-169">เหตุการณ์ในกระบวนการคำนวณข้อมูลค่าตอบแทนสำหรับรอบระยะเวลาที่ระบุสำหรับพนักงานทั้งหมดที่ลงทะเบียนในแผนค่าตอบแทนคงที่หรือผันแปรหนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="5f951-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="5f951-170">คุณสามารถรันเหตุการณ์ในกระบวนการซ้ำ ๆ เพื่อทดสอบหรืออัพเดตผลค่าตอบแทนที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="5f951-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

## <a name="compensation-events"></a><span data-ttu-id="5f951-171">เหตุการณ์ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-171">Compensation events</span></span>

<span data-ttu-id="5f951-172">แต่ละครั้งที่รันเหตุการณ์ในกระบวนการ จะมีการสร้างเหตุการณ์ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5f951-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="5f951-173">เหตุการณ์ค่าตอบแทนประกอบด้วยผลลัพธ์ของกระบวนการค่าตอบแทนสำหรับพนักงานแต่ละคนที่รวมอยู่ในเหตุการณ์กระบวนการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="5f951-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="5f951-174">เมื่อการคำนวณถูกต้อง คุณจะสามารถโหลดเหตุการณ์ค่าตอบแทนเพื่ออัพเดตเรกคอร์ดค่าตอบแทนสำหรับพนักงานที่ได้รับผลกระทบโดยเหตุการณ์ในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5f951-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="5f951-175"> คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="5f951-175">Recommendations</span></span>
<span data-ttu-id="5f951-176">หลังจากที่คุณรันเหตุการณ์ในกระบวนการ คุณจะสามารถแนะนำการปรับปรุงการขึ้นค่าตอบแทนของพนักงานหรือยอดเงินรางวัล ตามคำแนะนำที่คำนวณได้ของเหตุการณ์ในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5f951-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="5f951-177">เมื่อต้องการสร้างคำแนะนำสำหรับพนักงาน คุณต้องเปิดใช้งานคำแนะนำเมื่อคุณตั้งค่าแผนค่าตอบแทนหรือเมื่อคุณตั้งค่าเหตุการณ์ในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5f951-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]