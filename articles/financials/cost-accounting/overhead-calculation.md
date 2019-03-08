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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "335128"
---
# <a name="overhead-calculation"></a><span data-ttu-id="69f86-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="69f86-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69f86-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="69f86-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="69f86-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="69f86-105">Term definition</span></span>
---------------

<span data-ttu-id="69f86-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="69f86-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="69f86-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="69f86-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="69f86-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="69f86-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="69f86-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="69f86-109">Rent</span></span>
-   <span data-ttu-id="69f86-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-110">Electricity</span></span>
-   <span data-ttu-id="69f86-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="69f86-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="69f86-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="69f86-112">Overhead calculation overview</span></span>
<span data-ttu-id="69f86-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="69f86-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="69f86-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="69f86-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="69f86-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="69f86-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="69f86-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="69f86-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="69f86-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="69f86-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="69f86-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="69f86-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="69f86-119">Version type</span></span>
-   <span data-ttu-id="69f86-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="69f86-120">Date and time</span></span>
-   <span data-ttu-id="69f86-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="69f86-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-122">Fiscal year</span></span>
-   <span data-ttu-id="69f86-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-123">Fiscal period</span></span>

<span data-ttu-id="69f86-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="69f86-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="69f86-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="69f86-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="69f86-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="69f86-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="69f86-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="69f86-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="69f86-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="69f86-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="69f86-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="69f86-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="69f86-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="69f86-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="69f86-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="69f86-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="69f86-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="69f86-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="69f86-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="69f86-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="69f86-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="69f86-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="69f86-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="69f86-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="69f86-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="69f86-140">Main account</span></span></th>
<th><span data-ttu-id="69f86-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="69f86-143">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-143">CC099</span></span></td>
<td><span data-ttu-id="69f86-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-144">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-145">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-145">10001</span></span></td>
<td><span data-ttu-id="69f86-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-146">Electricity</span></span></td>
<td><span data-ttu-id="69f86-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="69f86-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="69f86-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="69f86-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="69f86-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="69f86-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-151">Define the cost behavior rule</span></span>

<span data-ttu-id="69f86-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="69f86-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="69f86-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="69f86-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="69f86-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="69f86-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="69f86-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="69f86-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="69f86-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="69f86-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="69f86-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="69f86-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-160">Journal</span></span></th>
<th><span data-ttu-id="69f86-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="69f86-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="69f86-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="69f86-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-164">00001</span><span class="sxs-lookup"><span data-stu-id="69f86-164">00001</span></span></td>
<td><span data-ttu-id="69f86-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="69f86-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-166">Fiscal</span></span></td>
<td><span data-ttu-id="69f86-167">2017</span><span class="sxs-lookup"><span data-stu-id="69f86-167">2017</span></span></td>
<td><span data-ttu-id="69f86-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-168">Period 1</span></span></td>
<td><span data-ttu-id="69f86-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="69f86-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="69f86-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-173">Cost element</span></span></th>
<th><span data-ttu-id="69f86-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-174">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="69f86-177">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-177">CC099</span></span></td>
<td><span data-ttu-id="69f86-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-178">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-179">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-179">10001</span></span></td>
<td><span data-ttu-id="69f86-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-180">Electricity</span></span></td>
<td><span data-ttu-id="69f86-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="69f86-181">Unclassified</span></span></td>
<td><span data-ttu-id="69f86-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="69f86-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-185">Cost element</span></span></th>
<th><span data-ttu-id="69f86-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-186">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-187">Amount</span></span></th>
<th><span data-ttu-id="69f86-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-189">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-189">CC099</span></span></td>
<td><span data-ttu-id="69f86-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-190">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-191">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-191">10001</span></span></td>
<td><span data-ttu-id="69f86-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-192">Electricity</span></span></td>
<td><span data-ttu-id="69f86-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="69f86-193">Unclassified</span></span></td>
<td><span data-ttu-id="69f86-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-194">10,000.00</span></span></td>
<td><span data-ttu-id="69f86-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-196">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-196">CC099</span></span></td>
<td><span data-ttu-id="69f86-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-197">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-198">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-198">10001</span></span></td>
<td><span data-ttu-id="69f86-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-199">Electricity</span></span></td>
<td><span data-ttu-id="69f86-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="69f86-200">Unclassified</span></span></td>
<td><span data-ttu-id="69f86-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-201">-10,000.00</span></span></td>
<td><span data-ttu-id="69f86-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-203">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-203">CC099</span></span></td>
<td><span data-ttu-id="69f86-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-204">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-205">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-205">10001</span></span></td>
<td><span data-ttu-id="69f86-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-206">Electricity</span></span></td>
<td><span data-ttu-id="69f86-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-207">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-208">1,000.00</span></span></td>
<td><span data-ttu-id="69f86-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-210">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-210">CC099</span></span></td>
<td><span data-ttu-id="69f86-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-211">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-212">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-212">10001</span></span></td>
<td><span data-ttu-id="69f86-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-213">Electricity</span></span></td>
<td><span data-ttu-id="69f86-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-214">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-215">9,000.00</span></span></td>
<td><span data-ttu-id="69f86-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="69f86-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="69f86-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="69f86-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="69f86-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="69f86-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="69f86-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="69f86-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-221">Define the cost distribution rule</span></span>

