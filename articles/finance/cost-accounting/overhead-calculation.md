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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759483"
---
# <a name="overhead-calculation"></a><span data-ttu-id="c0b5e-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0b5e-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c0b5e-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-105">Term definition</span></span>
---------------

<span data-ttu-id="c0b5e-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="c0b5e-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c0b5e-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c0b5e-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="c0b5e-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c0b5e-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-109">Rent</span></span>
-   <span data-ttu-id="c0b5e-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-110">Electricity</span></span>
-   <span data-ttu-id="c0b5e-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c0b5e-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-112">Overhead calculation overview</span></span>
<span data-ttu-id="c0b5e-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c0b5e-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c0b5e-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c0b5e-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c0b5e-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c0b5e-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c0b5e-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c0b5e-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c0b5e-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-119">Version type</span></span>
-   <span data-ttu-id="c0b5e-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c0b5e-120">Date and time</span></span>
-   <span data-ttu-id="c0b5e-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c0b5e-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-122">Fiscal year</span></span>
-   <span data-ttu-id="c0b5e-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-123">Fiscal period</span></span>

<span data-ttu-id="c0b5e-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c0b5e-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="c0b5e-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c0b5e-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c0b5e-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c0b5e-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c0b5e-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c0b5e-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c0b5e-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c0b5e-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c0b5e-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c0b5e-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c0b5e-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c0b5e-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c0b5e-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="c0b5e-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c0b5e-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c0b5e-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c0b5e-140">Main account</span></span></th>
<th><span data-ttu-id="c0b5e-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-143">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-144">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-145">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-145">10001</span></span></td>
<td><span data-ttu-id="c0b5e-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-146">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c0b5e-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c0b5e-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c0b5e-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="c0b5e-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c0b5e-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c0b5e-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c0b5e-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="c0b5e-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c0b5e-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c0b5e-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="c0b5e-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c0b5e-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c0b5e-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c0b5e-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c0b5e-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-160">Journal</span></span></th>
<th><span data-ttu-id="c0b5e-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0b5e-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0b5e-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-164">00001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-164">00001</span></span></td>
<td><span data-ttu-id="c0b5e-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c0b5e-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-166">Fiscal</span></span></td>
<td><span data-ttu-id="c0b5e-167">2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-167">2017</span></span></td>
<td><span data-ttu-id="c0b5e-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-168">Period 1</span></span></td>
<td><span data-ttu-id="c0b5e-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0b5e-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-173">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-177">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-178">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-179">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-179">10001</span></span></td>
<td><span data-ttu-id="c0b5e-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-180">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c0b5e-181">Unclassified</span></span></td>
<td><span data-ttu-id="c0b5e-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0b5e-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-185">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-187">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-189">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-190">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-191">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-191">10001</span></span></td>
<td><span data-ttu-id="c0b5e-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-192">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c0b5e-193">Unclassified</span></span></td>
<td><span data-ttu-id="c0b5e-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-194">10,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-196">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-197">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-198">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-198">10001</span></span></td>
<td><span data-ttu-id="c0b5e-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-199">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c0b5e-200">Unclassified</span></span></td>
<td><span data-ttu-id="c0b5e-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-203">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-204">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-205">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-205">10001</span></span></td>
<td><span data-ttu-id="c0b5e-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-206">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-208">1,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-210">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-211">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-212">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-212">10001</span></span></td>
<td><span data-ttu-id="c0b5e-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-213">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-214">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-215">9,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c0b5e-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c0b5e-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c0b5e-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c0b5e-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c0b5e-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c0b5e-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c0b5e-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c0b5e-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c0b5e-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c0b5e-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c0b5e-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-228">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="c0b5e-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-230">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-231">HR</span></span></td>
<td><span data-ttu-id="c0b5e-232">1,000</span><span class="sxs-lookup"><span data-stu-id="c0b5e-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-233">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-234">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-235">6,000</span><span class="sxs-lookup"><span data-stu-id="c0b5e-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-236">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-237">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-238">0</span><span class="sxs-lookup"><span data-stu-id="c0b5e-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-240">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-241">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-244">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-245">HR</span></span></td>
<td><span data-ttu-id="c0b5e-246">1,000</span><span class="sxs-lookup"><span data-stu-id="c0b5e-246">1,000</span></span></td>
<td><span data-ttu-id="c0b5e-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-249">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-250">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-251">6,000</span><span class="sxs-lookup"><span data-stu-id="c0b5e-251">6,000</span></span></td>
<td><span data-ttu-id="c0b5e-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c0b5e-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-254">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-255">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-256">0</span><span class="sxs-lookup"><span data-stu-id="c0b5e-256">0</span></span></td>
<td><span data-ttu-id="c0b5e-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-258">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c0b5e-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-261">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-262">Formula</span></span></th>
<th><span data-ttu-id="c0b5e-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-263">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-266">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-267">HR</span></span></td>
<td><span data-ttu-id="c0b5e-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0b5e-269">1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-269">1</span></span></td>
<td><span data-ttu-id="c0b5e-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-271">500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-272">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-273">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0b5e-275">1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-275">1</span></span></td>
<td><span data-ttu-id="c0b5e-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-277">500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-278">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-279">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c0b5e-281">0</span><span class="sxs-lookup"><span data-stu-id="c0b5e-281">0</span></span></td>
<td><span data-ttu-id="c0b5e-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-283">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c0b5e-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-285">Journal</span></span></th>
<th><span data-ttu-id="c0b5e-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0b5e-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0b5e-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-289">00002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-289">00002</span></span></td>
<td><span data-ttu-id="c0b5e-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c0b5e-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-291">Fiscal</span></span></td>
<td><span data-ttu-id="c0b5e-292">2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-292">2017</span></span></td>
<td><span data-ttu-id="c0b5e-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-293">Period 1</span></span></td>
<td><span data-ttu-id="c0b5e-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0b5e-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-298">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-302">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-303">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-304">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-304">10001</span></span></td>
<td><span data-ttu-id="c0b5e-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-305">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-309">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-310">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-311">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-311">10001</span></span></td>
<td><span data-ttu-id="c0b5e-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-312">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-313">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0b5e-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-317">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-319">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-321">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-322">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-323">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-323">10001</span></span></td>
<td><span data-ttu-id="c0b5e-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-324">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="c0b5e-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-328">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-329">HR</span></span></td>
<td><span data-ttu-id="c0b5e-330">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-330">10001</span></span></td>
<td><span data-ttu-id="c0b5e-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-331">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-333">500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-333">500.00</span></span></td>
<td><span data-ttu-id="c0b5e-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-335">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-336">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-337">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-337">10001</span></span></td>
<td><span data-ttu-id="c0b5e-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-338">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-340">500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-340">500.00</span></span></td>
<td><span data-ttu-id="c0b5e-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-342">CC099</span></span></td>
<td><span data-ttu-id="c0b5e-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0b5e-343">Default cost center</span></span></td>
<td><span data-ttu-id="c0b5e-344">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-344">10001</span></span></td>
<td><span data-ttu-id="c0b5e-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-345">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-346">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c0b5e-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-349">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-350">HR</span></span></td>
<td><span data-ttu-id="c0b5e-351">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-351">10001</span></span></td>
<td><span data-ttu-id="c0b5e-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-352">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-353">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-354">1,285.71</span></span></td>
<td><span data-ttu-id="c0b5e-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-356">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-357">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-358">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-358">10001</span></span></td>
<td><span data-ttu-id="c0b5e-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-359">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-360">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c0b5e-361">7,714.29</span></span></td>
<td><span data-ttu-id="c0b5e-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c0b5e-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c0b5e-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c0b5e-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c0b5e-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-367">Define the overhead rate</span></span>

