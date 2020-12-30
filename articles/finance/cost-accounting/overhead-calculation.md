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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448521"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e1d93-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="e1d93-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1d93-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="e1d93-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e1d93-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="e1d93-105">Term definition</span></span>
---------------

<span data-ttu-id="e1d93-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="e1d93-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e1d93-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="e1d93-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e1d93-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="e1d93-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e1d93-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="e1d93-109">Rent</span></span>
-   <span data-ttu-id="e1d93-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-110">Electricity</span></span>
-   <span data-ttu-id="e1d93-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="e1d93-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e1d93-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="e1d93-112">Overhead calculation overview</span></span>
<span data-ttu-id="e1d93-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e1d93-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e1d93-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="e1d93-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e1d93-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="e1d93-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e1d93-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e1d93-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e1d93-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e1d93-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1d93-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e1d93-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-119">Version type</span></span>
-   <span data-ttu-id="e1d93-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="e1d93-120">Date and time</span></span>
-   <span data-ttu-id="e1d93-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e1d93-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-122">Fiscal year</span></span>
-   <span data-ttu-id="e1d93-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-123">Fiscal period</span></span>

<span data-ttu-id="e1d93-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="e1d93-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e1d93-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="e1d93-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e1d93-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e1d93-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e1d93-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e1d93-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e1d93-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e1d93-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e1d93-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="e1d93-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e1d93-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e1d93-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e1d93-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e1d93-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e1d93-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e1d93-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e1d93-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="e1d93-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e1d93-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="e1d93-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e1d93-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e1d93-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="e1d93-140">Main account</span></span></th>
<th><span data-ttu-id="e1d93-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e1d93-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-143">CC099</span></span></td>
<td><span data-ttu-id="e1d93-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-144">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-145">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-145">10001</span></span></td>
<td><span data-ttu-id="e1d93-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-146">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e1d93-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e1d93-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e1d93-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร** ได้</span><span class="sxs-lookup"><span data-stu-id="e1d93-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e1d93-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e1d93-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="e1d93-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e1d93-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="e1d93-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e1d93-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="e1d93-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e1d93-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="e1d93-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e1d93-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e1d93-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e1d93-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e1d93-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-160">Journal</span></span></th>
<th><span data-ttu-id="e1d93-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e1d93-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e1d93-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-164">00001</span><span class="sxs-lookup"><span data-stu-id="e1d93-164">00001</span></span></td>
<td><span data-ttu-id="e1d93-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e1d93-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-166">Fiscal</span></span></td>
<td><span data-ttu-id="e1d93-167">2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-167">2017</span></span></td>
<td><span data-ttu-id="e1d93-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-168">Period 1</span></span></td>
<td><span data-ttu-id="e1d93-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e1d93-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="e1d93-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-173">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e1d93-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-177">CC099</span></span></td>
<td><span data-ttu-id="e1d93-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-178">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-179">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-179">10001</span></span></td>
<td><span data-ttu-id="e1d93-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-180">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="e1d93-181">Unclassified</span></span></td>
<td><span data-ttu-id="e1d93-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e1d93-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-185">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-187">Amount</span></span></th>
<th><span data-ttu-id="e1d93-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-189">CC099</span></span></td>
<td><span data-ttu-id="e1d93-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-190">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-191">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-191">10001</span></span></td>
<td><span data-ttu-id="e1d93-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-192">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="e1d93-193">Unclassified</span></span></td>
<td><span data-ttu-id="e1d93-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-194">10,000.00</span></span></td>
<td><span data-ttu-id="e1d93-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-196">CC099</span></span></td>
<td><span data-ttu-id="e1d93-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-197">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-198">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-198">10001</span></span></td>
<td><span data-ttu-id="e1d93-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-199">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="e1d93-200">Unclassified</span></span></td>
<td><span data-ttu-id="e1d93-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e1d93-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-203">CC099</span></span></td>
<td><span data-ttu-id="e1d93-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-204">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-205">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-205">10001</span></span></td>
<td><span data-ttu-id="e1d93-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-206">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-208">1,000.00</span></span></td>
<td><span data-ttu-id="e1d93-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-210">CC099</span></span></td>
<td><span data-ttu-id="e1d93-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-211">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-212">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-212">10001</span></span></td>
<td><span data-ttu-id="e1d93-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-213">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-214">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-215">9,000.00</span></span></td>
<td><span data-ttu-id="e1d93-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="e1d93-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e1d93-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e1d93-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e1d93-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e1d93-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="e1d93-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e1d93-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e1d93-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e1d93-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e1d93-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="e1d93-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e1d93-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="e1d93-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e1d93-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="e1d93-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e1d93-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e1d93-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-228">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="e1d93-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-230">CC001</span></span></td>
<td><span data-ttu-id="e1d93-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-231">HR</span></span></td>
<td><span data-ttu-id="e1d93-232">1,000</span><span class="sxs-lookup"><span data-stu-id="e1d93-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-233">CC002</span></span></td>
<td><span data-ttu-id="e1d93-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-234">Finance</span></span></td>
<td><span data-ttu-id="e1d93-235">6,000</span><span class="sxs-lookup"><span data-stu-id="e1d93-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-236">CC003</span></span></td>
<td><span data-ttu-id="e1d93-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-237">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-238">0</span><span class="sxs-lookup"><span data-stu-id="e1d93-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-240">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-241">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-244">CC001</span></span></td>
<td><span data-ttu-id="e1d93-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-245">HR</span></span></td>
<td><span data-ttu-id="e1d93-246">1,000</span><span class="sxs-lookup"><span data-stu-id="e1d93-246">1,000</span></span></td>
<td><span data-ttu-id="e1d93-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e1d93-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-249">CC002</span></span></td>
<td><span data-ttu-id="e1d93-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-250">Finance</span></span></td>
<td><span data-ttu-id="e1d93-251">6,000</span><span class="sxs-lookup"><span data-stu-id="e1d93-251">6,000</span></span></td>
<td><span data-ttu-id="e1d93-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e1d93-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e1d93-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-254">CC003</span></span></td>
<td><span data-ttu-id="e1d93-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-255">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-256">0</span><span class="sxs-lookup"><span data-stu-id="e1d93-256">0</span></span></td>
<td><span data-ttu-id="e1d93-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e1d93-258">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e1d93-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-261">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="e1d93-262">Formula</span></span></th>
<th><span data-ttu-id="e1d93-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-263">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-266">CC001</span></span></td>
<td><span data-ttu-id="e1d93-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-267">HR</span></span></td>
<td><span data-ttu-id="e1d93-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e1d93-269">1</span><span class="sxs-lookup"><span data-stu-id="e1d93-269">1</span></span></td>
<td><span data-ttu-id="e1d93-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e1d93-271">500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-272">CC002</span></span></td>
<td><span data-ttu-id="e1d93-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-273">Finance</span></span></td>
<td><span data-ttu-id="e1d93-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e1d93-275">1</span><span class="sxs-lookup"><span data-stu-id="e1d93-275">1</span></span></td>
<td><span data-ttu-id="e1d93-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e1d93-277">500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-278">CC003</span></span></td>
<td><span data-ttu-id="e1d93-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-279">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e1d93-281">0</span><span class="sxs-lookup"><span data-stu-id="e1d93-281">0</span></span></td>
<td><span data-ttu-id="e1d93-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e1d93-283">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e1d93-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-285">Journal</span></span></th>
<th><span data-ttu-id="e1d93-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e1d93-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e1d93-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-289">00002</span><span class="sxs-lookup"><span data-stu-id="e1d93-289">00002</span></span></td>
<td><span data-ttu-id="e1d93-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e1d93-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-291">Fiscal</span></span></td>
<td><span data-ttu-id="e1d93-292">2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-292">2017</span></span></td>
<td><span data-ttu-id="e1d93-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-293">Period 1</span></span></td>
<td><span data-ttu-id="e1d93-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e1d93-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="e1d93-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-298">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-302">CC099</span></span></td>
<td><span data-ttu-id="e1d93-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-303">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-304">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-304">10001</span></span></td>
<td><span data-ttu-id="e1d93-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-305">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-309">CC099</span></span></td>
<td><span data-ttu-id="e1d93-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-310">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-311">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-311">10001</span></span></td>
<td><span data-ttu-id="e1d93-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-312">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-313">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e1d93-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-317">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-319">Amount</span></span></th>
<th><span data-ttu-id="e1d93-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-321">CC099</span></span></td>
<td><span data-ttu-id="e1d93-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-322">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-323">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-323">10001</span></span></td>
<td><span data-ttu-id="e1d93-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-324">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="e1d93-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e1d93-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-328">CC001</span></span></td>
<td><span data-ttu-id="e1d93-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-329">HR</span></span></td>
<td><span data-ttu-id="e1d93-330">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-330">10001</span></span></td>
<td><span data-ttu-id="e1d93-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-331">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-333">500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-333">500.00</span></span></td>
<td><span data-ttu-id="e1d93-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-335">CC002</span></span></td>
<td><span data-ttu-id="e1d93-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-336">Finance</span></span></td>
<td><span data-ttu-id="e1d93-337">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-337">10001</span></span></td>
<td><span data-ttu-id="e1d93-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-338">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-340">500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-340">500.00</span></span></td>
<td><span data-ttu-id="e1d93-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-342">CC099</span></span></td>
<td><span data-ttu-id="e1d93-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1d93-343">Default cost center</span></span></td>
<td><span data-ttu-id="e1d93-344">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-344">10001</span></span></td>
<td><span data-ttu-id="e1d93-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-345">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-346">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e1d93-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-349">CC001</span></span></td>
<td><span data-ttu-id="e1d93-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-350">HR</span></span></td>
<td><span data-ttu-id="e1d93-351">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-351">10001</span></span></td>
<td><span data-ttu-id="e1d93-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-352">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-353">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-354">1,285.71</span></span></td>
<td><span data-ttu-id="e1d93-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-356">CC002</span></span></td>
<td><span data-ttu-id="e1d93-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-357">Finance</span></span></td>
<td><span data-ttu-id="e1d93-358">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-358">10001</span></span></td>
<td><span data-ttu-id="e1d93-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-359">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-360">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e1d93-361">7,714.29</span></span></td>
<td><span data-ttu-id="e1d93-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="e1d93-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e1d93-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="e1d93-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e1d93-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="e1d93-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e1d93-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e1d93-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e1d93-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="e1d93-367">Define the overhead rate</span></span>

