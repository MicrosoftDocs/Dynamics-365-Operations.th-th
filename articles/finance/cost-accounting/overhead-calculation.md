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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208858"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6dc83-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6dc83-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dc83-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6dc83-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6dc83-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="6dc83-105">Term definition</span></span>
---------------

<span data-ttu-id="6dc83-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="6dc83-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6dc83-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="6dc83-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6dc83-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="6dc83-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6dc83-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="6dc83-109">Rent</span></span>
-   <span data-ttu-id="6dc83-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-110">Electricity</span></span>
-   <span data-ttu-id="6dc83-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="6dc83-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6dc83-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6dc83-112">Overhead calculation overview</span></span>
<span data-ttu-id="6dc83-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6dc83-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6dc83-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6dc83-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6dc83-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="6dc83-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6dc83-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6dc83-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6dc83-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6dc83-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6dc83-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6dc83-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-119">Version type</span></span>
-   <span data-ttu-id="6dc83-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="6dc83-120">Date and time</span></span>
-   <span data-ttu-id="6dc83-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6dc83-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-122">Fiscal year</span></span>
-   <span data-ttu-id="6dc83-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-123">Fiscal period</span></span>

<span data-ttu-id="6dc83-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="6dc83-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6dc83-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="6dc83-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6dc83-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6dc83-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6dc83-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6dc83-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6dc83-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6dc83-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6dc83-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="6dc83-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6dc83-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6dc83-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6dc83-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6dc83-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6dc83-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6dc83-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6dc83-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="6dc83-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6dc83-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="6dc83-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6dc83-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6dc83-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="6dc83-140">Main account</span></span></th>
<th><span data-ttu-id="6dc83-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6dc83-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-143">CC099</span></span></td>
<td><span data-ttu-id="6dc83-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-144">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-145">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-145">10001</span></span></td>
<td><span data-ttu-id="6dc83-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-146">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6dc83-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6dc83-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6dc83-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร** ได้</span><span class="sxs-lookup"><span data-stu-id="6dc83-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6dc83-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6dc83-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="6dc83-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6dc83-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="6dc83-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6dc83-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="6dc83-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6dc83-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="6dc83-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6dc83-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6dc83-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6dc83-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6dc83-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-160">Journal</span></span></th>
<th><span data-ttu-id="6dc83-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6dc83-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6dc83-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-164">00001</span><span class="sxs-lookup"><span data-stu-id="6dc83-164">00001</span></span></td>
<td><span data-ttu-id="6dc83-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6dc83-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-166">Fiscal</span></span></td>
<td><span data-ttu-id="6dc83-167">2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-167">2017</span></span></td>
<td><span data-ttu-id="6dc83-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-168">Period 1</span></span></td>
<td><span data-ttu-id="6dc83-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6dc83-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="6dc83-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-173">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6dc83-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-177">CC099</span></span></td>
<td><span data-ttu-id="6dc83-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-178">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-179">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-179">10001</span></span></td>
<td><span data-ttu-id="6dc83-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-180">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6dc83-181">Unclassified</span></span></td>
<td><span data-ttu-id="6dc83-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6dc83-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-185">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-187">Amount</span></span></th>
<th><span data-ttu-id="6dc83-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-189">CC099</span></span></td>
<td><span data-ttu-id="6dc83-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-190">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-191">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-191">10001</span></span></td>
<td><span data-ttu-id="6dc83-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-192">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6dc83-193">Unclassified</span></span></td>
<td><span data-ttu-id="6dc83-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-194">10,000.00</span></span></td>
<td><span data-ttu-id="6dc83-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-196">CC099</span></span></td>
<td><span data-ttu-id="6dc83-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-197">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-198">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-198">10001</span></span></td>
<td><span data-ttu-id="6dc83-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-199">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6dc83-200">Unclassified</span></span></td>
<td><span data-ttu-id="6dc83-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6dc83-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-203">CC099</span></span></td>
<td><span data-ttu-id="6dc83-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-204">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-205">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-205">10001</span></span></td>
<td><span data-ttu-id="6dc83-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-206">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-208">1,000.00</span></span></td>
<td><span data-ttu-id="6dc83-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-210">CC099</span></span></td>
<td><span data-ttu-id="6dc83-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-211">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-212">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-212">10001</span></span></td>
<td><span data-ttu-id="6dc83-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-213">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-214">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-215">9,000.00</span></span></td>
<td><span data-ttu-id="6dc83-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6dc83-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6dc83-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6dc83-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6dc83-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6dc83-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="6dc83-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6dc83-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6dc83-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6dc83-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6dc83-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="6dc83-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6dc83-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="6dc83-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6dc83-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="6dc83-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6dc83-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6dc83-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-228">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="6dc83-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-230">CC001</span></span></td>
<td><span data-ttu-id="6dc83-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-231">HR</span></span></td>
<td><span data-ttu-id="6dc83-232">1,000</span><span class="sxs-lookup"><span data-stu-id="6dc83-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-233">CC002</span></span></td>
<td><span data-ttu-id="6dc83-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-234">Finance</span></span></td>
<td><span data-ttu-id="6dc83-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6dc83-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-236">CC003</span></span></td>
<td><span data-ttu-id="6dc83-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-237">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-238">0</span><span class="sxs-lookup"><span data-stu-id="6dc83-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-240">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-241">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-244">CC001</span></span></td>
<td><span data-ttu-id="6dc83-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-245">HR</span></span></td>
<td><span data-ttu-id="6dc83-246">1,000</span><span class="sxs-lookup"><span data-stu-id="6dc83-246">1,000</span></span></td>
<td><span data-ttu-id="6dc83-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6dc83-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-249">CC002</span></span></td>
<td><span data-ttu-id="6dc83-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-250">Finance</span></span></td>
<td><span data-ttu-id="6dc83-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6dc83-251">6,000</span></span></td>
<td><span data-ttu-id="6dc83-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6dc83-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6dc83-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-254">CC003</span></span></td>
<td><span data-ttu-id="6dc83-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-255">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-256">0</span><span class="sxs-lookup"><span data-stu-id="6dc83-256">0</span></span></td>
<td><span data-ttu-id="6dc83-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6dc83-258">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6dc83-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-261">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="6dc83-262">Formula</span></span></th>
<th><span data-ttu-id="6dc83-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-263">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-266">CC001</span></span></td>
<td><span data-ttu-id="6dc83-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-267">HR</span></span></td>
<td><span data-ttu-id="6dc83-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6dc83-269">1</span><span class="sxs-lookup"><span data-stu-id="6dc83-269">1</span></span></td>
<td><span data-ttu-id="6dc83-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6dc83-271">500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-272">CC002</span></span></td>
<td><span data-ttu-id="6dc83-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-273">Finance</span></span></td>
<td><span data-ttu-id="6dc83-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6dc83-275">1</span><span class="sxs-lookup"><span data-stu-id="6dc83-275">1</span></span></td>
<td><span data-ttu-id="6dc83-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6dc83-277">500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-278">CC003</span></span></td>
<td><span data-ttu-id="6dc83-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-279">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6dc83-281">0</span><span class="sxs-lookup"><span data-stu-id="6dc83-281">0</span></span></td>
<td><span data-ttu-id="6dc83-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6dc83-283">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6dc83-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-285">Journal</span></span></th>
<th><span data-ttu-id="6dc83-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6dc83-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6dc83-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-289">00002</span><span class="sxs-lookup"><span data-stu-id="6dc83-289">00002</span></span></td>
<td><span data-ttu-id="6dc83-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6dc83-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-291">Fiscal</span></span></td>
<td><span data-ttu-id="6dc83-292">2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-292">2017</span></span></td>
<td><span data-ttu-id="6dc83-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-293">Period 1</span></span></td>
<td><span data-ttu-id="6dc83-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6dc83-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="6dc83-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-298">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-302">CC099</span></span></td>
<td><span data-ttu-id="6dc83-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-303">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-304">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-304">10001</span></span></td>
<td><span data-ttu-id="6dc83-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-305">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-309">CC099</span></span></td>
<td><span data-ttu-id="6dc83-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-310">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-311">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-311">10001</span></span></td>
<td><span data-ttu-id="6dc83-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-312">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-313">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6dc83-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-317">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-319">Amount</span></span></th>
<th><span data-ttu-id="6dc83-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-321">CC099</span></span></td>
<td><span data-ttu-id="6dc83-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-322">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-323">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-323">10001</span></span></td>
<td><span data-ttu-id="6dc83-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-324">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="6dc83-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6dc83-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-328">CC001</span></span></td>
<td><span data-ttu-id="6dc83-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-329">HR</span></span></td>
<td><span data-ttu-id="6dc83-330">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-330">10001</span></span></td>
<td><span data-ttu-id="6dc83-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-331">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-333">500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-333">500.00</span></span></td>
<td><span data-ttu-id="6dc83-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-335">CC002</span></span></td>
<td><span data-ttu-id="6dc83-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-336">Finance</span></span></td>
<td><span data-ttu-id="6dc83-337">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-337">10001</span></span></td>
<td><span data-ttu-id="6dc83-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-338">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-340">500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-340">500.00</span></span></td>
<td><span data-ttu-id="6dc83-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-342">CC099</span></span></td>
<td><span data-ttu-id="6dc83-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6dc83-343">Default cost center</span></span></td>
<td><span data-ttu-id="6dc83-344">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-344">10001</span></span></td>
<td><span data-ttu-id="6dc83-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-345">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-346">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6dc83-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-349">CC001</span></span></td>
<td><span data-ttu-id="6dc83-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-350">HR</span></span></td>
<td><span data-ttu-id="6dc83-351">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-351">10001</span></span></td>
<td><span data-ttu-id="6dc83-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-352">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-353">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-354">1,285.71</span></span></td>
<td><span data-ttu-id="6dc83-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-356">CC002</span></span></td>
<td><span data-ttu-id="6dc83-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-357">Finance</span></span></td>
<td><span data-ttu-id="6dc83-358">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-358">10001</span></span></td>
<td><span data-ttu-id="6dc83-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-359">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-360">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6dc83-361">7,714.29</span></span></td>
<td><span data-ttu-id="6dc83-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6dc83-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6dc83-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6dc83-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6dc83-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="6dc83-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6dc83-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="6dc83-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6dc83-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6dc83-367">Define the overhead rate</span></span>

