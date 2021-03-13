---
title: VAT ที่ยังไม่รับรู้และที่รับรู้ของประเทศไทย
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับภาษีมูลค่าเพิ่ม (VAT) ที่ยังไม่รับรู้และที่รับรู้ในประเทศไทย
author: anasyash
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, VendParameters, CustParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265924
ms.assetid: 829a101f-e329-48b9-baf8-e36670ff43c8
ms.search.region: Thailand
ms.author: anasyash
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f8536a54da9fb0a0598155b25573c0179d1051c6
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060584"
---
# <a name="thailand-unrealized-and-realized-vat"></a><span data-ttu-id="896ea-103">VAT ที่ยังไม่รับรู้และที่รับรู้ของประเทศไทย</span><span class="sxs-lookup"><span data-stu-id="896ea-103">Thailand unrealized and realized VAT</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="896ea-104">หัวข้อนี้ให้ข้อมูลเกี่ยวกับภาษีมูลค่าเพิ่ม (VAT) ที่ยังไม่รับรู้และที่รับรู้ในประเทศไทย</span><span class="sxs-lookup"><span data-stu-id="896ea-104">This topic provides information about unrealized and realized value-added tax (VAT) for Thailand.</span></span> <span data-ttu-id="896ea-105">และยังอธิบายวิธีการชำระธุรกรรมที่มี VAT ที่ยังไม่รับรู้ วิธีการกลับรายการ VAT ที่ยังไม่รับรู้ และรายงานใดที่สามารถสร้างได้บ้าง</span><span class="sxs-lookup"><span data-stu-id="896ea-105">It also explains how to settle transactions that have unrealized VAT, how to reverse unrealized VAT, and what reports can be generated.</span></span>

<span data-ttu-id="896ea-106">ในปัจจุบัน สามารถคํานวณ VAT ได้สี่ชนิด</span><span class="sxs-lookup"><span data-stu-id="896ea-106">Currently, four types of VAT can be calculated.</span></span> <span data-ttu-id="896ea-107">จะได้รับการกำหนดโดยแอททริบิวต์สองหมวดหมู่ คือ **VAT การซื้อ/ขาย** และ **VAT ที่รับรู้/ที่ยังไม่รับรู้**</span><span class="sxs-lookup"><span data-stu-id="896ea-107">They are defined by two categorical attributes: **Purchase/Sales VAT** and **Realized/Unrealized VAT**.</span></span> <span data-ttu-id="896ea-108">ตารางต่อไปนี้จะให้ข้อมูลเกี่ยวกับ VAT แต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="896ea-108">The following table provides information about each type of VAT.</span></span>

