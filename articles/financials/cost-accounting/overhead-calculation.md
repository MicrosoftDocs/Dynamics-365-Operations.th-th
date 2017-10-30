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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 285799d70a945c2dae1e3c65296282d5c432a243
ms.contentlocale: th-th
ms.lasthandoff: 10/30/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="45d77-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="45d77-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="45d77-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="45d77-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="45d77-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="45d77-105">Term definition</span></span>
---------------

<span data-ttu-id="45d77-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="45d77-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="45d77-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="45d77-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="45d77-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="45d77-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="45d77-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="45d77-109">Rent</span></span>
-   <span data-ttu-id="45d77-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-110">Electricity</span></span>
-   <span data-ttu-id="45d77-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="45d77-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="45d77-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="45d77-112">Overhead calculation overview</span></span>
<span data-ttu-id="45d77-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="45d77-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="45d77-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="45d77-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="45d77-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="45d77-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="45d77-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="45d77-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="45d77-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="45d77-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45d77-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="45d77-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="45d77-119">Version type</span></span>
-   <span data-ttu-id="45d77-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="45d77-120">Date and time</span></span>
-   <span data-ttu-id="45d77-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="45d77-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-122">Fiscal year</span></span>
-   <span data-ttu-id="45d77-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-123">Fiscal period</span></span>

<span data-ttu-id="45d77-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="45d77-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="45d77-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="45d77-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="45d77-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="45d77-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="45d77-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="45d77-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="45d77-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="45d77-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="45d77-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="45d77-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="45d77-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="45d77-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="45d77-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="45d77-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="45d77-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="45d77-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="45d77-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="45d77-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="45d77-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="45d77-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="45d77-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="45d77-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="45d77-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="45d77-140">Main account</span></span></th>
<th><span data-ttu-id="45d77-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="45d77-143">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-143">CC099</span></span></td>
<td><span data-ttu-id="45d77-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-144">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-145">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-145">10001</span></span></td>
<td><span data-ttu-id="45d77-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-146">Electricity</span></span></td>
<td><span data-ttu-id="45d77-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="45d77-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="45d77-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="45d77-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="45d77-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="45d77-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-151">Define the cost behavior rule</span></span>

<span data-ttu-id="45d77-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="45d77-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="45d77-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="45d77-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="45d77-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="45d77-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="45d77-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="45d77-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="45d77-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="45d77-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="45d77-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="45d77-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-160">Journal</span></span></th>
<th><span data-ttu-id="45d77-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="45d77-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="45d77-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="45d77-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-164">00001</span><span class="sxs-lookup"><span data-stu-id="45d77-164">00001</span></span></td>
<td><span data-ttu-id="45d77-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="45d77-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-166">Fiscal</span></span></td>
<td><span data-ttu-id="45d77-167">2017</span><span class="sxs-lookup"><span data-stu-id="45d77-167">2017</span></span></td>
<td><span data-ttu-id="45d77-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-168">Period 1</span></span></td>
<td><span data-ttu-id="45d77-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="45d77-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="45d77-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-173">Cost element</span></span></th>
<th><span data-ttu-id="45d77-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-174">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="45d77-177">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-177">CC099</span></span></td>
<td><span data-ttu-id="45d77-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-178">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-179">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-179">10001</span></span></td>
<td><span data-ttu-id="45d77-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-180">Electricity</span></span></td>
<td><span data-ttu-id="45d77-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="45d77-181">Unclassified</span></span></td>
<td><span data-ttu-id="45d77-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="45d77-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-185">Cost element</span></span></th>
<th><span data-ttu-id="45d77-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-186">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-187">Amount</span></span></th>
<th><span data-ttu-id="45d77-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-189">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-189">CC099</span></span></td>
<td><span data-ttu-id="45d77-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-190">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-191">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-191">10001</span></span></td>
<td><span data-ttu-id="45d77-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-192">Electricity</span></span></td>
<td><span data-ttu-id="45d77-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="45d77-193">Unclassified</span></span></td>
<td><span data-ttu-id="45d77-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-194">10,000.00</span></span></td>
<td><span data-ttu-id="45d77-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-196">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-196">CC099</span></span></td>
<td><span data-ttu-id="45d77-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-197">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-198">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-198">10001</span></span></td>
<td><span data-ttu-id="45d77-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-199">Electricity</span></span></td>
<td><span data-ttu-id="45d77-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="45d77-200">Unclassified</span></span></td>
<td><span data-ttu-id="45d77-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-201">-10,000.00</span></span></td>
<td><span data-ttu-id="45d77-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-203">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-203">CC099</span></span></td>
<td><span data-ttu-id="45d77-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-204">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-205">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-205">10001</span></span></td>
<td><span data-ttu-id="45d77-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-206">Electricity</span></span></td>
<td><span data-ttu-id="45d77-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-207">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-208">1,000.00</span></span></td>
<td><span data-ttu-id="45d77-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-210">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-210">CC099</span></span></td>
<td><span data-ttu-id="45d77-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-211">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-212">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-212">10001</span></span></td>
<td><span data-ttu-id="45d77-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-213">Electricity</span></span></td>
<td><span data-ttu-id="45d77-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-214">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-215">9,000.00</span></span></td>
<td><span data-ttu-id="45d77-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-217">สำหรับข้อมูลรายละเอียดเกี่ยวกับพฤติกรรมต้นทุน ดูนโยบายพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="45d77-218">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="45d77-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="45d77-219">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="45d77-220">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="45d77-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="45d77-221">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="45d77-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="45d77-222">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-222">Define the cost distribution rule</span></span>

