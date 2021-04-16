---
title: กฎการตัดออก
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับกฎการตัดออกและตัวเลือกต่างๆ สำหรับการรายงานเกี่ยวกับการตัดออก
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0427c05f0c960bd898de3ac308d743f7ccec08f3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823775"
---
# <a name="elimination-rules"></a><span data-ttu-id="65d29-103">กฎการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65d29-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับกฎการตัดออกและตัวเลือกต่างๆ สำหรับการรายงานเกี่ยวกับการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="65d29-105">จำเป็นต้องมีธุรกรรมการตัดออกเมื่อนิติบุคคลหลักดำเนินธุรกิจกับนิติบุคคลในเครือหนึ่งนิติบุคคลขึ้นไป และใช้การรายงานการเงินที่รวมบัญชี </span><span class="sxs-lookup"><span data-stu-id="65d29-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="65d29-106">งบการเงินที่รวมบัญชีต้องรวมเฉพาะธุรกรรมที่เกิดขึ้นระหว่างองค์กรที่รวมบัญชี และเอนทิตี้อื่นภายนอกองค์กรนั้น</span><span class="sxs-lookup"><span data-stu-id="65d29-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="65d29-107">ดังนั้น ธุรกรรมระหว่างนิติบุคคลที่เป็นส่วนหนึ่งขององค์กรเดียวกันต้องถูกลบออก หรือตัดออกจากบัญชีแยกประเภททั่วไป เพื่อไม่ให้ปรากฏในรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="65d29-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="65d29-108">มีหลายวิธีในการรายงานเกี่ยวกับการตัดออก:</span><span class="sxs-lookup"><span data-stu-id="65d29-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="65d29-109">กฎการตัดออกสามารถสร้าง และประมวลผลในบริษัทที่รวมบัญชี หรือที่ตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="65d29-110">รายงานทางการเงินสามารถใช้เพื่อแสดงการตัดบัญชี และมิติเฉพาะในแถว หรือคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="65d29-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="65d29-111">นิติบุคคลที่แยกต่างหากที่สามารถใช้เพื่อลงรายการบัญชีธุรกรรมด้วยตนเองเพื่อติดตามการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="65d29-112">หัวข้อนี้เน้นเกี่ยวกับกฎการตัดออกที่ประมวลผลในบริษัทที่รวมบัญชี หรือที่ตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="65d29-113">คุณสามารถตั้งค่ากฎการตัดออกเพื่อสร้างธุรกรรมการตัดออกในนิติบุคคลที่ระบุเป็นปลายทางนิติบุคคลสำหรับการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="65d29-114">นิติบุคคลปลายทางนี้เรียกว่านิติบุคคลที่ตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="65d29-115">สมุดรายวันการตัดออกสามารถถูกสร้างระหว่างกระบวนการรวมบัญชี หรือโดยการใช้ข้อเสนอสมุดรายวันการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="65d29-116">ก่อนที่คุณจะตั้งค่ากฎการตัดออก คุณควรจะสร้างความคุ้นเคยกับข้อตกลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="65d29-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="65d29-117">**นิติบุคคลต้นทาง** – นิติบุคคลที่ยอดเงินที่ถูกตัดออกถูกลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="65d29-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="65d29-118">**นิติบุคคลปลายทาง** – นิติบุคคลที่กฎการตัดออกถูกลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="65d29-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="65d29-119">**นิติบุคคลที่ตัดออก** – นิติบุคคลที่ถูกระบุเป็นนิติบุคคลปลายทางสำหรับการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="65d29-120">**นิติบุคคลที่รวมบัญชี** – นิติบุคคลที่ถูกสร้างเพื่อรายงานผลลัพธ์ทางการเงินสำหรับกลุ่มของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="65d29-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="65d29-121">ข้อมูลทางการเงินจากนิติบุคคลถูกรวมบัญชีในนิติบุคคลนี้ และจากนั้นสร้างรายงานทางการเงินโดยใช้ข้อมูลที่รวม</span><span class="sxs-lookup"><span data-stu-id="65d29-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="65d29-122">ตารางต่อไปนี้แสดงชนิดของธุรกรรมที่อาจจำเป็นต้องมีการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65d29-123">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="65d29-123">Transaction type</span></span></th>
<th><span data-ttu-id="65d29-124">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="65d29-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65d29-125">รายการใบสั่งขายและการออกใบแจ้งหนี้ (การประมวลผลส่วนกลาง)</span><span class="sxs-lookup"><span data-stu-id="65d29-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="65d29-126">คุณขายผลิตภัณฑ์ให้กับลูกค้าในนามของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65d29-127">รายการใบสั่งขาย (ระหว่างบริษัท/ภายในบริษัท) และการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="65d29-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="65d29-128">คุณขายผลิตภัณฑ์ระหว่างนิติบุคคลในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65d29-129">ใบสั่งซื้อ (การประมวลผลส่วนกลาง)</span><span class="sxs-lookup"><span data-stu-id="65d29-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="65d29-130">คุณซื้อสินค้าคงคลัง วัสดุ บริการ สินทรัพย์ถาวร และผลิตภัณฑ์อื่นๆ จากผู้จัดจำหน่ายในนามของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65d29-131">การจัดการสินค้าคงคลัง (ระหว่างบริษัท/ภายในบริษัท)</span><span class="sxs-lookup"><span data-stu-id="65d29-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="65d29-132">คุณโอนย้ายสินค้าคงคลังหนึ่งของนิติบุคคลไปยังสินทรัพย์ถาวรของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="65d29-133">คุณโอนย้ายสินค้าคงคลังหนึ่งของนิติบุคคลไปยังสินค้าคงคลังของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65d29-134">การติดตามสินค้าคงคลังที่กำลังส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="65d29-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="65d29-135">คุณโอนย้ายสินค้าระหว่างคลังสินค้าในนิติบุคคลเดียวกันแต่เป็นการโอนย้ายระหว่างไซต์ทางภูมิศาสตร์ที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="65d29-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65d29-136">การประมวลผลใบแจ้งหนี้ส่วนกลางของบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="65d29-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="65d29-137">คุณบันทึกใบแจ้งหนี้ในนามของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65d29-138">การประมวลผลการชำระเงินส่วนกลางของบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="65d29-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="65d29-139">คุณชำระเงินในใบแจ้งหนี้ในนามของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65d29-140">การจัดการเงินสดและเงินคลัง (การประมวลผลจากส่วนกลาง)</span><span class="sxs-lookup"><span data-stu-id="65d29-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="65d29-141">คุณประมวลผลการชำระภาษี เงินคืนภาษี ค่าธรรมเนียมดอกเบี้ย เงินกู้ยืม เงินล่วงหน้า การชำระเงินปันผล และเงินค่าลิขสิทธิ์หรือค่าคอมมิชชันล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="65d29-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="65d29-142">คุณชำระค่าใช้จ่ายในนามของนิติบุคคลอื่นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="65d29-143">ใบแจ้งหนี้ถูกป้อนไว้ในสมุดบัญชีของนิติบุคคลปลายทาง และคุณต้องชำระเงินข้ามระหว่างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="65d29-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="65d29-144">ตัวอย่างเช่น นิติบุคคลหนึ่งชำระรายงานค่าใช้จ่ายของพนักงานในนิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="65d29-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="65d29-145">ในกรณีนี้ รายงานค่าใช้จ่ายของพนักงานที่มีค่าใช้จ่ายที่เกี่ยวข้องกับนิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="65d29-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="65d29-146">คุณโอนย้ายเงินสดจากนิติบุคคลหนึ่งไปยังอีกนิติบุคคลหนึ่งในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65d29-147">บัญชีลูกหนี้ (การประมวลผลส่วนกลาง)</span><span class="sxs-lookup"><span data-stu-id="65d29-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="65d29-148">คุณได้รับเงินสดสำหรับใบแจ้งหนี้ของลูกค้าของนิติบุคคลอื่น และคุณฝากเช็คเข้าไปยังบัญชีธนาคารของนิติบุคคลนั้น</span><span class="sxs-lookup"><span data-stu-id="65d29-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65d29-149">ค่าจ้าง (การประมวลผลส่วนกลาง ระหว่างบริษัท/ภายในบริษัท)</span><span class="sxs-lookup"><span data-stu-id="65d29-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="65d29-150">คุณชำระค่าจ้างของนิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="65d29-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="65d29-151">ตัวอย่างเช่น นิติบุคคลชำระค่าจ้างของพนักงานตัวเอง แต่เรียกคืนในส่วนที่พนักงานปฏิบัติงานให้กับอีกนิติบุคคลหนึ่งระหว่างการรันการจ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="65d29-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="65d29-152">หรือ พนักงานทำงานครึ่งเวลาสำหรับนิติบุคคล A และครึ่งเวลาสำหรับนิติบุคคล B และสวัสดิการอยู่ในค่าจ้างทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="65d29-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="65d29-153">ในกรณีดังกล่าว ค่าจ้างของพนักงานรวมค่าจ้างจากนิติบุคคลทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="65d29-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="65d29-154">ไม่เฉพาะเงินเดือนที่ลงรายการบัญชี แต่ภาษี สวัสดิการ การหักลด และรายการคงค้างสำหรับเงินเดือนยังได้รับการลงรายการบัญชีอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="65d29-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="65d29-155">คุณโอนย้ายแรงงานจากฝ่ายหรือแผนกหนึ่งไปยังฝ่ายหรือแผนกอื่น</span><span class="sxs-lookup"><span data-stu-id="65d29-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65d29-156">สินทรัพย์ถาวร (ระหว่างบริษัท/ภายในบริษัท)</span><span class="sxs-lookup"><span data-stu-id="65d29-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="65d29-157">คุณโอนย้ายสินทรัพย์ถาวรกับสินทรัพย์ถาวรหรือสินค้าคงคลังของนิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="65d29-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65d29-158">การปันส่วน (ระหว่างบริษัท/ภายในบริษัท)</span><span class="sxs-lookup"><span data-stu-id="65d29-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="65d29-159">คุณประมวลผลการปันส่วนองค์กร</span><span class="sxs-lookup"><span data-stu-id="65d29-159">You process corporate allocations.</span></span> <span data-ttu-id="65d29-160">การปันส่วนเป็นกิจกรรมสำหรับบัญชีใดๆ ซึ่งถูกปันส่วน โดยไม่คำนึงถึงโมดูลที่มา</span><span class="sxs-lookup"><span data-stu-id="65d29-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="65d29-161">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="65d29-161">Example</span></span>
<span data-ttu-id="65d29-162">นิติบุคคลของคุณ ซึ่งเป็นนิติบุคคล A ขายอุปกรณ์ให้กับนิติบุคคลอื่นในองค์กรของคุณ ซึ่งเป็นนิติบุคคล B ตัวอย่างต่อไปนี้แสดงว่าธุรกรรมที่เกิดขึ้นระหว่างนิติบุคคลทั้งสองอาจจำเป็นต้องมีการตัดออกมากน้อยเพียงใด:</span><span class="sxs-lookup"><span data-stu-id="65d29-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="65d29-163">นิติบุคคล A ขายอุปกรณ์ที่มีต้นทุน 10.00 ให้กับนิติบุคคล B ที่ 10.00</span><span class="sxs-lookup"><span data-stu-id="65d29-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="65d29-164">นิติบุคคล A ขายอุปกรณ์ที่มีต้นทุน 10.00 ให้กับนิติบุคคล B ที่ 10.00 บวกค่าจัดส่งตามจริง 2.00</span><span class="sxs-lookup"><span data-stu-id="65d29-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="65d29-165">นิติบุคคล A ขายอุปกรณ์ที่มีต้นทุน 10.00 ให้กับนิติบุคคล B ที่ 15.00 และรับกำไรขั้นต้นในราคาขาย</span><span class="sxs-lookup"><span data-stu-id="65d29-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="65d29-166">นิติบุคคล A ขายอุปกรณ์ที่มีต้นทุน 10.00 ให้กับนิติบุคคล B ที่ 15.00 และรับกำไรเบื้องต้นครึ่งนึงในราคาขาย</span><span class="sxs-lookup"><span data-stu-id="65d29-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="65d29-167">นิติบุคคล B รับอีกครึ่งหนึ่งของกำไรเบื้องต้นในราคาขาย</span><span class="sxs-lookup"><span data-stu-id="65d29-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="65d29-168">ดังนั้น รายได้จึงถูกแบ่ง</span><span class="sxs-lookup"><span data-stu-id="65d29-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="65d29-169">รายได้ที่แบ่งแสดงสิทธิประโยชน์ไปยังใบสั่งจากนิติบุคคลอื่นในองค์กรแทนที่จะเป็นองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="65d29-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="65d29-170">ธุรกรรมเหล่านี้ทั้งหมดสร้างธุรกรรมระหว่างบริษัทที่ลงรายการไปยังบัญชีลูกหนี้และบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="65d29-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="65d29-171">นอกจากนี้ธุรกรรมเหล่านี้อาจรวมยอดเงินการเพิ่มราคา และลดราคา เมื่อยอดเงินการขายระหว่างบริษัทไม่เท่ากับต้นทุนของสินค้าที่ขาย</span><span class="sxs-lookup"><span data-stu-id="65d29-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="65d29-172">ตั้งค่ากฎการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-172">Set up elimination rules</span></span>
<span data-ttu-id="65d29-173">เมื่อตั้งค่ากฎการกำจัดใน เราขอแนะนำให้คุณสร้างมิติทางการเงินโดยเฉพาะสำหรับวัตถุประสงค์การกำจัด</span><span class="sxs-lookup"><span data-stu-id="65d29-173">When setting up elimination rules, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="65d29-174">ลูกค้าส่วนใหญ่ตั้งชื่อเป็นคู่ค้าหรือชื่ออื่นที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="65d29-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="65d29-175">ถ้าคุณเลือกที่จะไม่ใช้มิติทางการเงิน ให้แน่ใจว่ามีบัญชีหลักที่เฉพาะเจาะจงสำหรับธุรกรรมระหว่างบริษัทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="65d29-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="65d29-176">การตั้งค่าสำหรับการตัดออกจะพบในพื้นที่การตั้งค่าของโมดูลการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="65d29-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="65d29-177">หลังจากที่คุณป้อนคำอธิบายสำหรับกฎ คุณต้องเลือกบริษัทที่จะลงรายการบัญชีสมุดรายวันการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="65d29-178">ซึ่งควรเป็นบริษัทที่เลือก **ใช้สำหรับกระบวนการตัดออกทางการเงิน** ไว้ในการตั้งค่านิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="65d29-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="65d29-179">คุณสามารถตั้งค่าวันที่ที่กฎการตัดออกมีผลบังคับใช้และเมื่อใดที่จะหมดอายุ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="65d29-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="65d29-180">คุณต้องตั้งค่า **ใช้งานอยู่** เป็น **ใช่** ถ้าคุณต้องการให้พร้อมใช้งานในกระบวนการข้อเสนอการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="65d29-181">เลือกชื่อสมุดรายวันที่มีชนิดของ **การตัดออก**</span><span class="sxs-lookup"><span data-stu-id="65d29-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="65d29-182">หลังจากที่คุณได้กำหนดพื้นฐานแล้ว คุณสามารถกำหนดกฎการประมวลผลจริงโดยการคลิก **บรรทัด**</span><span class="sxs-lookup"><span data-stu-id="65d29-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="65d29-183">มีสองตัวเลือกสำหรับการตัดออก การตัดการเปลี่ยนยอดเงินสุทธิหรือการกำหนดจำนวนเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="65d29-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="65d29-184">เลือกบัญชีต้นทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="65d29-184">Select your source account.</span></span> <span data-ttu-id="65d29-185">คุณสามารถใช้เครื่องหมายดอกจัน (\*) เป็นไวด์การ์ด</span><span class="sxs-lookup"><span data-stu-id="65d29-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="65d29-186">ตัวอย่างเช่น 1\* จะต้องเลือกบัญชีทั้งหมดที่เริ่มต้นด้วย 1 เป็นต้นทางข้อมูลสำหรับการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="65d29-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="65d29-187">หลังจากที่คุณได้เลือกบัญชีต้นทางของคุณแล้ว **ข้อมูลจำเพาะเกี่ยวกับบัญชี** จะกำหนดบัญชีจากบริษัทปลายทางที่ใช้</span><span class="sxs-lookup"><span data-stu-id="65d29-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="65d29-188">เลือก **ต้นทาง** ถ้าคุณต้องการใช้บัญชีหลักเดียวกันที่กำหนดไว้ในบัญชี **ต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="65d29-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="65d29-189">ถ้าคุณเลือก **กำหนดโดยผู้ใช้** จากนั้นคุณต้องระบุบัญชีปลายทาง</span><span class="sxs-lookup"><span data-stu-id="65d29-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="65d29-190">ข้อมูลจำเพาะของมิติทำหน้าที่ในลักษณะเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="65d29-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="65d29-191">ถ้าคุณเลือก **ต้นทาง** ระบบจะใช้มิติเดียวกันในบริษัทปลายทางเป็นบริษัทต้นทาง</span><span class="sxs-lookup"><span data-stu-id="65d29-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="65d29-192">ถ้าคุณเลือก **กำหนดโดยผู้ใช้** คุณจะต้องระบุมิติในบริษัทปลายทางโดยการคลิกรายการเมนู **มิติปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="65d29-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="65d29-193">เลือกมิติต้นทางและมิติทางการเงิน และค่าที่จะใช้เป็นต้นทางของการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="65d29-194">ดำเนินการธุรกรรมการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-194">Process elimination transactions</span></span>
<span data-ttu-id="65d29-195">มีสองวิธีในการประมวลผลธุรกรรมการตัดออกในระหว่างกระบวนการรวมบัญชีแบบออนไลน์ หรือโดยการสร้างสมุดรายวันการตัดออก และการเรียกใช้กระบวนการข้อเสนอการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="65d29-196">ส่วนนี้มุ่งเน้นเกี่ยวกับการสร้างสมุดรายวันและเรียกใช้กระบวนการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="65d29-197">ในบริษัทที่กำหนดให้เป็นบริษัทที่ตัดออก เลือก **สมุดรายวันการตัดออก** ในโมดูลการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="65d29-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="65d29-198">หลังจากที่คุณเลือกชื่อสมุดรายวันแล้ว ให้คลิก **บรรทัด**</span><span class="sxs-lookup"><span data-stu-id="65d29-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="65d29-199">คุณสามารถเรียกใช้ข้อเสนอโดยการเลือกเมนู **ข้อเสนอ** และจากนั้นเลือก **ข้อเสนอการตัดออก** ได้</span><span class="sxs-lookup"><span data-stu-id="65d29-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="65d29-200">เลือกบริษัทที่เป็นต้นทางของข้อมูลที่รวมไว้ และจากนั้น เลือกกฎที่คุณต้องการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="65d29-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="65d29-201">ป้อนวันที่เริ่มต้นเพื่อเริ่มการค้นหาสำหรับยอดเงินการตัดออก และวันที่สิ้นสุดเพื่อสิ้นสุดการค้นหาวันที่สำหรับยอดเงินการตัดออก</span><span class="sxs-lookup"><span data-stu-id="65d29-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="65d29-202">ในฟิลด์ **วันที่ลงรายการบัญชีแยกประเภททั่วไป** คือวันที่ใช้ในการลงรายการบัญชีสมุดรายวันไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="65d29-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="65d29-203">หลังจากที่คุณคลิก **ตกลง** คุณสามารถตรวจสอบยอดเงินและลงรายการบัญชีสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="65d29-203">After you click **OK**, you can review the amounts and post the journal.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]