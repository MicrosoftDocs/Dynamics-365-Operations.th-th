---
title: "วิธีการคำนวณภาษีขายในฟิลด์จุดเริ่มต้น"
description: "บทความนี้อธิบายถึงตัวเลือกในฟิลด์จุดเริ่มต้นในหน้ารหัสภาษีขาย และวิธีคำนวณภาษีขายตามตัวเลือกที่เลือกสำหรับรหัสภาษีขาย"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4c1e1a588e07b9f60880dcf1c34139c5c1ceba35
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="e518f-103">วิธีการคำนวณภาษีขายในฟิลด์จุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e518f-103">Sales tax calculation methods in the Origin field</span></span>

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

<span data-ttu-id="e518f-104">บทความนี้อธิบายถึงตัวเลือกในฟิลด์จุดเริ่มต้นในหน้ารหัสภาษีขาย และวิธีคำนวณภาษีขายตามตัวเลือกที่เลือกสำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="e518f-105">สำหรับรหัสภาษีขายแต่ละรหัสที่คุณสร้างในหน้ารหัสภาษีขาย คุณต้องเลือกวิธีการคำนวณที่จะใช้กับราคาฐานภาษีในฟิลด์จุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e518f-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="e518f-106">เปอร์เซ็นต์ของยอดเงินสุทธิ</span><span class="sxs-lookup"><span data-stu-id="e518f-106">Percentage of net amount</span></span>
<span data-ttu-id="e518f-107">เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินสุทธิเป็นค่าเริ่มต้นในฟิลด์จุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e518f-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="e518f-108">ภาษีขายจะคำนวณเป็นเปอร์เซ็นต์ของยอดซื้อหรือยอดขาย ที่ไม่รวมภาษีขายอื่นใด</span><span class="sxs-lookup"><span data-stu-id="e518f-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="e518f-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e518f-109">Example</span></span>

<span data-ttu-id="e518f-110">อัตราภาษีคือ 25%.</span><span class="sxs-lookup"><span data-stu-id="e518f-110">The tax rate is 25%.</span></span> <span data-ttu-id="e518f-111">บรรทัดใบแจ้งหนี้จะแสดงปริมาณของสินค้า 10 ชิ้น ในราคา 1.00 ต่อชิ้น และลูกค้าได้รับส่วนลด 10% ต่อรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="e518f-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="e518f-112">ยอดเงินสุทธิ: (10 x 1.00) -10% = 9.00 ภาษีขาย: 9.00 x 25% = 2.25 ยอดเงินรวม: 9.00 + 2.25 = 11.25</span><span class="sxs-lookup"><span data-stu-id="e518f-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="e518f-113"> เปอร์เซ็นต์ของยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="e518f-113">Percentage of gross amount</span></span>
<span data-ttu-id="e518f-114">ถ้าคุณเลือกวิธีเปอร์เซ็นต์ของยอดเงินรวม ภาษีขายจะถูกคำนวณเป็นเปอร์เซ็นต์ของยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="e518f-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="e518f-115">ยอดเงินรวมคือ รายการของยอดเงินสุทธิบวกรายการภาษีและค่าธรรมเนียมทั้งหมด ยกเว้นรายการภาษีจุดเริ่มต้น =เปอร์เซ็นต์ของยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="e518f-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="e518f-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e518f-116">Example</span></span>