<span data-ttu-id="45d77-223">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="45d77-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="45d77-224">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="45d77-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="45d77-225">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="45d77-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="45d77-226">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="45d77-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="45d77-227">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="45d77-228">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-229">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-229">Cost object</span></span></th>
<th><span data-ttu-id="45d77-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="45d77-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-231">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-231">CC001</span></span></td>
<td><span data-ttu-id="45d77-232">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-232">HR</span></span></td>
<td><span data-ttu-id="45d77-233">1,000</span><span class="sxs-lookup"><span data-stu-id="45d77-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-234">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-234">CC002</span></span></td>
<td><span data-ttu-id="45d77-235">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-235">Finance</span></span></td>
<td><span data-ttu-id="45d77-236">6,000</span><span class="sxs-lookup"><span data-stu-id="45d77-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-237">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-237">CC003</span></span></td>
<td><span data-ttu-id="45d77-238">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-238">Assembly</span></span></td>
<td><span data-ttu-id="45d77-239">0</span><span class="sxs-lookup"><span data-stu-id="45d77-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-240">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-241">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-241">Cost object</span></span></th>
<th><span data-ttu-id="45d77-242">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-242">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-243">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-243">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-244">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-245">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-245">CC001</span></span></td>
<td><span data-ttu-id="45d77-246">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-246">HR</span></span></td>
<td><span data-ttu-id="45d77-247">1,000</span><span class="sxs-lookup"><span data-stu-id="45d77-247">1,000</span></span></td>
<td><span data-ttu-id="45d77-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="45d77-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="45d77-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-250">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-250">CC002</span></span></td>
<td><span data-ttu-id="45d77-251">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-251">Finance</span></span></td>
<td><span data-ttu-id="45d77-252">6,000</span><span class="sxs-lookup"><span data-stu-id="45d77-252">6,000</span></span></td>
<td><span data-ttu-id="45d77-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="45d77-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="45d77-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-255">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-255">CC003</span></span></td>
<td><span data-ttu-id="45d77-256">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-256">Assembly</span></span></td>
<td><span data-ttu-id="45d77-257">0</span><span class="sxs-lookup"><span data-stu-id="45d77-257">0</span></span></td>
<td><span data-ttu-id="45d77-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="45d77-259">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-260">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="45d77-261">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-262">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-262">Cost object</span></span></th>
<th><span data-ttu-id="45d77-263">สูตร</span><span class="sxs-lookup"><span data-stu-id="45d77-263">Formula</span></span></th>
<th><span data-ttu-id="45d77-264">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-264">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-265">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-265">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-266">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-267">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-267">CC001</span></span></td>
<td><span data-ttu-id="45d77-268">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-268">HR</span></span></td>
<td><span data-ttu-id="45d77-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="45d77-270">1</span><span class="sxs-lookup"><span data-stu-id="45d77-270">1</span></span></td>
<td><span data-ttu-id="45d77-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="45d77-272">500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-273">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-273">CC002</span></span></td>
<td><span data-ttu-id="45d77-274">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-274">Finance</span></span></td>
<td><span data-ttu-id="45d77-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="45d77-276">1</span><span class="sxs-lookup"><span data-stu-id="45d77-276">1</span></span></td>
<td><span data-ttu-id="45d77-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="45d77-278">500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-279">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-279">CC003</span></span></td>
<td><span data-ttu-id="45d77-280">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-280">Assembly</span></span></td>
<td><span data-ttu-id="45d77-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="45d77-282">0</span><span class="sxs-lookup"><span data-stu-id="45d77-282">0</span></span></td>
<td><span data-ttu-id="45d77-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="45d77-284">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="45d77-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-286">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-286">Journal</span></span></th>
<th><span data-ttu-id="45d77-287">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="45d77-288">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="45d77-289">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="45d77-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-290">00002</span><span class="sxs-lookup"><span data-stu-id="45d77-290">00002</span></span></td>
<td><span data-ttu-id="45d77-291">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="45d77-292">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-292">Fiscal</span></span></td>
<td><span data-ttu-id="45d77-293">2017</span><span class="sxs-lookup"><span data-stu-id="45d77-293">2017</span></span></td>
<td><span data-ttu-id="45d77-294">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-294">Period 1</span></span></td>
<td><span data-ttu-id="45d77-295">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="45d77-296">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="45d77-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-297">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-298">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-299">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-299">Cost element</span></span></th>
<th><span data-ttu-id="45d77-300">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-300">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-301">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-302">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-303">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-303">CC099</span></span></td>
<td><span data-ttu-id="45d77-304">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-304">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-305">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-305">10001</span></span></td>
<td><span data-ttu-id="45d77-306">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-306">Electricity</span></span></td>
<td><span data-ttu-id="45d77-307">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-307">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-308">1,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-309">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-310">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-310">CC099</span></span></td>
<td><span data-ttu-id="45d77-311">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-311">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-312">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-312">10001</span></span></td>
<td><span data-ttu-id="45d77-313">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-313">Electricity</span></span></td>
<td><span data-ttu-id="45d77-314">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-314">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="45d77-316">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-317">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-318">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-318">Cost element</span></span></th>
<th><span data-ttu-id="45d77-319">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-319">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-320">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-320">Amount</span></span></th>
<th><span data-ttu-id="45d77-321">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-322">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-322">CC099</span></span></td>
<td><span data-ttu-id="45d77-323">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-323">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-324">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-324">10001</span></span></td>
<td><span data-ttu-id="45d77-325">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-325">Electricity</span></span></td>
<td><span data-ttu-id="45d77-326">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-326">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-327">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="45d77-327">-1,000.00</span></span></td>
<td><span data-ttu-id="45d77-328">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-329">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-329">CC001</span></span></td>
<td><span data-ttu-id="45d77-330">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-330">HR</span></span></td>
<td><span data-ttu-id="45d77-331">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-331">10001</span></span></td>
<td><span data-ttu-id="45d77-332">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-332">Electricity</span></span></td>
<td><span data-ttu-id="45d77-333">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-333">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-334">500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-334">500.00</span></span></td>
<td><span data-ttu-id="45d77-335">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-336">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-336">CC002</span></span></td>
<td><span data-ttu-id="45d77-337">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-337">Finance</span></span></td>
<td><span data-ttu-id="45d77-338">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-338">10001</span></span></td>
<td><span data-ttu-id="45d77-339">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-339">Electricity</span></span></td>
<td><span data-ttu-id="45d77-340">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-340">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-341">500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-341">500.00</span></span></td>
<td><span data-ttu-id="45d77-342">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-343">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-343">CC099</span></span></td>
<td><span data-ttu-id="45d77-344">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="45d77-344">Default cost center</span></span></td>
<td><span data-ttu-id="45d77-345">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-345">10001</span></span></td>
<td><span data-ttu-id="45d77-346">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-346">Electricity</span></span></td>
<td><span data-ttu-id="45d77-347">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-347">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="45d77-348">-9,000.00</span></span></td>
<td><span data-ttu-id="45d77-349">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-350">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-350">CC001</span></span></td>
<td><span data-ttu-id="45d77-351">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-351">HR</span></span></td>
<td><span data-ttu-id="45d77-352">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-352">10001</span></span></td>
<td><span data-ttu-id="45d77-353">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-353">Electricity</span></span></td>
<td><span data-ttu-id="45d77-354">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-354">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="45d77-355">1,285.71</span></span></td>
<td><span data-ttu-id="45d77-356">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-357">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-357">CC002</span></span></td>
<td><span data-ttu-id="45d77-358">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-358">Finance</span></span></td>
<td><span data-ttu-id="45d77-359">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-359">10001</span></span></td>
<td><span data-ttu-id="45d77-360">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-360">Electricity</span></span></td>
<td><span data-ttu-id="45d77-361">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-361">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="45d77-362">7,714.29</span></span></td>
<td><span data-ttu-id="45d77-363">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-364">สำหรับรายละเอียดเกี่ยวกับการกระจายต้นทุนและฐานการปันส่วน ให้ดูนโยบายการกระจายต้นทุนและฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="45d77-365">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="45d77-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="45d77-366">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="45d77-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="45d77-367">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="45d77-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="45d77-368">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="45d77-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="45d77-369">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="45d77-369">Define the overhead rate</span></span>

