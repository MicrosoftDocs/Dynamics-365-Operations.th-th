---
title: การคำนวณค่าโสหุ้ย
description: หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822914"
---
# <a name="overhead-calculation"></a><span data-ttu-id="f6fa3-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6fa3-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="f6fa3-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-105">Term definition</span></span>
---------------

<span data-ttu-id="f6fa3-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="f6fa3-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="f6fa3-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="f6fa3-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="f6fa3-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="f6fa3-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-109">Rent</span></span>
-   <span data-ttu-id="f6fa3-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-110">Electricity</span></span>
-   <span data-ttu-id="f6fa3-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="f6fa3-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-112">Overhead calculation overview</span></span>
<span data-ttu-id="f6fa3-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f6fa3-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="f6fa3-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="f6fa3-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="f6fa3-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="f6fa3-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="f6fa3-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f6fa3-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="f6fa3-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-119">Version type</span></span>
-   <span data-ttu-id="f6fa3-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f6fa3-120">Date and time</span></span>
-   <span data-ttu-id="f6fa3-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="f6fa3-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-122">Fiscal year</span></span>
-   <span data-ttu-id="f6fa3-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-123">Fiscal period</span></span>

<span data-ttu-id="f6fa3-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="f6fa3-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="f6fa3-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="f6fa3-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f6fa3-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="f6fa3-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="f6fa3-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="f6fa3-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="f6fa3-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="f6fa3-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="f6fa3-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="f6fa3-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="f6fa3-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="f6fa3-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="f6fa3-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="f6fa3-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="f6fa3-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f6fa3-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="f6fa3-140">Main account</span></span></th>
<th><span data-ttu-id="f6fa3-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-143">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-143">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-144">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-145">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-145">10001</span></span></td>
<td><span data-ttu-id="f6fa3-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-146">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="f6fa3-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="f6fa3-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="f6fa3-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร** ได้</span><span class="sxs-lookup"><span data-stu-id="f6fa3-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="f6fa3-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-151">Define the cost behavior rule</span></span>

<span data-ttu-id="f6fa3-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="f6fa3-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="f6fa3-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="f6fa3-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="f6fa3-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="f6fa3-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="f6fa3-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="f6fa3-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="f6fa3-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="f6fa3-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-160">Journal</span></span></th>
<th><span data-ttu-id="f6fa3-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6fa3-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6fa3-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-164">00001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-164">00001</span></span></td>
<td><span data-ttu-id="f6fa3-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="f6fa3-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-166">Fiscal</span></span></td>
<td><span data-ttu-id="f6fa3-167">2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-167">2017</span></span></td>
<td><span data-ttu-id="f6fa3-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-168">Period 1</span></span></td>
<td><span data-ttu-id="f6fa3-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f6fa3-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-173">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-174">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-177">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-177">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-178">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-179">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-179">10001</span></span></td>
<td><span data-ttu-id="f6fa3-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-180">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="f6fa3-181">Unclassified</span></span></td>
<td><span data-ttu-id="f6fa3-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6fa3-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-185">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-186">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-187">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-189">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-189">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-190">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-191">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-191">10001</span></span></td>
<td><span data-ttu-id="f6fa3-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-192">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="f6fa3-193">Unclassified</span></span></td>
<td><span data-ttu-id="f6fa3-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-194">10,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-196">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-196">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-197">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-198">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-198">10001</span></span></td>
<td><span data-ttu-id="f6fa3-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-199">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="f6fa3-200">Unclassified</span></span></td>
<td><span data-ttu-id="f6fa3-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-201">-10,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-203">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-203">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-204">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-205">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-205">10001</span></span></td>
<td><span data-ttu-id="f6fa3-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-206">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-207">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-208">1,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-210">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-210">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-211">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-212">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-212">10001</span></span></td>
<td><span data-ttu-id="f6fa3-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-213">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-214">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-215">9,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="f6fa3-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="f6fa3-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f6fa3-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="f6fa3-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="f6fa3-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-221">Define the cost distribution rule</span></span>

