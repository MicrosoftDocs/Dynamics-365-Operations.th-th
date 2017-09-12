---
title: "การคำนวณค่าโสหุ้ย"
description: "หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย"
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: th-th
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="dd0df-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="dd0df-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dd0df-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="dd0df-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="dd0df-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="dd0df-105">Term definition</span></span>
---------------

<span data-ttu-id="dd0df-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="dd0df-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="dd0df-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="dd0df-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="dd0df-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="dd0df-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="dd0df-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="dd0df-109">Rent</span></span>
-   <span data-ttu-id="dd0df-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-110">Electricity</span></span>
-   <span data-ttu-id="dd0df-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="dd0df-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="dd0df-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="dd0df-112">Overhead calculation overview</span></span>
<span data-ttu-id="dd0df-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dd0df-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="dd0df-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="dd0df-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="dd0df-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="dd0df-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="dd0df-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="dd0df-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="dd0df-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="dd0df-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="dd0df-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="dd0df-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-119">Version type</span></span>
-   <span data-ttu-id="dd0df-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="dd0df-120">Date and time</span></span>
-   <span data-ttu-id="dd0df-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="dd0df-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-122">Fiscal year</span></span>
-   <span data-ttu-id="dd0df-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-123">Fiscal period</span></span>

<span data-ttu-id="dd0df-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="dd0df-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="dd0df-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="dd0df-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="dd0df-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dd0df-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="dd0df-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="dd0df-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="dd0df-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="dd0df-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="dd0df-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="dd0df-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="dd0df-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="dd0df-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="dd0df-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="dd0df-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dd0df-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="dd0df-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="dd0df-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="dd0df-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="dd0df-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="dd0df-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="dd0df-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dd0df-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="dd0df-140">Main account</span></span></th>
<th><span data-ttu-id="dd0df-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="dd0df-143">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-143">CC099</span></span></td>
<td><span data-ttu-id="dd0df-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-144">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-145">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-145">10001</span></span></td>
<td><span data-ttu-id="dd0df-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-146">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="dd0df-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="dd0df-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="dd0df-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="dd0df-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="dd0df-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-151">Define the cost behavior rule</span></span>

<span data-ttu-id="dd0df-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="dd0df-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="dd0df-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="dd0df-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="dd0df-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="dd0df-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="dd0df-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="dd0df-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="dd0df-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="dd0df-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="dd0df-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="dd0df-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-160">Journal</span></span></th>
<th><span data-ttu-id="dd0df-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd0df-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd0df-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-164">00001</span><span class="sxs-lookup"><span data-stu-id="dd0df-164">00001</span></span></td>
<td><span data-ttu-id="dd0df-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="dd0df-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-166">Fiscal</span></span></td>
<td><span data-ttu-id="dd0df-167">2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-167">2017</span></span></td>
<td><span data-ttu-id="dd0df-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-168">Period 1</span></span></td>
<td><span data-ttu-id="dd0df-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dd0df-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="dd0df-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-173">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-174">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="dd0df-177">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-177">CC099</span></span></td>
<td><span data-ttu-id="dd0df-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-178">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-179">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-179">10001</span></span></td>
<td><span data-ttu-id="dd0df-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-180">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="dd0df-181">Unclassified</span></span></td>
<td><span data-ttu-id="dd0df-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd0df-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-185">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-186">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-187">Amount</span></span></th>
<th><span data-ttu-id="dd0df-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-189">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-189">CC099</span></span></td>
<td><span data-ttu-id="dd0df-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-190">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-191">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-191">10001</span></span></td>
<td><span data-ttu-id="dd0df-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-192">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="dd0df-193">Unclassified</span></span></td>
<td><span data-ttu-id="dd0df-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-194">10,000.00</span></span></td>
<td><span data-ttu-id="dd0df-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-196">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-196">CC099</span></span></td>
<td><span data-ttu-id="dd0df-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-197">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-198">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-198">10001</span></span></td>
<td><span data-ttu-id="dd0df-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-199">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="dd0df-200">Unclassified</span></span></td>
<td><span data-ttu-id="dd0df-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-201">-10,000.00</span></span></td>
<td><span data-ttu-id="dd0df-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-203">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-203">CC099</span></span></td>
<td><span data-ttu-id="dd0df-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-204">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-205">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-205">10001</span></span></td>
<td><span data-ttu-id="dd0df-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-206">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-207">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-208">1,000.00</span></span></td>
<td><span data-ttu-id="dd0df-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-210">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-210">CC099</span></span></td>
<td><span data-ttu-id="dd0df-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-211">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-212">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-212">10001</span></span></td>
<td><span data-ttu-id="dd0df-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-213">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-214">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-215">9,000.00</span></span></td>
<td><span data-ttu-id="dd0df-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-217">สำหรับข้อมูลรายละเอียดเกี่ยวกับพฤติกรรมต้นทุน ดูนโยบายพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="dd0df-218">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="dd0df-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="dd0df-219">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="dd0df-220">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="dd0df-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="dd0df-221">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="dd0df-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="dd0df-222">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-222">Define the cost distribution rule</span></span>

