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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180167"
---
# <a name="overhead-calculation"></a><span data-ttu-id="06f80-103">การคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="06f80-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06f80-104">หัวข้อนี้อธิบายกระบวนการทั่วไปสำหรับการคำนวณและการปันส่วนต้นทุนค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="06f80-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="06f80-105">คำนิยามข้อความ</span><span class="sxs-lookup"><span data-stu-id="06f80-105">Term definition</span></span>
---------------

<span data-ttu-id="06f80-106">ต้นทุนค่าโสหุ้ยคือต้นทุนที่จะเกิดขึ้นเมื่อต้องการรันธุรกิจ แต่ที่ไม่สามารถจัดสรรให้กับกิจกรรมทางธุรกิจเฉพาะ ผลิตภัณฑ์ หรือการบริการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="06f80-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="06f80-107">ต้นทุนค่าโสหุ้ยให้การสนับสนุนที่สำคัญสำหรับการสร้างกิจกรรมที่ทำกำไร</span><span class="sxs-lookup"><span data-stu-id="06f80-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="06f80-108">ต่อไปนี้เป็นตัวอย่างบางรายการของต้นทุนค่าโสหุ้ย:</span><span class="sxs-lookup"><span data-stu-id="06f80-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="06f80-109">ค่าเช่า</span><span class="sxs-lookup"><span data-stu-id="06f80-109">Rent</span></span>
-   <span data-ttu-id="06f80-110">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-110">Electricity</span></span>
-   <span data-ttu-id="06f80-111">เงินเดือนในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="06f80-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="06f80-112">ภาพรวมการคำนวณค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="06f80-112">Overhead calculation overview</span></span>
<span data-ttu-id="06f80-113">การคำนวณค่าโสหุ้ยรันนโยบายการบัญชีต้นทุนในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="06f80-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="06f80-114">คุณสามารถรันการคำนวณโสหุ้ยได้หลายครั้งสำหรับรอบระยะเวลาทางบัญชีเดียวกัน ถ้ามีการเปลี่ยนแปลงนโยบายการบัญชีต้นทุนหรือมีการตรวจพบข้อผิดพลาดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="06f80-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="06f80-115">การรันการคำนวณโสหุ้ยแต่ละครั้งจะถูกเก็บไว้ และรับรหัสเวอร์ชันที่ไม่ซ้ำกันที่จะช่วยให้คุณสามารถเปรียบเทียบการคำนวณในเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="06f80-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="06f80-116">รายการต้นทุนที่การคำนวณค่าโสหุ้ยที่สร้างขึ้นได้รับวันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="06f80-117">วันที่ลงบัญชีนี้ตรงกับวันที่สิ้นสุดของรอบระยะเวลาทางบัญชีที่ใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="06f80-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="06f80-118">รหัสเวอร์ชันที่ไม่ซ้ำกันประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="06f80-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="06f80-119">ชนิดของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="06f80-119">Version type</span></span>
-   <span data-ttu-id="06f80-120">วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="06f80-120">Date and time</span></span>
-   <span data-ttu-id="06f80-121">บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="06f80-122">ปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-122">Fiscal year</span></span>
-   <span data-ttu-id="06f80-123">รอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-123">Fiscal period</span></span>

<span data-ttu-id="06f80-124">การคำนวณค่าโสหุ้ยได้รับการรันโดยอิสระจากเวอร์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="06f80-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="06f80-125">ดังนั้น คุณสามารถคำนวณเวอร์ชันงบประมาณก่อนเวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="06f80-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="06f80-126">การคำนวณค่าโสหุ้ยประกอบด้วยขั้นตอน 4 รายการดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06f80-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="06f80-127">ในแต่ละขั้นตอน ส่วนหัวของสมุดรายวันจะถูกสร้างขึ้นโดยมีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="06f80-128">ส่วนหัวของสมุดรายวันนี้จะเก็บข้อมูลป้อนเข้าสำหรับแต่ละขั้นตอนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="06f80-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="06f80-129">นโยบายและกฎจะใช้กับแต่ละบรรทัดสมุดรายวัน และรายการต้นทุนจะถูกสร้างเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="06f80-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="06f80-130">ดังนั้น คุณจึงมีความสามารถในการติดตามเสมอ</span><span class="sxs-lookup"><span data-stu-id="06f80-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="06f80-131">[![การคำนวณค่าโสหุ้ย](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="06f80-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="06f80-132">คำนวณและปันส่วนต้นทุนค่าโสหุ้ยไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="06f80-133">ในการบัญชีทางการเงิน ต้นทุนบางอย่าง เช่น ไฟฟ้า จะถูกลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="06f80-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="06f80-134">ดังนั้น รายละเอียดข้อมูลเชิงลึกเชิงจัดการจึงไม่ได้มีไว้สำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="06f80-135">ในการบัญชีต้นทุน เพื่อให้ข้อมูลเชิงลึกเชิงจัดการที่ถูกต้องระหว่างหน่วยงานและระดับทั้งหมด ต้นทุนต้องไหลผ่านหน่วยงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="06f80-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="06f80-136">ขั้นตอนนี้ต้องยึดตามเรกคอร์ดที่ถูกต้องของปริมาณการใช้วัสดุหรือการประเมินที่ยุติธรรม</span><span class="sxs-lookup"><span data-stu-id="06f80-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="06f80-137">ในบัญชีแยกประเภททั่วไป ต้นทุนไฟฟ้าสามารถลงรายการดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06f80-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-138">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-139">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-140">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="06f80-140">Main account</span></span></th>
<th><span data-ttu-id="06f80-141">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-142">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="06f80-143">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-143">CC099</span></span></td>
<td><span data-ttu-id="06f80-144">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-144">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-145">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-145">10001</span></span></td>
<td><span data-ttu-id="06f80-146">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-146">Electricity</span></span></td>
<td><span data-ttu-id="06f80-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="06f80-148">ขั้นตอนที่ 1: ดำเนินการคำนวณพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="06f80-149">โดยค่าเริ่มต้น เมื่อมีการนำเข้ารายการต้นทุนจากข้อมูลแหล่งที่มา จะได้รับการจัดประเภทของพฤติกรรมต้นทุน **ไม่ได้จัดประเภท** ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="06f80-150">โดยการใช้กฎนโยบายพฤติกรรมต้นทุน คุณสามารถจัดประเภทรายการต้นทุนเป็น **ต้นทุนคงที่** หรือ **ต้นทุนผันแปร**ได้</span><span class="sxs-lookup"><span data-stu-id="06f80-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="06f80-151">กำหนดกฎพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-151">Define the cost behavior rule</span></span>