<span data-ttu-id="f6fa3-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="f6fa3-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="f6fa3-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="f6fa3-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="f6fa3-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="f6fa3-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-228">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="f6fa3-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-230">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-230">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-231">HR</span></span></td>
<td><span data-ttu-id="f6fa3-232">1,000</span><span class="sxs-lookup"><span data-stu-id="f6fa3-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-233">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-233">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-234">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-235">6,000</span><span class="sxs-lookup"><span data-stu-id="f6fa3-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-236">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-236">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-237">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-238">0</span><span class="sxs-lookup"><span data-stu-id="f6fa3-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-240">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-241">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-242">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-244">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-244">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-245">HR</span></span></td>
<td><span data-ttu-id="f6fa3-246">1,000</span><span class="sxs-lookup"><span data-stu-id="f6fa3-246">1,000</span></span></td>
<td><span data-ttu-id="f6fa3-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-249">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-249">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-250">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-251">6,000</span><span class="sxs-lookup"><span data-stu-id="f6fa3-251">6,000</span></span></td>
<td><span data-ttu-id="f6fa3-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f6fa3-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-254">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-254">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-255">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-256">0</span><span class="sxs-lookup"><span data-stu-id="f6fa3-256">0</span></span></td>
<td><span data-ttu-id="f6fa3-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-258">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="f6fa3-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-261">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-262">Formula</span></span></th>
<th><span data-ttu-id="f6fa3-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-263">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-264">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-266">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-266">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-267">HR</span></span></td>
<td><span data-ttu-id="f6fa3-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f6fa3-269">1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-269">1</span></span></td>
<td><span data-ttu-id="f6fa3-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-271">500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-272">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-272">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-273">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f6fa3-275">1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-275">1</span></span></td>
<td><span data-ttu-id="f6fa3-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-277">500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-278">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-278">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-279">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f6fa3-281">0</span><span class="sxs-lookup"><span data-stu-id="f6fa3-281">0</span></span></td>
<td><span data-ttu-id="f6fa3-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-283">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f6fa3-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-285">Journal</span></span></th>
<th><span data-ttu-id="f6fa3-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6fa3-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6fa3-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-289">00002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-289">00002</span></span></td>
<td><span data-ttu-id="f6fa3-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="f6fa3-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-291">Fiscal</span></span></td>
<td><span data-ttu-id="f6fa3-292">2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-292">2017</span></span></td>
<td><span data-ttu-id="f6fa3-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-293">Period 1</span></span></td>
<td><span data-ttu-id="f6fa3-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f6fa3-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-298">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-299">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-302">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-302">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-303">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-304">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-304">10001</span></span></td>
<td><span data-ttu-id="f6fa3-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-305">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-306">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-309">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-309">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-310">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-311">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-311">10001</span></span></td>
<td><span data-ttu-id="f6fa3-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-312">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-313">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6fa3-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-317">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-318">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-319">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-321">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-321">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-322">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-323">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-323">10001</span></span></td>
<td><span data-ttu-id="f6fa3-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-324">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-325">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="f6fa3-326">-1,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-328">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-328">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-329">HR</span></span></td>
<td><span data-ttu-id="f6fa3-330">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-330">10001</span></span></td>
<td><span data-ttu-id="f6fa3-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-331">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-332">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-333">500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-333">500.00</span></span></td>
<td><span data-ttu-id="f6fa3-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-335">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-335">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-336">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-337">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-337">10001</span></span></td>
<td><span data-ttu-id="f6fa3-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-338">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-339">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-340">500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-340">500.00</span></span></td>
<td><span data-ttu-id="f6fa3-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-342">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-342">CC099</span></span></td>
<td><span data-ttu-id="f6fa3-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6fa3-343">Default cost center</span></span></td>
<td><span data-ttu-id="f6fa3-344">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-344">10001</span></span></td>
<td><span data-ttu-id="f6fa3-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-345">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-346">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-347">-9,000.00</span></span></td>
<td><span data-ttu-id="f6fa3-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-349">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-349">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-350">HR</span></span></td>
<td><span data-ttu-id="f6fa3-351">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-351">10001</span></span></td>
<td><span data-ttu-id="f6fa3-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-352">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-353">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-354">1,285.71</span></span></td>
<td><span data-ttu-id="f6fa3-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-356">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-356">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-357">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-358">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-358">10001</span></span></td>
<td><span data-ttu-id="f6fa3-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-359">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-360">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f6fa3-361">7,714.29</span></span></td>
<td><span data-ttu-id="f6fa3-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="f6fa3-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="f6fa3-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="f6fa3-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="f6fa3-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-367">Define the overhead rate</span></span>

