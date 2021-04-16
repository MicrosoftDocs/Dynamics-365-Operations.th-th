---
title: การชำระภาษีขายและกฎการปัดเศษ
description: บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edbe92d009c77702a21d32afb5aebe93bc5e2ee0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815391"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="37040-103">การชำระภาษีขายและกฎการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="37040-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37040-104">บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="37040-105">ภาษีขายจำเป็นต้องมีรายงานและมีการชำระให้กับหน่วยจัดเก็บภาษีเป็นงวดๆ</span><span class="sxs-lookup"><span data-stu-id="37040-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="37040-106">การดำเนินการนี้สามารถทำได้โดยการดำเนินการชำระและลงรายการบัญชีกระบวนการภาษีขายในหน้าภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="37040-107">ภาษีขายสำหรับรอบระยะเวลาจะถูกจับคู่กับบัญชีภาษีขาย และยอดดุลภาษีขายจะถูกลงรายการบัญชีการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="37040-108">ยอดดุลภาษีขายซึ่งมีการลงรายการญชีการชำระภาษีขาย สามารถถูกปัดเศษตามความจำเป็นโดยหน่วยงานจัดเก็บภาษีด้วยการตั้งค่ากฎการปัดเศษในหน้าภาษีขายได้</span><span class="sxs-lookup"><span data-stu-id="37040-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="37040-109">ผลต่างการปัดเศษถูกลงรายการบัญชีไปยังบัญชีการปัดเศษภาษีขาย ที่ถูกเลือกในบัญชีฟิลด์ธุรกรรมอัตโนมัติในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="37040-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="37040-110">ในตัวอย่างด้านล่างนี้แสดงให้เห็นถึงวิธีการทำงานของกฎการปัดเศษในหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="37040-111">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="37040-111">Examples</span></span>

