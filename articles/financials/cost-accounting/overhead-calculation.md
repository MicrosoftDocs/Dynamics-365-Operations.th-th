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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544066"
---
# <a name="overhead-calculation"></a><span data-ttu-id="c6cc2-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6cc2-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c6cc2-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-105">Term definition</span></span>
---------------

<span data-ttu-id="c6cc2-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="c6cc2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c6cc2-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c6cc2-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="c6cc2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c6cc2-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-109">Rent</span></span>
-   <span data-ttu-id="c6cc2-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-110">Electricity</span></span>
-   <span data-ttu-id="c6cc2-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c6cc2-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-112">Overhead calculation overview</span></span>
<span data-ttu-id="c6cc2-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c6cc2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c6cc2-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c6cc2-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c6cc2-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c6cc2-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c6cc2-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6cc2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c6cc2-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-119">Version type</span></span>
-   <span data-ttu-id="c6cc2-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c6cc2-120">Date and time</span></span>
-   <span data-ttu-id="c6cc2-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c6cc2-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-122">Fiscal year</span></span>
-   <span data-ttu-id="c6cc2-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-123">Fiscal period</span></span>

<span data-ttu-id="c6cc2-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c6cc2-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="c6cc2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c6cc2-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6cc2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c6cc2-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c6cc2-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c6cc2-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c6cc2-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c6cc2-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c6cc2-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c6cc2-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c6cc2-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c6cc2-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c6cc2-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="c6cc2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c6cc2-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6cc2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c6cc2-140">Main account</span></span></th>
<th><span data-ttu-id="c6cc2-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-143">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-144">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-145">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-145">10001</span></span></td>
<td><span data-ttu-id="c6cc2-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-146">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c6cc2-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c6cc2-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c6cc2-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="c6cc2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c6cc2-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c6cc2-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c6cc2-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="c6cc2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c6cc2-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c6cc2-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="c6cc2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c6cc2-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c6cc2-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c6cc2-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c6cc2-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-160">Journal</span></span></th>
<th><span data-ttu-id="c6cc2-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c6cc2-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c6cc2-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-164">00001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-164">00001</span></span></td>
<td><span data-ttu-id="c6cc2-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c6cc2-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-166">Fiscal</span></span></td>
<td><span data-ttu-id="c6cc2-167">2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-167">2017</span></span></td>
<td><span data-ttu-id="c6cc2-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-168">Period 1</span></span></td>
<td><span data-ttu-id="c6cc2-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c6cc2-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-173">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-177">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-178">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-179">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-179">10001</span></span></td>
<td><span data-ttu-id="c6cc2-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-180">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c6cc2-181">Unclassified</span></span></td>
<td><span data-ttu-id="c6cc2-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c6cc2-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-185">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-187">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-189">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-190">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-191">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-191">10001</span></span></td>
<td><span data-ttu-id="c6cc2-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-192">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c6cc2-193">Unclassified</span></span></td>
<td><span data-ttu-id="c6cc2-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-194">10,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-196">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-197">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-198">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-198">10001</span></span></td>
<td><span data-ttu-id="c6cc2-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-199">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c6cc2-200">Unclassified</span></span></td>
<td><span data-ttu-id="c6cc2-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-203">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-204">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-205">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-205">10001</span></span></td>
<td><span data-ttu-id="c6cc2-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-206">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-208">1,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-210">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-211">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-212">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-212">10001</span></span></td>
<td><span data-ttu-id="c6cc2-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-213">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-214">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-215">9,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c6cc2-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c6cc2-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c6cc2-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c6cc2-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c6cc2-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c6cc2-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c6cc2-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c6cc2-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c6cc2-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c6cc2-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c6cc2-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-228">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="c6cc2-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-230">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-231">HR</span></span></td>
<td><span data-ttu-id="c6cc2-232">1,000</span><span class="sxs-lookup"><span data-stu-id="c6cc2-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-233">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-234">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-235">6,000</span><span class="sxs-lookup"><span data-stu-id="c6cc2-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-236">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-237">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-238">0</span><span class="sxs-lookup"><span data-stu-id="c6cc2-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-240">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-241">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-244">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-245">HR</span></span></td>
<td><span data-ttu-id="c6cc2-246">1,000</span><span class="sxs-lookup"><span data-stu-id="c6cc2-246">1,000</span></span></td>
<td><span data-ttu-id="c6cc2-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-249">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-250">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-251">6,000</span><span class="sxs-lookup"><span data-stu-id="c6cc2-251">6,000</span></span></td>
<td><span data-ttu-id="c6cc2-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c6cc2-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-254">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-255">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-256">0</span><span class="sxs-lookup"><span data-stu-id="c6cc2-256">0</span></span></td>
<td><span data-ttu-id="c6cc2-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-258">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c6cc2-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-261">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-262">Formula</span></span></th>
<th><span data-ttu-id="c6cc2-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-263">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-266">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-267">HR</span></span></td>
<td><span data-ttu-id="c6cc2-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c6cc2-269">1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-269">1</span></span></td>
<td><span data-ttu-id="c6cc2-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-271">500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-272">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-273">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c6cc2-275">1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-275">1</span></span></td>
<td><span data-ttu-id="c6cc2-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-277">500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-278">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-279">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c6cc2-281">0</span><span class="sxs-lookup"><span data-stu-id="c6cc2-281">0</span></span></td>
<td><span data-ttu-id="c6cc2-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-283">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c6cc2-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-285">Journal</span></span></th>
<th><span data-ttu-id="c6cc2-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c6cc2-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c6cc2-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-289">00002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-289">00002</span></span></td>
<td><span data-ttu-id="c6cc2-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c6cc2-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-291">Fiscal</span></span></td>
<td><span data-ttu-id="c6cc2-292">2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-292">2017</span></span></td>
<td><span data-ttu-id="c6cc2-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-293">Period 1</span></span></td>
<td><span data-ttu-id="c6cc2-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c6cc2-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-298">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-302">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-303">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-304">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-304">10001</span></span></td>
<td><span data-ttu-id="c6cc2-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-305">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-309">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-310">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-311">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-311">10001</span></span></td>
<td><span data-ttu-id="c6cc2-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-312">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-313">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c6cc2-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-317">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-319">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-321">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-322">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-323">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-323">10001</span></span></td>
<td><span data-ttu-id="c6cc2-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-324">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="c6cc2-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-328">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-329">HR</span></span></td>
<td><span data-ttu-id="c6cc2-330">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-330">10001</span></span></td>
<td><span data-ttu-id="c6cc2-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-331">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-333">500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-333">500.00</span></span></td>
<td><span data-ttu-id="c6cc2-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-335">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-336">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-337">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-337">10001</span></span></td>
<td><span data-ttu-id="c6cc2-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-338">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-340">500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-340">500.00</span></span></td>
<td><span data-ttu-id="c6cc2-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-342">CC099</span></span></td>
<td><span data-ttu-id="c6cc2-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6cc2-343">Default cost center</span></span></td>
<td><span data-ttu-id="c6cc2-344">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-344">10001</span></span></td>
<td><span data-ttu-id="c6cc2-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-345">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-346">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c6cc2-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-349">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-350">HR</span></span></td>
<td><span data-ttu-id="c6cc2-351">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-351">10001</span></span></td>
<td><span data-ttu-id="c6cc2-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-352">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-353">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-354">1,285.71</span></span></td>
<td><span data-ttu-id="c6cc2-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-356">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-357">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-358">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-358">10001</span></span></td>
<td><span data-ttu-id="c6cc2-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-359">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-360">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c6cc2-361">7,714.29</span></span></td>
<td><span data-ttu-id="c6cc2-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c6cc2-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c6cc2-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c6cc2-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c6cc2-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-367">Define the overhead rate</span></span>

