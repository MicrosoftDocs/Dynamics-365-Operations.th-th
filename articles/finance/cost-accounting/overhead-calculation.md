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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976486"
---
# <a name="overhead-calculation"></a><span data-ttu-id="5c185-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="5c185-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c185-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="5c185-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5c185-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="5c185-105">Term definition</span></span>
---------------

<span data-ttu-id="5c185-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="5c185-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5c185-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="5c185-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5c185-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="5c185-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5c185-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="5c185-109">Rent</span></span>
-   <span data-ttu-id="5c185-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-110">Electricity</span></span>
-   <span data-ttu-id="5c185-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="5c185-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5c185-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="5c185-112">Overhead calculation overview</span></span>
<span data-ttu-id="5c185-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5c185-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5c185-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="5c185-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5c185-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="5c185-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5c185-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5c185-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="5c185-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5c185-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5c185-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5c185-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="5c185-119">Version type</span></span>
-   <span data-ttu-id="5c185-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="5c185-120">Date and time</span></span>
-   <span data-ttu-id="5c185-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5c185-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-122">Fiscal year</span></span>
-   <span data-ttu-id="5c185-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-123">Fiscal period</span></span>

<span data-ttu-id="5c185-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="5c185-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5c185-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="5c185-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5c185-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c185-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5c185-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5c185-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="5c185-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5c185-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5c185-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5c185-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="5c185-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5c185-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5c185-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5c185-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5c185-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5c185-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5c185-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5c185-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5c185-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5c185-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="5c185-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5c185-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c185-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="5c185-140">Main account</span></span></th>
<th><span data-ttu-id="5c185-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5c185-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-143">CC099</span></span></td>
<td><span data-ttu-id="5c185-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-144">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-145">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-145">10001</span></span></td>
<td><span data-ttu-id="5c185-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-146">Electricity</span></span></td>
<td><span data-ttu-id="5c185-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5c185-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5c185-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5c185-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="5c185-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5c185-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5c185-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="5c185-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5c185-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="5c185-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5c185-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="5c185-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5c185-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="5c185-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5c185-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5c185-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5c185-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5c185-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-160">Journal</span></span></th>
<th><span data-ttu-id="5c185-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c185-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c185-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="5c185-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-164">00001</span><span class="sxs-lookup"><span data-stu-id="5c185-164">00001</span></span></td>
<td><span data-ttu-id="5c185-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5c185-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-166">Fiscal</span></span></td>
<td><span data-ttu-id="5c185-167">2017</span><span class="sxs-lookup"><span data-stu-id="5c185-167">2017</span></span></td>
<td><span data-ttu-id="5c185-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-168">Period 1</span></span></td>
<td><span data-ttu-id="5c185-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5c185-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="5c185-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-173">Cost element</span></span></th>
<th><span data-ttu-id="5c185-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5c185-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-177">CC099</span></span></td>
<td><span data-ttu-id="5c185-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-178">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-179">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-179">10001</span></span></td>
<td><span data-ttu-id="5c185-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-180">Electricity</span></span></td>
<td><span data-ttu-id="5c185-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="5c185-181">Unclassified</span></span></td>
<td><span data-ttu-id="5c185-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c185-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-185">Cost element</span></span></th>
<th><span data-ttu-id="5c185-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-187">Amount</span></span></th>
<th><span data-ttu-id="5c185-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-189">CC099</span></span></td>
<td><span data-ttu-id="5c185-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-190">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-191">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-191">10001</span></span></td>
<td><span data-ttu-id="5c185-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-192">Electricity</span></span></td>
<td><span data-ttu-id="5c185-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="5c185-193">Unclassified</span></span></td>
<td><span data-ttu-id="5c185-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-194">10,000.00</span></span></td>
<td><span data-ttu-id="5c185-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-196">CC099</span></span></td>
<td><span data-ttu-id="5c185-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-197">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-198">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-198">10001</span></span></td>
<td><span data-ttu-id="5c185-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-199">Electricity</span></span></td>
<td><span data-ttu-id="5c185-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="5c185-200">Unclassified</span></span></td>
<td><span data-ttu-id="5c185-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5c185-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-203">CC099</span></span></td>
<td><span data-ttu-id="5c185-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-204">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-205">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-205">10001</span></span></td>
<td><span data-ttu-id="5c185-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-206">Electricity</span></span></td>
<td><span data-ttu-id="5c185-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-208">1,000.00</span></span></td>
<td><span data-ttu-id="5c185-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-210">CC099</span></span></td>
<td><span data-ttu-id="5c185-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-211">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-212">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-212">10001</span></span></td>
<td><span data-ttu-id="5c185-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-213">Electricity</span></span></td>
<td><span data-ttu-id="5c185-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-214">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-215">9,000.00</span></span></td>
<td><span data-ttu-id="5c185-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="5c185-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5c185-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5c185-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5c185-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5c185-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="5c185-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5c185-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5c185-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5c185-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5c185-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="5c185-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5c185-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="5c185-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5c185-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="5c185-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5c185-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5c185-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-228">Cost object</span></span></th>
<th><span data-ttu-id="5c185-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="5c185-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-230">CC001</span></span></td>
<td><span data-ttu-id="5c185-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-231">HR</span></span></td>
<td><span data-ttu-id="5c185-232">1,000</span><span class="sxs-lookup"><span data-stu-id="5c185-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-233">CC002</span></span></td>
<td><span data-ttu-id="5c185-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-234">Finance</span></span></td>
<td><span data-ttu-id="5c185-235">6,000</span><span class="sxs-lookup"><span data-stu-id="5c185-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-236">CC003</span></span></td>
<td><span data-ttu-id="5c185-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-237">Assembly</span></span></td>
<td><span data-ttu-id="5c185-238">0</span><span class="sxs-lookup"><span data-stu-id="5c185-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-240">Cost object</span></span></th>
<th><span data-ttu-id="5c185-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-241">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-244">CC001</span></span></td>
<td><span data-ttu-id="5c185-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-245">HR</span></span></td>
<td><span data-ttu-id="5c185-246">1,000</span><span class="sxs-lookup"><span data-stu-id="5c185-246">1,000</span></span></td>
<td><span data-ttu-id="5c185-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5c185-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5c185-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-249">CC002</span></span></td>
<td><span data-ttu-id="5c185-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-250">Finance</span></span></td>
<td><span data-ttu-id="5c185-251">6,000</span><span class="sxs-lookup"><span data-stu-id="5c185-251">6,000</span></span></td>
<td><span data-ttu-id="5c185-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5c185-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5c185-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-254">CC003</span></span></td>
<td><span data-ttu-id="5c185-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-255">Assembly</span></span></td>
<td><span data-ttu-id="5c185-256">0</span><span class="sxs-lookup"><span data-stu-id="5c185-256">0</span></span></td>
<td><span data-ttu-id="5c185-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5c185-258">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5c185-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-261">Cost object</span></span></th>
<th><span data-ttu-id="5c185-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="5c185-262">Formula</span></span></th>
<th><span data-ttu-id="5c185-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-263">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-266">CC001</span></span></td>
<td><span data-ttu-id="5c185-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-267">HR</span></span></td>
<td><span data-ttu-id="5c185-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5c185-269">1</span><span class="sxs-lookup"><span data-stu-id="5c185-269">1</span></span></td>
<td><span data-ttu-id="5c185-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5c185-271">500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-272">CC002</span></span></td>
<td><span data-ttu-id="5c185-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-273">Finance</span></span></td>
<td><span data-ttu-id="5c185-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5c185-275">1</span><span class="sxs-lookup"><span data-stu-id="5c185-275">1</span></span></td>
<td><span data-ttu-id="5c185-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5c185-277">500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-278">CC003</span></span></td>
<td><span data-ttu-id="5c185-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-279">Assembly</span></span></td>
<td><span data-ttu-id="5c185-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5c185-281">0</span><span class="sxs-lookup"><span data-stu-id="5c185-281">0</span></span></td>
<td><span data-ttu-id="5c185-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5c185-283">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5c185-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-285">Journal</span></span></th>
<th><span data-ttu-id="5c185-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c185-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c185-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="5c185-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-289">00002</span><span class="sxs-lookup"><span data-stu-id="5c185-289">00002</span></span></td>
<td><span data-ttu-id="5c185-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5c185-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-291">Fiscal</span></span></td>
<td><span data-ttu-id="5c185-292">2017</span><span class="sxs-lookup"><span data-stu-id="5c185-292">2017</span></span></td>
<td><span data-ttu-id="5c185-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-293">Period 1</span></span></td>
<td><span data-ttu-id="5c185-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5c185-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="5c185-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-298">Cost element</span></span></th>
<th><span data-ttu-id="5c185-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-302">CC099</span></span></td>
<td><span data-ttu-id="5c185-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-303">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-304">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-304">10001</span></span></td>
<td><span data-ttu-id="5c185-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-305">Electricity</span></span></td>
<td><span data-ttu-id="5c185-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-309">CC099</span></span></td>
<td><span data-ttu-id="5c185-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-310">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-311">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-311">10001</span></span></td>
<td><span data-ttu-id="5c185-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-312">Electricity</span></span></td>
<td><span data-ttu-id="5c185-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-313">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c185-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-317">Cost element</span></span></th>
<th><span data-ttu-id="5c185-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-319">Amount</span></span></th>
<th><span data-ttu-id="5c185-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-321">CC099</span></span></td>
<td><span data-ttu-id="5c185-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-322">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-323">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-323">10001</span></span></td>
<td><span data-ttu-id="5c185-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-324">Electricity</span></span></td>
<td><span data-ttu-id="5c185-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="5c185-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5c185-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-328">CC001</span></span></td>
<td><span data-ttu-id="5c185-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-329">HR</span></span></td>
<td><span data-ttu-id="5c185-330">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-330">10001</span></span></td>
<td><span data-ttu-id="5c185-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-331">Electricity</span></span></td>
<td><span data-ttu-id="5c185-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-333">500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-333">500.00</span></span></td>
<td><span data-ttu-id="5c185-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-335">CC002</span></span></td>
<td><span data-ttu-id="5c185-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-336">Finance</span></span></td>
<td><span data-ttu-id="5c185-337">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-337">10001</span></span></td>
<td><span data-ttu-id="5c185-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-338">Electricity</span></span></td>
<td><span data-ttu-id="5c185-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-340">500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-340">500.00</span></span></td>
<td><span data-ttu-id="5c185-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-342">CC099</span></span></td>
<td><span data-ttu-id="5c185-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5c185-343">Default cost center</span></span></td>
<td><span data-ttu-id="5c185-344">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-344">10001</span></span></td>
<td><span data-ttu-id="5c185-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-345">Electricity</span></span></td>
<td><span data-ttu-id="5c185-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-346">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="5c185-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5c185-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-349">CC001</span></span></td>
<td><span data-ttu-id="5c185-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-350">HR</span></span></td>
<td><span data-ttu-id="5c185-351">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-351">10001</span></span></td>
<td><span data-ttu-id="5c185-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-352">Electricity</span></span></td>
<td><span data-ttu-id="5c185-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-353">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5c185-354">1,285.71</span></span></td>
<td><span data-ttu-id="5c185-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-356">CC002</span></span></td>
<td><span data-ttu-id="5c185-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-357">Finance</span></span></td>
<td><span data-ttu-id="5c185-358">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-358">10001</span></span></td>
<td><span data-ttu-id="5c185-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-359">Electricity</span></span></td>
<td><span data-ttu-id="5c185-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-360">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5c185-361">7,714.29</span></span></td>
<td><span data-ttu-id="5c185-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="5c185-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5c185-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="5c185-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5c185-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="5c185-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5c185-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="5c185-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5c185-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="5c185-367">Define the overhead rate</span></span>

