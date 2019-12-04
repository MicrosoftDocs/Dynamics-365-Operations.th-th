---
title: การคำนวณค่าโสหุ้ย
description: หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770815"
---
# <a name="overhead-calculation"></a><span data-ttu-id="04890-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="04890-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04890-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="04890-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="04890-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="04890-105">Term definition</span></span>
---------------

<span data-ttu-id="04890-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="04890-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="04890-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="04890-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="04890-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="04890-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="04890-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="04890-109">Rent</span></span>
-   <span data-ttu-id="04890-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-110">Electricity</span></span>
-   <span data-ttu-id="04890-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="04890-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="04890-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="04890-112">Overhead calculation overview</span></span>
<span data-ttu-id="04890-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="04890-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="04890-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="04890-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="04890-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="04890-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="04890-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="04890-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="04890-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="04890-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="04890-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="04890-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="04890-119">Version type</span></span>
-   <span data-ttu-id="04890-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="04890-120">Date and time</span></span>
-   <span data-ttu-id="04890-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="04890-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-122">Fiscal year</span></span>
-   <span data-ttu-id="04890-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-123">Fiscal period</span></span>

<span data-ttu-id="04890-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="04890-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="04890-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="04890-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="04890-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04890-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="04890-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="04890-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="04890-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="04890-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="04890-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="04890-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="04890-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="04890-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="04890-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="04890-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="04890-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="04890-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="04890-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="04890-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="04890-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="04890-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="04890-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="04890-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04890-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04890-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="04890-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="04890-140">Main account</span></span></th>
<th><span data-ttu-id="04890-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="04890-143">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-143">CC099</span></span></td>
<td><span data-ttu-id="04890-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-144">Default cost center</span></span></td>
<td><span data-ttu-id="04890-145">10001</span><span class="sxs-lookup"><span data-stu-id="04890-145">10001</span></span></td>
<td><span data-ttu-id="04890-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-146">Electricity</span></span></td>
<td><span data-ttu-id="04890-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="04890-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="04890-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="04890-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="04890-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="04890-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-151">Define the cost behavior rule</span></span>

<span data-ttu-id="04890-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="04890-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="04890-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="04890-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="04890-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="04890-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="04890-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="04890-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="04890-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="04890-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="04890-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="04890-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="04890-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-160">Journal</span></span></th>
<th><span data-ttu-id="04890-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04890-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04890-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="04890-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-164">00001</span><span class="sxs-lookup"><span data-stu-id="04890-164">00001</span></span></td>
<td><span data-ttu-id="04890-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="04890-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-166">Fiscal</span></span></td>
<td><span data-ttu-id="04890-167">2017</span><span class="sxs-lookup"><span data-stu-id="04890-167">2017</span></span></td>
<td><span data-ttu-id="04890-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-168">Period 1</span></span></td>
<td><span data-ttu-id="04890-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="04890-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="04890-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04890-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-173">Cost element</span></span></th>
<th><span data-ttu-id="04890-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-174">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="04890-177">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-177">CC099</span></span></td>
<td><span data-ttu-id="04890-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-178">Default cost center</span></span></td>
<td><span data-ttu-id="04890-179">10001</span><span class="sxs-lookup"><span data-stu-id="04890-179">10001</span></span></td>
<td><span data-ttu-id="04890-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-180">Electricity</span></span></td>
<td><span data-ttu-id="04890-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="04890-181">Unclassified</span></span></td>
<td><span data-ttu-id="04890-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04890-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-185">Cost element</span></span></th>
<th><span data-ttu-id="04890-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-186">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-187">Amount</span></span></th>
<th><span data-ttu-id="04890-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-189">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-189">CC099</span></span></td>
<td><span data-ttu-id="04890-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-190">Default cost center</span></span></td>
<td><span data-ttu-id="04890-191">10001</span><span class="sxs-lookup"><span data-stu-id="04890-191">10001</span></span></td>
<td><span data-ttu-id="04890-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-192">Electricity</span></span></td>
<td><span data-ttu-id="04890-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="04890-193">Unclassified</span></span></td>
<td><span data-ttu-id="04890-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-194">10,000.00</span></span></td>
<td><span data-ttu-id="04890-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-196">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-196">CC099</span></span></td>
<td><span data-ttu-id="04890-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-197">Default cost center</span></span></td>
<td><span data-ttu-id="04890-198">10001</span><span class="sxs-lookup"><span data-stu-id="04890-198">10001</span></span></td>
<td><span data-ttu-id="04890-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-199">Electricity</span></span></td>
<td><span data-ttu-id="04890-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="04890-200">Unclassified</span></span></td>
<td><span data-ttu-id="04890-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-201">-10,000.00</span></span></td>
<td><span data-ttu-id="04890-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-203">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-203">CC099</span></span></td>
<td><span data-ttu-id="04890-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-204">Default cost center</span></span></td>
<td><span data-ttu-id="04890-205">10001</span><span class="sxs-lookup"><span data-stu-id="04890-205">10001</span></span></td>
<td><span data-ttu-id="04890-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-206">Electricity</span></span></td>
<td><span data-ttu-id="04890-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-207">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-208">1,000.00</span></span></td>
<td><span data-ttu-id="04890-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-210">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-210">CC099</span></span></td>
<td><span data-ttu-id="04890-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-211">Default cost center</span></span></td>
<td><span data-ttu-id="04890-212">10001</span><span class="sxs-lookup"><span data-stu-id="04890-212">10001</span></span></td>
<td><span data-ttu-id="04890-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-213">Electricity</span></span></td>
<td><span data-ttu-id="04890-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-214">Variable cost</span></span></td>
<td><span data-ttu-id="04890-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-215">9,000.00</span></span></td>
<td><span data-ttu-id="04890-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="04890-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="04890-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="04890-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="04890-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="04890-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="04890-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="04890-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-221">Define the cost distribution rule</span></span>