<span data-ttu-id="dd0df-223">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dd0df-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="dd0df-224">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="dd0df-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="dd0df-225">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="dd0df-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="dd0df-226">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="dd0df-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="dd0df-227">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="dd0df-228">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-229">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-229">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="dd0df-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-231">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-231">CC001</span></span></td>
<td><span data-ttu-id="dd0df-232">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-232">HR</span></span></td>
<td><span data-ttu-id="dd0df-233">1,000</span><span class="sxs-lookup"><span data-stu-id="dd0df-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-234">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-234">CC002</span></span></td>
<td><span data-ttu-id="dd0df-235">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-235">Finance</span></span></td>
<td><span data-ttu-id="dd0df-236">6,000</span><span class="sxs-lookup"><span data-stu-id="dd0df-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-237">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-237">CC003</span></span></td>
<td><span data-ttu-id="dd0df-238">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-238">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-239">0</span><span class="sxs-lookup"><span data-stu-id="dd0df-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-240">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-241">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-241">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-242">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-242">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-243">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-243">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-244">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-245">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-245">CC001</span></span></td>
<td><span data-ttu-id="dd0df-246">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-246">HR</span></span></td>
<td><span data-ttu-id="dd0df-247">1,000</span><span class="sxs-lookup"><span data-stu-id="dd0df-247">1,000</span></span></td>
<td><span data-ttu-id="dd0df-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dd0df-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-250">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-250">CC002</span></span></td>
<td><span data-ttu-id="dd0df-251">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-251">Finance</span></span></td>
<td><span data-ttu-id="dd0df-252">6,000</span><span class="sxs-lookup"><span data-stu-id="dd0df-252">6,000</span></span></td>
<td><span data-ttu-id="dd0df-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dd0df-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="dd0df-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-255">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-255">CC003</span></span></td>
<td><span data-ttu-id="dd0df-256">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-256">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-257">0</span><span class="sxs-lookup"><span data-stu-id="dd0df-257">0</span></span></td>
<td><span data-ttu-id="dd0df-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="dd0df-259">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-260">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="dd0df-261">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-262">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-262">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-263">สูตร</span><span class="sxs-lookup"><span data-stu-id="dd0df-263">Formula</span></span></th>
<th><span data-ttu-id="dd0df-264">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-264">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-265">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-265">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-266">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-267">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-267">CC001</span></span></td>
<td><span data-ttu-id="dd0df-268">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-268">HR</span></span></td>
<td><span data-ttu-id="dd0df-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dd0df-270">1</span><span class="sxs-lookup"><span data-stu-id="dd0df-270">1</span></span></td>
<td><span data-ttu-id="dd0df-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dd0df-272">500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-273">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-273">CC002</span></span></td>
<td><span data-ttu-id="dd0df-274">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-274">Finance</span></span></td>
<td><span data-ttu-id="dd0df-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dd0df-276">1</span><span class="sxs-lookup"><span data-stu-id="dd0df-276">1</span></span></td>
<td><span data-ttu-id="dd0df-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dd0df-278">500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-279">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-279">CC003</span></span></td>
<td><span data-ttu-id="dd0df-280">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-280">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="dd0df-282">0</span><span class="sxs-lookup"><span data-stu-id="dd0df-282">0</span></span></td>
<td><span data-ttu-id="dd0df-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="dd0df-284">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="dd0df-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-286">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-286">Journal</span></span></th>
<th><span data-ttu-id="dd0df-287">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd0df-288">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd0df-289">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-290">00002</span><span class="sxs-lookup"><span data-stu-id="dd0df-290">00002</span></span></td>
<td><span data-ttu-id="dd0df-291">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="dd0df-292">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-292">Fiscal</span></span></td>
<td><span data-ttu-id="dd0df-293">2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-293">2017</span></span></td>
<td><span data-ttu-id="dd0df-294">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-294">Period 1</span></span></td>
<td><span data-ttu-id="dd0df-295">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dd0df-296">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="dd0df-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-297">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-298">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-299">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-299">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-300">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-300">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-301">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-302">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-303">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-303">CC099</span></span></td>
<td><span data-ttu-id="dd0df-304">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-304">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-305">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-305">10001</span></span></td>
<td><span data-ttu-id="dd0df-306">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-306">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-307">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-307">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-308">1,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-309">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-310">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-310">CC099</span></span></td>
<td><span data-ttu-id="dd0df-311">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-311">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-312">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-312">10001</span></span></td>
<td><span data-ttu-id="dd0df-313">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-313">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-314">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-314">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd0df-316">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-317">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-318">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-318">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-319">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-319">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-320">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-320">Amount</span></span></th>
<th><span data-ttu-id="dd0df-321">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-322">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-322">CC099</span></span></td>
<td><span data-ttu-id="dd0df-323">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-323">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-324">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-324">10001</span></span></td>
<td><span data-ttu-id="dd0df-325">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-325">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-326">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-326">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-327">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="dd0df-327">-1,000.00</span></span></td>
<td><span data-ttu-id="dd0df-328">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-329">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-329">CC001</span></span></td>
<td><span data-ttu-id="dd0df-330">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-330">HR</span></span></td>
<td><span data-ttu-id="dd0df-331">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-331">10001</span></span></td>
<td><span data-ttu-id="dd0df-332">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-332">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-333">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-333">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-334">500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-334">500.00</span></span></td>
<td><span data-ttu-id="dd0df-335">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-336">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-336">CC002</span></span></td>
<td><span data-ttu-id="dd0df-337">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-337">Finance</span></span></td>
<td><span data-ttu-id="dd0df-338">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-338">10001</span></span></td>
<td><span data-ttu-id="dd0df-339">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-339">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-340">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-340">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-341">500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-341">500.00</span></span></td>
<td><span data-ttu-id="dd0df-342">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-343">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-343">CC099</span></span></td>
<td><span data-ttu-id="dd0df-344">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd0df-344">Default cost center</span></span></td>
<td><span data-ttu-id="dd0df-345">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-345">10001</span></span></td>
<td><span data-ttu-id="dd0df-346">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-346">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-347">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-347">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-348">-9,000.00</span></span></td>
<td><span data-ttu-id="dd0df-349">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-350">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-350">CC001</span></span></td>
<td><span data-ttu-id="dd0df-351">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-351">HR</span></span></td>
<td><span data-ttu-id="dd0df-352">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-352">10001</span></span></td>
<td><span data-ttu-id="dd0df-353">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-353">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-354">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-354">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-355">1,285.71</span></span></td>
<td><span data-ttu-id="dd0df-356">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-357">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-357">CC002</span></span></td>
<td><span data-ttu-id="dd0df-358">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-358">Finance</span></span></td>
<td><span data-ttu-id="dd0df-359">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-359">10001</span></span></td>
<td><span data-ttu-id="dd0df-360">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-360">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-361">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-361">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="dd0df-362">7,714.29</span></span></td>
<td><span data-ttu-id="dd0df-363">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-364">สำหรับรายละเอียดเกี่ยวกับการกระจายต้นทุนและฐานการปันส่วน ให้ดูนโยบายการกระจายต้นทุนและฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="dd0df-365">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="dd0df-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="dd0df-366">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="dd0df-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="dd0df-367">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="dd0df-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="dd0df-368">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="dd0df-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="dd0df-369">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="dd0df-369">Define the overhead rate</span></span>