<span data-ttu-id="f6fa3-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="f6fa3-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f6fa3-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-370">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="f6fa3-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-372">Proj 1</span></span></td>
<td><span data-ttu-id="f6fa3-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-373">Project 1</span></span></td>
<td><span data-ttu-id="f6fa3-374">3</span><span class="sxs-lookup"><span data-stu-id="f6fa3-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-375">Proj 2</span></span></td>
<td><span data-ttu-id="f6fa3-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-376">Project 2</span></span></td>
<td><span data-ttu-id="f6fa3-377">1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-379">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-380">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-381">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-382">Units</span></span></th>
<th><span data-ttu-id="f6fa3-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="f6fa3-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-384">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-384">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-385">HR</span></span></td>
<td><span data-ttu-id="f6fa3-386">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-386">10001</span></span></td>
<td><span data-ttu-id="f6fa3-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-387">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-388">1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-388">1</span></span></td>
<td><span data-ttu-id="f6fa3-389">10</span><span class="sxs-lookup"><span data-stu-id="f6fa3-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-391">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-392">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-393">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-394">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-396">Proj 1</span></span></td>
<td><span data-ttu-id="f6fa3-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-397">Project 1</span></span></td>
<td><span data-ttu-id="f6fa3-398">3</span><span class="sxs-lookup"><span data-stu-id="f6fa3-398">3</span></span></td>
<td><span data-ttu-id="f6fa3-399">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-399">10001</span></span></td>
<td><span data-ttu-id="f6fa3-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f6fa3-401">30.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-402">Proj 2</span></span></td>
<td><span data-ttu-id="f6fa3-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-403">Project 2</span></span></td>
<td><span data-ttu-id="f6fa3-404">1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-404">1</span></span></td>
<td><span data-ttu-id="f6fa3-405">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-405">10001</span></span></td>
<td><span data-ttu-id="f6fa3-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f6fa3-407">10.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f6fa3-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-409">Journal</span></span></th>
<th><span data-ttu-id="f6fa3-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6fa3-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6fa3-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-413">00003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-413">00003</span></span></td>
<td><span data-ttu-id="f6fa3-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="f6fa3-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="f6fa3-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-415">Fiscal</span></span></td>
<td><span data-ttu-id="f6fa3-416">2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-416">2017</span></span></td>
<td><span data-ttu-id="f6fa3-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-417">Period 1</span></span></td>
<td><span data-ttu-id="f6fa3-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="f6fa3-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-421">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-424">Proj 1</span></span></td>
<td><span data-ttu-id="f6fa3-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f6fa3-426">3.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-428">Proj 2</span></span></td>
<td><span data-ttu-id="f6fa3-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f6fa3-430">1.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6fa3-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-433">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-434">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-435">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-437">CC0001</span></span></td>
<td><span data-ttu-id="f6fa3-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-438">HR</span></span></td>
<td><span data-ttu-id="f6fa3-439">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-439">10001</span></span></td>
<td><span data-ttu-id="f6fa3-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-440">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-441">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-442">-30.00</span></span></td>
<td><span data-ttu-id="f6fa3-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-444">Proj 1</span></span></td>
<td><span data-ttu-id="f6fa3-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f6fa3-446">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-446">10001</span></span></td>
<td><span data-ttu-id="f6fa3-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-447">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-448">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-449">30.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-449">30.00</span></span></td>
<td><span data-ttu-id="f6fa3-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-451">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-451">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-452">HR</span></span></td>
<td><span data-ttu-id="f6fa3-453">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-453">10001</span></span></td>
<td><span data-ttu-id="f6fa3-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-454">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-455">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-456">-10.00</span></span></td>
<td><span data-ttu-id="f6fa3-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-458">Proj 2</span></span></td>
<td><span data-ttu-id="f6fa3-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f6fa3-460">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-460">10001</span></span></td>
<td><span data-ttu-id="f6fa3-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-461">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-462">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-463">10.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-463">10.00</span></span></td>
<td><span data-ttu-id="f6fa3-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="f6fa3-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="f6fa3-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="f6fa3-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="f6fa3-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="f6fa3-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="f6fa3-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="f6fa3-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="f6fa3-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="f6fa3-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="f6fa3-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="f6fa3-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-475">Define the cost allocation</span></span>

