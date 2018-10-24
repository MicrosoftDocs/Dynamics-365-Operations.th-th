---
title: "การคำนวณค่าโสหุ้ย"
description: "หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย"
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: th-th
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="afddf-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="afddf-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afddf-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="afddf-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="afddf-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="afddf-105">Term definition</span></span>
---------------

<span data-ttu-id="afddf-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="afddf-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="afddf-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="afddf-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="afddf-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="afddf-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="afddf-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="afddf-109">Rent</span></span>
-   <span data-ttu-id="afddf-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-110">Electricity</span></span>
-   <span data-ttu-id="afddf-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="afddf-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="afddf-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="afddf-112">Overhead calculation overview</span></span>
<span data-ttu-id="afddf-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="afddf-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="afddf-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="afddf-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="afddf-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="afddf-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="afddf-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="afddf-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="afddf-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="afddf-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="afddf-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="afddf-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="afddf-119">Version type</span></span>
-   <span data-ttu-id="afddf-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="afddf-120">Date and time</span></span>
-   <span data-ttu-id="afddf-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="afddf-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-122">Fiscal year</span></span>
-   <span data-ttu-id="afddf-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-123">Fiscal period</span></span>

<span data-ttu-id="afddf-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="afddf-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="afddf-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="afddf-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="afddf-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afddf-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="afddf-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="afddf-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="afddf-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="afddf-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="afddf-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="afddf-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="afddf-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="afddf-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="afddf-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="afddf-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="afddf-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="afddf-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="afddf-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="afddf-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="afddf-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="afddf-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="afddf-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="afddf-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afddf-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="afddf-140">Main account</span></span></th>
<th><span data-ttu-id="afddf-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="afddf-143">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-143">CC099</span></span></td>
<td><span data-ttu-id="afddf-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-144">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-145">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-145">10001</span></span></td>
<td><span data-ttu-id="afddf-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-146">Electricity</span></span></td>
<td><span data-ttu-id="afddf-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="afddf-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="afddf-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="afddf-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="afddf-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="afddf-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-151">Define the cost behavior rule</span></span>

<span data-ttu-id="afddf-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="afddf-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="afddf-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="afddf-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="afddf-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="afddf-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="afddf-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="afddf-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="afddf-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="afddf-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="afddf-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="afddf-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-160">Journal</span></span></th>
<th><span data-ttu-id="afddf-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="afddf-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="afddf-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="afddf-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-164">00001</span><span class="sxs-lookup"><span data-stu-id="afddf-164">00001</span></span></td>
<td><span data-ttu-id="afddf-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="afddf-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-166">Fiscal</span></span></td>
<td><span data-ttu-id="afddf-167">2017</span><span class="sxs-lookup"><span data-stu-id="afddf-167">2017</span></span></td>
<td><span data-ttu-id="afddf-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-168">Period 1</span></span></td>
<td><span data-ttu-id="afddf-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="afddf-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="afddf-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-173">Cost element</span></span></th>
<th><span data-ttu-id="afddf-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-174">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="afddf-177">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-177">CC099</span></span></td>
<td><span data-ttu-id="afddf-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-178">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-179">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-179">10001</span></span></td>
<td><span data-ttu-id="afddf-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-180">Electricity</span></span></td>
<td><span data-ttu-id="afddf-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="afddf-181">Unclassified</span></span></td>
<td><span data-ttu-id="afddf-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="afddf-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-185">Cost element</span></span></th>
<th><span data-ttu-id="afddf-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-186">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-187">Amount</span></span></th>
<th><span data-ttu-id="afddf-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-189">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-189">CC099</span></span></td>
<td><span data-ttu-id="afddf-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-190">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-191">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-191">10001</span></span></td>
<td><span data-ttu-id="afddf-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-192">Electricity</span></span></td>
<td><span data-ttu-id="afddf-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="afddf-193">Unclassified</span></span></td>
<td><span data-ttu-id="afddf-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-194">10,000.00</span></span></td>
<td><span data-ttu-id="afddf-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-196">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-196">CC099</span></span></td>
<td><span data-ttu-id="afddf-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-197">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-198">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-198">10001</span></span></td>
<td><span data-ttu-id="afddf-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-199">Electricity</span></span></td>
<td><span data-ttu-id="afddf-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="afddf-200">Unclassified</span></span></td>
<td><span data-ttu-id="afddf-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-201">-10,000.00</span></span></td>
<td><span data-ttu-id="afddf-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-203">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-203">CC099</span></span></td>
<td><span data-ttu-id="afddf-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-204">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-205">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-205">10001</span></span></td>
<td><span data-ttu-id="afddf-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-206">Electricity</span></span></td>
<td><span data-ttu-id="afddf-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-207">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-208">1,000.00</span></span></td>
<td><span data-ttu-id="afddf-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-210">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-210">CC099</span></span></td>
<td><span data-ttu-id="afddf-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-211">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-212">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-212">10001</span></span></td>
<td><span data-ttu-id="afddf-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-213">Electricity</span></span></td>
<td><span data-ttu-id="afddf-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-214">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-215">9,000.00</span></span></td>
<td><span data-ttu-id="afddf-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="afddf-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="afddf-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="afddf-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="afddf-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="afddf-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="afddf-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="afddf-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-221">Define the cost distribution rule</span></span>

