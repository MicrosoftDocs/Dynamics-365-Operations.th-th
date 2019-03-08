---
title: การชำระภาษีขายและกฎการปัดเศษ
description: บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "367857"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="04f31-103">การชำระภาษีขายและกฎการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="04f31-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04f31-104">บทความนี้อธิบายวิธีการตั้งค่ากฎการปัดเศษการในการทำงานของหน่วยงานจัดเก็บภาษีขายและการปัดเศษภาษีขายยอดดุลในระหว่างงานและลงรายการบัญชีการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="04f31-105">ภาษีขายจำเป็นต้องมีรายงานและมีการชำระให้กับหน่วยจัดเก็บภาษีเป็นงวดๆ</span><span class="sxs-lookup"><span data-stu-id="04f31-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="04f31-106">การดำเนินการนี้สามารถทำได้โดยการดำเนินการชำระและลงรายการบัญชีกระบวนการภาษีขายในหน้าภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="04f31-107">ภาษีขายสำหรับรอบระยะเวลาจะถูกจับคู่กับบัญชีภาษีขาย และยอดดุลภาษีขายจะถูกลงรายการบัญชีการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="04f31-108">ยอดดุลภาษีขายซึ่งมีการลงรายการญชีการชำระภาษีขาย สามารถถูกปัดเศษตามความจำเป็นโดยหน่วยงานจัดเก็บภาษีด้วยการตั้งค่ากฎการปัดเศษในหน้าภาษีขายได้</span><span class="sxs-lookup"><span data-stu-id="04f31-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="04f31-109">ผลต่างการปัดเศษถูกลงรายการบัญชีไปยังบัญชีการปัดเศษภาษีขาย ที่ถูกเลือกในบัญชีฟิลด์ธุรกรรมอัตโนมัติในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="04f31-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="04f31-110">ในตัวอย่างด้านล่างนี้แสดงให้เห็นถึงวิธีการทำงานของกฎการปัดเศษในหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="04f31-111">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="04f31-111">Example:</span></span>