<span data-ttu-id="c6cc2-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c6cc2-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6cc2-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-370">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c6cc2-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-372">Proj 1</span></span></td>
<td><span data-ttu-id="c6cc2-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-373">Project 1</span></span></td>
<td><span data-ttu-id="c6cc2-374">3</span><span class="sxs-lookup"><span data-stu-id="c6cc2-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-375">Proj 2</span></span></td>
<td><span data-ttu-id="c6cc2-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-376">Project 2</span></span></td>
<td><span data-ttu-id="c6cc2-377">1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-379">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-380">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-382">Units</span></span></th>
<th><span data-ttu-id="c6cc2-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="c6cc2-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-384">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-385">HR</span></span></td>
<td><span data-ttu-id="c6cc2-386">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-386">10001</span></span></td>
<td><span data-ttu-id="c6cc2-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-387">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-388">1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-388">1</span></span></td>
<td><span data-ttu-id="c6cc2-389">10</span><span class="sxs-lookup"><span data-stu-id="c6cc2-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-391">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-392">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-393">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-396">Proj 1</span></span></td>
<td><span data-ttu-id="c6cc2-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-397">Project 1</span></span></td>
<td><span data-ttu-id="c6cc2-398">3</span><span class="sxs-lookup"><span data-stu-id="c6cc2-398">3</span></span></td>
<td><span data-ttu-id="c6cc2-399">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-399">10001</span></span></td>
<td><span data-ttu-id="c6cc2-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c6cc2-401">30.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-402">Proj 2</span></span></td>
<td><span data-ttu-id="c6cc2-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-403">Project 2</span></span></td>
<td><span data-ttu-id="c6cc2-404">1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-404">1</span></span></td>
<td><span data-ttu-id="c6cc2-405">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-405">10001</span></span></td>
<td><span data-ttu-id="c6cc2-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c6cc2-407">10.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c6cc2-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-409">Journal</span></span></th>
<th><span data-ttu-id="c6cc2-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c6cc2-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c6cc2-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-413">00003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-413">00003</span></span></td>
<td><span data-ttu-id="c6cc2-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="c6cc2-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c6cc2-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-415">Fiscal</span></span></td>
<td><span data-ttu-id="c6cc2-416">2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-416">2017</span></span></td>
<td><span data-ttu-id="c6cc2-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-417">Period 1</span></span></td>
<td><span data-ttu-id="c6cc2-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c6cc2-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-421">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-424">Proj 1</span></span></td>
<td><span data-ttu-id="c6cc2-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c6cc2-426">3.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-428">Proj 2</span></span></td>
<td><span data-ttu-id="c6cc2-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c6cc2-430">1.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c6cc2-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-433">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-435">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-437">CC0001</span></span></td>
<td><span data-ttu-id="c6cc2-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-438">HR</span></span></td>
<td><span data-ttu-id="c6cc2-439">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-439">10001</span></span></td>
<td><span data-ttu-id="c6cc2-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-440">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-441">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-442">-30.00</span></span></td>
<td><span data-ttu-id="c6cc2-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-444">Proj 1</span></span></td>
<td><span data-ttu-id="c6cc2-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c6cc2-446">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-446">10001</span></span></td>
<td><span data-ttu-id="c6cc2-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-447">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-448">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-449">30.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-449">30.00</span></span></td>
<td><span data-ttu-id="c6cc2-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-451">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-452">HR</span></span></td>
<td><span data-ttu-id="c6cc2-453">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-453">10001</span></span></td>
<td><span data-ttu-id="c6cc2-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-454">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-455">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-456">-10.00</span></span></td>
<td><span data-ttu-id="c6cc2-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-458">Proj 2</span></span></td>
<td><span data-ttu-id="c6cc2-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c6cc2-460">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-460">10001</span></span></td>
<td><span data-ttu-id="c6cc2-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-461">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-462">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-463">10.00</span></span></td>
<td><span data-ttu-id="c6cc2-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c6cc2-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c6cc2-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c6cc2-468">Finance and Operations สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c6cc2-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c6cc2-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c6cc2-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="c6cc2-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c6cc2-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c6cc2-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c6cc2-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c6cc2-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-475">Define the cost allocation</span></span>