<span data-ttu-id="afddf-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="afddf-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="afddf-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="afddf-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="afddf-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="afddf-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="afddf-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="afddf-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="afddf-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="afddf-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-228">Cost object</span></span></th>
<th><span data-ttu-id="afddf-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="afddf-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-230">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-230">CC001</span></span></td>
<td><span data-ttu-id="afddf-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-231">HR</span></span></td>
<td><span data-ttu-id="afddf-232">1,000</span><span class="sxs-lookup"><span data-stu-id="afddf-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-233">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-233">CC002</span></span></td>
<td><span data-ttu-id="afddf-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-234">Finance</span></span></td>
<td><span data-ttu-id="afddf-235">6,000</span><span class="sxs-lookup"><span data-stu-id="afddf-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-236">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-236">CC003</span></span></td>
<td><span data-ttu-id="afddf-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-237">Assembly</span></span></td>
<td><span data-ttu-id="afddf-238">0</span><span class="sxs-lookup"><span data-stu-id="afddf-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-240">Cost object</span></span></th>
<th><span data-ttu-id="afddf-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-241">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-242">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-244">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-244">CC001</span></span></td>
<td><span data-ttu-id="afddf-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-245">HR</span></span></td>
<td><span data-ttu-id="afddf-246">1,000</span><span class="sxs-lookup"><span data-stu-id="afddf-246">1,000</span></span></td>
<td><span data-ttu-id="afddf-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="afddf-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="afddf-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-249">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-249">CC002</span></span></td>
<td><span data-ttu-id="afddf-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-250">Finance</span></span></td>
<td><span data-ttu-id="afddf-251">6,000</span><span class="sxs-lookup"><span data-stu-id="afddf-251">6,000</span></span></td>
<td><span data-ttu-id="afddf-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="afddf-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="afddf-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-254">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-254">CC003</span></span></td>
<td><span data-ttu-id="afddf-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-255">Assembly</span></span></td>
<td><span data-ttu-id="afddf-256">0</span><span class="sxs-lookup"><span data-stu-id="afddf-256">0</span></span></td>
<td><span data-ttu-id="afddf-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="afddf-258">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="afddf-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-261">Cost object</span></span></th>
<th><span data-ttu-id="afddf-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="afddf-262">Formula</span></span></th>
<th><span data-ttu-id="afddf-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-263">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-264">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-266">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-266">CC001</span></span></td>
<td><span data-ttu-id="afddf-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-267">HR</span></span></td>
<td><span data-ttu-id="afddf-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="afddf-269">1</span><span class="sxs-lookup"><span data-stu-id="afddf-269">1</span></span></td>
<td><span data-ttu-id="afddf-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="afddf-271">500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-272">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-272">CC002</span></span></td>
<td><span data-ttu-id="afddf-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-273">Finance</span></span></td>
<td><span data-ttu-id="afddf-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="afddf-275">1</span><span class="sxs-lookup"><span data-stu-id="afddf-275">1</span></span></td>
<td><span data-ttu-id="afddf-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="afddf-277">500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-278">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-278">CC003</span></span></td>
<td><span data-ttu-id="afddf-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-279">Assembly</span></span></td>
<td><span data-ttu-id="afddf-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="afddf-281">0</span><span class="sxs-lookup"><span data-stu-id="afddf-281">0</span></span></td>
<td><span data-ttu-id="afddf-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="afddf-283">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="afddf-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-285">Journal</span></span></th>
<th><span data-ttu-id="afddf-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="afddf-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="afddf-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="afddf-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-289">00002</span><span class="sxs-lookup"><span data-stu-id="afddf-289">00002</span></span></td>
<td><span data-ttu-id="afddf-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="afddf-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-291">Fiscal</span></span></td>
<td><span data-ttu-id="afddf-292">2017</span><span class="sxs-lookup"><span data-stu-id="afddf-292">2017</span></span></td>
<td><span data-ttu-id="afddf-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-293">Period 1</span></span></td>
<td><span data-ttu-id="afddf-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="afddf-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="afddf-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-298">Cost element</span></span></th>
<th><span data-ttu-id="afddf-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-299">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-302">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-302">CC099</span></span></td>
<td><span data-ttu-id="afddf-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-303">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-304">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-304">10001</span></span></td>
<td><span data-ttu-id="afddf-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-305">Electricity</span></span></td>
<td><span data-ttu-id="afddf-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-306">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-309">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-309">CC099</span></span></td>
<td><span data-ttu-id="afddf-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-310">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-311">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-311">10001</span></span></td>
<td><span data-ttu-id="afddf-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-312">Electricity</span></span></td>
<td><span data-ttu-id="afddf-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-313">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="afddf-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-317">Cost element</span></span></th>
<th><span data-ttu-id="afddf-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-318">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-319">Amount</span></span></th>
<th><span data-ttu-id="afddf-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-321">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-321">CC099</span></span></td>
<td><span data-ttu-id="afddf-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-322">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-323">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-323">10001</span></span></td>
<td><span data-ttu-id="afddf-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-324">Electricity</span></span></td>
<td><span data-ttu-id="afddf-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-325">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="afddf-326">-1,000.00</span></span></td>
<td><span data-ttu-id="afddf-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-328">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-328">CC001</span></span></td>
<td><span data-ttu-id="afddf-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-329">HR</span></span></td>
<td><span data-ttu-id="afddf-330">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-330">10001</span></span></td>
<td><span data-ttu-id="afddf-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-331">Electricity</span></span></td>
<td><span data-ttu-id="afddf-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-332">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-333">500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-333">500.00</span></span></td>
<td><span data-ttu-id="afddf-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-335">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-335">CC002</span></span></td>
<td><span data-ttu-id="afddf-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-336">Finance</span></span></td>
<td><span data-ttu-id="afddf-337">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-337">10001</span></span></td>
<td><span data-ttu-id="afddf-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-338">Electricity</span></span></td>
<td><span data-ttu-id="afddf-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-339">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-340">500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-340">500.00</span></span></td>
<td><span data-ttu-id="afddf-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-342">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-342">CC099</span></span></td>
<td><span data-ttu-id="afddf-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afddf-343">Default cost center</span></span></td>
<td><span data-ttu-id="afddf-344">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-344">10001</span></span></td>
<td><span data-ttu-id="afddf-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-345">Electricity</span></span></td>
<td><span data-ttu-id="afddf-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-346">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="afddf-347">-9,000.00</span></span></td>
<td><span data-ttu-id="afddf-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-349">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-349">CC001</span></span></td>
<td><span data-ttu-id="afddf-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-350">HR</span></span></td>
<td><span data-ttu-id="afddf-351">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-351">10001</span></span></td>
<td><span data-ttu-id="afddf-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-352">Electricity</span></span></td>
<td><span data-ttu-id="afddf-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-353">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="afddf-354">1,285.71</span></span></td>
<td><span data-ttu-id="afddf-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-356">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-356">CC002</span></span></td>
<td><span data-ttu-id="afddf-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-357">Finance</span></span></td>
<td><span data-ttu-id="afddf-358">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-358">10001</span></span></td>
<td><span data-ttu-id="afddf-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-359">Electricity</span></span></td>
<td><span data-ttu-id="afddf-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-360">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="afddf-361">7,714.29</span></span></td>
<td><span data-ttu-id="afddf-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="afddf-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="afddf-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="afddf-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="afddf-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="afddf-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="afddf-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="afddf-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="afddf-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="afddf-367">Define the overhead rate</span></span>

