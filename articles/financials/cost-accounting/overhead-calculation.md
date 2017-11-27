---
title: "การคำนวณค่าโสหุ้ย"
description: "หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 549e9b4b073a4e93dd3a1dd52dd6f43e7420a31b
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="8ad56-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="8ad56-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8ad56-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="8ad56-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8ad56-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="8ad56-105">Term definition</span></span>
---------------

<span data-ttu-id="8ad56-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="8ad56-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8ad56-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="8ad56-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8ad56-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="8ad56-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8ad56-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="8ad56-109">Rent</span></span>
-   <span data-ttu-id="8ad56-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-110">Electricity</span></span>
-   <span data-ttu-id="8ad56-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="8ad56-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8ad56-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="8ad56-112">Overhead calculation overview</span></span>
<span data-ttu-id="8ad56-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8ad56-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8ad56-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8ad56-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8ad56-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="8ad56-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8ad56-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8ad56-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8ad56-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8ad56-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ad56-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8ad56-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-119">Version type</span></span>
-   <span data-ttu-id="8ad56-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="8ad56-120">Date and time</span></span>
-   <span data-ttu-id="8ad56-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8ad56-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-122">Fiscal year</span></span>
-   <span data-ttu-id="8ad56-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-123">Fiscal period</span></span>

<span data-ttu-id="8ad56-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="8ad56-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8ad56-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="8ad56-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8ad56-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8ad56-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8ad56-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8ad56-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8ad56-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8ad56-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8ad56-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="8ad56-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8ad56-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8ad56-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8ad56-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8ad56-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8ad56-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8ad56-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8ad56-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="8ad56-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8ad56-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="8ad56-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8ad56-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8ad56-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="8ad56-140">Main account</span></span></th>
<th><span data-ttu-id="8ad56-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8ad56-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-143">CC099</span></span></td>
<td><span data-ttu-id="8ad56-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-144">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-145">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-145">10001</span></span></td>
<td><span data-ttu-id="8ad56-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-146">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8ad56-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8ad56-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8ad56-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="8ad56-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8ad56-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8ad56-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="8ad56-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8ad56-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="8ad56-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8ad56-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="8ad56-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8ad56-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="8ad56-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8ad56-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8ad56-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8ad56-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8ad56-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-160">Journal</span></span></th>
<th><span data-ttu-id="8ad56-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8ad56-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8ad56-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-164">00001</span><span class="sxs-lookup"><span data-stu-id="8ad56-164">00001</span></span></td>
<td><span data-ttu-id="8ad56-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8ad56-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-166">Fiscal</span></span></td>
<td><span data-ttu-id="8ad56-167">2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-167">2017</span></span></td>
<td><span data-ttu-id="8ad56-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-168">Period 1</span></span></td>
<td><span data-ttu-id="8ad56-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8ad56-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="8ad56-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-173">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8ad56-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-177">CC099</span></span></td>
<td><span data-ttu-id="8ad56-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-178">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-179">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-179">10001</span></span></td>
<td><span data-ttu-id="8ad56-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-180">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="8ad56-181">Unclassified</span></span></td>
<td><span data-ttu-id="8ad56-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8ad56-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-185">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-187">Amount</span></span></th>
<th><span data-ttu-id="8ad56-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-189">CC099</span></span></td>
<td><span data-ttu-id="8ad56-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-190">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-191">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-191">10001</span></span></td>
<td><span data-ttu-id="8ad56-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-192">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="8ad56-193">Unclassified</span></span></td>
<td><span data-ttu-id="8ad56-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-194">10,000.00</span></span></td>
<td><span data-ttu-id="8ad56-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-196">CC099</span></span></td>
<td><span data-ttu-id="8ad56-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-197">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-198">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-198">10001</span></span></td>
<td><span data-ttu-id="8ad56-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-199">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="8ad56-200">Unclassified</span></span></td>
<td><span data-ttu-id="8ad56-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8ad56-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-203">CC099</span></span></td>
<td><span data-ttu-id="8ad56-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-204">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-205">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-205">10001</span></span></td>
<td><span data-ttu-id="8ad56-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-206">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-208">1,000.00</span></span></td>
<td><span data-ttu-id="8ad56-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-210">CC099</span></span></td>
<td><span data-ttu-id="8ad56-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-211">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-212">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-212">10001</span></span></td>
<td><span data-ttu-id="8ad56-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-213">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-214">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-215">9,000.00</span></span></td>
<td><span data-ttu-id="8ad56-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-217">สำหรับข้อมูลรายละเอียดเกี่ยวกับพฤติกรรมต้นทุน ดูนโยบายพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="8ad56-218">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="8ad56-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8ad56-219">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8ad56-220">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8ad56-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8ad56-221">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="8ad56-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8ad56-222">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-222">Define the cost distribution rule</span></span>