<span data-ttu-id="06f80-152">ในบางกรณี ส่วนหนึ่งของต้นทุนจะเป็นค่าธรรมเนียมคงที่ และต้นทุนที่เหลือจะขึ้นอยู่กับปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="06f80-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="06f80-153">บิลไฟฟ้ามักจะตรงกับคำนิยามนี้</span><span class="sxs-lookup"><span data-stu-id="06f80-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="06f80-154">หลังจากที่คุณชำระเงินค่าธรรมเนียมคงที่เฉพาะเจาะจง คุณจะต้องชำระเงินสำหรับปริมาณการใช้วัสดุต่อชั่วโมงเป็นกิโลวัตต์ (Kwh)</span><span class="sxs-lookup"><span data-stu-id="06f80-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="06f80-155">ตัวอย่างเช่น ถ้าค่าธรรมเนียมต้นทุนคงที่คือ 1, 000.00 นี่เป็นวิธีกำหนดกฎพฤติกรรมต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="06f80-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="06f80-156">ยอดคงที่ 1,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="06f80-157">0 &lt;= 1,000.00 = คงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="06f80-158">1000,01 &lt; N = ผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="06f80-159">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-160">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-160">Journal</span></span></th>
<th><span data-ttu-id="06f80-161">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="06f80-162">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="06f80-163">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="06f80-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-164">00001</span><span class="sxs-lookup"><span data-stu-id="06f80-164">00001</span></span></td>
<td><span data-ttu-id="06f80-165">สมุดรายวันของพฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="06f80-166">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-166">Fiscal</span></span></td>
<td><span data-ttu-id="06f80-167">2017</span><span class="sxs-lookup"><span data-stu-id="06f80-167">2017</span></span></td>
<td><span data-ttu-id="06f80-168">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-168">Period 1</span></span></td>
<td><span data-ttu-id="06f80-169">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="06f80-170">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="06f80-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-171">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-172">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-173">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-173">Cost element</span></span></th>
<th><span data-ttu-id="06f80-174">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-174">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-175">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-176">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="06f80-177">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-177">CC099</span></span></td>
<td><span data-ttu-id="06f80-178">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-178">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-179">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-179">10001</span></span></td>
<td><span data-ttu-id="06f80-180">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-180">Electricity</span></span></td>
<td><span data-ttu-id="06f80-181">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="06f80-181">Unclassified</span></span></td>
<td><span data-ttu-id="06f80-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="06f80-183">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-184">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-185">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-185">Cost element</span></span></th>
<th><span data-ttu-id="06f80-186">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-186">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-187">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-187">Amount</span></span></th>
<th><span data-ttu-id="06f80-188">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-189">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-189">CC099</span></span></td>
<td><span data-ttu-id="06f80-190">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-190">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-191">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-191">10001</span></span></td>
<td><span data-ttu-id="06f80-192">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-192">Electricity</span></span></td>
<td><span data-ttu-id="06f80-193">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="06f80-193">Unclassified</span></span></td>
<td><span data-ttu-id="06f80-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-194">10,000.00</span></span></td>
<td><span data-ttu-id="06f80-195">3 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-196">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-196">CC099</span></span></td>
<td><span data-ttu-id="06f80-197">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-197">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-198">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-198">10001</span></span></td>
<td><span data-ttu-id="06f80-199">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-199">Electricity</span></span></td>
<td><span data-ttu-id="06f80-200">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="06f80-200">Unclassified</span></span></td>
<td><span data-ttu-id="06f80-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-201">-10,000.00</span></span></td>
<td><span data-ttu-id="06f80-202">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-203">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-203">CC099</span></span></td>
<td><span data-ttu-id="06f80-204">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-204">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-205">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-205">10001</span></span></td>
<td><span data-ttu-id="06f80-206">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-206">Electricity</span></span></td>
<td><span data-ttu-id="06f80-207">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-207">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-208">1,000.00</span></span></td>
<td><span data-ttu-id="06f80-209">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-210">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-210">CC099</span></span></td>
<td><span data-ttu-id="06f80-211">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-211">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-212">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-212">10001</span></span></td>
<td><span data-ttu-id="06f80-213">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-213">Electricity</span></span></td>
<td><span data-ttu-id="06f80-214">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-214">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-215">9,000.00</span></span></td>
<td><span data-ttu-id="06f80-216">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-217">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายพฤติกรรมต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="06f80-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="06f80-218">ขั้นตอนที่ 2: ดำเนินการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="06f80-219">การกระจายต้นทุนจะใช้ในการกระจายต้นทุนจากออบเจ็กต์ต้นทุนหนึ่งไปยังออบเจ็กต์ต้นทุนอื่นอย่างน้อยหนึ่งรายการโดยใช้ฐานการปันส่วนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="06f80-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="06f80-220">การกระจายต้นทุนและการปันส่วนต้นทุนแตกต่างกันในแง่ที่ว่าการกระจายต้นทุนจะเกิดขึ้นในระดับขององค์ประกอบต้นทุนหลักของต้นทุนเดิมเสมอ</span><span class="sxs-lookup"><span data-stu-id="06f80-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="06f80-221">กำหนดกฎการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-221">Define the cost distribution rule</span></span>

<span data-ttu-id="06f80-222">ในการบัญชีทางการเงิน ต้นทุนไฟฟ้ามักจะลงทะเบียนเป็นจำนวนเงินรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="06f80-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="06f80-223">ในการบัญชีต้นทุน วิธีการนี้ยังให้รายละเอียดไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="06f80-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="06f80-224">ควรกระจายต้นทุนผันแปรไปยังแต่ละออบเจ็กต์ต้นทุนตามปกติ</span><span class="sxs-lookup"><span data-stu-id="06f80-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="06f80-225">เกณฑ์การปันส่วนทางตรรกะมากที่สุดคือปริมาณการใช้พลังงานไฟฟ้า (Kwh)</span><span class="sxs-lookup"><span data-stu-id="06f80-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="06f80-226">สมาชิกมิติทางสถิติที่มีชื่อว่าไฟฟ้าถูกสร้างขึ้น และมีการบันทึกปริมาณการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="06f80-227">โดยค่าเริ่มต้น สมาชิกมิติทางสถิติทั้งหมดจะพร้อมใช้งานเป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-228">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-228">Cost object</span></span></th>
<th><span data-ttu-id="06f80-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="06f80-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-230">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-230">CC001</span></span></td>
<td><span data-ttu-id="06f80-231">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-231">HR</span></span></td>
<td><span data-ttu-id="06f80-232">1,000</span><span class="sxs-lookup"><span data-stu-id="06f80-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-233">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-233">CC002</span></span></td>
<td><span data-ttu-id="06f80-234">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-234">Finance</span></span></td>
<td><span data-ttu-id="06f80-235">6,000</span><span class="sxs-lookup"><span data-stu-id="06f80-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-236">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-236">CC003</span></span></td>
<td><span data-ttu-id="06f80-237">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-237">Assembly</span></span></td>
<td><span data-ttu-id="06f80-238">0</span><span class="sxs-lookup"><span data-stu-id="06f80-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-239">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-240">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-240">Cost object</span></span></th>
<th><span data-ttu-id="06f80-241">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-241">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-242">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-242">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-243">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-244">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-244">CC001</span></span></td>
<td><span data-ttu-id="06f80-245">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-245">HR</span></span></td>
<td><span data-ttu-id="06f80-246">1,000</span><span class="sxs-lookup"><span data-stu-id="06f80-246">1,000</span></span></td>
<td><span data-ttu-id="06f80-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="06f80-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="06f80-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-249">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-249">CC002</span></span></td>
<td><span data-ttu-id="06f80-250">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-250">Finance</span></span></td>
<td><span data-ttu-id="06f80-251">6,000</span><span class="sxs-lookup"><span data-stu-id="06f80-251">6,000</span></span></td>
<td><span data-ttu-id="06f80-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="06f80-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="06f80-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-254">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-254">CC003</span></span></td>
<td><span data-ttu-id="06f80-255">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-255">Assembly</span></span></td>
<td><span data-ttu-id="06f80-256">0</span><span class="sxs-lookup"><span data-stu-id="06f80-256">0</span></span></td>
<td><span data-ttu-id="06f80-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="06f80-258">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-259">ควรกระจายต้นทุนคงที่เท่ากันกับแต่ละออบเจ็กต์ต้นทุนที่มีการใช้ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="06f80-260">คุณสามารถใช้ผลลัพธ์นี้โดยใช้สมาชิกของมิติทางสถิติไฟฟ้าในฐานการปันส่วนตามสูตร: (ไฟฟ้า &gt; 0.00) ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้ปริมาณการใช้ไฟฟ้าเป็นฐานการปันส่วนสำหรับต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-261">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-261">Cost object</span></span></th>
<th><span data-ttu-id="06f80-262">สูตร</span><span class="sxs-lookup"><span data-stu-id="06f80-262">Formula</span></span></th>
<th><span data-ttu-id="06f80-263">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-263">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-264">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-264">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-265">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-266">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-266">CC001</span></span></td>
<td><span data-ttu-id="06f80-267">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-267">HR</span></span></td>
<td><span data-ttu-id="06f80-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="06f80-269">1</span><span class="sxs-lookup"><span data-stu-id="06f80-269">1</span></span></td>
<td><span data-ttu-id="06f80-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="06f80-271">500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-272">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-272">CC002</span></span></td>
<td><span data-ttu-id="06f80-273">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-273">Finance</span></span></td>
<td><span data-ttu-id="06f80-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="06f80-275">1</span><span class="sxs-lookup"><span data-stu-id="06f80-275">1</span></span></td>
<td><span data-ttu-id="06f80-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="06f80-277">500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-278">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-278">CC003</span></span></td>
<td><span data-ttu-id="06f80-279">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-279">Assembly</span></span></td>
<td><span data-ttu-id="06f80-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="06f80-281">0</span><span class="sxs-lookup"><span data-stu-id="06f80-281">0</span></span></td>
<td><span data-ttu-id="06f80-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="06f80-283">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="06f80-284">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-285">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-285">Journal</span></span></th>
<th><span data-ttu-id="06f80-286">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="06f80-287">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="06f80-288">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="06f80-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-289">00002</span><span class="sxs-lookup"><span data-stu-id="06f80-289">00002</span></span></td>
<td><span data-ttu-id="06f80-290">สมุดรายวันการคำนวณการกระจายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="06f80-291">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-291">Fiscal</span></span></td>
<td><span data-ttu-id="06f80-292">2017</span><span class="sxs-lookup"><span data-stu-id="06f80-292">2017</span></span></td>
<td><span data-ttu-id="06f80-293">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-293">Period 1</span></span></td>
<td><span data-ttu-id="06f80-294">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="06f80-295">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="06f80-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-296">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-297">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-298">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-298">Cost element</span></span></th>
<th><span data-ttu-id="06f80-299">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-299">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-300">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-301">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-302">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-302">CC099</span></span></td>
<td><span data-ttu-id="06f80-303">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-303">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-304">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-304">10001</span></span></td>
<td><span data-ttu-id="06f80-305">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-305">Electricity</span></span></td>
<td><span data-ttu-id="06f80-306">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-306">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-308">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-309">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-309">CC099</span></span></td>
<td><span data-ttu-id="06f80-310">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-310">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-311">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-311">10001</span></span></td>
<td><span data-ttu-id="06f80-312">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-312">Electricity</span></span></td>
<td><span data-ttu-id="06f80-313">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-313">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="06f80-315">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-316">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-317">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-317">Cost element</span></span></th>
<th><span data-ttu-id="06f80-318">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-318">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-319">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-319">Amount</span></span></th>
<th><span data-ttu-id="06f80-320">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-321">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-321">CC099</span></span></td>
<td><span data-ttu-id="06f80-322">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-322">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-323">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-323">10001</span></span></td>
<td><span data-ttu-id="06f80-324">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-324">Electricity</span></span></td>
<td><span data-ttu-id="06f80-325">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-325">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-326">-1,000.00.</span><span class="sxs-lookup"><span data-stu-id="06f80-326">-1,000.00</span></span></td>
<td><span data-ttu-id="06f80-327">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-328">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-328">CC001</span></span></td>
<td><span data-ttu-id="06f80-329">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-329">HR</span></span></td>
<td><span data-ttu-id="06f80-330">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-330">10001</span></span></td>
<td><span data-ttu-id="06f80-331">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-331">Electricity</span></span></td>
<td><span data-ttu-id="06f80-332">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-332">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-333">500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-333">500.00</span></span></td>
<td><span data-ttu-id="06f80-334">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-335">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-335">CC002</span></span></td>
<td><span data-ttu-id="06f80-336">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-336">Finance</span></span></td>
<td><span data-ttu-id="06f80-337">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-337">10001</span></span></td>
<td><span data-ttu-id="06f80-338">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-338">Electricity</span></span></td>
<td><span data-ttu-id="06f80-339">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-339">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-340">500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-340">500.00</span></span></td>
<td><span data-ttu-id="06f80-341">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-342">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-342">CC099</span></span></td>
<td><span data-ttu-id="06f80-343">ศูนย์ต้นทุนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="06f80-343">Default cost center</span></span></td>
<td><span data-ttu-id="06f80-344">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-344">10001</span></span></td>
<td><span data-ttu-id="06f80-345">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-345">Electricity</span></span></td>
<td><span data-ttu-id="06f80-346">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-346">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="06f80-347">-9,000.00</span></span></td>
<td><span data-ttu-id="06f80-348">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-349">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-349">CC001</span></span></td>
<td><span data-ttu-id="06f80-350">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-350">HR</span></span></td>
<td><span data-ttu-id="06f80-351">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-351">10001</span></span></td>
<td><span data-ttu-id="06f80-352">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-352">Electricity</span></span></td>
<td><span data-ttu-id="06f80-353">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-353">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="06f80-354">1,285.71</span></span></td>
<td><span data-ttu-id="06f80-355">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-356">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-356">CC002</span></span></td>
<td><span data-ttu-id="06f80-357">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-357">Finance</span></span></td>
<td><span data-ttu-id="06f80-358">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-358">10001</span></span></td>
<td><span data-ttu-id="06f80-359">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-359">Electricity</span></span></td>
<td><span data-ttu-id="06f80-360">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-360">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="06f80-361">7,714.29</span></span></td>
<td><span data-ttu-id="06f80-362">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-363">สำหรับข้อมูลเพิ่มเติม ดู [สร้างและกำหนดนโยบายการกระจายต้นทุนไปยังหน่วยการควบคุมต้นทุน](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="06f80-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="06f80-364">ขั้นตอนที่ 3: ดำเนินการคำนวณอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="06f80-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="06f80-365">อัตราค่าโสหุ้ยจะถูกใช้ในการเรียกเก็บออบเจ็กต์ต้นทุนเฉพาะอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="06f80-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="06f80-366">ค่าธรรมเนียมจะขึ้นอยู่กับอัตราต้นทุนที่กำหนดไว้ล่วงหน้าและขนาดจากฐานการปันส่วนที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="06f80-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="06f80-367">กำหนดอัตราค่าโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="06f80-367">Define the overhead rate</span></span>