<span data-ttu-id="f6fa3-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="f6fa3-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="f6fa3-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f6fa3-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-479">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="f6fa3-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-481">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-481">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-482">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-483">35</span><span class="sxs-lookup"><span data-stu-id="f6fa3-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-484">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-484">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-485">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-486">55</span><span class="sxs-lookup"><span data-stu-id="f6fa3-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-487">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-487">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-488">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-489">10</span><span class="sxs-lookup"><span data-stu-id="f6fa3-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="f6fa3-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f6fa3-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-492">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-494">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-494">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-495">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-496">65</span><span class="sxs-lookup"><span data-stu-id="f6fa3-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-497">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-497">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-498">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-499">35</span><span class="sxs-lookup"><span data-stu-id="f6fa3-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="f6fa3-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f6fa3-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-502">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-504">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-505">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-506">60</span><span class="sxs-lookup"><span data-stu-id="f6fa3-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-507">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-508">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-509">20</span><span class="sxs-lookup"><span data-stu-id="f6fa3-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="f6fa3-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f6fa3-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-512">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-514">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-515">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-516">80</span><span class="sxs-lookup"><span data-stu-id="f6fa3-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-517">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-518">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="f6fa3-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f6fa3-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="f6fa3-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="f6fa3-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-523">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-524">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-525">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-526">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-528">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-528">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-529">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-530">35</span><span class="sxs-lookup"><span data-stu-id="f6fa3-530">35</span></span></td>
<td><span data-ttu-id="f6fa3-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f6fa3-532">175.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-532">175.00</span></span></td>
<td><span data-ttu-id="f6fa3-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-534">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-534">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-535">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-536">55</span><span class="sxs-lookup"><span data-stu-id="f6fa3-536">55</span></span></td>
<td><span data-ttu-id="f6fa3-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f6fa3-538">275.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-538">275.00</span></span></td>
<td><span data-ttu-id="f6fa3-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-540">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-540">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-541">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-542">10</span><span class="sxs-lookup"><span data-stu-id="f6fa3-542">10</span></span></td>
<td><span data-ttu-id="f6fa3-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f6fa3-544">50.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-544">50.00</span></span></td>
<td><span data-ttu-id="f6fa3-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-546">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-546">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-547">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-548">35</span><span class="sxs-lookup"><span data-stu-id="f6fa3-548">35</span></span></td>
<td><span data-ttu-id="f6fa3-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f6fa3-550">436.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-550">436.00</span></span></td>
<td><span data-ttu-id="f6fa3-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-552">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-552">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-553">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-554">55</span><span class="sxs-lookup"><span data-stu-id="f6fa3-554">55</span></span></td>
<td><span data-ttu-id="f6fa3-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f6fa3-556">685.14</span><span class="sxs-lookup"><span data-stu-id="f6fa3-556">685.14</span></span></td>
<td><span data-ttu-id="f6fa3-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-558">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-558">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-559">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-560">10</span><span class="sxs-lookup"><span data-stu-id="f6fa3-560">10</span></span></td>
<td><span data-ttu-id="f6fa3-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f6fa3-562">124.57</span><span class="sxs-lookup"><span data-stu-id="f6fa3-562">124.57</span></span></td>
<td><span data-ttu-id="f6fa3-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-565">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-566">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-567">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-568">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-570">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-570">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-571">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-572">65</span><span class="sxs-lookup"><span data-stu-id="f6fa3-572">65</span></span></td>
<td><span data-ttu-id="f6fa3-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f6fa3-574">438.75</span><span class="sxs-lookup"><span data-stu-id="f6fa3-574">438.75</span></span></td>
<td><span data-ttu-id="f6fa3-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-576">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-576">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-577">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-578">35</span><span class="sxs-lookup"><span data-stu-id="f6fa3-578">35</span></span></td>
<td><span data-ttu-id="f6fa3-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f6fa3-580">236.25</span><span class="sxs-lookup"><span data-stu-id="f6fa3-580">236.25</span></span></td>
<td><span data-ttu-id="f6fa3-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-582">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-582">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-583">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-584">65</span><span class="sxs-lookup"><span data-stu-id="f6fa3-584">65</span></span></td>
<td><span data-ttu-id="f6fa3-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f6fa3-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f6fa3-586">5,297.69</span></span></td>
<td><span data-ttu-id="f6fa3-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-588">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-588">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-589">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-590">35</span><span class="sxs-lookup"><span data-stu-id="f6fa3-590">35</span></span></td>
<td><span data-ttu-id="f6fa3-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f6fa3-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f6fa3-592">2,852.60</span></span></td>
<td><span data-ttu-id="f6fa3-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-595">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-596">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-597">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-598">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-600">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-601">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-602">60</span><span class="sxs-lookup"><span data-stu-id="f6fa3-602">60</span></span></td>
<td><span data-ttu-id="f6fa3-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f6fa3-604">535.31</span><span class="sxs-lookup"><span data-stu-id="f6fa3-604">535.31</span></span></td>
<td><span data-ttu-id="f6fa3-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-606">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-607">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-608">20</span><span class="sxs-lookup"><span data-stu-id="f6fa3-608">20</span></span></td>
<td><span data-ttu-id="f6fa3-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f6fa3-610">178.44</span><span class="sxs-lookup"><span data-stu-id="f6fa3-610">178.44</span></span></td>
<td><span data-ttu-id="f6fa3-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-612">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-613">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-614">60</span><span class="sxs-lookup"><span data-stu-id="f6fa3-614">60</span></span></td>
<td><span data-ttu-id="f6fa3-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f6fa3-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f6fa3-616">4,487.12</span></span></td>
<td><span data-ttu-id="f6fa3-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-618">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-619">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-620">20</span><span class="sxs-lookup"><span data-stu-id="f6fa3-620">20</span></span></td>
<td><span data-ttu-id="f6fa3-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f6fa3-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-622">1,495.71</span></span></td>
<td><span data-ttu-id="f6fa3-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6fa3-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-625">Cost object</span></span></th>
<th><span data-ttu-id="f6fa3-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="f6fa3-626">Magnitude</span></span></th>
<th><span data-ttu-id="f6fa3-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-627">Allocation factor</span></span></th>
<th><span data-ttu-id="f6fa3-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-628">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-630">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-631">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-632">80</span><span class="sxs-lookup"><span data-stu-id="f6fa3-632">80</span></span></td>
<td><span data-ttu-id="f6fa3-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f6fa3-634">241.05</span><span class="sxs-lookup"><span data-stu-id="f6fa3-634">241.05</span></span></td>
<td><span data-ttu-id="f6fa3-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-636">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-637">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="f6fa3-638">15</span></span></td>
<td><span data-ttu-id="f6fa3-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f6fa3-640">45.20</span><span class="sxs-lookup"><span data-stu-id="f6fa3-640">45.20</span></span></td>
<td><span data-ttu-id="f6fa3-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-642">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-643">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-644">80</span><span class="sxs-lookup"><span data-stu-id="f6fa3-644">80</span></span></td>
<td><span data-ttu-id="f6fa3-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f6fa3-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f6fa3-646">2,507.09</span></span></td>
<td><span data-ttu-id="f6fa3-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-648">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-649">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="f6fa3-650">15</span></span></td>
<td><span data-ttu-id="f6fa3-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f6fa3-652">470.08</span><span class="sxs-lookup"><span data-stu-id="f6fa3-652">470.08</span></span></td>
<td><span data-ttu-id="f6fa3-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f6fa3-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-655">Journal</span></span></th>
<th><span data-ttu-id="f6fa3-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f6fa3-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f6fa3-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-659">00004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-659">00004</span></span></td>
<td><span data-ttu-id="f6fa3-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="f6fa3-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-661">Fiscal</span></span></td>
<td><span data-ttu-id="f6fa3-662">2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-662">2017</span></span></td>
<td><span data-ttu-id="f6fa3-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-663">Period 1</span></span></td>
<td><span data-ttu-id="f6fa3-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="f6fa3-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6fa3-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-668">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-669">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-672">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-672">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-673">HR</span></span></td>
<td><span data-ttu-id="f6fa3-674">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-674">10001</span></span></td>
<td><span data-ttu-id="f6fa3-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-675">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-676">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-677">500.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-679">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-679">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-680">HR</span></span></td>
<td><span data-ttu-id="f6fa3-681">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-681">10001</span></span></td>
<td><span data-ttu-id="f6fa3-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-682">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-683">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-686">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-686">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-687">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-688">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-688">10001</span></span></td>
<td><span data-ttu-id="f6fa3-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-689">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-690">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-691">675.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-693">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-693">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-694">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-695">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-695">10001</span></span></td>
<td><span data-ttu-id="f6fa3-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-696">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-697">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="f6fa3-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-700">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-700">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-701">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-702">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-702">10001</span></span></td>
<td><span data-ttu-id="f6fa3-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-703">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-704">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-705">713.75</span><span class="sxs-lookup"><span data-stu-id="f6fa3-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-707">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-707">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-708">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-709">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-709">10001</span></span></td>
<td><span data-ttu-id="f6fa3-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-710">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-711">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="f6fa3-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-714">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-714">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-715">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-716">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-716">10001</span></span></td>
<td><span data-ttu-id="f6fa3-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-717">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-718">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-719">286.25</span><span class="sxs-lookup"><span data-stu-id="f6fa3-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-721">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-721">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-722">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-723">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-723">10001</span></span></td>
<td><span data-ttu-id="f6fa3-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-724">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-725">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="f6fa3-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-728">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-729">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-730">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-730">10001</span></span></td>
<td><span data-ttu-id="f6fa3-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-731">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-732">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-733">776.36</span><span class="sxs-lookup"><span data-stu-id="f6fa3-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-735">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-736">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-737">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-737">10001</span></span></td>
<td><span data-ttu-id="f6fa3-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-738">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-739">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f6fa3-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-742">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-743">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-744">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-744">10001</span></span></td>
<td><span data-ttu-id="f6fa3-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-745">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-746">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-747">223.64</span><span class="sxs-lookup"><span data-stu-id="f6fa3-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="f6fa3-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-749">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-750">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-751">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-751">10001</span></span></td>
<td><span data-ttu-id="f6fa3-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-752">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-753">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f6fa3-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f6fa3-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f6fa3-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f6fa3-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-757">Cost element</span></span></th>
<th><span data-ttu-id="f6fa3-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-758">Cost behavior</span></span></th>
<th><span data-ttu-id="f6fa3-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-759">Amount</span></span></th>
<th><span data-ttu-id="f6fa3-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6fa3-761">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-761">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-762">HR</span></span></td>
<td><span data-ttu-id="f6fa3-763">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-763">10001</span></span></td>
<td><span data-ttu-id="f6fa3-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-764">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-765">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="f6fa3-766">-500.00</span></span></td>
<td><span data-ttu-id="f6fa3-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-768">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-768">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-769">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-770">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-770">10001</span></span></td>
<td><span data-ttu-id="f6fa3-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-771">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-772">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-773">175.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-773">175.00</span></span></td>
<td><span data-ttu-id="f6fa3-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-775">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-775">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-776">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-777">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-777">10001</span></span></td>
<td><span data-ttu-id="f6fa3-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-778">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-779">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-780">275.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-780">275.00</span></span></td>
<td><span data-ttu-id="f6fa3-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-782">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-782">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-783">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-784">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-784">10001</span></span></td>
<td><span data-ttu-id="f6fa3-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-785">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-786">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-787">50,00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-787">50,00</span></span></td>
<td><span data-ttu-id="f6fa3-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-789">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-789">CC001</span></span></td>
<td><span data-ttu-id="f6fa3-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f6fa3-790">HR</span></span></td>
<td><span data-ttu-id="f6fa3-791">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-791">10001</span></span></td>
<td><span data-ttu-id="f6fa3-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-792">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-793">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-794">-1,245.71</span></span></td>
<td><span data-ttu-id="f6fa3-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-796">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-796">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-797">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-798">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-798">10001</span></span></td>
<td><span data-ttu-id="f6fa3-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-799">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-800">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-801">436.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-801">436.00</span></span></td>
<td><span data-ttu-id="f6fa3-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-803">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-803">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-804">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-805">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-805">10001</span></span></td>
<td><span data-ttu-id="f6fa3-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-806">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-807">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-808">685.14</span><span class="sxs-lookup"><span data-stu-id="f6fa3-808">685.14</span></span></td>
<td><span data-ttu-id="f6fa3-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-810">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-810">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-811">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-812">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-812">10001</span></span></td>
<td><span data-ttu-id="f6fa3-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-813">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-814">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-815">124.57</span><span class="sxs-lookup"><span data-stu-id="f6fa3-815">124.57</span></span></td>
<td><span data-ttu-id="f6fa3-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-817">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-817">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-818">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-819">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-819">10001</span></span></td>
<td><span data-ttu-id="f6fa3-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-820">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-821">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-822">-675.00</span></span></td>
<td><span data-ttu-id="f6fa3-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-824">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-824">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-825">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-826">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-826">10001</span></span></td>
<td><span data-ttu-id="f6fa3-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-827">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-828">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-829">438.75</span><span class="sxs-lookup"><span data-stu-id="f6fa3-829">438.75</span></span></td>
<td><span data-ttu-id="f6fa3-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-831">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-831">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-832">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-833">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-833">10001</span></span></td>
<td><span data-ttu-id="f6fa3-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-834">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-835">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-836">236.25</span><span class="sxs-lookup"><span data-stu-id="f6fa3-836">236.25</span></span></td>
<td><span data-ttu-id="f6fa3-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-838">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-838">CC002</span></span></td>
<td><span data-ttu-id="f6fa3-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-839">Finance</span></span></td>
<td><span data-ttu-id="f6fa3-840">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-840">10001</span></span></td>
<td><span data-ttu-id="f6fa3-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-841">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-842">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="f6fa3-843">-8,150.29</span></span></td>
<td><span data-ttu-id="f6fa3-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-845">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-845">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-846">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-847">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-847">10001</span></span></td>
<td><span data-ttu-id="f6fa3-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-848">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-849">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f6fa3-850">5,297.69</span></span></td>
<td><span data-ttu-id="f6fa3-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-852">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-852">CC004</span></span></td>
<td><span data-ttu-id="f6fa3-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f6fa3-853">Packaging</span></span></td>
<td><span data-ttu-id="f6fa3-854">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-854">10001</span></span></td>
<td><span data-ttu-id="f6fa3-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-855">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-856">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f6fa3-857">2,852.60</span></span></td>
<td><span data-ttu-id="f6fa3-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-859">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-859">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-860">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-861">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-861">10001</span></span></td>
<td><span data-ttu-id="f6fa3-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-862">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-863">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="f6fa3-864">-713.75</span></span></td>
<td><span data-ttu-id="f6fa3-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-866">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-867">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-868">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-868">10001</span></span></td>
<td><span data-ttu-id="f6fa3-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-869">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-870">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-871">535.31</span><span class="sxs-lookup"><span data-stu-id="f6fa3-871">535.31</span></span></td>
<td><span data-ttu-id="f6fa3-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-873">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-874">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-875">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-875">10001</span></span></td>
<td><span data-ttu-id="f6fa3-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-876">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-877">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-878">178.44</span><span class="sxs-lookup"><span data-stu-id="f6fa3-878">178.44</span></span></td>
<td><span data-ttu-id="f6fa3-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-880">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-880">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-881">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-882">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-882">10001</span></span></td>
<td><span data-ttu-id="f6fa3-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-883">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-884">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="f6fa3-885">-5,982.83</span></span></td>
<td><span data-ttu-id="f6fa3-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-887">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-888">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-889">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-889">10001</span></span></td>
<td><span data-ttu-id="f6fa3-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-890">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-891">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f6fa3-892">4,487.12</span></span></td>
<td><span data-ttu-id="f6fa3-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-894">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-895">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-896">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-896">10001</span></span></td>
<td><span data-ttu-id="f6fa3-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-897">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-898">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f6fa3-899">1,495.71</span></span></td>
<td><span data-ttu-id="f6fa3-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-901">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-901">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-902">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-903">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-903">10001</span></span></td>
<td><span data-ttu-id="f6fa3-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-904">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-905">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="f6fa3-906">-286.25</span></span></td>
<td><span data-ttu-id="f6fa3-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-908">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-909">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-910">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-910">10001</span></span></td>
<td><span data-ttu-id="f6fa3-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-911">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-912">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-913">241.05</span><span class="sxs-lookup"><span data-stu-id="f6fa3-913">241.05</span></span></td>
<td><span data-ttu-id="f6fa3-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-915">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-916">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-917">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-917">10001</span></span></td>
<td><span data-ttu-id="f6fa3-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-918">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-919">Fixed cost</span></span></td>
<td><span data-ttu-id="f6fa3-920">45.20</span><span class="sxs-lookup"><span data-stu-id="f6fa3-920">45.20</span></span></td>
<td><span data-ttu-id="f6fa3-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-922">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-922">CC003</span></span></td>
<td><span data-ttu-id="f6fa3-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="f6fa3-923">Assembly</span></span></td>
<td><span data-ttu-id="f6fa3-924">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-924">10001</span></span></td>
<td><span data-ttu-id="f6fa3-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-925">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-926">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="f6fa3-927">-2,977.17</span></span></td>
<td><span data-ttu-id="f6fa3-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-929">Prod 1</span></span></td>
<td><span data-ttu-id="f6fa3-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-930">Product 1</span></span></td>
<td><span data-ttu-id="f6fa3-931">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-931">10001</span></span></td>
<td><span data-ttu-id="f6fa3-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-932">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-933">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f6fa3-934">2,507.09</span></span></td>
<td><span data-ttu-id="f6fa3-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6fa3-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-936">Prod 2</span></span></td>
<td><span data-ttu-id="f6fa3-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-937">Product 2</span></span></td>
<td><span data-ttu-id="f6fa3-938">10001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-938">10001</span></span></td>
<td><span data-ttu-id="f6fa3-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-939">Electricity</span></span></td>
<td><span data-ttu-id="f6fa3-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-940">Variable cost</span></span></td>
<td><span data-ttu-id="f6fa3-941">470.08</span><span class="sxs-lookup"><span data-stu-id="f6fa3-941">470.08</span></span></td>
<td><span data-ttu-id="f6fa3-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="f6fa3-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="f6fa3-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="f6fa3-943">Conclusion</span></span>
<span data-ttu-id="f6fa3-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="f6fa3-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="f6fa3-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="f6fa3-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="f6fa3-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="f6fa3-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="f6fa3-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="f6fa3-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="f6fa3-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="f6fa3-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="f6fa3-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6fa3-951">CC099</span><span class="sxs-lookup"><span data-stu-id="f6fa3-951">CC099</span></span></th>
<th><span data-ttu-id="f6fa3-952">CC001</span><span class="sxs-lookup"><span data-stu-id="f6fa3-952">CC001</span></span></th>
<th><span data-ttu-id="f6fa3-953">CC002</span><span class="sxs-lookup"><span data-stu-id="f6fa3-953">CC002</span></span></th>
<th><span data-ttu-id="f6fa3-954">CC003</span><span class="sxs-lookup"><span data-stu-id="f6fa3-954">CC003</span></span></th>
<th><span data-ttu-id="f6fa3-955">CC004</span><span class="sxs-lookup"><span data-stu-id="f6fa3-955">CC004</span></span></th>
<th><span data-ttu-id="f6fa3-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-956">Proj 1</span></span></th>
<th><span data-ttu-id="f6fa3-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-957">Proj 2</span></span></th>
<th><span data-ttu-id="f6fa3-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="f6fa3-958">Prod 1</span></span></th>
<th><span data-ttu-id="f6fa3-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="f6fa3-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="f6fa3-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="f6fa3-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="f6fa3-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="f6fa3-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-971">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="f6fa3-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="f6fa3-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-973">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-974">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-975">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-976">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-977">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-978">776.36</span><span class="sxs-lookup"><span data-stu-id="f6fa3-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-979">223.64</span><span class="sxs-lookup"><span data-stu-id="f6fa3-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="f6fa3-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-982">000</span><span class="sxs-lookup"><span data-stu-id="f6fa3-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-983">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-984">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-985">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-986">0.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-987">30.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-988">10.00</span><span class="sxs-lookup"><span data-stu-id="f6fa3-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f6fa3-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f6fa3-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f6fa3-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f6fa3-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f6fa3-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="f6fa3-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="f6fa3-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="f6fa3-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="f6fa3-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="f6fa3-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="f6fa3-996">สำหรับข้อมูลเพิ่มเติม ดู [นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="f6fa3-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]