<span data-ttu-id="45d77-370">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="45d77-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="45d77-371">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="45d77-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-372">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-372">Cost object</span></span></th>
<th><span data-ttu-id="45d77-373">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="45d77-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-374">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-374">Proj 1</span></span></td>
<td><span data-ttu-id="45d77-375">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-375">Project 1</span></span></td>
<td><span data-ttu-id="45d77-376">3</span><span class="sxs-lookup"><span data-stu-id="45d77-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-377">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-377">Proj 2</span></span></td>
<td><span data-ttu-id="45d77-378">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-378">Project 2</span></span></td>
<td><span data-ttu-id="45d77-379">1</span><span class="sxs-lookup"><span data-stu-id="45d77-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-380">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-381">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-381">Cost object</span></span></th>
<th><span data-ttu-id="45d77-382">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-382">Cost element</span></span></th>
<th><span data-ttu-id="45d77-383">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-383">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-384">หน่วย</span><span class="sxs-lookup"><span data-stu-id="45d77-384">Units</span></span></th>
<th><span data-ttu-id="45d77-385">อัตรา</span><span class="sxs-lookup"><span data-stu-id="45d77-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-386">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-386">CC001</span></span></td>
<td><span data-ttu-id="45d77-387">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-387">HR</span></span></td>
<td><span data-ttu-id="45d77-388">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-388">10001</span></span></td>
<td><span data-ttu-id="45d77-389">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-389">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-390">1</span><span class="sxs-lookup"><span data-stu-id="45d77-390">1</span></span></td>
<td><span data-ttu-id="45d77-391">10</span><span class="sxs-lookup"><span data-stu-id="45d77-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-392">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-393">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-393">Cost object</span></span></th>
<th><span data-ttu-id="45d77-394">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-394">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-395">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-395">Cost element</span></span></th>
<th><span data-ttu-id="45d77-396">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-396">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-397">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-398">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-398">Proj 1</span></span></td>
<td><span data-ttu-id="45d77-399">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-399">Project 1</span></span></td>
<td><span data-ttu-id="45d77-400">3</span><span class="sxs-lookup"><span data-stu-id="45d77-400">3</span></span></td>
<td><span data-ttu-id="45d77-401">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-401">10001</span></span></td>
<td><span data-ttu-id="45d77-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="45d77-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="45d77-403">30.00</span><span class="sxs-lookup"><span data-stu-id="45d77-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-404">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-404">Proj 2</span></span></td>
<td><span data-ttu-id="45d77-405">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-405">Project 2</span></span></td>
<td><span data-ttu-id="45d77-406">1</span><span class="sxs-lookup"><span data-stu-id="45d77-406">1</span></span></td>
<td><span data-ttu-id="45d77-407">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-407">10001</span></span></td>
<td><span data-ttu-id="45d77-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="45d77-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="45d77-409">10.00</span><span class="sxs-lookup"><span data-stu-id="45d77-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="45d77-410">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-411">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-411">Journal</span></span></th>
<th><span data-ttu-id="45d77-412">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="45d77-413">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="45d77-414">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="45d77-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-415">00003</span><span class="sxs-lookup"><span data-stu-id="45d77-415">00003</span></span></td>
<td><span data-ttu-id="45d77-416">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="45d77-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="45d77-417">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-417">Fiscal</span></span></td>
<td><span data-ttu-id="45d77-418">2017</span><span class="sxs-lookup"><span data-stu-id="45d77-418">2017</span></span></td>
<td><span data-ttu-id="45d77-419">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-419">Period 1</span></span></td>
<td><span data-ttu-id="45d77-420">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="45d77-421">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="45d77-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-422">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-423">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-423">Cost object</span></span></th>
<th><span data-ttu-id="45d77-424">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-425">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-426">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-426">Proj 1</span></span></td>
<td><span data-ttu-id="45d77-427">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="45d77-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="45d77-428">3.00</span><span class="sxs-lookup"><span data-stu-id="45d77-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-429">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-430">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-430">Proj 2</span></span></td>
<td><span data-ttu-id="45d77-431">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="45d77-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="45d77-432">1.00</span><span class="sxs-lookup"><span data-stu-id="45d77-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="45d77-433">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-434">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-435">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-435">Cost element</span></span></th>
<th><span data-ttu-id="45d77-436">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-436">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-437">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-437">Amount</span></span></th>
<th><span data-ttu-id="45d77-438">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="45d77-439">CC0001</span></span></td>
<td><span data-ttu-id="45d77-440">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-440">HR</span></span></td>
<td><span data-ttu-id="45d77-441">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-441">10001</span></span></td>
<td><span data-ttu-id="45d77-442">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-442">Electricity</span></span></td>
<td><span data-ttu-id="45d77-443">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-443">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="45d77-444">-30.00</span></span></td>
<td><span data-ttu-id="45d77-445">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-446">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-446">Proj 1</span></span></td>
<td><span data-ttu-id="45d77-447">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="45d77-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="45d77-448">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-448">10001</span></span></td>
<td><span data-ttu-id="45d77-449">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-449">Electricity</span></span></td>
<td><span data-ttu-id="45d77-450">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-450">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-451">30.00</span><span class="sxs-lookup"><span data-stu-id="45d77-451">30.00</span></span></td>
<td><span data-ttu-id="45d77-452">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-453">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-453">CC001</span></span></td>
<td><span data-ttu-id="45d77-454">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-454">HR</span></span></td>
<td><span data-ttu-id="45d77-455">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-455">10001</span></span></td>
<td><span data-ttu-id="45d77-456">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-456">Electricity</span></span></td>
<td><span data-ttu-id="45d77-457">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-457">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="45d77-458">-10.00</span></span></td>
<td><span data-ttu-id="45d77-459">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-460">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-460">Proj 2</span></span></td>
<td><span data-ttu-id="45d77-461">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="45d77-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="45d77-462">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-462">10001</span></span></td>
<td><span data-ttu-id="45d77-463">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-463">Electricity</span></span></td>
<td><span data-ttu-id="45d77-464">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-464">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-465">10.00</span><span class="sxs-lookup"><span data-stu-id="45d77-465">10.00</span></span></td>
<td><span data-ttu-id="45d77-466">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-467">สำหรับข้อมูลรายละเอียดเกี่ยวกับนโยบายอัตราค่าโสหุ้ย ให้ดูนโยบายอัตราค่าโสหุ้ยและฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="45d77-468">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="45d77-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="45d77-469">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="45d77-470">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="45d77-471">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="45d77-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="45d77-472">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="45d77-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="45d77-473">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="45d77-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="45d77-474">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="45d77-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="45d77-475">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="45d77-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="45d77-476">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="45d77-477">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="45d77-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="45d77-478">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-478">Define the cost allocation</span></span>