<span data-ttu-id="69f86-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="69f86-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="69f86-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="69f86-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="69f86-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="69f86-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="69f86-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="69f86-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="69f86-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="69f86-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-228">Cost object</span></span></th>
<th><span data-ttu-id="69f86-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="69f86-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-230">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-230">CC001</span></span></td>
<td><span data-ttu-id="69f86-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-231">HR</span></span></td>
<td><span data-ttu-id="69f86-232">1,000</span><span class="sxs-lookup"><span data-stu-id="69f86-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-233">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-233">CC002</span></span></td>
<td><span data-ttu-id="69f86-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-234">Finance</span></span></td>
<td><span data-ttu-id="69f86-235">6,000</span><span class="sxs-lookup"><span data-stu-id="69f86-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-236">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-236">CC003</span></span></td>
<td><span data-ttu-id="69f86-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-237">Assembly</span></span></td>
<td><span data-ttu-id="69f86-238">0</span><span class="sxs-lookup"><span data-stu-id="69f86-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-240">Cost object</span></span></th>
<th><span data-ttu-id="69f86-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-241">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-242">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-244">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-244">CC001</span></span></td>
<td><span data-ttu-id="69f86-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-245">HR</span></span></td>
<td><span data-ttu-id="69f86-246">1,000</span><span class="sxs-lookup"><span data-stu-id="69f86-246">1,000</span></span></td>
<td><span data-ttu-id="69f86-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="69f86-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="69f86-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-249">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-249">CC002</span></span></td>
<td><span data-ttu-id="69f86-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-250">Finance</span></span></td>
<td><span data-ttu-id="69f86-251">6,000</span><span class="sxs-lookup"><span data-stu-id="69f86-251">6,000</span></span></td>
<td><span data-ttu-id="69f86-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="69f86-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="69f86-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-254">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-254">CC003</span></span></td>
<td><span data-ttu-id="69f86-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-255">Assembly</span></span></td>
<td><span data-ttu-id="69f86-256">0</span><span class="sxs-lookup"><span data-stu-id="69f86-256">0</span></span></td>
<td><span data-ttu-id="69f86-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="69f86-258">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="69f86-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-261">Cost object</span></span></th>
<th><span data-ttu-id="69f86-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="69f86-262">Formula</span></span></th>
<th><span data-ttu-id="69f86-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-263">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-264">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-266">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-266">CC001</span></span></td>
<td><span data-ttu-id="69f86-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-267">HR</span></span></td>
<td><span data-ttu-id="69f86-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="69f86-269">1</span><span class="sxs-lookup"><span data-stu-id="69f86-269">1</span></span></td>
<td><span data-ttu-id="69f86-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="69f86-271">500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-272">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-272">CC002</span></span></td>
<td><span data-ttu-id="69f86-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-273">Finance</span></span></td>
<td><span data-ttu-id="69f86-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="69f86-275">1</span><span class="sxs-lookup"><span data-stu-id="69f86-275">1</span></span></td>
<td><span data-ttu-id="69f86-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="69f86-277">500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-278">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-278">CC003</span></span></td>
<td><span data-ttu-id="69f86-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-279">Assembly</span></span></td>
<td><span data-ttu-id="69f86-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="69f86-281">0</span><span class="sxs-lookup"><span data-stu-id="69f86-281">0</span></span></td>
<td><span data-ttu-id="69f86-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="69f86-283">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="69f86-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-285">Journal</span></span></th>
<th><span data-ttu-id="69f86-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="69f86-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="69f86-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="69f86-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-289">00002</span><span class="sxs-lookup"><span data-stu-id="69f86-289">00002</span></span></td>
<td><span data-ttu-id="69f86-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="69f86-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-291">Fiscal</span></span></td>
<td><span data-ttu-id="69f86-292">2017</span><span class="sxs-lookup"><span data-stu-id="69f86-292">2017</span></span></td>
<td><span data-ttu-id="69f86-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-293">Period 1</span></span></td>
<td><span data-ttu-id="69f86-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="69f86-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="69f86-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-298">Cost element</span></span></th>
<th><span data-ttu-id="69f86-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-299">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-302">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-302">CC099</span></span></td>
<td><span data-ttu-id="69f86-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-303">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-304">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-304">10001</span></span></td>
<td><span data-ttu-id="69f86-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-305">Electricity</span></span></td>
<td><span data-ttu-id="69f86-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-306">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-309">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-309">CC099</span></span></td>
<td><span data-ttu-id="69f86-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-310">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-311">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-311">10001</span></span></td>
<td><span data-ttu-id="69f86-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-312">Electricity</span></span></td>
<td><span data-ttu-id="69f86-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-313">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="69f86-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-317">Cost element</span></span></th>
<th><span data-ttu-id="69f86-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-318">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-319">Amount</span></span></th>
<th><span data-ttu-id="69f86-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-321">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-321">CC099</span></span></td>
<td><span data-ttu-id="69f86-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-322">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-323">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-323">10001</span></span></td>
<td><span data-ttu-id="69f86-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-324">Electricity</span></span></td>
<td><span data-ttu-id="69f86-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-325">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="69f86-326">-1,000.00</span></span></td>
<td><span data-ttu-id="69f86-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-328">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-328">CC001</span></span></td>
<td><span data-ttu-id="69f86-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-329">HR</span></span></td>
<td><span data-ttu-id="69f86-330">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-330">10001</span></span></td>
<td><span data-ttu-id="69f86-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-331">Electricity</span></span></td>
<td><span data-ttu-id="69f86-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-332">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-333">500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-333">500.00</span></span></td>
<td><span data-ttu-id="69f86-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-335">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-335">CC002</span></span></td>
<td><span data-ttu-id="69f86-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-336">Finance</span></span></td>
<td><span data-ttu-id="69f86-337">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-337">10001</span></span></td>
<td><span data-ttu-id="69f86-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-338">Electricity</span></span></td>
<td><span data-ttu-id="69f86-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-339">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-340">500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-340">500.00</span></span></td>
<td><span data-ttu-id="69f86-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-342">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-342">CC099</span></span></td>
<td><span data-ttu-id="69f86-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="69f86-343">Default cost center</span></span></td>
<td><span data-ttu-id="69f86-344">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-344">10001</span></span></td>
<td><span data-ttu-id="69f86-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-345">Electricity</span></span></td>
<td><span data-ttu-id="69f86-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-346">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="69f86-347">-9,000.00</span></span></td>
<td><span data-ttu-id="69f86-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-349">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-349">CC001</span></span></td>
<td><span data-ttu-id="69f86-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-350">HR</span></span></td>
<td><span data-ttu-id="69f86-351">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-351">10001</span></span></td>
<td><span data-ttu-id="69f86-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-352">Electricity</span></span></td>
<td><span data-ttu-id="69f86-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-353">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="69f86-354">1,285.71</span></span></td>
<td><span data-ttu-id="69f86-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-356">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-356">CC002</span></span></td>
<td><span data-ttu-id="69f86-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-357">Finance</span></span></td>
<td><span data-ttu-id="69f86-358">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-358">10001</span></span></td>
<td><span data-ttu-id="69f86-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-359">Electricity</span></span></td>
<td><span data-ttu-id="69f86-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-360">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="69f86-361">7,714.29</span></span></td>
<td><span data-ttu-id="69f86-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="69f86-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="69f86-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="69f86-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="69f86-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="69f86-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="69f86-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="69f86-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="69f86-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="69f86-367">Define the overhead rate</span></span>