<span data-ttu-id="04f31-112">ภาษีขายรวมสำหรับรอบระยะเวลาแสดงยอดดุลเครดิตเป็น -98,765.43</span><span class="sxs-lookup"><span data-stu-id="04f31-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="04f31-113">นิติบุคคลรวบรวมภาษีขายได้มากกว่าที่ได้ชำระไป</span><span class="sxs-lookup"><span data-stu-id="04f31-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="04f31-114">ดังนั้น นิติบุคคลค้างชำระเงินหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="04f31-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="04f31-115">นิติบุคคลต้องการใช้วิธีการปัดเศษซึ่งจะปัดเศษยอดดุลลงให้ใกล้เคียงกับ 1.00 มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="04f31-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="04f31-116">พนักงานผู้รับผิดชอบการลงบัญชีภาษีขายต้องดำเนินการขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04f31-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="04f31-117">คลิกภาษี &gt; ภาษีทางอ้อม &gt; ภาษีขาย &gt; หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="04f31-118">บนแท็บด่วนทั่วไป เลือกปกติในฟิลด์แบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="04f31-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="04f31-119">ในฟิลด์ปัดเศษ ให้ป้อน 1.00</span><span class="sxs-lookup"><span data-stu-id="04f31-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="04f31-120">เมื่อถึงเวลาชำระภาษีขายให้แก่หน่วยงานจัดเก็บภาษี ให้เปิดหน้าชำระและลงรายการบัญชีภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="04f31-121">(คลิกภาษี &gt; การรายงาน &gt; ภาษีขาย &gt; ชำระและลงรายการบัญชีภาษีขาย)</span><span class="sxs-lookup"><span data-stu-id="04f31-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="04f31-122">ในบัญชีการชำระภาษีขาย ยอดภาระภาษีจำนวน 98,765.43 ถูกปัดเศษเป็น 98,765</span><span class="sxs-lookup"><span data-stu-id="04f31-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="04f31-123">ตารางต่อไปนี้แสดงวิธีการปัดเศษจำนวน 98,765.43 โดยใช้วิธีการปัดเศษแต่ละวิธีที่พร้อมใช้งานในฟิลด์แบบฟอร์มการปัดเศษในหน้าของหน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="04f31-124">ตัวเลือกแบบฟอร์มการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="04f31-124">Rounding form option</span></span>                | <span data-ttu-id="04f31-125">ค่าปัดเศษ = 0.01</span><span class="sxs-lookup"><span data-stu-id="04f31-125">Round-off value = 0.01</span></span> | <span data-ttu-id="04f31-126">ค่าปัดเศษ = 0.10</span><span class="sxs-lookup"><span data-stu-id="04f31-126">Round-off value = 0.10</span></span> | <span data-ttu-id="04f31-127">ค่าปัดเศษ = 1.00</span><span class="sxs-lookup"><span data-stu-id="04f31-127">Round-off value = 1.00</span></span> | <span data-ttu-id="04f31-128">ค่าปัดเศษ = 100.00</span><span class="sxs-lookup"><span data-stu-id="04f31-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="04f31-129">ปกติ</span><span class="sxs-lookup"><span data-stu-id="04f31-129">Normal</span></span>                              | <span data-ttu-id="04f31-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="04f31-130">98,765.43</span></span>              | <span data-ttu-id="04f31-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="04f31-131">98,765.40</span></span>              | <span data-ttu-id="04f31-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="04f31-132">98,765.00</span></span>              | <span data-ttu-id="04f31-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="04f31-133">98,800.00</span></span>                |
| <span data-ttu-id="04f31-134">ลงข้างล่าง</span><span class="sxs-lookup"><span data-stu-id="04f31-134">Downward</span></span>                            | <span data-ttu-id="04f31-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="04f31-135">98,765.43</span></span>              | <span data-ttu-id="04f31-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="04f31-136">98,765.40</span></span>              | <span data-ttu-id="04f31-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="04f31-137">98,765.00</span></span>              | <span data-ttu-id="04f31-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="04f31-138">98,700.00</span></span>                |
| <span data-ttu-id="04f31-139">การปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="04f31-139">Rounding-up</span></span>                         | <span data-ttu-id="04f31-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="04f31-140">98,765.43</span></span>              | <span data-ttu-id="04f31-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="04f31-141">98,765.50</span></span>              | <span data-ttu-id="04f31-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="04f31-142">98,766.00</span></span>              | <span data-ttu-id="04f31-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="04f31-143">98,800.00</span></span>                |
| <span data-ttu-id="04f31-144">มีข้อได้เปรียบ สำหรับยอดดุลเครดิต</span><span class="sxs-lookup"><span data-stu-id="04f31-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="04f31-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="04f31-145">98,765.43</span></span>              | <span data-ttu-id="04f31-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="04f31-146">98,765.40</span></span>              | <span data-ttu-id="04f31-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="04f31-147">98,765.00</span></span>              | <span data-ttu-id="04f31-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="04f31-148">98,700.00</span></span>                |
| <span data-ttu-id="04f31-149">มีข้อได้เปรียบ สำหรับยอดดุลเดบิต</span><span class="sxs-lookup"><span data-stu-id="04f31-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="04f31-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="04f31-150">98,765.43</span></span>              | <span data-ttu-id="04f31-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="04f31-151">98,765.50</span></span>              | <span data-ttu-id="04f31-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="04f31-152">98,766.00</span></span>              | <span data-ttu-id="04f31-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="04f31-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="04f31-154">ถ้าคุณเลือกมีข้อได้เปรียบ การปัดเศษจะเป็นข้อได้เปรียบของนิติบุคคลเสมอ</span><span class="sxs-lookup"><span data-stu-id="04f31-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="04f31-155">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="04f31-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="04f31-156">ภาพรวมของภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="04f31-157">การสร้างการชำระเงินภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="04f31-158">สร้างเอกสารเกี่ยวกับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="04f31-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="04f31-159">ดูธุรกรรมภาษีขายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="04f31-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)