<table width="100%">
<tbody>
<tr>
<td width="15%">
<p><span data-ttu-id="896ea-109"><strong>เงื่อนไข</strong></span><span class="sxs-lookup"><span data-stu-id="896ea-109"><strong>Term</strong></span></span></p>
</td>
<td width="30%">
<p><span data-ttu-id="896ea-110"><strong>คำนิยาม</strong></span><span class="sxs-lookup"><span data-stu-id="896ea-110"><strong>Definition</strong></span></span></p>
</td>
<td width="54%">
<p><span data-ttu-id="896ea-111"><strong>เมื่อมีการคํานวณ VAT</strong></span><span class="sxs-lookup"><span data-stu-id="896ea-111"><strong>When the VAT is calculated</strong></span></span></p>
</td>
</tr>
<tr>
<td width="15%">
<p><span data-ttu-id="896ea-112">VAT ของการซื้อที่ยังไม่รับรู้ (หรือที่เรียกอีกอย่างว่า VAT ที่ยังไม่รับรู้)</span><span class="sxs-lookup"><span data-stu-id="896ea-112">Unrealized purchase VAT (also known as deferred input VAT)</span></span></p>
</td>
<td width="30%">
<p><span data-ttu-id="896ea-113">ยอด VAT ที่คํานวณได้&rsquo;ซึ่งไม่ครบกําหนดชําระจนกว่าจะชําระใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-113">The calculated VAT amount that isn&rsquo;t due until the invoice is paid.</span></span> <span data-ttu-id="896ea-114">จำนวนนี้มีการลงรายการบัญชี VAT ซื้อที่ยังไม่รับรู้ และสามารถเรียกหลังจากได้รับใบกำกับภาษีแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="896ea-114">This amount is posted to an unrealized purchase VAT account and can be claimed only after a tax invoice is received.</span></span></p>
</td>
<td width="54%">
<p><span data-ttu-id="896ea-115">คุณสร้างและลงรายการบัญชีใบสั่งซื้อที่มี VAT ของการซื้อที่ยังไม่รับรู้ สำหรับสินค้าหรือบริการก่อนที่คุณจะได้รับใบกำกับภาษีจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="896ea-115">You create and post a purchase order that has unrealized purchase VAT for items or services before you receive the tax invoice from the vendor.</span></span></p>
</td>
</tr>
<tr>
<td width="15%">
<p><span data-ttu-id="896ea-116">VAT ของการซื้อที่รับรู้ (หรือที่เรียกอีกอย่างว่า VAT ซื้อ)</span><span class="sxs-lookup"><span data-stu-id="896ea-116">Realized purchase VAT (also known as input VAT)</span></span></p>
</td>
<td width="30%">
<p><span data-ttu-id="896ea-117">ภาษีการซื้อ&rsquo;หรือจัดหาวัสดุของบริษัท</span><span class="sxs-lookup"><span data-stu-id="896ea-117">The tax on a company&rsquo;s purchases or input supplies.</span></span> <span data-ttu-id="896ea-118">ภาษีนี้ใช้ได้กับราคาซื้อและถูกอ้างอิงเป็น VAT ของการซื้อด้วย</span><span class="sxs-lookup"><span data-stu-id="896ea-118">This tax is applicable to the purchase price and is also referred to as the purchase VAT.</span></span></p>
</td>
<td width="54%">
<p><span data-ttu-id="896ea-119">คุณย้อนกลับ VAT ซื้อที่ยังไม่รับรู้เพื่อลงรายการบัญชี VAT ซื้อที่รับรู้ไปยังบัญชี VAT ซื้อ หลังจากที่คุณได้รับใบกำกับภาษีจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="896ea-119">You reverse the unrealized purchase VAT to post the realized purchase VAT to the purchase VAT account after you receive the tax invoice from the vendor.</span></span></p>
<p><span data-ttu-id="896ea-120">คุณสามารถรับทราบว่าคุณ&rsquo;ได้รับใบกำกับภาษีจากผู้จัดจำหน่าย และรับรู้ VAT ในสถานการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-120">You can acknowledge that you&rsquo;ve received the tax invoice from the vendor, and realize the VAT, in the following situations:</span></span></p>
<ul>
<li><span data-ttu-id="896ea-121">คุณลงรายการบัญชีใบสั่งซื้อหรือสมุดรายวันใบแจ้งหนี้หลังจากที่คุณได้รับใบกำกับภาษีจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="896ea-121">You post a purchase order or invoice journal after you receive the tax invoice from the vendor.</span></span> <span data-ttu-id="896ea-122">เมื่อต้องการบันทึก VAT ของการซื้อที่รับรู้โดยตรง คุณต้องป้อนหมายเลขใบกำกับภาษี วันที่ในใบกำกับภาษี และวันที่รับสินค้าในใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="896ea-122">To record the realized purchase VAT directly, you must enter the tax invoice number, tax invoice date, and tax invoice receipt date.</span></span></li>
<li><span data-ttu-id="896ea-123">คุณลงรายการบัญชีสมุดรายวันการชำระเงินหลังจากที่คุณได้รับใบกำกับภาษีจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="896ea-123">You post the payment journal after you receive the tax invoice from the vendor.</span></span> <span data-ttu-id="896ea-124">หากต้องการย้อนกลับ VAT ที่ยังไม่รับรู้โดยตรง คุณต้องป้อนหมายเลขใบกำกับภาษี วันที่ในใบกำกับภาษี และวันที่รับใบกำกับภาษีที่เกี่ยวข้องกับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="896ea-124">To reverse the unrealized VAT directly, you must enter the tax invoice number, tax invoice date, and tax invoice receipt date that are applicable to the payment.</span></span></li>
<li><span data-ttu-id="896ea-125">คุณยืนยันสมุดรายวันของการกลับรายการ เพื่อกลับรายการ VAT ที่ยังไม่รับรู้โดยทางอ้อม</span><span class="sxs-lookup"><span data-stu-id="896ea-125">You confirm the reversal journal to reverse the unrealized VAT indirectly.</span></span> <span data-ttu-id="896ea-126">หากไม่ได้&rsquo;รับใบกำกับภาษีเมื่อชำระเงิน หรือหากมีการชำระเงินสำหรับใบกำกับภาษีหลายใบ คุณจะสามารถใช้ <strong>หน้าสมุดรายวันการกลับรายการ</strong> ได้</span><span class="sxs-lookup"><span data-stu-id="896ea-126">If the tax invoice isn&rsquo;t received at the time of payment, or if the payment is made for multiple tax invoices, you can use the <strong>Reversal journal</strong> page.</span></span> <span data-ttu-id="896ea-127">หากต้องการย้อนกลับ VAT ที่ยังไม่รับรู้และลงรายการบัญชี VAT ซื้อที่รับรู้แล้ว คุณต้องป้อนหมายเลขใบกำกับภาษี วันที่ในใบกำกับภาษี และวันที่รับใบกำกับภาษีที่เกี่ยวข้องกับใบแจ้งหนี้แต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="896ea-127">To reverse the unrealized VAT and post the realized purchase VAT, you must enter the tax invoice number, tax invoice date, and tax invoice receipt date that are applicable for each invoice.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td width="15%">
<p><span data-ttu-id="896ea-128">VAT ของการขายที่ยังไม่รับรู้ (หรือที่เรียกอีกอย่างว่า VAT ของการขายที่ยังไม่รับรู้)</span><span class="sxs-lookup"><span data-stu-id="896ea-128">Unrealized sales VAT (also known as deferred output VAT)</span></span></p>
</td>
<td width="30%">
<p><span data-ttu-id="896ea-129">ยอด VAT ที่คํานวณได้&rsquo;ซึ่งไม่ครบกําหนดชําระจนกว่าจะชําระใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-129">The calculated VAT amount that isn&rsquo;t due until the invoice is paid.</span></span> <span data-ttu-id="896ea-130">จำนวนนี้มีการลงรายการบัญชี VAT ขายที่ยังไม่รับรู้ และสามารถเรียกหลังจากพิมพ์ใบเสร็จหรือใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="896ea-130">This amount is posted to an unrealized sales VAT account and can be claimed only after a tax invoice or receipt is printed.</span></span></p>
</td>
<td width="54%">
<p><span data-ttu-id="896ea-131">คุณสร้างและลงรายการบัญชีใบสั่งขายหรือใบแจ้งหนี้ข้อความอิสระที่มี VAT ของการขายที่ยังไม่รับรู้ของสินค้าหรือบริการโดยการสร้างใบแจ้งหนี้เพียงใบเดียว</span><span class="sxs-lookup"><span data-stu-id="896ea-131">You create and post a sales order or free text invoice that has unrealized sales VAT for items or services by generating only an invoice.</span></span></p>
</td>
</tr>
<tr>
<td width="15%">
<p><span data-ttu-id="896ea-132">VAT ของการขายที่รับรู้ (หรือที่เรียกอีกอย่างว่า VAT ขาย)</span><span class="sxs-lookup"><span data-stu-id="896ea-132">Realized sales VAT (also known as output VAT)</span></span></p>
</td>
<td width="30%">
<p><span data-ttu-id="896ea-133">ภาษีของ&rsquo;การขายของบริษัท</span><span class="sxs-lookup"><span data-stu-id="896ea-133">The tax on a company&rsquo;s sales.</span></span> <span data-ttu-id="896ea-134">ภาษีนี้ใช้ได้กับราคาขายและถูกอ้างอิงเป็น VAT ของการขายด้วย</span><span class="sxs-lookup"><span data-stu-id="896ea-134">This tax is applicable to the sales price and is also referred to as the sales VAT.</span></span></p>
</td>
<td width="54%">
<p><span data-ttu-id="896ea-135">คุณกลับรายการ VAT ของการขายที่ยังไม่รับรู้ เพื่อลงรายการบัญชี VAT ของการขายที่รับรู้ในบัญชี VAT ของการขาย หลังจากที่คุณสร้างใบกำกับภาษีหรือใบเสร็จรับเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="896ea-135">You reverse the unrealized sales VAT to post the realized sales VAT to the sales VAT account after you generate the tax invoice or receipt for the customer.</span></span></p>
<p><span data-ttu-id="896ea-136">คุณสามารถสร้างใบกำกับภาษีหรือใบเสร็จรับเงิน และรับรู้ VAT ในสถานการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-136">You can generate the tax invoice or receipt, and realize the VAT, in the following situations:</span></span></p>
<ul>
<li><span data-ttu-id="896ea-137">คุณลงรายการบัญชีใบสั่งขายหรือใบแจ้งหนี้ข้อความอิสระ และสร้างใบกำกับภาษีหรือใบเสร็จรับเงิน หลังจากที่คุณได้รับการชำระเงินจากลูกค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="896ea-137">You post a sales order or free text invoice, and generate the tax invoice or receipt, after you receive the payment from the customer.</span></span> <span data-ttu-id="896ea-138">คุณสามารถบันทึก VAT ของการขายที่รับรู้ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="896ea-138">You can record the realized sales VAT directly.</span></span></li>
<li><span data-ttu-id="896ea-139">คุณกลับรายการ VAT ของการขายที่ยังไม่รับรู้ และลงรายการบัญชี VAT ของการขายที่รับรู้ หลังจากที่คุณส่งใบกำกับภาษีหรือใบเสร็จรับเงินให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="896ea-139">You reverse the unrealized sales VAT and post the realized sales VAT after you send the tax invoice or receipt to the customer.</span></span> <span data-ttu-id="896ea-140">คุณสามารถสร้างใบกรับหรือใบกำกับภาษีหรือใบเสร็จรับเงินเมื่อคุณชำระเงินตามใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-140">You can generate the tax invoice or receipt when you settle the payment with the invoice.</span></span></li>
<li><span data-ttu-id="896ea-141">คุณสร้างและลงรายการบัญชีบันทึกเดบิตและใบลดหนี้จากใบสั่งขายและใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="896ea-141">You create and post debit and credit notes from sales orders and free text invoices.</span></span> <span data-ttu-id="896ea-142">เมื่อคุณลงรายการบัญชีบันทึกเดบิตหรือใบลดหนี้ จะมีการลงรายการบัญชีเฉพาะ VAT ของการขายที่รับรู้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="896ea-142">When you post the debit or credit notes, only the realized sales VAT is posted.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="set-up-unrealized-vat-and-realized-vat"></a><span data-ttu-id="896ea-143">ตั้งค่า VAT ที่ยังไม่รับรู้และ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-143">Set up unrealized VAT and realized VAT</span></span>