<span data-ttu-id="e518f-117">หน่วยงานจัดเก็บภาษีได้กำหนดภาษีพิเศษสำหรับสินค้าชนิดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e518f-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="e518f-118">ยอดเงินภาษีจะถูกบวกเพิ่มเข้าไปในยอดเงินสุทธิก่อนคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="e518f-119">กำหนดรหัสภาษีขายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e518f-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="e518f-120">ภาษี 1 = 10% โดยใช้เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินสุทธิ</span><span class="sxs-lookup"><span data-stu-id="e518f-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="e518f-121">ภาษี 2 = 20% โดยใช้เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินสุทธิ</span><span class="sxs-lookup"><span data-stu-id="e518f-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="e518f-122">ภาษีขาย= 25% โดยใช้เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="e518f-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="e518f-123">ถ้ายอดเงินสุทธิ = 10.00 ดังนั้น ภาษี 1 = 1.00 x (10.00 x 10%) และ ภาษี 2 = 2.00 x (10.00 x 20%)</span><span class="sxs-lookup"><span data-stu-id="e518f-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="e518f-124">ยอดเงินจะเป็นดังนี้: ยอดเงินรวม: สุทธิภาษี + ยอดเงินสุทธิ + ยอดเงินภาษี 1 + ยอดเงินภาษี 2 (10.00 + 1.00 + 2.00) = 13.00 ภาษีขาย = 13.00 x 25% = 3.25 ยอดรวมภาษีและภาษีขาย: 1.00 + 2.00 + 3.25 = 6.25 ยอดเงินรวม: 10.00 + 6.25 = 16.25</span><span class="sxs-lookup"><span data-stu-id="e518f-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="e518f-125">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="e518f-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e518f-126">ภาษีจุดเริ่มต้นรหัสเดียวเท่านั้น = เปอร์เซ็นต์ของยอดเงินรวมที่สามารถใช้สำหรับธุรกรรมได้</span><span class="sxs-lookup"><span data-stu-id="e518f-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="e518f-127">ถ้าภาษีถูกกำหนดมากกว่าหนึงรหัสสำหรับธุรกรรม ข้อผิดพลาดจะถูกแสดงออกมาว่า ไม่สามารถคำนวณภาษีขายได้</span><span class="sxs-lookup"><span data-stu-id="e518f-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="e518f-128">เปอร์เซ็นต์ของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="e518f-129">เมื่อคุณเลือกเปอร์เซ็นต์ของภาษีขายในฟิลด์จุดเริ่มต้น ภาษีขายจะถูกคำนวณเป็นเปอร์เซ็นต์ของภาษีขายที่ถูกเลือกภาษีขายที่คิดจากฟิลด์ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="e518f-130">ภาษีขายที่ถูกเลือกในฟิลด์ภาษีขายภาษีขาย จะถูกคำนวณก่อน</span><span class="sxs-lookup"><span data-stu-id="e518f-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="e518f-131">ภาษีขายที่สองจะคำนวณตามยอดเงินภาษีขายแรก</span><span class="sxs-lookup"><span data-stu-id="e518f-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="e518f-132">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e518f-132">Example</span></span>

<span data-ttu-id="e518f-133">กำหนดรหัสภาษีขายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e518f-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="e518f-134">ภาษี 1 = 10% โดยใช้เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินสุทธิ</span><span class="sxs-lookup"><span data-stu-id="e518f-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="e518f-135">ภาษี 2 = 20% โดยใช้เปอร์เซ็นต์ของวิธีคำนวณภาษีขาย ด้วย ภาษี 1 ในภาษีขายที่คิดจากฟิลด์ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="e518f-136">ภาษีขาย= 25% โดยใช้เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="e518f-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="e518f-137">ยอดเงินสุทธิ: 10.00 ภาษี 1: 10.00 x 10% = 1.00 ภาษี 2: 1.00 x 20% = 0.20 ยอดเงินรวม: 10.00 + 1.00 + 0.20 = 11.20 ภาษีขาย: 11.20 x 25% = 2.80 รวมภาษีและภาษีขาย: 1.00 + 0.20 + 2.80 = 4.00 ยอดเงินรวม: 10.00 + 4.00 = 14.00</span><span class="sxs-lookup"><span data-stu-id="e518f-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="e518f-138">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="e518f-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e518f-139">ในการคำนวณภาษีจะไม่สามารถคำนวณภาษีหลายระดับได้</span><span class="sxs-lookup"><span data-stu-id="e518f-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="e518f-140">ภาษีจะไม่ถูกคำนวณตามภาษีที่ถูกคำนวณแล้วโดยภาษีอื่น</span><span class="sxs-lookup"><span data-stu-id="e518f-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="e518f-141">ภาษีหลายระดับและภาษีระดับเดียวตามรหัสภาษีสามารถคำนวณในธุรกรรมได้</span><span class="sxs-lookup"><span data-stu-id="e518f-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="e518f-142"> ยอดเงินต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="e518f-142">Amount per unit</span></span>
<span data-ttu-id="e518f-143">เมื่อคุณเลือกยอดเงินต่อหน่วยในฟิลด์จุดเริ่มต้น ภาษีขายจะคำนวณเป็นยอดเงินคงที่ต่อหน่วยคูณ ด้วยปริมาณป้อนไว้ในบรรทัดเอกสาร</span><span class="sxs-lookup"><span data-stu-id="e518f-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="e518f-144">หน่วยที่ต้องเลือกในฟิลด์หน่วย</span><span class="sxs-lookup"><span data-stu-id="e518f-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="e518f-145">ยอดเงินต่อหน่วยถูกระบุในหน้าค่ารหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="e518f-146">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e518f-146">Example</span></span>