<span data-ttu-id="8ad56-223">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8ad56-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8ad56-224">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="8ad56-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8ad56-225">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="8ad56-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8ad56-226">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="8ad56-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8ad56-227">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8ad56-228">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-229">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-229">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="8ad56-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-231">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-231">CC001</span></span></td>
<td><span data-ttu-id="8ad56-232">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-232">HR</span></span></td>
<td><span data-ttu-id="8ad56-233">1,000</span><span class="sxs-lookup"><span data-stu-id="8ad56-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-234">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-234">CC002</span></span></td>
<td><span data-ttu-id="8ad56-235">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-235">Finance</span></span></td>
<td><span data-ttu-id="8ad56-236">6,000</span><span class="sxs-lookup"><span data-stu-id="8ad56-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-237">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-237">CC003</span></span></td>
<td><span data-ttu-id="8ad56-238">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-238">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-239">0</span><span class="sxs-lookup"><span data-stu-id="8ad56-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-240">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-241">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-241">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-242">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-242">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-243">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-243">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-244">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-245">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-245">CC001</span></span></td>
<td><span data-ttu-id="8ad56-246">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-246">HR</span></span></td>
<td><span data-ttu-id="8ad56-247">1,000</span><span class="sxs-lookup"><span data-stu-id="8ad56-247">1,000</span></span></td>
<td><span data-ttu-id="8ad56-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8ad56-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-250">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-250">CC002</span></span></td>
<td><span data-ttu-id="8ad56-251">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-251">Finance</span></span></td>
<td><span data-ttu-id="8ad56-252">6,000</span><span class="sxs-lookup"><span data-stu-id="8ad56-252">6,000</span></span></td>
<td><span data-ttu-id="8ad56-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8ad56-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8ad56-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-255">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-255">CC003</span></span></td>
<td><span data-ttu-id="8ad56-256">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-256">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-257">0</span><span class="sxs-lookup"><span data-stu-id="8ad56-257">0</span></span></td>
<td><span data-ttu-id="8ad56-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8ad56-259">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-260">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8ad56-261">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-262">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-262">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-263">สูตร</span><span class="sxs-lookup"><span data-stu-id="8ad56-263">Formula</span></span></th>
<th><span data-ttu-id="8ad56-264">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-264">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-265">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-265">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-266">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-267">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-267">CC001</span></span></td>
<td><span data-ttu-id="8ad56-268">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-268">HR</span></span></td>
<td><span data-ttu-id="8ad56-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8ad56-270">1</span><span class="sxs-lookup"><span data-stu-id="8ad56-270">1</span></span></td>
<td><span data-ttu-id="8ad56-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8ad56-272">500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-273">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-273">CC002</span></span></td>
<td><span data-ttu-id="8ad56-274">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-274">Finance</span></span></td>
<td><span data-ttu-id="8ad56-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8ad56-276">1</span><span class="sxs-lookup"><span data-stu-id="8ad56-276">1</span></span></td>
<td><span data-ttu-id="8ad56-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8ad56-278">500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-279">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-279">CC003</span></span></td>
<td><span data-ttu-id="8ad56-280">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-280">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8ad56-282">0</span><span class="sxs-lookup"><span data-stu-id="8ad56-282">0</span></span></td>
<td><span data-ttu-id="8ad56-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8ad56-284">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8ad56-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-286">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-286">Journal</span></span></th>
<th><span data-ttu-id="8ad56-287">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8ad56-288">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8ad56-289">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-290">00002</span><span class="sxs-lookup"><span data-stu-id="8ad56-290">00002</span></span></td>
<td><span data-ttu-id="8ad56-291">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8ad56-292">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-292">Fiscal</span></span></td>
<td><span data-ttu-id="8ad56-293">2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-293">2017</span></span></td>
<td><span data-ttu-id="8ad56-294">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-294">Period 1</span></span></td>
<td><span data-ttu-id="8ad56-295">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8ad56-296">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="8ad56-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-297">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-298">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-299">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-299">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-300">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-300">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-301">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-302">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-303">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-303">CC099</span></span></td>
<td><span data-ttu-id="8ad56-304">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-304">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-305">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-305">10001</span></span></td>
<td><span data-ttu-id="8ad56-306">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-306">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-307">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-307">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-308">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-309">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-310">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-310">CC099</span></span></td>
<td><span data-ttu-id="8ad56-311">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-311">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-312">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-312">10001</span></span></td>
<td><span data-ttu-id="8ad56-313">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-313">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-314">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-314">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8ad56-316">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-317">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-318">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-318">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-319">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-319">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-320">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-320">Amount</span></span></th>
<th><span data-ttu-id="8ad56-321">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-322">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-322">CC099</span></span></td>
<td><span data-ttu-id="8ad56-323">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-323">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-324">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-324">10001</span></span></td>
<td><span data-ttu-id="8ad56-325">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-325">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-326">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-326">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-327">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="8ad56-327">-1,000.00</span></span></td>
<td><span data-ttu-id="8ad56-328">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-329">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-329">CC001</span></span></td>
<td><span data-ttu-id="8ad56-330">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-330">HR</span></span></td>
<td><span data-ttu-id="8ad56-331">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-331">10001</span></span></td>
<td><span data-ttu-id="8ad56-332">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-332">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-333">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-333">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-334">500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-334">500.00</span></span></td>
<td><span data-ttu-id="8ad56-335">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-336">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-336">CC002</span></span></td>
<td><span data-ttu-id="8ad56-337">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-337">Finance</span></span></td>
<td><span data-ttu-id="8ad56-338">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-338">10001</span></span></td>
<td><span data-ttu-id="8ad56-339">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-339">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-340">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-340">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-341">500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-341">500.00</span></span></td>
<td><span data-ttu-id="8ad56-342">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-343">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-343">CC099</span></span></td>
<td><span data-ttu-id="8ad56-344">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad56-344">Default cost center</span></span></td>
<td><span data-ttu-id="8ad56-345">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-345">10001</span></span></td>
<td><span data-ttu-id="8ad56-346">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-346">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-347">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-347">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-348">-9,000.00</span></span></td>
<td><span data-ttu-id="8ad56-349">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-350">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-350">CC001</span></span></td>
<td><span data-ttu-id="8ad56-351">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-351">HR</span></span></td>
<td><span data-ttu-id="8ad56-352">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-352">10001</span></span></td>
<td><span data-ttu-id="8ad56-353">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-353">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-354">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-354">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-355">1,285.71</span></span></td>
<td><span data-ttu-id="8ad56-356">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-357">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-357">CC002</span></span></td>
<td><span data-ttu-id="8ad56-358">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-358">Finance</span></span></td>
<td><span data-ttu-id="8ad56-359">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-359">10001</span></span></td>
<td><span data-ttu-id="8ad56-360">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-360">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-361">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-361">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8ad56-362">7,714.29</span></span></td>
<td><span data-ttu-id="8ad56-363">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-364">สำหรับรายละเอียดเกี่ยวกับการกระจายต้นทุนและฐานการปันส่วน ให้ดูนโยบายการกระจายต้นทุนและฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="8ad56-365">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="8ad56-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8ad56-366">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="8ad56-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8ad56-367">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="8ad56-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8ad56-368">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="8ad56-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8ad56-369">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="8ad56-369">Define the overhead rate</span></span>

