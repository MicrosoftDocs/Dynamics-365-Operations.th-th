---
title: "การกระจายการลงบัญชีและรายการสมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ข้อความอิสระ"
description: "การกระจายการลงบัญชีถูกใช้เพื่อกำหนดวิธีลงบัญชีของยอดเงิน เช่น วิธีการลงบัญชีค่าใช้จ่าย ภาษี หรือค่าธรรมเนียม ในใบแจ้งหนี้ข้อความอิสระ  ทุกๆ ยอดเงินที่ต้องนำมาลงบัญชีเมื่อใบแจ้งหนี้ข้อความอิสระถูกบันทึกบัญชีในสมุดรายวัน จะมีการกระจายการลงบัญชีหนึ่งรายการหรือมากกว่า"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5d1546e8537110daec5d6655f68d3328a58ca1cb
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="4d318-104">การกระจายการลงบัญชีและรายการสมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d318-105">การกระจายการลงบัญชีถูกใช้เพื่อกำหนดวิธีลงบัญชีของยอดเงิน เช่น วิธีการลงบัญชีค่าใช้จ่าย ภาษี หรือค่าธรรมเนียม ในใบแจ้งหนี้ข้อความอิสระ </span><span class="sxs-lookup"><span data-stu-id="4d318-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="4d318-106">ทุกๆ ยอดเงินที่ต้องนำมาลงบัญชีเมื่อใบแจ้งหนี้ข้อความอิสระถูกบันทึกบัญชีในสมุดรายวัน จะมีการกระจายการลงบัญชีหนึ่งรายการหรือมากกว่า</span><span class="sxs-lookup"><span data-stu-id="4d318-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="4d318-107">การกระจายการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d318-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="4d318-108">คุณสามารถใช้ปุ่มต่างๆต่อไปนี้ในหน้าใบแจ้งหนี้ข้อความอิสระเพื่อดู และอาจเปลี่ยนแปลง การกระจายการลงบัญชีสำหรับแต่ละยอดเงินในใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="4d318-109">**กระจายยอดเงิน**—ดูและเปลี่ยนแปลงการกระจายการลงบัญชีสำหรับแต่ละรายการและรายการข้อมูลรองใดๆ เช่น ภาษีหรือค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="4d318-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="4d318-110">นอกจากนี้คุณยังสามารถดูและเปลี่ยนแปลงการกระจายการลงบัญชีสำหรับรายการรองโดยตรงจากหน้าธุรกรรมภาษีขายหรือหน้าธุรกรรมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="4d318-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="4d318-111">เปลี่ยนแปลงยอดในส่วนหัวใบแจ้งหนี้ข้อความอิสระ เช่นค่าธรรมเนียมหรือยอดเงินการปัดเศษสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="4d318-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="4d318-112">เปลี่ยนแปลงยอดรายการของใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="4d318-113">**ดูการกระจาย**ดูการกระจายการลงบัญชีสำหรับรายการเอกสารทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4d318-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="4d318-114">คุณไม่สามารถที่จะเปลี่ยนแปลงการกระจายการลงบัญชีจากมุมมองนี้</span><span class="sxs-lookup"><span data-stu-id="4d318-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="4d318-115">ดูยอดส่วนหัวและยอดรายการ</span><span class="sxs-lookup"><span data-stu-id="4d318-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="4d318-116">ยอดการกระจาย</span><span class="sxs-lookup"><span data-stu-id="4d318-116">Distributing amounts</span></span>
<span data-ttu-id="4d318-117">เมื่อคุณป้อนใบแจ้งหนี้ข้อความอิสระ แต่ละยอดจะมีกระจายดังนี้</span><span class="sxs-lookup"><span data-stu-id="4d318-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d318-118">ชนิดของยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="4d318-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="4d318-119">บัญชีหลักถูกแสดงมาจากที่ใด</span><span class="sxs-lookup"><span data-stu-id="4d318-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="4d318-120">ลำดับความสำคัญที่กำหนดมิติทางการเงินเริ่มต้นที่จะแสดง</span><span class="sxs-lookup"><span data-stu-id="4d318-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d318-121">รายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="4d318-122">บัญชีแยกประเภทในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="4d318-123">ถ้าบัญชีหลักเป็นบัญชีการปันส่วน ใช้ค่าเริ่มต้นจากข้อกำหนดบัญชีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="4d318-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4d318-124">ถ้าบัญชีหลักไม่ใช่บัญชีการปันส่วน ให้ใช้เท็มเพลตเริ่มต้นของมิติทางการเงินในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-125">ใช้ค่ามิติทางการเงินเริ่มต้นในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-126">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีแยกประเภทในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d318-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d318-127">รายการใบแจ้งหนี้ข้อความอิสระสำหรับหมายเลขสินทรัพย์ถาวรและรูปแบบมูลค่า</span><span class="sxs-lookup"><span data-stu-id="4d318-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4d318-128"><strong>หมายเหตุ</strong></span><span class="sxs-lookup"><span data-stu-id="4d318-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d318-129">บัญชีหลักในรายการใบแจ้งหนี้ข้อความอิสระจะเป็นบัญชีการตัดจำหน่ายสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="4d318-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="4d318-130">บัญชีแยกประเภทในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="4d318-131">ใช้ค่ามิติทางการเงินเริ่มต้นในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-132">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีแยกประเภทในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d318-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d318-133">ยอดส่วนลดในใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="4d318-134">บัญชีหลักสำหรับฟิลด์ส่วนลดของลูกค้าในหน้าส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="4d318-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4d318-135">ถ้าบัญชีหลักเป็นบัญชีการปันส่วน ใช้ค่าเริ่มต้นจากข้อกำหนดบัญชีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="4d318-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4d318-136">ถ้าบัญชีหลักไม่ใช่บัญชีการปันส่วน ให้ใช้เท็มเพลตเริ่มต้นของมิติทางการเงินในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-137">ใช้ค่ามิติทางการเงินเริ่มต้นในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-138">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีแยกประเภทในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d318-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d318-139">ยอดภาษีขายของใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="4d318-140">ฟิลด์เจ้าหนี้ภาษีขายในหน้ากลุ่มการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4d318-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4d318-141">ใช้มิติทางการเงินที่ถูกกำหนดไว้ในยอดรายการใบแจ้งหนี้ข้อความอิสระหรือการกระจายสำหรับยอดในรายการค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="4d318-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="4d318-142">ใช้ค่ามิติทางการเงินเริ่มต้นในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-143">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีแยกประเภทในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d318-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d318-144">ยอดในรายการค่าธรรมเนียมใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="4d318-145">ฟิลด์บัญชีเครดิตในหน้ารหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="4d318-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4d318-146">ถ้าบัญชีหลักเป็นบัญชีการปันส่วน ใช้ค่าเริ่มต้นจากข้อกำหนดบัญชีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="4d318-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4d318-147">ถ้าบัญชีหลักไม่ใช่บัญชีการปันส่วน ให้ใช้เท็มเพลตเริ่มต้นของมิติทางการเงินในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-148">ใช้ค่ามิติทางการเงินเริ่มต้นในรายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4d318-149">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีแยกประเภทในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="4d318-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="4d318-150">การกระจายภาษี</span><span class="sxs-lookup"><span data-stu-id="4d318-150">Distributing taxes</span></span>
<span data-ttu-id="4d318-151">ไม่สามารถสร้างการกระจายการลงบัญชีสำหรับภาษีจนกว่าจะมีการคำนวณภาษี</span><span class="sxs-lookup"><span data-stu-id="4d318-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="4d318-152">ในการคำนวณภาษีขาย คุณต้องกรอกอย่างใดอย่างหนึ่งต่อไปนี้ในแบบฟอร์มใบแจ้งหนี้ข้อความอิสระ:</span><span class="sxs-lookup"><span data-stu-id="4d318-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="4d318-153">ดูรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="4d318-153">View the sales tax.</span></span>
-   <span data-ttu-id="4d318-154">ดูผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4d318-154">View the invoice total.</span></span>
-   <span data-ttu-id="4d318-155">ดูกระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="4d318-155">View the cash flow.</span></span>
-   <span data-ttu-id="4d318-156">ดูการกระจายการลงบัญชีสำหรับใบแจ้งหนี้ข้อความอิสระทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4d318-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="4d318-157">ดูสมุดรายวันของบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="4d318-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="4d318-158"> สมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="4d318-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="4d318-159">ก่อนที่คุณจะลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระคุณสามารถดูรายการบัญชีแบบเต็มของใบแจ้งหนี้ ซึ่งมีเดบิตและเครดิต เพื่อตรวจสอบว่าใบแจ้งหนี้นั้นมีการลงรายการบัญชีไปยังบัญชีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4d318-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="4d318-160">มุมมองรายการบัญชีแบบเต็มนี้เรียกว่าสมุดรายวันบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="4d318-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="4d318-161">ถ้ารายการสมุดรายวันบัญชีแยกประเภทย่อยไม่ถูกต้องเมื่อคุณดูตัวอย่างก่อนที่คุณบันทึกบัญชีใบแจ้งหนี้ข้อความอิสระ คุณไม่สามารถเปลี่ยนรายการสมุดรายวันบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="4d318-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="4d318-162">คุณต้องเปลี่ยนการกระจายการลงบัญชีหรือโพรไฟล์การลงรายการบัญชีแทน</span><span class="sxs-lookup"><span data-stu-id="4d318-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="4d318-163">การกระจายการลงบัญชีจะใช้เพื่อกำหนดด้านหนึ่งของรายการบัญชี เดบิตหรือเครดิต</span><span class="sxs-lookup"><span data-stu-id="4d318-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="4d318-164">การออฟเซ็ตรายการบัญชีสมุดรายวันบัญชีแยกประเภทย่อยที่สร้างจากโพรไฟล์การลงรายการบัญชี เช่นจากบัญชีลูกค้าหรือภาษี</span><span class="sxs-lookup"><span data-stu-id="4d318-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>