<span data-ttu-id="6dc83-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="6dc83-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6dc83-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6dc83-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-370">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="6dc83-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-372">Proj 1</span></span></td>
<td><span data-ttu-id="6dc83-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-373">Project 1</span></span></td>
<td><span data-ttu-id="6dc83-374">3</span><span class="sxs-lookup"><span data-stu-id="6dc83-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-375">Proj 2</span></span></td>
<td><span data-ttu-id="6dc83-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-376">Project 2</span></span></td>
<td><span data-ttu-id="6dc83-377">1</span><span class="sxs-lookup"><span data-stu-id="6dc83-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-379">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-380">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="6dc83-382">Units</span></span></th>
<th><span data-ttu-id="6dc83-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="6dc83-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-384">CC001</span></span></td>
<td><span data-ttu-id="6dc83-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-385">HR</span></span></td>
<td><span data-ttu-id="6dc83-386">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-386">10001</span></span></td>
<td><span data-ttu-id="6dc83-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-387">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-388">1</span><span class="sxs-lookup"><span data-stu-id="6dc83-388">1</span></span></td>
<td><span data-ttu-id="6dc83-389">10</span><span class="sxs-lookup"><span data-stu-id="6dc83-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-391">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-392">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-393">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-396">Proj 1</span></span></td>
<td><span data-ttu-id="6dc83-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-397">Project 1</span></span></td>
<td><span data-ttu-id="6dc83-398">3</span><span class="sxs-lookup"><span data-stu-id="6dc83-398">3</span></span></td>
<td><span data-ttu-id="6dc83-399">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-399">10001</span></span></td>
<td><span data-ttu-id="6dc83-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6dc83-401">30.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-402">Proj 2</span></span></td>
<td><span data-ttu-id="6dc83-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-403">Project 2</span></span></td>
<td><span data-ttu-id="6dc83-404">1</span><span class="sxs-lookup"><span data-stu-id="6dc83-404">1</span></span></td>
<td><span data-ttu-id="6dc83-405">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-405">10001</span></span></td>
<td><span data-ttu-id="6dc83-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6dc83-407">10.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6dc83-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-409">Journal</span></span></th>
<th><span data-ttu-id="6dc83-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6dc83-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6dc83-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-413">00003</span><span class="sxs-lookup"><span data-stu-id="6dc83-413">00003</span></span></td>
<td><span data-ttu-id="6dc83-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6dc83-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6dc83-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-415">Fiscal</span></span></td>
<td><span data-ttu-id="6dc83-416">2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-416">2017</span></span></td>
<td><span data-ttu-id="6dc83-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-417">Period 1</span></span></td>
<td><span data-ttu-id="6dc83-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6dc83-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="6dc83-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-421">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-424">Proj 1</span></span></td>
<td><span data-ttu-id="6dc83-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6dc83-426">3.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-428">Proj 2</span></span></td>
<td><span data-ttu-id="6dc83-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6dc83-430">1.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6dc83-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-433">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-435">Amount</span></span></th>
<th><span data-ttu-id="6dc83-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6dc83-437">CC0001</span></span></td>
<td><span data-ttu-id="6dc83-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-438">HR</span></span></td>
<td><span data-ttu-id="6dc83-439">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-439">10001</span></span></td>
<td><span data-ttu-id="6dc83-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-440">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-441">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-442">-30.00</span></span></td>
<td><span data-ttu-id="6dc83-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-444">Proj 1</span></span></td>
<td><span data-ttu-id="6dc83-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6dc83-446">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-446">10001</span></span></td>
<td><span data-ttu-id="6dc83-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-447">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-448">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-449">30.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-449">30.00</span></span></td>
<td><span data-ttu-id="6dc83-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-451">CC001</span></span></td>
<td><span data-ttu-id="6dc83-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-452">HR</span></span></td>
<td><span data-ttu-id="6dc83-453">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-453">10001</span></span></td>
<td><span data-ttu-id="6dc83-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-454">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-455">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-456">-10.00</span></span></td>
<td><span data-ttu-id="6dc83-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-458">Proj 2</span></span></td>
<td><span data-ttu-id="6dc83-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6dc83-460">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-460">10001</span></span></td>
<td><span data-ttu-id="6dc83-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-461">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-462">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-463">10.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-463">10.00</span></span></td>
<td><span data-ttu-id="6dc83-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="6dc83-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6dc83-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6dc83-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6dc83-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="6dc83-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="6dc83-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6dc83-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6dc83-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6dc83-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6dc83-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="6dc83-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6dc83-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6dc83-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6dc83-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6dc83-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6dc83-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-475">Define the cost allocation</span></span>

