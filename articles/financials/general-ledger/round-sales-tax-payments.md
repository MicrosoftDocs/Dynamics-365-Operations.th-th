---
title: "การชำระภาษีขายและกฎการปัดเศษ"
description: "บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย"
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="14839-103">การชำระภาษีขายและกฎการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="14839-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="14839-104">บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="14839-105">ภาษีขายจำเป็นต้องมีรายงานและมีการชำระให้กับหน่วยจัดเก็บภาษีเป็นงวดๆ</span><span class="sxs-lookup"><span data-stu-id="14839-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="14839-106">การดำเนินการนี้สามารถทำได้โดยการดำเนินการชำระและลงรายการบัญชีกระบวนการภาษีขายในหน้าภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="14839-107">ภาษีขายสำหรับรอบระยะเวลาจะถูกจับคู่กับบัญชีภาษีขาย และยอดดุลภาษีขายจะถูกลงรายการบัญชีการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="14839-108">ยอดดุลภาษีขายซึ่งมีการลงรายการญชีการชำระภาษีขาย สามารถถูกปัดเศษตามความจำเป็นโดยหน่วยงานจัดเก็บภาษีด้วยการตั้งค่ากฎการปัดเศษในหน้าภาษีขายได้</span><span class="sxs-lookup"><span data-stu-id="14839-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="14839-109">ผลต่างการปัดเศษถูกลงรายการบัญชีไปยังบัญชีการปัดเศษภาษีขาย ที่ถูกเลือกในบัญชีฟิลด์ธุรกรรมอัตโนมัติในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="14839-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="14839-110">ในตัวอย่างด้านล่างนี้แสดงให้เห็นถึงวิธีการทำงานของกฎการปัดเศษในหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="14839-111">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="14839-111">Example:</span></span>

<span data-ttu-id="14839-112">ภาษีขายรวมสำหรับรอบระยะเวลาแสดงยอดดุลเครดิตเป็น -98,765.43</span><span class="sxs-lookup"><span data-stu-id="14839-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="14839-113">นิติบุคคลรวบรวมภาษีขายได้มากกว่าที่ได้ชำระไป</span><span class="sxs-lookup"><span data-stu-id="14839-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="14839-114">ดังนั้น นิติบุคคลค้างชำระเงินหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="14839-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="14839-115">นิติบุคคลต้องการใช้วิธีการปัดเศษซึ่งจะปัดเศษยอดดุลลงให้ใกล้เคียงกับ 1.00 มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="14839-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="14839-116">พนักงานผู้รับผิดชอบการลงบัญชีภาษีขายต้องดำเนินการขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14839-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="14839-117">คลิกภาษี &gt; ภาษีทางอ้อม &gt; ภาษีขาย &gt; หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="14839-118">บนแท็บด่วนทั่วไป เลือกปกติในฟิลด์แบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="14839-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="14839-119">ในฟิลด์ปัดเศษ ให้ป้อน 1.00</span><span class="sxs-lookup"><span data-stu-id="14839-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="14839-120">เมื่อถึงเวลาชำระภาษีขายให้แก่หน่วยงานจัดเก็บภาษี ให้เปิดหน้าชำระและลงรายการบัญชีภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="14839-121">(คลิกภาษี &gt; การรายงาน &gt; ภาษีขาย &gt; ชำระและลงรายการบัญชีภาษีขาย)</span><span class="sxs-lookup"><span data-stu-id="14839-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="14839-122">ในบัญชีการชำระภาษีขาย ยอดภาระภาษีจำนวน 98,765.43 ถูกปัดเศษเป็น 98,765</span><span class="sxs-lookup"><span data-stu-id="14839-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="14839-123">ตารางต่อไปนี้แสดงวิธีการปัดเศษจำนวน 98,765.43 โดยใช้วิธีการปัดเศษแต่ละวิธีที่พร้อมใช้งานในฟิลด์แบบฟอร์มการปัดเศษในหน้าของหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="14839-124">ตัวเลือกแบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="14839-124">Rounding form option</span></span>                | <span data-ttu-id="14839-125">ค่าปัดเศษ = 0.01</span><span class="sxs-lookup"><span data-stu-id="14839-125">Round-off value = 0.01</span></span> | <span data-ttu-id="14839-126">ค่าปัดเศษ = 0.10</span><span class="sxs-lookup"><span data-stu-id="14839-126">Round-off value = 0.10</span></span> | <span data-ttu-id="14839-127">ค่าปัดเศษ = 1.00</span><span class="sxs-lookup"><span data-stu-id="14839-127">Round-off value = 1.00</span></span> | <span data-ttu-id="14839-128">ค่าปัดเศษ = 100.00</span><span class="sxs-lookup"><span data-stu-id="14839-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="14839-129">ปกติ</span><span class="sxs-lookup"><span data-stu-id="14839-129">Normal</span></span>                              | <span data-ttu-id="14839-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="14839-130">98,765.43</span></span>              | <span data-ttu-id="14839-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="14839-131">98,765.40</span></span>              | <span data-ttu-id="14839-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="14839-132">98,765.00</span></span>              | <span data-ttu-id="14839-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="14839-133">98,800.00</span></span>                |
| <span data-ttu-id="14839-134">ลงข้างล่าง</span><span class="sxs-lookup"><span data-stu-id="14839-134">Downward</span></span>                            | <span data-ttu-id="14839-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="14839-135">98,765.43</span></span>              | <span data-ttu-id="14839-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="14839-136">98,765.40</span></span>              | <span data-ttu-id="14839-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="14839-137">98,765.00</span></span>              | <span data-ttu-id="14839-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="14839-138">98,700.00</span></span>                |
| <span data-ttu-id="14839-139">การปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="14839-139">Rounding-up</span></span>                         | <span data-ttu-id="14839-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="14839-140">98,765.43</span></span>              | <span data-ttu-id="14839-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="14839-141">98,765.50</span></span>              | <span data-ttu-id="14839-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="14839-142">98,766.00</span></span>              | <span data-ttu-id="14839-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="14839-143">98,800.00</span></span>                |
| <span data-ttu-id="14839-144">มีข้อได้เปรียบ สำหรับยอดดุลเครดิต</span><span class="sxs-lookup"><span data-stu-id="14839-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="14839-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="14839-145">98,765.43</span></span>              | <span data-ttu-id="14839-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="14839-146">98,765.40</span></span>              | <span data-ttu-id="14839-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="14839-147">98,765.00</span></span>              | <span data-ttu-id="14839-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="14839-148">98,700.00</span></span>                |
| <span data-ttu-id="14839-149">มีข้อได้เปรียบ สำหรับยอดดุลเดบิต</span><span class="sxs-lookup"><span data-stu-id="14839-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="14839-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="14839-150">98,765.43</span></span>              | <span data-ttu-id="14839-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="14839-151">98,765.50</span></span>              | <span data-ttu-id="14839-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="14839-152">98,766.00</span></span>              | <span data-ttu-id="14839-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="14839-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="14839-154">ถ้าคุณเลือกมีข้อได้เปรียบ การปัดเศษจะเป็นข้อได้เปรียบของนิติบุคคลเสมอ</span><span class="sxs-lookup"><span data-stu-id="14839-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="14839-155">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="14839-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="14839-156">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="14839-157">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="14839-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="14839-158">สร้างเอกสารเกี่ยวกับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="14839-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="14839-159">ดูธุรกรรมภาษีขายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="14839-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