<span data-ttu-id="afddf-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="afddf-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="afddf-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="afddf-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-370">Cost object</span></span></th>
<th><span data-ttu-id="afddf-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="afddf-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-372">Proj 1</span></span></td>
<td><span data-ttu-id="afddf-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-373">Project 1</span></span></td>
<td><span data-ttu-id="afddf-374">3</span><span class="sxs-lookup"><span data-stu-id="afddf-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-375">Proj 2</span></span></td>
<td><span data-ttu-id="afddf-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-376">Project 2</span></span></td>
<td><span data-ttu-id="afddf-377">1</span><span class="sxs-lookup"><span data-stu-id="afddf-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-379">Cost object</span></span></th>
<th><span data-ttu-id="afddf-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-380">Cost element</span></span></th>
<th><span data-ttu-id="afddf-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-381">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="afddf-382">Units</span></span></th>
<th><span data-ttu-id="afddf-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="afddf-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-384">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-384">CC001</span></span></td>
<td><span data-ttu-id="afddf-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-385">HR</span></span></td>
<td><span data-ttu-id="afddf-386">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-386">10001</span></span></td>
<td><span data-ttu-id="afddf-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-387">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-388">1</span><span class="sxs-lookup"><span data-stu-id="afddf-388">1</span></span></td>
<td><span data-ttu-id="afddf-389">10</span><span class="sxs-lookup"><span data-stu-id="afddf-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-391">Cost object</span></span></th>
<th><span data-ttu-id="afddf-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-392">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-393">Cost element</span></span></th>
<th><span data-ttu-id="afddf-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-394">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-396">Proj 1</span></span></td>
<td><span data-ttu-id="afddf-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-397">Project 1</span></span></td>
<td><span data-ttu-id="afddf-398">3</span><span class="sxs-lookup"><span data-stu-id="afddf-398">3</span></span></td>
<td><span data-ttu-id="afddf-399">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-399">10001</span></span></td>
<td><span data-ttu-id="afddf-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="afddf-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="afddf-401">30.00</span><span class="sxs-lookup"><span data-stu-id="afddf-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-402">Proj 2</span></span></td>
<td><span data-ttu-id="afddf-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-403">Project 2</span></span></td>
<td><span data-ttu-id="afddf-404">1</span><span class="sxs-lookup"><span data-stu-id="afddf-404">1</span></span></td>
<td><span data-ttu-id="afddf-405">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-405">10001</span></span></td>
<td><span data-ttu-id="afddf-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="afddf-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="afddf-407">10.00</span><span class="sxs-lookup"><span data-stu-id="afddf-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="afddf-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-409">Journal</span></span></th>
<th><span data-ttu-id="afddf-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="afddf-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="afddf-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="afddf-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-413">00003</span><span class="sxs-lookup"><span data-stu-id="afddf-413">00003</span></span></td>
<td><span data-ttu-id="afddf-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="afddf-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="afddf-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-415">Fiscal</span></span></td>
<td><span data-ttu-id="afddf-416">2017</span><span class="sxs-lookup"><span data-stu-id="afddf-416">2017</span></span></td>
<td><span data-ttu-id="afddf-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-417">Period 1</span></span></td>
<td><span data-ttu-id="afddf-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="afddf-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="afddf-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-421">Cost object</span></span></th>
<th><span data-ttu-id="afddf-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-424">Proj 1</span></span></td>
<td><span data-ttu-id="afddf-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="afddf-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="afddf-426">3.00</span><span class="sxs-lookup"><span data-stu-id="afddf-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-428">Proj 2</span></span></td>
<td><span data-ttu-id="afddf-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="afddf-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="afddf-430">1.00</span><span class="sxs-lookup"><span data-stu-id="afddf-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="afddf-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-433">Cost element</span></span></th>
<th><span data-ttu-id="afddf-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-434">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-435">Amount</span></span></th>
<th><span data-ttu-id="afddf-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="afddf-437">CC0001</span></span></td>
<td><span data-ttu-id="afddf-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-438">HR</span></span></td>
<td><span data-ttu-id="afddf-439">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-439">10001</span></span></td>
<td><span data-ttu-id="afddf-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-440">Electricity</span></span></td>
<td><span data-ttu-id="afddf-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-441">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="afddf-442">-30.00</span></span></td>
<td><span data-ttu-id="afddf-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-444">Proj 1</span></span></td>
<td><span data-ttu-id="afddf-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="afddf-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="afddf-446">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-446">10001</span></span></td>
<td><span data-ttu-id="afddf-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-447">Electricity</span></span></td>
<td><span data-ttu-id="afddf-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-448">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-449">30.00</span><span class="sxs-lookup"><span data-stu-id="afddf-449">30.00</span></span></td>
<td><span data-ttu-id="afddf-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-451">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-451">CC001</span></span></td>
<td><span data-ttu-id="afddf-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-452">HR</span></span></td>
<td><span data-ttu-id="afddf-453">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-453">10001</span></span></td>
<td><span data-ttu-id="afddf-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-454">Electricity</span></span></td>
<td><span data-ttu-id="afddf-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-455">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="afddf-456">-10.00</span></span></td>
<td><span data-ttu-id="afddf-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-458">Proj 2</span></span></td>
<td><span data-ttu-id="afddf-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="afddf-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="afddf-460">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-460">10001</span></span></td>
<td><span data-ttu-id="afddf-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-461">Electricity</span></span></td>
<td><span data-ttu-id="afddf-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-462">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-463">10.00</span><span class="sxs-lookup"><span data-stu-id="afddf-463">10.00</span></span></td>
<td><span data-ttu-id="afddf-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="afddf-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="afddf-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="afddf-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="afddf-468">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="afddf-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="afddf-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="afddf-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="afddf-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="afddf-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="afddf-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="afddf-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="afddf-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="afddf-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="afddf-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="afddf-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="afddf-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="afddf-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-475">Define the cost allocation</span></span>