<span data-ttu-id="e518f-147">รหัสภาษีขายถูกตั้งค่าเป็น: USD 1.20 ต่อหน่วย =กล่องในใบแจ้งหนี้การขายรายการ 25 กล่องของสินค้าที่ขาย ภาษีขายจะคำนวณเป็น 25 x 1.20 = 30.00</span><span class="sxs-lookup"><span data-stu-id="e518f-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="e518f-148">-**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="e518f-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e518f-149">ถ้ามีธุรกรรมถูกป้อนในหน่วยที่แตกต่างจากหน่วยที่ระบุในรหัสภาษีขาย ระบบจะแปลงค่าโดยอัตโนมัติตามการแปลงหน่วยที่ถูกตั้งค่าในหน้าการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="e518f-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="e518f-150"> ยอดเงินต่อหน่วย ตัวเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e518f-150">Amount per unit, additional option</span></span>

<span data-ttu-id="e518f-151">บนแท็บการคำนวณ คุณสามารถเลือกว่าภาษีที่ถูกคำนวณในยอดเงินต่อหน่วยจะคำนวณก่อนรหัสภาษีอื่น ๆ และเพิ่มเข้าในยอดเงินสุทธิได้ก่อนจุดเริ่มต้นของรหัสภาษีอื่น ๆ = เปอร์เซ็นต์ของยอดเงินสุทธิจะถูกคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e518f-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="e518f-152">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="e518f-152">Examples</span></span>

<span data-ttu-id="e518f-153">สมมติว่าเราคำนวณ 2 รหัสภาษีในธุรกรรม:</span><span class="sxs-lookup"><span data-stu-id="e518f-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="e518f-154">ภาษี: จุดเริ่มต้น = ยอดเงินต่อหน่วยและภาษีขาย ที่ตั้งค่าเป็น 5.00 ต่อหน่วย = ชิ้น</span><span class="sxs-lookup"><span data-stu-id="e518f-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="e518f-155">ภาษีขาย: จุดเริ่มต้น = ตั้งค่าเป็น 25% ดังที่แสดงในตัวอย่างด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="e518f-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="e518f-156">เราขายสินค้า1 ชิ้น ที่ราคาต่อหน่วย 10.00</span><span class="sxs-lookup"><span data-stu-id="e518f-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="e518f-157">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="e518f-157">Example 1</span></span>

<span data-ttu-id="e518f-158">ภาษีขาย: จุดเริ่มต้น = เปอร์เซ็นต์ของวิธีการคำนวณยอดเงินรวมก่อนภาษีขายตามตัวเลือกจะไม่มีผล เนื่องจากภาษีขายจะถูกคำนวณเป็นเปอร์เซ็นต์ของยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="e518f-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="e518f-159">ภาษี: 1 x 5.00 = 5.00 ยอดเงินรวม: 10.00 + 5.00 = 15.00 ภาษีขาย: 15.00 x 25% = 3.75 รวมภาษีขาย: 5.00 + 3.75 = 8.75 ยอดเงินรวม: 10.00 + 8.75 = 18.75</span><span class="sxs-lookup"><span data-stu-id="e518f-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="e518f-160">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="e518f-160">Example 2</span></span>

<span data-ttu-id="e518f-161">ภาษีขาย: จุดเริ่มต้น = เปอร์เซ็นต์ของยอดเงินสุทธิคำนวณก่อนภาษีขายจะไม่ถูกเลือกสำหรับการคำนวณภาษี</span><span class="sxs-lookup"><span data-stu-id="e518f-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="e518f-162">ยอดเงินสุทธิ: 10.00 ภาษี: 1 x 5.00 = 5.00 ภาษีขาย: 10.00 x 25% = 2.50 รวมภาษีขายที่: 5.00 + 2.50 = 7.50 ยอดเงินรวม: 10.00 + 7.50 = 17.50</span><span class="sxs-lookup"><span data-stu-id="e518f-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="e518f-163">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="e518f-163">Example 3</span></span>

<span data-ttu-id="e518f-164">ภาษีขาย: จุดเริ่มต้น = เปอร์เซ็นต์ของยอดเงินสุทธิคำนวณก่อนภาษีขายจะถูกเลือกสำหรับการคำนวณภาษี</span><span class="sxs-lookup"><span data-stu-id="e518f-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="e518f-165">ยอดเงินสุทธิ: 10.00 ภาษี: 1 x 5.00 = 5.00 ภาษีขาย: (10.00 + 5.00) x 25% = 3.75 รวมภาษีขายที่: 5.00 + 3.75 = 8.75 ยอดเงินรวม: 10.00 + 8.75 = 18.75</span><span class="sxs-lookup"><span data-stu-id="e518f-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="e518f-166">ตัวอย่างที่ 4</span><span class="sxs-lookup"><span data-stu-id="e518f-166">Example 4</span></span>