1. <span data-ttu-id="896ea-144">ไปที่ **ภาษี** > **พารามิเตอร์** > **ตั้งค่า** > **พารามิเตอร์บัญชีแยกประเภททั่วไป** และตรวจสอบให้แน่ใจว่าตัวเลือก **จัดการ VAT ที่รับรู้และยังไม่รับรู้** ได้รับการตั้งค่าเป็น **ใช่** และได้ตั้งค่าฟิลด์ **วิธีการคํานวณ** เป็น **รวม**</span><span class="sxs-lookup"><span data-stu-id="896ea-144">Go to **Tax** > **Parameters** > **Setup** > **General ledger parameters**, and make sure that the **Manage realized and unrealized VAT** option is set to **Yes**, and that the **Calculation method** field is set to **Total**.</span></span>

2. <span data-ttu-id="896ea-145">ไปที่ **ภาษี** > **การตั้งค่า** > **ภาษีขาย** > **กลุ่มการลงรายการบัญชีแยกประเภท** และตั้งค่ากลุ่มการลงรายการบัญชีแยกประเภทให้กับ VAT ที่ยังไม่รับรู้และ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-145">Go to **Tax** > **Setup** > **Sales tax** > **Ledger posting groups**, and set up ledger posting groups for unrealized VAT and realized VAT.</span></span> <span data-ttu-id="896ea-146">ตัวอย่างเช่น สร้างกลุ่มการลงรายการบัญชีแยกประเภทสองกลุ่ม คือ **UVAT** สำหรับ VAT ที่ยังไม่รับรู้ และ **VAT** VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-146">For example, create two ledger posting groups: **UVAT** for unrealized VAT and **VAT** for realized VAT.</span></span>

    <span data-ttu-id="896ea-147">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่ากลุ่มการลงรายการบัญชีแยกประเภทสำหรับภาษีขาย](../general-ledger/tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-147">For more information, see [Set up Ledger posting groups for sales tax](../general-ledger/tasks/set-up-ledger-posting-groups-sales-tax.md).</span></span>

3. <span data-ttu-id="896ea-148">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **รหัสภาษีขาย** และตั้งค่ารหัสภาษีขายให้กับ VAT ที่ยังไม่รับรู้และ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-148">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax codes**, and set up sales tax codes for unrealized VAT and realized VAT.</span></span> <span data-ttu-id="896ea-149">ตัวอย่างเช่น สร้างรหัสภาษีขายสองตัว คือ **UVAT** สำหรับ VAT ที่ยังไม่รับรู้ และ **VAT** VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-149">For example, create two sales tax codes: **UVAT** for unrealized VAT and **VAT** for realized VAT.</span></span>

    > [!NOTE]
    > <span data-ttu-id="896ea-150">สำหรับรหัสภาษีขายสองตัว ฟิลด์ **ชนิดภาษี** ควรตั้งเป็น **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="896ea-150">For both sales tax codes, the **Tax type** field should beset to **Normal**.</span></span>

4. <span data-ttu-id="896ea-151">สำหรับรหัสภาษีขายแต่ละตัว ในฟิลด์ **กลุ่มการลงรายการบัญชีแยกประเภท** ให้เลือกกลุ่มการลงรายการบัญชีแยกประเภทที่เกี่ยวข้องซึ่งคุณสร้างขึ้นในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="896ea-151">For each sales tax code, in the **Ledger posting group** field, select the corresponding ledger posting group that you created in step 2.</span></span>

5. <span data-ttu-id="896ea-152">สำหรับรหัสภาษีขายสำหรับ VAT ที่ยังไม่รับรู้ ในฟิลด์ **การชำระเงินรหัสภาษีขาย** เลือกรหัสภาษีขายที่สอดคล้องกันของ VAT ที่รับรู้ เพื่อเปิดใช้งาน VAT ที่ยังไม่รับรู้ที่จะกลับรายการเป็น VAT ที่รับรู้เมื่อมีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="896ea-152">For the sales tax code for unrealized VAT, in the **Payment sales tax code** field, select the corresponding sales tax code for realized VAT to enable unrealized VAT to be reversed to realized VAT at the time of payment.</span></span>

    <span data-ttu-id="896ea-153">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่ารหัสภาษีขาย](../general-ledger/tasks/set-up-sales-tax-codes.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-153">For more information, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).</span></span>

6. <span data-ttu-id="896ea-154">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **กลุ่มภาษีขาย** และตั้งค่ากลุ่มภาษีขายให้กับ VAT ที่ยังไม่รับรู้และ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-154">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax groups**, and set up sales tax groups for unrealized VAT and realized VAT.</span></span>

7. <span data-ttu-id="896ea-155">ไปที่ **ภาษี** > **ภาษีทางอ้อม** > **ภาษีขาย** > **กลุ่มภาษีขายตามประเภทสินค้า** และตั้งค่ากลุ่มภาษีขายให้กับ VAT ที่ยังไม่รับรู้และ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-155">Go to **Tax** > **Indirect taxes** > **Sales tax** > **Item sales tax groups**, and set up item sales tax groups for unrealized VAT and realized VAT.</span></span>

8. <span data-ttu-id="896ea-156">กำหนดรหัสภาษีขายให้กับกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="896ea-156">Assign sales tax codes to sales tax groups and item sales tax groups.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="896ea-157">เมื่อต้องการป้องกันไม่ให้ทั้ง VAT ที่ยังไม่รับรู้และ VAT ที่รับรู้ถูกคํานวณในเรกคอร์ดเดียวกัน ให้ตรวจสอบให้แน่ใจว่าได้เพิ่มรหัสภาษีขายเฉพาะในกลุ่มภาษีขายหรือกลุ่มภาษีขายตามประเภทสินค้าที่มีภาษีชนิดเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="896ea-157">To prevent both unrealized VAT and realized VAT from being calculated for the same record, be sure to add the sales tax codes only to the sales tax group or item sales tax group that has the same tax type.</span></span> <span data-ttu-id="896ea-158">ตัวอย่างเช่น เพิ่มรหัสภาษีขายให้กับ VAT ที่ยังไม่รับรู้เฉพาะในกลุ่มภาษีขายหรือกลุ่มภาษีขายตามประเภทสินค้าของ VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-158">For example, add the sales tax codes for unrealized VAT only to the sales tax group or item sales tax group for unrealized VAT.</span></span>

<span data-ttu-id="896ea-159">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าภาษีขาย ให้ดูที่ [ภาพรวมของภาษีขาย](../general-ledger/indirect-taxes-overview.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-159">For more information about how to set up sales taxes, see [Sales tax overview](../general-ledger/indirect-taxes-overview.md).</span></span>

## <a name="working-with-unrealized-and-realized-sales-vat"></a><span data-ttu-id="896ea-160">การทำงานกับ VAT ขายที่ยังไม่รับรู้และที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-160">Working with unrealized and realized sales VAT</span></span>

### <a name="create-and-post-a-sales-order-or-free-text-invoice-that-has-unrealized-vat"></a><span data-ttu-id="896ea-161">สร้างและลงรายการบัญชีใบสั่งขายหรือใบแจ้งหนี้ข้อความอิสระที่มี VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-161">Create and post a sales order or free text invoice that has unrealized VAT</span></span>

<span data-ttu-id="896ea-162">หากคุณไม่ได้รับการชำระเงินจากลูกค้า ให้สร้างและลงรายการบัญชีใบแจ้งหนี้การขายที่มี VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-162">If you didn't receive the payment from the customer, create and post a sales invoice that has unrealized VAT.</span></span> <span data-ttu-id="896ea-163">เมื่อคุณสร้างใบสั่งขายหรือใบแจ้งหนี้ข้อความอิสระ บนแท็บด่วน **รายละเอียดของรายการ** ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** และ **กลุ่มภาษีขาย** ให้เลือกกลุ่มภาษีขายที่เกี่ยวข้องซึ่งคุณสร้างขึ้นก่อนหน้านี้ให้กับ VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-163">When you create a sales order or free text invoice, on the **Line details** FastTab, in the **Item sales tax group** and **Sales tax group** fields, select the corresponding sales tax groups that you created earlier for unrealized VAT.</span></span> <span data-ttu-id="896ea-164">จากนั้นลงรายการบัญชีใบสั่งขายหรือใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="896ea-164">Then post the sales order or free text invoice.</span></span>

<span data-ttu-id="896ea-165">เมื่อคุณลงรายการบัญชีใบสั่งขายก่อนที่คุณจะได้รับการชำระเงินจากลูกค้า VAT ขายที่ยังไม่รับรู้จะถูกลงรายการบัญชีไปยังบัญชี VAT ขายที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-165">When you post the sales order before you receive the payment from the customer, the unrealized sales VAT is posted to the unrealized sales VAT account.</span></span> <span data-ttu-id="896ea-166">ตัวอย่างเช่น ถ้าคุณวางใบสั่งขายของสินค้าที่มีมูลค่า 100 บาท (THB) และมี VAT ที่ยังไม่รับรู้ จะมีการลงรายการบัญชีธุรกรรมดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-166">For example, if you place a sales order for goods that is worth 100 Thai bahts (THB) and has unrealized VAT, the following transaction is posted.</span></span>

| <span data-ttu-id="896ea-167">**ชื่อบัญชี**</span><span class="sxs-lookup"><span data-stu-id="896ea-167">**Account name**</span></span> | <span data-ttu-id="896ea-168">**จำนวนเงินในสกุลเงินของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="896ea-168">**Amount in transaction currency**</span></span> |
|-------------------------|-------------------------|
| <span data-ttu-id="896ea-169">การขาย วัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="896ea-169">Sales - Raw materials</span></span> | <span data-ttu-id="896ea-170">-100.00</span><span class="sxs-lookup"><span data-stu-id="896ea-170">-100.00</span></span> |
| <span data-ttu-id="896ea-171">เจ้าหนี้ VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-171">Unrealized VAT payable</span></span> | <span data-ttu-id="896ea-172">-7.00</span><span class="sxs-lookup"><span data-stu-id="896ea-172">-7.00</span></span> |
| <span data-ttu-id="896ea-173">ลูกหนี้การค้า ภายในประเทศ</span><span class="sxs-lookup"><span data-stu-id="896ea-173">Trade Receivables - Domestic</span></span> | <span data-ttu-id="896ea-174">107.00</span><span class="sxs-lookup"><span data-stu-id="896ea-174">107.00</span></span> |


> [!NOTE]
> <span data-ttu-id="896ea-175">หากคุณได้รับการชำระเงินสำหรับการขายจากลูกค้าแล้ว ให้เลือกกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าสำหรับ VAT ที่รับรู้ ในฟิลด์ **กลุ่มภาษีขาย** และ **กลุ่มภาษีขายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="896ea-175">If you already received the payment for the sale from the customer, select the sales tax group and item sales tax group for realized VAT in the **Sales tax group** and **Item sales tax group** fields.</span></span>

### <a name="settle-a-customer-transaction-to-generate-a-tax-invoice-or-receipt-and-reverse-posted-unrealized-sales-vat"></a><span data-ttu-id="896ea-176">ชำระธุรกรรมลูกค้าเพื่อสร้างใบกำกับภาษีหรือใบเสร็จรับเงิน และกลับรายการ VAT การขายที่ยังไม่รับรู้ที่ลงรายการบัญชีไว้</span><span class="sxs-lookup"><span data-stu-id="896ea-176">Settle a customer transaction to generate a tax invoice or receipt and reverse posted unrealized sales VAT</span></span>

<span data-ttu-id="896ea-177">หลังจากที่คุณได้รับการชำระเงินจากลูกค้าแล้ว ให้ลงรายการบัญชีการชำระเงินของลูกค้าในหน้า **สมุดรายวันการชำระเงินของลูกค้า** และจับคู่กับใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="896ea-177">After you receive the payment from the customer, post the customer payment on the **Customer payment journal** page, and settle it to the sales invoice.</span></span> <span data-ttu-id="896ea-178">หลังจากลงรายการบัญชีสมุดรายวันและจับคู่การชำระเงินกับใบแจ้งหนี้แล้ว VAT ของการขายที่ยังไม่รับรู้จะถูกกลับรายการ และหมายเลขใบกำกับภาษีจะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="896ea-178">After the journal is posted and the payment is settled to the invoice, the unrealized sales VAT is reversed, and a tax invoice number is automatically generated.</span></span>

<span data-ttu-id="896ea-179">หลังจากที่คุณกลับรายการ VAT ของการขายที่ยังไม่รับรู้ ธุรกรรมภาษีต่อไปนี้จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="896ea-179">After you reverse the unrealized sales VAT, the following tax transactions are generated.</span></span>

| <span data-ttu-id="896ea-180">**แหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="896ea-180">**Source**</span></span> | <span data-ttu-id="896ea-181">**รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="896ea-181">**Sales tax code**</span></span> | <span data-ttu-id="896ea-182">**จำนวนเงินเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="896ea-182">**Amount origin**</span></span> | <span data-ttu-id="896ea-183">**ยอดภาษีขายที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="896ea-183">**Calculated sales tax amount**</span></span> | <span data-ttu-id="896ea-184">**เลขที่ใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-184">**Tax invoice number**</span></span> | <span data-ttu-id="896ea-185">**วันที่ในใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-185">**Tax invoice date**</span></span> | <span data-ttu-id="896ea-186">**วันที่รับใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-186">**Tax invoice receipt date**</span></span> |
|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| <span data-ttu-id="896ea-187">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="896ea-187">Sales order</span></span> | <span data-ttu-id="896ea-188">UVAT</span><span class="sxs-lookup"><span data-stu-id="896ea-188">UVAT</span></span> | <span data-ttu-id="896ea-189">1000.00</span><span class="sxs-lookup"><span data-stu-id="896ea-189">1000.00</span></span> | <span data-ttu-id="896ea-190">70.00</span><span class="sxs-lookup"><span data-stu-id="896ea-190">70.00</span></span> |  |  |  |
| <span data-ttu-id="896ea-191">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="896ea-191">Voucher</span></span> | <span data-ttu-id="896ea-192">UVAT</span><span class="sxs-lookup"><span data-stu-id="896ea-192">UVAT</span></span> | <span data-ttu-id="896ea-193">-1000.00</span><span class="sxs-lookup"><span data-stu-id="896ea-193">-1000.00</span></span> | <span data-ttu-id="896ea-194">-70.00</span><span class="sxs-lookup"><span data-stu-id="896ea-194">-70.00</span></span> |  |  |  |
| <span data-ttu-id="896ea-195">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="896ea-195">Voucher</span></span> | <span data-ttu-id="896ea-196">VAT</span><span class="sxs-lookup"><span data-stu-id="896ea-196">VAT</span></span> | <span data-ttu-id="896ea-197">1000.00</span><span class="sxs-lookup"><span data-stu-id="896ea-197">1000.00</span></span> | <span data-ttu-id="896ea-198">70.00</span><span class="sxs-lookup"><span data-stu-id="896ea-198">70.00</span></span> | <span data-ttu-id="896ea-199">THMF-000006</span><span class="sxs-lookup"><span data-stu-id="896ea-199">THMF-000006</span></span> | <span data-ttu-id="896ea-200">วันที่ 12/2/2020</span><span class="sxs-lookup"><span data-stu-id="896ea-200">12/2/2020</span></span> | <span data-ttu-id="896ea-201">วันที่ 12/3/2020</span><span class="sxs-lookup"><span data-stu-id="896ea-201">12/3/2020</span></span> |


> [!NOTE]
> <span data-ttu-id="896ea-202">คุณยังสามารถจับคู่การชำระเงินกับใบแจ้งหนี้จากหน้า **จับคู่ธุรกรรมที่เปิดไว้**</span><span class="sxs-lookup"><span data-stu-id="896ea-202">You can also settle the payment to the invoice from the **Settle open transactions** page.</span></span>

<span data-ttu-id="896ea-203">คุณต้องพิมพ์ใบกำกับภาษีก่อนที่จะทำการชำระเงินและชำระธุรกรรมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="896ea-203">You must print a tax invoice before you make the payment and settle the customer transaction.</span></span>

<span data-ttu-id="896ea-204">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีป้อนและจับคู่การการชำระเงินของลูกค้า โปรดดูที่ [ภาพรวมการชำระเงินของลูกค้า](../cash-bank-management/tasks/customer-payment-overview.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-204">For more information about how to enter and settle customer payments, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

<span data-ttu-id="896ea-205">คุณสามารถสร้างรายงาน **VAT การขาย** ซึ่งรวมธุรกรรมที่มี VAT ขายที่รับรู้แล้ว และรวมรายละเอียดของ VAT ที่นิติบุคคลได้รับสำหรับการขายสินค้าและบริการ</span><span class="sxs-lookup"><span data-stu-id="896ea-205">You can generate the **Sales VAT** report, which includes the realized sales VAT transactions together with the details of the VAT that the legal entity receives for the sales of goods and services.</span></span> <span data-ttu-id="896ea-206">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [รายงานภาษีขาย](apac-tha-sales-vat-report.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-206">For more information, see [Sales tax reports](apac-tha-sales-vat-report.md).</span></span>

## <a name="working-with-unrealized-and-realized-purchase-vat"></a><span data-ttu-id="896ea-207">การทำงานกับ VAT ซื้อที่ยังไม่รับรู้และที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-207">Working with unrealized and realized purchase VAT</span></span>

### <a name="create-and-post-a-purchase-order-that-has-unrealized-vat"></a><span data-ttu-id="896ea-208">สร้างและลงรายการบัญชีใบสั่งซื้อที่มี VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-208">Create and post a purchase order that has unrealized VAT</span></span>

<span data-ttu-id="896ea-209">หากคุณไม่ได้รับใบกำกับภาษีสำหรับการซื้อจากผู้จัดจำหน่าย ให้สร้างใบสั่งซื้อที่มี VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-209">If you didn't receive the tax invoice for the purchase from the vendor, create a purchase order that has unrealized VAT.</span></span> <span data-ttu-id="896ea-210">เมื่อคุณสร้างใบสั่งซื้อ บนแท็บด่วน **รายละเอียดของรายการ** บนแท็บ **การตั้งค่า** ในส่วน **ภาษีขาย** ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** และ **กลุ่มภาษีขาย** ให้เลือกกลุ่มภาษีขายที่เกี่ยวข้องซึ่งคุณสร้างขึ้นก่อนหน้านี้ให้กับ VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-210">When you create a purchase order, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, in the **Item sales tax group** and **Sales tax group** fields, select the corresponding sales tax groups that you created earlier for unrealized VAT.</span></span>

<span data-ttu-id="896ea-211">เมื่อคุณลงรายการบัญชีใบสั่งซื้อก่อนที่คุณจะได้รับใบกำกับภาษีจากผู้จัดจำหน่าย VAT ซื้อที่ยังไม่รับรู้จะถูกลงรายการบัญชีไปยังบัญชี VAT ซื้อที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-211">When you post the purchase order before you receive the tax invoice from the vendor, the unrealized purchase VAT is posted to the unrealized purchase VAT account.</span></span> <span data-ttu-id="896ea-212">ตัวอย่างเช่น ถ้าคุณวางใบสั่งซื้อของสินค้าที่มีมูลค่า 100 บาท (THB) และมี VAT ที่ยังไม่รับรู้ จะมีการลงรายการบัญชีธุรกรรมดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-212">For example, if you place a purchase order for goods that is worth 100 THB and has unrealized VAT, the following transaction is posted.</span></span>

| <span data-ttu-id="896ea-213">**ชื่อบัญชี**</span><span class="sxs-lookup"><span data-stu-id="896ea-213">**Account name**</span></span> | <span data-ttu-id="896ea-214">**จำนวนเงินในสกุลเงินของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="896ea-214">**Amount in transaction currency**</span></span> |
|-------------------------|-------------------------|
| <span data-ttu-id="896ea-215">ใบรับวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="896ea-215">Raw Materials Receipts</span></span> | <span data-ttu-id="896ea-216">100.00</span><span class="sxs-lookup"><span data-stu-id="896ea-216">100.00</span></span> |
| <span data-ttu-id="896ea-217">บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-217">Accounts Payable</span></span> | <span data-ttu-id="896ea-218">-107.00</span><span class="sxs-lookup"><span data-stu-id="896ea-218">-107.00</span></span> |
| <span data-ttu-id="896ea-219">ลูกหนี้ VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-219">Unrealized VAT receivable</span></span> | <span data-ttu-id="896ea-220">7.00 น.</span><span class="sxs-lookup"><span data-stu-id="896ea-220">7.00</span></span> |


> [!NOTE]
> <span data-ttu-id="896ea-221">หากคุณได้รับใบกำกับภาษีสำหรับการซื้อจากผู้จัดจำหน่ายแล้ว ให้เลือกกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าสำหรับ VAT ที่รับรู้ ในฟิลด์ **กลุ่มภาษีขาย** และ **กลุ่มภาษีขายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="896ea-221">If you already received the tax invoice for the purchase from the vendor, select the sales tax group and item sales tax group for realized VAT in the **Sales tax group** and **Item sales tax group** fields.</span></span> <span data-ttu-id="896ea-222">เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย ให้ป้อนหมายเลขใบกำกับภาษีที่คุณได้รับจากผู้จัดจำหน่ายในฟิลด์ **หมายเลขใบกำกับภาษี** ให้ป้อนวันที่ที่ผู้จัดจำหน่ายสร้างใบกำกับภาษีในฟิลด์ **วันที่ในใบกำกับภาษี** และป้อนวันที่เมื่อคุณได้รับใบกำกับภาษีจากผู้จัดจำหน่ายในฟิลด์ **วันที่รับสินค้าตามใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-222">When you post the vendor invoice, enter the number of the tax invoice that you received from the vendor in the **Tax invoice number** field, enter the date when the vendor generated the tax invoice in the **Tax invoice date** field, and enter the date when you received the tax invoice from the vendor in the **Tax invoice receipt date** field.</span></span>

### <a name="create-and-post-a-vendor-invoice-journal-that-has-unrealized-vat"></a><span data-ttu-id="896ea-223">สร้างและลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่ายที่มี VAT ขายที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-223">Create and post a vendor invoice journal that has unrealized VAT</span></span>

<span data-ttu-id="896ea-224">หากคุณไม่ได้รับใบกำกับภาษีจากธุรกรรมค่าใช้จ่ายบริการจากผู้จัดจำหน่าย ให้สร้างสมุดรายวันใบแจ้งหนี้จากผู้จัดจำหน่ายที่มี VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-224">If you didn't receive the tax invoice for the service expense transaction from the vendor, create a vendor invoice journal that has unrealized VAT.</span></span> <span data-ttu-id="896ea-225">เมื่อคุณสร้างบรรทัด บนแท็บ **ทั่วไป** ให้เลือกกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าสำหรับ VAT ที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-225">When you create a line, on the **General** tab, select the sales tax group and item sales tax group for unrealized VAT.</span></span> <span data-ttu-id="896ea-226">มีการลงรายการบัญชี VAT ของการซื้อที่ยังไม่รับรู้ไปยังบัญชี VAT ของการซื้อที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-226">The unrealized purchase VAT is posted to the unrealized purchase VAT account.</span></span>

<span data-ttu-id="896ea-227">หากคุณลงรายการบัญชีธุรกรรมค่าใช้จ่ายบริการหลังจากที่คุณได้รับใบกำกับภาษีจากผู้จัดจำหน่าย บนแท็บ **ทั่วไป** ให้เลือกกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าของ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-227">If you post the service expense transaction after you receive the tax invoice from the vendor, on the **General** tab, select the sales tax group and item sales tax group for the realized VAT.</span></span> <span data-ttu-id="896ea-228">จากนั้น บนแท็บ **ใบแจ้งหนี้** ในส่วน **เอกสาร** ให้ป้อนรายละเอียดใบกำกับภาษี</span><span class="sxs-lookup"><span data-stu-id="896ea-228">Then, on the **Invoice** tab, in the **Document** section, enter the tax invoice details.</span></span> <span data-ttu-id="896ea-229">มีการลงรายการบัญชี VAT ของการซื้อที่รับรู้ไปยังบัญชี VAT ของการซื้อ</span><span class="sxs-lookup"><span data-stu-id="896ea-229">The realized purchase VAT is posted to the purchase VAT account.</span></span>

<span data-ttu-id="896ea-230">คุณสามารถสร้างรายงาน **มูลค่าส่วนที่เหลือของ VAT ซื้อที่ยังไม่รับรู้** ซึ่งประกอบด้วยธุรกรรมที่มีภาษีที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-230">You can generate the **Purchase Unrealized VAT Remaining** report, which includes the transactions that have unrealized tax.</span></span> <span data-ttu-id="896ea-231">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [รายงานภาษีขาย](apac-tha-sales-vat-report.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-231">For more information, see [Sales tax reports](apac-tha-sales-vat-report.md).</span></span>

### <a name="reverse-the-unrealized-purchase-vat"></a><span data-ttu-id="896ea-232">กลับรายการ VAT ซื้อที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-232">Reverse the unrealized purchase VAT</span></span>

<span data-ttu-id="896ea-233">กระบวนการในการกลับรายการ VAT ซื้อที่ยังไม่รับรู้จะแตกต่างกันไป ขึ้นอยู่กับเมื่อคุณได้รับใบกำกับภาษีจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="896ea-233">The process for reversing the unrealized purchase VAT varies, depending on when you receive the tax invoice from the vendor.</span></span>

- <span data-ttu-id="896ea-234">หากคุณได้รับใบกำกับภาษีเมื่อคุณลงรายการบัญชีใบสั่งซื้อ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-234">If you receive the tax invoice when you post the purchase order, follow these steps:</span></span>

    1. <span data-ttu-id="896ea-235">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="896ea-235">Create a purchase order.</span></span> <span data-ttu-id="896ea-236">บนแท็บด่วน **รายละเอียดของรายการ** บนแท็บ **การตั้งค่า** ในส่วน **ภาษีขาย** ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** **กลุ่ม** และ **กลุ่มภาษีขาย** ให้เลือกกลุ่มภาษีขายที่เกี่ยวข้องให้กับ VAT ที่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-236">On the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, in the **Item sales tax** **group** and **Sales tax group** fields, select the corresponding sales tax group for realized VAT.</span></span>
    
    2. <span data-ttu-id="896ea-237">สร้างใบแจ้งหนี้ของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="896ea-237">Generate an invoice for the order.</span></span> <span data-ttu-id="896ea-238">บนแท็บด่วน **ส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย** ให้ตั้งค่าฟิลด์ **หมายเลขใบกำกับภาษี** **วันที่ในใบกำกับภาษี** และ **วันที่รับสินค้าในใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-238">On the **Vendor invoice header** FastTab, set the **Tax invoice number**, **Tax invoice date**, and **Tax invoice receipt date** fields.</span></span>

- <span data-ttu-id="896ea-239">หากคุณได้รับใบกำกับภาษีเมื่อคุณลงรายการบัญชีสมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย ในหน้า **การจ่ายภาษีให้แก่ผู้จัดจำหน่าย** บนแท็บด่วน **การชำระเงิน** ให้ตั้งค่า **หมายเลขใบกำกับภาษี** **วันที่ในใบกำกับภาษี** และฟิลด์ **วันที่รับสินค้าตามใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-239">If you receive the tax invoice when you post the Vendor payment journal: On the **Vendor payments** page, on the **Payment** FastTab, set the **Tax invoice number**, **Tax invoice date**, and **Tax invoice receipt date** fields.</span></span>

- <span data-ttu-id="896ea-240">หากคุณได้รับใบกำกับภาษีหลังจากที่คุณได้ชำระเงินและจับคู่รายการใบแจ้งหนี้แล้ว ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="896ea-240">If you receive the tax invoice after you've made the payment and settled the invoice, follow these steps:</span></span>

    1.  <span data-ttu-id="896ea-241">ไปที่ **บัญชีเจ้าหนี้** > **การชำระเงิน** > **กลับรายการ VAT ที่ยังไม่รับรู้**</span><span class="sxs-lookup"><span data-stu-id="896ea-241">Go to **Accounts payable** > **Payments** > **Reverse unrealized VAT**.</span></span>

    2.  <span data-ttu-id="896ea-242">บนบานหน้าต่างการดำเนินการ บนแท็บ **สมุดรายวันการกลับรายการ** ในกลุ่ม **ใหม่** ให้เลือก **สมุดรายวันการกลับรายการ**</span><span class="sxs-lookup"><span data-stu-id="896ea-242">On the Action Pane, on the **Reversal journal** tab, in the **New** group, select **Reversal journal**.</span></span>

    3.  <span data-ttu-id="896ea-243">เลือกเงื่อนไขที่จะรวมสมุดรายวันการชำระเงินที่ไม่ได้รับรู้ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="896ea-243">Select criteria to include the payment journals that aren't realized, and then select **OK**.</span></span>

    4.  <span data-ttu-id="896ea-244">เลือกค่า **รหัสการกลับรายการผู้จัดจำหน่ายที่ยังไม่รับรู้** ของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="896ea-244">Select the **Vendor unrealized reversal ID** value of the journal.</span></span> <span data-ttu-id="896ea-245">หรือเลือกบรรทัดของสมุดรายวัน จากนั้นบนบานหน้าต่างการดำเนินการ บนแท็บ **สมุดรายวันการกลับรายการ** ในกลุ่ม **รักษา** ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="896ea-245">Alternatively, select the line for the journal, and then, on the Action Pane, on the **Reversal journal** tab, in the **Maintain** group, select **Edit**.</span></span>

    5.  <span data-ttu-id="896ea-246">ใช้ฟิลด์ **ทำเครื่องหมาย** เพื่อเลือกธุรกรรมที่ได้รับใบกำกับภาษีและต้องกลับรายการ VAT ของการซื้อที่ยังไม่รับรู้</span><span class="sxs-lookup"><span data-stu-id="896ea-246">Use the **Mark** field to select the transactions that the tax invoice was received for, and that the unrealized purchase VAT must be reversed for.</span></span>

    6.  <span data-ttu-id="896ea-247">บนแท็บด่วน **ส่วนหัวของสมุดรายวันการกลับรายการ** ให้ตั้งค่าฟิลด์ **หมายเลขใบกำกับภาษี** **วันที่ในใบกำกับภาษี** และ **วันที่รับสินค้าในใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-247">On the **Reversal journal header** FastTab, set the **Tax invoice number**, **Tax invoice date**, and **Tax invoice receipt date** fields.</span></span>

    7.  <span data-ttu-id="896ea-248">บนบานหน้าต่างการดำเนินการ บนแท็บ **สมุดรายวันการกลับรายการ** ในกลุ่ม **รักษา** ให้เลือก **ลงรายการบัญชี** เพื่อลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="896ea-248">On the Action Pane, on the **Reversal journal** tab, in the **Maintain** group, select **Post** to post the journal.</span></span>

        ![หน้าสมุดรายวันการกลับรายการ](media/apac_tha_reversal_journal_page.png)

<span data-ttu-id="896ea-250">หลังจากที่คุณกลับรายการ VAT ซื้อที่ยังไม่รับรู้ ธุรกรรมภาษีต่อไปนี้จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="896ea-250">After you reverse the unrealized purchase VAT, the following tax transactions will be present.</span></span>

| <span data-ttu-id="896ea-251">**แหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="896ea-251">**Source**</span></span> | <span data-ttu-id="896ea-252">**รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="896ea-252">**Sales tax code**</span></span> | <span data-ttu-id="896ea-253">**จำนวนเงินเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="896ea-253">**Amount origin**</span></span> | <span data-ttu-id="896ea-254">**ยอดภาษีขายที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="896ea-254">**Calculated sales tax amount**</span></span> | <span data-ttu-id="896ea-255">**เลขที่ใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-255">**Tax invoice number**</span></span> | <span data-ttu-id="896ea-256">**วันที่ในใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-256">**Tax invoice date**</span></span> | <span data-ttu-id="896ea-257">**วันที่รับใบกำกับภาษี**</span><span class="sxs-lookup"><span data-stu-id="896ea-257">**Tax invoice receipt date**</span></span> |
|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| <span data-ttu-id="896ea-258">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="896ea-258">Purchase order</span></span> | <span data-ttu-id="896ea-259">UVAT</span><span class="sxs-lookup"><span data-stu-id="896ea-259">UVAT</span></span> | <span data-ttu-id="896ea-260">75.00</span><span class="sxs-lookup"><span data-stu-id="896ea-260">75.00</span></span> | <span data-ttu-id="896ea-261">5.25</span><span class="sxs-lookup"><span data-stu-id="896ea-261">5.25</span></span> |  |  |  |
| <span data-ttu-id="896ea-262">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="896ea-262">Voucher</span></span> | <span data-ttu-id="896ea-263">UVAT</span><span class="sxs-lookup"><span data-stu-id="896ea-263">UVAT</span></span> | <span data-ttu-id="896ea-264">-75.00</span><span class="sxs-lookup"><span data-stu-id="896ea-264">-75.00</span></span> | <span data-ttu-id="896ea-265">-5.25</span><span class="sxs-lookup"><span data-stu-id="896ea-265">-5.25</span></span> |  |  |  |
| <span data-ttu-id="896ea-266">ใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="896ea-266">Voucher</span></span> | <span data-ttu-id="896ea-267">VAT</span><span class="sxs-lookup"><span data-stu-id="896ea-267">VAT</span></span> | <span data-ttu-id="896ea-268">75.00</span><span class="sxs-lookup"><span data-stu-id="896ea-268">75.00</span></span> | <span data-ttu-id="896ea-269">5.25</span><span class="sxs-lookup"><span data-stu-id="896ea-269">5.25</span></span> | <span data-ttu-id="896ea-270">TH-0004</span><span class="sxs-lookup"><span data-stu-id="896ea-270">TH-0004</span></span> | <span data-ttu-id="896ea-271">วันที่ 12/2/2020</span><span class="sxs-lookup"><span data-stu-id="896ea-271">12/2/2020</span></span> | <span data-ttu-id="896ea-272">วันที่ 12/3/2020</span><span class="sxs-lookup"><span data-stu-id="896ea-272">12/3/2020</span></span> |


<span data-ttu-id="896ea-273">มีการลงรายการบัญชี VAT ของการซื้อที่รับรู้ไปยังบัญชี VAT ของการซื้อ</span><span class="sxs-lookup"><span data-stu-id="896ea-273">The realized purchase VAT is posted to the purchase VAT account.</span></span>

<span data-ttu-id="896ea-274">คุณสามารถสร้างรายงาน **VAT ซื้อ** ซึ่งรวมธุรกรรมที่มี VAT ซื้อที่รับรู้แล้ว และรวมรายละเอียดของ VAT ที่นิติบุคคลจะต้องจ่ายในการซื้อสินค้าและบริการ</span><span class="sxs-lookup"><span data-stu-id="896ea-274">You can generate the **Purchase VAT** report, which includes the realized purchase VAT transactions together with the details of the VAT that the legal entity must pay for the purchase of goods and services.</span></span> <span data-ttu-id="896ea-275">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [รายงานภาษีขาย](apac-tha-sales-vat-report.md)</span><span class="sxs-lookup"><span data-stu-id="896ea-275">For more information, see [Sales tax reports](apac-tha-sales-vat-report.md).</span></span>