<span data-ttu-id="5c185-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="5c185-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5c185-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="5c185-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-370">Cost object</span></span></th>
<th><span data-ttu-id="5c185-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5c185-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-372">Proj 1</span></span></td>
<td><span data-ttu-id="5c185-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-373">Project 1</span></span></td>
<td><span data-ttu-id="5c185-374">3</span><span class="sxs-lookup"><span data-stu-id="5c185-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-375">Proj 2</span></span></td>
<td><span data-ttu-id="5c185-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-376">Project 2</span></span></td>
<td><span data-ttu-id="5c185-377">1</span><span class="sxs-lookup"><span data-stu-id="5c185-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-379">Cost object</span></span></th>
<th><span data-ttu-id="5c185-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-380">Cost element</span></span></th>
<th><span data-ttu-id="5c185-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="5c185-382">Units</span></span></th>
<th><span data-ttu-id="5c185-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="5c185-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-384">CC001</span></span></td>
<td><span data-ttu-id="5c185-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-385">HR</span></span></td>
<td><span data-ttu-id="5c185-386">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-386">10001</span></span></td>
<td><span data-ttu-id="5c185-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-387">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-388">1</span><span class="sxs-lookup"><span data-stu-id="5c185-388">1</span></span></td>
<td><span data-ttu-id="5c185-389">10</span><span class="sxs-lookup"><span data-stu-id="5c185-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-391">Cost object</span></span></th>
<th><span data-ttu-id="5c185-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-392">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-393">Cost element</span></span></th>
<th><span data-ttu-id="5c185-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-396">Proj 1</span></span></td>
<td><span data-ttu-id="5c185-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-397">Project 1</span></span></td>
<td><span data-ttu-id="5c185-398">3</span><span class="sxs-lookup"><span data-stu-id="5c185-398">3</span></span></td>
<td><span data-ttu-id="5c185-399">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-399">10001</span></span></td>
<td><span data-ttu-id="5c185-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5c185-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5c185-401">30.00</span><span class="sxs-lookup"><span data-stu-id="5c185-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-402">Proj 2</span></span></td>
<td><span data-ttu-id="5c185-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-403">Project 2</span></span></td>
<td><span data-ttu-id="5c185-404">1</span><span class="sxs-lookup"><span data-stu-id="5c185-404">1</span></span></td>
<td><span data-ttu-id="5c185-405">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-405">10001</span></span></td>
<td><span data-ttu-id="5c185-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5c185-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5c185-407">10.00</span><span class="sxs-lookup"><span data-stu-id="5c185-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5c185-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-409">Journal</span></span></th>
<th><span data-ttu-id="5c185-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c185-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c185-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="5c185-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-413">00003</span><span class="sxs-lookup"><span data-stu-id="5c185-413">00003</span></span></td>
<td><span data-ttu-id="5c185-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="5c185-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5c185-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-415">Fiscal</span></span></td>
<td><span data-ttu-id="5c185-416">2017</span><span class="sxs-lookup"><span data-stu-id="5c185-416">2017</span></span></td>
<td><span data-ttu-id="5c185-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-417">Period 1</span></span></td>
<td><span data-ttu-id="5c185-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5c185-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="5c185-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-421">Cost object</span></span></th>
<th><span data-ttu-id="5c185-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-424">Proj 1</span></span></td>
<td><span data-ttu-id="5c185-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="5c185-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5c185-426">3.00</span><span class="sxs-lookup"><span data-stu-id="5c185-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-428">Proj 2</span></span></td>
<td><span data-ttu-id="5c185-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="5c185-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5c185-430">1.00</span><span class="sxs-lookup"><span data-stu-id="5c185-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c185-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-433">Cost element</span></span></th>
<th><span data-ttu-id="5c185-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-435">Amount</span></span></th>
<th><span data-ttu-id="5c185-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5c185-437">CC0001</span></span></td>
<td><span data-ttu-id="5c185-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-438">HR</span></span></td>
<td><span data-ttu-id="5c185-439">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-439">10001</span></span></td>
<td><span data-ttu-id="5c185-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-440">Electricity</span></span></td>
<td><span data-ttu-id="5c185-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-441">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="5c185-442">-30.00</span></span></td>
<td><span data-ttu-id="5c185-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-444">Proj 1</span></span></td>
<td><span data-ttu-id="5c185-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="5c185-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5c185-446">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-446">10001</span></span></td>
<td><span data-ttu-id="5c185-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-447">Electricity</span></span></td>
<td><span data-ttu-id="5c185-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-448">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-449">30.00</span><span class="sxs-lookup"><span data-stu-id="5c185-449">30.00</span></span></td>
<td><span data-ttu-id="5c185-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-451">CC001</span></span></td>
<td><span data-ttu-id="5c185-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-452">HR</span></span></td>
<td><span data-ttu-id="5c185-453">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-453">10001</span></span></td>
<td><span data-ttu-id="5c185-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-454">Electricity</span></span></td>
<td><span data-ttu-id="5c185-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-455">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="5c185-456">-10.00</span></span></td>
<td><span data-ttu-id="5c185-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-458">Proj 2</span></span></td>
<td><span data-ttu-id="5c185-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="5c185-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5c185-460">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-460">10001</span></span></td>
<td><span data-ttu-id="5c185-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-461">Electricity</span></span></td>
<td><span data-ttu-id="5c185-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-462">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-463">10.00</span><span class="sxs-lookup"><span data-stu-id="5c185-463">10.00</span></span></td>
<td><span data-ttu-id="5c185-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="5c185-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5c185-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5c185-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5c185-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5c185-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="5c185-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5c185-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5c185-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5c185-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5c185-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="5c185-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5c185-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5c185-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5c185-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5c185-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5c185-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5c185-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-475">Define the cost allocation</span></span>