<span data-ttu-id="afddf-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="afddf-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="afddf-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="afddf-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="afddf-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-479">Cost object</span></span></th>
<th><span data-ttu-id="afddf-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="afddf-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-481">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-481">CC002</span></span></td>
<td><span data-ttu-id="afddf-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-482">Finance</span></span></td>
<td><span data-ttu-id="afddf-483">35</span><span class="sxs-lookup"><span data-stu-id="afddf-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-484">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-484">CC003</span></span></td>
<td><span data-ttu-id="afddf-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-485">Assembly</span></span></td>
<td><span data-ttu-id="afddf-486">55</span><span class="sxs-lookup"><span data-stu-id="afddf-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-487">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-487">CC004</span></span></td>
<td><span data-ttu-id="afddf-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-488">Packaging</span></span></td>
<td><span data-ttu-id="afddf-489">10</span><span class="sxs-lookup"><span data-stu-id="afddf-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="afddf-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="afddf-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="afddf-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-492">Cost object</span></span></th>
<th><span data-ttu-id="afddf-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-494">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-494">CC003</span></span></td>
<td><span data-ttu-id="afddf-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-495">Assembly</span></span></td>
<td><span data-ttu-id="afddf-496">65</span><span class="sxs-lookup"><span data-stu-id="afddf-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-497">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-497">CC004</span></span></td>
<td><span data-ttu-id="afddf-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-498">Packaging</span></span></td>
<td><span data-ttu-id="afddf-499">35</span><span class="sxs-lookup"><span data-stu-id="afddf-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="afddf-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="afddf-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="afddf-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-502">Cost object</span></span></th>
<th><span data-ttu-id="afddf-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="afddf-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-504">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-505">Product 1</span></span></td>
<td><span data-ttu-id="afddf-506">60</span><span class="sxs-lookup"><span data-stu-id="afddf-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-507">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-508">Product 2</span></span></td>
<td><span data-ttu-id="afddf-509">20</span><span class="sxs-lookup"><span data-stu-id="afddf-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="afddf-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="afddf-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="afddf-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-512">Cost object</span></span></th>
<th><span data-ttu-id="afddf-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="afddf-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-514">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-515">Product 1</span></span></td>
<td><span data-ttu-id="afddf-516">80</span><span class="sxs-lookup"><span data-stu-id="afddf-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-517">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-518">Product 2</span></span></td>
<td><span data-ttu-id="afddf-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="afddf-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="afddf-520">ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้ สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afddf-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="afddf-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="afddf-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="afddf-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="afddf-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-523">Cost object</span></span></th>
<th><span data-ttu-id="afddf-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-524">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-525">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-526">Amount</span></span></th>
<th><span data-ttu-id="afddf-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-528">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-528">CC002</span></span></td>
<td><span data-ttu-id="afddf-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-529">Finance</span></span></td>
<td><span data-ttu-id="afddf-530">35</span><span class="sxs-lookup"><span data-stu-id="afddf-530">35</span></span></td>
<td><span data-ttu-id="afddf-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="afddf-532">175.00</span><span class="sxs-lookup"><span data-stu-id="afddf-532">175.00</span></span></td>
<td><span data-ttu-id="afddf-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-534">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-534">CC003</span></span></td>
<td><span data-ttu-id="afddf-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-535">Assembly</span></span></td>
<td><span data-ttu-id="afddf-536">55</span><span class="sxs-lookup"><span data-stu-id="afddf-536">55</span></span></td>
<td><span data-ttu-id="afddf-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="afddf-538">275.00</span><span class="sxs-lookup"><span data-stu-id="afddf-538">275.00</span></span></td>
<td><span data-ttu-id="afddf-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-540">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-540">CC004</span></span></td>
<td><span data-ttu-id="afddf-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-541">Packaging</span></span></td>
<td><span data-ttu-id="afddf-542">10</span><span class="sxs-lookup"><span data-stu-id="afddf-542">10</span></span></td>
<td><span data-ttu-id="afddf-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="afddf-544">50.00</span><span class="sxs-lookup"><span data-stu-id="afddf-544">50.00</span></span></td>
<td><span data-ttu-id="afddf-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-546">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-546">CC002</span></span></td>
<td><span data-ttu-id="afddf-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-547">Finance</span></span></td>
<td><span data-ttu-id="afddf-548">35</span><span class="sxs-lookup"><span data-stu-id="afddf-548">35</span></span></td>
<td><span data-ttu-id="afddf-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="afddf-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="afddf-550">436.00</span><span class="sxs-lookup"><span data-stu-id="afddf-550">436.00</span></span></td>
<td><span data-ttu-id="afddf-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-552">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-552">CC003</span></span></td>
<td><span data-ttu-id="afddf-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-553">Assembly</span></span></td>
<td><span data-ttu-id="afddf-554">55</span><span class="sxs-lookup"><span data-stu-id="afddf-554">55</span></span></td>
<td><span data-ttu-id="afddf-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="afddf-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="afddf-556">685.14</span><span class="sxs-lookup"><span data-stu-id="afddf-556">685.14</span></span></td>
<td><span data-ttu-id="afddf-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-558">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-558">CC004</span></span></td>
<td><span data-ttu-id="afddf-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-559">Packaging</span></span></td>
<td><span data-ttu-id="afddf-560">10</span><span class="sxs-lookup"><span data-stu-id="afddf-560">10</span></span></td>
<td><span data-ttu-id="afddf-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="afddf-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="afddf-562">124.57</span><span class="sxs-lookup"><span data-stu-id="afddf-562">124.57</span></span></td>
<td><span data-ttu-id="afddf-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="afddf-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-565">Cost object</span></span></th>
<th><span data-ttu-id="afddf-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-566">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-567">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-568">Amount</span></span></th>
<th><span data-ttu-id="afddf-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-570">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-570">CC003</span></span></td>
<td><span data-ttu-id="afddf-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-571">Assembly</span></span></td>
<td><span data-ttu-id="afddf-572">65</span><span class="sxs-lookup"><span data-stu-id="afddf-572">65</span></span></td>
<td><span data-ttu-id="afddf-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="afddf-574">438.75</span><span class="sxs-lookup"><span data-stu-id="afddf-574">438.75</span></span></td>
<td><span data-ttu-id="afddf-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-576">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-576">CC004</span></span></td>
<td><span data-ttu-id="afddf-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-577">Packaging</span></span></td>
<td><span data-ttu-id="afddf-578">35</span><span class="sxs-lookup"><span data-stu-id="afddf-578">35</span></span></td>
<td><span data-ttu-id="afddf-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="afddf-580">236.25</span><span class="sxs-lookup"><span data-stu-id="afddf-580">236.25</span></span></td>
<td><span data-ttu-id="afddf-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-582">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-582">CC003</span></span></td>
<td><span data-ttu-id="afddf-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-583">Assembly</span></span></td>
<td><span data-ttu-id="afddf-584">65</span><span class="sxs-lookup"><span data-stu-id="afddf-584">65</span></span></td>
<td><span data-ttu-id="afddf-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="afddf-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="afddf-586">5,297.69</span></span></td>
<td><span data-ttu-id="afddf-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-588">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-588">CC004</span></span></td>
<td><span data-ttu-id="afddf-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-589">Packaging</span></span></td>
<td><span data-ttu-id="afddf-590">35</span><span class="sxs-lookup"><span data-stu-id="afddf-590">35</span></span></td>
<td><span data-ttu-id="afddf-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="afddf-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="afddf-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="afddf-592">2,852.60</span></span></td>
<td><span data-ttu-id="afddf-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="afddf-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-595">Cost object</span></span></th>
<th><span data-ttu-id="afddf-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-596">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-597">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-598">Amount</span></span></th>
<th><span data-ttu-id="afddf-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-600">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-601">Product 1</span></span></td>
<td><span data-ttu-id="afddf-602">60</span><span class="sxs-lookup"><span data-stu-id="afddf-602">60</span></span></td>
<td><span data-ttu-id="afddf-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="afddf-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="afddf-604">535.31</span><span class="sxs-lookup"><span data-stu-id="afddf-604">535.31</span></span></td>
<td><span data-ttu-id="afddf-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-606">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-607">Product 2</span></span></td>
<td><span data-ttu-id="afddf-608">20</span><span class="sxs-lookup"><span data-stu-id="afddf-608">20</span></span></td>
<td><span data-ttu-id="afddf-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="afddf-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="afddf-610">178.44</span><span class="sxs-lookup"><span data-stu-id="afddf-610">178.44</span></span></td>
<td><span data-ttu-id="afddf-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-612">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-613">Product 1</span></span></td>
<td><span data-ttu-id="afddf-614">60</span><span class="sxs-lookup"><span data-stu-id="afddf-614">60</span></span></td>
<td><span data-ttu-id="afddf-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="afddf-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="afddf-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="afddf-616">4,487.12</span></span></td>
<td><span data-ttu-id="afddf-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-618">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-619">Product 2</span></span></td>
<td><span data-ttu-id="afddf-620">20</span><span class="sxs-lookup"><span data-stu-id="afddf-620">20</span></span></td>
<td><span data-ttu-id="afddf-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="afddf-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="afddf-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="afddf-622">1,495.71</span></span></td>
<td><span data-ttu-id="afddf-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="afddf-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="afddf-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-625">Cost object</span></span></th>
<th><span data-ttu-id="afddf-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="afddf-626">Magnitude</span></span></th>
<th><span data-ttu-id="afddf-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="afddf-627">Allocation factor</span></span></th>
<th><span data-ttu-id="afddf-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-628">Amount</span></span></th>
<th><span data-ttu-id="afddf-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-630">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-631">Product 1</span></span></td>
<td><span data-ttu-id="afddf-632">80</span><span class="sxs-lookup"><span data-stu-id="afddf-632">80</span></span></td>
<td><span data-ttu-id="afddf-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="afddf-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="afddf-634">241.05</span><span class="sxs-lookup"><span data-stu-id="afddf-634">241.05</span></span></td>
<td><span data-ttu-id="afddf-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-636">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-637">Product 2</span></span></td>
<td><span data-ttu-id="afddf-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="afddf-638">15</span></span></td>
<td><span data-ttu-id="afddf-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="afddf-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="afddf-640">45.20</span><span class="sxs-lookup"><span data-stu-id="afddf-640">45.20</span></span></td>
<td><span data-ttu-id="afddf-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-642">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-643">Product 1</span></span></td>
<td><span data-ttu-id="afddf-644">80</span><span class="sxs-lookup"><span data-stu-id="afddf-644">80</span></span></td>
<td><span data-ttu-id="afddf-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="afddf-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="afddf-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="afddf-646">2,507.09</span></span></td>
<td><span data-ttu-id="afddf-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-648">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-649">Product 2</span></span></td>
<td><span data-ttu-id="afddf-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="afddf-650">15</span></span></td>
<td><span data-ttu-id="afddf-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="afddf-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="afddf-652">470.08</span><span class="sxs-lookup"><span data-stu-id="afddf-652">470.08</span></span></td>
<td><span data-ttu-id="afddf-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="afddf-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="afddf-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-655">Journal</span></span></th>
<th><span data-ttu-id="afddf-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="afddf-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="afddf-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="afddf-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-659">00004</span><span class="sxs-lookup"><span data-stu-id="afddf-659">00004</span></span></td>
<td><span data-ttu-id="afddf-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="afddf-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-661">Fiscal</span></span></td>
<td><span data-ttu-id="afddf-662">2017</span><span class="sxs-lookup"><span data-stu-id="afddf-662">2017</span></span></td>
<td><span data-ttu-id="afddf-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-663">Period 1</span></span></td>
<td><span data-ttu-id="afddf-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="afddf-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="afddf-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afddf-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="afddf-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-668">Cost element</span></span></th>
<th><span data-ttu-id="afddf-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-669">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-672">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-672">CC001</span></span></td>
<td><span data-ttu-id="afddf-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-673">HR</span></span></td>
<td><span data-ttu-id="afddf-674">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-674">10001</span></span></td>
<td><span data-ttu-id="afddf-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-675">Electricity</span></span></td>
<td><span data-ttu-id="afddf-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-676">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-677">500.00</span><span class="sxs-lookup"><span data-stu-id="afddf-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-679">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-679">CC001</span></span></td>
<td><span data-ttu-id="afddf-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-680">HR</span></span></td>
<td><span data-ttu-id="afddf-681">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-681">10001</span></span></td>
<td><span data-ttu-id="afddf-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-682">Electricity</span></span></td>
<td><span data-ttu-id="afddf-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-683">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="afddf-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-686">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-686">CC002</span></span></td>
<td><span data-ttu-id="afddf-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-687">Finance</span></span></td>
<td><span data-ttu-id="afddf-688">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-688">10001</span></span></td>
<td><span data-ttu-id="afddf-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-689">Electricity</span></span></td>
<td><span data-ttu-id="afddf-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-690">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-691">675.00</span><span class="sxs-lookup"><span data-stu-id="afddf-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-693">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-693">CC002</span></span></td>
<td><span data-ttu-id="afddf-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-694">Finance</span></span></td>
<td><span data-ttu-id="afddf-695">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-695">10001</span></span></td>
<td><span data-ttu-id="afddf-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-696">Electricity</span></span></td>
<td><span data-ttu-id="afddf-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-697">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="afddf-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-700">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-700">CC003</span></span></td>
<td><span data-ttu-id="afddf-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-701">Assembly</span></span></td>
<td><span data-ttu-id="afddf-702">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-702">10001</span></span></td>
<td><span data-ttu-id="afddf-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-703">Electricity</span></span></td>
<td><span data-ttu-id="afddf-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-704">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-705">713.75</span><span class="sxs-lookup"><span data-stu-id="afddf-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-707">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-707">CC003</span></span></td>
<td><span data-ttu-id="afddf-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-708">Assembly</span></span></td>
<td><span data-ttu-id="afddf-709">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-709">10001</span></span></td>
<td><span data-ttu-id="afddf-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-710">Electricity</span></span></td>
<td><span data-ttu-id="afddf-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-711">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="afddf-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-714">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-714">CC003</span></span></td>
<td><span data-ttu-id="afddf-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-715">Packaging</span></span></td>
<td><span data-ttu-id="afddf-716">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-716">10001</span></span></td>
<td><span data-ttu-id="afddf-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-717">Electricity</span></span></td>
<td><span data-ttu-id="afddf-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-718">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-719">286.25</span><span class="sxs-lookup"><span data-stu-id="afddf-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-721">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-721">CC003</span></span></td>
<td><span data-ttu-id="afddf-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-722">Packaging</span></span></td>
<td><span data-ttu-id="afddf-723">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-723">10001</span></span></td>
<td><span data-ttu-id="afddf-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-724">Electricity</span></span></td>
<td><span data-ttu-id="afddf-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-725">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="afddf-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-728">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-729">Product 1</span></span></td>
<td><span data-ttu-id="afddf-730">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-730">10001</span></span></td>
<td><span data-ttu-id="afddf-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-731">Electricity</span></span></td>
<td><span data-ttu-id="afddf-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-732">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-733">776.36</span><span class="sxs-lookup"><span data-stu-id="afddf-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-735">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-736">Product 1</span></span></td>
<td><span data-ttu-id="afddf-737">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-737">10001</span></span></td>
<td><span data-ttu-id="afddf-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-738">Electricity</span></span></td>
<td><span data-ttu-id="afddf-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-739">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="afddf-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-742">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-743">Product 1</span></span></td>
<td><span data-ttu-id="afddf-744">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-744">10001</span></span></td>
<td><span data-ttu-id="afddf-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-745">Electricity</span></span></td>
<td><span data-ttu-id="afddf-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-746">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-747">223.64</span><span class="sxs-lookup"><span data-stu-id="afddf-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="afddf-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-749">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-750">Product 1</span></span></td>
<td><span data-ttu-id="afddf-751">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-751">10001</span></span></td>
<td><span data-ttu-id="afddf-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-752">Electricity</span></span></td>
<td><span data-ttu-id="afddf-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-753">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="afddf-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="afddf-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="afddf-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="afddf-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-757">Cost element</span></span></th>
<th><span data-ttu-id="afddf-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-758">Cost behavior</span></span></th>
<th><span data-ttu-id="afddf-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-759">Amount</span></span></th>
<th><span data-ttu-id="afddf-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="afddf-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="afddf-761">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-761">CC001</span></span></td>
<td><span data-ttu-id="afddf-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-762">HR</span></span></td>
<td><span data-ttu-id="afddf-763">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-763">10001</span></span></td>
<td><span data-ttu-id="afddf-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-764">Electricity</span></span></td>
<td><span data-ttu-id="afddf-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-765">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="afddf-766">-500.00</span></span></td>
<td><span data-ttu-id="afddf-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-768">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-768">CC002</span></span></td>
<td><span data-ttu-id="afddf-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-769">Finance</span></span></td>
<td><span data-ttu-id="afddf-770">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-770">10001</span></span></td>
<td><span data-ttu-id="afddf-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-771">Electricity</span></span></td>
<td><span data-ttu-id="afddf-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-772">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-773">175.00</span><span class="sxs-lookup"><span data-stu-id="afddf-773">175.00</span></span></td>
<td><span data-ttu-id="afddf-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-775">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-775">CC003</span></span></td>
<td><span data-ttu-id="afddf-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-776">Assembly</span></span></td>
<td><span data-ttu-id="afddf-777">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-777">10001</span></span></td>
<td><span data-ttu-id="afddf-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-778">Electricity</span></span></td>
<td><span data-ttu-id="afddf-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-779">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-780">275.00</span><span class="sxs-lookup"><span data-stu-id="afddf-780">275.00</span></span></td>
<td><span data-ttu-id="afddf-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-782">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-782">CC004</span></span></td>
<td><span data-ttu-id="afddf-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-783">Packaging</span></span></td>
<td><span data-ttu-id="afddf-784">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-784">10001</span></span></td>
<td><span data-ttu-id="afddf-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-785">Electricity</span></span></td>
<td><span data-ttu-id="afddf-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-786">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-787">50,00</span><span class="sxs-lookup"><span data-stu-id="afddf-787">50,00</span></span></td>
<td><span data-ttu-id="afddf-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-789">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-789">CC001</span></span></td>
<td><span data-ttu-id="afddf-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="afddf-790">HR</span></span></td>
<td><span data-ttu-id="afddf-791">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-791">10001</span></span></td>
<td><span data-ttu-id="afddf-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-792">Electricity</span></span></td>
<td><span data-ttu-id="afddf-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-793">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="afddf-794">-1,245.71</span></span></td>
<td><span data-ttu-id="afddf-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-796">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-796">CC002</span></span></td>
<td><span data-ttu-id="afddf-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-797">Finance</span></span></td>
<td><span data-ttu-id="afddf-798">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-798">10001</span></span></td>
<td><span data-ttu-id="afddf-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-799">Electricity</span></span></td>
<td><span data-ttu-id="afddf-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-800">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-801">436.00</span><span class="sxs-lookup"><span data-stu-id="afddf-801">436.00</span></span></td>
<td><span data-ttu-id="afddf-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-803">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-803">CC003</span></span></td>
<td><span data-ttu-id="afddf-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-804">Assembly</span></span></td>
<td><span data-ttu-id="afddf-805">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-805">10001</span></span></td>
<td><span data-ttu-id="afddf-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-806">Electricity</span></span></td>
<td><span data-ttu-id="afddf-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-807">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-808">685.14</span><span class="sxs-lookup"><span data-stu-id="afddf-808">685.14</span></span></td>
<td><span data-ttu-id="afddf-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-810">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-810">CC004</span></span></td>
<td><span data-ttu-id="afddf-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-811">Packaging</span></span></td>
<td><span data-ttu-id="afddf-812">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-812">10001</span></span></td>
<td><span data-ttu-id="afddf-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-813">Electricity</span></span></td>
<td><span data-ttu-id="afddf-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-814">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-815">124.57</span><span class="sxs-lookup"><span data-stu-id="afddf-815">124.57</span></span></td>
<td><span data-ttu-id="afddf-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-817">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-817">CC002</span></span></td>
<td><span data-ttu-id="afddf-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-818">Finance</span></span></td>
<td><span data-ttu-id="afddf-819">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-819">10001</span></span></td>
<td><span data-ttu-id="afddf-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-820">Electricity</span></span></td>
<td><span data-ttu-id="afddf-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-821">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="afddf-822">-675.00</span></span></td>
<td><span data-ttu-id="afddf-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-824">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-824">CC003</span></span></td>
<td><span data-ttu-id="afddf-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-825">Assembly</span></span></td>
<td><span data-ttu-id="afddf-826">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-826">10001</span></span></td>
<td><span data-ttu-id="afddf-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-827">Electricity</span></span></td>
<td><span data-ttu-id="afddf-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-828">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-829">438.75</span><span class="sxs-lookup"><span data-stu-id="afddf-829">438.75</span></span></td>
<td><span data-ttu-id="afddf-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-831">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-831">CC004</span></span></td>
<td><span data-ttu-id="afddf-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-832">Packaging</span></span></td>
<td><span data-ttu-id="afddf-833">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-833">10001</span></span></td>
<td><span data-ttu-id="afddf-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-834">Electricity</span></span></td>
<td><span data-ttu-id="afddf-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-835">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-836">236.25</span><span class="sxs-lookup"><span data-stu-id="afddf-836">236.25</span></span></td>
<td><span data-ttu-id="afddf-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-838">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-838">CC002</span></span></td>
<td><span data-ttu-id="afddf-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="afddf-839">Finance</span></span></td>
<td><span data-ttu-id="afddf-840">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-840">10001</span></span></td>
<td><span data-ttu-id="afddf-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-841">Electricity</span></span></td>
<td><span data-ttu-id="afddf-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-842">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="afddf-843">-8,150.29</span></span></td>
<td><span data-ttu-id="afddf-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-845">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-845">CC003</span></span></td>
<td><span data-ttu-id="afddf-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-846">Assembly</span></span></td>
<td><span data-ttu-id="afddf-847">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-847">10001</span></span></td>
<td><span data-ttu-id="afddf-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-848">Electricity</span></span></td>
<td><span data-ttu-id="afddf-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-849">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="afddf-850">5,297.69</span></span></td>
<td><span data-ttu-id="afddf-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-852">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-852">CC004</span></span></td>
<td><span data-ttu-id="afddf-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="afddf-853">Packaging</span></span></td>
<td><span data-ttu-id="afddf-854">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-854">10001</span></span></td>
<td><span data-ttu-id="afddf-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-855">Electricity</span></span></td>
<td><span data-ttu-id="afddf-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-856">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="afddf-857">2,852.60</span></span></td>
<td><span data-ttu-id="afddf-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-859">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-859">CC003</span></span></td>
<td><span data-ttu-id="afddf-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-860">Assembly</span></span></td>
<td><span data-ttu-id="afddf-861">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-861">10001</span></span></td>
<td><span data-ttu-id="afddf-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-862">Electricity</span></span></td>
<td><span data-ttu-id="afddf-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-863">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="afddf-864">-713.75</span></span></td>
<td><span data-ttu-id="afddf-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-866">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-867">Product 1</span></span></td>
<td><span data-ttu-id="afddf-868">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-868">10001</span></span></td>
<td><span data-ttu-id="afddf-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-869">Electricity</span></span></td>
<td><span data-ttu-id="afddf-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-870">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-871">535.31</span><span class="sxs-lookup"><span data-stu-id="afddf-871">535.31</span></span></td>
<td><span data-ttu-id="afddf-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-873">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-874">Product 2</span></span></td>
<td><span data-ttu-id="afddf-875">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-875">10001</span></span></td>
<td><span data-ttu-id="afddf-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-876">Electricity</span></span></td>
<td><span data-ttu-id="afddf-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-877">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-878">178.44</span><span class="sxs-lookup"><span data-stu-id="afddf-878">178.44</span></span></td>
<td><span data-ttu-id="afddf-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-880">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-880">CC003</span></span></td>
<td><span data-ttu-id="afddf-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-881">Assembly</span></span></td>
<td><span data-ttu-id="afddf-882">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-882">10001</span></span></td>
<td><span data-ttu-id="afddf-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-883">Electricity</span></span></td>
<td><span data-ttu-id="afddf-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-884">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="afddf-885">-5,982.83</span></span></td>
<td><span data-ttu-id="afddf-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-887">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-888">Product 1</span></span></td>
<td><span data-ttu-id="afddf-889">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-889">10001</span></span></td>
<td><span data-ttu-id="afddf-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-890">Electricity</span></span></td>
<td><span data-ttu-id="afddf-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-891">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="afddf-892">4,487.12</span></span></td>
<td><span data-ttu-id="afddf-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-894">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-895">Product 2</span></span></td>
<td><span data-ttu-id="afddf-896">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-896">10001</span></span></td>
<td><span data-ttu-id="afddf-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-897">Electricity</span></span></td>
<td><span data-ttu-id="afddf-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-898">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="afddf-899">1,495.71</span></span></td>
<td><span data-ttu-id="afddf-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-901">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-901">CC003</span></span></td>
<td><span data-ttu-id="afddf-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-902">Assembly</span></span></td>
<td><span data-ttu-id="afddf-903">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-903">10001</span></span></td>
<td><span data-ttu-id="afddf-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-904">Electricity</span></span></td>
<td><span data-ttu-id="afddf-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-905">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="afddf-906">-286.25</span></span></td>
<td><span data-ttu-id="afddf-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-908">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-909">Product 1</span></span></td>
<td><span data-ttu-id="afddf-910">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-910">10001</span></span></td>
<td><span data-ttu-id="afddf-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-911">Electricity</span></span></td>
<td><span data-ttu-id="afddf-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-912">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-913">241.05</span><span class="sxs-lookup"><span data-stu-id="afddf-913">241.05</span></span></td>
<td><span data-ttu-id="afddf-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-915">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-916">Product 2</span></span></td>
<td><span data-ttu-id="afddf-917">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-917">10001</span></span></td>
<td><span data-ttu-id="afddf-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-918">Electricity</span></span></td>
<td><span data-ttu-id="afddf-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-919">Fixed cost</span></span></td>
<td><span data-ttu-id="afddf-920">45.20</span><span class="sxs-lookup"><span data-stu-id="afddf-920">45.20</span></span></td>
<td><span data-ttu-id="afddf-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-922">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-922">CC003</span></span></td>
<td><span data-ttu-id="afddf-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="afddf-923">Assembly</span></span></td>
<td><span data-ttu-id="afddf-924">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-924">10001</span></span></td>
<td><span data-ttu-id="afddf-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-925">Electricity</span></span></td>
<td><span data-ttu-id="afddf-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-926">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="afddf-927">-2,977.17</span></span></td>
<td><span data-ttu-id="afddf-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-929">Prod 1</span></span></td>
<td><span data-ttu-id="afddf-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-930">Product 1</span></span></td>
<td><span data-ttu-id="afddf-931">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-931">10001</span></span></td>
<td><span data-ttu-id="afddf-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-932">Electricity</span></span></td>
<td><span data-ttu-id="afddf-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-933">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="afddf-934">2,507.09</span></span></td>
<td><span data-ttu-id="afddf-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="afddf-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-936">Prod 2</span></span></td>
<td><span data-ttu-id="afddf-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-937">Product 2</span></span></td>
<td><span data-ttu-id="afddf-938">10001</span><span class="sxs-lookup"><span data-stu-id="afddf-938">10001</span></span></td>
<td><span data-ttu-id="afddf-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-939">Electricity</span></span></td>
<td><span data-ttu-id="afddf-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-940">Variable cost</span></span></td>
<td><span data-ttu-id="afddf-941">470.08</span><span class="sxs-lookup"><span data-stu-id="afddf-941">470.08</span></span></td>
<td><span data-ttu-id="afddf-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="afddf-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="afddf-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="afddf-943">Conclusion</span></span>
<span data-ttu-id="afddf-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="afddf-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="afddf-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="afddf-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="afddf-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="afddf-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="afddf-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="afddf-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="afddf-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="afddf-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="afddf-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="afddf-951">CC099</span><span class="sxs-lookup"><span data-stu-id="afddf-951">CC099</span></span></th>
<th><span data-ttu-id="afddf-952">CC001</span><span class="sxs-lookup"><span data-stu-id="afddf-952">CC001</span></span></th>
<th><span data-ttu-id="afddf-953">CC002</span><span class="sxs-lookup"><span data-stu-id="afddf-953">CC002</span></span></th>
<th><span data-ttu-id="afddf-954">CC003</span><span class="sxs-lookup"><span data-stu-id="afddf-954">CC003</span></span></th>
<th><span data-ttu-id="afddf-955">CC004</span><span class="sxs-lookup"><span data-stu-id="afddf-955">CC004</span></span></th>
<th><span data-ttu-id="afddf-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-956">Proj 1</span></span></th>
<th><span data-ttu-id="afddf-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-957">Proj 2</span></span></th>
<th><span data-ttu-id="afddf-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="afddf-958">Prod 1</span></span></th>
<th><span data-ttu-id="afddf-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="afddf-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="afddf-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="afddf-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="afddf-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="afddf-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="afddf-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-971">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="afddf-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="afddf-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-973">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-974">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-975">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-976">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-977">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="afddf-978">776.36</span><span class="sxs-lookup"><span data-stu-id="afddf-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-979">223.64</span><span class="sxs-lookup"><span data-stu-id="afddf-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="afddf-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="afddf-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-982">000</span><span class="sxs-lookup"><span data-stu-id="afddf-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-983">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-984">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-985">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-986">0.00</span><span class="sxs-lookup"><span data-stu-id="afddf-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-987">30.00</span><span class="sxs-lookup"><span data-stu-id="afddf-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-988">10.00</span><span class="sxs-lookup"><span data-stu-id="afddf-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="afddf-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="afddf-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="afddf-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="afddf-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="afddf-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="afddf-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="afddf-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="afddf-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="afddf-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="afddf-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="afddf-996">สำหรับข้อมูลเพิ่มเติม ให้ดู [การรวบรวมต้นทุน](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="afddf-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




