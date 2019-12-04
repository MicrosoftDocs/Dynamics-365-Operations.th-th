---
title: การชำระภาษีขายและกฎการปัดเศษ
description: บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e66a62007025964b3d58ff0620ebecd6d9769f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771763"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="9da87-103">การชำระภาษีขายและกฎการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="9da87-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9da87-104">บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="9da87-105">ภาษีขายจำเป็นต้องมีรายงานและมีการชำระให้กับหน่วยจัดเก็บภาษีเป็นงวดๆ</span><span class="sxs-lookup"><span data-stu-id="9da87-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="9da87-106">การดำเนินการนี้สามารถทำได้โดยการดำเนินการชำระและลงรายการบัญชีกระบวนการภาษีขายในหน้าภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="9da87-107">ภาษีขายสำหรับรอบระยะเวลาจะถูกจับคู่กับบัญชีภาษีขาย และยอดดุลภาษีขายจะถูกลงรายการบัญชีการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="9da87-108">ยอดดุลภาษีขายซึ่งมีการลงรายการญชีการชำระภาษีขาย สามารถถูกปัดเศษตามความจำเป็นโดยหน่วยงานจัดเก็บภาษีด้วยการตั้งค่ากฎการปัดเศษในหน้าภาษีขายได้</span><span class="sxs-lookup"><span data-stu-id="9da87-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="9da87-109">ผลต่างการปัดเศษถูกลงรายการบัญชีไปยังบัญชีการปัดเศษภาษีขาย ที่ถูกเลือกในบัญชีฟิลด์ธุรกรรมอัตโนมัติในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9da87-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="9da87-110">ในตัวอย่างด้านล่างนี้แสดงให้เห็นถึงวิธีการทำงานของกฎการปัดเศษในหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="9da87-111">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="9da87-111">Examples</span></span>

