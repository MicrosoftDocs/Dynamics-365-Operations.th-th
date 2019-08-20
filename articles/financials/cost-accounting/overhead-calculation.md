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
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841500"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6c293-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6c293-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c293-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6c293-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6c293-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="6c293-105">Term definition</span></span>
---------------

<span data-ttu-id="6c293-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="6c293-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6c293-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="6c293-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6c293-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="6c293-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6c293-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="6c293-109">Rent</span></span>
-   <span data-ttu-id="6c293-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-110">Electricity</span></span>
-   <span data-ttu-id="6c293-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="6c293-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6c293-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6c293-112">Overhead calculation overview</span></span>
<span data-ttu-id="6c293-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6c293-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6c293-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6c293-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6c293-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="6c293-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6c293-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6c293-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6c293-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6c293-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c293-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6c293-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6c293-119">Version type</span></span>
-   <span data-ttu-id="6c293-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="6c293-120">Date and time</span></span>
-   <span data-ttu-id="6c293-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6c293-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-122">Fiscal year</span></span>
-   <span data-ttu-id="6c293-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-123">Fiscal period</span></span>

<span data-ttu-id="6c293-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="6c293-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6c293-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="6c293-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6c293-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6c293-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6c293-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6c293-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6c293-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6c293-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="6c293-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6c293-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="6c293-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6c293-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6c293-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6c293-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6c293-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6c293-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6c293-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6c293-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="6c293-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6c293-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="6c293-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6c293-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6c293-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="6c293-140">Main account</span></span></th>
<th><span data-ttu-id="6c293-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6c293-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-143">CC099</span></span></td>
<td><span data-ttu-id="6c293-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-144">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-145">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-145">10001</span></span></td>
<td><span data-ttu-id="6c293-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-146">Electricity</span></span></td>
<td><span data-ttu-id="6c293-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6c293-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6c293-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6c293-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="6c293-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6c293-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6c293-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="6c293-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6c293-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="6c293-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6c293-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="6c293-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6c293-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="6c293-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6c293-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6c293-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6c293-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6c293-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-160">Journal</span></span></th>
<th><span data-ttu-id="6c293-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6c293-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6c293-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6c293-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-164">00001</span><span class="sxs-lookup"><span data-stu-id="6c293-164">00001</span></span></td>
<td><span data-ttu-id="6c293-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6c293-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-166">Fiscal</span></span></td>
<td><span data-ttu-id="6c293-167">2017</span><span class="sxs-lookup"><span data-stu-id="6c293-167">2017</span></span></td>
<td><span data-ttu-id="6c293-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-168">Period 1</span></span></td>
<td><span data-ttu-id="6c293-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6c293-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="6c293-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-173">Cost element</span></span></th>
<th><span data-ttu-id="6c293-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6c293-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-177">CC099</span></span></td>
<td><span data-ttu-id="6c293-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-178">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-179">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-179">10001</span></span></td>
<td><span data-ttu-id="6c293-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-180">Electricity</span></span></td>
<td><span data-ttu-id="6c293-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6c293-181">Unclassified</span></span></td>
<td><span data-ttu-id="6c293-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6c293-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-185">Cost element</span></span></th>
<th><span data-ttu-id="6c293-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-187">Amount</span></span></th>
<th><span data-ttu-id="6c293-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-189">CC099</span></span></td>
<td><span data-ttu-id="6c293-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-190">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-191">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-191">10001</span></span></td>
<td><span data-ttu-id="6c293-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-192">Electricity</span></span></td>
<td><span data-ttu-id="6c293-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6c293-193">Unclassified</span></span></td>
<td><span data-ttu-id="6c293-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-194">10,000.00</span></span></td>
<td><span data-ttu-id="6c293-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-196">CC099</span></span></td>
<td><span data-ttu-id="6c293-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-197">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-198">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-198">10001</span></span></td>
<td><span data-ttu-id="6c293-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-199">Electricity</span></span></td>
<td><span data-ttu-id="6c293-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6c293-200">Unclassified</span></span></td>
<td><span data-ttu-id="6c293-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6c293-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-203">CC099</span></span></td>
<td><span data-ttu-id="6c293-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-204">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-205">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-205">10001</span></span></td>
<td><span data-ttu-id="6c293-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-206">Electricity</span></span></td>
<td><span data-ttu-id="6c293-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-208">1,000.00</span></span></td>
<td><span data-ttu-id="6c293-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-210">CC099</span></span></td>
<td><span data-ttu-id="6c293-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-211">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-212">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-212">10001</span></span></td>
<td><span data-ttu-id="6c293-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-213">Electricity</span></span></td>
<td><span data-ttu-id="6c293-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-214">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-215">9,000.00</span></span></td>
<td><span data-ttu-id="6c293-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6c293-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6c293-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6c293-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6c293-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6c293-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="6c293-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6c293-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6c293-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6c293-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6c293-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="6c293-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6c293-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="6c293-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6c293-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="6c293-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6c293-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6c293-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-228">Cost object</span></span></th>
<th><span data-ttu-id="6c293-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="6c293-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-230">CC001</span></span></td>
<td><span data-ttu-id="6c293-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-231">HR</span></span></td>
<td><span data-ttu-id="6c293-232">1,000</span><span class="sxs-lookup"><span data-stu-id="6c293-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-233">CC002</span></span></td>
<td><span data-ttu-id="6c293-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-234">Finance</span></span></td>
<td><span data-ttu-id="6c293-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6c293-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-236">CC003</span></span></td>
<td><span data-ttu-id="6c293-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-237">Assembly</span></span></td>
<td><span data-ttu-id="6c293-238">0</span><span class="sxs-lookup"><span data-stu-id="6c293-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-240">Cost object</span></span></th>
<th><span data-ttu-id="6c293-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-241">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-244">CC001</span></span></td>
<td><span data-ttu-id="6c293-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-245">HR</span></span></td>
<td><span data-ttu-id="6c293-246">1,000</span><span class="sxs-lookup"><span data-stu-id="6c293-246">1,000</span></span></td>
<td><span data-ttu-id="6c293-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6c293-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6c293-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-249">CC002</span></span></td>
<td><span data-ttu-id="6c293-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-250">Finance</span></span></td>
<td><span data-ttu-id="6c293-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6c293-251">6,000</span></span></td>
<td><span data-ttu-id="6c293-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6c293-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6c293-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-254">CC003</span></span></td>
<td><span data-ttu-id="6c293-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-255">Assembly</span></span></td>
<td><span data-ttu-id="6c293-256">0</span><span class="sxs-lookup"><span data-stu-id="6c293-256">0</span></span></td>
<td><span data-ttu-id="6c293-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6c293-258">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6c293-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-261">Cost object</span></span></th>
<th><span data-ttu-id="6c293-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="6c293-262">Formula</span></span></th>
<th><span data-ttu-id="6c293-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-263">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-266">CC001</span></span></td>
<td><span data-ttu-id="6c293-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-267">HR</span></span></td>
<td><span data-ttu-id="6c293-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6c293-269">1</span><span class="sxs-lookup"><span data-stu-id="6c293-269">1</span></span></td>
<td><span data-ttu-id="6c293-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6c293-271">500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-272">CC002</span></span></td>
<td><span data-ttu-id="6c293-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-273">Finance</span></span></td>
<td><span data-ttu-id="6c293-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6c293-275">1</span><span class="sxs-lookup"><span data-stu-id="6c293-275">1</span></span></td>
<td><span data-ttu-id="6c293-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6c293-277">500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-278">CC003</span></span></td>
<td><span data-ttu-id="6c293-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-279">Assembly</span></span></td>
<td><span data-ttu-id="6c293-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6c293-281">0</span><span class="sxs-lookup"><span data-stu-id="6c293-281">0</span></span></td>
<td><span data-ttu-id="6c293-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6c293-283">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6c293-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-285">Journal</span></span></th>
<th><span data-ttu-id="6c293-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6c293-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6c293-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6c293-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-289">00002</span><span class="sxs-lookup"><span data-stu-id="6c293-289">00002</span></span></td>
<td><span data-ttu-id="6c293-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6c293-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-291">Fiscal</span></span></td>
<td><span data-ttu-id="6c293-292">2017</span><span class="sxs-lookup"><span data-stu-id="6c293-292">2017</span></span></td>
<td><span data-ttu-id="6c293-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-293">Period 1</span></span></td>
<td><span data-ttu-id="6c293-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6c293-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="6c293-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-298">Cost element</span></span></th>
<th><span data-ttu-id="6c293-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-302">CC099</span></span></td>
<td><span data-ttu-id="6c293-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-303">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-304">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-304">10001</span></span></td>
<td><span data-ttu-id="6c293-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-305">Electricity</span></span></td>
<td><span data-ttu-id="6c293-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-309">CC099</span></span></td>
<td><span data-ttu-id="6c293-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-310">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-311">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-311">10001</span></span></td>
<td><span data-ttu-id="6c293-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-312">Electricity</span></span></td>
<td><span data-ttu-id="6c293-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-313">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6c293-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-317">Cost element</span></span></th>
<th><span data-ttu-id="6c293-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-319">Amount</span></span></th>
<th><span data-ttu-id="6c293-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-321">CC099</span></span></td>
<td><span data-ttu-id="6c293-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-322">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-323">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-323">10001</span></span></td>
<td><span data-ttu-id="6c293-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-324">Electricity</span></span></td>
<td><span data-ttu-id="6c293-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="6c293-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6c293-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-328">CC001</span></span></td>
<td><span data-ttu-id="6c293-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-329">HR</span></span></td>
<td><span data-ttu-id="6c293-330">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-330">10001</span></span></td>
<td><span data-ttu-id="6c293-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-331">Electricity</span></span></td>
<td><span data-ttu-id="6c293-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-333">500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-333">500.00</span></span></td>
<td><span data-ttu-id="6c293-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-335">CC002</span></span></td>
<td><span data-ttu-id="6c293-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-336">Finance</span></span></td>
<td><span data-ttu-id="6c293-337">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-337">10001</span></span></td>
<td><span data-ttu-id="6c293-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-338">Electricity</span></span></td>
<td><span data-ttu-id="6c293-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-340">500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-340">500.00</span></span></td>
<td><span data-ttu-id="6c293-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-342">CC099</span></span></td>
<td><span data-ttu-id="6c293-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c293-343">Default cost center</span></span></td>
<td><span data-ttu-id="6c293-344">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-344">10001</span></span></td>
<td><span data-ttu-id="6c293-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-345">Electricity</span></span></td>
<td><span data-ttu-id="6c293-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-346">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="6c293-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6c293-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-349">CC001</span></span></td>
<td><span data-ttu-id="6c293-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-350">HR</span></span></td>
<td><span data-ttu-id="6c293-351">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-351">10001</span></span></td>
<td><span data-ttu-id="6c293-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-352">Electricity</span></span></td>
<td><span data-ttu-id="6c293-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-353">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6c293-354">1,285.71</span></span></td>
<td><span data-ttu-id="6c293-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-356">CC002</span></span></td>
<td><span data-ttu-id="6c293-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-357">Finance</span></span></td>
<td><span data-ttu-id="6c293-358">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-358">10001</span></span></td>
<td><span data-ttu-id="6c293-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-359">Electricity</span></span></td>
<td><span data-ttu-id="6c293-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-360">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6c293-361">7,714.29</span></span></td>
<td><span data-ttu-id="6c293-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6c293-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6c293-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6c293-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6c293-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="6c293-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6c293-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="6c293-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6c293-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6c293-367">Define the overhead rate</span></span>