<span data-ttu-id="8ad56-370">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="8ad56-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8ad56-371">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ad56-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-372">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-372">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-373">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="8ad56-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-374">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-374">Proj 1</span></span></td>
<td><span data-ttu-id="8ad56-375">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-375">Project 1</span></span></td>
<td><span data-ttu-id="8ad56-376">3</span><span class="sxs-lookup"><span data-stu-id="8ad56-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-377">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-377">Proj 2</span></span></td>
<td><span data-ttu-id="8ad56-378">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-378">Project 2</span></span></td>
<td><span data-ttu-id="8ad56-379">1</span><span class="sxs-lookup"><span data-stu-id="8ad56-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-380">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-381">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-381">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-382">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-382">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-383">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-383">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-384">หน่วย</span><span class="sxs-lookup"><span data-stu-id="8ad56-384">Units</span></span></th>
<th><span data-ttu-id="8ad56-385">อัตรา</span><span class="sxs-lookup"><span data-stu-id="8ad56-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-386">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-386">CC001</span></span></td>
<td><span data-ttu-id="8ad56-387">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-387">HR</span></span></td>
<td><span data-ttu-id="8ad56-388">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-388">10001</span></span></td>
<td><span data-ttu-id="8ad56-389">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-389">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-390">1</span><span class="sxs-lookup"><span data-stu-id="8ad56-390">1</span></span></td>
<td><span data-ttu-id="8ad56-391">10</span><span class="sxs-lookup"><span data-stu-id="8ad56-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-392">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-393">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-393">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-394">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-394">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-395">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-395">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-396">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-396">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-397">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-398">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-398">Proj 1</span></span></td>
<td><span data-ttu-id="8ad56-399">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-399">Project 1</span></span></td>
<td><span data-ttu-id="8ad56-400">3</span><span class="sxs-lookup"><span data-stu-id="8ad56-400">3</span></span></td>
<td><span data-ttu-id="8ad56-401">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-401">10001</span></span></td>
<td><span data-ttu-id="8ad56-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8ad56-403">30.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-404">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-404">Proj 2</span></span></td>
<td><span data-ttu-id="8ad56-405">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-405">Project 2</span></span></td>
<td><span data-ttu-id="8ad56-406">1</span><span class="sxs-lookup"><span data-stu-id="8ad56-406">1</span></span></td>
<td><span data-ttu-id="8ad56-407">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-407">10001</span></span></td>
<td><span data-ttu-id="8ad56-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8ad56-409">10.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8ad56-410">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-411">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-411">Journal</span></span></th>
<th><span data-ttu-id="8ad56-412">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8ad56-413">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8ad56-414">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-415">00003</span><span class="sxs-lookup"><span data-stu-id="8ad56-415">00003</span></span></td>
<td><span data-ttu-id="8ad56-416">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="8ad56-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8ad56-417">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-417">Fiscal</span></span></td>
<td><span data-ttu-id="8ad56-418">2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-418">2017</span></span></td>
<td><span data-ttu-id="8ad56-419">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-419">Period 1</span></span></td>
<td><span data-ttu-id="8ad56-420">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8ad56-421">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="8ad56-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-422">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-423">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-423">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-424">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-425">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-426">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-426">Proj 1</span></span></td>
<td><span data-ttu-id="8ad56-427">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8ad56-428">3.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-429">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-430">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-430">Proj 2</span></span></td>
<td><span data-ttu-id="8ad56-431">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8ad56-432">1.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8ad56-433">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-434">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-435">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-435">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-436">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-436">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-437">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-437">Amount</span></span></th>
<th><span data-ttu-id="8ad56-438">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="8ad56-439">CC0001</span></span></td>
<td><span data-ttu-id="8ad56-440">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-440">HR</span></span></td>
<td><span data-ttu-id="8ad56-441">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-441">10001</span></span></td>
<td><span data-ttu-id="8ad56-442">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-442">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-443">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-443">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-444">-30.00</span></span></td>
<td><span data-ttu-id="8ad56-445">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-446">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-446">Proj 1</span></span></td>
<td><span data-ttu-id="8ad56-447">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8ad56-448">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-448">10001</span></span></td>
<td><span data-ttu-id="8ad56-449">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-449">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-450">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-450">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-451">30.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-451">30.00</span></span></td>
<td><span data-ttu-id="8ad56-452">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-453">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-453">CC001</span></span></td>
<td><span data-ttu-id="8ad56-454">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-454">HR</span></span></td>
<td><span data-ttu-id="8ad56-455">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-455">10001</span></span></td>
<td><span data-ttu-id="8ad56-456">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-456">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-457">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-457">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-458">-10.00</span></span></td>
<td><span data-ttu-id="8ad56-459">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-460">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-460">Proj 2</span></span></td>
<td><span data-ttu-id="8ad56-461">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8ad56-462">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-462">10001</span></span></td>
<td><span data-ttu-id="8ad56-463">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-463">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-464">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-464">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-465">10.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-465">10.00</span></span></td>
<td><span data-ttu-id="8ad56-466">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-467">สำหรับข้อมูลรายละเอียดเกี่ยวกับนโยบายอัตราค่าโสหุ้ย ให้ดูนโยบายอัตราค่าโสหุ้ยและฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="8ad56-468">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="8ad56-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8ad56-469">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8ad56-470">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8ad56-471">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="8ad56-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="8ad56-472">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8ad56-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8ad56-473">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8ad56-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8ad56-474">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="8ad56-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8ad56-475">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8ad56-476">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8ad56-477">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8ad56-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8ad56-478">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-478">Define the cost allocation</span></span>

