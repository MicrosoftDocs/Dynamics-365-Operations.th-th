---
title: "การชำระภาษีขายและกฎการปัดเศษ"
description: "บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย"
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="207bd-103">การชำระภาษีขายและกฎการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="207bd-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="207bd-104">บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="207bd-105">ภาษีขายจำเป็นต้องมีรายงานและมีการชำระให้กับหน่วยจัดเก็บภาษีเป็นงวดๆ</span><span class="sxs-lookup"><span data-stu-id="207bd-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="207bd-106">การดำเนินการนี้สามารถทำได้โดยการดำเนินการชำระและลงรายการบัญชีกระบวนการภาษีขายในหน้าภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="207bd-107">ภาษีขายสำหรับรอบระยะเวลาจะถูกจับคู่กับบัญชีภาษีขาย และยอดดุลภาษีขายจะถูกลงรายการบัญชีการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="207bd-108">ยอดดุลภาษีขายซึ่งมีการลงรายการญชีการชำระภาษีขาย สามารถถูกปัดเศษตามความจำเป็นโดยหน่วยงานจัดเก็บภาษีด้วยการตั้งค่ากฎการปัดเศษในหน้าภาษีขายได้</span><span class="sxs-lookup"><span data-stu-id="207bd-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="207bd-109">ผลต่างการปัดเศษถูกลงรายการบัญชีไปยังบัญชีการปัดเศษภาษีขาย ที่ถูกเลือกในบัญชีฟิลด์ธุรกรรมอัตโนมัติในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="207bd-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="207bd-110">ในตัวอย่างด้านล่างนี้แสดงให้เห็นถึงวิธีการทำงานของกฎการปัดเศษในหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="207bd-111">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="207bd-111">Example:</span></span>

<span data-ttu-id="207bd-112">ภาษีขายรวมสำหรับรอบระยะเวลาแสดงยอดดุลเครดิตเป็น -98,765.43</span><span class="sxs-lookup"><span data-stu-id="207bd-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="207bd-113">นิติบุคคลรวบรวมภาษีขายได้มากกว่าที่ได้ชำระไป</span><span class="sxs-lookup"><span data-stu-id="207bd-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="207bd-114">ดังนั้น นิติบุคคลค้างชำระเงินหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="207bd-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="207bd-115">นิติบุคคลต้องการใช้วิธีการปัดเศษซึ่งจะปัดเศษยอดดุลลงให้ใกล้เคียงกับ 1.00 มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="207bd-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="207bd-116">พนักงานผู้รับผิดชอบการลงบัญชีภาษีขายต้องดำเนินการขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="207bd-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="207bd-117">คลิกภาษี &gt; ภาษีทางอ้อม &gt; ภาษีขาย &gt; หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="207bd-118">บนแท็บด่วนทั่วไป เลือกปกติในฟิลด์แบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="207bd-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="207bd-119">ในฟิลด์ปัดเศษ ให้ป้อน 1.00</span><span class="sxs-lookup"><span data-stu-id="207bd-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="207bd-120">เมื่อถึงเวลาชำระภาษีขายให้แก่หน่วยงานจัดเก็บภาษี ให้เปิดหน้าชำระและลงรายการบัญชีภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="207bd-121">(คลิกภาษี &gt; การรายงาน &gt; ภาษีขาย &gt; ชำระและลงรายการบัญชีภาษีขาย)</span><span class="sxs-lookup"><span data-stu-id="207bd-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="207bd-122">ในบัญชีการชำระภาษีขาย ยอดภาระภาษีจำนวน 98,765.43 ถูกปัดเศษเป็น 98,765</span><span class="sxs-lookup"><span data-stu-id="207bd-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="207bd-123">ตารางต่อไปนี้แสดงวิธีการปัดเศษจำนวน 98,765.43 โดยใช้วิธีการปัดเศษแต่ละวิธีที่พร้อมใช้งานในฟิลด์แบบฟอร์มการปัดเศษในหน้าของหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="207bd-124">ตัวเลือกแบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="207bd-124">Rounding form option</span></span>                | <span data-ttu-id="207bd-125">ค่าปัดเศษ = 0.01</span><span class="sxs-lookup"><span data-stu-id="207bd-125">Round-off value = 0.01</span></span> | <span data-ttu-id="207bd-126">ค่าปัดเศษ = 0.10</span><span class="sxs-lookup"><span data-stu-id="207bd-126">Round-off value = 0.10</span></span> | <span data-ttu-id="207bd-127">ค่าปัดเศษ = 1.00</span><span class="sxs-lookup"><span data-stu-id="207bd-127">Round-off value = 1.00</span></span> | <span data-ttu-id="207bd-128">ค่าปัดเศษ = 100.00</span><span class="sxs-lookup"><span data-stu-id="207bd-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="207bd-129">ปกติ</span><span class="sxs-lookup"><span data-stu-id="207bd-129">Normal</span></span>                              | <span data-ttu-id="207bd-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="207bd-130">98,765.43</span></span>              | <span data-ttu-id="207bd-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="207bd-131">98,765.40</span></span>              | <span data-ttu-id="207bd-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="207bd-132">98,765.00</span></span>              | <span data-ttu-id="207bd-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="207bd-133">98,800.00</span></span>                |
| <span data-ttu-id="207bd-134">ลงข้างล่าง</span><span class="sxs-lookup"><span data-stu-id="207bd-134">Downward</span></span>                            | <span data-ttu-id="207bd-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="207bd-135">98,765.43</span></span>              | <span data-ttu-id="207bd-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="207bd-136">98,765.40</span></span>              | <span data-ttu-id="207bd-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="207bd-137">98,765.00</span></span>              | <span data-ttu-id="207bd-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="207bd-138">98,700.00</span></span>                |
| <span data-ttu-id="207bd-139">การปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="207bd-139">Rounding-up</span></span>                         | <span data-ttu-id="207bd-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="207bd-140">98,765.43</span></span>              | <span data-ttu-id="207bd-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="207bd-141">98,765.50</span></span>              | <span data-ttu-id="207bd-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="207bd-142">98,766.00</span></span>              | <span data-ttu-id="207bd-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="207bd-143">98,800.00</span></span>                |
| <span data-ttu-id="207bd-144">มีข้อได้เปรียบ สำหรับยอดดุลเครดิต</span><span class="sxs-lookup"><span data-stu-id="207bd-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="207bd-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="207bd-145">98,765.43</span></span>              | <span data-ttu-id="207bd-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="207bd-146">98,765.40</span></span>              | <span data-ttu-id="207bd-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="207bd-147">98,765.00</span></span>              | <span data-ttu-id="207bd-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="207bd-148">98,700.00</span></span>                |
| <span data-ttu-id="207bd-149">มีข้อได้เปรียบ สำหรับยอดดุลเดบิต</span><span class="sxs-lookup"><span data-stu-id="207bd-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="207bd-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="207bd-150">98,765.43</span></span>              | <span data-ttu-id="207bd-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="207bd-151">98,765.50</span></span>              | <span data-ttu-id="207bd-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="207bd-152">98,766.00</span></span>              | <span data-ttu-id="207bd-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="207bd-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="207bd-154">ถ้าคุณเลือกมีข้อได้เปรียบ การปัดเศษจะเป็นข้อได้เปรียบของนิติบุคคลเสมอ</span><span class="sxs-lookup"><span data-stu-id="207bd-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="207bd-155">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="207bd-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="207bd-156">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="207bd-157">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="207bd-158">สร้างเอกสารเกี่ยวกับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="207bd-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="207bd-159">ดูธุรกรรมภาษีขายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="207bd-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