<span data-ttu-id="e518f-167">ผลลัพธ์ของตัวอย่างที่ 3 และตัวอย่างที่ 1 จะเหมือนกัน เนื่องจากมีภาษีเพียงตัวเดียว</span><span class="sxs-lookup"><span data-stu-id="e518f-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="e518f-168">สมมติว่า คุณมีภาษีสองภาษี และแค่หนึ่งในนั้นจะรวมอยู่ในยอดเงินสุทธิสำหรับการคำนวณภาษีขาย: ภาษี 1:5.00 โดยใช้วิธีคำนวณยอดเงินต่อหน่วย และคำนวณก่อนที่จะเลือกตัวเลือกภาษีขาย ภาษี 2:2.50 โดยใช้วิธีคำนวณยอดเงินต่อหน่วย และคำนวณก่อนที่จะไม่เลือกตัวเลือกภาษีขาย : 25% โดยใช้วิธีคำนวณเปอร์เซ็นต์ของยอดเงินสุทธิ ยอดเงินสุทธิ: 10.00 ภาษี 1:1 x 5.00 = 5.00 ภาษี 2:1 x 2.50 = 2.50 ยอดสุทธิที่ต้องเสียภาษีขาย: 10.00 + 5.00 = 15.00 ภาษีขาย: 15.00 x 25% = 3.75 รวมภาษีขาย รวมถึงภาษี: 5.00 + 2.50 + 3.75 = 11.25 ยอดเงินรวม: 10.00 + 11.25 = 21.25 25% ภาษีขายจะถูกคำนวณสำหรับผลรวมของยอดเงินสุทธิ (10.00) + ภาษี 1 (5.00) = 15.00</span><span class="sxs-lookup"><span data-stu-id="e518f-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="e518f-169">ภาษี 2 ถูกเพิ่มไปยังยอดภาษีหลังจากที่คำนวณภาษีขายแล้ว</span><span class="sxs-lookup"><span data-stu-id="e518f-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="e518f-170"> เปอร์เซ็นต์ของยอดเงินสุทธิที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="e518f-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="e518f-171">เปอร์เซ็นต์ที่ถูกคำนวณของยอดเงินสุทธิจัดการการคำนวณภาษีที่แตกต่างกันโดยขึ้นอยู่กับการตั้งค่าของยอดเงินรวมกับพารามิเตอร์ภาษีขายสำหรับเอกสารหรือสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e518f-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="e518f-172">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="e518f-172">Example 1</span></span>

<span data-ttu-id="e518f-173">การตั้งค่าเอกสาร / สมุดรายวันเป็นยอดเงินรวมกับภาษีขาย = ใช่ ยอดเงินรายการธุรกรรม: 10.00 อัตราภาษี: ภาษีขาย 25%: ยอดเงินในรายการธุรกรรม x อัตราภาษี (10.00 x 25%) = 2.50 ยอดเงินฐานภาษี (ยอดเงินเดิม): ยอดเงินในรายการธุรกรรม - ภาษีขาย (10.00 2.50) = 7.50</span><span class="sxs-lookup"><span data-stu-id="e518f-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="e518f-174">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="e518f-174">Example 2</span></span>

<span data-ttu-id="e518f-175">การตั้งค่าเอกสาร / สมุดรายวันเป็นยอดเงินรวมกับภาษีขาย = ไม่ ยอดเงินรายการธุรกรรม: 10.00 อัตราภาษี: ภาษีขาย 25%: (ยอดเงินในรายการธุรกรรม x อัตราภาษี) / (100 - อัตราภาษี) (10.00 x 25%) / (100% - 25%) = 3.33 ยอดเงินฐานภาษี (ยอดเงินเดิม): ยอดเงินในรายการธุรกรรม = 10.00</span><span class="sxs-lookup"><span data-stu-id="e518f-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="see-also"></a><span data-ttu-id="e518f-176">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="e518f-176">See also</span></span>
--------

[<span data-ttu-id="e518f-177">การกำหนดอัตราภาษีขายตามฐานกำไรเบื้องต้นและฟิลด์วิธีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e518f-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="e518f-178">ยอดเงินทั้งหมดและตัวเลือกการคำนวณช่วงเวลาสำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e518f-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