<span data-ttu-id="37040-112">ภาษีขายรวมสำหรับรอบระยะเวลาแสดงยอดดุลเครดิตเป็น -98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="37040-113">นิติบุคคลรวบรวมภาษีขายได้มากกว่าที่ได้ชำระไป</span><span class="sxs-lookup"><span data-stu-id="37040-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="37040-114">ดังนั้น นิติบุคคลค้างชำระเงินหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="37040-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="37040-115">นิติบุคคลต้องการใช้วิธีการปัดเศษซึ่งจะปัดเศษยอดดุลลงให้ใกล้เคียงกับ 1.00 มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="37040-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="37040-116">พนักงานผู้รับผิดชอบการลงบัญชีภาษีขายต้องดำเนินการขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="37040-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="37040-117">คลิก **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **หน่วยงานจัดเก็บภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="37040-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="37040-118">บน FastTab **ทั่วไป** เลือกฟิลด์ **ฟอร์มการปัดเศษ** เลือก **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="37040-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="37040-119">ในฟิลด์ **ปัดเศษ** ให้ป้อน 1.00</span><span class="sxs-lookup"><span data-stu-id="37040-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="37040-120">เมื่อถึงเวลาชำระภาษีขายให้แก่หน่วยงานจัดเก็บภาษี ไปที่ **ภาษี** > **ประกาศต่างๆ** > **ภาษีขาย** > **ชำระและลงรายการบัญชีภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="37040-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="37040-121">ในบัญชีการชำระภาษีขาย คุณสามารถดูว่ายอดภาระภาษีจำนวน **98,765.43** ถูกปัดเศษเป็น **98,765**</span><span class="sxs-lookup"><span data-stu-id="37040-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="37040-122">ตารางต่อไปนี้แสดงวิธีการปัดเศษจำนวน 98,765.43 โดยใช้วิธีการปัดเศษแต่ละวิธีที่พร้อมใช้งานในฟิลด์ **ฟอร์มการปัดเศษ** ในหน้าของ **หน่วยงานจัดเก็บภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="37040-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="37040-123">ถ้ามีการตั้งค่าการปัดเศษเป็น 0.00 จากนั้น:</span><span class="sxs-lookup"><span data-stu-id="37040-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="37040-124">สำหรับการปัดเศษปกติ ลักษณะการปัดเศษจะเหมือนกันสำหรับ **การปัดเศษ = 0.01**</span><span class="sxs-lookup"><span data-stu-id="37040-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="37040-125">สำหรับ **ตัวเลือกฟอร์มการปัดเศษ** **ลงข้างล่าง** **การปัดเศษขึ้น** และ **ผลประโยชน์ของตนเอง** ลักษณะการทำงานจะเหมือนกันสำหรับ **การปัดเศษ = 1.00**</span><span class="sxs-lookup"><span data-stu-id="37040-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="37040-126">ตัวเลือกแบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="37040-126">Rounding form option</span></span>                | <span data-ttu-id="37040-127">ค่าปัดเศษ = 0.01</span><span class="sxs-lookup"><span data-stu-id="37040-127">Round-off value = 0.01</span></span> | <span data-ttu-id="37040-128">ค่าปัดเศษ = 0.10</span><span class="sxs-lookup"><span data-stu-id="37040-128">Round-off value = 0.10</span></span> | <span data-ttu-id="37040-129">ค่าปัดเศษ = 1.00</span><span class="sxs-lookup"><span data-stu-id="37040-129">Round-off value = 1.00</span></span> | <span data-ttu-id="37040-130">ค่าปัดเศษ = 100.00</span><span class="sxs-lookup"><span data-stu-id="37040-130">Round-off value = 100.00</span></span> | <span data-ttu-id="37040-131">ค่าปัดเศษ = 0.00</span><span class="sxs-lookup"><span data-stu-id="37040-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="37040-132">ปกติ</span><span class="sxs-lookup"><span data-stu-id="37040-132">Normal</span></span>                              | <span data-ttu-id="37040-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-133">98,765.43</span></span>              | <span data-ttu-id="37040-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="37040-134">98,765.40</span></span>              | <span data-ttu-id="37040-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="37040-135">98,765.00</span></span>              | <span data-ttu-id="37040-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="37040-136">98,800.00</span></span>                | <span data-ttu-id="37040-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-137">98,765.43</span></span>                |
| <span data-ttu-id="37040-138">ลงข้างล่าง</span><span class="sxs-lookup"><span data-stu-id="37040-138">Downward</span></span>                            | <span data-ttu-id="37040-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-139">98,765.43</span></span>              | <span data-ttu-id="37040-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="37040-140">98,765.40</span></span>              | <span data-ttu-id="37040-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="37040-141">98,765.00</span></span>              | <span data-ttu-id="37040-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="37040-142">98,700.00</span></span>                | <span data-ttu-id="37040-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="37040-143">98,765.00</span></span>                |
| <span data-ttu-id="37040-144">การปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="37040-144">Rounding-up</span></span>                         | <span data-ttu-id="37040-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-145">98,765.43</span></span>              | <span data-ttu-id="37040-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="37040-146">98,765.50</span></span>              | <span data-ttu-id="37040-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="37040-147">98,766.00</span></span>              | <span data-ttu-id="37040-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="37040-148">98,800.00</span></span>                | <span data-ttu-id="37040-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="37040-149">98,766.00</span></span>                |
| <span data-ttu-id="37040-150">มีข้อได้เปรียบ สำหรับยอดดุลเครดิต</span><span class="sxs-lookup"><span data-stu-id="37040-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="37040-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-151">98,765.43</span></span>              | <span data-ttu-id="37040-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="37040-152">98,765.40</span></span>              | <span data-ttu-id="37040-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="37040-153">98,765.00</span></span>              | <span data-ttu-id="37040-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="37040-154">98,700.00</span></span>                | <span data-ttu-id="37040-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="37040-155">98,765.00</span></span>                |
| <span data-ttu-id="37040-156">มีข้อได้เปรียบ สำหรับยอดดุลเดบิต</span><span class="sxs-lookup"><span data-stu-id="37040-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="37040-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="37040-157">98,765.43</span></span>              | <span data-ttu-id="37040-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="37040-158">98,765.50</span></span>              | <span data-ttu-id="37040-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="37040-159">98,766.00</span></span>              | <span data-ttu-id="37040-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="37040-160">98,800.00</span></span>                | <span data-ttu-id="37040-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="37040-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="37040-162">การปัดเศษปกติ และความแม่นยำในการปัดเศษเป็น 0.01</span><span class="sxs-lookup"><span data-stu-id="37040-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="37040-163">การปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="37040-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="37040-164">กระบวนการในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="37040-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="37040-165">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="37040-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="37040-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="37040-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="37040-167">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="37040-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="37040-168">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="37040-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="37040-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="37040-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="37040-170">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="37040-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="37040-171">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="37040-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="37040-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="37040-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="37040-173">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="37040-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="37040-174">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="37040-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="37040-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="37040-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="37040-176">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="37040-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="37040-177">ถ้าคุณเลือกมีข้อได้เปรียบ การปัดเศษจะเป็นข้อได้เปรียบของนิติบุคคลเสมอ</span><span class="sxs-lookup"><span data-stu-id="37040-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="37040-178">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="37040-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="37040-179">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="37040-180">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="37040-181">สร้างเอกสารเกี่ยวกับธุรกรรมภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="37040-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="37040-182">ดูธุรกรรมภาษีขายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="37040-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="37040-183">ฟังก์ชันการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="37040-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]