<span data-ttu-id="69f86-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="69f86-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="69f86-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="69f86-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-370">Cost object</span></span></th>
<th><span data-ttu-id="69f86-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="69f86-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-372">Proj 1</span></span></td>
<td><span data-ttu-id="69f86-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-373">Project 1</span></span></td>
<td><span data-ttu-id="69f86-374">3</span><span class="sxs-lookup"><span data-stu-id="69f86-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-375">Proj 2</span></span></td>
<td><span data-ttu-id="69f86-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-376">Project 2</span></span></td>
<td><span data-ttu-id="69f86-377">1</span><span class="sxs-lookup"><span data-stu-id="69f86-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-379">Cost object</span></span></th>
<th><span data-ttu-id="69f86-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-380">Cost element</span></span></th>
<th><span data-ttu-id="69f86-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-381">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="69f86-382">Units</span></span></th>
<th><span data-ttu-id="69f86-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="69f86-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-384">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-384">CC001</span></span></td>
<td><span data-ttu-id="69f86-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-385">HR</span></span></td>
<td><span data-ttu-id="69f86-386">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-386">10001</span></span></td>
<td><span data-ttu-id="69f86-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-387">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-388">1</span><span class="sxs-lookup"><span data-stu-id="69f86-388">1</span></span></td>
<td><span data-ttu-id="69f86-389">10</span><span class="sxs-lookup"><span data-stu-id="69f86-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-391">Cost object</span></span></th>
<th><span data-ttu-id="69f86-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-392">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-393">Cost element</span></span></th>
<th><span data-ttu-id="69f86-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-394">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-396">Proj 1</span></span></td>
<td><span data-ttu-id="69f86-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-397">Project 1</span></span></td>
<td><span data-ttu-id="69f86-398">3</span><span class="sxs-lookup"><span data-stu-id="69f86-398">3</span></span></td>
<td><span data-ttu-id="69f86-399">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-399">10001</span></span></td>
<td><span data-ttu-id="69f86-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="69f86-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="69f86-401">30.00</span><span class="sxs-lookup"><span data-stu-id="69f86-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-402">Proj 2</span></span></td>
<td><span data-ttu-id="69f86-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-403">Project 2</span></span></td>
<td><span data-ttu-id="69f86-404">1</span><span class="sxs-lookup"><span data-stu-id="69f86-404">1</span></span></td>
<td><span data-ttu-id="69f86-405">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-405">10001</span></span></td>
<td><span data-ttu-id="69f86-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="69f86-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="69f86-407">10.00</span><span class="sxs-lookup"><span data-stu-id="69f86-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="69f86-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-409">Journal</span></span></th>
<th><span data-ttu-id="69f86-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="69f86-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="69f86-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="69f86-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-413">00003</span><span class="sxs-lookup"><span data-stu-id="69f86-413">00003</span></span></td>
<td><span data-ttu-id="69f86-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="69f86-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="69f86-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-415">Fiscal</span></span></td>
<td><span data-ttu-id="69f86-416">2017</span><span class="sxs-lookup"><span data-stu-id="69f86-416">2017</span></span></td>
<td><span data-ttu-id="69f86-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-417">Period 1</span></span></td>
<td><span data-ttu-id="69f86-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="69f86-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="69f86-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-421">Cost object</span></span></th>
<th><span data-ttu-id="69f86-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-424">Proj 1</span></span></td>
<td><span data-ttu-id="69f86-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="69f86-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="69f86-426">3.00</span><span class="sxs-lookup"><span data-stu-id="69f86-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-428">Proj 2</span></span></td>
<td><span data-ttu-id="69f86-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="69f86-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="69f86-430">1.00</span><span class="sxs-lookup"><span data-stu-id="69f86-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="69f86-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-433">Cost element</span></span></th>
<th><span data-ttu-id="69f86-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-434">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-435">Amount</span></span></th>
<th><span data-ttu-id="69f86-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="69f86-437">CC0001</span></span></td>
<td><span data-ttu-id="69f86-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-438">HR</span></span></td>
<td><span data-ttu-id="69f86-439">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-439">10001</span></span></td>
<td><span data-ttu-id="69f86-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-440">Electricity</span></span></td>
<td><span data-ttu-id="69f86-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-441">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="69f86-442">-30.00</span></span></td>
<td><span data-ttu-id="69f86-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-444">Proj 1</span></span></td>
<td><span data-ttu-id="69f86-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="69f86-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="69f86-446">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-446">10001</span></span></td>
<td><span data-ttu-id="69f86-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-447">Electricity</span></span></td>
<td><span data-ttu-id="69f86-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-448">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-449">30.00</span><span class="sxs-lookup"><span data-stu-id="69f86-449">30.00</span></span></td>
<td><span data-ttu-id="69f86-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-451">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-451">CC001</span></span></td>
<td><span data-ttu-id="69f86-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-452">HR</span></span></td>
<td><span data-ttu-id="69f86-453">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-453">10001</span></span></td>
<td><span data-ttu-id="69f86-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-454">Electricity</span></span></td>
<td><span data-ttu-id="69f86-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-455">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="69f86-456">-10.00</span></span></td>
<td><span data-ttu-id="69f86-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-458">Proj 2</span></span></td>
<td><span data-ttu-id="69f86-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="69f86-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="69f86-460">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-460">10001</span></span></td>
<td><span data-ttu-id="69f86-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-461">Electricity</span></span></td>
<td><span data-ttu-id="69f86-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-462">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-463">10.00</span><span class="sxs-lookup"><span data-stu-id="69f86-463">10.00</span></span></td>
<td><span data-ttu-id="69f86-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="69f86-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="69f86-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="69f86-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="69f86-468">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="69f86-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="69f86-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="69f86-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="69f86-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="69f86-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="69f86-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="69f86-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="69f86-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="69f86-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="69f86-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="69f86-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="69f86-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="69f86-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-475">Define the cost allocation</span></span>