<span data-ttu-id="c0b5e-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c0b5e-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0b5e-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-370">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c0b5e-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-372">Proj 1</span></span></td>
<td><span data-ttu-id="c0b5e-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-373">Project 1</span></span></td>
<td><span data-ttu-id="c0b5e-374">3</span><span class="sxs-lookup"><span data-stu-id="c0b5e-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-375">Proj 2</span></span></td>
<td><span data-ttu-id="c0b5e-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-376">Project 2</span></span></td>
<td><span data-ttu-id="c0b5e-377">1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-379">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-380">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-382">Units</span></span></th>
<th><span data-ttu-id="c0b5e-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="c0b5e-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-384">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-385">HR</span></span></td>
<td><span data-ttu-id="c0b5e-386">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-386">10001</span></span></td>
<td><span data-ttu-id="c0b5e-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-387">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-388">1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-388">1</span></span></td>
<td><span data-ttu-id="c0b5e-389">10</span><span class="sxs-lookup"><span data-stu-id="c0b5e-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-391">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-392">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-393">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-396">Proj 1</span></span></td>
<td><span data-ttu-id="c0b5e-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-397">Project 1</span></span></td>
<td><span data-ttu-id="c0b5e-398">3</span><span class="sxs-lookup"><span data-stu-id="c0b5e-398">3</span></span></td>
<td><span data-ttu-id="c0b5e-399">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-399">10001</span></span></td>
<td><span data-ttu-id="c0b5e-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c0b5e-401">30.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-402">Proj 2</span></span></td>
<td><span data-ttu-id="c0b5e-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-403">Project 2</span></span></td>
<td><span data-ttu-id="c0b5e-404">1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-404">1</span></span></td>
<td><span data-ttu-id="c0b5e-405">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-405">10001</span></span></td>
<td><span data-ttu-id="c0b5e-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c0b5e-407">10.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c0b5e-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-409">Journal</span></span></th>
<th><span data-ttu-id="c0b5e-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0b5e-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0b5e-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-413">00003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-413">00003</span></span></td>
<td><span data-ttu-id="c0b5e-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c0b5e-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c0b5e-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-415">Fiscal</span></span></td>
<td><span data-ttu-id="c0b5e-416">2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-416">2017</span></span></td>
<td><span data-ttu-id="c0b5e-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-417">Period 1</span></span></td>
<td><span data-ttu-id="c0b5e-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c0b5e-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-421">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-424">Proj 1</span></span></td>
<td><span data-ttu-id="c0b5e-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c0b5e-426">3.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-428">Proj 2</span></span></td>
<td><span data-ttu-id="c0b5e-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c0b5e-430">1.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0b5e-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-433">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-435">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-437">CC0001</span></span></td>
<td><span data-ttu-id="c0b5e-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-438">HR</span></span></td>
<td><span data-ttu-id="c0b5e-439">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-439">10001</span></span></td>
<td><span data-ttu-id="c0b5e-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-440">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-441">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-442">-30.00</span></span></td>
<td><span data-ttu-id="c0b5e-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-444">Proj 1</span></span></td>
<td><span data-ttu-id="c0b5e-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c0b5e-446">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-446">10001</span></span></td>
<td><span data-ttu-id="c0b5e-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-447">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-448">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-449">30.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-449">30.00</span></span></td>
<td><span data-ttu-id="c0b5e-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-451">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-452">HR</span></span></td>
<td><span data-ttu-id="c0b5e-453">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-453">10001</span></span></td>
<td><span data-ttu-id="c0b5e-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-454">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-455">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-456">-10.00</span></span></td>
<td><span data-ttu-id="c0b5e-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-458">Proj 2</span></span></td>
<td><span data-ttu-id="c0b5e-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c0b5e-460">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-460">10001</span></span></td>
<td><span data-ttu-id="c0b5e-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-461">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-462">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-463">10.00</span></span></td>
<td><span data-ttu-id="c0b5e-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c0b5e-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c0b5e-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c0b5e-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="c0b5e-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c0b5e-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c0b5e-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="c0b5e-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c0b5e-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c0b5e-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c0b5e-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c0b5e-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-475">Define the cost allocation</span></span>