<span data-ttu-id="e1d93-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="e1d93-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e1d93-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1d93-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-370">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="e1d93-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-372">Proj 1</span></span></td>
<td><span data-ttu-id="e1d93-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-373">Project 1</span></span></td>
<td><span data-ttu-id="e1d93-374">3</span><span class="sxs-lookup"><span data-stu-id="e1d93-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-375">Proj 2</span></span></td>
<td><span data-ttu-id="e1d93-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-376">Project 2</span></span></td>
<td><span data-ttu-id="e1d93-377">1</span><span class="sxs-lookup"><span data-stu-id="e1d93-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-379">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-380">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="e1d93-382">Units</span></span></th>
<th><span data-ttu-id="e1d93-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="e1d93-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-384">CC001</span></span></td>
<td><span data-ttu-id="e1d93-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-385">HR</span></span></td>
<td><span data-ttu-id="e1d93-386">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-386">10001</span></span></td>
<td><span data-ttu-id="e1d93-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-387">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-388">1</span><span class="sxs-lookup"><span data-stu-id="e1d93-388">1</span></span></td>
<td><span data-ttu-id="e1d93-389">10</span><span class="sxs-lookup"><span data-stu-id="e1d93-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-391">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-392">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-393">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-396">Proj 1</span></span></td>
<td><span data-ttu-id="e1d93-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-397">Project 1</span></span></td>
<td><span data-ttu-id="e1d93-398">3</span><span class="sxs-lookup"><span data-stu-id="e1d93-398">3</span></span></td>
<td><span data-ttu-id="e1d93-399">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-399">10001</span></span></td>
<td><span data-ttu-id="e1d93-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e1d93-401">30.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-402">Proj 2</span></span></td>
<td><span data-ttu-id="e1d93-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-403">Project 2</span></span></td>
<td><span data-ttu-id="e1d93-404">1</span><span class="sxs-lookup"><span data-stu-id="e1d93-404">1</span></span></td>
<td><span data-ttu-id="e1d93-405">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-405">10001</span></span></td>
<td><span data-ttu-id="e1d93-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e1d93-407">10.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e1d93-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-409">Journal</span></span></th>
<th><span data-ttu-id="e1d93-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e1d93-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e1d93-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-413">00003</span><span class="sxs-lookup"><span data-stu-id="e1d93-413">00003</span></span></td>
<td><span data-ttu-id="e1d93-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="e1d93-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e1d93-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-415">Fiscal</span></span></td>
<td><span data-ttu-id="e1d93-416">2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-416">2017</span></span></td>
<td><span data-ttu-id="e1d93-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-417">Period 1</span></span></td>
<td><span data-ttu-id="e1d93-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e1d93-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="e1d93-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-421">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-424">Proj 1</span></span></td>
<td><span data-ttu-id="e1d93-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e1d93-426">3.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-428">Proj 2</span></span></td>
<td><span data-ttu-id="e1d93-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e1d93-430">1.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e1d93-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-433">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-435">Amount</span></span></th>
<th><span data-ttu-id="e1d93-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e1d93-437">CC0001</span></span></td>
<td><span data-ttu-id="e1d93-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-438">HR</span></span></td>
<td><span data-ttu-id="e1d93-439">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-439">10001</span></span></td>
<td><span data-ttu-id="e1d93-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-440">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-441">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-442">-30.00</span></span></td>
<td><span data-ttu-id="e1d93-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-444">Proj 1</span></span></td>
<td><span data-ttu-id="e1d93-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e1d93-446">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-446">10001</span></span></td>
<td><span data-ttu-id="e1d93-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-447">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-448">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-449">30.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-449">30.00</span></span></td>
<td><span data-ttu-id="e1d93-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-451">CC001</span></span></td>
<td><span data-ttu-id="e1d93-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-452">HR</span></span></td>
<td><span data-ttu-id="e1d93-453">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-453">10001</span></span></td>
<td><span data-ttu-id="e1d93-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-454">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-455">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-456">-10.00</span></span></td>
<td><span data-ttu-id="e1d93-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-458">Proj 2</span></span></td>
<td><span data-ttu-id="e1d93-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e1d93-460">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-460">10001</span></span></td>
<td><span data-ttu-id="e1d93-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-461">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-462">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-463">10.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-463">10.00</span></span></td>
<td><span data-ttu-id="e1d93-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="e1d93-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e1d93-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e1d93-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e1d93-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="e1d93-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="e1d93-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e1d93-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e1d93-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e1d93-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e1d93-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="e1d93-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e1d93-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e1d93-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e1d93-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e1d93-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e1d93-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-475">Define the cost allocation</span></span>