<span data-ttu-id="6dc83-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6dc83-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6dc83-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6dc83-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6dc83-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-479">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="6dc83-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-481">CC002</span></span></td>
<td><span data-ttu-id="6dc83-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-482">Finance</span></span></td>
<td><span data-ttu-id="6dc83-483">35</span><span class="sxs-lookup"><span data-stu-id="6dc83-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-484">CC003</span></span></td>
<td><span data-ttu-id="6dc83-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-485">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-486">55</span><span class="sxs-lookup"><span data-stu-id="6dc83-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-487">CC004</span></span></td>
<td><span data-ttu-id="6dc83-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-488">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-489">10</span><span class="sxs-lookup"><span data-stu-id="6dc83-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6dc83-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6dc83-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6dc83-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-492">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-494">CC003</span></span></td>
<td><span data-ttu-id="6dc83-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-495">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-496">65</span><span class="sxs-lookup"><span data-stu-id="6dc83-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-497">CC004</span></span></td>
<td><span data-ttu-id="6dc83-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-498">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-499">35</span><span class="sxs-lookup"><span data-stu-id="6dc83-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6dc83-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6dc83-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6dc83-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-502">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="6dc83-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-504">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-505">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-506">60</span><span class="sxs-lookup"><span data-stu-id="6dc83-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-507">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-508">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-509">20</span><span class="sxs-lookup"><span data-stu-id="6dc83-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6dc83-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6dc83-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6dc83-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-512">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="6dc83-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-514">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-515">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-516">80</span><span class="sxs-lookup"><span data-stu-id="6dc83-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-517">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-518">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="6dc83-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6dc83-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6dc83-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6dc83-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="6dc83-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6dc83-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6dc83-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-523">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-524">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-526">Amount</span></span></th>
<th><span data-ttu-id="6dc83-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-528">CC002</span></span></td>
<td><span data-ttu-id="6dc83-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-529">Finance</span></span></td>
<td><span data-ttu-id="6dc83-530">35</span><span class="sxs-lookup"><span data-stu-id="6dc83-530">35</span></span></td>
<td><span data-ttu-id="6dc83-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6dc83-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-532">175.00</span></span></td>
<td><span data-ttu-id="6dc83-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-534">CC003</span></span></td>
<td><span data-ttu-id="6dc83-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-535">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-536">55</span><span class="sxs-lookup"><span data-stu-id="6dc83-536">55</span></span></td>
<td><span data-ttu-id="6dc83-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6dc83-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-538">275.00</span></span></td>
<td><span data-ttu-id="6dc83-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-540">CC004</span></span></td>
<td><span data-ttu-id="6dc83-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-541">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-542">10</span><span class="sxs-lookup"><span data-stu-id="6dc83-542">10</span></span></td>
<td><span data-ttu-id="6dc83-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6dc83-544">50.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-544">50.00</span></span></td>
<td><span data-ttu-id="6dc83-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-546">CC002</span></span></td>
<td><span data-ttu-id="6dc83-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-547">Finance</span></span></td>
<td><span data-ttu-id="6dc83-548">35</span><span class="sxs-lookup"><span data-stu-id="6dc83-548">35</span></span></td>
<td><span data-ttu-id="6dc83-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6dc83-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-550">436.00</span></span></td>
<td><span data-ttu-id="6dc83-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-552">CC003</span></span></td>
<td><span data-ttu-id="6dc83-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-553">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-554">55</span><span class="sxs-lookup"><span data-stu-id="6dc83-554">55</span></span></td>
<td><span data-ttu-id="6dc83-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6dc83-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6dc83-556">685.14</span></span></td>
<td><span data-ttu-id="6dc83-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-558">CC004</span></span></td>
<td><span data-ttu-id="6dc83-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-559">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-560">10</span><span class="sxs-lookup"><span data-stu-id="6dc83-560">10</span></span></td>
<td><span data-ttu-id="6dc83-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6dc83-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6dc83-562">124.57</span></span></td>
<td><span data-ttu-id="6dc83-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6dc83-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-565">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-566">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-568">Amount</span></span></th>
<th><span data-ttu-id="6dc83-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-570">CC003</span></span></td>
<td><span data-ttu-id="6dc83-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-571">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-572">65</span><span class="sxs-lookup"><span data-stu-id="6dc83-572">65</span></span></td>
<td><span data-ttu-id="6dc83-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6dc83-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6dc83-574">438.75</span></span></td>
<td><span data-ttu-id="6dc83-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-576">CC004</span></span></td>
<td><span data-ttu-id="6dc83-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-577">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-578">35</span><span class="sxs-lookup"><span data-stu-id="6dc83-578">35</span></span></td>
<td><span data-ttu-id="6dc83-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6dc83-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6dc83-580">236.25</span></span></td>
<td><span data-ttu-id="6dc83-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-582">CC003</span></span></td>
<td><span data-ttu-id="6dc83-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-583">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-584">65</span><span class="sxs-lookup"><span data-stu-id="6dc83-584">65</span></span></td>
<td><span data-ttu-id="6dc83-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6dc83-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6dc83-586">5,297.69</span></span></td>
<td><span data-ttu-id="6dc83-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-588">CC004</span></span></td>
<td><span data-ttu-id="6dc83-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-589">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-590">35</span><span class="sxs-lookup"><span data-stu-id="6dc83-590">35</span></span></td>
<td><span data-ttu-id="6dc83-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="6dc83-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6dc83-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6dc83-592">2,852.60</span></span></td>
<td><span data-ttu-id="6dc83-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6dc83-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-595">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-596">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-598">Amount</span></span></th>
<th><span data-ttu-id="6dc83-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-600">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-601">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-602">60</span><span class="sxs-lookup"><span data-stu-id="6dc83-602">60</span></span></td>
<td><span data-ttu-id="6dc83-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="6dc83-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6dc83-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6dc83-604">535.31</span></span></td>
<td><span data-ttu-id="6dc83-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-606">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-607">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-608">20</span><span class="sxs-lookup"><span data-stu-id="6dc83-608">20</span></span></td>
<td><span data-ttu-id="6dc83-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="6dc83-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6dc83-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6dc83-610">178.44</span></span></td>
<td><span data-ttu-id="6dc83-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-612">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-613">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-614">60</span><span class="sxs-lookup"><span data-stu-id="6dc83-614">60</span></span></td>
<td><span data-ttu-id="6dc83-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="6dc83-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6dc83-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6dc83-616">4,487.12</span></span></td>
<td><span data-ttu-id="6dc83-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-618">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-619">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-620">20</span><span class="sxs-lookup"><span data-stu-id="6dc83-620">20</span></span></td>
<td><span data-ttu-id="6dc83-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="6dc83-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6dc83-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-622">1,495.71</span></span></td>
<td><span data-ttu-id="6dc83-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6dc83-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6dc83-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-625">Cost object</span></span></th>
<th><span data-ttu-id="6dc83-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6dc83-626">Magnitude</span></span></th>
<th><span data-ttu-id="6dc83-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6dc83-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6dc83-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-628">Amount</span></span></th>
<th><span data-ttu-id="6dc83-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-630">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-631">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-632">80</span><span class="sxs-lookup"><span data-stu-id="6dc83-632">80</span></span></td>
<td><span data-ttu-id="6dc83-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="6dc83-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6dc83-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6dc83-634">241.05</span></span></td>
<td><span data-ttu-id="6dc83-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-636">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-637">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="6dc83-638">15</span></span></td>
<td><span data-ttu-id="6dc83-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="6dc83-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6dc83-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6dc83-640">45.20</span></span></td>
<td><span data-ttu-id="6dc83-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-642">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-643">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-644">80</span><span class="sxs-lookup"><span data-stu-id="6dc83-644">80</span></span></td>
<td><span data-ttu-id="6dc83-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="6dc83-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6dc83-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6dc83-646">2,507.09</span></span></td>
<td><span data-ttu-id="6dc83-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-648">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-649">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="6dc83-650">15</span></span></td>
<td><span data-ttu-id="6dc83-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="6dc83-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6dc83-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6dc83-652">470.08</span></span></td>
<td><span data-ttu-id="6dc83-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6dc83-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="6dc83-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-655">Journal</span></span></th>
<th><span data-ttu-id="6dc83-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6dc83-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6dc83-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-659">00004</span><span class="sxs-lookup"><span data-stu-id="6dc83-659">00004</span></span></td>
<td><span data-ttu-id="6dc83-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6dc83-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-661">Fiscal</span></span></td>
<td><span data-ttu-id="6dc83-662">2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-662">2017</span></span></td>
<td><span data-ttu-id="6dc83-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-663">Period 1</span></span></td>
<td><span data-ttu-id="6dc83-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6dc83-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6dc83-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6dc83-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-668">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-672">CC001</span></span></td>
<td><span data-ttu-id="6dc83-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-673">HR</span></span></td>
<td><span data-ttu-id="6dc83-674">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-674">10001</span></span></td>
<td><span data-ttu-id="6dc83-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-675">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-677">500.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-679">CC001</span></span></td>
<td><span data-ttu-id="6dc83-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-680">HR</span></span></td>
<td><span data-ttu-id="6dc83-681">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-681">10001</span></span></td>
<td><span data-ttu-id="6dc83-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-682">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-683">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-686">CC002</span></span></td>
<td><span data-ttu-id="6dc83-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-687">Finance</span></span></td>
<td><span data-ttu-id="6dc83-688">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-688">10001</span></span></td>
<td><span data-ttu-id="6dc83-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-689">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-693">CC002</span></span></td>
<td><span data-ttu-id="6dc83-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-694">Finance</span></span></td>
<td><span data-ttu-id="6dc83-695">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-695">10001</span></span></td>
<td><span data-ttu-id="6dc83-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-696">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-697">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6dc83-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-700">CC003</span></span></td>
<td><span data-ttu-id="6dc83-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-701">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-702">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-702">10001</span></span></td>
<td><span data-ttu-id="6dc83-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-703">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6dc83-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-707">CC003</span></span></td>
<td><span data-ttu-id="6dc83-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-708">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-709">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-709">10001</span></span></td>
<td><span data-ttu-id="6dc83-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-710">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-711">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6dc83-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-714">CC003</span></span></td>
<td><span data-ttu-id="6dc83-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-715">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-716">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-716">10001</span></span></td>
<td><span data-ttu-id="6dc83-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-717">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6dc83-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-721">CC003</span></span></td>
<td><span data-ttu-id="6dc83-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-722">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-723">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-723">10001</span></span></td>
<td><span data-ttu-id="6dc83-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-724">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-725">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6dc83-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-728">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-729">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-730">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-730">10001</span></span></td>
<td><span data-ttu-id="6dc83-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-731">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6dc83-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-735">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-736">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-737">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-737">10001</span></span></td>
<td><span data-ttu-id="6dc83-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-738">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-739">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6dc83-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-742">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-743">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-744">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-744">10001</span></span></td>
<td><span data-ttu-id="6dc83-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-745">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6dc83-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6dc83-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-749">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-750">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-751">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-751">10001</span></span></td>
<td><span data-ttu-id="6dc83-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-752">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-753">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6dc83-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6dc83-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6dc83-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6dc83-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-757">Cost element</span></span></th>
<th><span data-ttu-id="6dc83-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6dc83-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-759">Amount</span></span></th>
<th><span data-ttu-id="6dc83-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6dc83-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6dc83-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-761">CC001</span></span></td>
<td><span data-ttu-id="6dc83-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-762">HR</span></span></td>
<td><span data-ttu-id="6dc83-763">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-763">10001</span></span></td>
<td><span data-ttu-id="6dc83-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-764">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="6dc83-766">-500.00</span></span></td>
<td><span data-ttu-id="6dc83-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-768">CC002</span></span></td>
<td><span data-ttu-id="6dc83-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-769">Finance</span></span></td>
<td><span data-ttu-id="6dc83-770">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-770">10001</span></span></td>
<td><span data-ttu-id="6dc83-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-771">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-773">175.00</span></span></td>
<td><span data-ttu-id="6dc83-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-775">CC003</span></span></td>
<td><span data-ttu-id="6dc83-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-776">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-777">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-777">10001</span></span></td>
<td><span data-ttu-id="6dc83-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-778">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-780">275.00</span></span></td>
<td><span data-ttu-id="6dc83-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-782">CC004</span></span></td>
<td><span data-ttu-id="6dc83-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-783">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-784">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-784">10001</span></span></td>
<td><span data-ttu-id="6dc83-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-785">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6dc83-787">50,00</span></span></td>
<td><span data-ttu-id="6dc83-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-789">CC001</span></span></td>
<td><span data-ttu-id="6dc83-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6dc83-790">HR</span></span></td>
<td><span data-ttu-id="6dc83-791">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-791">10001</span></span></td>
<td><span data-ttu-id="6dc83-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-792">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-793">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6dc83-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-796">CC002</span></span></td>
<td><span data-ttu-id="6dc83-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-797">Finance</span></span></td>
<td><span data-ttu-id="6dc83-798">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-798">10001</span></span></td>
<td><span data-ttu-id="6dc83-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-799">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-800">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-801">436.00</span></span></td>
<td><span data-ttu-id="6dc83-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-803">CC003</span></span></td>
<td><span data-ttu-id="6dc83-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-804">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-805">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-805">10001</span></span></td>
<td><span data-ttu-id="6dc83-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-806">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-807">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6dc83-808">685.14</span></span></td>
<td><span data-ttu-id="6dc83-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-810">CC004</span></span></td>
<td><span data-ttu-id="6dc83-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-811">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-812">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-812">10001</span></span></td>
<td><span data-ttu-id="6dc83-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-813">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-814">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6dc83-815">124.57</span></span></td>
<td><span data-ttu-id="6dc83-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-817">CC002</span></span></td>
<td><span data-ttu-id="6dc83-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-818">Finance</span></span></td>
<td><span data-ttu-id="6dc83-819">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-819">10001</span></span></td>
<td><span data-ttu-id="6dc83-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-820">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-822">-675.00</span></span></td>
<td><span data-ttu-id="6dc83-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-824">CC003</span></span></td>
<td><span data-ttu-id="6dc83-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-825">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-826">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-826">10001</span></span></td>
<td><span data-ttu-id="6dc83-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-827">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6dc83-829">438.75</span></span></td>
<td><span data-ttu-id="6dc83-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-831">CC004</span></span></td>
<td><span data-ttu-id="6dc83-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-832">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-833">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-833">10001</span></span></td>
<td><span data-ttu-id="6dc83-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-834">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6dc83-836">236.25</span></span></td>
<td><span data-ttu-id="6dc83-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-838">CC002</span></span></td>
<td><span data-ttu-id="6dc83-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6dc83-839">Finance</span></span></td>
<td><span data-ttu-id="6dc83-840">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-840">10001</span></span></td>
<td><span data-ttu-id="6dc83-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-841">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-842">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="6dc83-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6dc83-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-845">CC003</span></span></td>
<td><span data-ttu-id="6dc83-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-846">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-847">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-847">10001</span></span></td>
<td><span data-ttu-id="6dc83-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-848">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-849">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6dc83-850">5,297.69</span></span></td>
<td><span data-ttu-id="6dc83-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-852">CC004</span></span></td>
<td><span data-ttu-id="6dc83-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6dc83-853">Packaging</span></span></td>
<td><span data-ttu-id="6dc83-854">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-854">10001</span></span></td>
<td><span data-ttu-id="6dc83-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-855">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-856">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6dc83-857">2,852.60</span></span></td>
<td><span data-ttu-id="6dc83-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-859">CC003</span></span></td>
<td><span data-ttu-id="6dc83-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-860">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-861">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-861">10001</span></span></td>
<td><span data-ttu-id="6dc83-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-862">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="6dc83-864">-713.75</span></span></td>
<td><span data-ttu-id="6dc83-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-866">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-867">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-868">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-868">10001</span></span></td>
<td><span data-ttu-id="6dc83-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-869">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6dc83-871">535.31</span></span></td>
<td><span data-ttu-id="6dc83-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-873">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-874">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-875">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-875">10001</span></span></td>
<td><span data-ttu-id="6dc83-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-876">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6dc83-878">178.44</span></span></td>
<td><span data-ttu-id="6dc83-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-880">CC003</span></span></td>
<td><span data-ttu-id="6dc83-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-881">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-882">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-882">10001</span></span></td>
<td><span data-ttu-id="6dc83-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-883">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-884">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="6dc83-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6dc83-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-887">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-888">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-889">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-889">10001</span></span></td>
<td><span data-ttu-id="6dc83-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-890">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-891">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6dc83-892">4,487.12</span></span></td>
<td><span data-ttu-id="6dc83-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-894">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-895">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-896">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-896">10001</span></span></td>
<td><span data-ttu-id="6dc83-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-897">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-898">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6dc83-899">1,495.71</span></span></td>
<td><span data-ttu-id="6dc83-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-901">CC003</span></span></td>
<td><span data-ttu-id="6dc83-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-902">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-903">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-903">10001</span></span></td>
<td><span data-ttu-id="6dc83-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-904">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="6dc83-906">-286.25</span></span></td>
<td><span data-ttu-id="6dc83-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-908">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-909">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-910">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-910">10001</span></span></td>
<td><span data-ttu-id="6dc83-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-911">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6dc83-913">241.05</span></span></td>
<td><span data-ttu-id="6dc83-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-915">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-916">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-917">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-917">10001</span></span></td>
<td><span data-ttu-id="6dc83-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-918">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6dc83-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6dc83-920">45.20</span></span></td>
<td><span data-ttu-id="6dc83-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-922">CC003</span></span></td>
<td><span data-ttu-id="6dc83-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6dc83-923">Assembly</span></span></td>
<td><span data-ttu-id="6dc83-924">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-924">10001</span></span></td>
<td><span data-ttu-id="6dc83-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-925">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-926">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="6dc83-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6dc83-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-929">Prod 1</span></span></td>
<td><span data-ttu-id="6dc83-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-930">Product 1</span></span></td>
<td><span data-ttu-id="6dc83-931">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-931">10001</span></span></td>
<td><span data-ttu-id="6dc83-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-932">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-933">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6dc83-934">2,507.09</span></span></td>
<td><span data-ttu-id="6dc83-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6dc83-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-936">Prod 2</span></span></td>
<td><span data-ttu-id="6dc83-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-937">Product 2</span></span></td>
<td><span data-ttu-id="6dc83-938">10001</span><span class="sxs-lookup"><span data-stu-id="6dc83-938">10001</span></span></td>
<td><span data-ttu-id="6dc83-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-939">Electricity</span></span></td>
<td><span data-ttu-id="6dc83-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-940">Variable cost</span></span></td>
<td><span data-ttu-id="6dc83-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6dc83-941">470.08</span></span></td>
<td><span data-ttu-id="6dc83-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6dc83-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6dc83-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="6dc83-943">Conclusion</span></span>
<span data-ttu-id="6dc83-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="6dc83-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6dc83-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="6dc83-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6dc83-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="6dc83-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6dc83-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6dc83-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6dc83-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6dc83-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="6dc83-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6dc83-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6dc83-951">CC099</span></span></th>
<th><span data-ttu-id="6dc83-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6dc83-952">CC001</span></span></th>
<th><span data-ttu-id="6dc83-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6dc83-953">CC002</span></span></th>
<th><span data-ttu-id="6dc83-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6dc83-954">CC003</span></span></th>
<th><span data-ttu-id="6dc83-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6dc83-955">CC004</span></span></th>
<th><span data-ttu-id="6dc83-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-956">Proj 1</span></span></th>
<th><span data-ttu-id="6dc83-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-957">Proj 2</span></span></th>
<th><span data-ttu-id="6dc83-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6dc83-958">Prod 1</span></span></th>
<th><span data-ttu-id="6dc83-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6dc83-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6dc83-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6dc83-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6dc83-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6dc83-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-971">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6dc83-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6dc83-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-973">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-974">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-975">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-976">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-977">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6dc83-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6dc83-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6dc83-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6dc83-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-982">000</span><span class="sxs-lookup"><span data-stu-id="6dc83-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-983">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-984">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-985">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-986">0.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-987">30.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-988">10.00</span><span class="sxs-lookup"><span data-stu-id="6dc83-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6dc83-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6dc83-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6dc83-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6dc83-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6dc83-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6dc83-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="6dc83-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6dc83-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6dc83-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6dc83-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6dc83-996">สำหรับข้อมูลเพิ่มเติม ดู [นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="6dc83-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]