<span data-ttu-id="06f80-368">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรสำหรับชุดของโครงการภายใน</span><span class="sxs-lookup"><span data-stu-id="06f80-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="06f80-369">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าโครงการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="06f80-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-370">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-370">Cost object</span></span></th>
<th><span data-ttu-id="06f80-371">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="06f80-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-372">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-372">Proj 1</span></span></td>
<td><span data-ttu-id="06f80-373">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-373">Project 1</span></span></td>
<td><span data-ttu-id="06f80-374">3</span><span class="sxs-lookup"><span data-stu-id="06f80-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-375">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-375">Proj 2</span></span></td>
<td><span data-ttu-id="06f80-376">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-376">Project 2</span></span></td>
<td><span data-ttu-id="06f80-377">1</span><span class="sxs-lookup"><span data-stu-id="06f80-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-378">มีการกำหนดอัตราต้นทุนที่กำหนดไว้ล่วงหน้าสำหรับการกระจายโครงการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-379">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-379">Cost object</span></span></th>
<th><span data-ttu-id="06f80-380">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-380">Cost element</span></span></th>
<th><span data-ttu-id="06f80-381">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-381">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-382">หน่วย</span><span class="sxs-lookup"><span data-stu-id="06f80-382">Units</span></span></th>
<th><span data-ttu-id="06f80-383">อัตรา</span><span class="sxs-lookup"><span data-stu-id="06f80-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-384">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-384">CC001</span></span></td>
<td><span data-ttu-id="06f80-385">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-385">HR</span></span></td>
<td><span data-ttu-id="06f80-386">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-386">10001</span></span></td>
<td><span data-ttu-id="06f80-387">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-387">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-388">1</span><span class="sxs-lookup"><span data-stu-id="06f80-388">1</span></span></td>
<td><span data-ttu-id="06f80-389">10</span><span class="sxs-lookup"><span data-stu-id="06f80-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-390">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้โครงการ HR เป็นฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-391">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-391">Cost object</span></span></th>
<th><span data-ttu-id="06f80-392">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-392">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-393">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-393">Cost element</span></span></th>
<th><span data-ttu-id="06f80-394">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-394">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-395">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-396">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-396">Proj 1</span></span></td>
<td><span data-ttu-id="06f80-397">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-397">Project 1</span></span></td>
<td><span data-ttu-id="06f80-398">3</span><span class="sxs-lookup"><span data-stu-id="06f80-398">3</span></span></td>
<td><span data-ttu-id="06f80-399">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-399">10001</span></span></td>
<td><span data-ttu-id="06f80-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="06f80-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="06f80-401">30.00</span><span class="sxs-lookup"><span data-stu-id="06f80-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-402">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-402">Proj 2</span></span></td>
<td><span data-ttu-id="06f80-403">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-403">Project 2</span></span></td>
<td><span data-ttu-id="06f80-404">1</span><span class="sxs-lookup"><span data-stu-id="06f80-404">1</span></span></td>
<td><span data-ttu-id="06f80-405">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-405">10001</span></span></td>
<td><span data-ttu-id="06f80-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="06f80-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="06f80-407">10.00</span><span class="sxs-lookup"><span data-stu-id="06f80-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="06f80-408">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-409">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-409">Journal</span></span></th>
<th><span data-ttu-id="06f80-410">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="06f80-411">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="06f80-412">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="06f80-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-413">00003</span><span class="sxs-lookup"><span data-stu-id="06f80-413">00003</span></span></td>
<td><span data-ttu-id="06f80-414">สมุดรายวันการคำนวณอัตราโสหุ้ย</span><span class="sxs-lookup"><span data-stu-id="06f80-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="06f80-415">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-415">Fiscal</span></span></td>
<td><span data-ttu-id="06f80-416">2017</span><span class="sxs-lookup"><span data-stu-id="06f80-416">2017</span></span></td>
<td><span data-ttu-id="06f80-417">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-417">Period 1</span></span></td>
<td><span data-ttu-id="06f80-418">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="06f80-419">รายการสมุดรายวัน (รายการสมุดรายวันสำหรับการคำนวณอัตราโสหุ้ย)</span><span class="sxs-lookup"><span data-stu-id="06f80-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-420">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-421">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-421">Cost object</span></span></th>
<th><span data-ttu-id="06f80-422">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-423">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-424">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-424">Proj 1</span></span></td>
<td><span data-ttu-id="06f80-425">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="06f80-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="06f80-426">3.00</span><span class="sxs-lookup"><span data-stu-id="06f80-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-427">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-428">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-428">Proj 2</span></span></td>
<td><span data-ttu-id="06f80-429">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="06f80-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="06f80-430">1.00</span><span class="sxs-lookup"><span data-stu-id="06f80-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="06f80-431">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-432">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-433">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-433">Cost element</span></span></th>
<th><span data-ttu-id="06f80-434">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-434">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-435">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-435">Amount</span></span></th>
<th><span data-ttu-id="06f80-436">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="06f80-437">CC0001</span></span></td>
<td><span data-ttu-id="06f80-438">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-438">HR</span></span></td>
<td><span data-ttu-id="06f80-439">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-439">10001</span></span></td>
<td><span data-ttu-id="06f80-440">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-440">Electricity</span></span></td>
<td><span data-ttu-id="06f80-441">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-441">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="06f80-442">-30.00</span></span></td>
<td><span data-ttu-id="06f80-443">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-444">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-444">Proj 1</span></span></td>
<td><span data-ttu-id="06f80-445">โครงการภายใน 1</span><span class="sxs-lookup"><span data-stu-id="06f80-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="06f80-446">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-446">10001</span></span></td>
<td><span data-ttu-id="06f80-447">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-447">Electricity</span></span></td>
<td><span data-ttu-id="06f80-448">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-448">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-449">30.00</span><span class="sxs-lookup"><span data-stu-id="06f80-449">30.00</span></span></td>
<td><span data-ttu-id="06f80-450">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-451">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-451">CC001</span></span></td>
<td><span data-ttu-id="06f80-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-452">HR</span></span></td>
<td><span data-ttu-id="06f80-453">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-453">10001</span></span></td>
<td><span data-ttu-id="06f80-454">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-454">Electricity</span></span></td>
<td><span data-ttu-id="06f80-455">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-455">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="06f80-456">-10.00</span></span></td>
<td><span data-ttu-id="06f80-457">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-458">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-458">Proj 2</span></span></td>
<td><span data-ttu-id="06f80-459">โครงการภายใน 2</span><span class="sxs-lookup"><span data-stu-id="06f80-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="06f80-460">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-460">10001</span></span></td>
<td><span data-ttu-id="06f80-461">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-461">Electricity</span></span></td>
<td><span data-ttu-id="06f80-462">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-462">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-463">10.00</span><span class="sxs-lookup"><span data-stu-id="06f80-463">10.00</span></span></td>
<td><span data-ttu-id="06f80-464">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-465">สำหรับข้อมูลเพิ่มเติม โปรดดู [ทำการคำนวณค่าโสหุ้ย](cost-rollup.md#perform-overhead-calculation)</span><span class="sxs-lookup"><span data-stu-id="06f80-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="06f80-466">ขั้นตอนที่ 4: ดำเนินการคำนวณการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="06f80-467">การปันส่วนถูกนำมาใช้ในการปันส่วนยอดดุลของออบเจ็กต์ต้นทุนหนึ่งกับออบเจ็กต์ต้นทุนอื่นโดยใช้ฐานการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="06f80-468">Finance สนับสนุนวิธีการปันส่วนต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="06f80-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="06f80-469">ในวิธีการปันส่วนต่างตอบแทน มีการรับรู้การบริการที่มีร่วมกันที่ออบเจ็กต์ต้นทุนเสริมแลกเปลี่ยนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="06f80-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="06f80-470">ระบบกำหนดลำดับที่ถูกต้องในการดำเนินการปันส่วนโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="06f80-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="06f80-471">ยอดดุลของออบเจ็กต์ต้นทุนมีการปันส่วนโดยฐานการปันส่วนเดียว</span><span class="sxs-lookup"><span data-stu-id="06f80-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="06f80-472">การปันส่วนในมิติออบเจ็กต์ต้นทุนและสมาชิกที่เกี่ยวข้องได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="06f80-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="06f80-473">ลำดับการปันส่วนจะถูกควบคุมโดยหน่วยควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="06f80-474">[![วิธีการต่างตอบแทน](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="06f80-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="06f80-475">กำหนดการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-475">Define the cost allocation</span></span>

