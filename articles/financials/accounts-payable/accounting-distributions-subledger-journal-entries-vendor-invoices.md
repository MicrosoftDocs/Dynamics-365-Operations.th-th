---
title: การกระจายการลงบัญชีและรายการสมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย
description: การกระจายการลงบัญชีจะใช้เพื่อกำหนดวิธีลงบัญชีของบอดเงิน เช่น วิธีการลงบัญชีค่าใช้จ่าย ภาษี หรือค่าธรรมเนียม ในใบแจ้งหนี้ของผู้จัดจำหน่าย  ทุกยอดเงินที่ต้องนำมาลงบัญชีเมื่อใบแจ้งหนี้ของผู้จัดจำหน่ายถูกบันทึกบัญชีในสมุดรายวัน จะมีการกระจายการลงบัญชีหนึ่งรายการขึ้นไป
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f59eb2f61bc6bc887461683408b57c4672ce5bf1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "351366"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="e48f6-104">การกระจายการลงบัญชีและรายการสมุดรายวันของบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e48f6-105">การกระจายการลงบัญชีจะใช้เพื่อกำหนดวิธีลงบัญชีของบอดเงิน เช่น วิธีการลงบัญชีค่าใช้จ่าย ภาษี หรือค่าธรรมเนียม ในใบแจ้งหนี้ของผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="e48f6-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="e48f6-106">ทุกยอดเงินที่ต้องนำมาลงบัญชีเมื่อใบแจ้งหนี้ของผู้จัดจำหน่ายถูกบันทึกบัญชีในสมุดรายวัน จะมีการกระจายการลงบัญชีหนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="e48f6-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="e48f6-107">การกระจายการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="e48f6-108">คุณสามารถใช้ปุ่มต่างๆ ต่อไปนี้ในหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อดู และอาจแก้ไข การกระจายการลงบัญชีสำหรับแต่ละยอดเงินบนใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="e48f6-109">**กระจายยอดเงิน** – ดูและเปลี่ยนแปลงการกระจายการลงบัญชี สำหรับแต่ละรายการและรายการข้อมูลรองใดๆ เช่น ภาษีหรือค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="e48f6-110">คุณยังสามารถดูและแก้ไขการกระจายการลงบัญชีสำหรับรายการรองโดยตรงจากหน้าธุรกรรมภาษีขายหรือหน้าธุรกรรมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="e48f6-111">แก้ไขยอดเงินในส่วนหัวใบแจ้งหนี้ผู้จัดจำหน่าย เช่น ค่าธรรมเนียมหรือยอดเงินการปัดเศษสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="e48f6-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="e48f6-112">แก้ไขยอดเงินรายการใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="e48f6-113">**ดูการกระจาย**- ดูการกระจายการลงบัญชีสำหรับรายการเอกสารทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e48f6-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="e48f6-114">คุณไม่สามารถที่จะแก้ไขการกระจายการลงบัญชีจากมุมมองนี้</span><span class="sxs-lookup"><span data-stu-id="e48f6-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="e48f6-115">ดูยอดส่วนหัวและยอดรายการ</span><span class="sxs-lookup"><span data-stu-id="e48f6-115">View header and line amounts.</span></span>