<span data-ttu-id="c6cc2-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c6cc2-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c6cc2-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6cc2-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-479">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="c6cc2-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-481">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-482">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-483">35</span><span class="sxs-lookup"><span data-stu-id="c6cc2-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-484">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-485">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-486">55</span><span class="sxs-lookup"><span data-stu-id="c6cc2-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-487">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-488">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-489">10</span><span class="sxs-lookup"><span data-stu-id="c6cc2-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c6cc2-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6cc2-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-492">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-494">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-495">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-496">65</span><span class="sxs-lookup"><span data-stu-id="c6cc2-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-497">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-498">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-499">35</span><span class="sxs-lookup"><span data-stu-id="c6cc2-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c6cc2-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6cc2-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-502">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-504">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-505">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-506">60</span><span class="sxs-lookup"><span data-stu-id="c6cc2-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-507">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-508">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-509">20</span><span class="sxs-lookup"><span data-stu-id="c6cc2-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c6cc2-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6cc2-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-512">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-514">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-515">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-516">80</span><span class="sxs-lookup"><span data-stu-id="c6cc2-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-517">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-518">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="c6cc2-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c6cc2-520">ใน Finance and Operations การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้ สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c6cc2-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c6cc2-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-523">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-524">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-526">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-528">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-529">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-530">35</span><span class="sxs-lookup"><span data-stu-id="c6cc2-530">35</span></span></td>
<td><span data-ttu-id="c6cc2-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c6cc2-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-532">175.00</span></span></td>
<td><span data-ttu-id="c6cc2-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-534">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-535">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-536">55</span><span class="sxs-lookup"><span data-stu-id="c6cc2-536">55</span></span></td>
<td><span data-ttu-id="c6cc2-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c6cc2-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-538">275.00</span></span></td>
<td><span data-ttu-id="c6cc2-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-540">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-541">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-542">10</span><span class="sxs-lookup"><span data-stu-id="c6cc2-542">10</span></span></td>
<td><span data-ttu-id="c6cc2-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c6cc2-544">50.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-544">50.00</span></span></td>
<td><span data-ttu-id="c6cc2-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-546">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-547">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-548">35</span><span class="sxs-lookup"><span data-stu-id="c6cc2-548">35</span></span></td>
<td><span data-ttu-id="c6cc2-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c6cc2-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-550">436.00</span></span></td>
<td><span data-ttu-id="c6cc2-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-552">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-553">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-554">55</span><span class="sxs-lookup"><span data-stu-id="c6cc2-554">55</span></span></td>
<td><span data-ttu-id="c6cc2-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c6cc2-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c6cc2-556">685.14</span></span></td>
<td><span data-ttu-id="c6cc2-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-558">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-559">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-560">10</span><span class="sxs-lookup"><span data-stu-id="c6cc2-560">10</span></span></td>
<td><span data-ttu-id="c6cc2-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c6cc2-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c6cc2-562">124.57</span></span></td>
<td><span data-ttu-id="c6cc2-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-565">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-566">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-568">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-570">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-571">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-572">65</span><span class="sxs-lookup"><span data-stu-id="c6cc2-572">65</span></span></td>
<td><span data-ttu-id="c6cc2-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c6cc2-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c6cc2-574">438.75</span></span></td>
<td><span data-ttu-id="c6cc2-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-576">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-577">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-578">35</span><span class="sxs-lookup"><span data-stu-id="c6cc2-578">35</span></span></td>
<td><span data-ttu-id="c6cc2-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c6cc2-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c6cc2-580">236.25</span></span></td>
<td><span data-ttu-id="c6cc2-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-582">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-583">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-584">65</span><span class="sxs-lookup"><span data-stu-id="c6cc2-584">65</span></span></td>
<td><span data-ttu-id="c6cc2-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c6cc2-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c6cc2-586">5,297.69</span></span></td>
<td><span data-ttu-id="c6cc2-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-588">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-589">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-590">35</span><span class="sxs-lookup"><span data-stu-id="c6cc2-590">35</span></span></td>
<td><span data-ttu-id="c6cc2-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c6cc2-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c6cc2-592">2,852.60</span></span></td>
<td><span data-ttu-id="c6cc2-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-595">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-596">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-598">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-600">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-601">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-602">60</span><span class="sxs-lookup"><span data-stu-id="c6cc2-602">60</span></span></td>
<td><span data-ttu-id="c6cc2-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c6cc2-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c6cc2-604">535.31</span></span></td>
<td><span data-ttu-id="c6cc2-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-606">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-607">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-608">20</span><span class="sxs-lookup"><span data-stu-id="c6cc2-608">20</span></span></td>
<td><span data-ttu-id="c6cc2-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c6cc2-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c6cc2-610">178.44</span></span></td>
<td><span data-ttu-id="c6cc2-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-612">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-613">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-614">60</span><span class="sxs-lookup"><span data-stu-id="c6cc2-614">60</span></span></td>
<td><span data-ttu-id="c6cc2-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c6cc2-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c6cc2-616">4,487.12</span></span></td>
<td><span data-ttu-id="c6cc2-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-618">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-619">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-620">20</span><span class="sxs-lookup"><span data-stu-id="c6cc2-620">20</span></span></td>
<td><span data-ttu-id="c6cc2-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c6cc2-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-622">1,495.71</span></span></td>
<td><span data-ttu-id="c6cc2-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6cc2-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-625">Cost object</span></span></th>
<th><span data-ttu-id="c6cc2-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="c6cc2-626">Magnitude</span></span></th>
<th><span data-ttu-id="c6cc2-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c6cc2-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-628">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-630">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-631">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-632">80</span><span class="sxs-lookup"><span data-stu-id="c6cc2-632">80</span></span></td>
<td><span data-ttu-id="c6cc2-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c6cc2-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c6cc2-634">241.05</span></span></td>
<td><span data-ttu-id="c6cc2-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-636">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-637">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="c6cc2-638">15</span></span></td>
<td><span data-ttu-id="c6cc2-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c6cc2-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c6cc2-640">45.20</span></span></td>
<td><span data-ttu-id="c6cc2-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-642">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-643">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-644">80</span><span class="sxs-lookup"><span data-stu-id="c6cc2-644">80</span></span></td>
<td><span data-ttu-id="c6cc2-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c6cc2-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c6cc2-646">2,507.09</span></span></td>
<td><span data-ttu-id="c6cc2-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-648">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-649">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="c6cc2-650">15</span></span></td>
<td><span data-ttu-id="c6cc2-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c6cc2-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c6cc2-652">470.08</span></span></td>
<td><span data-ttu-id="c6cc2-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c6cc2-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-655">Journal</span></span></th>
<th><span data-ttu-id="c6cc2-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c6cc2-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c6cc2-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-659">00004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-659">00004</span></span></td>
<td><span data-ttu-id="c6cc2-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c6cc2-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-661">Fiscal</span></span></td>
<td><span data-ttu-id="c6cc2-662">2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-662">2017</span></span></td>
<td><span data-ttu-id="c6cc2-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-663">Period 1</span></span></td>
<td><span data-ttu-id="c6cc2-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c6cc2-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c6cc2-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-668">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-672">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-673">HR</span></span></td>
<td><span data-ttu-id="c6cc2-674">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-674">10001</span></span></td>
<td><span data-ttu-id="c6cc2-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-675">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-677">500.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-679">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-680">HR</span></span></td>
<td><span data-ttu-id="c6cc2-681">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-681">10001</span></span></td>
<td><span data-ttu-id="c6cc2-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-682">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-683">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-686">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-687">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-688">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-688">10001</span></span></td>
<td><span data-ttu-id="c6cc2-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-689">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-693">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-694">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-695">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-695">10001</span></span></td>
<td><span data-ttu-id="c6cc2-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-696">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-697">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c6cc2-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-700">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-701">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-702">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-702">10001</span></span></td>
<td><span data-ttu-id="c6cc2-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-703">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c6cc2-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-707">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-708">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-709">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-709">10001</span></span></td>
<td><span data-ttu-id="c6cc2-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-710">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-711">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c6cc2-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-714">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-715">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-716">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-716">10001</span></span></td>
<td><span data-ttu-id="c6cc2-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-717">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c6cc2-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-721">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-722">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-723">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-723">10001</span></span></td>
<td><span data-ttu-id="c6cc2-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-724">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-725">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c6cc2-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-728">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-729">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-730">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-730">10001</span></span></td>
<td><span data-ttu-id="c6cc2-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-731">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c6cc2-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-735">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-736">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-737">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-737">10001</span></span></td>
<td><span data-ttu-id="c6cc2-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-738">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-739">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c6cc2-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-742">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-743">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-744">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-744">10001</span></span></td>
<td><span data-ttu-id="c6cc2-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-745">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c6cc2-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c6cc2-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-749">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-750">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-751">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-751">10001</span></span></td>
<td><span data-ttu-id="c6cc2-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-752">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-753">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c6cc2-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c6cc2-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c6cc2-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c6cc2-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-757">Cost element</span></span></th>
<th><span data-ttu-id="c6cc2-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c6cc2-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-759">Amount</span></span></th>
<th><span data-ttu-id="c6cc2-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6cc2-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-761">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-762">HR</span></span></td>
<td><span data-ttu-id="c6cc2-763">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-763">10001</span></span></td>
<td><span data-ttu-id="c6cc2-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-764">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="c6cc2-766">-500.00</span></span></td>
<td><span data-ttu-id="c6cc2-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-768">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-769">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-770">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-770">10001</span></span></td>
<td><span data-ttu-id="c6cc2-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-771">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-773">175.00</span></span></td>
<td><span data-ttu-id="c6cc2-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-775">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-776">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-777">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-777">10001</span></span></td>
<td><span data-ttu-id="c6cc2-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-778">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-780">275.00</span></span></td>
<td><span data-ttu-id="c6cc2-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-782">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-783">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-784">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-784">10001</span></span></td>
<td><span data-ttu-id="c6cc2-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-785">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-787">50,00</span></span></td>
<td><span data-ttu-id="c6cc2-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-789">CC001</span></span></td>
<td><span data-ttu-id="c6cc2-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cc2-790">HR</span></span></td>
<td><span data-ttu-id="c6cc2-791">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-791">10001</span></span></td>
<td><span data-ttu-id="c6cc2-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-792">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-793">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c6cc2-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-796">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-797">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-798">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-798">10001</span></span></td>
<td><span data-ttu-id="c6cc2-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-799">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-800">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-801">436.00</span></span></td>
<td><span data-ttu-id="c6cc2-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-803">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-804">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-805">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-805">10001</span></span></td>
<td><span data-ttu-id="c6cc2-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-806">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-807">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c6cc2-808">685.14</span></span></td>
<td><span data-ttu-id="c6cc2-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-810">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-811">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-812">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-812">10001</span></span></td>
<td><span data-ttu-id="c6cc2-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-813">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-814">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c6cc2-815">124.57</span></span></td>
<td><span data-ttu-id="c6cc2-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-817">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-818">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-819">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-819">10001</span></span></td>
<td><span data-ttu-id="c6cc2-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-820">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-822">-675.00</span></span></td>
<td><span data-ttu-id="c6cc2-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-824">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-825">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-826">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-826">10001</span></span></td>
<td><span data-ttu-id="c6cc2-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-827">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c6cc2-829">438.75</span></span></td>
<td><span data-ttu-id="c6cc2-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-831">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-832">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-833">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-833">10001</span></span></td>
<td><span data-ttu-id="c6cc2-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-834">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c6cc2-836">236.25</span></span></td>
<td><span data-ttu-id="c6cc2-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-838">CC002</span></span></td>
<td><span data-ttu-id="c6cc2-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-839">Finance</span></span></td>
<td><span data-ttu-id="c6cc2-840">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-840">10001</span></span></td>
<td><span data-ttu-id="c6cc2-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-841">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-842">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="c6cc2-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c6cc2-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-845">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-846">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-847">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-847">10001</span></span></td>
<td><span data-ttu-id="c6cc2-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-848">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-849">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c6cc2-850">5,297.69</span></span></td>
<td><span data-ttu-id="c6cc2-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-852">CC004</span></span></td>
<td><span data-ttu-id="c6cc2-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c6cc2-853">Packaging</span></span></td>
<td><span data-ttu-id="c6cc2-854">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-854">10001</span></span></td>
<td><span data-ttu-id="c6cc2-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-855">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-856">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c6cc2-857">2,852.60</span></span></td>
<td><span data-ttu-id="c6cc2-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-859">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-860">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-861">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-861">10001</span></span></td>
<td><span data-ttu-id="c6cc2-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-862">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c6cc2-864">-713.75</span></span></td>
<td><span data-ttu-id="c6cc2-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-866">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-867">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-868">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-868">10001</span></span></td>
<td><span data-ttu-id="c6cc2-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-869">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c6cc2-871">535.31</span></span></td>
<td><span data-ttu-id="c6cc2-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-873">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-874">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-875">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-875">10001</span></span></td>
<td><span data-ttu-id="c6cc2-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-876">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c6cc2-878">178.44</span></span></td>
<td><span data-ttu-id="c6cc2-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-880">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-881">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-882">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-882">10001</span></span></td>
<td><span data-ttu-id="c6cc2-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-883">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-884">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="c6cc2-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c6cc2-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-887">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-888">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-889">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-889">10001</span></span></td>
<td><span data-ttu-id="c6cc2-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-890">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-891">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c6cc2-892">4,487.12</span></span></td>
<td><span data-ttu-id="c6cc2-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-894">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-895">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-896">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-896">10001</span></span></td>
<td><span data-ttu-id="c6cc2-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-897">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-898">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c6cc2-899">1,495.71</span></span></td>
<td><span data-ttu-id="c6cc2-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-901">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-902">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-903">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-903">10001</span></span></td>
<td><span data-ttu-id="c6cc2-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-904">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="c6cc2-906">-286.25</span></span></td>
<td><span data-ttu-id="c6cc2-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-908">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-909">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-910">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-910">10001</span></span></td>
<td><span data-ttu-id="c6cc2-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-911">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c6cc2-913">241.05</span></span></td>
<td><span data-ttu-id="c6cc2-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-915">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-916">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-917">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-917">10001</span></span></td>
<td><span data-ttu-id="c6cc2-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-918">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c6cc2-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c6cc2-920">45.20</span></span></td>
<td><span data-ttu-id="c6cc2-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-922">CC003</span></span></td>
<td><span data-ttu-id="c6cc2-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="c6cc2-923">Assembly</span></span></td>
<td><span data-ttu-id="c6cc2-924">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-924">10001</span></span></td>
<td><span data-ttu-id="c6cc2-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-925">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-926">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="c6cc2-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c6cc2-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-929">Prod 1</span></span></td>
<td><span data-ttu-id="c6cc2-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-930">Product 1</span></span></td>
<td><span data-ttu-id="c6cc2-931">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-931">10001</span></span></td>
<td><span data-ttu-id="c6cc2-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-932">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-933">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c6cc2-934">2,507.09</span></span></td>
<td><span data-ttu-id="c6cc2-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6cc2-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-936">Prod 2</span></span></td>
<td><span data-ttu-id="c6cc2-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-937">Product 2</span></span></td>
<td><span data-ttu-id="c6cc2-938">10001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-938">10001</span></span></td>
<td><span data-ttu-id="c6cc2-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-939">Electricity</span></span></td>
<td><span data-ttu-id="c6cc2-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-940">Variable cost</span></span></td>
<td><span data-ttu-id="c6cc2-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c6cc2-941">470.08</span></span></td>
<td><span data-ttu-id="c6cc2-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="c6cc2-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c6cc2-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="c6cc2-943">Conclusion</span></span>
<span data-ttu-id="c6cc2-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="c6cc2-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c6cc2-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="c6cc2-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c6cc2-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="c6cc2-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c6cc2-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c6cc2-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c6cc2-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c6cc2-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="c6cc2-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c6cc2-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c6cc2-951">CC099</span></span></th>
<th><span data-ttu-id="c6cc2-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c6cc2-952">CC001</span></span></th>
<th><span data-ttu-id="c6cc2-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c6cc2-953">CC002</span></span></th>
<th><span data-ttu-id="c6cc2-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c6cc2-954">CC003</span></span></th>
<th><span data-ttu-id="c6cc2-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c6cc2-955">CC004</span></span></th>
<th><span data-ttu-id="c6cc2-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-956">Proj 1</span></span></th>
<th><span data-ttu-id="c6cc2-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-957">Proj 2</span></span></th>
<th><span data-ttu-id="c6cc2-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="c6cc2-958">Prod 1</span></span></th>
<th><span data-ttu-id="c6cc2-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="c6cc2-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c6cc2-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="c6cc2-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c6cc2-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="c6cc2-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-971">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c6cc2-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="c6cc2-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-973">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-974">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-975">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-976">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-977">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c6cc2-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c6cc2-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c6cc2-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-982">000</span><span class="sxs-lookup"><span data-stu-id="c6cc2-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-983">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-984">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-985">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-986">0.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-987">30.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-988">10.00</span><span class="sxs-lookup"><span data-stu-id="c6cc2-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c6cc2-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c6cc2-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c6cc2-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c6cc2-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c6cc2-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c6cc2-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="c6cc2-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c6cc2-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c6cc2-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c6cc2-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c6cc2-996">สำหรับข้อมูลเพิ่มเติม ให้ดู [การรวบรวมต้นทุน](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="c6cc2-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