<span data-ttu-id="45d77-479">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="45d77-480">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="45d77-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="45d77-481">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="45d77-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-482">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-482">Cost object</span></span></th>
<th><span data-ttu-id="45d77-483">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="45d77-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-484">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-484">CC002</span></span></td>
<td><span data-ttu-id="45d77-485">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-485">Finance</span></span></td>
<td><span data-ttu-id="45d77-486">35</span><span class="sxs-lookup"><span data-stu-id="45d77-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-487">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-487">CC003</span></span></td>
<td><span data-ttu-id="45d77-488">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-488">Assembly</span></span></td>
<td><span data-ttu-id="45d77-489">55</span><span class="sxs-lookup"><span data-stu-id="45d77-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-490">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-490">CC004</span></span></td>
<td><span data-ttu-id="45d77-491">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-491">Packaging</span></span></td>
<td><span data-ttu-id="45d77-492">10</span><span class="sxs-lookup"><span data-stu-id="45d77-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-493">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="45d77-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="45d77-494">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="45d77-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-495">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-495">Cost object</span></span></th>
<th><span data-ttu-id="45d77-496">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-497">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-497">CC003</span></span></td>
<td><span data-ttu-id="45d77-498">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-498">Assembly</span></span></td>
<td><span data-ttu-id="45d77-499">65</span><span class="sxs-lookup"><span data-stu-id="45d77-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-500">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-500">CC004</span></span></td>
<td><span data-ttu-id="45d77-501">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-501">Packaging</span></span></td>
<td><span data-ttu-id="45d77-502">35</span><span class="sxs-lookup"><span data-stu-id="45d77-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-503">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="45d77-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="45d77-504">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="45d77-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-505">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-505">Cost object</span></span></th>
<th><span data-ttu-id="45d77-506">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="45d77-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-507">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-507">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-508">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-508">Product 1</span></span></td>
<td><span data-ttu-id="45d77-509">60</span><span class="sxs-lookup"><span data-stu-id="45d77-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-510">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-510">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-511">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-511">Product 2</span></span></td>
<td><span data-ttu-id="45d77-512">20</span><span class="sxs-lookup"><span data-stu-id="45d77-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-513">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="45d77-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="45d77-514">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="45d77-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-515">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-515">Cost object</span></span></th>
<th><span data-ttu-id="45d77-516">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="45d77-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-517">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-517">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-518">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-518">Product 1</span></span></td>
<td><span data-ttu-id="45d77-519">80</span><span class="sxs-lookup"><span data-stu-id="45d77-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-520">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-520">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-521">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-521">Product 2</span></span></td>
<td><span data-ttu-id="45d77-522">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="45d77-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-523">**หมายเหตุ:** ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ใช้กับผลิตภัณฑ์สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="45d77-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="45d77-524">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวให้บริการการประเมินทางสถิติ ให้ดูเท็มเพลตตัวให้บริการการประเมินทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="45d77-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="45d77-525">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในอีกไม่ช้านี้) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="45d77-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-526">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-526">Cost object</span></span></th>
<th><span data-ttu-id="45d77-527">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-527">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-528">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-528">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-529">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-529">Amount</span></span></th>
<th><span data-ttu-id="45d77-530">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-531">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-531">CC002</span></span></td>
<td><span data-ttu-id="45d77-532">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-532">Finance</span></span></td>
<td><span data-ttu-id="45d77-533">35</span><span class="sxs-lookup"><span data-stu-id="45d77-533">35</span></span></td>
<td><span data-ttu-id="45d77-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="45d77-535">175.00</span><span class="sxs-lookup"><span data-stu-id="45d77-535">175.00</span></span></td>
<td><span data-ttu-id="45d77-536">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-537">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-537">CC003</span></span></td>
<td><span data-ttu-id="45d77-538">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-538">Assembly</span></span></td>
<td><span data-ttu-id="45d77-539">55</span><span class="sxs-lookup"><span data-stu-id="45d77-539">55</span></span></td>
<td><span data-ttu-id="45d77-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="45d77-541">275.00</span><span class="sxs-lookup"><span data-stu-id="45d77-541">275.00</span></span></td>
<td><span data-ttu-id="45d77-542">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-543">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-543">CC004</span></span></td>
<td><span data-ttu-id="45d77-544">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-544">Packaging</span></span></td>
<td><span data-ttu-id="45d77-545">10</span><span class="sxs-lookup"><span data-stu-id="45d77-545">10</span></span></td>
<td><span data-ttu-id="45d77-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="45d77-547">50.00</span><span class="sxs-lookup"><span data-stu-id="45d77-547">50.00</span></span></td>
<td><span data-ttu-id="45d77-548">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-549">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-549">CC002</span></span></td>
<td><span data-ttu-id="45d77-550">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-550">Finance</span></span></td>
<td><span data-ttu-id="45d77-551">35</span><span class="sxs-lookup"><span data-stu-id="45d77-551">35</span></span></td>
<td><span data-ttu-id="45d77-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="45d77-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="45d77-553">436.00</span><span class="sxs-lookup"><span data-stu-id="45d77-553">436.00</span></span></td>
<td><span data-ttu-id="45d77-554">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-555">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-555">CC003</span></span></td>
<td><span data-ttu-id="45d77-556">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-556">Assembly</span></span></td>
<td><span data-ttu-id="45d77-557">55</span><span class="sxs-lookup"><span data-stu-id="45d77-557">55</span></span></td>
<td><span data-ttu-id="45d77-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="45d77-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="45d77-559">685.14</span><span class="sxs-lookup"><span data-stu-id="45d77-559">685.14</span></span></td>
<td><span data-ttu-id="45d77-560">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-561">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-561">CC004</span></span></td>
<td><span data-ttu-id="45d77-562">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-562">Packaging</span></span></td>
<td><span data-ttu-id="45d77-563">10</span><span class="sxs-lookup"><span data-stu-id="45d77-563">10</span></span></td>
<td><span data-ttu-id="45d77-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="45d77-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="45d77-565">124.57</span><span class="sxs-lookup"><span data-stu-id="45d77-565">124.57</span></span></td>
<td><span data-ttu-id="45d77-566">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-567">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="45d77-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-568">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-568">Cost object</span></span></th>
<th><span data-ttu-id="45d77-569">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-569">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-570">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-570">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-571">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-571">Amount</span></span></th>
<th><span data-ttu-id="45d77-572">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-573">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-573">CC003</span></span></td>
<td><span data-ttu-id="45d77-574">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-574">Assembly</span></span></td>
<td><span data-ttu-id="45d77-575">65</span><span class="sxs-lookup"><span data-stu-id="45d77-575">65</span></span></td>
<td><span data-ttu-id="45d77-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="45d77-577">438.75</span><span class="sxs-lookup"><span data-stu-id="45d77-577">438.75</span></span></td>
<td><span data-ttu-id="45d77-578">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-579">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-579">CC004</span></span></td>
<td><span data-ttu-id="45d77-580">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-580">Packaging</span></span></td>
<td><span data-ttu-id="45d77-581">35</span><span class="sxs-lookup"><span data-stu-id="45d77-581">35</span></span></td>
<td><span data-ttu-id="45d77-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="45d77-583">236.25</span><span class="sxs-lookup"><span data-stu-id="45d77-583">236.25</span></span></td>
<td><span data-ttu-id="45d77-584">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-585">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-585">CC003</span></span></td>
<td><span data-ttu-id="45d77-586">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-586">Assembly</span></span></td>
<td><span data-ttu-id="45d77-587">65</span><span class="sxs-lookup"><span data-stu-id="45d77-587">65</span></span></td>
<td><span data-ttu-id="45d77-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="45d77-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="45d77-589">5,297.69</span></span></td>
<td><span data-ttu-id="45d77-590">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-591">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-591">CC004</span></span></td>
<td><span data-ttu-id="45d77-592">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-592">Packaging</span></span></td>
<td><span data-ttu-id="45d77-593">35</span><span class="sxs-lookup"><span data-stu-id="45d77-593">35</span></span></td>
<td><span data-ttu-id="45d77-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="45d77-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="45d77-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="45d77-595">2,852.60</span></span></td>
<td><span data-ttu-id="45d77-596">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-597">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="45d77-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-598">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-598">Cost object</span></span></th>
<th><span data-ttu-id="45d77-599">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-599">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-600">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-600">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-601">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-601">Amount</span></span></th>
<th><span data-ttu-id="45d77-602">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-603">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-603">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-604">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-604">Product 1</span></span></td>
<td><span data-ttu-id="45d77-605">60</span><span class="sxs-lookup"><span data-stu-id="45d77-605">60</span></span></td>
<td><span data-ttu-id="45d77-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="45d77-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="45d77-607">535.31</span><span class="sxs-lookup"><span data-stu-id="45d77-607">535.31</span></span></td>
<td><span data-ttu-id="45d77-608">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-609">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-609">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-610">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-610">Product 2</span></span></td>
<td><span data-ttu-id="45d77-611">20</span><span class="sxs-lookup"><span data-stu-id="45d77-611">20</span></span></td>
<td><span data-ttu-id="45d77-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="45d77-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="45d77-613">178.44</span><span class="sxs-lookup"><span data-stu-id="45d77-613">178.44</span></span></td>
<td><span data-ttu-id="45d77-614">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-615">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-615">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-616">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-616">Product 1</span></span></td>
<td><span data-ttu-id="45d77-617">60</span><span class="sxs-lookup"><span data-stu-id="45d77-617">60</span></span></td>
<td><span data-ttu-id="45d77-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="45d77-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="45d77-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="45d77-619">4,487.12</span></span></td>
<td><span data-ttu-id="45d77-620">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-621">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-621">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-622">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-622">Product 2</span></span></td>
<td><span data-ttu-id="45d77-623">20</span><span class="sxs-lookup"><span data-stu-id="45d77-623">20</span></span></td>
<td><span data-ttu-id="45d77-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="45d77-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="45d77-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="45d77-625">1,495.71</span></span></td>
<td><span data-ttu-id="45d77-626">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45d77-627">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="45d77-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-628">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-628">Cost object</span></span></th>
<th><span data-ttu-id="45d77-629">ขนาด</span><span class="sxs-lookup"><span data-stu-id="45d77-629">Magnitude</span></span></th>
<th><span data-ttu-id="45d77-630">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="45d77-630">Allocation factor</span></span></th>
<th><span data-ttu-id="45d77-631">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-631">Amount</span></span></th>
<th><span data-ttu-id="45d77-632">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-633">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-633">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-634">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-634">Product 1</span></span></td>
<td><span data-ttu-id="45d77-635">80</span><span class="sxs-lookup"><span data-stu-id="45d77-635">80</span></span></td>
<td><span data-ttu-id="45d77-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="45d77-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="45d77-637">241.05</span><span class="sxs-lookup"><span data-stu-id="45d77-637">241.05</span></span></td>
<td><span data-ttu-id="45d77-638">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-639">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-639">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-640">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-640">Product 2</span></span></td>
<td><span data-ttu-id="45d77-641">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="45d77-641">15</span></span></td>
<td><span data-ttu-id="45d77-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="45d77-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="45d77-643">45.20</span><span class="sxs-lookup"><span data-stu-id="45d77-643">45.20</span></span></td>
<td><span data-ttu-id="45d77-644">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-645">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-645">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-646">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-646">Product 1</span></span></td>
<td><span data-ttu-id="45d77-647">80</span><span class="sxs-lookup"><span data-stu-id="45d77-647">80</span></span></td>
<td><span data-ttu-id="45d77-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="45d77-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="45d77-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="45d77-649">2,507.09</span></span></td>
<td><span data-ttu-id="45d77-650">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-651">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-651">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-652">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-652">Product 2</span></span></td>
<td><span data-ttu-id="45d77-653">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="45d77-653">15</span></span></td>
<td><span data-ttu-id="45d77-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="45d77-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="45d77-655">470.08</span><span class="sxs-lookup"><span data-stu-id="45d77-655">470.08</span></span></td>
<td><span data-ttu-id="45d77-656">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="45d77-657">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="45d77-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-658">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-658">Journal</span></span></th>
<th><span data-ttu-id="45d77-659">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="45d77-660">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="45d77-661">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="45d77-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-662">00004</span><span class="sxs-lookup"><span data-stu-id="45d77-662">00004</span></span></td>
<td><span data-ttu-id="45d77-663">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="45d77-664">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-664">Fiscal</span></span></td>
<td><span data-ttu-id="45d77-665">2017</span><span class="sxs-lookup"><span data-stu-id="45d77-665">2017</span></span></td>
<td><span data-ttu-id="45d77-666">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-666">Period 1</span></span></td>
<td><span data-ttu-id="45d77-667">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="45d77-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="45d77-668">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="45d77-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="45d77-669">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-670">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-671">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-671">Cost element</span></span></th>
<th><span data-ttu-id="45d77-672">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-672">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-673">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-674">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-675">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-675">CC001</span></span></td>
<td><span data-ttu-id="45d77-676">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-676">HR</span></span></td>
<td><span data-ttu-id="45d77-677">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-677">10001</span></span></td>
<td><span data-ttu-id="45d77-678">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-678">Electricity</span></span></td>
<td><span data-ttu-id="45d77-679">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-679">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-680">500.00</span><span class="sxs-lookup"><span data-stu-id="45d77-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-681">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-682">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-682">CC001</span></span></td>
<td><span data-ttu-id="45d77-683">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-683">HR</span></span></td>
<td><span data-ttu-id="45d77-684">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-684">10001</span></span></td>
<td><span data-ttu-id="45d77-685">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-685">Electricity</span></span></td>
<td><span data-ttu-id="45d77-686">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-686">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="45d77-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-688">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-689">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-689">CC002</span></span></td>
<td><span data-ttu-id="45d77-690">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-690">Finance</span></span></td>
<td><span data-ttu-id="45d77-691">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-691">10001</span></span></td>
<td><span data-ttu-id="45d77-692">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-692">Electricity</span></span></td>
<td><span data-ttu-id="45d77-693">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-693">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-694">675.00</span><span class="sxs-lookup"><span data-stu-id="45d77-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-695">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-696">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-696">CC002</span></span></td>
<td><span data-ttu-id="45d77-697">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-697">Finance</span></span></td>
<td><span data-ttu-id="45d77-698">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-698">10001</span></span></td>
<td><span data-ttu-id="45d77-699">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-699">Electricity</span></span></td>
<td><span data-ttu-id="45d77-700">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-700">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="45d77-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-702">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-703">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-703">CC003</span></span></td>
<td><span data-ttu-id="45d77-704">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-704">Assembly</span></span></td>
<td><span data-ttu-id="45d77-705">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-705">10001</span></span></td>
<td><span data-ttu-id="45d77-706">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-706">Electricity</span></span></td>
<td><span data-ttu-id="45d77-707">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-707">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-708">713.75</span><span class="sxs-lookup"><span data-stu-id="45d77-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-709">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-710">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-710">CC003</span></span></td>
<td><span data-ttu-id="45d77-711">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-711">Assembly</span></span></td>
<td><span data-ttu-id="45d77-712">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-712">10001</span></span></td>
<td><span data-ttu-id="45d77-713">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-713">Electricity</span></span></td>
<td><span data-ttu-id="45d77-714">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-714">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="45d77-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-716">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-717">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-717">CC003</span></span></td>
<td><span data-ttu-id="45d77-718">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-718">Packaging</span></span></td>
<td><span data-ttu-id="45d77-719">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-719">10001</span></span></td>
<td><span data-ttu-id="45d77-720">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-720">Electricity</span></span></td>
<td><span data-ttu-id="45d77-721">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-721">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-722">286.25</span><span class="sxs-lookup"><span data-stu-id="45d77-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-723">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-724">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-724">CC003</span></span></td>
<td><span data-ttu-id="45d77-725">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-725">Packaging</span></span></td>
<td><span data-ttu-id="45d77-726">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-726">10001</span></span></td>
<td><span data-ttu-id="45d77-727">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-727">Electricity</span></span></td>
<td><span data-ttu-id="45d77-728">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-728">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="45d77-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-730">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-731">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-731">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-732">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-732">Product 1</span></span></td>
<td><span data-ttu-id="45d77-733">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-733">10001</span></span></td>
<td><span data-ttu-id="45d77-734">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-734">Electricity</span></span></td>
<td><span data-ttu-id="45d77-735">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-735">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-736">776.36</span><span class="sxs-lookup"><span data-stu-id="45d77-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-737">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-738">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-738">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-739">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-739">Product 1</span></span></td>
<td><span data-ttu-id="45d77-740">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-740">10001</span></span></td>
<td><span data-ttu-id="45d77-741">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-741">Electricity</span></span></td>
<td><span data-ttu-id="45d77-742">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-742">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="45d77-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-744">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-745">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-745">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-746">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-746">Product 1</span></span></td>
<td><span data-ttu-id="45d77-747">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-747">10001</span></span></td>
<td><span data-ttu-id="45d77-748">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-748">Electricity</span></span></td>
<td><span data-ttu-id="45d77-749">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-749">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-750">223.64</span><span class="sxs-lookup"><span data-stu-id="45d77-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-751">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="45d77-752">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-752">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-753">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-753">Product 1</span></span></td>
<td><span data-ttu-id="45d77-754">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-754">10001</span></span></td>
<td><span data-ttu-id="45d77-755">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-755">Electricity</span></span></td>
<td><span data-ttu-id="45d77-756">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-756">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="45d77-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="45d77-758">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="45d77-759">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="45d77-760">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-760">Cost element</span></span></th>
<th><span data-ttu-id="45d77-761">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-761">Cost behavior</span></span></th>
<th><span data-ttu-id="45d77-762">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-762">Amount</span></span></th>
<th><span data-ttu-id="45d77-763">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="45d77-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="45d77-764">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-764">CC001</span></span></td>
<td><span data-ttu-id="45d77-765">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-765">HR</span></span></td>
<td><span data-ttu-id="45d77-766">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-766">10001</span></span></td>
<td><span data-ttu-id="45d77-767">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-767">Electricity</span></span></td>
<td><span data-ttu-id="45d77-768">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-768">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-769">-500.00.</span><span class="sxs-lookup"><span data-stu-id="45d77-769">-500.00</span></span></td>
<td><span data-ttu-id="45d77-770">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-771">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-771">CC002</span></span></td>
<td><span data-ttu-id="45d77-772">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-772">Finance</span></span></td>
<td><span data-ttu-id="45d77-773">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-773">10001</span></span></td>
<td><span data-ttu-id="45d77-774">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-774">Electricity</span></span></td>
<td><span data-ttu-id="45d77-775">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-775">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-776">175.00</span><span class="sxs-lookup"><span data-stu-id="45d77-776">175.00</span></span></td>
<td><span data-ttu-id="45d77-777">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-778">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-778">CC003</span></span></td>
<td><span data-ttu-id="45d77-779">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-779">Assembly</span></span></td>
<td><span data-ttu-id="45d77-780">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-780">10001</span></span></td>
<td><span data-ttu-id="45d77-781">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-781">Electricity</span></span></td>
<td><span data-ttu-id="45d77-782">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-782">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-783">275.00</span><span class="sxs-lookup"><span data-stu-id="45d77-783">275.00</span></span></td>
<td><span data-ttu-id="45d77-784">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-785">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-785">CC004</span></span></td>
<td><span data-ttu-id="45d77-786">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-786">Packaging</span></span></td>
<td><span data-ttu-id="45d77-787">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-787">10001</span></span></td>
<td><span data-ttu-id="45d77-788">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-788">Electricity</span></span></td>
<td><span data-ttu-id="45d77-789">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-789">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-790">50,00</span><span class="sxs-lookup"><span data-stu-id="45d77-790">50,00</span></span></td>
<td><span data-ttu-id="45d77-791">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-792">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-792">CC001</span></span></td>
<td><span data-ttu-id="45d77-793">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="45d77-793">HR</span></span></td>
<td><span data-ttu-id="45d77-794">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-794">10001</span></span></td>
<td><span data-ttu-id="45d77-795">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-795">Electricity</span></span></td>
<td><span data-ttu-id="45d77-796">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-796">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="45d77-797">-1,245.71</span></span></td>
<td><span data-ttu-id="45d77-798">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-799">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-799">CC002</span></span></td>
<td><span data-ttu-id="45d77-800">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-800">Finance</span></span></td>
<td><span data-ttu-id="45d77-801">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-801">10001</span></span></td>
<td><span data-ttu-id="45d77-802">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-802">Electricity</span></span></td>
<td><span data-ttu-id="45d77-803">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-803">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-804">436.00</span><span class="sxs-lookup"><span data-stu-id="45d77-804">436.00</span></span></td>
<td><span data-ttu-id="45d77-805">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-806">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-806">CC003</span></span></td>
<td><span data-ttu-id="45d77-807">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-807">Assembly</span></span></td>
<td><span data-ttu-id="45d77-808">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-808">10001</span></span></td>
<td><span data-ttu-id="45d77-809">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-809">Electricity</span></span></td>
<td><span data-ttu-id="45d77-810">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-810">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-811">685.14</span><span class="sxs-lookup"><span data-stu-id="45d77-811">685.14</span></span></td>
<td><span data-ttu-id="45d77-812">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-813">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-813">CC004</span></span></td>
<td><span data-ttu-id="45d77-814">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-814">Packaging</span></span></td>
<td><span data-ttu-id="45d77-815">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-815">10001</span></span></td>
<td><span data-ttu-id="45d77-816">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-816">Electricity</span></span></td>
<td><span data-ttu-id="45d77-817">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-817">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-818">124.57</span><span class="sxs-lookup"><span data-stu-id="45d77-818">124.57</span></span></td>
<td><span data-ttu-id="45d77-819">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-820">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-820">CC002</span></span></td>
<td><span data-ttu-id="45d77-821">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-821">Finance</span></span></td>
<td><span data-ttu-id="45d77-822">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-822">10001</span></span></td>
<td><span data-ttu-id="45d77-823">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-823">Electricity</span></span></td>
<td><span data-ttu-id="45d77-824">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-824">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="45d77-825">-675.00</span></span></td>
<td><span data-ttu-id="45d77-826">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-827">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-827">CC003</span></span></td>
<td><span data-ttu-id="45d77-828">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-828">Assembly</span></span></td>
<td><span data-ttu-id="45d77-829">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-829">10001</span></span></td>
<td><span data-ttu-id="45d77-830">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-830">Electricity</span></span></td>
<td><span data-ttu-id="45d77-831">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-831">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-832">438.75</span><span class="sxs-lookup"><span data-stu-id="45d77-832">438.75</span></span></td>
<td><span data-ttu-id="45d77-833">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-834">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-834">CC004</span></span></td>
<td><span data-ttu-id="45d77-835">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-835">Packaging</span></span></td>
<td><span data-ttu-id="45d77-836">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-836">10001</span></span></td>
<td><span data-ttu-id="45d77-837">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-837">Electricity</span></span></td>
<td><span data-ttu-id="45d77-838">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-838">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-839">236.25</span><span class="sxs-lookup"><span data-stu-id="45d77-839">236.25</span></span></td>
<td><span data-ttu-id="45d77-840">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-841">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-841">CC002</span></span></td>
<td><span data-ttu-id="45d77-842">การเงิน</span><span class="sxs-lookup"><span data-stu-id="45d77-842">Finance</span></span></td>
<td><span data-ttu-id="45d77-843">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-843">10001</span></span></td>
<td><span data-ttu-id="45d77-844">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-844">Electricity</span></span></td>
<td><span data-ttu-id="45d77-845">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-845">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="45d77-846">-8,150.29</span></span></td>
<td><span data-ttu-id="45d77-847">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-848">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-848">CC003</span></span></td>
<td><span data-ttu-id="45d77-849">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-849">Assembly</span></span></td>
<td><span data-ttu-id="45d77-850">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-850">10001</span></span></td>
<td><span data-ttu-id="45d77-851">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-851">Electricity</span></span></td>
<td><span data-ttu-id="45d77-852">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-852">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="45d77-853">5,297.69</span></span></td>
<td><span data-ttu-id="45d77-854">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-855">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-855">CC004</span></span></td>
<td><span data-ttu-id="45d77-856">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45d77-856">Packaging</span></span></td>
<td><span data-ttu-id="45d77-857">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-857">10001</span></span></td>
<td><span data-ttu-id="45d77-858">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-858">Electricity</span></span></td>
<td><span data-ttu-id="45d77-859">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-859">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="45d77-860">2,852.60</span></span></td>
<td><span data-ttu-id="45d77-861">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-862">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-862">CC003</span></span></td>
<td><span data-ttu-id="45d77-863">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-863">Assembly</span></span></td>
<td><span data-ttu-id="45d77-864">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-864">10001</span></span></td>
<td><span data-ttu-id="45d77-865">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-865">Electricity</span></span></td>
<td><span data-ttu-id="45d77-866">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-866">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="45d77-867">-713.75</span></span></td>
<td><span data-ttu-id="45d77-868">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-869">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-869">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-870">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-870">Product 1</span></span></td>
<td><span data-ttu-id="45d77-871">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-871">10001</span></span></td>
<td><span data-ttu-id="45d77-872">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-872">Electricity</span></span></td>
<td><span data-ttu-id="45d77-873">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-873">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-874">535.31</span><span class="sxs-lookup"><span data-stu-id="45d77-874">535.31</span></span></td>
<td><span data-ttu-id="45d77-875">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-876">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-876">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-877">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-877">Product 2</span></span></td>
<td><span data-ttu-id="45d77-878">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-878">10001</span></span></td>
<td><span data-ttu-id="45d77-879">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-879">Electricity</span></span></td>
<td><span data-ttu-id="45d77-880">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-880">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-881">178.44</span><span class="sxs-lookup"><span data-stu-id="45d77-881">178.44</span></span></td>
<td><span data-ttu-id="45d77-882">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-883">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-883">CC003</span></span></td>
<td><span data-ttu-id="45d77-884">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-884">Assembly</span></span></td>
<td><span data-ttu-id="45d77-885">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-885">10001</span></span></td>
<td><span data-ttu-id="45d77-886">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-886">Electricity</span></span></td>
<td><span data-ttu-id="45d77-887">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-887">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="45d77-888">-5,982.83</span></span></td>
<td><span data-ttu-id="45d77-889">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-890">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-890">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-891">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-891">Product 1</span></span></td>
<td><span data-ttu-id="45d77-892">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-892">10001</span></span></td>
<td><span data-ttu-id="45d77-893">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-893">Electricity</span></span></td>
<td><span data-ttu-id="45d77-894">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-894">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="45d77-895">4,487.12</span></span></td>
<td><span data-ttu-id="45d77-896">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-897">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-897">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-898">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-898">Product 2</span></span></td>
<td><span data-ttu-id="45d77-899">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-899">10001</span></span></td>
<td><span data-ttu-id="45d77-900">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-900">Electricity</span></span></td>
<td><span data-ttu-id="45d77-901">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-901">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="45d77-902">1,495.71</span></span></td>
<td><span data-ttu-id="45d77-903">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-904">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-904">CC003</span></span></td>
<td><span data-ttu-id="45d77-905">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-905">Assembly</span></span></td>
<td><span data-ttu-id="45d77-906">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-906">10001</span></span></td>
<td><span data-ttu-id="45d77-907">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-907">Electricity</span></span></td>
<td><span data-ttu-id="45d77-908">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-908">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="45d77-909">-286.25</span></span></td>
<td><span data-ttu-id="45d77-910">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-911">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-911">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-912">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-912">Product 1</span></span></td>
<td><span data-ttu-id="45d77-913">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-913">10001</span></span></td>
<td><span data-ttu-id="45d77-914">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-914">Electricity</span></span></td>
<td><span data-ttu-id="45d77-915">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-915">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-916">241.05</span><span class="sxs-lookup"><span data-stu-id="45d77-916">241.05</span></span></td>
<td><span data-ttu-id="45d77-917">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-918">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-918">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-919">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-919">Product 2</span></span></td>
<td><span data-ttu-id="45d77-920">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-920">10001</span></span></td>
<td><span data-ttu-id="45d77-921">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-921">Electricity</span></span></td>
<td><span data-ttu-id="45d77-922">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-922">Fixed cost</span></span></td>
<td><span data-ttu-id="45d77-923">45.20</span><span class="sxs-lookup"><span data-stu-id="45d77-923">45.20</span></span></td>
<td><span data-ttu-id="45d77-924">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-925">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-925">CC003</span></span></td>
<td><span data-ttu-id="45d77-926">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="45d77-926">Assembly</span></span></td>
<td><span data-ttu-id="45d77-927">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-927">10001</span></span></td>
<td><span data-ttu-id="45d77-928">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-928">Electricity</span></span></td>
<td><span data-ttu-id="45d77-929">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-929">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="45d77-930">-2,977.17</span></span></td>
<td><span data-ttu-id="45d77-931">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-932">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-932">Prod 1</span></span></td>
<td><span data-ttu-id="45d77-933">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-933">Product 1</span></span></td>
<td><span data-ttu-id="45d77-934">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-934">10001</span></span></td>
<td><span data-ttu-id="45d77-935">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-935">Electricity</span></span></td>
<td><span data-ttu-id="45d77-936">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-936">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="45d77-937">2,507.09</span></span></td>
<td><span data-ttu-id="45d77-938">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="45d77-939">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-939">Prod 2</span></span></td>
<td><span data-ttu-id="45d77-940">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-940">Product 2</span></span></td>
<td><span data-ttu-id="45d77-941">10001</span><span class="sxs-lookup"><span data-stu-id="45d77-941">10001</span></span></td>
<td><span data-ttu-id="45d77-942">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-942">Electricity</span></span></td>
<td><span data-ttu-id="45d77-943">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-943">Variable cost</span></span></td>
<td><span data-ttu-id="45d77-944">470.08</span><span class="sxs-lookup"><span data-stu-id="45d77-944">470.08</span></span></td>
<td><span data-ttu-id="45d77-945">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="45d77-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="45d77-946">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="45d77-946">Conclusion</span></span>
<span data-ttu-id="45d77-947">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="45d77-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="45d77-948">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="45d77-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="45d77-949">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="45d77-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="45d77-950">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="45d77-951">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="45d77-952">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="45d77-953">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="45d77-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="45d77-954">CC099</span><span class="sxs-lookup"><span data-stu-id="45d77-954">CC099</span></span></th>
<th><span data-ttu-id="45d77-955">CC001</span><span class="sxs-lookup"><span data-stu-id="45d77-955">CC001</span></span></th>
<th><span data-ttu-id="45d77-956">CC002</span><span class="sxs-lookup"><span data-stu-id="45d77-956">CC002</span></span></th>
<th><span data-ttu-id="45d77-957">CC003</span><span class="sxs-lookup"><span data-stu-id="45d77-957">CC003</span></span></th>
<th><span data-ttu-id="45d77-958">CC004</span><span class="sxs-lookup"><span data-stu-id="45d77-958">CC004</span></span></th>
<th><span data-ttu-id="45d77-959">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-959">Proj 1</span></span></th>
<th><span data-ttu-id="45d77-960">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-960">Proj 2</span></span></th>
<th><span data-ttu-id="45d77-961">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="45d77-961">Prod 1</span></span></th>
<th><span data-ttu-id="45d77-962">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="45d77-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="45d77-963">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="45d77-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="45d77-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="45d77-973">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="45d77-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-974">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="45d77-975">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="45d77-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-976">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-977">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-978">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-979">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-980">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="45d77-981">776.36</span><span class="sxs-lookup"><span data-stu-id="45d77-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-982">223.64</span><span class="sxs-lookup"><span data-stu-id="45d77-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="45d77-984">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="45d77-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-985">000</span><span class="sxs-lookup"><span data-stu-id="45d77-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-986">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-987">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-988">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-989">0.00</span><span class="sxs-lookup"><span data-stu-id="45d77-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-990">30.00</span><span class="sxs-lookup"><span data-stu-id="45d77-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-991">10.00</span><span class="sxs-lookup"><span data-stu-id="45d77-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="45d77-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="45d77-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="45d77-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="45d77-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="45d77-995">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="45d77-996">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="45d77-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="45d77-997">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="45d77-998">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="45d77-999">สำหรับข้อมูลเพิ่มเติม ให้ดูที่นโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="45d77-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="45d77-1000">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="45d77-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