<span data-ttu-id="5c185-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5c185-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5c185-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5c185-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="5c185-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-479">Cost object</span></span></th>
<th><span data-ttu-id="5c185-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="5c185-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-481">CC002</span></span></td>
<td><span data-ttu-id="5c185-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-482">Finance</span></span></td>
<td><span data-ttu-id="5c185-483">35</span><span class="sxs-lookup"><span data-stu-id="5c185-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-484">CC003</span></span></td>
<td><span data-ttu-id="5c185-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-485">Assembly</span></span></td>
<td><span data-ttu-id="5c185-486">55</span><span class="sxs-lookup"><span data-stu-id="5c185-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-487">CC004</span></span></td>
<td><span data-ttu-id="5c185-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-488">Packaging</span></span></td>
<td><span data-ttu-id="5c185-489">10</span><span class="sxs-lookup"><span data-stu-id="5c185-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5c185-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5c185-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="5c185-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-492">Cost object</span></span></th>
<th><span data-ttu-id="5c185-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-494">CC003</span></span></td>
<td><span data-ttu-id="5c185-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-495">Assembly</span></span></td>
<td><span data-ttu-id="5c185-496">65</span><span class="sxs-lookup"><span data-stu-id="5c185-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-497">CC004</span></span></td>
<td><span data-ttu-id="5c185-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-498">Packaging</span></span></td>
<td><span data-ttu-id="5c185-499">35</span><span class="sxs-lookup"><span data-stu-id="5c185-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5c185-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5c185-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="5c185-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-502">Cost object</span></span></th>
<th><span data-ttu-id="5c185-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="5c185-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-504">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-505">Product 1</span></span></td>
<td><span data-ttu-id="5c185-506">60</span><span class="sxs-lookup"><span data-stu-id="5c185-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-507">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-508">Product 2</span></span></td>
<td><span data-ttu-id="5c185-509">20</span><span class="sxs-lookup"><span data-stu-id="5c185-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="5c185-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5c185-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="5c185-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-512">Cost object</span></span></th>
<th><span data-ttu-id="5c185-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="5c185-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-514">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-515">Product 1</span></span></td>
<td><span data-ttu-id="5c185-516">80</span><span class="sxs-lookup"><span data-stu-id="5c185-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-517">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-518">Product 2</span></span></td>
<td><span data-ttu-id="5c185-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="5c185-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5c185-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5c185-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5c185-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="5c185-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5c185-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="5c185-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-523">Cost object</span></span></th>
<th><span data-ttu-id="5c185-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-524">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-526">Amount</span></span></th>
<th><span data-ttu-id="5c185-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-528">CC002</span></span></td>
<td><span data-ttu-id="5c185-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-529">Finance</span></span></td>
<td><span data-ttu-id="5c185-530">35</span><span class="sxs-lookup"><span data-stu-id="5c185-530">35</span></span></td>
<td><span data-ttu-id="5c185-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5c185-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5c185-532">175.00</span></span></td>
<td><span data-ttu-id="5c185-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-534">CC003</span></span></td>
<td><span data-ttu-id="5c185-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-535">Assembly</span></span></td>
<td><span data-ttu-id="5c185-536">55</span><span class="sxs-lookup"><span data-stu-id="5c185-536">55</span></span></td>
<td><span data-ttu-id="5c185-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5c185-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5c185-538">275.00</span></span></td>
<td><span data-ttu-id="5c185-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-540">CC004</span></span></td>
<td><span data-ttu-id="5c185-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-541">Packaging</span></span></td>
<td><span data-ttu-id="5c185-542">10</span><span class="sxs-lookup"><span data-stu-id="5c185-542">10</span></span></td>
<td><span data-ttu-id="5c185-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5c185-544">50.00</span><span class="sxs-lookup"><span data-stu-id="5c185-544">50.00</span></span></td>
<td><span data-ttu-id="5c185-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-546">CC002</span></span></td>
<td><span data-ttu-id="5c185-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-547">Finance</span></span></td>
<td><span data-ttu-id="5c185-548">35</span><span class="sxs-lookup"><span data-stu-id="5c185-548">35</span></span></td>
<td><span data-ttu-id="5c185-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5c185-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5c185-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5c185-550">436.00</span></span></td>
<td><span data-ttu-id="5c185-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-552">CC003</span></span></td>
<td><span data-ttu-id="5c185-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-553">Assembly</span></span></td>
<td><span data-ttu-id="5c185-554">55</span><span class="sxs-lookup"><span data-stu-id="5c185-554">55</span></span></td>
<td><span data-ttu-id="5c185-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5c185-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5c185-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5c185-556">685.14</span></span></td>
<td><span data-ttu-id="5c185-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-558">CC004</span></span></td>
<td><span data-ttu-id="5c185-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-559">Packaging</span></span></td>
<td><span data-ttu-id="5c185-560">10</span><span class="sxs-lookup"><span data-stu-id="5c185-560">10</span></span></td>
<td><span data-ttu-id="5c185-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5c185-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5c185-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5c185-562">124.57</span></span></td>
<td><span data-ttu-id="5c185-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="5c185-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-565">Cost object</span></span></th>
<th><span data-ttu-id="5c185-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-566">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-568">Amount</span></span></th>
<th><span data-ttu-id="5c185-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-570">CC003</span></span></td>
<td><span data-ttu-id="5c185-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-571">Assembly</span></span></td>
<td><span data-ttu-id="5c185-572">65</span><span class="sxs-lookup"><span data-stu-id="5c185-572">65</span></span></td>
<td><span data-ttu-id="5c185-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5c185-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5c185-574">438.75</span></span></td>
<td><span data-ttu-id="5c185-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-576">CC004</span></span></td>
<td><span data-ttu-id="5c185-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-577">Packaging</span></span></td>
<td><span data-ttu-id="5c185-578">35</span><span class="sxs-lookup"><span data-stu-id="5c185-578">35</span></span></td>
<td><span data-ttu-id="5c185-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5c185-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5c185-580">236.25</span></span></td>
<td><span data-ttu-id="5c185-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-582">CC003</span></span></td>
<td><span data-ttu-id="5c185-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-583">Assembly</span></span></td>
<td><span data-ttu-id="5c185-584">65</span><span class="sxs-lookup"><span data-stu-id="5c185-584">65</span></span></td>
<td><span data-ttu-id="5c185-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5c185-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5c185-586">5,297.69</span></span></td>
<td><span data-ttu-id="5c185-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-588">CC004</span></span></td>
<td><span data-ttu-id="5c185-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-589">Packaging</span></span></td>
<td><span data-ttu-id="5c185-590">35</span><span class="sxs-lookup"><span data-stu-id="5c185-590">35</span></span></td>
<td><span data-ttu-id="5c185-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5c185-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5c185-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5c185-592">2,852.60</span></span></td>
<td><span data-ttu-id="5c185-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="5c185-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-595">Cost object</span></span></th>
<th><span data-ttu-id="5c185-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-596">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-598">Amount</span></span></th>
<th><span data-ttu-id="5c185-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-600">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-601">Product 1</span></span></td>
<td><span data-ttu-id="5c185-602">60</span><span class="sxs-lookup"><span data-stu-id="5c185-602">60</span></span></td>
<td><span data-ttu-id="5c185-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5c185-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5c185-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5c185-604">535.31</span></span></td>
<td><span data-ttu-id="5c185-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-606">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-607">Product 2</span></span></td>
<td><span data-ttu-id="5c185-608">20</span><span class="sxs-lookup"><span data-stu-id="5c185-608">20</span></span></td>
<td><span data-ttu-id="5c185-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5c185-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5c185-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5c185-610">178.44</span></span></td>
<td><span data-ttu-id="5c185-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-612">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-613">Product 1</span></span></td>
<td><span data-ttu-id="5c185-614">60</span><span class="sxs-lookup"><span data-stu-id="5c185-614">60</span></span></td>
<td><span data-ttu-id="5c185-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5c185-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5c185-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5c185-616">4,487.12</span></span></td>
<td><span data-ttu-id="5c185-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-618">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-619">Product 2</span></span></td>
<td><span data-ttu-id="5c185-620">20</span><span class="sxs-lookup"><span data-stu-id="5c185-620">20</span></span></td>
<td><span data-ttu-id="5c185-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5c185-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5c185-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5c185-622">1,495.71</span></span></td>
<td><span data-ttu-id="5c185-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c185-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="5c185-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-625">Cost object</span></span></th>
<th><span data-ttu-id="5c185-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="5c185-626">Magnitude</span></span></th>
<th><span data-ttu-id="5c185-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="5c185-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5c185-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-628">Amount</span></span></th>
<th><span data-ttu-id="5c185-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-630">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-631">Product 1</span></span></td>
<td><span data-ttu-id="5c185-632">80</span><span class="sxs-lookup"><span data-stu-id="5c185-632">80</span></span></td>
<td><span data-ttu-id="5c185-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5c185-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5c185-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5c185-634">241.05</span></span></td>
<td><span data-ttu-id="5c185-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-636">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-637">Product 2</span></span></td>
<td><span data-ttu-id="5c185-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="5c185-638">15</span></span></td>
<td><span data-ttu-id="5c185-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5c185-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5c185-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5c185-640">45.20</span></span></td>
<td><span data-ttu-id="5c185-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-642">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-643">Product 1</span></span></td>
<td><span data-ttu-id="5c185-644">80</span><span class="sxs-lookup"><span data-stu-id="5c185-644">80</span></span></td>
<td><span data-ttu-id="5c185-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5c185-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5c185-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5c185-646">2,507.09</span></span></td>
<td><span data-ttu-id="5c185-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-648">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-649">Product 2</span></span></td>
<td><span data-ttu-id="5c185-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="5c185-650">15</span></span></td>
<td><span data-ttu-id="5c185-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5c185-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5c185-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5c185-652">470.08</span></span></td>
<td><span data-ttu-id="5c185-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5c185-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="5c185-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-655">Journal</span></span></th>
<th><span data-ttu-id="5c185-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c185-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c185-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="5c185-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-659">00004</span><span class="sxs-lookup"><span data-stu-id="5c185-659">00004</span></span></td>
<td><span data-ttu-id="5c185-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5c185-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-661">Fiscal</span></span></td>
<td><span data-ttu-id="5c185-662">2017</span><span class="sxs-lookup"><span data-stu-id="5c185-662">2017</span></span></td>
<td><span data-ttu-id="5c185-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-663">Period 1</span></span></td>
<td><span data-ttu-id="5c185-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="5c185-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5c185-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c185-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c185-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-668">Cost element</span></span></th>
<th><span data-ttu-id="5c185-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-672">CC001</span></span></td>
<td><span data-ttu-id="5c185-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-673">HR</span></span></td>
<td><span data-ttu-id="5c185-674">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-674">10001</span></span></td>
<td><span data-ttu-id="5c185-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-675">Electricity</span></span></td>
<td><span data-ttu-id="5c185-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-677">500.00</span><span class="sxs-lookup"><span data-stu-id="5c185-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-679">CC001</span></span></td>
<td><span data-ttu-id="5c185-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-680">HR</span></span></td>
<td><span data-ttu-id="5c185-681">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-681">10001</span></span></td>
<td><span data-ttu-id="5c185-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-682">Electricity</span></span></td>
<td><span data-ttu-id="5c185-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-683">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5c185-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-686">CC002</span></span></td>
<td><span data-ttu-id="5c185-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-687">Finance</span></span></td>
<td><span data-ttu-id="5c185-688">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-688">10001</span></span></td>
<td><span data-ttu-id="5c185-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-689">Electricity</span></span></td>
<td><span data-ttu-id="5c185-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5c185-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-693">CC002</span></span></td>
<td><span data-ttu-id="5c185-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-694">Finance</span></span></td>
<td><span data-ttu-id="5c185-695">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-695">10001</span></span></td>
<td><span data-ttu-id="5c185-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-696">Electricity</span></span></td>
<td><span data-ttu-id="5c185-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-697">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5c185-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-700">CC003</span></span></td>
<td><span data-ttu-id="5c185-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-701">Assembly</span></span></td>
<td><span data-ttu-id="5c185-702">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-702">10001</span></span></td>
<td><span data-ttu-id="5c185-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-703">Electricity</span></span></td>
<td><span data-ttu-id="5c185-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5c185-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-707">CC003</span></span></td>
<td><span data-ttu-id="5c185-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-708">Assembly</span></span></td>
<td><span data-ttu-id="5c185-709">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-709">10001</span></span></td>
<td><span data-ttu-id="5c185-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-710">Electricity</span></span></td>
<td><span data-ttu-id="5c185-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-711">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5c185-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-714">CC003</span></span></td>
<td><span data-ttu-id="5c185-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-715">Packaging</span></span></td>
<td><span data-ttu-id="5c185-716">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-716">10001</span></span></td>
<td><span data-ttu-id="5c185-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-717">Electricity</span></span></td>
<td><span data-ttu-id="5c185-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5c185-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-721">CC003</span></span></td>
<td><span data-ttu-id="5c185-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-722">Packaging</span></span></td>
<td><span data-ttu-id="5c185-723">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-723">10001</span></span></td>
<td><span data-ttu-id="5c185-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-724">Electricity</span></span></td>
<td><span data-ttu-id="5c185-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-725">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5c185-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-728">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-729">Product 1</span></span></td>
<td><span data-ttu-id="5c185-730">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-730">10001</span></span></td>
<td><span data-ttu-id="5c185-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-731">Electricity</span></span></td>
<td><span data-ttu-id="5c185-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5c185-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-735">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-736">Product 1</span></span></td>
<td><span data-ttu-id="5c185-737">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-737">10001</span></span></td>
<td><span data-ttu-id="5c185-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-738">Electricity</span></span></td>
<td><span data-ttu-id="5c185-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-739">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5c185-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-742">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-743">Product 1</span></span></td>
<td><span data-ttu-id="5c185-744">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-744">10001</span></span></td>
<td><span data-ttu-id="5c185-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-745">Electricity</span></span></td>
<td><span data-ttu-id="5c185-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5c185-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c185-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-749">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-750">Product 1</span></span></td>
<td><span data-ttu-id="5c185-751">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-751">10001</span></span></td>
<td><span data-ttu-id="5c185-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-752">Electricity</span></span></td>
<td><span data-ttu-id="5c185-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-753">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5c185-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c185-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c185-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c185-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-757">Cost element</span></span></th>
<th><span data-ttu-id="5c185-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5c185-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-759">Amount</span></span></th>
<th><span data-ttu-id="5c185-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c185-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c185-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-761">CC001</span></span></td>
<td><span data-ttu-id="5c185-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-762">HR</span></span></td>
<td><span data-ttu-id="5c185-763">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-763">10001</span></span></td>
<td><span data-ttu-id="5c185-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-764">Electricity</span></span></td>
<td><span data-ttu-id="5c185-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="5c185-766">-500.00</span></span></td>
<td><span data-ttu-id="5c185-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-768">CC002</span></span></td>
<td><span data-ttu-id="5c185-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-769">Finance</span></span></td>
<td><span data-ttu-id="5c185-770">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-770">10001</span></span></td>
<td><span data-ttu-id="5c185-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-771">Electricity</span></span></td>
<td><span data-ttu-id="5c185-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5c185-773">175.00</span></span></td>
<td><span data-ttu-id="5c185-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-775">CC003</span></span></td>
<td><span data-ttu-id="5c185-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-776">Assembly</span></span></td>
<td><span data-ttu-id="5c185-777">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-777">10001</span></span></td>
<td><span data-ttu-id="5c185-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-778">Electricity</span></span></td>
<td><span data-ttu-id="5c185-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5c185-780">275.00</span></span></td>
<td><span data-ttu-id="5c185-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-782">CC004</span></span></td>
<td><span data-ttu-id="5c185-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-783">Packaging</span></span></td>
<td><span data-ttu-id="5c185-784">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-784">10001</span></span></td>
<td><span data-ttu-id="5c185-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-785">Electricity</span></span></td>
<td><span data-ttu-id="5c185-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5c185-787">50,00</span></span></td>
<td><span data-ttu-id="5c185-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-789">CC001</span></span></td>
<td><span data-ttu-id="5c185-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5c185-790">HR</span></span></td>
<td><span data-ttu-id="5c185-791">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-791">10001</span></span></td>
<td><span data-ttu-id="5c185-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-792">Electricity</span></span></td>
<td><span data-ttu-id="5c185-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-793">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="5c185-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5c185-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-796">CC002</span></span></td>
<td><span data-ttu-id="5c185-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-797">Finance</span></span></td>
<td><span data-ttu-id="5c185-798">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-798">10001</span></span></td>
<td><span data-ttu-id="5c185-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-799">Electricity</span></span></td>
<td><span data-ttu-id="5c185-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-800">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5c185-801">436.00</span></span></td>
<td><span data-ttu-id="5c185-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-803">CC003</span></span></td>
<td><span data-ttu-id="5c185-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-804">Assembly</span></span></td>
<td><span data-ttu-id="5c185-805">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-805">10001</span></span></td>
<td><span data-ttu-id="5c185-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-806">Electricity</span></span></td>
<td><span data-ttu-id="5c185-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-807">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5c185-808">685.14</span></span></td>
<td><span data-ttu-id="5c185-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-810">CC004</span></span></td>
<td><span data-ttu-id="5c185-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-811">Packaging</span></span></td>
<td><span data-ttu-id="5c185-812">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-812">10001</span></span></td>
<td><span data-ttu-id="5c185-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-813">Electricity</span></span></td>
<td><span data-ttu-id="5c185-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-814">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5c185-815">124.57</span></span></td>
<td><span data-ttu-id="5c185-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-817">CC002</span></span></td>
<td><span data-ttu-id="5c185-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-818">Finance</span></span></td>
<td><span data-ttu-id="5c185-819">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-819">10001</span></span></td>
<td><span data-ttu-id="5c185-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-820">Electricity</span></span></td>
<td><span data-ttu-id="5c185-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="5c185-822">-675.00</span></span></td>
<td><span data-ttu-id="5c185-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-824">CC003</span></span></td>
<td><span data-ttu-id="5c185-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-825">Assembly</span></span></td>
<td><span data-ttu-id="5c185-826">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-826">10001</span></span></td>
<td><span data-ttu-id="5c185-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-827">Electricity</span></span></td>
<td><span data-ttu-id="5c185-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5c185-829">438.75</span></span></td>
<td><span data-ttu-id="5c185-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-831">CC004</span></span></td>
<td><span data-ttu-id="5c185-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-832">Packaging</span></span></td>
<td><span data-ttu-id="5c185-833">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-833">10001</span></span></td>
<td><span data-ttu-id="5c185-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-834">Electricity</span></span></td>
<td><span data-ttu-id="5c185-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5c185-836">236.25</span></span></td>
<td><span data-ttu-id="5c185-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-838">CC002</span></span></td>
<td><span data-ttu-id="5c185-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="5c185-839">Finance</span></span></td>
<td><span data-ttu-id="5c185-840">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-840">10001</span></span></td>
<td><span data-ttu-id="5c185-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-841">Electricity</span></span></td>
<td><span data-ttu-id="5c185-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-842">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="5c185-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5c185-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-845">CC003</span></span></td>
<td><span data-ttu-id="5c185-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-846">Assembly</span></span></td>
<td><span data-ttu-id="5c185-847">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-847">10001</span></span></td>
<td><span data-ttu-id="5c185-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-848">Electricity</span></span></td>
<td><span data-ttu-id="5c185-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-849">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5c185-850">5,297.69</span></span></td>
<td><span data-ttu-id="5c185-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-852">CC004</span></span></td>
<td><span data-ttu-id="5c185-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5c185-853">Packaging</span></span></td>
<td><span data-ttu-id="5c185-854">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-854">10001</span></span></td>
<td><span data-ttu-id="5c185-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-855">Electricity</span></span></td>
<td><span data-ttu-id="5c185-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-856">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5c185-857">2,852.60</span></span></td>
<td><span data-ttu-id="5c185-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-859">CC003</span></span></td>
<td><span data-ttu-id="5c185-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-860">Assembly</span></span></td>
<td><span data-ttu-id="5c185-861">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-861">10001</span></span></td>
<td><span data-ttu-id="5c185-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-862">Electricity</span></span></td>
<td><span data-ttu-id="5c185-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="5c185-864">-713.75</span></span></td>
<td><span data-ttu-id="5c185-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-866">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-867">Product 1</span></span></td>
<td><span data-ttu-id="5c185-868">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-868">10001</span></span></td>
<td><span data-ttu-id="5c185-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-869">Electricity</span></span></td>
<td><span data-ttu-id="5c185-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5c185-871">535.31</span></span></td>
<td><span data-ttu-id="5c185-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-873">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-874">Product 2</span></span></td>
<td><span data-ttu-id="5c185-875">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-875">10001</span></span></td>
<td><span data-ttu-id="5c185-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-876">Electricity</span></span></td>
<td><span data-ttu-id="5c185-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5c185-878">178.44</span></span></td>
<td><span data-ttu-id="5c185-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-880">CC003</span></span></td>
<td><span data-ttu-id="5c185-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-881">Assembly</span></span></td>
<td><span data-ttu-id="5c185-882">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-882">10001</span></span></td>
<td><span data-ttu-id="5c185-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-883">Electricity</span></span></td>
<td><span data-ttu-id="5c185-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-884">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="5c185-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5c185-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-887">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-888">Product 1</span></span></td>
<td><span data-ttu-id="5c185-889">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-889">10001</span></span></td>
<td><span data-ttu-id="5c185-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-890">Electricity</span></span></td>
<td><span data-ttu-id="5c185-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-891">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5c185-892">4,487.12</span></span></td>
<td><span data-ttu-id="5c185-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-894">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-895">Product 2</span></span></td>
<td><span data-ttu-id="5c185-896">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-896">10001</span></span></td>
<td><span data-ttu-id="5c185-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-897">Electricity</span></span></td>
<td><span data-ttu-id="5c185-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-898">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5c185-899">1,495.71</span></span></td>
<td><span data-ttu-id="5c185-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-901">CC003</span></span></td>
<td><span data-ttu-id="5c185-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-902">Assembly</span></span></td>
<td><span data-ttu-id="5c185-903">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-903">10001</span></span></td>
<td><span data-ttu-id="5c185-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-904">Electricity</span></span></td>
<td><span data-ttu-id="5c185-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="5c185-906">-286.25</span></span></td>
<td><span data-ttu-id="5c185-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-908">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-909">Product 1</span></span></td>
<td><span data-ttu-id="5c185-910">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-910">10001</span></span></td>
<td><span data-ttu-id="5c185-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-911">Electricity</span></span></td>
<td><span data-ttu-id="5c185-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5c185-913">241.05</span></span></td>
<td><span data-ttu-id="5c185-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-915">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-916">Product 2</span></span></td>
<td><span data-ttu-id="5c185-917">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-917">10001</span></span></td>
<td><span data-ttu-id="5c185-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-918">Electricity</span></span></td>
<td><span data-ttu-id="5c185-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5c185-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5c185-920">45.20</span></span></td>
<td><span data-ttu-id="5c185-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-922">CC003</span></span></td>
<td><span data-ttu-id="5c185-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="5c185-923">Assembly</span></span></td>
<td><span data-ttu-id="5c185-924">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-924">10001</span></span></td>
<td><span data-ttu-id="5c185-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-925">Electricity</span></span></td>
<td><span data-ttu-id="5c185-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-926">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="5c185-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5c185-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-929">Prod 1</span></span></td>
<td><span data-ttu-id="5c185-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-930">Product 1</span></span></td>
<td><span data-ttu-id="5c185-931">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-931">10001</span></span></td>
<td><span data-ttu-id="5c185-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-932">Electricity</span></span></td>
<td><span data-ttu-id="5c185-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-933">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5c185-934">2,507.09</span></span></td>
<td><span data-ttu-id="5c185-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c185-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-936">Prod 2</span></span></td>
<td><span data-ttu-id="5c185-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-937">Product 2</span></span></td>
<td><span data-ttu-id="5c185-938">10001</span><span class="sxs-lookup"><span data-stu-id="5c185-938">10001</span></span></td>
<td><span data-ttu-id="5c185-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-939">Electricity</span></span></td>
<td><span data-ttu-id="5c185-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-940">Variable cost</span></span></td>
<td><span data-ttu-id="5c185-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5c185-941">470.08</span></span></td>
<td><span data-ttu-id="5c185-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="5c185-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5c185-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="5c185-943">Conclusion</span></span>
<span data-ttu-id="5c185-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="5c185-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5c185-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="5c185-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5c185-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="5c185-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5c185-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5c185-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5c185-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5c185-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="5c185-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5c185-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5c185-951">CC099</span></span></th>
<th><span data-ttu-id="5c185-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5c185-952">CC001</span></span></th>
<th><span data-ttu-id="5c185-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5c185-953">CC002</span></span></th>
<th><span data-ttu-id="5c185-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5c185-954">CC003</span></span></th>
<th><span data-ttu-id="5c185-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5c185-955">CC004</span></span></th>
<th><span data-ttu-id="5c185-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-956">Proj 1</span></span></th>
<th><span data-ttu-id="5c185-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-957">Proj 2</span></span></th>
<th><span data-ttu-id="5c185-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="5c185-958">Prod 1</span></span></th>
<th><span data-ttu-id="5c185-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="5c185-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5c185-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="5c185-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5c185-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5c185-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="5c185-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-971">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5c185-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="5c185-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-973">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-974">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-975">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-976">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-977">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5c185-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5c185-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5c185-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5c185-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5c185-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-982">000</span><span class="sxs-lookup"><span data-stu-id="5c185-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-983">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-984">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-985">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-986">0.00</span><span class="sxs-lookup"><span data-stu-id="5c185-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-987">30.00</span><span class="sxs-lookup"><span data-stu-id="5c185-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-988">10.00</span><span class="sxs-lookup"><span data-stu-id="5c185-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5c185-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5c185-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c185-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c185-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5c185-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5c185-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="5c185-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5c185-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5c185-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="5c185-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5c185-996">สำหรับข้อมูลเพิ่มเติม ดู [นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="5c185-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