<span data-ttu-id="04890-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="04890-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="04890-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="04890-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="04890-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="04890-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="04890-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="04890-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="04890-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="04890-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-228">Cost object</span></span></th>
<th><span data-ttu-id="04890-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="04890-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-230">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-230">CC001</span></span></td>
<td><span data-ttu-id="04890-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-231">HR</span></span></td>
<td><span data-ttu-id="04890-232">1,000</span><span class="sxs-lookup"><span data-stu-id="04890-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-233">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-233">CC002</span></span></td>
<td><span data-ttu-id="04890-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-234">Finance</span></span></td>
<td><span data-ttu-id="04890-235">6,000</span><span class="sxs-lookup"><span data-stu-id="04890-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-236">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-236">CC003</span></span></td>
<td><span data-ttu-id="04890-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-237">Assembly</span></span></td>
<td><span data-ttu-id="04890-238">0</span><span class="sxs-lookup"><span data-stu-id="04890-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-240">Cost object</span></span></th>
<th><span data-ttu-id="04890-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-241">Magnitude</span></span></th>
<th><span data-ttu-id="04890-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-242">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-244">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-244">CC001</span></span></td>
<td><span data-ttu-id="04890-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-245">HR</span></span></td>
<td><span data-ttu-id="04890-246">1,000</span><span class="sxs-lookup"><span data-stu-id="04890-246">1,000</span></span></td>
<td><span data-ttu-id="04890-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="04890-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="04890-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-249">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-249">CC002</span></span></td>
<td><span data-ttu-id="04890-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-250">Finance</span></span></td>
<td><span data-ttu-id="04890-251">6,000</span><span class="sxs-lookup"><span data-stu-id="04890-251">6,000</span></span></td>
<td><span data-ttu-id="04890-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="04890-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="04890-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-254">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-254">CC003</span></span></td>
<td><span data-ttu-id="04890-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-255">Assembly</span></span></td>
<td><span data-ttu-id="04890-256">0</span><span class="sxs-lookup"><span data-stu-id="04890-256">0</span></span></td>
<td><span data-ttu-id="04890-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="04890-258">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="04890-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-261">Cost object</span></span></th>
<th><span data-ttu-id="04890-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="04890-262">Formula</span></span></th>
<th><span data-ttu-id="04890-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-263">Magnitude</span></span></th>
<th><span data-ttu-id="04890-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-264">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-266">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-266">CC001</span></span></td>
<td><span data-ttu-id="04890-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-267">HR</span></span></td>
<td><span data-ttu-id="04890-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="04890-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="04890-269">1</span><span class="sxs-lookup"><span data-stu-id="04890-269">1</span></span></td>
<td><span data-ttu-id="04890-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="04890-271">500.00</span><span class="sxs-lookup"><span data-stu-id="04890-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-272">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-272">CC002</span></span></td>
<td><span data-ttu-id="04890-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-273">Finance</span></span></td>
<td><span data-ttu-id="04890-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="04890-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="04890-275">1</span><span class="sxs-lookup"><span data-stu-id="04890-275">1</span></span></td>
<td><span data-ttu-id="04890-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="04890-277">500.00</span><span class="sxs-lookup"><span data-stu-id="04890-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-278">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-278">CC003</span></span></td>
<td><span data-ttu-id="04890-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-279">Assembly</span></span></td>
<td><span data-ttu-id="04890-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="04890-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="04890-281">0</span><span class="sxs-lookup"><span data-stu-id="04890-281">0</span></span></td>
<td><span data-ttu-id="04890-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="04890-283">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="04890-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-285">Journal</span></span></th>
<th><span data-ttu-id="04890-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04890-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04890-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="04890-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-289">00002</span><span class="sxs-lookup"><span data-stu-id="04890-289">00002</span></span></td>
<td><span data-ttu-id="04890-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="04890-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-291">Fiscal</span></span></td>
<td><span data-ttu-id="04890-292">2017</span><span class="sxs-lookup"><span data-stu-id="04890-292">2017</span></span></td>
<td><span data-ttu-id="04890-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-293">Period 1</span></span></td>
<td><span data-ttu-id="04890-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="04890-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="04890-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04890-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-298">Cost element</span></span></th>
<th><span data-ttu-id="04890-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-299">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-302">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-302">CC099</span></span></td>
<td><span data-ttu-id="04890-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-303">Default cost center</span></span></td>
<td><span data-ttu-id="04890-304">10001</span><span class="sxs-lookup"><span data-stu-id="04890-304">10001</span></span></td>
<td><span data-ttu-id="04890-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-305">Electricity</span></span></td>
<td><span data-ttu-id="04890-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-306">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-309">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-309">CC099</span></span></td>
<td><span data-ttu-id="04890-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-310">Default cost center</span></span></td>
<td><span data-ttu-id="04890-311">10001</span><span class="sxs-lookup"><span data-stu-id="04890-311">10001</span></span></td>
<td><span data-ttu-id="04890-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-312">Electricity</span></span></td>
<td><span data-ttu-id="04890-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-313">Variable cost</span></span></td>
<td><span data-ttu-id="04890-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04890-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-317">Cost element</span></span></th>
<th><span data-ttu-id="04890-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-318">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-319">Amount</span></span></th>
<th><span data-ttu-id="04890-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-321">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-321">CC099</span></span></td>
<td><span data-ttu-id="04890-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-322">Default cost center</span></span></td>
<td><span data-ttu-id="04890-323">10001</span><span class="sxs-lookup"><span data-stu-id="04890-323">10001</span></span></td>
<td><span data-ttu-id="04890-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-324">Electricity</span></span></td>
<td><span data-ttu-id="04890-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-325">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="04890-326">-1,000.00</span></span></td>
<td><span data-ttu-id="04890-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-328">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-328">CC001</span></span></td>
<td><span data-ttu-id="04890-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-329">HR</span></span></td>
<td><span data-ttu-id="04890-330">10001</span><span class="sxs-lookup"><span data-stu-id="04890-330">10001</span></span></td>
<td><span data-ttu-id="04890-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-331">Electricity</span></span></td>
<td><span data-ttu-id="04890-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-332">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-333">500.00</span><span class="sxs-lookup"><span data-stu-id="04890-333">500.00</span></span></td>
<td><span data-ttu-id="04890-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-335">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-335">CC002</span></span></td>
<td><span data-ttu-id="04890-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-336">Finance</span></span></td>
<td><span data-ttu-id="04890-337">10001</span><span class="sxs-lookup"><span data-stu-id="04890-337">10001</span></span></td>
<td><span data-ttu-id="04890-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-338">Electricity</span></span></td>
<td><span data-ttu-id="04890-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-339">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-340">500.00</span><span class="sxs-lookup"><span data-stu-id="04890-340">500.00</span></span></td>
<td><span data-ttu-id="04890-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-342">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-342">CC099</span></span></td>
<td><span data-ttu-id="04890-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="04890-343">Default cost center</span></span></td>
<td><span data-ttu-id="04890-344">10001</span><span class="sxs-lookup"><span data-stu-id="04890-344">10001</span></span></td>
<td><span data-ttu-id="04890-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-345">Electricity</span></span></td>
<td><span data-ttu-id="04890-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-346">Variable cost</span></span></td>
<td><span data-ttu-id="04890-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="04890-347">-9,000.00</span></span></td>
<td><span data-ttu-id="04890-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-349">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-349">CC001</span></span></td>
<td><span data-ttu-id="04890-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-350">HR</span></span></td>
<td><span data-ttu-id="04890-351">10001</span><span class="sxs-lookup"><span data-stu-id="04890-351">10001</span></span></td>
<td><span data-ttu-id="04890-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-352">Electricity</span></span></td>
<td><span data-ttu-id="04890-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-353">Variable cost</span></span></td>
<td><span data-ttu-id="04890-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="04890-354">1,285.71</span></span></td>
<td><span data-ttu-id="04890-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-356">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-356">CC002</span></span></td>
<td><span data-ttu-id="04890-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-357">Finance</span></span></td>
<td><span data-ttu-id="04890-358">10001</span><span class="sxs-lookup"><span data-stu-id="04890-358">10001</span></span></td>
<td><span data-ttu-id="04890-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-359">Electricity</span></span></td>
<td><span data-ttu-id="04890-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-360">Variable cost</span></span></td>
<td><span data-ttu-id="04890-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="04890-361">7,714.29</span></span></td>
<td><span data-ttu-id="04890-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="04890-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="04890-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="04890-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="04890-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="04890-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="04890-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="04890-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="04890-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="04890-367">Define the overhead rate</span></span>