<span data-ttu-id="c0b5e-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c0b5e-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c0b5e-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0b5e-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-479">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="c0b5e-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-481">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-482">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-483">35</span><span class="sxs-lookup"><span data-stu-id="c0b5e-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-484">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-485">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-486">55</span><span class="sxs-lookup"><span data-stu-id="c0b5e-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-487">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-488">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-489">10</span><span class="sxs-lookup"><span data-stu-id="c0b5e-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c0b5e-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0b5e-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-492">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-494">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-495">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-496">65</span><span class="sxs-lookup"><span data-stu-id="c0b5e-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-497">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-498">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-499">35</span><span class="sxs-lookup"><span data-stu-id="c0b5e-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c0b5e-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0b5e-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-502">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-504">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-505">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-506">60</span><span class="sxs-lookup"><span data-stu-id="c0b5e-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-507">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-508">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-509">20</span><span class="sxs-lookup"><span data-stu-id="c0b5e-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c0b5e-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0b5e-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-512">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-514">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-515">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-516">80</span><span class="sxs-lookup"><span data-stu-id="c0b5e-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-517">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-518">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="c0b5e-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0b5e-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c0b5e-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c0b5e-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-523">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-524">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-526">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-528">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-529">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-530">35</span><span class="sxs-lookup"><span data-stu-id="c0b5e-530">35</span></span></td>
<td><span data-ttu-id="c0b5e-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0b5e-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-532">175.00</span></span></td>
<td><span data-ttu-id="c0b5e-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-534">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-535">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-536">55</span><span class="sxs-lookup"><span data-stu-id="c0b5e-536">55</span></span></td>
<td><span data-ttu-id="c0b5e-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0b5e-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-538">275.00</span></span></td>
<td><span data-ttu-id="c0b5e-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-540">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-541">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-542">10</span><span class="sxs-lookup"><span data-stu-id="c0b5e-542">10</span></span></td>
<td><span data-ttu-id="c0b5e-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c0b5e-544">50.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-544">50.00</span></span></td>
<td><span data-ttu-id="c0b5e-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-546">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-547">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-548">35</span><span class="sxs-lookup"><span data-stu-id="c0b5e-548">35</span></span></td>
<td><span data-ttu-id="c0b5e-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0b5e-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-550">436.00</span></span></td>
<td><span data-ttu-id="c0b5e-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-552">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-553">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-554">55</span><span class="sxs-lookup"><span data-stu-id="c0b5e-554">55</span></span></td>
<td><span data-ttu-id="c0b5e-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0b5e-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c0b5e-556">685.14</span></span></td>
<td><span data-ttu-id="c0b5e-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-558">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-559">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-560">10</span><span class="sxs-lookup"><span data-stu-id="c0b5e-560">10</span></span></td>
<td><span data-ttu-id="c0b5e-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c0b5e-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c0b5e-562">124.57</span></span></td>
<td><span data-ttu-id="c0b5e-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-565">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-566">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-568">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-570">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-571">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-572">65</span><span class="sxs-lookup"><span data-stu-id="c0b5e-572">65</span></span></td>
<td><span data-ttu-id="c0b5e-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c0b5e-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c0b5e-574">438.75</span></span></td>
<td><span data-ttu-id="c0b5e-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-576">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-577">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-578">35</span><span class="sxs-lookup"><span data-stu-id="c0b5e-578">35</span></span></td>
<td><span data-ttu-id="c0b5e-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c0b5e-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c0b5e-580">236.25</span></span></td>
<td><span data-ttu-id="c0b5e-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-582">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-583">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-584">65</span><span class="sxs-lookup"><span data-stu-id="c0b5e-584">65</span></span></td>
<td><span data-ttu-id="c0b5e-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c0b5e-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c0b5e-586">5,297.69</span></span></td>
<td><span data-ttu-id="c0b5e-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-588">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-589">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-590">35</span><span class="sxs-lookup"><span data-stu-id="c0b5e-590">35</span></span></td>
<td><span data-ttu-id="c0b5e-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c0b5e-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c0b5e-592">2,852.60</span></span></td>
<td><span data-ttu-id="c0b5e-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-595">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-596">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-598">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-600">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-601">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-602">60</span><span class="sxs-lookup"><span data-stu-id="c0b5e-602">60</span></span></td>
<td><span data-ttu-id="c0b5e-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c0b5e-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c0b5e-604">535.31</span></span></td>
<td><span data-ttu-id="c0b5e-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-606">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-607">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-608">20</span><span class="sxs-lookup"><span data-stu-id="c0b5e-608">20</span></span></td>
<td><span data-ttu-id="c0b5e-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c0b5e-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c0b5e-610">178.44</span></span></td>
<td><span data-ttu-id="c0b5e-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-612">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-613">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-614">60</span><span class="sxs-lookup"><span data-stu-id="c0b5e-614">60</span></span></td>
<td><span data-ttu-id="c0b5e-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c0b5e-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c0b5e-616">4,487.12</span></span></td>
<td><span data-ttu-id="c0b5e-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-618">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-619">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-620">20</span><span class="sxs-lookup"><span data-stu-id="c0b5e-620">20</span></span></td>
<td><span data-ttu-id="c0b5e-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c0b5e-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-622">1,495.71</span></span></td>
<td><span data-ttu-id="c0b5e-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c0b5e-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-625">Cost object</span></span></th>
<th><span data-ttu-id="c0b5e-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c0b5e-626">Magnitude</span></span></th>
<th><span data-ttu-id="c0b5e-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c0b5e-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-628">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-630">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-631">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-632">80</span><span class="sxs-lookup"><span data-stu-id="c0b5e-632">80</span></span></td>
<td><span data-ttu-id="c0b5e-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c0b5e-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c0b5e-634">241.05</span></span></td>
<td><span data-ttu-id="c0b5e-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-636">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-637">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="c0b5e-638">15</span></span></td>
<td><span data-ttu-id="c0b5e-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c0b5e-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c0b5e-640">45.20</span></span></td>
<td><span data-ttu-id="c0b5e-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-642">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-643">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-644">80</span><span class="sxs-lookup"><span data-stu-id="c0b5e-644">80</span></span></td>
<td><span data-ttu-id="c0b5e-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c0b5e-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c0b5e-646">2,507.09</span></span></td>
<td><span data-ttu-id="c0b5e-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-648">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-649">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="c0b5e-650">15</span></span></td>
<td><span data-ttu-id="c0b5e-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c0b5e-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c0b5e-652">470.08</span></span></td>
<td><span data-ttu-id="c0b5e-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c0b5e-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-655">Journal</span></span></th>
<th><span data-ttu-id="c0b5e-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c0b5e-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c0b5e-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-659">00004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-659">00004</span></span></td>
<td><span data-ttu-id="c0b5e-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c0b5e-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-661">Fiscal</span></span></td>
<td><span data-ttu-id="c0b5e-662">2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-662">2017</span></span></td>
<td><span data-ttu-id="c0b5e-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-663">Period 1</span></span></td>
<td><span data-ttu-id="c0b5e-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c0b5e-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c0b5e-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-668">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-672">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-673">HR</span></span></td>
<td><span data-ttu-id="c0b5e-674">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-674">10001</span></span></td>
<td><span data-ttu-id="c0b5e-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-675">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-677">500.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-679">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-680">HR</span></span></td>
<td><span data-ttu-id="c0b5e-681">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-681">10001</span></span></td>
<td><span data-ttu-id="c0b5e-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-682">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-683">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-686">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-687">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-688">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-688">10001</span></span></td>
<td><span data-ttu-id="c0b5e-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-689">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-693">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-694">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-695">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-695">10001</span></span></td>
<td><span data-ttu-id="c0b5e-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-696">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-697">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c0b5e-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-700">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-701">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-702">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-702">10001</span></span></td>
<td><span data-ttu-id="c0b5e-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-703">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c0b5e-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-707">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-708">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-709">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-709">10001</span></span></td>
<td><span data-ttu-id="c0b5e-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-710">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-711">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c0b5e-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-714">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-715">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-716">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-716">10001</span></span></td>
<td><span data-ttu-id="c0b5e-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-717">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c0b5e-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-721">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-722">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-723">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-723">10001</span></span></td>
<td><span data-ttu-id="c0b5e-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-724">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-725">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c0b5e-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-728">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-729">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-730">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-730">10001</span></span></td>
<td><span data-ttu-id="c0b5e-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-731">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c0b5e-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-735">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-736">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-737">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-737">10001</span></span></td>
<td><span data-ttu-id="c0b5e-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-738">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-739">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c0b5e-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-742">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-743">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-744">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-744">10001</span></span></td>
<td><span data-ttu-id="c0b5e-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-745">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c0b5e-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c0b5e-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-749">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-750">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-751">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-751">10001</span></span></td>
<td><span data-ttu-id="c0b5e-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-752">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-753">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c0b5e-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c0b5e-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c0b5e-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c0b5e-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-757">Cost element</span></span></th>
<th><span data-ttu-id="c0b5e-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c0b5e-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-759">Amount</span></span></th>
<th><span data-ttu-id="c0b5e-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c0b5e-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-761">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-762">HR</span></span></td>
<td><span data-ttu-id="c0b5e-763">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-763">10001</span></span></td>
<td><span data-ttu-id="c0b5e-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-764">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="c0b5e-766">-500.00</span></span></td>
<td><span data-ttu-id="c0b5e-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-768">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-769">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-770">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-770">10001</span></span></td>
<td><span data-ttu-id="c0b5e-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-771">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-773">175.00</span></span></td>
<td><span data-ttu-id="c0b5e-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-775">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-776">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-777">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-777">10001</span></span></td>
<td><span data-ttu-id="c0b5e-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-778">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-780">275.00</span></span></td>
<td><span data-ttu-id="c0b5e-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-782">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-783">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-784">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-784">10001</span></span></td>
<td><span data-ttu-id="c0b5e-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-785">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-787">50,00</span></span></td>
<td><span data-ttu-id="c0b5e-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-789">CC001</span></span></td>
<td><span data-ttu-id="c0b5e-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0b5e-790">HR</span></span></td>
<td><span data-ttu-id="c0b5e-791">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-791">10001</span></span></td>
<td><span data-ttu-id="c0b5e-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-792">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-793">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c0b5e-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-796">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-797">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-798">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-798">10001</span></span></td>
<td><span data-ttu-id="c0b5e-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-799">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-800">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-801">436.00</span></span></td>
<td><span data-ttu-id="c0b5e-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-803">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-804">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-805">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-805">10001</span></span></td>
<td><span data-ttu-id="c0b5e-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-806">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-807">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c0b5e-808">685.14</span></span></td>
<td><span data-ttu-id="c0b5e-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-810">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-811">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-812">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-812">10001</span></span></td>
<td><span data-ttu-id="c0b5e-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-813">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-814">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c0b5e-815">124.57</span></span></td>
<td><span data-ttu-id="c0b5e-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-817">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-818">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-819">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-819">10001</span></span></td>
<td><span data-ttu-id="c0b5e-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-820">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-822">-675.00</span></span></td>
<td><span data-ttu-id="c0b5e-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-824">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-825">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-826">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-826">10001</span></span></td>
<td><span data-ttu-id="c0b5e-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-827">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c0b5e-829">438.75</span></span></td>
<td><span data-ttu-id="c0b5e-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-831">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-832">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-833">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-833">10001</span></span></td>
<td><span data-ttu-id="c0b5e-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-834">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c0b5e-836">236.25</span></span></td>
<td><span data-ttu-id="c0b5e-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-838">CC002</span></span></td>
<td><span data-ttu-id="c0b5e-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-839">Finance</span></span></td>
<td><span data-ttu-id="c0b5e-840">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-840">10001</span></span></td>
<td><span data-ttu-id="c0b5e-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-841">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-842">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="c0b5e-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c0b5e-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-845">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-846">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-847">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-847">10001</span></span></td>
<td><span data-ttu-id="c0b5e-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-848">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-849">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c0b5e-850">5,297.69</span></span></td>
<td><span data-ttu-id="c0b5e-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-852">CC004</span></span></td>
<td><span data-ttu-id="c0b5e-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0b5e-853">Packaging</span></span></td>
<td><span data-ttu-id="c0b5e-854">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-854">10001</span></span></td>
<td><span data-ttu-id="c0b5e-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-855">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-856">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c0b5e-857">2,852.60</span></span></td>
<td><span data-ttu-id="c0b5e-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-859">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-860">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-861">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-861">10001</span></span></td>
<td><span data-ttu-id="c0b5e-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-862">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c0b5e-864">-713.75</span></span></td>
<td><span data-ttu-id="c0b5e-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-866">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-867">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-868">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-868">10001</span></span></td>
<td><span data-ttu-id="c0b5e-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-869">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c0b5e-871">535.31</span></span></td>
<td><span data-ttu-id="c0b5e-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-873">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-874">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-875">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-875">10001</span></span></td>
<td><span data-ttu-id="c0b5e-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-876">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c0b5e-878">178.44</span></span></td>
<td><span data-ttu-id="c0b5e-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-880">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-881">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-882">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-882">10001</span></span></td>
<td><span data-ttu-id="c0b5e-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-883">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-884">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="c0b5e-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c0b5e-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-887">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-888">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-889">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-889">10001</span></span></td>
<td><span data-ttu-id="c0b5e-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-890">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-891">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c0b5e-892">4,487.12</span></span></td>
<td><span data-ttu-id="c0b5e-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-894">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-895">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-896">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-896">10001</span></span></td>
<td><span data-ttu-id="c0b5e-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-897">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-898">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c0b5e-899">1,495.71</span></span></td>
<td><span data-ttu-id="c0b5e-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-901">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-902">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-903">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-903">10001</span></span></td>
<td><span data-ttu-id="c0b5e-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-904">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="c0b5e-906">-286.25</span></span></td>
<td><span data-ttu-id="c0b5e-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-908">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-909">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-910">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-910">10001</span></span></td>
<td><span data-ttu-id="c0b5e-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-911">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c0b5e-913">241.05</span></span></td>
<td><span data-ttu-id="c0b5e-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-915">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-916">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-917">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-917">10001</span></span></td>
<td><span data-ttu-id="c0b5e-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-918">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c0b5e-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c0b5e-920">45.20</span></span></td>
<td><span data-ttu-id="c0b5e-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-922">CC003</span></span></td>
<td><span data-ttu-id="c0b5e-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c0b5e-923">Assembly</span></span></td>
<td><span data-ttu-id="c0b5e-924">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-924">10001</span></span></td>
<td><span data-ttu-id="c0b5e-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-925">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-926">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="c0b5e-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c0b5e-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-929">Prod 1</span></span></td>
<td><span data-ttu-id="c0b5e-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-930">Product 1</span></span></td>
<td><span data-ttu-id="c0b5e-931">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-931">10001</span></span></td>
<td><span data-ttu-id="c0b5e-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-932">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-933">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c0b5e-934">2,507.09</span></span></td>
<td><span data-ttu-id="c0b5e-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c0b5e-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-936">Prod 2</span></span></td>
<td><span data-ttu-id="c0b5e-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-937">Product 2</span></span></td>
<td><span data-ttu-id="c0b5e-938">10001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-938">10001</span></span></td>
<td><span data-ttu-id="c0b5e-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-939">Electricity</span></span></td>
<td><span data-ttu-id="c0b5e-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-940">Variable cost</span></span></td>
<td><span data-ttu-id="c0b5e-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c0b5e-941">470.08</span></span></td>
<td><span data-ttu-id="c0b5e-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c0b5e-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c0b5e-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="c0b5e-943">Conclusion</span></span>
<span data-ttu-id="c0b5e-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="c0b5e-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c0b5e-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="c0b5e-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c0b5e-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="c0b5e-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c0b5e-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c0b5e-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c0b5e-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c0b5e-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="c0b5e-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c0b5e-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c0b5e-951">CC099</span></span></th>
<th><span data-ttu-id="c0b5e-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c0b5e-952">CC001</span></span></th>
<th><span data-ttu-id="c0b5e-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c0b5e-953">CC002</span></span></th>
<th><span data-ttu-id="c0b5e-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c0b5e-954">CC003</span></span></th>
<th><span data-ttu-id="c0b5e-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c0b5e-955">CC004</span></span></th>
<th><span data-ttu-id="c0b5e-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-956">Proj 1</span></span></th>
<th><span data-ttu-id="c0b5e-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-957">Proj 2</span></span></th>
<th><span data-ttu-id="c0b5e-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c0b5e-958">Prod 1</span></span></th>
<th><span data-ttu-id="c0b5e-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c0b5e-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c0b5e-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c0b5e-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c0b5e-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c0b5e-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-971">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c0b5e-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c0b5e-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-973">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-974">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-975">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-976">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-977">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c0b5e-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c0b5e-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c0b5e-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-982">000</span><span class="sxs-lookup"><span data-stu-id="c0b5e-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-983">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-984">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-985">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-986">0.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-987">30.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-988">10.00</span><span class="sxs-lookup"><span data-stu-id="c0b5e-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c0b5e-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c0b5e-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c0b5e-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c0b5e-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0b5e-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c0b5e-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="c0b5e-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c0b5e-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c0b5e-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c0b5e-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c0b5e-996">สำหรับข้อมูลเพิ่มเติม ดู [นโยบายการรวบรวมต้นทุนและการคำนวณค่าโสหุ้ย](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="c0b5e-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