<span data-ttu-id="6c293-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="6c293-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6c293-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c293-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-370">Cost object</span></span></th>
<th><span data-ttu-id="6c293-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="6c293-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-372">Proj 1</span></span></td>
<td><span data-ttu-id="6c293-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-373">Project 1</span></span></td>
<td><span data-ttu-id="6c293-374">3</span><span class="sxs-lookup"><span data-stu-id="6c293-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-375">Proj 2</span></span></td>
<td><span data-ttu-id="6c293-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-376">Project 2</span></span></td>
<td><span data-ttu-id="6c293-377">1</span><span class="sxs-lookup"><span data-stu-id="6c293-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-379">Cost object</span></span></th>
<th><span data-ttu-id="6c293-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-380">Cost element</span></span></th>
<th><span data-ttu-id="6c293-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="6c293-382">Units</span></span></th>
<th><span data-ttu-id="6c293-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="6c293-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-384">CC001</span></span></td>
<td><span data-ttu-id="6c293-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-385">HR</span></span></td>
<td><span data-ttu-id="6c293-386">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-386">10001</span></span></td>
<td><span data-ttu-id="6c293-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-387">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-388">1</span><span class="sxs-lookup"><span data-stu-id="6c293-388">1</span></span></td>
<td><span data-ttu-id="6c293-389">10</span><span class="sxs-lookup"><span data-stu-id="6c293-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-391">Cost object</span></span></th>
<th><span data-ttu-id="6c293-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-392">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-393">Cost element</span></span></th>
<th><span data-ttu-id="6c293-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-396">Proj 1</span></span></td>
<td><span data-ttu-id="6c293-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-397">Project 1</span></span></td>
<td><span data-ttu-id="6c293-398">3</span><span class="sxs-lookup"><span data-stu-id="6c293-398">3</span></span></td>
<td><span data-ttu-id="6c293-399">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-399">10001</span></span></td>
<td><span data-ttu-id="6c293-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="6c293-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6c293-401">30.00</span><span class="sxs-lookup"><span data-stu-id="6c293-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-402">Proj 2</span></span></td>
<td><span data-ttu-id="6c293-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-403">Project 2</span></span></td>
<td><span data-ttu-id="6c293-404">1</span><span class="sxs-lookup"><span data-stu-id="6c293-404">1</span></span></td>
<td><span data-ttu-id="6c293-405">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-405">10001</span></span></td>
<td><span data-ttu-id="6c293-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="6c293-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6c293-407">10.00</span><span class="sxs-lookup"><span data-stu-id="6c293-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6c293-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-409">Journal</span></span></th>
<th><span data-ttu-id="6c293-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6c293-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6c293-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6c293-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-413">00003</span><span class="sxs-lookup"><span data-stu-id="6c293-413">00003</span></span></td>
<td><span data-ttu-id="6c293-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="6c293-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6c293-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-415">Fiscal</span></span></td>
<td><span data-ttu-id="6c293-416">2017</span><span class="sxs-lookup"><span data-stu-id="6c293-416">2017</span></span></td>
<td><span data-ttu-id="6c293-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-417">Period 1</span></span></td>
<td><span data-ttu-id="6c293-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6c293-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="6c293-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-421">Cost object</span></span></th>
<th><span data-ttu-id="6c293-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-424">Proj 1</span></span></td>
<td><span data-ttu-id="6c293-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="6c293-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6c293-426">3.00</span><span class="sxs-lookup"><span data-stu-id="6c293-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-428">Proj 2</span></span></td>
<td><span data-ttu-id="6c293-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="6c293-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6c293-430">1.00</span><span class="sxs-lookup"><span data-stu-id="6c293-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6c293-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-433">Cost element</span></span></th>
<th><span data-ttu-id="6c293-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-435">Amount</span></span></th>
<th><span data-ttu-id="6c293-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6c293-437">CC0001</span></span></td>
<td><span data-ttu-id="6c293-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-438">HR</span></span></td>
<td><span data-ttu-id="6c293-439">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-439">10001</span></span></td>
<td><span data-ttu-id="6c293-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-440">Electricity</span></span></td>
<td><span data-ttu-id="6c293-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-441">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="6c293-442">-30.00</span></span></td>
<td><span data-ttu-id="6c293-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-444">Proj 1</span></span></td>
<td><span data-ttu-id="6c293-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="6c293-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6c293-446">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-446">10001</span></span></td>
<td><span data-ttu-id="6c293-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-447">Electricity</span></span></td>
<td><span data-ttu-id="6c293-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-448">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-449">30.00</span><span class="sxs-lookup"><span data-stu-id="6c293-449">30.00</span></span></td>
<td><span data-ttu-id="6c293-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-451">CC001</span></span></td>
<td><span data-ttu-id="6c293-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-452">HR</span></span></td>
<td><span data-ttu-id="6c293-453">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-453">10001</span></span></td>
<td><span data-ttu-id="6c293-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-454">Electricity</span></span></td>
<td><span data-ttu-id="6c293-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-455">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="6c293-456">-10.00</span></span></td>
<td><span data-ttu-id="6c293-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-458">Proj 2</span></span></td>
<td><span data-ttu-id="6c293-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="6c293-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6c293-460">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-460">10001</span></span></td>
<td><span data-ttu-id="6c293-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-461">Electricity</span></span></td>
<td><span data-ttu-id="6c293-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-462">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-463">10.00</span><span class="sxs-lookup"><span data-stu-id="6c293-463">10.00</span></span></td>
<td><span data-ttu-id="6c293-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="6c293-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6c293-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6c293-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6c293-468">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="6c293-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="6c293-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6c293-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6c293-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6c293-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6c293-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="6c293-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6c293-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="6c293-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6c293-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6c293-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6c293-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6c293-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-475">Define the cost allocation</span></span>