<span data-ttu-id="04890-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="04890-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="04890-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="04890-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-370">Cost object</span></span></th>
<th><span data-ttu-id="04890-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="04890-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-372">Proj 1</span></span></td>
<td><span data-ttu-id="04890-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-373">Project 1</span></span></td>
<td><span data-ttu-id="04890-374">3</span><span class="sxs-lookup"><span data-stu-id="04890-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-375">Proj 2</span></span></td>
<td><span data-ttu-id="04890-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-376">Project 2</span></span></td>
<td><span data-ttu-id="04890-377">1</span><span class="sxs-lookup"><span data-stu-id="04890-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-379">Cost object</span></span></th>
<th><span data-ttu-id="04890-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-380">Cost element</span></span></th>
<th><span data-ttu-id="04890-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-381">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="04890-382">Units</span></span></th>
<th><span data-ttu-id="04890-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="04890-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-384">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-384">CC001</span></span></td>
<td><span data-ttu-id="04890-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-385">HR</span></span></td>
<td><span data-ttu-id="04890-386">10001</span><span class="sxs-lookup"><span data-stu-id="04890-386">10001</span></span></td>
<td><span data-ttu-id="04890-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-387">Variable cost</span></span></td>
<td><span data-ttu-id="04890-388">1</span><span class="sxs-lookup"><span data-stu-id="04890-388">1</span></span></td>
<td><span data-ttu-id="04890-389">10</span><span class="sxs-lookup"><span data-stu-id="04890-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-391">Cost object</span></span></th>
<th><span data-ttu-id="04890-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-392">Magnitude</span></span></th>
<th><span data-ttu-id="04890-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-393">Cost element</span></span></th>
<th><span data-ttu-id="04890-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-394">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-396">Proj 1</span></span></td>
<td><span data-ttu-id="04890-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-397">Project 1</span></span></td>
<td><span data-ttu-id="04890-398">3</span><span class="sxs-lookup"><span data-stu-id="04890-398">3</span></span></td>
<td><span data-ttu-id="04890-399">10001</span><span class="sxs-lookup"><span data-stu-id="04890-399">10001</span></span></td>
<td><span data-ttu-id="04890-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="04890-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="04890-401">30.00</span><span class="sxs-lookup"><span data-stu-id="04890-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-402">Proj 2</span></span></td>
<td><span data-ttu-id="04890-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-403">Project 2</span></span></td>
<td><span data-ttu-id="04890-404">1</span><span class="sxs-lookup"><span data-stu-id="04890-404">1</span></span></td>
<td><span data-ttu-id="04890-405">10001</span><span class="sxs-lookup"><span data-stu-id="04890-405">10001</span></span></td>
<td><span data-ttu-id="04890-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="04890-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="04890-407">10.00</span><span class="sxs-lookup"><span data-stu-id="04890-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="04890-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-409">Journal</span></span></th>
<th><span data-ttu-id="04890-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04890-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04890-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="04890-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-413">00003</span><span class="sxs-lookup"><span data-stu-id="04890-413">00003</span></span></td>
<td><span data-ttu-id="04890-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="04890-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="04890-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-415">Fiscal</span></span></td>
<td><span data-ttu-id="04890-416">2017</span><span class="sxs-lookup"><span data-stu-id="04890-416">2017</span></span></td>
<td><span data-ttu-id="04890-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-417">Period 1</span></span></td>
<td><span data-ttu-id="04890-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="04890-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="04890-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04890-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-421">Cost object</span></span></th>
<th><span data-ttu-id="04890-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-424">Proj 1</span></span></td>
<td><span data-ttu-id="04890-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="04890-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="04890-426">3.00</span><span class="sxs-lookup"><span data-stu-id="04890-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-428">Proj 2</span></span></td>
<td><span data-ttu-id="04890-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="04890-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="04890-430">1.00</span><span class="sxs-lookup"><span data-stu-id="04890-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04890-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-433">Cost element</span></span></th>
<th><span data-ttu-id="04890-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-434">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-435">Amount</span></span></th>
<th><span data-ttu-id="04890-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="04890-437">CC0001</span></span></td>
<td><span data-ttu-id="04890-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-438">HR</span></span></td>
<td><span data-ttu-id="04890-439">10001</span><span class="sxs-lookup"><span data-stu-id="04890-439">10001</span></span></td>
<td><span data-ttu-id="04890-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-440">Electricity</span></span></td>
<td><span data-ttu-id="04890-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-441">Variable cost</span></span></td>
<td><span data-ttu-id="04890-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="04890-442">-30.00</span></span></td>
<td><span data-ttu-id="04890-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-444">Proj 1</span></span></td>
<td><span data-ttu-id="04890-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="04890-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="04890-446">10001</span><span class="sxs-lookup"><span data-stu-id="04890-446">10001</span></span></td>
<td><span data-ttu-id="04890-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-447">Electricity</span></span></td>
<td><span data-ttu-id="04890-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-448">Variable cost</span></span></td>
<td><span data-ttu-id="04890-449">30.00</span><span class="sxs-lookup"><span data-stu-id="04890-449">30.00</span></span></td>
<td><span data-ttu-id="04890-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-451">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-451">CC001</span></span></td>
<td><span data-ttu-id="04890-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-452">HR</span></span></td>
<td><span data-ttu-id="04890-453">10001</span><span class="sxs-lookup"><span data-stu-id="04890-453">10001</span></span></td>
<td><span data-ttu-id="04890-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-454">Electricity</span></span></td>
<td><span data-ttu-id="04890-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-455">Variable cost</span></span></td>
<td><span data-ttu-id="04890-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="04890-456">-10.00</span></span></td>
<td><span data-ttu-id="04890-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-458">Proj 2</span></span></td>
<td><span data-ttu-id="04890-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="04890-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="04890-460">10001</span><span class="sxs-lookup"><span data-stu-id="04890-460">10001</span></span></td>
<td><span data-ttu-id="04890-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-461">Electricity</span></span></td>
<td><span data-ttu-id="04890-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-462">Variable cost</span></span></td>
<td><span data-ttu-id="04890-463">10.00</span><span class="sxs-lookup"><span data-stu-id="04890-463">10.00</span></span></td>
<td><span data-ttu-id="04890-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="04890-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="04890-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="04890-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="04890-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="04890-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="04890-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="04890-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="04890-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="04890-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="04890-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="04890-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="04890-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="04890-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="04890-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="04890-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="04890-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="04890-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-475">Define the cost allocation</span></span>