<span data-ttu-id="06f80-476">นี่คือตัวอย่างง่าย ๆ ที่อธิบายวิธีที่คุณสามารถติดตามกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="06f80-477">ออบเจ็กต์ต้นทุน CC001 HR จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="06f80-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="06f80-478">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการ HR เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="06f80-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-479">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-479">Cost object</span></span></th>
<th><span data-ttu-id="06f80-480">บริการ HR</span><span class="sxs-lookup"><span data-stu-id="06f80-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-481">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-481">CC002</span></span></td>
<td><span data-ttu-id="06f80-482">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-482">Finance</span></span></td>
<td><span data-ttu-id="06f80-483">35</span><span class="sxs-lookup"><span data-stu-id="06f80-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-484">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-484">CC003</span></span></td>
<td><span data-ttu-id="06f80-485">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-485">Assembly</span></span></td>
<td><span data-ttu-id="06f80-486">55</span><span class="sxs-lookup"><span data-stu-id="06f80-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-487">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-487">CC004</span></span></td>
<td><span data-ttu-id="06f80-488">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-488">Packaging</span></span></td>
<td><span data-ttu-id="06f80-489">10</span><span class="sxs-lookup"><span data-stu-id="06f80-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-490">ออบเจ็กต์ต้นทุน CC002 การเงินจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="06f80-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="06f80-491">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการการเงินเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="06f80-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-492">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-492">Cost object</span></span></th>
<th><span data-ttu-id="06f80-493">บริการการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-494">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-494">CC003</span></span></td>
<td><span data-ttu-id="06f80-495">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-495">Assembly</span></span></td>
<td><span data-ttu-id="06f80-496">65</span><span class="sxs-lookup"><span data-stu-id="06f80-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-497">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-497">CC004</span></span></td>
<td><span data-ttu-id="06f80-498">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-498">Packaging</span></span></td>
<td><span data-ttu-id="06f80-499">35</span><span class="sxs-lookup"><span data-stu-id="06f80-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-500">ออบเจ็กต์ต้นทุน CC003 ส่วนประกอบจัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="06f80-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="06f80-501">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการส่วนประกอบเพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="06f80-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-502">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-502">Cost object</span></span></th>
<th><span data-ttu-id="06f80-503">บริการส่วนประกอบ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="06f80-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-504">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-504">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-505">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-505">Product 1</span></span></td>
<td><span data-ttu-id="06f80-506">60</span><span class="sxs-lookup"><span data-stu-id="06f80-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-507">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-507">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-508">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-508">Product 2</span></span></td>
<td><span data-ttu-id="06f80-509">20</span><span class="sxs-lookup"><span data-stu-id="06f80-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-510">ออบเจ็กต์ต้นทุน CC004 บรรจุภัณฑ์จัดสรรไปยังออบเจ็กต์ต้นทุนหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="06f80-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="06f80-511">มีการสร้างสมาชิกมิติทางสถิติที่มีชื่อว่าบริการบรรจุภัณฑ์เพื่อวัดขนาดที่ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="06f80-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-512">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-512">Cost object</span></span></th>
<th><span data-ttu-id="06f80-513">บริการบรรจุภัณฑ์ (ชั่วโมง)</span><span class="sxs-lookup"><span data-stu-id="06f80-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-514">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-514">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-515">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-515">Product 1</span></span></td>
<td><span data-ttu-id="06f80-516">80</span><span class="sxs-lookup"><span data-stu-id="06f80-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-517">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-517">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-518">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-518">Product 2</span></span></td>
<td><span data-ttu-id="06f80-519">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="06f80-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="06f80-520">การประเมินทางสถิติ เช่น จำนวนชั่วโมงการผลิตที่ผลิตภัณฑ์ใช้สามารถได้รับมาจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="06f80-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="06f80-521">สำหรับข้อมูลเพิ่มเติม ดู [เท็มเพลตผู้ให้บริการการประเมินทางสถิติ](statistical-measure-provider-template.md#statistical-measure-provider-template)</span><span class="sxs-lookup"><span data-stu-id="06f80-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="06f80-522">ตารางต่อไปนี้แสดงผลลัพธ์ เมื่อมีการใช้บริการ HR เป็นฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="06f80-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-523">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-523">Cost object</span></span></th>
<th><span data-ttu-id="06f80-524">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-524">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-525">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-525">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-526">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-526">Amount</span></span></th>
<th><span data-ttu-id="06f80-527">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-528">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-528">CC002</span></span></td>
<td><span data-ttu-id="06f80-529">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-529">Finance</span></span></td>
<td><span data-ttu-id="06f80-530">35</span><span class="sxs-lookup"><span data-stu-id="06f80-530">35</span></span></td>
<td><span data-ttu-id="06f80-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="06f80-532">175.00</span><span class="sxs-lookup"><span data-stu-id="06f80-532">175.00</span></span></td>
<td><span data-ttu-id="06f80-533">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-534">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-534">CC003</span></span></td>
<td><span data-ttu-id="06f80-535">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-535">Assembly</span></span></td>
<td><span data-ttu-id="06f80-536">55</span><span class="sxs-lookup"><span data-stu-id="06f80-536">55</span></span></td>
<td><span data-ttu-id="06f80-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="06f80-538">275.00</span><span class="sxs-lookup"><span data-stu-id="06f80-538">275.00</span></span></td>
<td><span data-ttu-id="06f80-539">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-540">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-540">CC004</span></span></td>
<td><span data-ttu-id="06f80-541">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-541">Packaging</span></span></td>
<td><span data-ttu-id="06f80-542">10</span><span class="sxs-lookup"><span data-stu-id="06f80-542">10</span></span></td>
<td><span data-ttu-id="06f80-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="06f80-544">50.00</span><span class="sxs-lookup"><span data-stu-id="06f80-544">50.00</span></span></td>
<td><span data-ttu-id="06f80-545">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-546">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-546">CC002</span></span></td>
<td><span data-ttu-id="06f80-547">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-547">Finance</span></span></td>
<td><span data-ttu-id="06f80-548">35</span><span class="sxs-lookup"><span data-stu-id="06f80-548">35</span></span></td>
<td><span data-ttu-id="06f80-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="06f80-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="06f80-550">436.00</span><span class="sxs-lookup"><span data-stu-id="06f80-550">436.00</span></span></td>
<td><span data-ttu-id="06f80-551">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-552">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-552">CC003</span></span></td>
<td><span data-ttu-id="06f80-553">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-553">Assembly</span></span></td>
<td><span data-ttu-id="06f80-554">55</span><span class="sxs-lookup"><span data-stu-id="06f80-554">55</span></span></td>
<td><span data-ttu-id="06f80-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="06f80-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="06f80-556">685.14</span><span class="sxs-lookup"><span data-stu-id="06f80-556">685.14</span></span></td>
<td><span data-ttu-id="06f80-557">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-558">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-558">CC004</span></span></td>
<td><span data-ttu-id="06f80-559">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-559">Packaging</span></span></td>
<td><span data-ttu-id="06f80-560">10</span><span class="sxs-lookup"><span data-stu-id="06f80-560">10</span></span></td>
<td><span data-ttu-id="06f80-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="06f80-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="06f80-562">124.57</span><span class="sxs-lookup"><span data-stu-id="06f80-562">124.57</span></span></td>
<td><span data-ttu-id="06f80-563">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-564">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการการเงินกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="06f80-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-565">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-565">Cost object</span></span></th>
<th><span data-ttu-id="06f80-566">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-566">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-567">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-567">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-568">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-568">Amount</span></span></th>
<th><span data-ttu-id="06f80-569">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-570">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-570">CC003</span></span></td>
<td><span data-ttu-id="06f80-571">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-571">Assembly</span></span></td>
<td><span data-ttu-id="06f80-572">65</span><span class="sxs-lookup"><span data-stu-id="06f80-572">65</span></span></td>
<td><span data-ttu-id="06f80-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="06f80-574">438.75</span><span class="sxs-lookup"><span data-stu-id="06f80-574">438.75</span></span></td>
<td><span data-ttu-id="06f80-575">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-576">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-576">CC004</span></span></td>
<td><span data-ttu-id="06f80-577">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-577">Packaging</span></span></td>
<td><span data-ttu-id="06f80-578">35</span><span class="sxs-lookup"><span data-stu-id="06f80-578">35</span></span></td>
<td><span data-ttu-id="06f80-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="06f80-580">236.25</span><span class="sxs-lookup"><span data-stu-id="06f80-580">236.25</span></span></td>
<td><span data-ttu-id="06f80-581">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-582">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-582">CC003</span></span></td>
<td><span data-ttu-id="06f80-583">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-583">Assembly</span></span></td>
<td><span data-ttu-id="06f80-584">65</span><span class="sxs-lookup"><span data-stu-id="06f80-584">65</span></span></td>
<td><span data-ttu-id="06f80-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="06f80-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="06f80-586">5,297.69</span></span></td>
<td><span data-ttu-id="06f80-587">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-588">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-588">CC004</span></span></td>
<td><span data-ttu-id="06f80-589">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-589">Packaging</span></span></td>
<td><span data-ttu-id="06f80-590">35</span><span class="sxs-lookup"><span data-stu-id="06f80-590">35</span></span></td>
<td><span data-ttu-id="06f80-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="06f80-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="06f80-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="06f80-592">2,852.60</span></span></td>
<td><span data-ttu-id="06f80-593">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-594">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการส่วนประกอบกับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="06f80-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-595">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-595">Cost object</span></span></th>
<th><span data-ttu-id="06f80-596">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-596">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-597">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-597">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-598">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-598">Amount</span></span></th>
<th><span data-ttu-id="06f80-599">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-600">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-600">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-601">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-601">Product 1</span></span></td>
<td><span data-ttu-id="06f80-602">60</span><span class="sxs-lookup"><span data-stu-id="06f80-602">60</span></span></td>
<td><span data-ttu-id="06f80-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="06f80-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="06f80-604">535.31</span><span class="sxs-lookup"><span data-stu-id="06f80-604">535.31</span></span></td>
<td><span data-ttu-id="06f80-605">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-606">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-606">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-607">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-607">Product 2</span></span></td>
<td><span data-ttu-id="06f80-608">20</span><span class="sxs-lookup"><span data-stu-id="06f80-608">20</span></span></td>
<td><span data-ttu-id="06f80-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="06f80-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="06f80-610">178.44</span><span class="sxs-lookup"><span data-stu-id="06f80-610">178.44</span></span></td>
<td><span data-ttu-id="06f80-611">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-612">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-612">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-613">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-613">Product 1</span></span></td>
<td><span data-ttu-id="06f80-614">60</span><span class="sxs-lookup"><span data-stu-id="06f80-614">60</span></span></td>
<td><span data-ttu-id="06f80-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="06f80-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="06f80-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="06f80-616">4,487.12</span></span></td>
<td><span data-ttu-id="06f80-617">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-618">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-618">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-619">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-619">Product 2</span></span></td>
<td><span data-ttu-id="06f80-620">20</span><span class="sxs-lookup"><span data-stu-id="06f80-620">20</span></span></td>
<td><span data-ttu-id="06f80-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="06f80-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="06f80-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="06f80-622">1,495.71</span></span></td>
<td><span data-ttu-id="06f80-623">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06f80-624">ตารางต่อไปนี้แสดงผลลัพธ์เมื่อมีการใช้บริการบรรจุภัณฑ์กับฐานการปันส่วนสำหรับต้นทุนรวม (ต้นทุนคงที่และต้นทุนผันแปร)</span><span class="sxs-lookup"><span data-stu-id="06f80-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-625">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-625">Cost object</span></span></th>
<th><span data-ttu-id="06f80-626">ขนาด</span><span class="sxs-lookup"><span data-stu-id="06f80-626">Magnitude</span></span></th>
<th><span data-ttu-id="06f80-627">ตัวคูณการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="06f80-627">Allocation factor</span></span></th>
<th><span data-ttu-id="06f80-628">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-628">Amount</span></span></th>
<th><span data-ttu-id="06f80-629">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-630">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-630">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-631">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-631">Product 1</span></span></td>
<td><span data-ttu-id="06f80-632">80</span><span class="sxs-lookup"><span data-stu-id="06f80-632">80</span></span></td>
<td><span data-ttu-id="06f80-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="06f80-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="06f80-634">241.05</span><span class="sxs-lookup"><span data-stu-id="06f80-634">241.05</span></span></td>
<td><span data-ttu-id="06f80-635">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-636">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-636">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-637">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-637">Product 2</span></span></td>
<td><span data-ttu-id="06f80-638">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="06f80-638">15</span></span></td>
<td><span data-ttu-id="06f80-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="06f80-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="06f80-640">45.20</span><span class="sxs-lookup"><span data-stu-id="06f80-640">45.20</span></span></td>
<td><span data-ttu-id="06f80-641">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-642">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-642">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-643">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-643">Product 1</span></span></td>
<td><span data-ttu-id="06f80-644">80</span><span class="sxs-lookup"><span data-stu-id="06f80-644">80</span></span></td>
<td><span data-ttu-id="06f80-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="06f80-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="06f80-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="06f80-646">2,507.09</span></span></td>
<td><span data-ttu-id="06f80-647">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-648">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-648">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-649">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-649">Product 2</span></span></td>
<td><span data-ttu-id="06f80-650">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="06f80-650">15</span></span></td>
<td><span data-ttu-id="06f80-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="06f80-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="06f80-652">470.08</span><span class="sxs-lookup"><span data-stu-id="06f80-652">470.08</span></span></td>
<td><span data-ttu-id="06f80-653">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="06f80-654">รายการสมุดรายวัน (รายการสมุดรายวันของยอดดุลออบเจ็กต์ต้นทุน)</span><span class="sxs-lookup"><span data-stu-id="06f80-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-655">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-655">Journal</span></span></th>
<th><span data-ttu-id="06f80-656">ชนิดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="06f80-657">รอบระยะเวลาปฏิทินทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="06f80-658">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="06f80-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-659">00004</span><span class="sxs-lookup"><span data-stu-id="06f80-659">00004</span></span></td>
<td><span data-ttu-id="06f80-660">สมุดรายวันการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="06f80-661">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-661">Fiscal</span></span></td>
<td><span data-ttu-id="06f80-662">2017</span><span class="sxs-lookup"><span data-stu-id="06f80-662">2017</span></span></td>
<td><span data-ttu-id="06f80-663">รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-663">Period 1</span></span></td>
<td><span data-ttu-id="06f80-664">การคำนวณค่าโสหุ้ย / 01-02-2017 11:51:00 PM / บัญชีแยกประเภท /2017 / รอบระยะเวลา 1</span><span class="sxs-lookup"><span data-stu-id="06f80-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="06f80-665">รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="06f80-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="06f80-666">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-667">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-668">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-668">Cost element</span></span></th>
<th><span data-ttu-id="06f80-669">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-669">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-670">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-671">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-672">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-672">CC001</span></span></td>
<td><span data-ttu-id="06f80-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-673">HR</span></span></td>
<td><span data-ttu-id="06f80-674">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-674">10001</span></span></td>
<td><span data-ttu-id="06f80-675">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-675">Electricity</span></span></td>
<td><span data-ttu-id="06f80-676">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-676">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-677">500.00</span><span class="sxs-lookup"><span data-stu-id="06f80-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-678">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-679">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-679">CC001</span></span></td>
<td><span data-ttu-id="06f80-680">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-680">HR</span></span></td>
<td><span data-ttu-id="06f80-681">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-681">10001</span></span></td>
<td><span data-ttu-id="06f80-682">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-682">Electricity</span></span></td>
<td><span data-ttu-id="06f80-683">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-683">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="06f80-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-685">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-686">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-686">CC002</span></span></td>
<td><span data-ttu-id="06f80-687">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-687">Finance</span></span></td>
<td><span data-ttu-id="06f80-688">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-688">10001</span></span></td>
<td><span data-ttu-id="06f80-689">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-689">Electricity</span></span></td>
<td><span data-ttu-id="06f80-690">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-690">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-691">675.00</span><span class="sxs-lookup"><span data-stu-id="06f80-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-692">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-693">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-693">CC002</span></span></td>
<td><span data-ttu-id="06f80-694">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-694">Finance</span></span></td>
<td><span data-ttu-id="06f80-695">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-695">10001</span></span></td>
<td><span data-ttu-id="06f80-696">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-696">Electricity</span></span></td>
<td><span data-ttu-id="06f80-697">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-697">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="06f80-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-699">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-700">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-700">CC003</span></span></td>
<td><span data-ttu-id="06f80-701">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-701">Assembly</span></span></td>
<td><span data-ttu-id="06f80-702">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-702">10001</span></span></td>
<td><span data-ttu-id="06f80-703">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-703">Electricity</span></span></td>
<td><span data-ttu-id="06f80-704">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-704">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-705">713.75</span><span class="sxs-lookup"><span data-stu-id="06f80-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-706">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-707">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-707">CC003</span></span></td>
<td><span data-ttu-id="06f80-708">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-708">Assembly</span></span></td>
<td><span data-ttu-id="06f80-709">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-709">10001</span></span></td>
<td><span data-ttu-id="06f80-710">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-710">Electricity</span></span></td>
<td><span data-ttu-id="06f80-711">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-711">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="06f80-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-713">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-714">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-714">CC003</span></span></td>
<td><span data-ttu-id="06f80-715">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-715">Packaging</span></span></td>
<td><span data-ttu-id="06f80-716">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-716">10001</span></span></td>
<td><span data-ttu-id="06f80-717">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-717">Electricity</span></span></td>
<td><span data-ttu-id="06f80-718">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-718">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-719">286.25</span><span class="sxs-lookup"><span data-stu-id="06f80-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-720">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-721">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-721">CC003</span></span></td>
<td><span data-ttu-id="06f80-722">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-722">Packaging</span></span></td>
<td><span data-ttu-id="06f80-723">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-723">10001</span></span></td>
<td><span data-ttu-id="06f80-724">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-724">Electricity</span></span></td>
<td><span data-ttu-id="06f80-725">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-725">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="06f80-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-727">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-728">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-728">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-729">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-729">Product 1</span></span></td>
<td><span data-ttu-id="06f80-730">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-730">10001</span></span></td>
<td><span data-ttu-id="06f80-731">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-731">Electricity</span></span></td>
<td><span data-ttu-id="06f80-732">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-732">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-733">776.36</span><span class="sxs-lookup"><span data-stu-id="06f80-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-734">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-735">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-735">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-736">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-736">Product 1</span></span></td>
<td><span data-ttu-id="06f80-737">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-737">10001</span></span></td>
<td><span data-ttu-id="06f80-738">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-738">Electricity</span></span></td>
<td><span data-ttu-id="06f80-739">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-739">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="06f80-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-741">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-742">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-742">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-743">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-743">Product 1</span></span></td>
<td><span data-ttu-id="06f80-744">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-744">10001</span></span></td>
<td><span data-ttu-id="06f80-745">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-745">Electricity</span></span></td>
<td><span data-ttu-id="06f80-746">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-746">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-747">223.64</span><span class="sxs-lookup"><span data-stu-id="06f80-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-748">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="06f80-749">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-749">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-750">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-750">Product 1</span></span></td>
<td><span data-ttu-id="06f80-751">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-751">10001</span></span></td>
<td><span data-ttu-id="06f80-752">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-752">Electricity</span></span></td>
<td><span data-ttu-id="06f80-753">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-753">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="06f80-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="06f80-755">รายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="06f80-756">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="06f80-757">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-757">Cost element</span></span></th>
<th><span data-ttu-id="06f80-758">พฤติกรรมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-758">Cost behavior</span></span></th>
<th><span data-ttu-id="06f80-759">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-759">Amount</span></span></th>
<th><span data-ttu-id="06f80-760">วันที่ลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="06f80-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="06f80-761">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-761">CC001</span></span></td>
<td><span data-ttu-id="06f80-762">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-762">HR</span></span></td>
<td><span data-ttu-id="06f80-763">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-763">10001</span></span></td>
<td><span data-ttu-id="06f80-764">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-764">Electricity</span></span></td>
<td><span data-ttu-id="06f80-765">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-765">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-766">-500.00.</span><span class="sxs-lookup"><span data-stu-id="06f80-766">-500.00</span></span></td>
<td><span data-ttu-id="06f80-767">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-768">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-768">CC002</span></span></td>
<td><span data-ttu-id="06f80-769">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-769">Finance</span></span></td>
<td><span data-ttu-id="06f80-770">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-770">10001</span></span></td>
<td><span data-ttu-id="06f80-771">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-771">Electricity</span></span></td>
<td><span data-ttu-id="06f80-772">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-772">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-773">175.00</span><span class="sxs-lookup"><span data-stu-id="06f80-773">175.00</span></span></td>
<td><span data-ttu-id="06f80-774">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-775">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-775">CC003</span></span></td>
<td><span data-ttu-id="06f80-776">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-776">Assembly</span></span></td>
<td><span data-ttu-id="06f80-777">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-777">10001</span></span></td>
<td><span data-ttu-id="06f80-778">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-778">Electricity</span></span></td>
<td><span data-ttu-id="06f80-779">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-779">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-780">275.00</span><span class="sxs-lookup"><span data-stu-id="06f80-780">275.00</span></span></td>
<td><span data-ttu-id="06f80-781">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-782">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-782">CC004</span></span></td>
<td><span data-ttu-id="06f80-783">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-783">Packaging</span></span></td>
<td><span data-ttu-id="06f80-784">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-784">10001</span></span></td>
<td><span data-ttu-id="06f80-785">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-785">Electricity</span></span></td>
<td><span data-ttu-id="06f80-786">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-786">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-787">50,00</span><span class="sxs-lookup"><span data-stu-id="06f80-787">50,00</span></span></td>
<td><span data-ttu-id="06f80-788">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-789">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-789">CC001</span></span></td>
<td><span data-ttu-id="06f80-790">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="06f80-790">HR</span></span></td>
<td><span data-ttu-id="06f80-791">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-791">10001</span></span></td>
<td><span data-ttu-id="06f80-792">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-792">Electricity</span></span></td>
<td><span data-ttu-id="06f80-793">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-793">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="06f80-794">-1,245.71</span></span></td>
<td><span data-ttu-id="06f80-795">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-796">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-796">CC002</span></span></td>
<td><span data-ttu-id="06f80-797">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-797">Finance</span></span></td>
<td><span data-ttu-id="06f80-798">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-798">10001</span></span></td>
<td><span data-ttu-id="06f80-799">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-799">Electricity</span></span></td>
<td><span data-ttu-id="06f80-800">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-800">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-801">436.00</span><span class="sxs-lookup"><span data-stu-id="06f80-801">436.00</span></span></td>
<td><span data-ttu-id="06f80-802">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-803">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-803">CC003</span></span></td>
<td><span data-ttu-id="06f80-804">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-804">Assembly</span></span></td>
<td><span data-ttu-id="06f80-805">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-805">10001</span></span></td>
<td><span data-ttu-id="06f80-806">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-806">Electricity</span></span></td>
<td><span data-ttu-id="06f80-807">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-807">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-808">685.14</span><span class="sxs-lookup"><span data-stu-id="06f80-808">685.14</span></span></td>
<td><span data-ttu-id="06f80-809">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-810">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-810">CC004</span></span></td>
<td><span data-ttu-id="06f80-811">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-811">Packaging</span></span></td>
<td><span data-ttu-id="06f80-812">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-812">10001</span></span></td>
<td><span data-ttu-id="06f80-813">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-813">Electricity</span></span></td>
<td><span data-ttu-id="06f80-814">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-814">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-815">124.57</span><span class="sxs-lookup"><span data-stu-id="06f80-815">124.57</span></span></td>
<td><span data-ttu-id="06f80-816">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-817">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-817">CC002</span></span></td>
<td><span data-ttu-id="06f80-818">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-818">Finance</span></span></td>
<td><span data-ttu-id="06f80-819">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-819">10001</span></span></td>
<td><span data-ttu-id="06f80-820">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-820">Electricity</span></span></td>
<td><span data-ttu-id="06f80-821">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-821">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="06f80-822">-675.00</span></span></td>
<td><span data-ttu-id="06f80-823">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-824">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-824">CC003</span></span></td>
<td><span data-ttu-id="06f80-825">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-825">Assembly</span></span></td>
<td><span data-ttu-id="06f80-826">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-826">10001</span></span></td>
<td><span data-ttu-id="06f80-827">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-827">Electricity</span></span></td>
<td><span data-ttu-id="06f80-828">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-828">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-829">438.75</span><span class="sxs-lookup"><span data-stu-id="06f80-829">438.75</span></span></td>
<td><span data-ttu-id="06f80-830">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-831">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-831">CC004</span></span></td>
<td><span data-ttu-id="06f80-832">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-832">Packaging</span></span></td>
<td><span data-ttu-id="06f80-833">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-833">10001</span></span></td>
<td><span data-ttu-id="06f80-834">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-834">Electricity</span></span></td>
<td><span data-ttu-id="06f80-835">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-835">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-836">236.25</span><span class="sxs-lookup"><span data-stu-id="06f80-836">236.25</span></span></td>
<td><span data-ttu-id="06f80-837">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-838">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-838">CC002</span></span></td>
<td><span data-ttu-id="06f80-839">การเงิน</span><span class="sxs-lookup"><span data-stu-id="06f80-839">Finance</span></span></td>
<td><span data-ttu-id="06f80-840">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-840">10001</span></span></td>
<td><span data-ttu-id="06f80-841">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-841">Electricity</span></span></td>
<td><span data-ttu-id="06f80-842">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-842">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="06f80-843">-8,150.29</span></span></td>
<td><span data-ttu-id="06f80-844">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-845">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-845">CC003</span></span></td>
<td><span data-ttu-id="06f80-846">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-846">Assembly</span></span></td>
<td><span data-ttu-id="06f80-847">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-847">10001</span></span></td>
<td><span data-ttu-id="06f80-848">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-848">Electricity</span></span></td>
<td><span data-ttu-id="06f80-849">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-849">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="06f80-850">5,297.69</span></span></td>
<td><span data-ttu-id="06f80-851">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-852">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-852">CC004</span></span></td>
<td><span data-ttu-id="06f80-853">บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="06f80-853">Packaging</span></span></td>
<td><span data-ttu-id="06f80-854">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-854">10001</span></span></td>
<td><span data-ttu-id="06f80-855">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-855">Electricity</span></span></td>
<td><span data-ttu-id="06f80-856">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-856">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="06f80-857">2,852.60</span></span></td>
<td><span data-ttu-id="06f80-858">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-859">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-859">CC003</span></span></td>
<td><span data-ttu-id="06f80-860">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-860">Assembly</span></span></td>
<td><span data-ttu-id="06f80-861">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-861">10001</span></span></td>
<td><span data-ttu-id="06f80-862">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-862">Electricity</span></span></td>
<td><span data-ttu-id="06f80-863">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-863">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="06f80-864">-713.75</span></span></td>
<td><span data-ttu-id="06f80-865">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-866">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-866">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-867">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-867">Product 1</span></span></td>
<td><span data-ttu-id="06f80-868">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-868">10001</span></span></td>
<td><span data-ttu-id="06f80-869">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-869">Electricity</span></span></td>
<td><span data-ttu-id="06f80-870">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-870">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-871">535.31</span><span class="sxs-lookup"><span data-stu-id="06f80-871">535.31</span></span></td>
<td><span data-ttu-id="06f80-872">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-873">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-873">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-874">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-874">Product 2</span></span></td>
<td><span data-ttu-id="06f80-875">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-875">10001</span></span></td>
<td><span data-ttu-id="06f80-876">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-876">Electricity</span></span></td>
<td><span data-ttu-id="06f80-877">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-877">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-878">178.44</span><span class="sxs-lookup"><span data-stu-id="06f80-878">178.44</span></span></td>
<td><span data-ttu-id="06f80-879">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-880">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-880">CC003</span></span></td>
<td><span data-ttu-id="06f80-881">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-881">Assembly</span></span></td>
<td><span data-ttu-id="06f80-882">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-882">10001</span></span></td>
<td><span data-ttu-id="06f80-883">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-883">Electricity</span></span></td>
<td><span data-ttu-id="06f80-884">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-884">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="06f80-885">-5,982.83</span></span></td>
<td><span data-ttu-id="06f80-886">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-887">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-887">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-888">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-888">Product 1</span></span></td>
<td><span data-ttu-id="06f80-889">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-889">10001</span></span></td>
<td><span data-ttu-id="06f80-890">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-890">Electricity</span></span></td>
<td><span data-ttu-id="06f80-891">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-891">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="06f80-892">4,487.12</span></span></td>
<td><span data-ttu-id="06f80-893">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-894">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-894">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-895">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-895">Product 2</span></span></td>
<td><span data-ttu-id="06f80-896">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-896">10001</span></span></td>
<td><span data-ttu-id="06f80-897">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-897">Electricity</span></span></td>
<td><span data-ttu-id="06f80-898">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-898">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="06f80-899">1,495.71</span></span></td>
<td><span data-ttu-id="06f80-900">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-901">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-901">CC003</span></span></td>
<td><span data-ttu-id="06f80-902">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-902">Assembly</span></span></td>
<td><span data-ttu-id="06f80-903">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-903">10001</span></span></td>
<td><span data-ttu-id="06f80-904">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-904">Electricity</span></span></td>
<td><span data-ttu-id="06f80-905">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-905">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="06f80-906">-286.25</span></span></td>
<td><span data-ttu-id="06f80-907">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-908">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-908">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-909">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-909">Product 1</span></span></td>
<td><span data-ttu-id="06f80-910">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-910">10001</span></span></td>
<td><span data-ttu-id="06f80-911">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-911">Electricity</span></span></td>
<td><span data-ttu-id="06f80-912">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-912">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-913">241.05</span><span class="sxs-lookup"><span data-stu-id="06f80-913">241.05</span></span></td>
<td><span data-ttu-id="06f80-914">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-915">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-915">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-916">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-916">Product 2</span></span></td>
<td><span data-ttu-id="06f80-917">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-917">10001</span></span></td>
<td><span data-ttu-id="06f80-918">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-918">Electricity</span></span></td>
<td><span data-ttu-id="06f80-919">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-919">Fixed cost</span></span></td>
<td><span data-ttu-id="06f80-920">45.20</span><span class="sxs-lookup"><span data-stu-id="06f80-920">45.20</span></span></td>
<td><span data-ttu-id="06f80-921">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-922">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-922">CC003</span></span></td>
<td><span data-ttu-id="06f80-923">ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="06f80-923">Assembly</span></span></td>
<td><span data-ttu-id="06f80-924">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-924">10001</span></span></td>
<td><span data-ttu-id="06f80-925">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-925">Electricity</span></span></td>
<td><span data-ttu-id="06f80-926">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-926">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="06f80-927">-2,977.17</span></span></td>
<td><span data-ttu-id="06f80-928">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-929">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-929">Prod 1</span></span></td>
<td><span data-ttu-id="06f80-930">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-930">Product 1</span></span></td>
<td><span data-ttu-id="06f80-931">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-931">10001</span></span></td>
<td><span data-ttu-id="06f80-932">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-932">Electricity</span></span></td>
<td><span data-ttu-id="06f80-933">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-933">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="06f80-934">2,507.09</span></span></td>
<td><span data-ttu-id="06f80-935">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06f80-936">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-936">Prod 2</span></span></td>
<td><span data-ttu-id="06f80-937">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-937">Product 2</span></span></td>
<td><span data-ttu-id="06f80-938">10001</span><span class="sxs-lookup"><span data-stu-id="06f80-938">10001</span></span></td>
<td><span data-ttu-id="06f80-939">ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-939">Electricity</span></span></td>
<td><span data-ttu-id="06f80-940">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-940">Variable cost</span></span></td>
<td><span data-ttu-id="06f80-941">470.08</span><span class="sxs-lookup"><span data-stu-id="06f80-941">470.08</span></span></td>
<td><span data-ttu-id="06f80-942">31 มกราคม 2017</span><span class="sxs-lookup"><span data-stu-id="06f80-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="06f80-943">บทสรุป</span><span class="sxs-lookup"><span data-stu-id="06f80-943">Conclusion</span></span>
<span data-ttu-id="06f80-944">ในการบัญชีทางการเงิน ต้นทุน 10,000.00 สำหรับไฟฟ้าจะถูกลงรายการบัญชีไปยังรหัสศูนย์ต้นทุนดัมมี</span><span class="sxs-lookup"><span data-stu-id="06f80-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="06f80-945">ดังนั้น ผู้จัดทำบัญชีต้นทุนจะทราบว่าต้องปันส่วนต้นทุนนี้</span><span class="sxs-lookup"><span data-stu-id="06f80-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="06f80-946">ในการบัญชีต้นทุน ขั้นตอนของต้นทุนระหว่างหน่วยงานและระดับต่าง ๆ ขึ้นอยู่กับนโยบายและกฎที่ใช้</span><span class="sxs-lookup"><span data-stu-id="06f80-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="06f80-947">ต้นทุนแต่ละรายการถูกเชื่อมโยงกับฐานการปันส่วนที่แสดงการประเมินที่ดีที่สุดสำหรับการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="06f80-948">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="06f80-949">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="06f80-950">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="06f80-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="06f80-951">CC099</span><span class="sxs-lookup"><span data-stu-id="06f80-951">CC099</span></span></th>
<th><span data-ttu-id="06f80-952">CC001</span><span class="sxs-lookup"><span data-stu-id="06f80-952">CC001</span></span></th>
<th><span data-ttu-id="06f80-953">CC002</span><span class="sxs-lookup"><span data-stu-id="06f80-953">CC002</span></span></th>
<th><span data-ttu-id="06f80-954">CC003</span><span class="sxs-lookup"><span data-stu-id="06f80-954">CC003</span></span></th>
<th><span data-ttu-id="06f80-955">CC004</span><span class="sxs-lookup"><span data-stu-id="06f80-955">CC004</span></span></th>
<th><span data-ttu-id="06f80-956">โครงการ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-956">Proj 1</span></span></th>
<th><span data-ttu-id="06f80-957">โครงการ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-957">Proj 2</span></span></th>
<th><span data-ttu-id="06f80-958">ผลิตภัณฑ์ 1</span><span class="sxs-lookup"><span data-stu-id="06f80-958">Prod 1</span></span></th>
<th><span data-ttu-id="06f80-959">ผลิตภัณฑ์ 2</span><span class="sxs-lookup"><span data-stu-id="06f80-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="06f80-960">10001 ไฟฟ้า</span><span class="sxs-lookup"><span data-stu-id="06f80-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="06f80-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="06f80-970">ไม่ได้จัดประเภท</span><span class="sxs-lookup"><span data-stu-id="06f80-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-971">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="06f80-972">ต้นทุนคงที่</span><span class="sxs-lookup"><span data-stu-id="06f80-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-973">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-974">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-975">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-976">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-977">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="06f80-978">776.36</span><span class="sxs-lookup"><span data-stu-id="06f80-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-979">223.64</span><span class="sxs-lookup"><span data-stu-id="06f80-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="06f80-981">ต้นทุนผันแปร</span><span class="sxs-lookup"><span data-stu-id="06f80-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-982">000</span><span class="sxs-lookup"><span data-stu-id="06f80-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-983">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-984">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-985">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-986">0.00</span><span class="sxs-lookup"><span data-stu-id="06f80-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-987">30.00</span><span class="sxs-lookup"><span data-stu-id="06f80-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-988">10.00</span><span class="sxs-lookup"><span data-stu-id="06f80-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="06f80-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="06f80-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="06f80-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="06f80-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="06f80-992">หัวข้อนี้อธิบายวิธีการไหลขององค์ประกอบต้นทุนหลัก 10001 ไฟฟ้า 10001 ผ่านออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="06f80-993">ดังนั้น ต้นทุนค่าโสหุ้ยนี้จึงมีการปันส่วนไปยังระดับต่ำสุดในองค์กร</span><span class="sxs-lookup"><span data-stu-id="06f80-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="06f80-994">กล่าวคือ ออบเจ็กต์ต้นทุนในระดับต่ำสุดเป็นผู้รับผิดชอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="06f80-995">ถ้าคุณต้องการขั้นตอนที่เป็นภาพของต้นทุนระหว่างออบเจ็กต์ต้นทุนต่าง ๆ คุณสามารถใช้กฎนโยบายการรวบรวมต้นทุนเพื่อแสดงภาพของกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="06f80-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="06f80-996">สำหรับข้อมูลเพิ่มเติม ให้ดู [การรวบรวมต้นทุน](cost-rollup.md)</span><span class="sxs-lookup"><span data-stu-id="06f80-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