<span data-ttu-id="8ad56-479">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8ad56-480">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8ad56-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8ad56-481">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ad56-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-482">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-482">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-483">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="8ad56-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-484">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-484">CC002</span></span></td>
<td><span data-ttu-id="8ad56-485">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-485">Finance</span></span></td>
<td><span data-ttu-id="8ad56-486">35</span><span class="sxs-lookup"><span data-stu-id="8ad56-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-487">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-487">CC003</span></span></td>
<td><span data-ttu-id="8ad56-488">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-488">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-489">55</span><span class="sxs-lookup"><span data-stu-id="8ad56-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-490">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-490">CC004</span></span></td>
<td><span data-ttu-id="8ad56-491">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-491">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-492">10</span><span class="sxs-lookup"><span data-stu-id="8ad56-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-493">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8ad56-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8ad56-494">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ad56-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-495">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-495">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-496">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-497">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-497">CC003</span></span></td>
<td><span data-ttu-id="8ad56-498">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-498">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-499">65</span><span class="sxs-lookup"><span data-stu-id="8ad56-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-500">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-500">CC004</span></span></td>
<td><span data-ttu-id="8ad56-501">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-501">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-502">35</span><span class="sxs-lookup"><span data-stu-id="8ad56-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-503">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8ad56-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8ad56-504">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ad56-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-505">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-505">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-506">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="8ad56-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-507">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-507">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-508">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-508">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-509">60</span><span class="sxs-lookup"><span data-stu-id="8ad56-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-510">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-510">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-511">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-511">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-512">20</span><span class="sxs-lookup"><span data-stu-id="8ad56-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-513">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8ad56-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8ad56-514">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ad56-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-515">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-515">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-516">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="8ad56-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-517">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-517">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-518">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-518">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-519">80</span><span class="sxs-lookup"><span data-stu-id="8ad56-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-520">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-520">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-521">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-521">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-522">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="8ad56-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-523">**หมายเหตุ:** ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ใช้กับผลิตภัณฑ์สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8ad56-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8ad56-524">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวให้บริการการประเมินทางสถิติ ให้ดูเท็มเพลตตัวให้บริการการประเมินทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="8ad56-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="8ad56-525">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในอีกไม่ช้านี้) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="8ad56-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-526">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-526">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-527">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-527">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-528">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-528">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-529">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-529">Amount</span></span></th>
<th><span data-ttu-id="8ad56-530">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-531">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-531">CC002</span></span></td>
<td><span data-ttu-id="8ad56-532">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-532">Finance</span></span></td>
<td><span data-ttu-id="8ad56-533">35</span><span class="sxs-lookup"><span data-stu-id="8ad56-533">35</span></span></td>
<td><span data-ttu-id="8ad56-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8ad56-535">175.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-535">175.00</span></span></td>
<td><span data-ttu-id="8ad56-536">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-537">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-537">CC003</span></span></td>
<td><span data-ttu-id="8ad56-538">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-538">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-539">55</span><span class="sxs-lookup"><span data-stu-id="8ad56-539">55</span></span></td>
<td><span data-ttu-id="8ad56-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8ad56-541">275.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-541">275.00</span></span></td>
<td><span data-ttu-id="8ad56-542">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-543">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-543">CC004</span></span></td>
<td><span data-ttu-id="8ad56-544">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-544">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-545">10</span><span class="sxs-lookup"><span data-stu-id="8ad56-545">10</span></span></td>
<td><span data-ttu-id="8ad56-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8ad56-547">50.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-547">50.00</span></span></td>
<td><span data-ttu-id="8ad56-548">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-549">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-549">CC002</span></span></td>
<td><span data-ttu-id="8ad56-550">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-550">Finance</span></span></td>
<td><span data-ttu-id="8ad56-551">35</span><span class="sxs-lookup"><span data-stu-id="8ad56-551">35</span></span></td>
<td><span data-ttu-id="8ad56-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8ad56-553">436.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-553">436.00</span></span></td>
<td><span data-ttu-id="8ad56-554">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-555">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-555">CC003</span></span></td>
<td><span data-ttu-id="8ad56-556">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-556">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-557">55</span><span class="sxs-lookup"><span data-stu-id="8ad56-557">55</span></span></td>
<td><span data-ttu-id="8ad56-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8ad56-559">685.14</span><span class="sxs-lookup"><span data-stu-id="8ad56-559">685.14</span></span></td>
<td><span data-ttu-id="8ad56-560">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-561">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-561">CC004</span></span></td>
<td><span data-ttu-id="8ad56-562">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-562">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-563">10</span><span class="sxs-lookup"><span data-stu-id="8ad56-563">10</span></span></td>
<td><span data-ttu-id="8ad56-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8ad56-565">124.57</span><span class="sxs-lookup"><span data-stu-id="8ad56-565">124.57</span></span></td>
<td><span data-ttu-id="8ad56-566">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-567">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="8ad56-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-568">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-568">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-569">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-569">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-570">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-570">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-571">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-571">Amount</span></span></th>
<th><span data-ttu-id="8ad56-572">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-573">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-573">CC003</span></span></td>
<td><span data-ttu-id="8ad56-574">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-574">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-575">65</span><span class="sxs-lookup"><span data-stu-id="8ad56-575">65</span></span></td>
<td><span data-ttu-id="8ad56-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8ad56-577">438.75</span><span class="sxs-lookup"><span data-stu-id="8ad56-577">438.75</span></span></td>
<td><span data-ttu-id="8ad56-578">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-579">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-579">CC004</span></span></td>
<td><span data-ttu-id="8ad56-580">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-580">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-581">35</span><span class="sxs-lookup"><span data-stu-id="8ad56-581">35</span></span></td>
<td><span data-ttu-id="8ad56-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8ad56-583">236.25</span><span class="sxs-lookup"><span data-stu-id="8ad56-583">236.25</span></span></td>
<td><span data-ttu-id="8ad56-584">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-585">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-585">CC003</span></span></td>
<td><span data-ttu-id="8ad56-586">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-586">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-587">65</span><span class="sxs-lookup"><span data-stu-id="8ad56-587">65</span></span></td>
<td><span data-ttu-id="8ad56-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8ad56-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8ad56-589">5,297.69</span></span></td>
<td><span data-ttu-id="8ad56-590">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-591">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-591">CC004</span></span></td>
<td><span data-ttu-id="8ad56-592">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-592">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-593">35</span><span class="sxs-lookup"><span data-stu-id="8ad56-593">35</span></span></td>
<td><span data-ttu-id="8ad56-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="8ad56-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8ad56-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8ad56-595">2,852.60</span></span></td>
<td><span data-ttu-id="8ad56-596">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-597">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="8ad56-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-598">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-598">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-599">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-599">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-600">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-600">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-601">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-601">Amount</span></span></th>
<th><span data-ttu-id="8ad56-602">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-603">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-603">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-604">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-604">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-605">60</span><span class="sxs-lookup"><span data-stu-id="8ad56-605">60</span></span></td>
<td><span data-ttu-id="8ad56-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="8ad56-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8ad56-607">535.31</span><span class="sxs-lookup"><span data-stu-id="8ad56-607">535.31</span></span></td>
<td><span data-ttu-id="8ad56-608">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-609">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-609">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-610">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-610">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-611">20</span><span class="sxs-lookup"><span data-stu-id="8ad56-611">20</span></span></td>
<td><span data-ttu-id="8ad56-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="8ad56-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8ad56-613">178.44</span><span class="sxs-lookup"><span data-stu-id="8ad56-613">178.44</span></span></td>
<td><span data-ttu-id="8ad56-614">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-615">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-615">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-616">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-616">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-617">60</span><span class="sxs-lookup"><span data-stu-id="8ad56-617">60</span></span></td>
<td><span data-ttu-id="8ad56-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="8ad56-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8ad56-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8ad56-619">4,487.12</span></span></td>
<td><span data-ttu-id="8ad56-620">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-621">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-621">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-622">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-622">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-623">20</span><span class="sxs-lookup"><span data-stu-id="8ad56-623">20</span></span></td>
<td><span data-ttu-id="8ad56-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="8ad56-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8ad56-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-625">1,495.71</span></span></td>
<td><span data-ttu-id="8ad56-626">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8ad56-627">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="8ad56-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-628">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-628">Cost object</span></span></th>
<th><span data-ttu-id="8ad56-629">ขนาด</span><span class="sxs-lookup"><span data-stu-id="8ad56-629">Magnitude</span></span></th>
<th><span data-ttu-id="8ad56-630">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="8ad56-630">Allocation factor</span></span></th>
<th><span data-ttu-id="8ad56-631">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-631">Amount</span></span></th>
<th><span data-ttu-id="8ad56-632">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-633">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-633">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-634">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-634">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-635">80</span><span class="sxs-lookup"><span data-stu-id="8ad56-635">80</span></span></td>
<td><span data-ttu-id="8ad56-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="8ad56-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8ad56-637">241.05</span><span class="sxs-lookup"><span data-stu-id="8ad56-637">241.05</span></span></td>
<td><span data-ttu-id="8ad56-638">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-639">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-639">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-640">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-640">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-641">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="8ad56-641">15</span></span></td>
<td><span data-ttu-id="8ad56-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="8ad56-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8ad56-643">45.20</span><span class="sxs-lookup"><span data-stu-id="8ad56-643">45.20</span></span></td>
<td><span data-ttu-id="8ad56-644">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-645">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-645">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-646">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-646">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-647">80</span><span class="sxs-lookup"><span data-stu-id="8ad56-647">80</span></span></td>
<td><span data-ttu-id="8ad56-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="8ad56-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8ad56-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8ad56-649">2,507.09</span></span></td>
<td><span data-ttu-id="8ad56-650">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-651">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-651">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-652">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-652">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-653">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="8ad56-653">15</span></span></td>
<td><span data-ttu-id="8ad56-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="8ad56-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8ad56-655">470.08</span><span class="sxs-lookup"><span data-stu-id="8ad56-655">470.08</span></span></td>
<td><span data-ttu-id="8ad56-656">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8ad56-657">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="8ad56-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-658">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-658">Journal</span></span></th>
<th><span data-ttu-id="8ad56-659">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8ad56-660">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8ad56-661">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-662">00004</span><span class="sxs-lookup"><span data-stu-id="8ad56-662">00004</span></span></td>
<td><span data-ttu-id="8ad56-663">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8ad56-664">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-664">Fiscal</span></span></td>
<td><span data-ttu-id="8ad56-665">2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-665">2017</span></span></td>
<td><span data-ttu-id="8ad56-666">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-666">Period 1</span></span></td>
<td><span data-ttu-id="8ad56-667">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8ad56-668">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ad56-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ad56-669">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-670">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-671">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-671">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-672">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-672">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-673">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-674">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-675">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-675">CC001</span></span></td>
<td><span data-ttu-id="8ad56-676">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-676">HR</span></span></td>
<td><span data-ttu-id="8ad56-677">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-677">10001</span></span></td>
<td><span data-ttu-id="8ad56-678">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-678">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-679">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-679">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-680">500.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-681">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-682">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-682">CC001</span></span></td>
<td><span data-ttu-id="8ad56-683">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-683">HR</span></span></td>
<td><span data-ttu-id="8ad56-684">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-684">10001</span></span></td>
<td><span data-ttu-id="8ad56-685">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-685">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-686">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-686">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-688">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-689">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-689">CC002</span></span></td>
<td><span data-ttu-id="8ad56-690">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-690">Finance</span></span></td>
<td><span data-ttu-id="8ad56-691">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-691">10001</span></span></td>
<td><span data-ttu-id="8ad56-692">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-692">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-693">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-693">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-694">675.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-695">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-696">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-696">CC002</span></span></td>
<td><span data-ttu-id="8ad56-697">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-697">Finance</span></span></td>
<td><span data-ttu-id="8ad56-698">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-698">10001</span></span></td>
<td><span data-ttu-id="8ad56-699">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-699">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-700">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-700">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8ad56-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-702">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-703">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-703">CC003</span></span></td>
<td><span data-ttu-id="8ad56-704">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-704">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-705">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-705">10001</span></span></td>
<td><span data-ttu-id="8ad56-706">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-706">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-707">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-707">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-708">713.75</span><span class="sxs-lookup"><span data-stu-id="8ad56-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-709">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-710">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-710">CC003</span></span></td>
<td><span data-ttu-id="8ad56-711">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-711">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-712">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-712">10001</span></span></td>
<td><span data-ttu-id="8ad56-713">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-713">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-714">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-714">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8ad56-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-716">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-717">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-717">CC003</span></span></td>
<td><span data-ttu-id="8ad56-718">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-718">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-719">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-719">10001</span></span></td>
<td><span data-ttu-id="8ad56-720">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-720">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-721">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-721">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-722">286.25</span><span class="sxs-lookup"><span data-stu-id="8ad56-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-723">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-724">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-724">CC003</span></span></td>
<td><span data-ttu-id="8ad56-725">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-725">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-726">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-726">10001</span></span></td>
<td><span data-ttu-id="8ad56-727">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-727">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-728">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-728">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8ad56-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-730">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-731">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-731">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-732">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-732">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-733">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-733">10001</span></span></td>
<td><span data-ttu-id="8ad56-734">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-734">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-735">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-735">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-736">776.36</span><span class="sxs-lookup"><span data-stu-id="8ad56-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-737">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-738">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-738">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-739">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-739">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-740">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-740">10001</span></span></td>
<td><span data-ttu-id="8ad56-741">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-741">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-742">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-742">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8ad56-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-744">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-745">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-745">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-746">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-746">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-747">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-747">10001</span></span></td>
<td><span data-ttu-id="8ad56-748">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-748">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-749">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-749">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-750">223.64</span><span class="sxs-lookup"><span data-stu-id="8ad56-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-751">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="8ad56-752">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-752">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-753">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-753">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-754">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-754">10001</span></span></td>
<td><span data-ttu-id="8ad56-755">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-755">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-756">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-756">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8ad56-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8ad56-758">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8ad56-759">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8ad56-760">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-760">Cost element</span></span></th>
<th><span data-ttu-id="8ad56-761">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-761">Cost behavior</span></span></th>
<th><span data-ttu-id="8ad56-762">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-762">Amount</span></span></th>
<th><span data-ttu-id="8ad56-763">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ad56-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ad56-764">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-764">CC001</span></span></td>
<td><span data-ttu-id="8ad56-765">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-765">HR</span></span></td>
<td><span data-ttu-id="8ad56-766">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-766">10001</span></span></td>
<td><span data-ttu-id="8ad56-767">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-767">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-768">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-768">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-769">-500.00.</span><span class="sxs-lookup"><span data-stu-id="8ad56-769">-500.00</span></span></td>
<td><span data-ttu-id="8ad56-770">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-771">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-771">CC002</span></span></td>
<td><span data-ttu-id="8ad56-772">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-772">Finance</span></span></td>
<td><span data-ttu-id="8ad56-773">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-773">10001</span></span></td>
<td><span data-ttu-id="8ad56-774">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-774">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-775">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-775">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-776">175.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-776">175.00</span></span></td>
<td><span data-ttu-id="8ad56-777">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-778">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-778">CC003</span></span></td>
<td><span data-ttu-id="8ad56-779">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-779">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-780">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-780">10001</span></span></td>
<td><span data-ttu-id="8ad56-781">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-781">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-782">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-782">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-783">275.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-783">275.00</span></span></td>
<td><span data-ttu-id="8ad56-784">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-785">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-785">CC004</span></span></td>
<td><span data-ttu-id="8ad56-786">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-786">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-787">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-787">10001</span></span></td>
<td><span data-ttu-id="8ad56-788">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-788">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-789">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-789">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-790">50,00</span><span class="sxs-lookup"><span data-stu-id="8ad56-790">50,00</span></span></td>
<td><span data-ttu-id="8ad56-791">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-792">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-792">CC001</span></span></td>
<td><span data-ttu-id="8ad56-793">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="8ad56-793">HR</span></span></td>
<td><span data-ttu-id="8ad56-794">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-794">10001</span></span></td>
<td><span data-ttu-id="8ad56-795">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-795">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-796">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-796">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-797">-1,245.71</span></span></td>
<td><span data-ttu-id="8ad56-798">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-799">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-799">CC002</span></span></td>
<td><span data-ttu-id="8ad56-800">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-800">Finance</span></span></td>
<td><span data-ttu-id="8ad56-801">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-801">10001</span></span></td>
<td><span data-ttu-id="8ad56-802">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-802">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-803">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-803">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-804">436.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-804">436.00</span></span></td>
<td><span data-ttu-id="8ad56-805">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-806">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-806">CC003</span></span></td>
<td><span data-ttu-id="8ad56-807">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-807">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-808">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-808">10001</span></span></td>
<td><span data-ttu-id="8ad56-809">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-809">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-810">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-810">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-811">685.14</span><span class="sxs-lookup"><span data-stu-id="8ad56-811">685.14</span></span></td>
<td><span data-ttu-id="8ad56-812">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-813">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-813">CC004</span></span></td>
<td><span data-ttu-id="8ad56-814">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-814">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-815">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-815">10001</span></span></td>
<td><span data-ttu-id="8ad56-816">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-816">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-817">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-817">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-818">124.57</span><span class="sxs-lookup"><span data-stu-id="8ad56-818">124.57</span></span></td>
<td><span data-ttu-id="8ad56-819">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-820">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-820">CC002</span></span></td>
<td><span data-ttu-id="8ad56-821">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-821">Finance</span></span></td>
<td><span data-ttu-id="8ad56-822">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-822">10001</span></span></td>
<td><span data-ttu-id="8ad56-823">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-823">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-824">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-824">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-825">-675.00</span></span></td>
<td><span data-ttu-id="8ad56-826">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-827">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-827">CC003</span></span></td>
<td><span data-ttu-id="8ad56-828">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-828">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-829">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-829">10001</span></span></td>
<td><span data-ttu-id="8ad56-830">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-830">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-831">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-831">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-832">438.75</span><span class="sxs-lookup"><span data-stu-id="8ad56-832">438.75</span></span></td>
<td><span data-ttu-id="8ad56-833">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-834">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-834">CC004</span></span></td>
<td><span data-ttu-id="8ad56-835">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-835">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-836">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-836">10001</span></span></td>
<td><span data-ttu-id="8ad56-837">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-837">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-838">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-838">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-839">236.25</span><span class="sxs-lookup"><span data-stu-id="8ad56-839">236.25</span></span></td>
<td><span data-ttu-id="8ad56-840">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-841">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-841">CC002</span></span></td>
<td><span data-ttu-id="8ad56-842">การเงิน</span><span class="sxs-lookup"><span data-stu-id="8ad56-842">Finance</span></span></td>
<td><span data-ttu-id="8ad56-843">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-843">10001</span></span></td>
<td><span data-ttu-id="8ad56-844">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-844">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-845">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-845">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="8ad56-846">-8,150.29</span></span></td>
<td><span data-ttu-id="8ad56-847">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-848">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-848">CC003</span></span></td>
<td><span data-ttu-id="8ad56-849">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-849">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-850">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-850">10001</span></span></td>
<td><span data-ttu-id="8ad56-851">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-851">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-852">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-852">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8ad56-853">5,297.69</span></span></td>
<td><span data-ttu-id="8ad56-854">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-855">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-855">CC004</span></span></td>
<td><span data-ttu-id="8ad56-856">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad56-856">Packaging</span></span></td>
<td><span data-ttu-id="8ad56-857">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-857">10001</span></span></td>
<td><span data-ttu-id="8ad56-858">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-858">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-859">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-859">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8ad56-860">2,852.60</span></span></td>
<td><span data-ttu-id="8ad56-861">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-862">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-862">CC003</span></span></td>
<td><span data-ttu-id="8ad56-863">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-863">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-864">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-864">10001</span></span></td>
<td><span data-ttu-id="8ad56-865">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-865">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-866">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-866">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="8ad56-867">-713.75</span></span></td>
<td><span data-ttu-id="8ad56-868">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-869">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-869">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-870">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-870">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-871">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-871">10001</span></span></td>
<td><span data-ttu-id="8ad56-872">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-872">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-873">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-873">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-874">535.31</span><span class="sxs-lookup"><span data-stu-id="8ad56-874">535.31</span></span></td>
<td><span data-ttu-id="8ad56-875">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-876">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-876">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-877">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-877">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-878">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-878">10001</span></span></td>
<td><span data-ttu-id="8ad56-879">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-879">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-880">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-880">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-881">178.44</span><span class="sxs-lookup"><span data-stu-id="8ad56-881">178.44</span></span></td>
<td><span data-ttu-id="8ad56-882">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-883">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-883">CC003</span></span></td>
<td><span data-ttu-id="8ad56-884">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-884">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-885">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-885">10001</span></span></td>
<td><span data-ttu-id="8ad56-886">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-886">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-887">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-887">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="8ad56-888">-5,982.83</span></span></td>
<td><span data-ttu-id="8ad56-889">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-890">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-890">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-891">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-891">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-892">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-892">10001</span></span></td>
<td><span data-ttu-id="8ad56-893">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-893">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-894">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-894">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8ad56-895">4,487.12</span></span></td>
<td><span data-ttu-id="8ad56-896">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-897">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-897">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-898">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-898">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-899">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-899">10001</span></span></td>
<td><span data-ttu-id="8ad56-900">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-900">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-901">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-901">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8ad56-902">1,495.71</span></span></td>
<td><span data-ttu-id="8ad56-903">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-904">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-904">CC003</span></span></td>
<td><span data-ttu-id="8ad56-905">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-905">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-906">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-906">10001</span></span></td>
<td><span data-ttu-id="8ad56-907">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-907">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-908">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-908">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="8ad56-909">-286.25</span></span></td>
<td><span data-ttu-id="8ad56-910">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-911">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-911">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-912">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-912">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-913">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-913">10001</span></span></td>
<td><span data-ttu-id="8ad56-914">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-914">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-915">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-915">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-916">241.05</span><span class="sxs-lookup"><span data-stu-id="8ad56-916">241.05</span></span></td>
<td><span data-ttu-id="8ad56-917">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-918">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-918">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-919">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-919">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-920">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-920">10001</span></span></td>
<td><span data-ttu-id="8ad56-921">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-921">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-922">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-922">Fixed cost</span></span></td>
<td><span data-ttu-id="8ad56-923">45.20</span><span class="sxs-lookup"><span data-stu-id="8ad56-923">45.20</span></span></td>
<td><span data-ttu-id="8ad56-924">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-925">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-925">CC003</span></span></td>
<td><span data-ttu-id="8ad56-926">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="8ad56-926">Assembly</span></span></td>
<td><span data-ttu-id="8ad56-927">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-927">10001</span></span></td>
<td><span data-ttu-id="8ad56-928">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-928">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-929">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-929">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="8ad56-930">-2,977.17</span></span></td>
<td><span data-ttu-id="8ad56-931">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-932">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-932">Prod 1</span></span></td>
<td><span data-ttu-id="8ad56-933">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-933">Product 1</span></span></td>
<td><span data-ttu-id="8ad56-934">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-934">10001</span></span></td>
<td><span data-ttu-id="8ad56-935">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-935">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-936">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-936">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8ad56-937">2,507.09</span></span></td>
<td><span data-ttu-id="8ad56-938">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ad56-939">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-939">Prod 2</span></span></td>
<td><span data-ttu-id="8ad56-940">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-940">Product 2</span></span></td>
<td><span data-ttu-id="8ad56-941">10001</span><span class="sxs-lookup"><span data-stu-id="8ad56-941">10001</span></span></td>
<td><span data-ttu-id="8ad56-942">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-942">Electricity</span></span></td>
<td><span data-ttu-id="8ad56-943">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-943">Variable cost</span></span></td>
<td><span data-ttu-id="8ad56-944">470.08</span><span class="sxs-lookup"><span data-stu-id="8ad56-944">470.08</span></span></td>
<td><span data-ttu-id="8ad56-945">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="8ad56-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8ad56-946">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="8ad56-946">Conclusion</span></span>
<span data-ttu-id="8ad56-947">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="8ad56-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8ad56-948">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="8ad56-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8ad56-949">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="8ad56-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8ad56-950">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8ad56-951">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8ad56-952">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8ad56-953">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="8ad56-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8ad56-954">CC099</span><span class="sxs-lookup"><span data-stu-id="8ad56-954">CC099</span></span></th>
<th><span data-ttu-id="8ad56-955">CC001</span><span class="sxs-lookup"><span data-stu-id="8ad56-955">CC001</span></span></th>
<th><span data-ttu-id="8ad56-956">CC002</span><span class="sxs-lookup"><span data-stu-id="8ad56-956">CC002</span></span></th>
<th><span data-ttu-id="8ad56-957">CC003</span><span class="sxs-lookup"><span data-stu-id="8ad56-957">CC003</span></span></th>
<th><span data-ttu-id="8ad56-958">CC004</span><span class="sxs-lookup"><span data-stu-id="8ad56-958">CC004</span></span></th>
<th><span data-ttu-id="8ad56-959">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-959">Proj 1</span></span></th>
<th><span data-ttu-id="8ad56-960">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-960">Proj 2</span></span></th>
<th><span data-ttu-id="8ad56-961">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="8ad56-961">Prod 1</span></span></th>
<th><span data-ttu-id="8ad56-962">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="8ad56-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8ad56-963">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="8ad56-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8ad56-973">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="8ad56-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-974">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8ad56-975">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="8ad56-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-976">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-977">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-978">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-979">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-980">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-981">776.36</span><span class="sxs-lookup"><span data-stu-id="8ad56-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-982">223.64</span><span class="sxs-lookup"><span data-stu-id="8ad56-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8ad56-984">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="8ad56-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-985">000</span><span class="sxs-lookup"><span data-stu-id="8ad56-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-986">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-987">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-988">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-989">0.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-990">30.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-991">10.00</span><span class="sxs-lookup"><span data-stu-id="8ad56-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8ad56-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8ad56-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8ad56-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="8ad56-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8ad56-995">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8ad56-996">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8ad56-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8ad56-997">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8ad56-998">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8ad56-999">สำหรับข้อมูลเพิ่มเติม ให้ดูที่นโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="8ad56-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="8ad56-1000">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="8ad56-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