<span data-ttu-id="04890-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="04890-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="04890-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="04890-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="04890-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-479">Cost object</span></span></th>
<th><span data-ttu-id="04890-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="04890-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-481">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-481">CC002</span></span></td>
<td><span data-ttu-id="04890-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-482">Finance</span></span></td>
<td><span data-ttu-id="04890-483">35</span><span class="sxs-lookup"><span data-stu-id="04890-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-484">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-484">CC003</span></span></td>
<td><span data-ttu-id="04890-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-485">Assembly</span></span></td>
<td><span data-ttu-id="04890-486">55</span><span class="sxs-lookup"><span data-stu-id="04890-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-487">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-487">CC004</span></span></td>
<td><span data-ttu-id="04890-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-488">Packaging</span></span></td>
<td><span data-ttu-id="04890-489">10</span><span class="sxs-lookup"><span data-stu-id="04890-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="04890-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="04890-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="04890-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-492">Cost object</span></span></th>
<th><span data-ttu-id="04890-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-494">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-494">CC003</span></span></td>
<td><span data-ttu-id="04890-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-495">Assembly</span></span></td>
<td><span data-ttu-id="04890-496">65</span><span class="sxs-lookup"><span data-stu-id="04890-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-497">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-497">CC004</span></span></td>
<td><span data-ttu-id="04890-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-498">Packaging</span></span></td>
<td><span data-ttu-id="04890-499">35</span><span class="sxs-lookup"><span data-stu-id="04890-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="04890-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="04890-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="04890-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-502">Cost object</span></span></th>
<th><span data-ttu-id="04890-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="04890-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-504">Prod 1</span></span></td>
<td><span data-ttu-id="04890-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-505">Product 1</span></span></td>
<td><span data-ttu-id="04890-506">60</span><span class="sxs-lookup"><span data-stu-id="04890-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-507">Prod 2</span></span></td>
<td><span data-ttu-id="04890-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-508">Product 2</span></span></td>
<td><span data-ttu-id="04890-509">20</span><span class="sxs-lookup"><span data-stu-id="04890-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="04890-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="04890-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="04890-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-512">Cost object</span></span></th>
<th><span data-ttu-id="04890-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="04890-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-514">Prod 1</span></span></td>
<td><span data-ttu-id="04890-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-515">Product 1</span></span></td>
<td><span data-ttu-id="04890-516">80</span><span class="sxs-lookup"><span data-stu-id="04890-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-517">Prod 2</span></span></td>
<td><span data-ttu-id="04890-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-518">Product 2</span></span></td>
<td><span data-ttu-id="04890-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="04890-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="04890-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="04890-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="04890-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="04890-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="04890-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="04890-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-523">Cost object</span></span></th>
<th><span data-ttu-id="04890-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-524">Magnitude</span></span></th>
<th><span data-ttu-id="04890-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-525">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-526">Amount</span></span></th>
<th><span data-ttu-id="04890-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-528">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-528">CC002</span></span></td>
<td><span data-ttu-id="04890-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-529">Finance</span></span></td>
<td><span data-ttu-id="04890-530">35</span><span class="sxs-lookup"><span data-stu-id="04890-530">35</span></span></td>
<td><span data-ttu-id="04890-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="04890-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="04890-532">175.00</span><span class="sxs-lookup"><span data-stu-id="04890-532">175.00</span></span></td>
<td><span data-ttu-id="04890-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-534">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-534">CC003</span></span></td>
<td><span data-ttu-id="04890-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-535">Assembly</span></span></td>
<td><span data-ttu-id="04890-536">55</span><span class="sxs-lookup"><span data-stu-id="04890-536">55</span></span></td>
<td><span data-ttu-id="04890-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="04890-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="04890-538">275.00</span><span class="sxs-lookup"><span data-stu-id="04890-538">275.00</span></span></td>
<td><span data-ttu-id="04890-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-540">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-540">CC004</span></span></td>
<td><span data-ttu-id="04890-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-541">Packaging</span></span></td>
<td><span data-ttu-id="04890-542">10</span><span class="sxs-lookup"><span data-stu-id="04890-542">10</span></span></td>
<td><span data-ttu-id="04890-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="04890-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="04890-544">50.00</span><span class="sxs-lookup"><span data-stu-id="04890-544">50.00</span></span></td>
<td><span data-ttu-id="04890-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-546">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-546">CC002</span></span></td>
<td><span data-ttu-id="04890-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-547">Finance</span></span></td>
<td><span data-ttu-id="04890-548">35</span><span class="sxs-lookup"><span data-stu-id="04890-548">35</span></span></td>
<td><span data-ttu-id="04890-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="04890-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="04890-550">436.00</span><span class="sxs-lookup"><span data-stu-id="04890-550">436.00</span></span></td>
<td><span data-ttu-id="04890-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-552">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-552">CC003</span></span></td>
<td><span data-ttu-id="04890-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-553">Assembly</span></span></td>
<td><span data-ttu-id="04890-554">55</span><span class="sxs-lookup"><span data-stu-id="04890-554">55</span></span></td>
<td><span data-ttu-id="04890-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="04890-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="04890-556">685.14</span><span class="sxs-lookup"><span data-stu-id="04890-556">685.14</span></span></td>
<td><span data-ttu-id="04890-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-558">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-558">CC004</span></span></td>
<td><span data-ttu-id="04890-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-559">Packaging</span></span></td>
<td><span data-ttu-id="04890-560">10</span><span class="sxs-lookup"><span data-stu-id="04890-560">10</span></span></td>
<td><span data-ttu-id="04890-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="04890-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="04890-562">124.57</span><span class="sxs-lookup"><span data-stu-id="04890-562">124.57</span></span></td>
<td><span data-ttu-id="04890-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="04890-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-565">Cost object</span></span></th>
<th><span data-ttu-id="04890-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-566">Magnitude</span></span></th>
<th><span data-ttu-id="04890-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-567">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-568">Amount</span></span></th>
<th><span data-ttu-id="04890-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-570">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-570">CC003</span></span></td>
<td><span data-ttu-id="04890-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-571">Assembly</span></span></td>
<td><span data-ttu-id="04890-572">65</span><span class="sxs-lookup"><span data-stu-id="04890-572">65</span></span></td>
<td><span data-ttu-id="04890-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="04890-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="04890-574">438.75</span><span class="sxs-lookup"><span data-stu-id="04890-574">438.75</span></span></td>
<td><span data-ttu-id="04890-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-576">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-576">CC004</span></span></td>
<td><span data-ttu-id="04890-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-577">Packaging</span></span></td>
<td><span data-ttu-id="04890-578">35</span><span class="sxs-lookup"><span data-stu-id="04890-578">35</span></span></td>
<td><span data-ttu-id="04890-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="04890-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="04890-580">236.25</span><span class="sxs-lookup"><span data-stu-id="04890-580">236.25</span></span></td>
<td><span data-ttu-id="04890-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-582">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-582">CC003</span></span></td>
<td><span data-ttu-id="04890-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-583">Assembly</span></span></td>
<td><span data-ttu-id="04890-584">65</span><span class="sxs-lookup"><span data-stu-id="04890-584">65</span></span></td>
<td><span data-ttu-id="04890-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="04890-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="04890-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="04890-586">5,297.69</span></span></td>
<td><span data-ttu-id="04890-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-588">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-588">CC004</span></span></td>
<td><span data-ttu-id="04890-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-589">Packaging</span></span></td>
<td><span data-ttu-id="04890-590">35</span><span class="sxs-lookup"><span data-stu-id="04890-590">35</span></span></td>
<td><span data-ttu-id="04890-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="04890-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="04890-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="04890-592">2,852.60</span></span></td>
<td><span data-ttu-id="04890-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="04890-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-595">Cost object</span></span></th>
<th><span data-ttu-id="04890-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-596">Magnitude</span></span></th>
<th><span data-ttu-id="04890-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-597">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-598">Amount</span></span></th>
<th><span data-ttu-id="04890-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-600">Prod 1</span></span></td>
<td><span data-ttu-id="04890-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-601">Product 1</span></span></td>
<td><span data-ttu-id="04890-602">60</span><span class="sxs-lookup"><span data-stu-id="04890-602">60</span></span></td>
<td><span data-ttu-id="04890-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="04890-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="04890-604">535.31</span><span class="sxs-lookup"><span data-stu-id="04890-604">535.31</span></span></td>
<td><span data-ttu-id="04890-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-606">Prod 2</span></span></td>
<td><span data-ttu-id="04890-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-607">Product 2</span></span></td>
<td><span data-ttu-id="04890-608">20</span><span class="sxs-lookup"><span data-stu-id="04890-608">20</span></span></td>
<td><span data-ttu-id="04890-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="04890-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="04890-610">178.44</span><span class="sxs-lookup"><span data-stu-id="04890-610">178.44</span></span></td>
<td><span data-ttu-id="04890-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-612">Prod 1</span></span></td>
<td><span data-ttu-id="04890-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-613">Product 1</span></span></td>
<td><span data-ttu-id="04890-614">60</span><span class="sxs-lookup"><span data-stu-id="04890-614">60</span></span></td>
<td><span data-ttu-id="04890-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="04890-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="04890-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="04890-616">4,487.12</span></span></td>
<td><span data-ttu-id="04890-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-618">Prod 2</span></span></td>
<td><span data-ttu-id="04890-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-619">Product 2</span></span></td>
<td><span data-ttu-id="04890-620">20</span><span class="sxs-lookup"><span data-stu-id="04890-620">20</span></span></td>
<td><span data-ttu-id="04890-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="04890-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="04890-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="04890-622">1,495.71</span></span></td>
<td><span data-ttu-id="04890-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04890-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="04890-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-625">Cost object</span></span></th>
<th><span data-ttu-id="04890-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="04890-626">Magnitude</span></span></th>
<th><span data-ttu-id="04890-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="04890-627">Allocation factor</span></span></th>
<th><span data-ttu-id="04890-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-628">Amount</span></span></th>
<th><span data-ttu-id="04890-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-630">Prod 1</span></span></td>
<td><span data-ttu-id="04890-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-631">Product 1</span></span></td>
<td><span data-ttu-id="04890-632">80</span><span class="sxs-lookup"><span data-stu-id="04890-632">80</span></span></td>
<td><span data-ttu-id="04890-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="04890-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="04890-634">241.05</span><span class="sxs-lookup"><span data-stu-id="04890-634">241.05</span></span></td>
<td><span data-ttu-id="04890-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-636">Prod 2</span></span></td>
<td><span data-ttu-id="04890-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-637">Product 2</span></span></td>
<td><span data-ttu-id="04890-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="04890-638">15</span></span></td>
<td><span data-ttu-id="04890-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="04890-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="04890-640">45.20</span><span class="sxs-lookup"><span data-stu-id="04890-640">45.20</span></span></td>
<td><span data-ttu-id="04890-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-642">Prod 1</span></span></td>
<td><span data-ttu-id="04890-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-643">Product 1</span></span></td>
<td><span data-ttu-id="04890-644">80</span><span class="sxs-lookup"><span data-stu-id="04890-644">80</span></span></td>
<td><span data-ttu-id="04890-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="04890-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="04890-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="04890-646">2,507.09</span></span></td>
<td><span data-ttu-id="04890-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-648">Prod 2</span></span></td>
<td><span data-ttu-id="04890-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-649">Product 2</span></span></td>
<td><span data-ttu-id="04890-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="04890-650">15</span></span></td>
<td><span data-ttu-id="04890-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="04890-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="04890-652">470.08</span><span class="sxs-lookup"><span data-stu-id="04890-652">470.08</span></span></td>
<td><span data-ttu-id="04890-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="04890-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="04890-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-655">Journal</span></span></th>
<th><span data-ttu-id="04890-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="04890-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="04890-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="04890-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-659">00004</span><span class="sxs-lookup"><span data-stu-id="04890-659">00004</span></span></td>
<td><span data-ttu-id="04890-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="04890-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-661">Fiscal</span></span></td>
<td><span data-ttu-id="04890-662">2017</span><span class="sxs-lookup"><span data-stu-id="04890-662">2017</span></span></td>
<td><span data-ttu-id="04890-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-663">Period 1</span></span></td>
<td><span data-ttu-id="04890-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="04890-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="04890-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="04890-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04890-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="04890-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-668">Cost element</span></span></th>
<th><span data-ttu-id="04890-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-669">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-672">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-672">CC001</span></span></td>
<td><span data-ttu-id="04890-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-673">HR</span></span></td>
<td><span data-ttu-id="04890-674">10001</span><span class="sxs-lookup"><span data-stu-id="04890-674">10001</span></span></td>
<td><span data-ttu-id="04890-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-675">Electricity</span></span></td>
<td><span data-ttu-id="04890-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-676">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-677">500.00</span><span class="sxs-lookup"><span data-stu-id="04890-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-679">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-679">CC001</span></span></td>
<td><span data-ttu-id="04890-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-680">HR</span></span></td>
<td><span data-ttu-id="04890-681">10001</span><span class="sxs-lookup"><span data-stu-id="04890-681">10001</span></span></td>
<td><span data-ttu-id="04890-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-682">Electricity</span></span></td>
<td><span data-ttu-id="04890-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-683">Variable cost</span></span></td>
<td><span data-ttu-id="04890-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="04890-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-686">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-686">CC002</span></span></td>
<td><span data-ttu-id="04890-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-687">Finance</span></span></td>
<td><span data-ttu-id="04890-688">10001</span><span class="sxs-lookup"><span data-stu-id="04890-688">10001</span></span></td>
<td><span data-ttu-id="04890-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-689">Electricity</span></span></td>
<td><span data-ttu-id="04890-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-690">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-691">675.00</span><span class="sxs-lookup"><span data-stu-id="04890-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-693">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-693">CC002</span></span></td>
<td><span data-ttu-id="04890-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-694">Finance</span></span></td>
<td><span data-ttu-id="04890-695">10001</span><span class="sxs-lookup"><span data-stu-id="04890-695">10001</span></span></td>
<td><span data-ttu-id="04890-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-696">Electricity</span></span></td>
<td><span data-ttu-id="04890-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-697">Variable cost</span></span></td>
<td><span data-ttu-id="04890-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="04890-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-700">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-700">CC003</span></span></td>
<td><span data-ttu-id="04890-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-701">Assembly</span></span></td>
<td><span data-ttu-id="04890-702">10001</span><span class="sxs-lookup"><span data-stu-id="04890-702">10001</span></span></td>
<td><span data-ttu-id="04890-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-703">Electricity</span></span></td>
<td><span data-ttu-id="04890-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-704">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-705">713.75</span><span class="sxs-lookup"><span data-stu-id="04890-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-707">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-707">CC003</span></span></td>
<td><span data-ttu-id="04890-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-708">Assembly</span></span></td>
<td><span data-ttu-id="04890-709">10001</span><span class="sxs-lookup"><span data-stu-id="04890-709">10001</span></span></td>
<td><span data-ttu-id="04890-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-710">Electricity</span></span></td>
<td><span data-ttu-id="04890-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-711">Variable cost</span></span></td>
<td><span data-ttu-id="04890-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="04890-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-714">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-714">CC003</span></span></td>
<td><span data-ttu-id="04890-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-715">Packaging</span></span></td>
<td><span data-ttu-id="04890-716">10001</span><span class="sxs-lookup"><span data-stu-id="04890-716">10001</span></span></td>
<td><span data-ttu-id="04890-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-717">Electricity</span></span></td>
<td><span data-ttu-id="04890-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-718">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-719">286.25</span><span class="sxs-lookup"><span data-stu-id="04890-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-721">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-721">CC003</span></span></td>
<td><span data-ttu-id="04890-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-722">Packaging</span></span></td>
<td><span data-ttu-id="04890-723">10001</span><span class="sxs-lookup"><span data-stu-id="04890-723">10001</span></span></td>
<td><span data-ttu-id="04890-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-724">Electricity</span></span></td>
<td><span data-ttu-id="04890-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-725">Variable cost</span></span></td>
<td><span data-ttu-id="04890-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="04890-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-728">Prod 1</span></span></td>
<td><span data-ttu-id="04890-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-729">Product 1</span></span></td>
<td><span data-ttu-id="04890-730">10001</span><span class="sxs-lookup"><span data-stu-id="04890-730">10001</span></span></td>
<td><span data-ttu-id="04890-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-731">Electricity</span></span></td>
<td><span data-ttu-id="04890-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-732">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-733">776.36</span><span class="sxs-lookup"><span data-stu-id="04890-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-735">Prod 1</span></span></td>
<td><span data-ttu-id="04890-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-736">Product 1</span></span></td>
<td><span data-ttu-id="04890-737">10001</span><span class="sxs-lookup"><span data-stu-id="04890-737">10001</span></span></td>
<td><span data-ttu-id="04890-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-738">Electricity</span></span></td>
<td><span data-ttu-id="04890-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-739">Variable cost</span></span></td>
<td><span data-ttu-id="04890-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="04890-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-742">Prod 2</span></span></td>
<td><span data-ttu-id="04890-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-743">Product 1</span></span></td>
<td><span data-ttu-id="04890-744">10001</span><span class="sxs-lookup"><span data-stu-id="04890-744">10001</span></span></td>
<td><span data-ttu-id="04890-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-745">Electricity</span></span></td>
<td><span data-ttu-id="04890-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-746">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-747">223.64</span><span class="sxs-lookup"><span data-stu-id="04890-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="04890-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-749">Prod 2</span></span></td>
<td><span data-ttu-id="04890-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-750">Product 1</span></span></td>
<td><span data-ttu-id="04890-751">10001</span><span class="sxs-lookup"><span data-stu-id="04890-751">10001</span></span></td>
<td><span data-ttu-id="04890-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-752">Electricity</span></span></td>
<td><span data-ttu-id="04890-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-753">Variable cost</span></span></td>
<td><span data-ttu-id="04890-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="04890-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="04890-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="04890-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="04890-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-757">Cost element</span></span></th>
<th><span data-ttu-id="04890-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-758">Cost behavior</span></span></th>
<th><span data-ttu-id="04890-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-759">Amount</span></span></th>
<th><span data-ttu-id="04890-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="04890-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04890-761">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-761">CC001</span></span></td>
<td><span data-ttu-id="04890-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-762">HR</span></span></td>
<td><span data-ttu-id="04890-763">10001</span><span class="sxs-lookup"><span data-stu-id="04890-763">10001</span></span></td>
<td><span data-ttu-id="04890-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-764">Electricity</span></span></td>
<td><span data-ttu-id="04890-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-765">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="04890-766">-500.00</span></span></td>
<td><span data-ttu-id="04890-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-768">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-768">CC002</span></span></td>
<td><span data-ttu-id="04890-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-769">Finance</span></span></td>
<td><span data-ttu-id="04890-770">10001</span><span class="sxs-lookup"><span data-stu-id="04890-770">10001</span></span></td>
<td><span data-ttu-id="04890-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-771">Electricity</span></span></td>
<td><span data-ttu-id="04890-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-772">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-773">175.00</span><span class="sxs-lookup"><span data-stu-id="04890-773">175.00</span></span></td>
<td><span data-ttu-id="04890-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-775">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-775">CC003</span></span></td>
<td><span data-ttu-id="04890-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-776">Assembly</span></span></td>
<td><span data-ttu-id="04890-777">10001</span><span class="sxs-lookup"><span data-stu-id="04890-777">10001</span></span></td>
<td><span data-ttu-id="04890-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-778">Electricity</span></span></td>
<td><span data-ttu-id="04890-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-779">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-780">275.00</span><span class="sxs-lookup"><span data-stu-id="04890-780">275.00</span></span></td>
<td><span data-ttu-id="04890-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-782">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-782">CC004</span></span></td>
<td><span data-ttu-id="04890-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-783">Packaging</span></span></td>
<td><span data-ttu-id="04890-784">10001</span><span class="sxs-lookup"><span data-stu-id="04890-784">10001</span></span></td>
<td><span data-ttu-id="04890-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-785">Electricity</span></span></td>
<td><span data-ttu-id="04890-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-786">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-787">50,00</span><span class="sxs-lookup"><span data-stu-id="04890-787">50,00</span></span></td>
<td><span data-ttu-id="04890-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-789">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-789">CC001</span></span></td>
<td><span data-ttu-id="04890-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="04890-790">HR</span></span></td>
<td><span data-ttu-id="04890-791">10001</span><span class="sxs-lookup"><span data-stu-id="04890-791">10001</span></span></td>
<td><span data-ttu-id="04890-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-792">Electricity</span></span></td>
<td><span data-ttu-id="04890-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-793">Variable cost</span></span></td>
<td><span data-ttu-id="04890-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="04890-794">-1,245.71</span></span></td>
<td><span data-ttu-id="04890-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-796">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-796">CC002</span></span></td>
<td><span data-ttu-id="04890-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-797">Finance</span></span></td>
<td><span data-ttu-id="04890-798">10001</span><span class="sxs-lookup"><span data-stu-id="04890-798">10001</span></span></td>
<td><span data-ttu-id="04890-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-799">Electricity</span></span></td>
<td><span data-ttu-id="04890-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-800">Variable cost</span></span></td>
<td><span data-ttu-id="04890-801">436.00</span><span class="sxs-lookup"><span data-stu-id="04890-801">436.00</span></span></td>
<td><span data-ttu-id="04890-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-803">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-803">CC003</span></span></td>
<td><span data-ttu-id="04890-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-804">Assembly</span></span></td>
<td><span data-ttu-id="04890-805">10001</span><span class="sxs-lookup"><span data-stu-id="04890-805">10001</span></span></td>
<td><span data-ttu-id="04890-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-806">Electricity</span></span></td>
<td><span data-ttu-id="04890-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-807">Variable cost</span></span></td>
<td><span data-ttu-id="04890-808">685.14</span><span class="sxs-lookup"><span data-stu-id="04890-808">685.14</span></span></td>
<td><span data-ttu-id="04890-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-810">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-810">CC004</span></span></td>
<td><span data-ttu-id="04890-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-811">Packaging</span></span></td>
<td><span data-ttu-id="04890-812">10001</span><span class="sxs-lookup"><span data-stu-id="04890-812">10001</span></span></td>
<td><span data-ttu-id="04890-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-813">Electricity</span></span></td>
<td><span data-ttu-id="04890-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-814">Variable cost</span></span></td>
<td><span data-ttu-id="04890-815">124.57</span><span class="sxs-lookup"><span data-stu-id="04890-815">124.57</span></span></td>
<td><span data-ttu-id="04890-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-817">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-817">CC002</span></span></td>
<td><span data-ttu-id="04890-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-818">Finance</span></span></td>
<td><span data-ttu-id="04890-819">10001</span><span class="sxs-lookup"><span data-stu-id="04890-819">10001</span></span></td>
<td><span data-ttu-id="04890-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-820">Electricity</span></span></td>
<td><span data-ttu-id="04890-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-821">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="04890-822">-675.00</span></span></td>
<td><span data-ttu-id="04890-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-824">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-824">CC003</span></span></td>
<td><span data-ttu-id="04890-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-825">Assembly</span></span></td>
<td><span data-ttu-id="04890-826">10001</span><span class="sxs-lookup"><span data-stu-id="04890-826">10001</span></span></td>
<td><span data-ttu-id="04890-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-827">Electricity</span></span></td>
<td><span data-ttu-id="04890-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-828">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-829">438.75</span><span class="sxs-lookup"><span data-stu-id="04890-829">438.75</span></span></td>
<td><span data-ttu-id="04890-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-831">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-831">CC004</span></span></td>
<td><span data-ttu-id="04890-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-832">Packaging</span></span></td>
<td><span data-ttu-id="04890-833">10001</span><span class="sxs-lookup"><span data-stu-id="04890-833">10001</span></span></td>
<td><span data-ttu-id="04890-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-834">Electricity</span></span></td>
<td><span data-ttu-id="04890-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-835">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-836">236.25</span><span class="sxs-lookup"><span data-stu-id="04890-836">236.25</span></span></td>
<td><span data-ttu-id="04890-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-838">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-838">CC002</span></span></td>
<td><span data-ttu-id="04890-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="04890-839">Finance</span></span></td>
<td><span data-ttu-id="04890-840">10001</span><span class="sxs-lookup"><span data-stu-id="04890-840">10001</span></span></td>
<td><span data-ttu-id="04890-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-841">Electricity</span></span></td>
<td><span data-ttu-id="04890-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-842">Variable cost</span></span></td>
<td><span data-ttu-id="04890-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="04890-843">-8,150.29</span></span></td>
<td><span data-ttu-id="04890-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-845">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-845">CC003</span></span></td>
<td><span data-ttu-id="04890-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-846">Assembly</span></span></td>
<td><span data-ttu-id="04890-847">10001</span><span class="sxs-lookup"><span data-stu-id="04890-847">10001</span></span></td>
<td><span data-ttu-id="04890-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-848">Electricity</span></span></td>
<td><span data-ttu-id="04890-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-849">Variable cost</span></span></td>
<td><span data-ttu-id="04890-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="04890-850">5,297.69</span></span></td>
<td><span data-ttu-id="04890-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-852">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-852">CC004</span></span></td>
<td><span data-ttu-id="04890-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="04890-853">Packaging</span></span></td>
<td><span data-ttu-id="04890-854">10001</span><span class="sxs-lookup"><span data-stu-id="04890-854">10001</span></span></td>
<td><span data-ttu-id="04890-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-855">Electricity</span></span></td>
<td><span data-ttu-id="04890-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-856">Variable cost</span></span></td>
<td><span data-ttu-id="04890-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="04890-857">2,852.60</span></span></td>
<td><span data-ttu-id="04890-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-859">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-859">CC003</span></span></td>
<td><span data-ttu-id="04890-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-860">Assembly</span></span></td>
<td><span data-ttu-id="04890-861">10001</span><span class="sxs-lookup"><span data-stu-id="04890-861">10001</span></span></td>
<td><span data-ttu-id="04890-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-862">Electricity</span></span></td>
<td><span data-ttu-id="04890-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-863">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="04890-864">-713.75</span></span></td>
<td><span data-ttu-id="04890-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-866">Prod 1</span></span></td>
<td><span data-ttu-id="04890-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-867">Product 1</span></span></td>
<td><span data-ttu-id="04890-868">10001</span><span class="sxs-lookup"><span data-stu-id="04890-868">10001</span></span></td>
<td><span data-ttu-id="04890-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-869">Electricity</span></span></td>
<td><span data-ttu-id="04890-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-870">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-871">535.31</span><span class="sxs-lookup"><span data-stu-id="04890-871">535.31</span></span></td>
<td><span data-ttu-id="04890-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-873">Prod 2</span></span></td>
<td><span data-ttu-id="04890-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-874">Product 2</span></span></td>
<td><span data-ttu-id="04890-875">10001</span><span class="sxs-lookup"><span data-stu-id="04890-875">10001</span></span></td>
<td><span data-ttu-id="04890-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-876">Electricity</span></span></td>
<td><span data-ttu-id="04890-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-877">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-878">178.44</span><span class="sxs-lookup"><span data-stu-id="04890-878">178.44</span></span></td>
<td><span data-ttu-id="04890-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-880">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-880">CC003</span></span></td>
<td><span data-ttu-id="04890-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-881">Assembly</span></span></td>
<td><span data-ttu-id="04890-882">10001</span><span class="sxs-lookup"><span data-stu-id="04890-882">10001</span></span></td>
<td><span data-ttu-id="04890-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-883">Electricity</span></span></td>
<td><span data-ttu-id="04890-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-884">Variable cost</span></span></td>
<td><span data-ttu-id="04890-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="04890-885">-5,982.83</span></span></td>
<td><span data-ttu-id="04890-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-887">Prod 1</span></span></td>
<td><span data-ttu-id="04890-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-888">Product 1</span></span></td>
<td><span data-ttu-id="04890-889">10001</span><span class="sxs-lookup"><span data-stu-id="04890-889">10001</span></span></td>
<td><span data-ttu-id="04890-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-890">Electricity</span></span></td>
<td><span data-ttu-id="04890-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-891">Variable cost</span></span></td>
<td><span data-ttu-id="04890-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="04890-892">4,487.12</span></span></td>
<td><span data-ttu-id="04890-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-894">Prod 2</span></span></td>
<td><span data-ttu-id="04890-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-895">Product 2</span></span></td>
<td><span data-ttu-id="04890-896">10001</span><span class="sxs-lookup"><span data-stu-id="04890-896">10001</span></span></td>
<td><span data-ttu-id="04890-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-897">Electricity</span></span></td>
<td><span data-ttu-id="04890-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-898">Variable cost</span></span></td>
<td><span data-ttu-id="04890-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="04890-899">1,495.71</span></span></td>
<td><span data-ttu-id="04890-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-901">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-901">CC003</span></span></td>
<td><span data-ttu-id="04890-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-902">Assembly</span></span></td>
<td><span data-ttu-id="04890-903">10001</span><span class="sxs-lookup"><span data-stu-id="04890-903">10001</span></span></td>
<td><span data-ttu-id="04890-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-904">Electricity</span></span></td>
<td><span data-ttu-id="04890-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-905">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="04890-906">-286.25</span></span></td>
<td><span data-ttu-id="04890-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-908">Prod 1</span></span></td>
<td><span data-ttu-id="04890-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-909">Product 1</span></span></td>
<td><span data-ttu-id="04890-910">10001</span><span class="sxs-lookup"><span data-stu-id="04890-910">10001</span></span></td>
<td><span data-ttu-id="04890-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-911">Electricity</span></span></td>
<td><span data-ttu-id="04890-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-912">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-913">241.05</span><span class="sxs-lookup"><span data-stu-id="04890-913">241.05</span></span></td>
<td><span data-ttu-id="04890-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-915">Prod 2</span></span></td>
<td><span data-ttu-id="04890-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-916">Product 2</span></span></td>
<td><span data-ttu-id="04890-917">10001</span><span class="sxs-lookup"><span data-stu-id="04890-917">10001</span></span></td>
<td><span data-ttu-id="04890-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-918">Electricity</span></span></td>
<td><span data-ttu-id="04890-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-919">Fixed cost</span></span></td>
<td><span data-ttu-id="04890-920">45.20</span><span class="sxs-lookup"><span data-stu-id="04890-920">45.20</span></span></td>
<td><span data-ttu-id="04890-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-922">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-922">CC003</span></span></td>
<td><span data-ttu-id="04890-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="04890-923">Assembly</span></span></td>
<td><span data-ttu-id="04890-924">10001</span><span class="sxs-lookup"><span data-stu-id="04890-924">10001</span></span></td>
<td><span data-ttu-id="04890-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-925">Electricity</span></span></td>
<td><span data-ttu-id="04890-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-926">Variable cost</span></span></td>
<td><span data-ttu-id="04890-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="04890-927">-2,977.17</span></span></td>
<td><span data-ttu-id="04890-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-929">Prod 1</span></span></td>
<td><span data-ttu-id="04890-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-930">Product 1</span></span></td>
<td><span data-ttu-id="04890-931">10001</span><span class="sxs-lookup"><span data-stu-id="04890-931">10001</span></span></td>
<td><span data-ttu-id="04890-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-932">Electricity</span></span></td>
<td><span data-ttu-id="04890-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-933">Variable cost</span></span></td>
<td><span data-ttu-id="04890-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="04890-934">2,507.09</span></span></td>
<td><span data-ttu-id="04890-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04890-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-936">Prod 2</span></span></td>
<td><span data-ttu-id="04890-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-937">Product 2</span></span></td>
<td><span data-ttu-id="04890-938">10001</span><span class="sxs-lookup"><span data-stu-id="04890-938">10001</span></span></td>
<td><span data-ttu-id="04890-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-939">Electricity</span></span></td>
<td><span data-ttu-id="04890-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-940">Variable cost</span></span></td>
<td><span data-ttu-id="04890-941">470.08</span><span class="sxs-lookup"><span data-stu-id="04890-941">470.08</span></span></td>
<td><span data-ttu-id="04890-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="04890-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="04890-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="04890-943">Conclusion</span></span>
<span data-ttu-id="04890-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="04890-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="04890-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="04890-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="04890-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="04890-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="04890-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="04890-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="04890-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="04890-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="04890-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="04890-951">CC099</span><span class="sxs-lookup"><span data-stu-id="04890-951">CC099</span></span></th>
<th><span data-ttu-id="04890-952">CC001</span><span class="sxs-lookup"><span data-stu-id="04890-952">CC001</span></span></th>
<th><span data-ttu-id="04890-953">CC002</span><span class="sxs-lookup"><span data-stu-id="04890-953">CC002</span></span></th>
<th><span data-ttu-id="04890-954">CC003</span><span class="sxs-lookup"><span data-stu-id="04890-954">CC003</span></span></th>
<th><span data-ttu-id="04890-955">CC004</span><span class="sxs-lookup"><span data-stu-id="04890-955">CC004</span></span></th>
<th><span data-ttu-id="04890-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="04890-956">Proj 1</span></span></th>
<th><span data-ttu-id="04890-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="04890-957">Proj 2</span></span></th>
<th><span data-ttu-id="04890-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="04890-958">Prod 1</span></span></th>
<th><span data-ttu-id="04890-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="04890-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="04890-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="04890-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="04890-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="04890-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="04890-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="04890-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="04890-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-971">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="04890-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="04890-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-973">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-974">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-975">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-976">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-977">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="04890-978">776.36</span><span class="sxs-lookup"><span data-stu-id="04890-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-979">223.64</span><span class="sxs-lookup"><span data-stu-id="04890-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="04890-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="04890-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-982">000</span><span class="sxs-lookup"><span data-stu-id="04890-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-983">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-984">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-985">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-986">0.00</span><span class="sxs-lookup"><span data-stu-id="04890-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-987">30.00</span><span class="sxs-lookup"><span data-stu-id="04890-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-988">10.00</span><span class="sxs-lookup"><span data-stu-id="04890-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="04890-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="04890-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="04890-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="04890-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="04890-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="04890-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="04890-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="04890-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="04890-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="04890-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="04890-996">สำหรับข้อมูลเพิ่มเติม ดู [นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="04890-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