<span data-ttu-id="6c293-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6c293-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6c293-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6c293-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c293-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-479">Cost object</span></span></th>
<th><span data-ttu-id="6c293-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="6c293-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-481">CC002</span></span></td>
<td><span data-ttu-id="6c293-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-482">Finance</span></span></td>
<td><span data-ttu-id="6c293-483">35</span><span class="sxs-lookup"><span data-stu-id="6c293-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-484">CC003</span></span></td>
<td><span data-ttu-id="6c293-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-485">Assembly</span></span></td>
<td><span data-ttu-id="6c293-486">55</span><span class="sxs-lookup"><span data-stu-id="6c293-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-487">CC004</span></span></td>
<td><span data-ttu-id="6c293-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-488">Packaging</span></span></td>
<td><span data-ttu-id="6c293-489">10</span><span class="sxs-lookup"><span data-stu-id="6c293-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6c293-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6c293-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c293-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-492">Cost object</span></span></th>
<th><span data-ttu-id="6c293-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-494">CC003</span></span></td>
<td><span data-ttu-id="6c293-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-495">Assembly</span></span></td>
<td><span data-ttu-id="6c293-496">65</span><span class="sxs-lookup"><span data-stu-id="6c293-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-497">CC004</span></span></td>
<td><span data-ttu-id="6c293-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-498">Packaging</span></span></td>
<td><span data-ttu-id="6c293-499">35</span><span class="sxs-lookup"><span data-stu-id="6c293-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6c293-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6c293-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c293-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-502">Cost object</span></span></th>
<th><span data-ttu-id="6c293-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="6c293-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-504">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-505">Product 1</span></span></td>
<td><span data-ttu-id="6c293-506">60</span><span class="sxs-lookup"><span data-stu-id="6c293-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-507">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-508">Product 2</span></span></td>
<td><span data-ttu-id="6c293-509">20</span><span class="sxs-lookup"><span data-stu-id="6c293-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="6c293-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6c293-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c293-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-512">Cost object</span></span></th>
<th><span data-ttu-id="6c293-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="6c293-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-514">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-515">Product 1</span></span></td>
<td><span data-ttu-id="6c293-516">80</span><span class="sxs-lookup"><span data-stu-id="6c293-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-517">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-518">Product 2</span></span></td>
<td><span data-ttu-id="6c293-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="6c293-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6c293-520">ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้ สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6c293-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6c293-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="6c293-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6c293-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6c293-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-523">Cost object</span></span></th>
<th><span data-ttu-id="6c293-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-524">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-526">Amount</span></span></th>
<th><span data-ttu-id="6c293-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-528">CC002</span></span></td>
<td><span data-ttu-id="6c293-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-529">Finance</span></span></td>
<td><span data-ttu-id="6c293-530">35</span><span class="sxs-lookup"><span data-stu-id="6c293-530">35</span></span></td>
<td><span data-ttu-id="6c293-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6c293-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6c293-532">175.00</span></span></td>
<td><span data-ttu-id="6c293-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-534">CC003</span></span></td>
<td><span data-ttu-id="6c293-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-535">Assembly</span></span></td>
<td><span data-ttu-id="6c293-536">55</span><span class="sxs-lookup"><span data-stu-id="6c293-536">55</span></span></td>
<td><span data-ttu-id="6c293-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6c293-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6c293-538">275.00</span></span></td>
<td><span data-ttu-id="6c293-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-540">CC004</span></span></td>
<td><span data-ttu-id="6c293-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-541">Packaging</span></span></td>
<td><span data-ttu-id="6c293-542">10</span><span class="sxs-lookup"><span data-stu-id="6c293-542">10</span></span></td>
<td><span data-ttu-id="6c293-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6c293-544">50.00</span><span class="sxs-lookup"><span data-stu-id="6c293-544">50.00</span></span></td>
<td><span data-ttu-id="6c293-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-546">CC002</span></span></td>
<td><span data-ttu-id="6c293-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-547">Finance</span></span></td>
<td><span data-ttu-id="6c293-548">35</span><span class="sxs-lookup"><span data-stu-id="6c293-548">35</span></span></td>
<td><span data-ttu-id="6c293-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6c293-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6c293-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6c293-550">436.00</span></span></td>
<td><span data-ttu-id="6c293-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-552">CC003</span></span></td>
<td><span data-ttu-id="6c293-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-553">Assembly</span></span></td>
<td><span data-ttu-id="6c293-554">55</span><span class="sxs-lookup"><span data-stu-id="6c293-554">55</span></span></td>
<td><span data-ttu-id="6c293-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6c293-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6c293-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6c293-556">685.14</span></span></td>
<td><span data-ttu-id="6c293-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-558">CC004</span></span></td>
<td><span data-ttu-id="6c293-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-559">Packaging</span></span></td>
<td><span data-ttu-id="6c293-560">10</span><span class="sxs-lookup"><span data-stu-id="6c293-560">10</span></span></td>
<td><span data-ttu-id="6c293-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="6c293-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6c293-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6c293-562">124.57</span></span></td>
<td><span data-ttu-id="6c293-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6c293-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-565">Cost object</span></span></th>
<th><span data-ttu-id="6c293-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-566">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-568">Amount</span></span></th>
<th><span data-ttu-id="6c293-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-570">CC003</span></span></td>
<td><span data-ttu-id="6c293-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-571">Assembly</span></span></td>
<td><span data-ttu-id="6c293-572">65</span><span class="sxs-lookup"><span data-stu-id="6c293-572">65</span></span></td>
<td><span data-ttu-id="6c293-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6c293-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6c293-574">438.75</span></span></td>
<td><span data-ttu-id="6c293-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-576">CC004</span></span></td>
<td><span data-ttu-id="6c293-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-577">Packaging</span></span></td>
<td><span data-ttu-id="6c293-578">35</span><span class="sxs-lookup"><span data-stu-id="6c293-578">35</span></span></td>
<td><span data-ttu-id="6c293-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6c293-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6c293-580">236.25</span></span></td>
<td><span data-ttu-id="6c293-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-582">CC003</span></span></td>
<td><span data-ttu-id="6c293-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-583">Assembly</span></span></td>
<td><span data-ttu-id="6c293-584">65</span><span class="sxs-lookup"><span data-stu-id="6c293-584">65</span></span></td>
<td><span data-ttu-id="6c293-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6c293-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6c293-586">5,297.69</span></span></td>
<td><span data-ttu-id="6c293-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-588">CC004</span></span></td>
<td><span data-ttu-id="6c293-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-589">Packaging</span></span></td>
<td><span data-ttu-id="6c293-590">35</span><span class="sxs-lookup"><span data-stu-id="6c293-590">35</span></span></td>
<td><span data-ttu-id="6c293-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="6c293-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6c293-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6c293-592">2,852.60</span></span></td>
<td><span data-ttu-id="6c293-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6c293-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-595">Cost object</span></span></th>
<th><span data-ttu-id="6c293-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-596">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-598">Amount</span></span></th>
<th><span data-ttu-id="6c293-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-600">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-601">Product 1</span></span></td>
<td><span data-ttu-id="6c293-602">60</span><span class="sxs-lookup"><span data-stu-id="6c293-602">60</span></span></td>
<td><span data-ttu-id="6c293-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="6c293-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6c293-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6c293-604">535.31</span></span></td>
<td><span data-ttu-id="6c293-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-606">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-607">Product 2</span></span></td>
<td><span data-ttu-id="6c293-608">20</span><span class="sxs-lookup"><span data-stu-id="6c293-608">20</span></span></td>
<td><span data-ttu-id="6c293-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="6c293-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6c293-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6c293-610">178.44</span></span></td>
<td><span data-ttu-id="6c293-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-612">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-613">Product 1</span></span></td>
<td><span data-ttu-id="6c293-614">60</span><span class="sxs-lookup"><span data-stu-id="6c293-614">60</span></span></td>
<td><span data-ttu-id="6c293-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="6c293-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6c293-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6c293-616">4,487.12</span></span></td>
<td><span data-ttu-id="6c293-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-618">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-619">Product 2</span></span></td>
<td><span data-ttu-id="6c293-620">20</span><span class="sxs-lookup"><span data-stu-id="6c293-620">20</span></span></td>
<td><span data-ttu-id="6c293-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="6c293-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6c293-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6c293-622">1,495.71</span></span></td>
<td><span data-ttu-id="6c293-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c293-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="6c293-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-625">Cost object</span></span></th>
<th><span data-ttu-id="6c293-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="6c293-626">Magnitude</span></span></th>
<th><span data-ttu-id="6c293-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="6c293-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6c293-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-628">Amount</span></span></th>
<th><span data-ttu-id="6c293-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-630">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-631">Product 1</span></span></td>
<td><span data-ttu-id="6c293-632">80</span><span class="sxs-lookup"><span data-stu-id="6c293-632">80</span></span></td>
<td><span data-ttu-id="6c293-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="6c293-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6c293-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6c293-634">241.05</span></span></td>
<td><span data-ttu-id="6c293-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-636">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-637">Product 2</span></span></td>
<td><span data-ttu-id="6c293-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="6c293-638">15</span></span></td>
<td><span data-ttu-id="6c293-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="6c293-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6c293-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6c293-640">45.20</span></span></td>
<td><span data-ttu-id="6c293-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-642">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-643">Product 1</span></span></td>
<td><span data-ttu-id="6c293-644">80</span><span class="sxs-lookup"><span data-stu-id="6c293-644">80</span></span></td>
<td><span data-ttu-id="6c293-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="6c293-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6c293-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6c293-646">2,507.09</span></span></td>
<td><span data-ttu-id="6c293-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-648">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-649">Product 2</span></span></td>
<td><span data-ttu-id="6c293-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="6c293-650">15</span></span></td>
<td><span data-ttu-id="6c293-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="6c293-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6c293-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6c293-652">470.08</span></span></td>
<td><span data-ttu-id="6c293-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6c293-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="6c293-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-655">Journal</span></span></th>
<th><span data-ttu-id="6c293-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6c293-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6c293-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="6c293-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-659">00004</span><span class="sxs-lookup"><span data-stu-id="6c293-659">00004</span></span></td>
<td><span data-ttu-id="6c293-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6c293-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-661">Fiscal</span></span></td>
<td><span data-ttu-id="6c293-662">2017</span><span class="sxs-lookup"><span data-stu-id="6c293-662">2017</span></span></td>
<td><span data-ttu-id="6c293-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-663">Period 1</span></span></td>
<td><span data-ttu-id="6c293-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="6c293-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6c293-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6c293-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6c293-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-668">Cost element</span></span></th>
<th><span data-ttu-id="6c293-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-672">CC001</span></span></td>
<td><span data-ttu-id="6c293-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-673">HR</span></span></td>
<td><span data-ttu-id="6c293-674">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-674">10001</span></span></td>
<td><span data-ttu-id="6c293-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-675">Electricity</span></span></td>
<td><span data-ttu-id="6c293-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-677">500.00</span><span class="sxs-lookup"><span data-stu-id="6c293-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-679">CC001</span></span></td>
<td><span data-ttu-id="6c293-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-680">HR</span></span></td>
<td><span data-ttu-id="6c293-681">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-681">10001</span></span></td>
<td><span data-ttu-id="6c293-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-682">Electricity</span></span></td>
<td><span data-ttu-id="6c293-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-683">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6c293-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-686">CC002</span></span></td>
<td><span data-ttu-id="6c293-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-687">Finance</span></span></td>
<td><span data-ttu-id="6c293-688">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-688">10001</span></span></td>
<td><span data-ttu-id="6c293-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-689">Electricity</span></span></td>
<td><span data-ttu-id="6c293-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6c293-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-693">CC002</span></span></td>
<td><span data-ttu-id="6c293-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-694">Finance</span></span></td>
<td><span data-ttu-id="6c293-695">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-695">10001</span></span></td>
<td><span data-ttu-id="6c293-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-696">Electricity</span></span></td>
<td><span data-ttu-id="6c293-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-697">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6c293-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-700">CC003</span></span></td>
<td><span data-ttu-id="6c293-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-701">Assembly</span></span></td>
<td><span data-ttu-id="6c293-702">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-702">10001</span></span></td>
<td><span data-ttu-id="6c293-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-703">Electricity</span></span></td>
<td><span data-ttu-id="6c293-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6c293-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-707">CC003</span></span></td>
<td><span data-ttu-id="6c293-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-708">Assembly</span></span></td>
<td><span data-ttu-id="6c293-709">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-709">10001</span></span></td>
<td><span data-ttu-id="6c293-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-710">Electricity</span></span></td>
<td><span data-ttu-id="6c293-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-711">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6c293-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-714">CC003</span></span></td>
<td><span data-ttu-id="6c293-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-715">Packaging</span></span></td>
<td><span data-ttu-id="6c293-716">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-716">10001</span></span></td>
<td><span data-ttu-id="6c293-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-717">Electricity</span></span></td>
<td><span data-ttu-id="6c293-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6c293-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-721">CC003</span></span></td>
<td><span data-ttu-id="6c293-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-722">Packaging</span></span></td>
<td><span data-ttu-id="6c293-723">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-723">10001</span></span></td>
<td><span data-ttu-id="6c293-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-724">Electricity</span></span></td>
<td><span data-ttu-id="6c293-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-725">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6c293-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-728">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-729">Product 1</span></span></td>
<td><span data-ttu-id="6c293-730">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-730">10001</span></span></td>
<td><span data-ttu-id="6c293-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-731">Electricity</span></span></td>
<td><span data-ttu-id="6c293-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6c293-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-735">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-736">Product 1</span></span></td>
<td><span data-ttu-id="6c293-737">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-737">10001</span></span></td>
<td><span data-ttu-id="6c293-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-738">Electricity</span></span></td>
<td><span data-ttu-id="6c293-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-739">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6c293-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-742">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-743">Product 1</span></span></td>
<td><span data-ttu-id="6c293-744">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-744">10001</span></span></td>
<td><span data-ttu-id="6c293-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-745">Electricity</span></span></td>
<td><span data-ttu-id="6c293-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6c293-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6c293-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-749">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-750">Product 1</span></span></td>
<td><span data-ttu-id="6c293-751">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-751">10001</span></span></td>
<td><span data-ttu-id="6c293-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-752">Electricity</span></span></td>
<td><span data-ttu-id="6c293-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-753">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6c293-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6c293-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6c293-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6c293-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-757">Cost element</span></span></th>
<th><span data-ttu-id="6c293-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6c293-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-759">Amount</span></span></th>
<th><span data-ttu-id="6c293-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="6c293-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c293-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-761">CC001</span></span></td>
<td><span data-ttu-id="6c293-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-762">HR</span></span></td>
<td><span data-ttu-id="6c293-763">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-763">10001</span></span></td>
<td><span data-ttu-id="6c293-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-764">Electricity</span></span></td>
<td><span data-ttu-id="6c293-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="6c293-766">-500.00</span></span></td>
<td><span data-ttu-id="6c293-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-768">CC002</span></span></td>
<td><span data-ttu-id="6c293-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-769">Finance</span></span></td>
<td><span data-ttu-id="6c293-770">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-770">10001</span></span></td>
<td><span data-ttu-id="6c293-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-771">Electricity</span></span></td>
<td><span data-ttu-id="6c293-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6c293-773">175.00</span></span></td>
<td><span data-ttu-id="6c293-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-775">CC003</span></span></td>
<td><span data-ttu-id="6c293-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-776">Assembly</span></span></td>
<td><span data-ttu-id="6c293-777">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-777">10001</span></span></td>
<td><span data-ttu-id="6c293-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-778">Electricity</span></span></td>
<td><span data-ttu-id="6c293-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6c293-780">275.00</span></span></td>
<td><span data-ttu-id="6c293-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-782">CC004</span></span></td>
<td><span data-ttu-id="6c293-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-783">Packaging</span></span></td>
<td><span data-ttu-id="6c293-784">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-784">10001</span></span></td>
<td><span data-ttu-id="6c293-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-785">Electricity</span></span></td>
<td><span data-ttu-id="6c293-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6c293-787">50,00</span></span></td>
<td><span data-ttu-id="6c293-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-789">CC001</span></span></td>
<td><span data-ttu-id="6c293-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c293-790">HR</span></span></td>
<td><span data-ttu-id="6c293-791">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-791">10001</span></span></td>
<td><span data-ttu-id="6c293-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-792">Electricity</span></span></td>
<td><span data-ttu-id="6c293-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-793">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="6c293-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6c293-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-796">CC002</span></span></td>
<td><span data-ttu-id="6c293-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-797">Finance</span></span></td>
<td><span data-ttu-id="6c293-798">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-798">10001</span></span></td>
<td><span data-ttu-id="6c293-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-799">Electricity</span></span></td>
<td><span data-ttu-id="6c293-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-800">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6c293-801">436.00</span></span></td>
<td><span data-ttu-id="6c293-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-803">CC003</span></span></td>
<td><span data-ttu-id="6c293-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-804">Assembly</span></span></td>
<td><span data-ttu-id="6c293-805">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-805">10001</span></span></td>
<td><span data-ttu-id="6c293-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-806">Electricity</span></span></td>
<td><span data-ttu-id="6c293-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-807">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6c293-808">685.14</span></span></td>
<td><span data-ttu-id="6c293-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-810">CC004</span></span></td>
<td><span data-ttu-id="6c293-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-811">Packaging</span></span></td>
<td><span data-ttu-id="6c293-812">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-812">10001</span></span></td>
<td><span data-ttu-id="6c293-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-813">Electricity</span></span></td>
<td><span data-ttu-id="6c293-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-814">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6c293-815">124.57</span></span></td>
<td><span data-ttu-id="6c293-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-817">CC002</span></span></td>
<td><span data-ttu-id="6c293-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-818">Finance</span></span></td>
<td><span data-ttu-id="6c293-819">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-819">10001</span></span></td>
<td><span data-ttu-id="6c293-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-820">Electricity</span></span></td>
<td><span data-ttu-id="6c293-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="6c293-822">-675.00</span></span></td>
<td><span data-ttu-id="6c293-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-824">CC003</span></span></td>
<td><span data-ttu-id="6c293-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-825">Assembly</span></span></td>
<td><span data-ttu-id="6c293-826">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-826">10001</span></span></td>
<td><span data-ttu-id="6c293-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-827">Electricity</span></span></td>
<td><span data-ttu-id="6c293-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6c293-829">438.75</span></span></td>
<td><span data-ttu-id="6c293-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-831">CC004</span></span></td>
<td><span data-ttu-id="6c293-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-832">Packaging</span></span></td>
<td><span data-ttu-id="6c293-833">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-833">10001</span></span></td>
<td><span data-ttu-id="6c293-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-834">Electricity</span></span></td>
<td><span data-ttu-id="6c293-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6c293-836">236.25</span></span></td>
<td><span data-ttu-id="6c293-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-838">CC002</span></span></td>
<td><span data-ttu-id="6c293-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="6c293-839">Finance</span></span></td>
<td><span data-ttu-id="6c293-840">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-840">10001</span></span></td>
<td><span data-ttu-id="6c293-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-841">Electricity</span></span></td>
<td><span data-ttu-id="6c293-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-842">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="6c293-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6c293-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-845">CC003</span></span></td>
<td><span data-ttu-id="6c293-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-846">Assembly</span></span></td>
<td><span data-ttu-id="6c293-847">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-847">10001</span></span></td>
<td><span data-ttu-id="6c293-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-848">Electricity</span></span></td>
<td><span data-ttu-id="6c293-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-849">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6c293-850">5,297.69</span></span></td>
<td><span data-ttu-id="6c293-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-852">CC004</span></span></td>
<td><span data-ttu-id="6c293-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6c293-853">Packaging</span></span></td>
<td><span data-ttu-id="6c293-854">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-854">10001</span></span></td>
<td><span data-ttu-id="6c293-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-855">Electricity</span></span></td>
<td><span data-ttu-id="6c293-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-856">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6c293-857">2,852.60</span></span></td>
<td><span data-ttu-id="6c293-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-859">CC003</span></span></td>
<td><span data-ttu-id="6c293-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-860">Assembly</span></span></td>
<td><span data-ttu-id="6c293-861">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-861">10001</span></span></td>
<td><span data-ttu-id="6c293-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-862">Electricity</span></span></td>
<td><span data-ttu-id="6c293-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="6c293-864">-713.75</span></span></td>
<td><span data-ttu-id="6c293-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-866">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-867">Product 1</span></span></td>
<td><span data-ttu-id="6c293-868">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-868">10001</span></span></td>
<td><span data-ttu-id="6c293-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-869">Electricity</span></span></td>
<td><span data-ttu-id="6c293-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6c293-871">535.31</span></span></td>
<td><span data-ttu-id="6c293-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-873">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-874">Product 2</span></span></td>
<td><span data-ttu-id="6c293-875">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-875">10001</span></span></td>
<td><span data-ttu-id="6c293-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-876">Electricity</span></span></td>
<td><span data-ttu-id="6c293-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6c293-878">178.44</span></span></td>
<td><span data-ttu-id="6c293-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-880">CC003</span></span></td>
<td><span data-ttu-id="6c293-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-881">Assembly</span></span></td>
<td><span data-ttu-id="6c293-882">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-882">10001</span></span></td>
<td><span data-ttu-id="6c293-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-883">Electricity</span></span></td>
<td><span data-ttu-id="6c293-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-884">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="6c293-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6c293-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-887">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-888">Product 1</span></span></td>
<td><span data-ttu-id="6c293-889">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-889">10001</span></span></td>
<td><span data-ttu-id="6c293-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-890">Electricity</span></span></td>
<td><span data-ttu-id="6c293-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-891">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6c293-892">4,487.12</span></span></td>
<td><span data-ttu-id="6c293-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-894">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-895">Product 2</span></span></td>
<td><span data-ttu-id="6c293-896">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-896">10001</span></span></td>
<td><span data-ttu-id="6c293-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-897">Electricity</span></span></td>
<td><span data-ttu-id="6c293-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-898">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6c293-899">1,495.71</span></span></td>
<td><span data-ttu-id="6c293-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-901">CC003</span></span></td>
<td><span data-ttu-id="6c293-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-902">Assembly</span></span></td>
<td><span data-ttu-id="6c293-903">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-903">10001</span></span></td>
<td><span data-ttu-id="6c293-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-904">Electricity</span></span></td>
<td><span data-ttu-id="6c293-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="6c293-906">-286.25</span></span></td>
<td><span data-ttu-id="6c293-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-908">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-909">Product 1</span></span></td>
<td><span data-ttu-id="6c293-910">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-910">10001</span></span></td>
<td><span data-ttu-id="6c293-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-911">Electricity</span></span></td>
<td><span data-ttu-id="6c293-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6c293-913">241.05</span></span></td>
<td><span data-ttu-id="6c293-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-915">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-916">Product 2</span></span></td>
<td><span data-ttu-id="6c293-917">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-917">10001</span></span></td>
<td><span data-ttu-id="6c293-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-918">Electricity</span></span></td>
<td><span data-ttu-id="6c293-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6c293-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6c293-920">45.20</span></span></td>
<td><span data-ttu-id="6c293-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-922">CC003</span></span></td>
<td><span data-ttu-id="6c293-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="6c293-923">Assembly</span></span></td>
<td><span data-ttu-id="6c293-924">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-924">10001</span></span></td>
<td><span data-ttu-id="6c293-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-925">Electricity</span></span></td>
<td><span data-ttu-id="6c293-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-926">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="6c293-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6c293-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-929">Prod 1</span></span></td>
<td><span data-ttu-id="6c293-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-930">Product 1</span></span></td>
<td><span data-ttu-id="6c293-931">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-931">10001</span></span></td>
<td><span data-ttu-id="6c293-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-932">Electricity</span></span></td>
<td><span data-ttu-id="6c293-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-933">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6c293-934">2,507.09</span></span></td>
<td><span data-ttu-id="6c293-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c293-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-936">Prod 2</span></span></td>
<td><span data-ttu-id="6c293-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-937">Product 2</span></span></td>
<td><span data-ttu-id="6c293-938">10001</span><span class="sxs-lookup"><span data-stu-id="6c293-938">10001</span></span></td>
<td><span data-ttu-id="6c293-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-939">Electricity</span></span></td>
<td><span data-ttu-id="6c293-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-940">Variable cost</span></span></td>
<td><span data-ttu-id="6c293-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6c293-941">470.08</span></span></td>
<td><span data-ttu-id="6c293-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="6c293-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6c293-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="6c293-943">Conclusion</span></span>
<span data-ttu-id="6c293-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="6c293-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6c293-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="6c293-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6c293-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="6c293-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6c293-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6c293-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6c293-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6c293-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="6c293-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c293-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6c293-951">CC099</span></span></th>
<th><span data-ttu-id="6c293-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6c293-952">CC001</span></span></th>
<th><span data-ttu-id="6c293-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6c293-953">CC002</span></span></th>
<th><span data-ttu-id="6c293-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6c293-954">CC003</span></span></th>
<th><span data-ttu-id="6c293-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6c293-955">CC004</span></span></th>
<th><span data-ttu-id="6c293-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-956">Proj 1</span></span></th>
<th><span data-ttu-id="6c293-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-957">Proj 2</span></span></th>
<th><span data-ttu-id="6c293-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="6c293-958">Prod 1</span></span></th>
<th><span data-ttu-id="6c293-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="6c293-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6c293-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="6c293-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6c293-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6c293-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="6c293-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-971">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6c293-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="6c293-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-973">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-974">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-975">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-976">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-977">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6c293-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6c293-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6c293-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6c293-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="6c293-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-982">000</span><span class="sxs-lookup"><span data-stu-id="6c293-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-983">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-984">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-985">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-986">0.00</span><span class="sxs-lookup"><span data-stu-id="6c293-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-987">30.00</span><span class="sxs-lookup"><span data-stu-id="6c293-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-988">10.00</span><span class="sxs-lookup"><span data-stu-id="6c293-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6c293-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6c293-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6c293-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6c293-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6c293-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6c293-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="6c293-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6c293-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6c293-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6c293-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6c293-996">สำหรับข้อมูลเพิ่มเติม ให้ดู [การรวบรวมต้นทุน](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="6c293-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