<span data-ttu-id="dd0df-370">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="dd0df-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="dd0df-371">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dd0df-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-372">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-372">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-373">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="dd0df-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-374">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-374">Proj 1</span></span></td>
<td><span data-ttu-id="dd0df-375">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-375">Project 1</span></span></td>
<td><span data-ttu-id="dd0df-376">3</span><span class="sxs-lookup"><span data-stu-id="dd0df-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-377">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-377">Proj 2</span></span></td>
<td><span data-ttu-id="dd0df-378">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-378">Project 2</span></span></td>
<td><span data-ttu-id="dd0df-379">1</span><span class="sxs-lookup"><span data-stu-id="dd0df-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-380">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-381">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-381">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-382">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-382">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-383">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-383">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-384">หน่วย</span><span class="sxs-lookup"><span data-stu-id="dd0df-384">Units</span></span></th>
<th><span data-ttu-id="dd0df-385">อัตรา</span><span class="sxs-lookup"><span data-stu-id="dd0df-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-386">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-386">CC001</span></span></td>
<td><span data-ttu-id="dd0df-387">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-387">HR</span></span></td>
<td><span data-ttu-id="dd0df-388">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-388">10001</span></span></td>
<td><span data-ttu-id="dd0df-389">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-389">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-390">1</span><span class="sxs-lookup"><span data-stu-id="dd0df-390">1</span></span></td>
<td><span data-ttu-id="dd0df-391">10</span><span class="sxs-lookup"><span data-stu-id="dd0df-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-392">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-393">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-393">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-394">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-394">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-395">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-395">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-396">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-396">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-397">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-398">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-398">Proj 1</span></span></td>
<td><span data-ttu-id="dd0df-399">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-399">Project 1</span></span></td>
<td><span data-ttu-id="dd0df-400">3</span><span class="sxs-lookup"><span data-stu-id="dd0df-400">3</span></span></td>
<td><span data-ttu-id="dd0df-401">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-401">10001</span></span></td>
<td><span data-ttu-id="dd0df-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="dd0df-403">30.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-404">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-404">Proj 2</span></span></td>
<td><span data-ttu-id="dd0df-405">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-405">Project 2</span></span></td>
<td><span data-ttu-id="dd0df-406">1</span><span class="sxs-lookup"><span data-stu-id="dd0df-406">1</span></span></td>
<td><span data-ttu-id="dd0df-407">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-407">10001</span></span></td>
<td><span data-ttu-id="dd0df-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="dd0df-409">10.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="dd0df-410">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-411">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-411">Journal</span></span></th>
<th><span data-ttu-id="dd0df-412">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd0df-413">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd0df-414">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-415">00003</span><span class="sxs-lookup"><span data-stu-id="dd0df-415">00003</span></span></td>
<td><span data-ttu-id="dd0df-416">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="dd0df-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="dd0df-417">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-417">Fiscal</span></span></td>
<td><span data-ttu-id="dd0df-418">2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-418">2017</span></span></td>
<td><span data-ttu-id="dd0df-419">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-419">Period 1</span></span></td>
<td><span data-ttu-id="dd0df-420">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="dd0df-421">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="dd0df-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-422">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-423">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-423">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-424">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-425">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-426">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-426">Proj 1</span></span></td>
<td><span data-ttu-id="dd0df-427">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="dd0df-428">3.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-429">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-430">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-430">Proj 2</span></span></td>
<td><span data-ttu-id="dd0df-431">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="dd0df-432">1.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd0df-433">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-434">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-435">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-435">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-436">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-436">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-437">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-437">Amount</span></span></th>
<th><span data-ttu-id="dd0df-438">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="dd0df-439">CC0001</span></span></td>
<td><span data-ttu-id="dd0df-440">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-440">HR</span></span></td>
<td><span data-ttu-id="dd0df-441">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-441">10001</span></span></td>
<td><span data-ttu-id="dd0df-442">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-442">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-443">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-443">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-444">-30.00</span></span></td>
<td><span data-ttu-id="dd0df-445">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-446">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-446">Proj 1</span></span></td>
<td><span data-ttu-id="dd0df-447">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="dd0df-448">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-448">10001</span></span></td>
<td><span data-ttu-id="dd0df-449">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-449">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-450">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-450">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-451">30.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-451">30.00</span></span></td>
<td><span data-ttu-id="dd0df-452">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-453">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-453">CC001</span></span></td>
<td><span data-ttu-id="dd0df-454">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-454">HR</span></span></td>
<td><span data-ttu-id="dd0df-455">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-455">10001</span></span></td>
<td><span data-ttu-id="dd0df-456">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-456">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-457">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-457">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-458">-10.00</span></span></td>
<td><span data-ttu-id="dd0df-459">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-460">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-460">Proj 2</span></span></td>
<td><span data-ttu-id="dd0df-461">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="dd0df-462">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-462">10001</span></span></td>
<td><span data-ttu-id="dd0df-463">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-463">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-464">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-464">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-465">10.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-465">10.00</span></span></td>
<td><span data-ttu-id="dd0df-466">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-467">สำหรับข้อมูลรายละเอียดเกี่ยวกับนโยบายอัตราค่าโสหุ้ย ให้ดูนโยบายอัตราค่าโสหุ้ยและฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="dd0df-468">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="dd0df-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="dd0df-469">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="dd0df-470">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="dd0df-471">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="dd0df-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="dd0df-472">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dd0df-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="dd0df-473">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="dd0df-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="dd0df-474">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="dd0df-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="dd0df-475">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="dd0df-476">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="dd0df-477">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="dd0df-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="dd0df-478">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-478">Define the cost allocation</span></span>