<span data-ttu-id="9da87-112">ภาษีขายรวมสำหรับรอบระยะเวลาแสดงยอดดุลเครดิตเป็น -98,765.43</span><span class="sxs-lookup"><span data-stu-id="9da87-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="9da87-113">นิติบุคคลรวบรวมภาษีขายได้มากกว่าที่ได้ชำระไป</span><span class="sxs-lookup"><span data-stu-id="9da87-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="9da87-114">ดังนั้น นิติบุคคลค้างชำระเงินหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="9da87-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="9da87-115">นิติบุคคลต้องการใช้วิธีการปัดเศษซึ่งจะปัดเศษยอดดุลลงให้ใกล้เคียงกับ 1.00 มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="9da87-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="9da87-116">พนักงานผู้รับผิดชอบการลงบัญชีภาษีขายต้องดำเนินการขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9da87-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="9da87-117">คลิกภาษี &gt; ภาษีทางอ้อม &gt; ภาษีขาย &gt; หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="9da87-118">บนแท็บด่วนทั่วไป เลือกปกติในฟิลด์แบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="9da87-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="9da87-119">ในฟิลด์ปัดเศษ ให้ป้อน 1.00</span><span class="sxs-lookup"><span data-stu-id="9da87-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="9da87-120">เมื่อถึงเวลาชำระภาษีขายให้แก่หน่วยงานจัดเก็บภาษี ให้เปิดหน้าชำระและลงรายการบัญชีภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="9da87-121">(คลิกภาษี &gt; การรายงาน &gt; ภาษีขาย &gt; ชำระและลงรายการบัญชีภาษีขาย)</span><span class="sxs-lookup"><span data-stu-id="9da87-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="9da87-122">ในบัญชีการชำระภาษีขาย ยอดภาระภาษีจำนวน 98,765.43 ถูกปัดเศษเป็น 98,765</span><span class="sxs-lookup"><span data-stu-id="9da87-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="9da87-123">ตารางต่อไปนี้แสดงวิธีการปัดเศษจำนวน 98,765.43 โดยใช้วิธีการปัดเศษแต่ละวิธีที่พร้อมใช้งานในฟิลด์แบบฟอร์มการปัดเศษในหน้าของหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="9da87-124">ตัวเลือกแบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="9da87-124">Rounding form option</span></span>                | <span data-ttu-id="9da87-125">ค่าปัดเศษ = 0.01</span><span class="sxs-lookup"><span data-stu-id="9da87-125">Round-off value = 0.01</span></span> | <span data-ttu-id="9da87-126">ค่าปัดเศษ = 0.10</span><span class="sxs-lookup"><span data-stu-id="9da87-126">Round-off value = 0.10</span></span> | <span data-ttu-id="9da87-127">ค่าปัดเศษ = 1.00</span><span class="sxs-lookup"><span data-stu-id="9da87-127">Round-off value = 1.00</span></span> | <span data-ttu-id="9da87-128">ค่าปัดเศษ = 100.00</span><span class="sxs-lookup"><span data-stu-id="9da87-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="9da87-129">ปกติ</span><span class="sxs-lookup"><span data-stu-id="9da87-129">Normal</span></span>                              | <span data-ttu-id="9da87-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="9da87-130">98,765.43</span></span>              | <span data-ttu-id="9da87-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="9da87-131">98,765.40</span></span>              | <span data-ttu-id="9da87-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="9da87-132">98,765.00</span></span>              | <span data-ttu-id="9da87-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="9da87-133">98,800.00</span></span>                |
| <span data-ttu-id="9da87-134">ลงข้างล่าง</span><span class="sxs-lookup"><span data-stu-id="9da87-134">Downward</span></span>                            | <span data-ttu-id="9da87-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="9da87-135">98,765.43</span></span>              | <span data-ttu-id="9da87-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="9da87-136">98,765.40</span></span>              | <span data-ttu-id="9da87-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="9da87-137">98,765.00</span></span>              | <span data-ttu-id="9da87-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="9da87-138">98,700.00</span></span>                |
| <span data-ttu-id="9da87-139">การปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="9da87-139">Rounding-up</span></span>                         | <span data-ttu-id="9da87-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="9da87-140">98,765.43</span></span>              | <span data-ttu-id="9da87-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="9da87-141">98,765.50</span></span>              | <span data-ttu-id="9da87-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="9da87-142">98,766.00</span></span>              | <span data-ttu-id="9da87-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="9da87-143">98,800.00</span></span>                |
| <span data-ttu-id="9da87-144">มีข้อได้เปรียบ สำหรับยอดดุลเครดิต</span><span class="sxs-lookup"><span data-stu-id="9da87-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="9da87-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="9da87-145">98,765.43</span></span>              | <span data-ttu-id="9da87-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="9da87-146">98,765.40</span></span>              | <span data-ttu-id="9da87-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="9da87-147">98,765.00</span></span>              | <span data-ttu-id="9da87-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="9da87-148">98,700.00</span></span>                |
| <span data-ttu-id="9da87-149">มีข้อได้เปรียบ สำหรับยอดดุลเดบิต</span><span class="sxs-lookup"><span data-stu-id="9da87-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="9da87-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="9da87-150">98,765.43</span></span>              | <span data-ttu-id="9da87-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="9da87-151">98,765.50</span></span>              | <span data-ttu-id="9da87-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="9da87-152">98,766.00</span></span>              | <span data-ttu-id="9da87-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="9da87-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="9da87-154">ไม่มีการปัดเศษเลย เนื่องจากการปัดเศษเป็น 0.00</span><span class="sxs-lookup"><span data-stu-id="9da87-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="9da87-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="9da87-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="9da87-156">การปัดเศษปกติ และความแม่นยำในการปัดเศษเป็น 0.01</span><span class="sxs-lookup"><span data-stu-id="9da87-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="9da87-157">การปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="9da87-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="9da87-158">กระบวนการในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="9da87-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="9da87-159">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="9da87-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="9da87-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="9da87-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="9da87-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="9da87-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="9da87-162">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="9da87-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="9da87-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="9da87-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="9da87-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="9da87-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="9da87-165">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="9da87-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="9da87-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="9da87-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="9da87-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="9da87-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="9da87-168">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="9da87-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="9da87-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="9da87-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="9da87-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="9da87-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="9da87-171">ถ้าคุณเลือกมีข้อได้เปรียบ การปัดเศษจะเป็นข้อได้เปรียบของนิติบุคคลเสมอ</span><span class="sxs-lookup"><span data-stu-id="9da87-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="9da87-172">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9da87-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="9da87-173">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="9da87-174">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="9da87-175">สร้างเอกสารเกี่ยวกับธุรกรรมภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9da87-175">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="9da87-176">ดูธุรกรรมภาษีขายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="9da87-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="9da87-177">ฟังก์ชันการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="9da87-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