<span data-ttu-id="69f86-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="69f86-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="69f86-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="69f86-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="69f86-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-479">Cost object</span></span></th>
<th><span data-ttu-id="69f86-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="69f86-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-481">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-481">CC002</span></span></td>
<td><span data-ttu-id="69f86-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-482">Finance</span></span></td>
<td><span data-ttu-id="69f86-483">35</span><span class="sxs-lookup"><span data-stu-id="69f86-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-484">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-484">CC003</span></span></td>
<td><span data-ttu-id="69f86-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-485">Assembly</span></span></td>
<td><span data-ttu-id="69f86-486">55</span><span class="sxs-lookup"><span data-stu-id="69f86-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-487">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-487">CC004</span></span></td>
<td><span data-ttu-id="69f86-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-488">Packaging</span></span></td>
<td><span data-ttu-id="69f86-489">10</span><span class="sxs-lookup"><span data-stu-id="69f86-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="69f86-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="69f86-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="69f86-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-492">Cost object</span></span></th>
<th><span data-ttu-id="69f86-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-494">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-494">CC003</span></span></td>
<td><span data-ttu-id="69f86-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-495">Assembly</span></span></td>
<td><span data-ttu-id="69f86-496">65</span><span class="sxs-lookup"><span data-stu-id="69f86-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-497">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-497">CC004</span></span></td>
<td><span data-ttu-id="69f86-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-498">Packaging</span></span></td>
<td><span data-ttu-id="69f86-499">35</span><span class="sxs-lookup"><span data-stu-id="69f86-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="69f86-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="69f86-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="69f86-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-502">Cost object</span></span></th>
<th><span data-ttu-id="69f86-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="69f86-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-504">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-505">Product 1</span></span></td>
<td><span data-ttu-id="69f86-506">60</span><span class="sxs-lookup"><span data-stu-id="69f86-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-507">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-508">Product 2</span></span></td>
<td><span data-ttu-id="69f86-509">20</span><span class="sxs-lookup"><span data-stu-id="69f86-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="69f86-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="69f86-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="69f86-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-512">Cost object</span></span></th>
<th><span data-ttu-id="69f86-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="69f86-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-514">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-515">Product 1</span></span></td>
<td><span data-ttu-id="69f86-516">80</span><span class="sxs-lookup"><span data-stu-id="69f86-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-517">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-518">Product 2</span></span></td>
<td><span data-ttu-id="69f86-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="69f86-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="69f86-520">ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้ สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69f86-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="69f86-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="69f86-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="69f86-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="69f86-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-523">Cost object</span></span></th>
<th><span data-ttu-id="69f86-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-524">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-525">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-526">Amount</span></span></th>
<th><span data-ttu-id="69f86-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-528">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-528">CC002</span></span></td>
<td><span data-ttu-id="69f86-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-529">Finance</span></span></td>
<td><span data-ttu-id="69f86-530">35</span><span class="sxs-lookup"><span data-stu-id="69f86-530">35</span></span></td>
<td><span data-ttu-id="69f86-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="69f86-532">175.00</span><span class="sxs-lookup"><span data-stu-id="69f86-532">175.00</span></span></td>
<td><span data-ttu-id="69f86-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-534">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-534">CC003</span></span></td>
<td><span data-ttu-id="69f86-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-535">Assembly</span></span></td>
<td><span data-ttu-id="69f86-536">55</span><span class="sxs-lookup"><span data-stu-id="69f86-536">55</span></span></td>
<td><span data-ttu-id="69f86-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="69f86-538">275.00</span><span class="sxs-lookup"><span data-stu-id="69f86-538">275.00</span></span></td>
<td><span data-ttu-id="69f86-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-540">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-540">CC004</span></span></td>
<td><span data-ttu-id="69f86-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-541">Packaging</span></span></td>
<td><span data-ttu-id="69f86-542">10</span><span class="sxs-lookup"><span data-stu-id="69f86-542">10</span></span></td>
<td><span data-ttu-id="69f86-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="69f86-544">50.00</span><span class="sxs-lookup"><span data-stu-id="69f86-544">50.00</span></span></td>
<td><span data-ttu-id="69f86-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-546">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-546">CC002</span></span></td>
<td><span data-ttu-id="69f86-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-547">Finance</span></span></td>
<td><span data-ttu-id="69f86-548">35</span><span class="sxs-lookup"><span data-stu-id="69f86-548">35</span></span></td>
<td><span data-ttu-id="69f86-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="69f86-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="69f86-550">436.00</span><span class="sxs-lookup"><span data-stu-id="69f86-550">436.00</span></span></td>
<td><span data-ttu-id="69f86-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-552">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-552">CC003</span></span></td>
<td><span data-ttu-id="69f86-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-553">Assembly</span></span></td>
<td><span data-ttu-id="69f86-554">55</span><span class="sxs-lookup"><span data-stu-id="69f86-554">55</span></span></td>
<td><span data-ttu-id="69f86-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="69f86-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="69f86-556">685.14</span><span class="sxs-lookup"><span data-stu-id="69f86-556">685.14</span></span></td>
<td><span data-ttu-id="69f86-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-558">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-558">CC004</span></span></td>
<td><span data-ttu-id="69f86-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-559">Packaging</span></span></td>
<td><span data-ttu-id="69f86-560">10</span><span class="sxs-lookup"><span data-stu-id="69f86-560">10</span></span></td>
<td><span data-ttu-id="69f86-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="69f86-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="69f86-562">124.57</span><span class="sxs-lookup"><span data-stu-id="69f86-562">124.57</span></span></td>
<td><span data-ttu-id="69f86-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="69f86-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-565">Cost object</span></span></th>
<th><span data-ttu-id="69f86-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-566">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-567">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-568">Amount</span></span></th>
<th><span data-ttu-id="69f86-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-570">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-570">CC003</span></span></td>
<td><span data-ttu-id="69f86-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-571">Assembly</span></span></td>
<td><span data-ttu-id="69f86-572">65</span><span class="sxs-lookup"><span data-stu-id="69f86-572">65</span></span></td>
<td><span data-ttu-id="69f86-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="69f86-574">438.75</span><span class="sxs-lookup"><span data-stu-id="69f86-574">438.75</span></span></td>
<td><span data-ttu-id="69f86-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-576">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-576">CC004</span></span></td>
<td><span data-ttu-id="69f86-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-577">Packaging</span></span></td>
<td><span data-ttu-id="69f86-578">35</span><span class="sxs-lookup"><span data-stu-id="69f86-578">35</span></span></td>
<td><span data-ttu-id="69f86-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="69f86-580">236.25</span><span class="sxs-lookup"><span data-stu-id="69f86-580">236.25</span></span></td>
<td><span data-ttu-id="69f86-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-582">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-582">CC003</span></span></td>
<td><span data-ttu-id="69f86-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-583">Assembly</span></span></td>
<td><span data-ttu-id="69f86-584">65</span><span class="sxs-lookup"><span data-stu-id="69f86-584">65</span></span></td>
<td><span data-ttu-id="69f86-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="69f86-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="69f86-586">5,297.69</span></span></td>
<td><span data-ttu-id="69f86-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-588">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-588">CC004</span></span></td>
<td><span data-ttu-id="69f86-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-589">Packaging</span></span></td>
<td><span data-ttu-id="69f86-590">35</span><span class="sxs-lookup"><span data-stu-id="69f86-590">35</span></span></td>
<td><span data-ttu-id="69f86-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="69f86-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="69f86-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="69f86-592">2,852.60</span></span></td>
<td><span data-ttu-id="69f86-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="69f86-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-595">Cost object</span></span></th>
<th><span data-ttu-id="69f86-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-596">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-597">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-598">Amount</span></span></th>
<th><span data-ttu-id="69f86-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-600">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-601">Product 1</span></span></td>
<td><span data-ttu-id="69f86-602">60</span><span class="sxs-lookup"><span data-stu-id="69f86-602">60</span></span></td>
<td><span data-ttu-id="69f86-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="69f86-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="69f86-604">535.31</span><span class="sxs-lookup"><span data-stu-id="69f86-604">535.31</span></span></td>
<td><span data-ttu-id="69f86-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-606">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-607">Product 2</span></span></td>
<td><span data-ttu-id="69f86-608">20</span><span class="sxs-lookup"><span data-stu-id="69f86-608">20</span></span></td>
<td><span data-ttu-id="69f86-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="69f86-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="69f86-610">178.44</span><span class="sxs-lookup"><span data-stu-id="69f86-610">178.44</span></span></td>
<td><span data-ttu-id="69f86-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-612">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-613">Product 1</span></span></td>
<td><span data-ttu-id="69f86-614">60</span><span class="sxs-lookup"><span data-stu-id="69f86-614">60</span></span></td>
<td><span data-ttu-id="69f86-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="69f86-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="69f86-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="69f86-616">4,487.12</span></span></td>
<td><span data-ttu-id="69f86-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-618">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-619">Product 2</span></span></td>
<td><span data-ttu-id="69f86-620">20</span><span class="sxs-lookup"><span data-stu-id="69f86-620">20</span></span></td>
<td><span data-ttu-id="69f86-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="69f86-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="69f86-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="69f86-622">1,495.71</span></span></td>
<td><span data-ttu-id="69f86-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69f86-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="69f86-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-625">Cost object</span></span></th>
<th><span data-ttu-id="69f86-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="69f86-626">Magnitude</span></span></th>
<th><span data-ttu-id="69f86-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="69f86-627">Allocation factor</span></span></th>
<th><span data-ttu-id="69f86-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-628">Amount</span></span></th>
<th><span data-ttu-id="69f86-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-630">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-631">Product 1</span></span></td>
<td><span data-ttu-id="69f86-632">80</span><span class="sxs-lookup"><span data-stu-id="69f86-632">80</span></span></td>
<td><span data-ttu-id="69f86-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="69f86-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="69f86-634">241.05</span><span class="sxs-lookup"><span data-stu-id="69f86-634">241.05</span></span></td>
<td><span data-ttu-id="69f86-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-636">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-637">Product 2</span></span></td>
<td><span data-ttu-id="69f86-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="69f86-638">15</span></span></td>
<td><span data-ttu-id="69f86-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="69f86-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="69f86-640">45.20</span><span class="sxs-lookup"><span data-stu-id="69f86-640">45.20</span></span></td>
<td><span data-ttu-id="69f86-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-642">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-643">Product 1</span></span></td>
<td><span data-ttu-id="69f86-644">80</span><span class="sxs-lookup"><span data-stu-id="69f86-644">80</span></span></td>
<td><span data-ttu-id="69f86-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="69f86-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="69f86-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="69f86-646">2,507.09</span></span></td>
<td><span data-ttu-id="69f86-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-648">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-649">Product 2</span></span></td>
<td><span data-ttu-id="69f86-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="69f86-650">15</span></span></td>
<td><span data-ttu-id="69f86-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="69f86-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="69f86-652">470.08</span><span class="sxs-lookup"><span data-stu-id="69f86-652">470.08</span></span></td>
<td><span data-ttu-id="69f86-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="69f86-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="69f86-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-655">Journal</span></span></th>
<th><span data-ttu-id="69f86-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="69f86-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="69f86-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="69f86-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-659">00004</span><span class="sxs-lookup"><span data-stu-id="69f86-659">00004</span></span></td>
<td><span data-ttu-id="69f86-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="69f86-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-661">Fiscal</span></span></td>
<td><span data-ttu-id="69f86-662">2017</span><span class="sxs-lookup"><span data-stu-id="69f86-662">2017</span></span></td>
<td><span data-ttu-id="69f86-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-663">Period 1</span></span></td>
<td><span data-ttu-id="69f86-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="69f86-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="69f86-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="69f86-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="69f86-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-668">Cost element</span></span></th>
<th><span data-ttu-id="69f86-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-669">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-672">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-672">CC001</span></span></td>
<td><span data-ttu-id="69f86-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-673">HR</span></span></td>
<td><span data-ttu-id="69f86-674">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-674">10001</span></span></td>
<td><span data-ttu-id="69f86-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-675">Electricity</span></span></td>
<td><span data-ttu-id="69f86-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-676">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-677">500.00</span><span class="sxs-lookup"><span data-stu-id="69f86-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-679">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-679">CC001</span></span></td>
<td><span data-ttu-id="69f86-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-680">HR</span></span></td>
<td><span data-ttu-id="69f86-681">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-681">10001</span></span></td>
<td><span data-ttu-id="69f86-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-682">Electricity</span></span></td>
<td><span data-ttu-id="69f86-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-683">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="69f86-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-686">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-686">CC002</span></span></td>
<td><span data-ttu-id="69f86-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-687">Finance</span></span></td>
<td><span data-ttu-id="69f86-688">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-688">10001</span></span></td>
<td><span data-ttu-id="69f86-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-689">Electricity</span></span></td>
<td><span data-ttu-id="69f86-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-690">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-691">675.00</span><span class="sxs-lookup"><span data-stu-id="69f86-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-693">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-693">CC002</span></span></td>
<td><span data-ttu-id="69f86-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-694">Finance</span></span></td>
<td><span data-ttu-id="69f86-695">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-695">10001</span></span></td>
<td><span data-ttu-id="69f86-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-696">Electricity</span></span></td>
<td><span data-ttu-id="69f86-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-697">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="69f86-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-700">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-700">CC003</span></span></td>
<td><span data-ttu-id="69f86-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-701">Assembly</span></span></td>
<td><span data-ttu-id="69f86-702">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-702">10001</span></span></td>
<td><span data-ttu-id="69f86-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-703">Electricity</span></span></td>
<td><span data-ttu-id="69f86-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-704">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-705">713.75</span><span class="sxs-lookup"><span data-stu-id="69f86-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-707">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-707">CC003</span></span></td>
<td><span data-ttu-id="69f86-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-708">Assembly</span></span></td>
<td><span data-ttu-id="69f86-709">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-709">10001</span></span></td>
<td><span data-ttu-id="69f86-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-710">Electricity</span></span></td>
<td><span data-ttu-id="69f86-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-711">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="69f86-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-714">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-714">CC003</span></span></td>
<td><span data-ttu-id="69f86-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-715">Packaging</span></span></td>
<td><span data-ttu-id="69f86-716">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-716">10001</span></span></td>
<td><span data-ttu-id="69f86-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-717">Electricity</span></span></td>
<td><span data-ttu-id="69f86-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-718">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-719">286.25</span><span class="sxs-lookup"><span data-stu-id="69f86-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-721">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-721">CC003</span></span></td>
<td><span data-ttu-id="69f86-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-722">Packaging</span></span></td>
<td><span data-ttu-id="69f86-723">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-723">10001</span></span></td>
<td><span data-ttu-id="69f86-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-724">Electricity</span></span></td>
<td><span data-ttu-id="69f86-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-725">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="69f86-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-728">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-729">Product 1</span></span></td>
<td><span data-ttu-id="69f86-730">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-730">10001</span></span></td>
<td><span data-ttu-id="69f86-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-731">Electricity</span></span></td>
<td><span data-ttu-id="69f86-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-732">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-733">776.36</span><span class="sxs-lookup"><span data-stu-id="69f86-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-735">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-736">Product 1</span></span></td>
<td><span data-ttu-id="69f86-737">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-737">10001</span></span></td>
<td><span data-ttu-id="69f86-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-738">Electricity</span></span></td>
<td><span data-ttu-id="69f86-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-739">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="69f86-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-742">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-743">Product 1</span></span></td>
<td><span data-ttu-id="69f86-744">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-744">10001</span></span></td>
<td><span data-ttu-id="69f86-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-745">Electricity</span></span></td>
<td><span data-ttu-id="69f86-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-746">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-747">223.64</span><span class="sxs-lookup"><span data-stu-id="69f86-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="69f86-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-749">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-750">Product 1</span></span></td>
<td><span data-ttu-id="69f86-751">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-751">10001</span></span></td>
<td><span data-ttu-id="69f86-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-752">Electricity</span></span></td>
<td><span data-ttu-id="69f86-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-753">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="69f86-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="69f86-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="69f86-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="69f86-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-757">Cost element</span></span></th>
<th><span data-ttu-id="69f86-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-758">Cost behavior</span></span></th>
<th><span data-ttu-id="69f86-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-759">Amount</span></span></th>
<th><span data-ttu-id="69f86-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="69f86-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69f86-761">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-761">CC001</span></span></td>
<td><span data-ttu-id="69f86-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-762">HR</span></span></td>
<td><span data-ttu-id="69f86-763">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-763">10001</span></span></td>
<td><span data-ttu-id="69f86-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-764">Electricity</span></span></td>
<td><span data-ttu-id="69f86-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-765">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="69f86-766">-500.00</span></span></td>
<td><span data-ttu-id="69f86-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-768">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-768">CC002</span></span></td>
<td><span data-ttu-id="69f86-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-769">Finance</span></span></td>
<td><span data-ttu-id="69f86-770">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-770">10001</span></span></td>
<td><span data-ttu-id="69f86-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-771">Electricity</span></span></td>
<td><span data-ttu-id="69f86-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-772">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-773">175.00</span><span class="sxs-lookup"><span data-stu-id="69f86-773">175.00</span></span></td>
<td><span data-ttu-id="69f86-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-775">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-775">CC003</span></span></td>
<td><span data-ttu-id="69f86-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-776">Assembly</span></span></td>
<td><span data-ttu-id="69f86-777">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-777">10001</span></span></td>
<td><span data-ttu-id="69f86-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-778">Electricity</span></span></td>
<td><span data-ttu-id="69f86-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-779">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-780">275.00</span><span class="sxs-lookup"><span data-stu-id="69f86-780">275.00</span></span></td>
<td><span data-ttu-id="69f86-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-782">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-782">CC004</span></span></td>
<td><span data-ttu-id="69f86-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-783">Packaging</span></span></td>
<td><span data-ttu-id="69f86-784">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-784">10001</span></span></td>
<td><span data-ttu-id="69f86-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-785">Electricity</span></span></td>
<td><span data-ttu-id="69f86-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-786">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-787">50,00</span><span class="sxs-lookup"><span data-stu-id="69f86-787">50,00</span></span></td>
<td><span data-ttu-id="69f86-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-789">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-789">CC001</span></span></td>
<td><span data-ttu-id="69f86-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="69f86-790">HR</span></span></td>
<td><span data-ttu-id="69f86-791">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-791">10001</span></span></td>
<td><span data-ttu-id="69f86-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-792">Electricity</span></span></td>
<td><span data-ttu-id="69f86-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-793">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="69f86-794">-1,245.71</span></span></td>
<td><span data-ttu-id="69f86-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-796">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-796">CC002</span></span></td>
<td><span data-ttu-id="69f86-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-797">Finance</span></span></td>
<td><span data-ttu-id="69f86-798">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-798">10001</span></span></td>
<td><span data-ttu-id="69f86-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-799">Electricity</span></span></td>
<td><span data-ttu-id="69f86-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-800">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-801">436.00</span><span class="sxs-lookup"><span data-stu-id="69f86-801">436.00</span></span></td>
<td><span data-ttu-id="69f86-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-803">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-803">CC003</span></span></td>
<td><span data-ttu-id="69f86-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-804">Assembly</span></span></td>
<td><span data-ttu-id="69f86-805">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-805">10001</span></span></td>
<td><span data-ttu-id="69f86-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-806">Electricity</span></span></td>
<td><span data-ttu-id="69f86-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-807">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-808">685.14</span><span class="sxs-lookup"><span data-stu-id="69f86-808">685.14</span></span></td>
<td><span data-ttu-id="69f86-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-810">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-810">CC004</span></span></td>
<td><span data-ttu-id="69f86-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-811">Packaging</span></span></td>
<td><span data-ttu-id="69f86-812">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-812">10001</span></span></td>
<td><span data-ttu-id="69f86-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-813">Electricity</span></span></td>
<td><span data-ttu-id="69f86-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-814">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-815">124.57</span><span class="sxs-lookup"><span data-stu-id="69f86-815">124.57</span></span></td>
<td><span data-ttu-id="69f86-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-817">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-817">CC002</span></span></td>
<td><span data-ttu-id="69f86-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-818">Finance</span></span></td>
<td><span data-ttu-id="69f86-819">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-819">10001</span></span></td>
<td><span data-ttu-id="69f86-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-820">Electricity</span></span></td>
<td><span data-ttu-id="69f86-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-821">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="69f86-822">-675.00</span></span></td>
<td><span data-ttu-id="69f86-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-824">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-824">CC003</span></span></td>
<td><span data-ttu-id="69f86-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-825">Assembly</span></span></td>
<td><span data-ttu-id="69f86-826">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-826">10001</span></span></td>
<td><span data-ttu-id="69f86-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-827">Electricity</span></span></td>
<td><span data-ttu-id="69f86-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-828">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-829">438.75</span><span class="sxs-lookup"><span data-stu-id="69f86-829">438.75</span></span></td>
<td><span data-ttu-id="69f86-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-831">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-831">CC004</span></span></td>
<td><span data-ttu-id="69f86-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-832">Packaging</span></span></td>
<td><span data-ttu-id="69f86-833">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-833">10001</span></span></td>
<td><span data-ttu-id="69f86-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-834">Electricity</span></span></td>
<td><span data-ttu-id="69f86-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-835">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-836">236.25</span><span class="sxs-lookup"><span data-stu-id="69f86-836">236.25</span></span></td>
<td><span data-ttu-id="69f86-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-838">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-838">CC002</span></span></td>
<td><span data-ttu-id="69f86-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="69f86-839">Finance</span></span></td>
<td><span data-ttu-id="69f86-840">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-840">10001</span></span></td>
<td><span data-ttu-id="69f86-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-841">Electricity</span></span></td>
<td><span data-ttu-id="69f86-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-842">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="69f86-843">-8,150.29</span></span></td>
<td><span data-ttu-id="69f86-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-845">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-845">CC003</span></span></td>
<td><span data-ttu-id="69f86-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-846">Assembly</span></span></td>
<td><span data-ttu-id="69f86-847">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-847">10001</span></span></td>
<td><span data-ttu-id="69f86-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-848">Electricity</span></span></td>
<td><span data-ttu-id="69f86-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-849">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="69f86-850">5,297.69</span></span></td>
<td><span data-ttu-id="69f86-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-852">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-852">CC004</span></span></td>
<td><span data-ttu-id="69f86-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="69f86-853">Packaging</span></span></td>
<td><span data-ttu-id="69f86-854">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-854">10001</span></span></td>
<td><span data-ttu-id="69f86-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-855">Electricity</span></span></td>
<td><span data-ttu-id="69f86-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-856">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="69f86-857">2,852.60</span></span></td>
<td><span data-ttu-id="69f86-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-859">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-859">CC003</span></span></td>
<td><span data-ttu-id="69f86-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-860">Assembly</span></span></td>
<td><span data-ttu-id="69f86-861">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-861">10001</span></span></td>
<td><span data-ttu-id="69f86-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-862">Electricity</span></span></td>
<td><span data-ttu-id="69f86-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-863">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="69f86-864">-713.75</span></span></td>
<td><span data-ttu-id="69f86-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-866">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-867">Product 1</span></span></td>
<td><span data-ttu-id="69f86-868">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-868">10001</span></span></td>
<td><span data-ttu-id="69f86-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-869">Electricity</span></span></td>
<td><span data-ttu-id="69f86-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-870">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-871">535.31</span><span class="sxs-lookup"><span data-stu-id="69f86-871">535.31</span></span></td>
<td><span data-ttu-id="69f86-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-873">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-874">Product 2</span></span></td>
<td><span data-ttu-id="69f86-875">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-875">10001</span></span></td>
<td><span data-ttu-id="69f86-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-876">Electricity</span></span></td>
<td><span data-ttu-id="69f86-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-877">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-878">178.44</span><span class="sxs-lookup"><span data-stu-id="69f86-878">178.44</span></span></td>
<td><span data-ttu-id="69f86-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-880">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-880">CC003</span></span></td>
<td><span data-ttu-id="69f86-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-881">Assembly</span></span></td>
<td><span data-ttu-id="69f86-882">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-882">10001</span></span></td>
<td><span data-ttu-id="69f86-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-883">Electricity</span></span></td>
<td><span data-ttu-id="69f86-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-884">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="69f86-885">-5,982.83</span></span></td>
<td><span data-ttu-id="69f86-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-887">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-888">Product 1</span></span></td>
<td><span data-ttu-id="69f86-889">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-889">10001</span></span></td>
<td><span data-ttu-id="69f86-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-890">Electricity</span></span></td>
<td><span data-ttu-id="69f86-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-891">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="69f86-892">4,487.12</span></span></td>
<td><span data-ttu-id="69f86-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-894">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-895">Product 2</span></span></td>
<td><span data-ttu-id="69f86-896">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-896">10001</span></span></td>
<td><span data-ttu-id="69f86-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-897">Electricity</span></span></td>
<td><span data-ttu-id="69f86-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-898">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="69f86-899">1,495.71</span></span></td>
<td><span data-ttu-id="69f86-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-901">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-901">CC003</span></span></td>
<td><span data-ttu-id="69f86-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-902">Assembly</span></span></td>
<td><span data-ttu-id="69f86-903">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-903">10001</span></span></td>
<td><span data-ttu-id="69f86-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-904">Electricity</span></span></td>
<td><span data-ttu-id="69f86-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-905">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="69f86-906">-286.25</span></span></td>
<td><span data-ttu-id="69f86-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-908">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-909">Product 1</span></span></td>
<td><span data-ttu-id="69f86-910">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-910">10001</span></span></td>
<td><span data-ttu-id="69f86-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-911">Electricity</span></span></td>
<td><span data-ttu-id="69f86-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-912">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-913">241.05</span><span class="sxs-lookup"><span data-stu-id="69f86-913">241.05</span></span></td>
<td><span data-ttu-id="69f86-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-915">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-916">Product 2</span></span></td>
<td><span data-ttu-id="69f86-917">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-917">10001</span></span></td>
<td><span data-ttu-id="69f86-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-918">Electricity</span></span></td>
<td><span data-ttu-id="69f86-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-919">Fixed cost</span></span></td>
<td><span data-ttu-id="69f86-920">45.20</span><span class="sxs-lookup"><span data-stu-id="69f86-920">45.20</span></span></td>
<td><span data-ttu-id="69f86-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-922">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-922">CC003</span></span></td>
<td><span data-ttu-id="69f86-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="69f86-923">Assembly</span></span></td>
<td><span data-ttu-id="69f86-924">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-924">10001</span></span></td>
<td><span data-ttu-id="69f86-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-925">Electricity</span></span></td>
<td><span data-ttu-id="69f86-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-926">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="69f86-927">-2,977.17</span></span></td>
<td><span data-ttu-id="69f86-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-929">Prod 1</span></span></td>
<td><span data-ttu-id="69f86-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-930">Product 1</span></span></td>
<td><span data-ttu-id="69f86-931">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-931">10001</span></span></td>
<td><span data-ttu-id="69f86-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-932">Electricity</span></span></td>
<td><span data-ttu-id="69f86-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-933">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="69f86-934">2,507.09</span></span></td>
<td><span data-ttu-id="69f86-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69f86-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-936">Prod 2</span></span></td>
<td><span data-ttu-id="69f86-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-937">Product 2</span></span></td>
<td><span data-ttu-id="69f86-938">10001</span><span class="sxs-lookup"><span data-stu-id="69f86-938">10001</span></span></td>
<td><span data-ttu-id="69f86-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-939">Electricity</span></span></td>
<td><span data-ttu-id="69f86-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-940">Variable cost</span></span></td>
<td><span data-ttu-id="69f86-941">470.08</span><span class="sxs-lookup"><span data-stu-id="69f86-941">470.08</span></span></td>
<td><span data-ttu-id="69f86-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="69f86-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="69f86-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="69f86-943">Conclusion</span></span>
<span data-ttu-id="69f86-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="69f86-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="69f86-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="69f86-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="69f86-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="69f86-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="69f86-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="69f86-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="69f86-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="69f86-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="69f86-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="69f86-951">CC099</span><span class="sxs-lookup"><span data-stu-id="69f86-951">CC099</span></span></th>
<th><span data-ttu-id="69f86-952">CC001</span><span class="sxs-lookup"><span data-stu-id="69f86-952">CC001</span></span></th>
<th><span data-ttu-id="69f86-953">CC002</span><span class="sxs-lookup"><span data-stu-id="69f86-953">CC002</span></span></th>
<th><span data-ttu-id="69f86-954">CC003</span><span class="sxs-lookup"><span data-stu-id="69f86-954">CC003</span></span></th>
<th><span data-ttu-id="69f86-955">CC004</span><span class="sxs-lookup"><span data-stu-id="69f86-955">CC004</span></span></th>
<th><span data-ttu-id="69f86-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-956">Proj 1</span></span></th>
<th><span data-ttu-id="69f86-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-957">Proj 2</span></span></th>
<th><span data-ttu-id="69f86-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="69f86-958">Prod 1</span></span></th>
<th><span data-ttu-id="69f86-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="69f86-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="69f86-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="69f86-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="69f86-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="69f86-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="69f86-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-971">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="69f86-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="69f86-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-973">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-974">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-975">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-976">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-977">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="69f86-978">776.36</span><span class="sxs-lookup"><span data-stu-id="69f86-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-979">223.64</span><span class="sxs-lookup"><span data-stu-id="69f86-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="69f86-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="69f86-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-982">000</span><span class="sxs-lookup"><span data-stu-id="69f86-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-983">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-984">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-985">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-986">0.00</span><span class="sxs-lookup"><span data-stu-id="69f86-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-987">30.00</span><span class="sxs-lookup"><span data-stu-id="69f86-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-988">10.00</span><span class="sxs-lookup"><span data-stu-id="69f86-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="69f86-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="69f86-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="69f86-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="69f86-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="69f86-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="69f86-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="69f86-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="69f86-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="69f86-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="69f86-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="69f86-996">สำหรับข้อมูลเพิ่มเติม ให้ดู [การรวบรวมต้นทุน](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="69f86-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