<span data-ttu-id="dd0df-479">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="dd0df-480">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="dd0df-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="dd0df-481">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dd0df-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-482">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-482">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-483">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="dd0df-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-484">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-484">CC002</span></span></td>
<td><span data-ttu-id="dd0df-485">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-485">Finance</span></span></td>
<td><span data-ttu-id="dd0df-486">35</span><span class="sxs-lookup"><span data-stu-id="dd0df-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-487">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-487">CC003</span></span></td>
<td><span data-ttu-id="dd0df-488">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-488">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-489">55</span><span class="sxs-lookup"><span data-stu-id="dd0df-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-490">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-490">CC004</span></span></td>
<td><span data-ttu-id="dd0df-491">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-491">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-492">10</span><span class="sxs-lookup"><span data-stu-id="dd0df-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-493">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="dd0df-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="dd0df-494">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dd0df-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-495">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-495">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-496">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-497">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-497">CC003</span></span></td>
<td><span data-ttu-id="dd0df-498">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-498">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-499">65</span><span class="sxs-lookup"><span data-stu-id="dd0df-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-500">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-500">CC004</span></span></td>
<td><span data-ttu-id="dd0df-501">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-501">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-502">35</span><span class="sxs-lookup"><span data-stu-id="dd0df-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-503">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="dd0df-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="dd0df-504">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dd0df-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-505">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-505">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-506">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="dd0df-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-507">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-507">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-508">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-508">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-509">60</span><span class="sxs-lookup"><span data-stu-id="dd0df-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-510">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-510">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-511">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-511">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-512">20</span><span class="sxs-lookup"><span data-stu-id="dd0df-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-513">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="dd0df-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="dd0df-514">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="dd0df-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-515">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-515">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-516">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="dd0df-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-517">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-517">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-518">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-518">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-519">80</span><span class="sxs-lookup"><span data-stu-id="dd0df-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-520">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-520">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-521">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-521">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-522">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="dd0df-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-523">**หมายเหตุ:** ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ใช้กับผลิตภัณฑ์สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd0df-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="dd0df-524">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวให้บริการการประเมินทางสถิติ ให้ดูเท็มเพลตตัวให้บริการการประเมินทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="dd0df-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="dd0df-525">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในอีกไม่ช้านี้) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="dd0df-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-526">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-526">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-527">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-527">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-528">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-528">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-529">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-529">Amount</span></span></th>
<th><span data-ttu-id="dd0df-530">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-531">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-531">CC002</span></span></td>
<td><span data-ttu-id="dd0df-532">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-532">Finance</span></span></td>
<td><span data-ttu-id="dd0df-533">35</span><span class="sxs-lookup"><span data-stu-id="dd0df-533">35</span></span></td>
<td><span data-ttu-id="dd0df-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dd0df-535">175.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-535">175.00</span></span></td>
<td><span data-ttu-id="dd0df-536">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-537">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-537">CC003</span></span></td>
<td><span data-ttu-id="dd0df-538">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-538">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-539">55</span><span class="sxs-lookup"><span data-stu-id="dd0df-539">55</span></span></td>
<td><span data-ttu-id="dd0df-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dd0df-541">275.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-541">275.00</span></span></td>
<td><span data-ttu-id="dd0df-542">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-543">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-543">CC004</span></span></td>
<td><span data-ttu-id="dd0df-544">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-544">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-545">10</span><span class="sxs-lookup"><span data-stu-id="dd0df-545">10</span></span></td>
<td><span data-ttu-id="dd0df-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="dd0df-547">50.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-547">50.00</span></span></td>
<td><span data-ttu-id="dd0df-548">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-549">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-549">CC002</span></span></td>
<td><span data-ttu-id="dd0df-550">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-550">Finance</span></span></td>
<td><span data-ttu-id="dd0df-551">35</span><span class="sxs-lookup"><span data-stu-id="dd0df-551">35</span></span></td>
<td><span data-ttu-id="dd0df-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dd0df-553">436.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-553">436.00</span></span></td>
<td><span data-ttu-id="dd0df-554">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-555">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-555">CC003</span></span></td>
<td><span data-ttu-id="dd0df-556">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-556">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-557">55</span><span class="sxs-lookup"><span data-stu-id="dd0df-557">55</span></span></td>
<td><span data-ttu-id="dd0df-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dd0df-559">685.14</span><span class="sxs-lookup"><span data-stu-id="dd0df-559">685.14</span></span></td>
<td><span data-ttu-id="dd0df-560">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-561">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-561">CC004</span></span></td>
<td><span data-ttu-id="dd0df-562">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-562">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-563">10</span><span class="sxs-lookup"><span data-stu-id="dd0df-563">10</span></span></td>
<td><span data-ttu-id="dd0df-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="dd0df-565">124.57</span><span class="sxs-lookup"><span data-stu-id="dd0df-565">124.57</span></span></td>
<td><span data-ttu-id="dd0df-566">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-567">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="dd0df-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-568">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-568">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-569">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-569">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-570">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-570">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-571">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-571">Amount</span></span></th>
<th><span data-ttu-id="dd0df-572">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-573">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-573">CC003</span></span></td>
<td><span data-ttu-id="dd0df-574">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-574">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-575">65</span><span class="sxs-lookup"><span data-stu-id="dd0df-575">65</span></span></td>
<td><span data-ttu-id="dd0df-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="dd0df-577">438.75</span><span class="sxs-lookup"><span data-stu-id="dd0df-577">438.75</span></span></td>
<td><span data-ttu-id="dd0df-578">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-579">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-579">CC004</span></span></td>
<td><span data-ttu-id="dd0df-580">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-580">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-581">35</span><span class="sxs-lookup"><span data-stu-id="dd0df-581">35</span></span></td>
<td><span data-ttu-id="dd0df-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="dd0df-583">236.25</span><span class="sxs-lookup"><span data-stu-id="dd0df-583">236.25</span></span></td>
<td><span data-ttu-id="dd0df-584">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-585">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-585">CC003</span></span></td>
<td><span data-ttu-id="dd0df-586">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-586">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-587">65</span><span class="sxs-lookup"><span data-stu-id="dd0df-587">65</span></span></td>
<td><span data-ttu-id="dd0df-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="dd0df-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="dd0df-589">5,297.69</span></span></td>
<td><span data-ttu-id="dd0df-590">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-591">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-591">CC004</span></span></td>
<td><span data-ttu-id="dd0df-592">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-592">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-593">35</span><span class="sxs-lookup"><span data-stu-id="dd0df-593">35</span></span></td>
<td><span data-ttu-id="dd0df-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="dd0df-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="dd0df-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="dd0df-595">2,852.60</span></span></td>
<td><span data-ttu-id="dd0df-596">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-597">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="dd0df-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-598">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-598">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-599">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-599">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-600">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-600">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-601">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-601">Amount</span></span></th>
<th><span data-ttu-id="dd0df-602">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-603">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-603">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-604">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-604">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-605">60</span><span class="sxs-lookup"><span data-stu-id="dd0df-605">60</span></span></td>
<td><span data-ttu-id="dd0df-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="dd0df-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="dd0df-607">535.31</span><span class="sxs-lookup"><span data-stu-id="dd0df-607">535.31</span></span></td>
<td><span data-ttu-id="dd0df-608">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-609">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-609">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-610">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-610">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-611">20</span><span class="sxs-lookup"><span data-stu-id="dd0df-611">20</span></span></td>
<td><span data-ttu-id="dd0df-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="dd0df-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="dd0df-613">178.44</span><span class="sxs-lookup"><span data-stu-id="dd0df-613">178.44</span></span></td>
<td><span data-ttu-id="dd0df-614">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-615">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-615">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-616">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-616">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-617">60</span><span class="sxs-lookup"><span data-stu-id="dd0df-617">60</span></span></td>
<td><span data-ttu-id="dd0df-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="dd0df-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="dd0df-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="dd0df-619">4,487.12</span></span></td>
<td><span data-ttu-id="dd0df-620">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-621">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-621">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-622">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-622">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-623">20</span><span class="sxs-lookup"><span data-stu-id="dd0df-623">20</span></span></td>
<td><span data-ttu-id="dd0df-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="dd0df-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="dd0df-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-625">1,495.71</span></span></td>
<td><span data-ttu-id="dd0df-626">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dd0df-627">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="dd0df-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-628">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-628">Cost object</span></span></th>
<th><span data-ttu-id="dd0df-629">ขนาด</span><span class="sxs-lookup"><span data-stu-id="dd0df-629">Magnitude</span></span></th>
<th><span data-ttu-id="dd0df-630">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="dd0df-630">Allocation factor</span></span></th>
<th><span data-ttu-id="dd0df-631">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-631">Amount</span></span></th>
<th><span data-ttu-id="dd0df-632">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-633">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-633">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-634">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-634">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-635">80</span><span class="sxs-lookup"><span data-stu-id="dd0df-635">80</span></span></td>
<td><span data-ttu-id="dd0df-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="dd0df-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="dd0df-637">241.05</span><span class="sxs-lookup"><span data-stu-id="dd0df-637">241.05</span></span></td>
<td><span data-ttu-id="dd0df-638">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-639">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-639">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-640">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-640">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-641">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="dd0df-641">15</span></span></td>
<td><span data-ttu-id="dd0df-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="dd0df-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="dd0df-643">45.20</span><span class="sxs-lookup"><span data-stu-id="dd0df-643">45.20</span></span></td>
<td><span data-ttu-id="dd0df-644">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-645">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-645">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-646">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-646">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-647">80</span><span class="sxs-lookup"><span data-stu-id="dd0df-647">80</span></span></td>
<td><span data-ttu-id="dd0df-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="dd0df-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="dd0df-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="dd0df-649">2,507.09</span></span></td>
<td><span data-ttu-id="dd0df-650">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-651">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-651">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-652">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-652">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-653">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="dd0df-653">15</span></span></td>
<td><span data-ttu-id="dd0df-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="dd0df-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="dd0df-655">470.08</span><span class="sxs-lookup"><span data-stu-id="dd0df-655">470.08</span></span></td>
<td><span data-ttu-id="dd0df-656">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="dd0df-657">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="dd0df-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-658">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-658">Journal</span></span></th>
<th><span data-ttu-id="dd0df-659">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="dd0df-660">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="dd0df-661">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-662">00004</span><span class="sxs-lookup"><span data-stu-id="dd0df-662">00004</span></span></td>
<td><span data-ttu-id="dd0df-663">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="dd0df-664">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-664">Fiscal</span></span></td>
<td><span data-ttu-id="dd0df-665">2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-665">2017</span></span></td>
<td><span data-ttu-id="dd0df-666">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-666">Period 1</span></span></td>
<td><span data-ttu-id="dd0df-667">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="dd0df-668">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dd0df-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="dd0df-669">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-670">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-671">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-671">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-672">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-672">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-673">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-674">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-675">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-675">CC001</span></span></td>
<td><span data-ttu-id="dd0df-676">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-676">HR</span></span></td>
<td><span data-ttu-id="dd0df-677">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-677">10001</span></span></td>
<td><span data-ttu-id="dd0df-678">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-678">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-679">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-679">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-680">500.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-681">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-682">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-682">CC001</span></span></td>
<td><span data-ttu-id="dd0df-683">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-683">HR</span></span></td>
<td><span data-ttu-id="dd0df-684">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-684">10001</span></span></td>
<td><span data-ttu-id="dd0df-685">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-685">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-686">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-686">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-688">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-689">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-689">CC002</span></span></td>
<td><span data-ttu-id="dd0df-690">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-690">Finance</span></span></td>
<td><span data-ttu-id="dd0df-691">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-691">10001</span></span></td>
<td><span data-ttu-id="dd0df-692">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-692">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-693">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-693">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-694">675.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-695">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-696">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-696">CC002</span></span></td>
<td><span data-ttu-id="dd0df-697">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-697">Finance</span></span></td>
<td><span data-ttu-id="dd0df-698">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-698">10001</span></span></td>
<td><span data-ttu-id="dd0df-699">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-699">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-700">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-700">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="dd0df-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-702">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-703">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-703">CC003</span></span></td>
<td><span data-ttu-id="dd0df-704">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-704">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-705">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-705">10001</span></span></td>
<td><span data-ttu-id="dd0df-706">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-706">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-707">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-707">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-708">713.75</span><span class="sxs-lookup"><span data-stu-id="dd0df-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-709">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-710">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-710">CC003</span></span></td>
<td><span data-ttu-id="dd0df-711">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-711">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-712">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-712">10001</span></span></td>
<td><span data-ttu-id="dd0df-713">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-713">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-714">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-714">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="dd0df-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-716">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-717">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-717">CC003</span></span></td>
<td><span data-ttu-id="dd0df-718">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-718">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-719">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-719">10001</span></span></td>
<td><span data-ttu-id="dd0df-720">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-720">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-721">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-721">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-722">286.25</span><span class="sxs-lookup"><span data-stu-id="dd0df-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-723">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-724">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-724">CC003</span></span></td>
<td><span data-ttu-id="dd0df-725">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-725">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-726">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-726">10001</span></span></td>
<td><span data-ttu-id="dd0df-727">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-727">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-728">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-728">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="dd0df-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-730">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-731">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-731">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-732">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-732">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-733">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-733">10001</span></span></td>
<td><span data-ttu-id="dd0df-734">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-734">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-735">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-735">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-736">776.36</span><span class="sxs-lookup"><span data-stu-id="dd0df-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-737">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-738">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-738">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-739">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-739">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-740">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-740">10001</span></span></td>
<td><span data-ttu-id="dd0df-741">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-741">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-742">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-742">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="dd0df-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-744">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-745">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-745">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-746">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-746">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-747">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-747">10001</span></span></td>
<td><span data-ttu-id="dd0df-748">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-748">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-749">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-749">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-750">223.64</span><span class="sxs-lookup"><span data-stu-id="dd0df-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-751">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="dd0df-752">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-752">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-753">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-753">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-754">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-754">10001</span></span></td>
<td><span data-ttu-id="dd0df-755">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-755">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-756">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-756">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="dd0df-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="dd0df-758">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="dd0df-759">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="dd0df-760">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-760">Cost element</span></span></th>
<th><span data-ttu-id="dd0df-761">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-761">Cost behavior</span></span></th>
<th><span data-ttu-id="dd0df-762">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-762">Amount</span></span></th>
<th><span data-ttu-id="dd0df-763">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd0df-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd0df-764">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-764">CC001</span></span></td>
<td><span data-ttu-id="dd0df-765">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-765">HR</span></span></td>
<td><span data-ttu-id="dd0df-766">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-766">10001</span></span></td>
<td><span data-ttu-id="dd0df-767">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-767">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-768">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-768">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-769">-500.00.</span><span class="sxs-lookup"><span data-stu-id="dd0df-769">-500.00</span></span></td>
<td><span data-ttu-id="dd0df-770">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-771">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-771">CC002</span></span></td>
<td><span data-ttu-id="dd0df-772">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-772">Finance</span></span></td>
<td><span data-ttu-id="dd0df-773">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-773">10001</span></span></td>
<td><span data-ttu-id="dd0df-774">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-774">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-775">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-775">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-776">175.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-776">175.00</span></span></td>
<td><span data-ttu-id="dd0df-777">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-778">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-778">CC003</span></span></td>
<td><span data-ttu-id="dd0df-779">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-779">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-780">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-780">10001</span></span></td>
<td><span data-ttu-id="dd0df-781">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-781">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-782">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-782">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-783">275.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-783">275.00</span></span></td>
<td><span data-ttu-id="dd0df-784">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-785">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-785">CC004</span></span></td>
<td><span data-ttu-id="dd0df-786">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-786">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-787">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-787">10001</span></span></td>
<td><span data-ttu-id="dd0df-788">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-788">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-789">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-789">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-790">50,00</span><span class="sxs-lookup"><span data-stu-id="dd0df-790">50,00</span></span></td>
<td><span data-ttu-id="dd0df-791">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-792">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-792">CC001</span></span></td>
<td><span data-ttu-id="dd0df-793">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="dd0df-793">HR</span></span></td>
<td><span data-ttu-id="dd0df-794">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-794">10001</span></span></td>
<td><span data-ttu-id="dd0df-795">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-795">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-796">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-796">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-797">-1,245.71</span></span></td>
<td><span data-ttu-id="dd0df-798">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-799">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-799">CC002</span></span></td>
<td><span data-ttu-id="dd0df-800">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-800">Finance</span></span></td>
<td><span data-ttu-id="dd0df-801">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-801">10001</span></span></td>
<td><span data-ttu-id="dd0df-802">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-802">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-803">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-803">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-804">436.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-804">436.00</span></span></td>
<td><span data-ttu-id="dd0df-805">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-806">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-806">CC003</span></span></td>
<td><span data-ttu-id="dd0df-807">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-807">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-808">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-808">10001</span></span></td>
<td><span data-ttu-id="dd0df-809">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-809">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-810">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-810">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-811">685.14</span><span class="sxs-lookup"><span data-stu-id="dd0df-811">685.14</span></span></td>
<td><span data-ttu-id="dd0df-812">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-813">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-813">CC004</span></span></td>
<td><span data-ttu-id="dd0df-814">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-814">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-815">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-815">10001</span></span></td>
<td><span data-ttu-id="dd0df-816">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-816">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-817">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-817">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-818">124.57</span><span class="sxs-lookup"><span data-stu-id="dd0df-818">124.57</span></span></td>
<td><span data-ttu-id="dd0df-819">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-820">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-820">CC002</span></span></td>
<td><span data-ttu-id="dd0df-821">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-821">Finance</span></span></td>
<td><span data-ttu-id="dd0df-822">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-822">10001</span></span></td>
<td><span data-ttu-id="dd0df-823">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-823">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-824">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-824">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-825">-675.00</span></span></td>
<td><span data-ttu-id="dd0df-826">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-827">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-827">CC003</span></span></td>
<td><span data-ttu-id="dd0df-828">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-828">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-829">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-829">10001</span></span></td>
<td><span data-ttu-id="dd0df-830">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-830">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-831">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-831">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-832">438.75</span><span class="sxs-lookup"><span data-stu-id="dd0df-832">438.75</span></span></td>
<td><span data-ttu-id="dd0df-833">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-834">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-834">CC004</span></span></td>
<td><span data-ttu-id="dd0df-835">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-835">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-836">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-836">10001</span></span></td>
<td><span data-ttu-id="dd0df-837">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-837">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-838">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-838">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-839">236.25</span><span class="sxs-lookup"><span data-stu-id="dd0df-839">236.25</span></span></td>
<td><span data-ttu-id="dd0df-840">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-841">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-841">CC002</span></span></td>
<td><span data-ttu-id="dd0df-842">การเงิน</span><span class="sxs-lookup"><span data-stu-id="dd0df-842">Finance</span></span></td>
<td><span data-ttu-id="dd0df-843">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-843">10001</span></span></td>
<td><span data-ttu-id="dd0df-844">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-844">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-845">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-845">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="dd0df-846">-8,150.29</span></span></td>
<td><span data-ttu-id="dd0df-847">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-848">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-848">CC003</span></span></td>
<td><span data-ttu-id="dd0df-849">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-849">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-850">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-850">10001</span></span></td>
<td><span data-ttu-id="dd0df-851">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-851">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-852">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-852">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="dd0df-853">5,297.69</span></span></td>
<td><span data-ttu-id="dd0df-854">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-855">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-855">CC004</span></span></td>
<td><span data-ttu-id="dd0df-856">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dd0df-856">Packaging</span></span></td>
<td><span data-ttu-id="dd0df-857">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-857">10001</span></span></td>
<td><span data-ttu-id="dd0df-858">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-858">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-859">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-859">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="dd0df-860">2,852.60</span></span></td>
<td><span data-ttu-id="dd0df-861">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-862">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-862">CC003</span></span></td>
<td><span data-ttu-id="dd0df-863">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-863">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-864">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-864">10001</span></span></td>
<td><span data-ttu-id="dd0df-865">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-865">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-866">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-866">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="dd0df-867">-713.75</span></span></td>
<td><span data-ttu-id="dd0df-868">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-869">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-869">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-870">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-870">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-871">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-871">10001</span></span></td>
<td><span data-ttu-id="dd0df-872">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-872">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-873">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-873">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-874">535.31</span><span class="sxs-lookup"><span data-stu-id="dd0df-874">535.31</span></span></td>
<td><span data-ttu-id="dd0df-875">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-876">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-876">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-877">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-877">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-878">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-878">10001</span></span></td>
<td><span data-ttu-id="dd0df-879">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-879">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-880">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-880">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-881">178.44</span><span class="sxs-lookup"><span data-stu-id="dd0df-881">178.44</span></span></td>
<td><span data-ttu-id="dd0df-882">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-883">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-883">CC003</span></span></td>
<td><span data-ttu-id="dd0df-884">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-884">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-885">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-885">10001</span></span></td>
<td><span data-ttu-id="dd0df-886">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-886">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-887">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-887">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="dd0df-888">-5,982.83</span></span></td>
<td><span data-ttu-id="dd0df-889">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-890">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-890">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-891">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-891">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-892">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-892">10001</span></span></td>
<td><span data-ttu-id="dd0df-893">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-893">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-894">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-894">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="dd0df-895">4,487.12</span></span></td>
<td><span data-ttu-id="dd0df-896">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-897">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-897">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-898">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-898">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-899">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-899">10001</span></span></td>
<td><span data-ttu-id="dd0df-900">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-900">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-901">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-901">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="dd0df-902">1,495.71</span></span></td>
<td><span data-ttu-id="dd0df-903">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-904">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-904">CC003</span></span></td>
<td><span data-ttu-id="dd0df-905">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-905">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-906">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-906">10001</span></span></td>
<td><span data-ttu-id="dd0df-907">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-907">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-908">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-908">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="dd0df-909">-286.25</span></span></td>
<td><span data-ttu-id="dd0df-910">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-911">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-911">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-912">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-912">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-913">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-913">10001</span></span></td>
<td><span data-ttu-id="dd0df-914">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-914">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-915">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-915">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-916">241.05</span><span class="sxs-lookup"><span data-stu-id="dd0df-916">241.05</span></span></td>
<td><span data-ttu-id="dd0df-917">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-918">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-918">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-919">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-919">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-920">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-920">10001</span></span></td>
<td><span data-ttu-id="dd0df-921">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-921">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-922">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-922">Fixed cost</span></span></td>
<td><span data-ttu-id="dd0df-923">45.20</span><span class="sxs-lookup"><span data-stu-id="dd0df-923">45.20</span></span></td>
<td><span data-ttu-id="dd0df-924">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-925">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-925">CC003</span></span></td>
<td><span data-ttu-id="dd0df-926">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="dd0df-926">Assembly</span></span></td>
<td><span data-ttu-id="dd0df-927">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-927">10001</span></span></td>
<td><span data-ttu-id="dd0df-928">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-928">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-929">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-929">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="dd0df-930">-2,977.17</span></span></td>
<td><span data-ttu-id="dd0df-931">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-932">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-932">Prod 1</span></span></td>
<td><span data-ttu-id="dd0df-933">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-933">Product 1</span></span></td>
<td><span data-ttu-id="dd0df-934">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-934">10001</span></span></td>
<td><span data-ttu-id="dd0df-935">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-935">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-936">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-936">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="dd0df-937">2,507.09</span></span></td>
<td><span data-ttu-id="dd0df-938">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd0df-939">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-939">Prod 2</span></span></td>
<td><span data-ttu-id="dd0df-940">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-940">Product 2</span></span></td>
<td><span data-ttu-id="dd0df-941">10001</span><span class="sxs-lookup"><span data-stu-id="dd0df-941">10001</span></span></td>
<td><span data-ttu-id="dd0df-942">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-942">Electricity</span></span></td>
<td><span data-ttu-id="dd0df-943">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-943">Variable cost</span></span></td>
<td><span data-ttu-id="dd0df-944">470.08</span><span class="sxs-lookup"><span data-stu-id="dd0df-944">470.08</span></span></td>
<td><span data-ttu-id="dd0df-945">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="dd0df-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="dd0df-946">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="dd0df-946">Conclusion</span></span>
<span data-ttu-id="dd0df-947">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="dd0df-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="dd0df-948">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="dd0df-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="dd0df-949">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="dd0df-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="dd0df-950">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="dd0df-951">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="dd0df-952">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="dd0df-953">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="dd0df-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dd0df-954">CC099</span><span class="sxs-lookup"><span data-stu-id="dd0df-954">CC099</span></span></th>
<th><span data-ttu-id="dd0df-955">CC001</span><span class="sxs-lookup"><span data-stu-id="dd0df-955">CC001</span></span></th>
<th><span data-ttu-id="dd0df-956">CC002</span><span class="sxs-lookup"><span data-stu-id="dd0df-956">CC002</span></span></th>
<th><span data-ttu-id="dd0df-957">CC003</span><span class="sxs-lookup"><span data-stu-id="dd0df-957">CC003</span></span></th>
<th><span data-ttu-id="dd0df-958">CC004</span><span class="sxs-lookup"><span data-stu-id="dd0df-958">CC004</span></span></th>
<th><span data-ttu-id="dd0df-959">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-959">Proj 1</span></span></th>
<th><span data-ttu-id="dd0df-960">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-960">Proj 2</span></span></th>
<th><span data-ttu-id="dd0df-961">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="dd0df-961">Prod 1</span></span></th>
<th><span data-ttu-id="dd0df-962">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="dd0df-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="dd0df-963">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="dd0df-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="dd0df-973">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="dd0df-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-974">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="dd0df-975">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="dd0df-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-976">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-977">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-978">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-979">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-980">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-981">776.36</span><span class="sxs-lookup"><span data-stu-id="dd0df-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-982">223.64</span><span class="sxs-lookup"><span data-stu-id="dd0df-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="dd0df-984">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="dd0df-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-985">000</span><span class="sxs-lookup"><span data-stu-id="dd0df-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-986">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-987">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-988">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-989">0.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-990">30.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-991">10.00</span><span class="sxs-lookup"><span data-stu-id="dd0df-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="dd0df-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="dd0df-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="dd0df-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="dd0df-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dd0df-995">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="dd0df-996">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="dd0df-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="dd0df-997">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="dd0df-998">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="dd0df-999">สำหรับข้อมูลเพิ่มเติม ให้ดูที่นโยบายการรวบรวมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dd0df-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="dd0df-1000">(หมายเหตุว่าหัวข้อนี้ยังไม่เสร็จสมบูรณ์ แต่ในไม่ช้านี้)</span><span class="sxs-lookup"><span data-stu-id="dd0df-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