<span data-ttu-id="e48f6-116">ถ้าใบแจ้งหนี้ของผู้จัดจำหน่ายอ้างอิงใบสั่งซื้อ คุณสามารถแบ่ง และแก้ไขการกระจายการลงบัญชีสำหรับบรรทัดที่มีสินค้าที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="e48f6-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="e48f6-117">ถ้าบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่ายไม่ได้อ้างอิงบรรทัดใบสั่งซื้อ คุณยังสามารถลบการกระจายการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="e48f6-118">คุณไม่สามารถแบ่งหรือลบรายการสำหรับค่าธรรมเนียม ภาษี และส่วนลดต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="e48f6-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="e48f6-119">คุณสามารถปรับเปลี่ยนบัญชีแยกประเภท แต่คุณไม่สามารถเปลี่ยนยอดเงินหรือเปอร์เซ็นต์ได้</span><span class="sxs-lookup"><span data-stu-id="e48f6-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="e48f6-120">ถ้ารายการหลักที่ประกอบด้วยสินค้าที่ไม่ได้เก็บในคลัง และกระจายการลงบัญชีจะถูกแยก รายการรองจะถูกแบ่งโดยอัตโนมัติเพื่อให้ตรงกับมิติทางการเงินของรายการหลัก </span><span class="sxs-lookup"><span data-stu-id="e48f6-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="e48f6-121">การกระจายการลงบัญชีสำหรับรายการรองไม่สามารถแบ่งหรือลบเพิ่มเติม แต่ขึ้นอยู่กับการตั้งค่าของรายการรอง คุณอาจสามารถแก้ไขบัญชีแยกประเภทสำหรับการกระจายการลงบัญชีของรายการรอง</span><span class="sxs-lookup"><span data-stu-id="e48f6-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="e48f6-122">ยอดการกระจาย</span><span class="sxs-lookup"><span data-stu-id="e48f6-122">Distributing amounts</span></span>
<span data-ttu-id="e48f6-123">เมื่อคุณป้อนใบแจ้งหนี้ของผู้จัดจำหน่าย แต่ละยอดจะมีกระจายดังนั้น</span><span class="sxs-lookup"><span data-stu-id="e48f6-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e48f6-124">บรรทัดชนิดของใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="e48f6-125">ลำดับความสำคัญที่กำหนดว่าบัญชีหลักจะแสดงจากไหน</span><span class="sxs-lookup"><span data-stu-id="e48f6-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="e48f6-126">ลำดับความสำคัญที่กำหนดมิติทางการเงินเริ่มต้นที่จะแสดง</span><span class="sxs-lookup"><span data-stu-id="e48f6-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e48f6-127">ผลิตภัณฑ์ที่เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="e48f6-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-128">การกระจายการลงบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-129">ในฟิลด์บัญชีหลัก เมื่อรายจ่ายการซื้อสำหรับผลิตภัณฑ์ถูกเลือกในหน้าการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-130">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-131">ใช้ค่ามิติทางการเงินเริ่มต้นในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e48f6-132">ประเภทการจัดซื้อหรือผลิตภัณฑ์ที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="e48f6-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-133">การกระจายการลงบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่ายอ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-134">ในฟิลด์บัญชีหลัก เมื่อรายจ่ายการซื้อสำหรับค่าใช้จ่ายถูกเลือกในหน้าการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-135">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-136">ถ้าบัญชีหลักเป็นบัญชีการปันส่วน ใช้ค่าเริ่มต้นจากข้อกำหนดบัญชีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e48f6-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="e48f6-137">ใช้ค่ามิติทางการเงินเริ่มต้นในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="e48f6-138">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-139">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e48f6-140">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e48f6-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-141">การกระจายการลงบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่ายอ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-142">ถ้าการซื้อสินทรัพย์ถูกเลือกไว้ในฟิลด์ชนิดธุรกรรมในแบบฟอร์มใบแจ้งหนี้ของผู้จัดจำหน่าย ฟิลด์บัญชีหลักเมื่อการซื้อสินทรัพย์จะถูกเลือกในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e48f6-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="e48f6-143">ถ้าการปรับปรุงการซื้อสินทรัพย์ถูกเลือกไว้ในฟิลด์ชนิดธุรกรรม ฟิลด์บัญชีหลักเมื่อการปรับปรุงการซื้อสินทรัพย์จะถูกเลือกในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e48f6-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-144">ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-145">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-146">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e48f6-147">โครงการที่กำหนดบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-148">การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-149">ถ้ายอดดุลถูกเลือกในต้นทุนลงรายการบัญชี - ฟิลด์สินค้าในหน้ากลุ่มโครงการ ฟิลด์บัญชีหลักเมื่อต้นทุนถูกเลือกไว้ในหน้าการตั้งค่าการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e48f6-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="e48f6-150">ถ้ากำไรและขาดทุนถูกเลือกในต้นทุนลงรายการบัญชี - ฟิลด์สินค้าในหน้ากลุ่มโครงการ ฟิลด์บัญชีหลักเมื่อต้นทุน - สินค้าถูกเลือกไว้ในหน้าการตั้งค่าการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e48f6-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-151">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e48f6-152">ส่วนลดต่อรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="e48f6-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-153">การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-154">ฟิลด์บัญชีหลักเมื่อส่วนลดถูกเลือกในหน้าการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="e48f6-155">ถ้าไม่มีการกำหนดบัญชีหลักสำหรับส่วนลดในโพรไฟล์การลงรายการบัญชี การกระจายการลงบัญชีสำหรับราคารวมบนบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-156">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายการลงบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-157">ใช้มิติทางการเงินจากการกระจายการลงบัญชีสำหรับราคารวมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-158">ใช้ค่ามิติทางการเงินสำหรับบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-159">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e48f6-160">ค่าธรรมเนียมการซื้อที่ป้อนบนแท็บราคาและส่วนลดของรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-161">การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-162">การกระจายการลงบัญชีของราคารวมบนบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-163">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-164">ใช้มิติทางการเงินจากการกระจายการลงบัญชีสำหรับราคารวมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e48f6-165">ค่าธรรมเนียมรายการ</span><span class="sxs-lookup"><span data-stu-id="e48f6-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-166">การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-167">ถ้าบัญชีแยกประเภทถูกเลือกในฟิลด์ชนิดเดบิตในแบบฟอร์มรหัสค่าธรรมเนียม ฟิลด์บัญชีเดบิตในหน้ารหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="e48f6-168">ถ้าสินค้าถูกเลือกในฟิลด์ชนิดเดบิตในแบบฟอร์มรหัสค่าธรรมเนียม การกระจายการลงบัญชีสำหรับราคารวมบนรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-169">ถ้าลูกค้า/ผู้จัดจำหน่ายถูกเลือกในฟิลด์ชนิดเดบิตในแบบฟอร์มรหัสค่าธรรมเนียม ฟิลด์บัญชีเครดิตในหน้ารหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-170">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-171">ใช้มิติทางการเงินจากการกระจายการลงบัญชีสำหรับราคารวมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-172">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-173">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e48f6-174">ภาษี มีเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e48f6-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="e48f6-175">ตัวเลือกกฎการเก็บภาษีที่ใช้ในสหรัฐอเมริกาถูกเลือกในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e48f6-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="e48f6-176">การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-177">การกระจายการลงบัญชีของราคารวมหรือค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-178">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-179">ใช้มิติทางการเงินจากการกระจายการลงบัญชีสำหรับราคารวมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-180">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e48f6-181">ภาษี มีเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e48f6-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e48f6-182">ตัวเลือกกฎการเก็บภาษีที่ใช้ในสหรัฐอเมริกาถูกล้างข้อมูลในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e48f6-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="e48f6-183">ฟิลด์ภาษีนำเข้าสำหรับกลุ่มภาษีขายถูกล้างข้อมูลในหน้ากลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e48f6-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="e48f6-184">ถ้ายอดเงินภาษีได้รับคืน ฟิลด์ลูกหนี้ภาษีขายในหน้ากลุ่มการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e48f6-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="e48f6-185">ถ้ายอดภาษีไม่สามารถกู้คืน ราคารวมหรือการกระจายการลงบัญชีสำหรับค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-186">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-187">ใช้มิติทางการเงินจากราคารวมหรือการกระจายการลงบัญชีสำหรับค่าธรรมเนียมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-188">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-189">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e48f6-190">ภาษี มีเงื่อนไขต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e48f6-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e48f6-191">ตัวเลือกกฎการเก็บภาษีที่ใช้ในสหรัฐอเมริกาถูกล้างข้อมูลในหน้าพารามิเตอร์บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="e48f6-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="e48f6-192">ฟิลด์ภาษีนำเข้าสำหรับกลุ่มภาษีขายถูกเลือกในหน้ากลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e48f6-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="e48f6-193">ถ้ายอดเงินภาษีได้รับคืน ฟิลด์ลูกหนี้ภาษีขายในหน้ากลุ่มการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e48f6-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="e48f6-194">ถ้ายอดเงินภาษีไม่ได้รับคืน ฟิลด์ค่าใช้จ่ายภาษีนำเข้าในหน้ากลุ่มการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="e48f6-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-195">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-196">ใช้มิติทางการเงินจากราคารวมหรือการกระจายการลงบัญชีสำหรับค่าธรรมเนียมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-197">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-198">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e48f6-199">ค่าธรรมเนียมในส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="e48f6-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-200">ถ้าบัญชีแยกประเภทถูกเลือกในฟิลด์ชนิดเดบิตในแบบฟอร์มรหัสค่าธรรมเนียม ฟิลด์บัญชีเดบิตในหน้ารหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="e48f6-201">ถ้าลูกค้า/ผู้จัดจำหน่ายถูกเลือกในฟิลด์ชนิดเดบิตในแบบฟอร์มรหัสค่าธรรมเนียม ฟิลด์บัญชีเครดิตในหน้ารหัสค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="e48f6-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-202">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-203">ถ้าบัญชีหลักเป็นบัญชีการปันส่วน ใช้ค่าเริ่มต้นจากข้อกำหนดบัญชีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="e48f6-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="e48f6-204">ใช้ค่าเท็มเพลตเริ่มต้นสำหรับมิติทางการเงินจากส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="e48f6-205">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-206">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e48f6-207">ส่วนลดหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="e48f6-208">ฟิลด์บัญชีหลักสำหรับชนิดการลงรายการบัญชีส่วนลดใบแจ้งหนี้ของผู้จัดจำหน่าย ในบัญชีสำหรับหน้าธุรกรรมอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e48f6-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="e48f6-209">ถ้าบรรทัดใบแจ้งหนี้อ้างอิงถึงบรรทัดใบสั่งซื้อ ใช้การกระจายบัญชีสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e48f6-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="e48f6-210">ใช้มิติทางการเงินจากการกระจายการลงบัญชีสำหรับราคารวมบนบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-211">ใช้ค่ามิติทางการเงินจากบรรทัดใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="e48f6-212">ใช้ค่ามิติทางการเงินเริ่มต้นจากบัญชีหลักในหน้าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e48f6-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="e48f6-213">การกระจายภาษี</span><span class="sxs-lookup"><span data-stu-id="e48f6-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="e48f6-214">ไม่สามารถสร้างการกระจายการลงบัญชีสำหรับภาษีจนกว่าจะมีการคำนวณภาษี</span><span class="sxs-lookup"><span data-stu-id="e48f6-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="e48f6-215">ในการคำนวณภาษีขาย คุณต้องดำเนินการงานอย่างใดอย่างหนึ่งต่อไปนี้ในหน้าใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="e48f6-216">ดูผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e48f6-216">View the invoice total.</span></span>
-   <span data-ttu-id="e48f6-217">ดูรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="e48f6-217">View the sales tax.</span></span>
-   <span data-ttu-id="e48f6-218">ดูสมุดรายวันของบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="e48f6-218">View the subledger journal.</span></span>
-   <span data-ttu-id="e48f6-219">ดูการกระจายการลงบัญชีสำหรับรายการใบแจ้งหนี้ของผู้จัดจำหน่ายที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e48f6-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="e48f6-220">ระงับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="e48f6-221">ลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="e48f6-222">สมุดรายวันบัญชีแยกประเภทย่อยสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="e48f6-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="e48f6-223">ก่อนที่คุณจะลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย คุณสามารถดูรายการบัญชีแบบเต็มของใบแจ้งหนี้ ซึ่งมีเดบิตและเครดิต เพื่อตรวจสอบว่าใบแจ้งหนี้นั้นได้ลงรายการบัญชีไปยังบัญชีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e48f6-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="e48f6-224">มุมมองรายการบัญชีแบบเต็มนี้เรียกว่าสมุดรายวันบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="e48f6-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="e48f6-225">ถ้ารายการสมุดรายวันของบัญชีแยกประเภทย่อยไม่ถูกต้อง เมื่อคุณดูตัวอย่างก่อนที่คุณบันทึกบัญชีใบแจ้งหนี้ผู้จัดจำหน่าย คุณไม่สามารถแก้ไขรายการสมุดรายวันของบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="e48f6-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="e48f6-226">คุณต้องแก้ไขการกระจายการลงบัญชีหรือโพรไฟล์การลงรายการบัญชีแทน</span><span class="sxs-lookup"><span data-stu-id="e48f6-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="e48f6-227">การกระจายการลงบัญชีจะใช้เพื่อกำหนดด้านหนึ่งของรายการบัญชี เดบิตหรือเครดิต</span><span class="sxs-lookup"><span data-stu-id="e48f6-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="e48f6-228">รายการบัญชีสมุดรายวันของบัญชีแยกประเภทย่อยออฟเซ็ตถูกสร้างโดยโพรไฟล์การลงรายการบัญชี เช่น จากบัญชีผู้จัดจำหน่าย หรือ ภาษี</span><span class="sxs-lookup"><span data-stu-id="e48f6-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