<span data-ttu-id="e1d93-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e1d93-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="e1d93-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e1d93-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1d93-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-479">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="e1d93-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-481">CC002</span></span></td>
<td><span data-ttu-id="e1d93-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-482">Finance</span></span></td>
<td><span data-ttu-id="e1d93-483">35</span><span class="sxs-lookup"><span data-stu-id="e1d93-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-484">CC003</span></span></td>
<td><span data-ttu-id="e1d93-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-485">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-486">55</span><span class="sxs-lookup"><span data-stu-id="e1d93-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-487">CC004</span></span></td>
<td><span data-ttu-id="e1d93-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-488">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-489">10</span><span class="sxs-lookup"><span data-stu-id="e1d93-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="e1d93-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e1d93-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1d93-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-492">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-494">CC003</span></span></td>
<td><span data-ttu-id="e1d93-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-495">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-496">65</span><span class="sxs-lookup"><span data-stu-id="e1d93-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-497">CC004</span></span></td>
<td><span data-ttu-id="e1d93-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-498">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-499">35</span><span class="sxs-lookup"><span data-stu-id="e1d93-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="e1d93-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e1d93-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1d93-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-502">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="e1d93-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-504">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-505">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-506">60</span><span class="sxs-lookup"><span data-stu-id="e1d93-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-507">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-508">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-509">20</span><span class="sxs-lookup"><span data-stu-id="e1d93-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="e1d93-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e1d93-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="e1d93-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-512">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="e1d93-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-514">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-515">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-516">80</span><span class="sxs-lookup"><span data-stu-id="e1d93-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-517">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-518">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="e1d93-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e1d93-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e1d93-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e1d93-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="e1d93-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e1d93-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="e1d93-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-523">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-524">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-526">Amount</span></span></th>
<th><span data-ttu-id="e1d93-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-528">CC002</span></span></td>
<td><span data-ttu-id="e1d93-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-529">Finance</span></span></td>
<td><span data-ttu-id="e1d93-530">35</span><span class="sxs-lookup"><span data-stu-id="e1d93-530">35</span></span></td>
<td><span data-ttu-id="e1d93-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e1d93-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-532">175.00</span></span></td>
<td><span data-ttu-id="e1d93-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-534">CC003</span></span></td>
<td><span data-ttu-id="e1d93-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-535">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-536">55</span><span class="sxs-lookup"><span data-stu-id="e1d93-536">55</span></span></td>
<td><span data-ttu-id="e1d93-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e1d93-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-538">275.00</span></span></td>
<td><span data-ttu-id="e1d93-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-540">CC004</span></span></td>
<td><span data-ttu-id="e1d93-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-541">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-542">10</span><span class="sxs-lookup"><span data-stu-id="e1d93-542">10</span></span></td>
<td><span data-ttu-id="e1d93-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e1d93-544">50.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-544">50.00</span></span></td>
<td><span data-ttu-id="e1d93-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-546">CC002</span></span></td>
<td><span data-ttu-id="e1d93-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-547">Finance</span></span></td>
<td><span data-ttu-id="e1d93-548">35</span><span class="sxs-lookup"><span data-stu-id="e1d93-548">35</span></span></td>
<td><span data-ttu-id="e1d93-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e1d93-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-550">436.00</span></span></td>
<td><span data-ttu-id="e1d93-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-552">CC003</span></span></td>
<td><span data-ttu-id="e1d93-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-553">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-554">55</span><span class="sxs-lookup"><span data-stu-id="e1d93-554">55</span></span></td>
<td><span data-ttu-id="e1d93-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e1d93-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e1d93-556">685.14</span></span></td>
<td><span data-ttu-id="e1d93-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-558">CC004</span></span></td>
<td><span data-ttu-id="e1d93-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-559">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-560">10</span><span class="sxs-lookup"><span data-stu-id="e1d93-560">10</span></span></td>
<td><span data-ttu-id="e1d93-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e1d93-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e1d93-562">124.57</span></span></td>
<td><span data-ttu-id="e1d93-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="e1d93-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-565">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-566">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-568">Amount</span></span></th>
<th><span data-ttu-id="e1d93-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-570">CC003</span></span></td>
<td><span data-ttu-id="e1d93-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-571">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-572">65</span><span class="sxs-lookup"><span data-stu-id="e1d93-572">65</span></span></td>
<td><span data-ttu-id="e1d93-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e1d93-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e1d93-574">438.75</span></span></td>
<td><span data-ttu-id="e1d93-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-576">CC004</span></span></td>
<td><span data-ttu-id="e1d93-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-577">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-578">35</span><span class="sxs-lookup"><span data-stu-id="e1d93-578">35</span></span></td>
<td><span data-ttu-id="e1d93-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e1d93-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e1d93-580">236.25</span></span></td>
<td><span data-ttu-id="e1d93-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-582">CC003</span></span></td>
<td><span data-ttu-id="e1d93-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-583">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-584">65</span><span class="sxs-lookup"><span data-stu-id="e1d93-584">65</span></span></td>
<td><span data-ttu-id="e1d93-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e1d93-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e1d93-586">5,297.69</span></span></td>
<td><span data-ttu-id="e1d93-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-588">CC004</span></span></td>
<td><span data-ttu-id="e1d93-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-589">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-590">35</span><span class="sxs-lookup"><span data-stu-id="e1d93-590">35</span></span></td>
<td><span data-ttu-id="e1d93-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="e1d93-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e1d93-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e1d93-592">2,852.60</span></span></td>
<td><span data-ttu-id="e1d93-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="e1d93-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-595">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-596">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-598">Amount</span></span></th>
<th><span data-ttu-id="e1d93-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-600">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-601">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-602">60</span><span class="sxs-lookup"><span data-stu-id="e1d93-602">60</span></span></td>
<td><span data-ttu-id="e1d93-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="e1d93-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e1d93-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e1d93-604">535.31</span></span></td>
<td><span data-ttu-id="e1d93-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-606">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-607">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-608">20</span><span class="sxs-lookup"><span data-stu-id="e1d93-608">20</span></span></td>
<td><span data-ttu-id="e1d93-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="e1d93-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e1d93-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e1d93-610">178.44</span></span></td>
<td><span data-ttu-id="e1d93-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-612">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-613">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-614">60</span><span class="sxs-lookup"><span data-stu-id="e1d93-614">60</span></span></td>
<td><span data-ttu-id="e1d93-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="e1d93-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e1d93-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e1d93-616">4,487.12</span></span></td>
<td><span data-ttu-id="e1d93-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-618">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-619">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-620">20</span><span class="sxs-lookup"><span data-stu-id="e1d93-620">20</span></span></td>
<td><span data-ttu-id="e1d93-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="e1d93-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e1d93-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-622">1,495.71</span></span></td>
<td><span data-ttu-id="e1d93-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e1d93-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="e1d93-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-625">Cost object</span></span></th>
<th><span data-ttu-id="e1d93-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="e1d93-626">Magnitude</span></span></th>
<th><span data-ttu-id="e1d93-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e1d93-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e1d93-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-628">Amount</span></span></th>
<th><span data-ttu-id="e1d93-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-630">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-631">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-632">80</span><span class="sxs-lookup"><span data-stu-id="e1d93-632">80</span></span></td>
<td><span data-ttu-id="e1d93-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="e1d93-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e1d93-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e1d93-634">241.05</span></span></td>
<td><span data-ttu-id="e1d93-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-636">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-637">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="e1d93-638">15</span></span></td>
<td><span data-ttu-id="e1d93-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="e1d93-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e1d93-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e1d93-640">45.20</span></span></td>
<td><span data-ttu-id="e1d93-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-642">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-643">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-644">80</span><span class="sxs-lookup"><span data-stu-id="e1d93-644">80</span></span></td>
<td><span data-ttu-id="e1d93-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="e1d93-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e1d93-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e1d93-646">2,507.09</span></span></td>
<td><span data-ttu-id="e1d93-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-648">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-649">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="e1d93-650">15</span></span></td>
<td><span data-ttu-id="e1d93-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="e1d93-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e1d93-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e1d93-652">470.08</span></span></td>
<td><span data-ttu-id="e1d93-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e1d93-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="e1d93-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-655">Journal</span></span></th>
<th><span data-ttu-id="e1d93-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e1d93-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e1d93-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-659">00004</span><span class="sxs-lookup"><span data-stu-id="e1d93-659">00004</span></span></td>
<td><span data-ttu-id="e1d93-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e1d93-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-661">Fiscal</span></span></td>
<td><span data-ttu-id="e1d93-662">2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-662">2017</span></span></td>
<td><span data-ttu-id="e1d93-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-663">Period 1</span></span></td>
<td><span data-ttu-id="e1d93-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e1d93-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e1d93-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e1d93-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-668">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-672">CC001</span></span></td>
<td><span data-ttu-id="e1d93-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-673">HR</span></span></td>
<td><span data-ttu-id="e1d93-674">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-674">10001</span></span></td>
<td><span data-ttu-id="e1d93-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-675">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-677">500.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-679">CC001</span></span></td>
<td><span data-ttu-id="e1d93-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-680">HR</span></span></td>
<td><span data-ttu-id="e1d93-681">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-681">10001</span></span></td>
<td><span data-ttu-id="e1d93-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-682">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-683">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-686">CC002</span></span></td>
<td><span data-ttu-id="e1d93-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-687">Finance</span></span></td>
<td><span data-ttu-id="e1d93-688">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-688">10001</span></span></td>
<td><span data-ttu-id="e1d93-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-689">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-693">CC002</span></span></td>
<td><span data-ttu-id="e1d93-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-694">Finance</span></span></td>
<td><span data-ttu-id="e1d93-695">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-695">10001</span></span></td>
<td><span data-ttu-id="e1d93-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-696">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-697">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e1d93-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-700">CC003</span></span></td>
<td><span data-ttu-id="e1d93-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-701">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-702">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-702">10001</span></span></td>
<td><span data-ttu-id="e1d93-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-703">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e1d93-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-707">CC003</span></span></td>
<td><span data-ttu-id="e1d93-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-708">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-709">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-709">10001</span></span></td>
<td><span data-ttu-id="e1d93-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-710">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-711">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e1d93-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-714">CC003</span></span></td>
<td><span data-ttu-id="e1d93-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-715">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-716">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-716">10001</span></span></td>
<td><span data-ttu-id="e1d93-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-717">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e1d93-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-721">CC003</span></span></td>
<td><span data-ttu-id="e1d93-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-722">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-723">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-723">10001</span></span></td>
<td><span data-ttu-id="e1d93-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-724">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-725">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e1d93-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-728">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-729">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-730">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-730">10001</span></span></td>
<td><span data-ttu-id="e1d93-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-731">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e1d93-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-735">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-736">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-737">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-737">10001</span></span></td>
<td><span data-ttu-id="e1d93-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-738">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-739">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e1d93-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-742">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-743">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-744">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-744">10001</span></span></td>
<td><span data-ttu-id="e1d93-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-745">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e1d93-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e1d93-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-749">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-750">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-751">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-751">10001</span></span></td>
<td><span data-ttu-id="e1d93-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-752">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-753">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e1d93-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e1d93-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e1d93-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e1d93-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-757">Cost element</span></span></th>
<th><span data-ttu-id="e1d93-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e1d93-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-759">Amount</span></span></th>
<th><span data-ttu-id="e1d93-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e1d93-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e1d93-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-761">CC001</span></span></td>
<td><span data-ttu-id="e1d93-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-762">HR</span></span></td>
<td><span data-ttu-id="e1d93-763">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-763">10001</span></span></td>
<td><span data-ttu-id="e1d93-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-764">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="e1d93-766">-500.00</span></span></td>
<td><span data-ttu-id="e1d93-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-768">CC002</span></span></td>
<td><span data-ttu-id="e1d93-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-769">Finance</span></span></td>
<td><span data-ttu-id="e1d93-770">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-770">10001</span></span></td>
<td><span data-ttu-id="e1d93-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-771">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-773">175.00</span></span></td>
<td><span data-ttu-id="e1d93-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-775">CC003</span></span></td>
<td><span data-ttu-id="e1d93-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-776">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-777">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-777">10001</span></span></td>
<td><span data-ttu-id="e1d93-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-778">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-780">275.00</span></span></td>
<td><span data-ttu-id="e1d93-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-782">CC004</span></span></td>
<td><span data-ttu-id="e1d93-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-783">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-784">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-784">10001</span></span></td>
<td><span data-ttu-id="e1d93-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-785">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e1d93-787">50,00</span></span></td>
<td><span data-ttu-id="e1d93-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-789">CC001</span></span></td>
<td><span data-ttu-id="e1d93-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="e1d93-790">HR</span></span></td>
<td><span data-ttu-id="e1d93-791">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-791">10001</span></span></td>
<td><span data-ttu-id="e1d93-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-792">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-793">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e1d93-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-796">CC002</span></span></td>
<td><span data-ttu-id="e1d93-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-797">Finance</span></span></td>
<td><span data-ttu-id="e1d93-798">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-798">10001</span></span></td>
<td><span data-ttu-id="e1d93-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-799">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-800">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-801">436.00</span></span></td>
<td><span data-ttu-id="e1d93-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-803">CC003</span></span></td>
<td><span data-ttu-id="e1d93-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-804">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-805">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-805">10001</span></span></td>
<td><span data-ttu-id="e1d93-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-806">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-807">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e1d93-808">685.14</span></span></td>
<td><span data-ttu-id="e1d93-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-810">CC004</span></span></td>
<td><span data-ttu-id="e1d93-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-811">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-812">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-812">10001</span></span></td>
<td><span data-ttu-id="e1d93-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-813">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-814">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e1d93-815">124.57</span></span></td>
<td><span data-ttu-id="e1d93-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-817">CC002</span></span></td>
<td><span data-ttu-id="e1d93-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-818">Finance</span></span></td>
<td><span data-ttu-id="e1d93-819">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-819">10001</span></span></td>
<td><span data-ttu-id="e1d93-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-820">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-822">-675.00</span></span></td>
<td><span data-ttu-id="e1d93-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-824">CC003</span></span></td>
<td><span data-ttu-id="e1d93-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-825">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-826">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-826">10001</span></span></td>
<td><span data-ttu-id="e1d93-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-827">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e1d93-829">438.75</span></span></td>
<td><span data-ttu-id="e1d93-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-831">CC004</span></span></td>
<td><span data-ttu-id="e1d93-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-832">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-833">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-833">10001</span></span></td>
<td><span data-ttu-id="e1d93-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-834">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e1d93-836">236.25</span></span></td>
<td><span data-ttu-id="e1d93-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-838">CC002</span></span></td>
<td><span data-ttu-id="e1d93-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="e1d93-839">Finance</span></span></td>
<td><span data-ttu-id="e1d93-840">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-840">10001</span></span></td>
<td><span data-ttu-id="e1d93-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-841">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-842">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="e1d93-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e1d93-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-845">CC003</span></span></td>
<td><span data-ttu-id="e1d93-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-846">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-847">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-847">10001</span></span></td>
<td><span data-ttu-id="e1d93-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-848">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-849">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e1d93-850">5,297.69</span></span></td>
<td><span data-ttu-id="e1d93-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-852">CC004</span></span></td>
<td><span data-ttu-id="e1d93-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1d93-853">Packaging</span></span></td>
<td><span data-ttu-id="e1d93-854">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-854">10001</span></span></td>
<td><span data-ttu-id="e1d93-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-855">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-856">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e1d93-857">2,852.60</span></span></td>
<td><span data-ttu-id="e1d93-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-859">CC003</span></span></td>
<td><span data-ttu-id="e1d93-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-860">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-861">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-861">10001</span></span></td>
<td><span data-ttu-id="e1d93-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-862">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="e1d93-864">-713.75</span></span></td>
<td><span data-ttu-id="e1d93-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-866">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-867">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-868">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-868">10001</span></span></td>
<td><span data-ttu-id="e1d93-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-869">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e1d93-871">535.31</span></span></td>
<td><span data-ttu-id="e1d93-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-873">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-874">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-875">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-875">10001</span></span></td>
<td><span data-ttu-id="e1d93-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-876">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e1d93-878">178.44</span></span></td>
<td><span data-ttu-id="e1d93-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-880">CC003</span></span></td>
<td><span data-ttu-id="e1d93-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-881">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-882">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-882">10001</span></span></td>
<td><span data-ttu-id="e1d93-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-883">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-884">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="e1d93-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e1d93-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-887">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-888">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-889">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-889">10001</span></span></td>
<td><span data-ttu-id="e1d93-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-890">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-891">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e1d93-892">4,487.12</span></span></td>
<td><span data-ttu-id="e1d93-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-894">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-895">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-896">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-896">10001</span></span></td>
<td><span data-ttu-id="e1d93-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-897">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-898">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e1d93-899">1,495.71</span></span></td>
<td><span data-ttu-id="e1d93-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-901">CC003</span></span></td>
<td><span data-ttu-id="e1d93-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-902">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-903">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-903">10001</span></span></td>
<td><span data-ttu-id="e1d93-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-904">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="e1d93-906">-286.25</span></span></td>
<td><span data-ttu-id="e1d93-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-908">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-909">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-910">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-910">10001</span></span></td>
<td><span data-ttu-id="e1d93-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-911">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e1d93-913">241.05</span></span></td>
<td><span data-ttu-id="e1d93-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-915">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-916">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-917">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-917">10001</span></span></td>
<td><span data-ttu-id="e1d93-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-918">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e1d93-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e1d93-920">45.20</span></span></td>
<td><span data-ttu-id="e1d93-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-922">CC003</span></span></td>
<td><span data-ttu-id="e1d93-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="e1d93-923">Assembly</span></span></td>
<td><span data-ttu-id="e1d93-924">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-924">10001</span></span></td>
<td><span data-ttu-id="e1d93-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-925">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-926">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="e1d93-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e1d93-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-929">Prod 1</span></span></td>
<td><span data-ttu-id="e1d93-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-930">Product 1</span></span></td>
<td><span data-ttu-id="e1d93-931">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-931">10001</span></span></td>
<td><span data-ttu-id="e1d93-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-932">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-933">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e1d93-934">2,507.09</span></span></td>
<td><span data-ttu-id="e1d93-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1d93-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-936">Prod 2</span></span></td>
<td><span data-ttu-id="e1d93-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-937">Product 2</span></span></td>
<td><span data-ttu-id="e1d93-938">10001</span><span class="sxs-lookup"><span data-stu-id="e1d93-938">10001</span></span></td>
<td><span data-ttu-id="e1d93-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-939">Electricity</span></span></td>
<td><span data-ttu-id="e1d93-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-940">Variable cost</span></span></td>
<td><span data-ttu-id="e1d93-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e1d93-941">470.08</span></span></td>
<td><span data-ttu-id="e1d93-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="e1d93-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e1d93-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="e1d93-943">Conclusion</span></span>
<span data-ttu-id="e1d93-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="e1d93-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e1d93-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="e1d93-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e1d93-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="e1d93-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e1d93-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e1d93-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e1d93-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e1d93-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="e1d93-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e1d93-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e1d93-951">CC099</span></span></th>
<th><span data-ttu-id="e1d93-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e1d93-952">CC001</span></span></th>
<th><span data-ttu-id="e1d93-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e1d93-953">CC002</span></span></th>
<th><span data-ttu-id="e1d93-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e1d93-954">CC003</span></span></th>
<th><span data-ttu-id="e1d93-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e1d93-955">CC004</span></span></th>
<th><span data-ttu-id="e1d93-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-956">Proj 1</span></span></th>
<th><span data-ttu-id="e1d93-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-957">Proj 2</span></span></th>
<th><span data-ttu-id="e1d93-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="e1d93-958">Prod 1</span></span></th>
<th><span data-ttu-id="e1d93-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="e1d93-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e1d93-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="e1d93-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e1d93-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="e1d93-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-971">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e1d93-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="e1d93-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-973">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-974">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-975">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-976">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-977">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e1d93-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e1d93-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e1d93-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="e1d93-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-982">000</span><span class="sxs-lookup"><span data-stu-id="e1d93-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-983">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-984">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-985">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-986">0.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-987">30.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-988">10.00</span><span class="sxs-lookup"><span data-stu-id="e1d93-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e1d93-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e1d93-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e1d93-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e1d93-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e1d93-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e1d93-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="e1d93-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e1d93-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e1d93-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e1d93-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e1d93-996">สำหรับข้อมูลเพิ่มเติม ดู [นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="e1d93-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



