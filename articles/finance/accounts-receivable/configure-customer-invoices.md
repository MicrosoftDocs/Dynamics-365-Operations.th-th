---
title: สร้างใบแจ้งหนี้ของลูกค้า
description: '**ใบแจ้งหนี้ของลูกค้าสำหรับใบสั่งขาย** คือใบตราที่เกี่ยวข้องกับการขาย และที่ทางองค์กรให้กับลูกค้า'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f5b9866fc7afba205b84b372c6a204ec4c8f64d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448280"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="92547-103">สร้างใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="92547-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92547-104">**ใบแจ้งหนี้ของลูกค้าสำหรับใบสั่งขาย** คือใบตราที่เกี่ยวข้องกับการขาย และที่ทางองค์กรให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="92547-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="92547-105">ชนิดของใบแจ้งหนี้ของลูกค้านี้ถูกสร้างขึ้นตามใบสั่งขาย ซึ่งรวมรายการใบสั่งและหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="92547-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="92547-106">ต้องมีการระบุและลงรายการบัญชีหมายเลขสินค้าในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="92547-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="92547-107">รายการสมุดรายวันของบัญชีแยกประเภทย่อยไม่พร้อมใช้งานสำหรับใบแจ้งหนี้ของลูกค้าสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="92547-108">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างใบแจ้งหนี้สำหรับใบสั่งขาย](tasks/create-sales-order-invoices.md)</span><span class="sxs-lookup"><span data-stu-id="92547-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="92547-109">**ใบแจ้งหนี้ข้อความอิสระ** ไม่เกี่ยวข้องกับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="92547-110">ประกอบด้วยรายการใบสั่งที่รวมถึงบัญชีแยกประเภท คำอธิบายข้อความอิสระ และยอดขายที่คุณป้อนด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="92547-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="92547-111">คุณไม่สามารถป้อนหมายเลขสินค้าบนใบแจ้งหนี้ชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="92547-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="92547-112">คุณต้องป้อนข้อมูลภาษีขายที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="92547-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="92547-113">บัญชีหลักสำหรับการขายจะระบุอยู่ในแต่ละรายการใบแจ้งหนี้ ซึ่งคุณสามารถกระจายไปยังบัญชีแยกประเภทหลายบัญชี โดยการคลิก **กระจายยอดเงิน** ในหน้า **ใบแจ้งหนี้ข้อความอิสระ**</span><span class="sxs-lookup"><span data-stu-id="92547-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="92547-114">นอกจากนี้ ยอดดุลลูกค้าจะมีการลงรายการบัญชีไปยังบัญชีสรุปจากโพรไฟล์การลงบัญชีที่ใช้สำหรับใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="92547-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="92547-115">สำหรับข้อมูลเพิ่มเติม โปรดดูที่:</span><span class="sxs-lookup"><span data-stu-id="92547-115">For more information see:</span></span>

[<span data-ttu-id="92547-116">สร้างใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="92547-116">Create free text invoices</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="92547-117">สร้างเท็มเพลตใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="92547-117">Create a free text invoice template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="92547-118">กำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="92547-118">Assign free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="92547-119">สร้างและลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="92547-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="92547-120">**ใบแจ้งหนี้ชั่วคราว** คือใบแจ้งหนี้ซึ่งเตรียมไว้เป็นการประเมินยอดเงินใบแจ้งหนี้จริงก่อนการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="92547-121">คุณสามารถพิมพ์ใบแจ้งหนี้ชั่วคราวสำหรับใบแจ้งหนี้ของลูกค้า สำหรับใบสั่งขาย หรือใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="92547-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="92547-122">ลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ของลูกค้าแต่ละใบตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="92547-123">ใช้ขั้นตอนนี้เพื่อสร้างใบแจ้งหนี้ตามใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="92547-124">คุณอาจดำเนินการนี้ถ้าคุณตัดสินใจที่จะออกใบแจ้งหนี้ลูกค้าก่อนที่คุณจัดส่งสินค้าหรือบริการ</span><span class="sxs-lookup"><span data-stu-id="92547-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="92547-125">เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** สำหรับสินค้าแต่ละรายการมีการอัพเดตด้วยยอดรวมของปริมาณใบแจ้งหนี้จากใบสั่งขายที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92547-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="92547-126">ถ้าทั้งทั้งคู่ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** และปริมาณ **ยอดค้างส่ง** สำหรับสินค้าทั้งหมดในใบสั่งขายเป็น 0 (ศูนย์) สถานะของใบสั่งขายจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="92547-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="92547-127">ถ้าปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** ไม่ใช่ 0 (ศูนย์) สถานะของใบสั่งขายยังคงไม่เปลี่ยนแปลง และสามารถป้อนใบแจ้งหนี้เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="92547-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="92547-128">คุณสามารถดูสถานะของใบสั่งขายในหน้ารายการ **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="92547-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="92547-129">ใช้หน้ารายการ **ใบแจ้งหนี้ของลูกค้าที่เปิด** เพื่อดูใบแจ้งหนี้ที่คุณลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="92547-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="92547-130">การลงรายการบัญชีและพิมพ์ใบแจ้งหนี้ของลูกค้าแต่ละใบตามบันทึกการจัดส่งและวันที่</span><span class="sxs-lookup"><span data-stu-id="92547-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="92547-131">ใช้กระบวนการนี้เมื่อบันทึกการจัดส่งอย่างน้อยหนึ่งได้ถูกลงรายการบัญชีสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="92547-132">ใบแจ้งหนี้ของลูกค้าจะขึ้นอยู่กับบันทึกการจัดส่งเหล่านี้และจะสะท้อนถึงปริมาณจากบันทึกเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="92547-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="92547-133">ข้อมูลทางการเงินสำหรับใบแจ้งหนี้จะขึ้นอยู่กับข้อมูลที่ป้อนเมื่อคุณลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="92547-134">คุณสามารถสร้างใบแจ้งหนี้ของลูกค้าที่ยึดตามรายการบันทึกการจัดส่งสินค้าที่ได้มีการส่งจนถึงวันนี้ แม้ว่าสินค้าทั้งหมดสำหรับใบสั่งขายหนึ่ง ๆ ยังไม่ได้จัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="92547-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="92547-135">คุณอาจดำเนินการนี้ถ้า ตัวอย่างเช่น นิติบุคคลของคุณออกใบแจ้งหนี้หนึ่งต่อลูกค้าต่อเดือนที่ครอบคลุมการจัดส่งทั้งหมดที่คุณส่งระหว่างเดือน</span><span class="sxs-lookup"><span data-stu-id="92547-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="92547-136">แต่ละบันทึกการจัดส่งแสดงถึงการจัดส่งสินค้าบางส่วนหรือทั้งหมดของสินค้าในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="92547-137">เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** สำหรับสินค้าแต่ละรายการมีการอัพเดตด้วยยอดรวมของปริมาณที่จัดส่งจากบันทึกการจัดส่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92547-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="92547-138">ถ้าทั้งคู่ปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** และปริมาณ **ยอดค้างส่ง** สำหรับสินค้าทั้งหมดในใบสั่งขายเป็น 0 (ศูนย์) สถานะของใบสั่งขายจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="92547-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="92547-139">ถ้าปริมาณ **ยอดคงเหลือในใบแจ้งหนี้** ไม่ใช่ 0 (ศูนย์) สถานะของใบสั่งขายยังคงไม่เปลี่ยนแปลง และสามารถป้อนใบแจ้งหนี้เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="92547-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="92547-140">ธุรกรรมสินค้าคงคลังมีการอัพเดตด้วยหมายเลขใบแจ้งหนี้ และสถานะฟิลด์ **สถานะของรายการ** ในใบสั่งขายจะเปลี่ยนเป็น **ออกใบแจ้งหนี้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="92547-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="92547-141">ดูสถานะของใบสั่งขายในหน้ารายการ **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="92547-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="92547-142">รวมใบสั่งขายหรือบันทึกการจัดส่งสำหรับการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="92547-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="92547-143">ใช้ขั้นตอนนี้เมื่อใบสั่งขายหนึ่งรายการขึ้นไปพร้อมจะออกใบแจ้งหนี้แล้ว และคุณต้องการรวมไว้ในใบแจ้งหนี้เดียว</span><span class="sxs-lookup"><span data-stu-id="92547-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="92547-144">คุณสามารถเลือกใบแจ้งหนี้หลายใบในหน้ารายการ **ใบสั่งขาย** และจากนั้นใช้ **สร้างใบแจ้งหนี้** เพื่อรวม</span><span class="sxs-lookup"><span data-stu-id="92547-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="92547-145">ในหน้า  **การลงรายการบัญชีใบแจ้งหนี้** คุณสามารถเปลี่ยนการตั้งค่า **ใบสั่งโดยสรุป** เพื่อสรุปตามหมายเลขใบสั่ง (ที่มีหลายบันทึกการจัดส่งสำหรับใบสั่งขายหนึ่ง ๆ) หรือตามบัญชีใบแจ้งหนี้ (ที่มีใบสั่งขายหลายใบสำหรับบัญชีใบแจ้งหนี้เดียว)</span><span class="sxs-lookup"><span data-stu-id="92547-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="92547-146">ใช้ปุ่ม **จัดเรียง** เพื่อรวมใบสั่งขายลงในใบแจ้งหนี้เดียว ตามการตั้งค่า **ใบสั่งโดยสรุป**</span><span class="sxs-lookup"><span data-stu-id="92547-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="92547-147">การตั้งค่าเพิ่มเติมที่เปลี่ยนแปลงพฤติกรรมการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="92547-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="92547-148">ฟิลด์ต่อไปนี้เปลี่ยนแปลงกระบวนการพฤติกรรมการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="92547-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92547-149">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="92547-149">Field</span></span></th>
<th><span data-ttu-id="92547-150">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="92547-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92547-151">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="92547-151">Quantity</span></span></td>
<td><span data-ttu-id="92547-152">เลือกปริมาณเพื่อใช้เป็นพื้นฐานของการลงรายการบัญชีของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="92547-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="92547-153">ตัวเลือกที่พร้อมใช้งานจะแตกต่างกันไป ขึ้นอยู่กับชนิดของเอกสารที่คุณกำลังลงรายการบัญชี เช่นบันทึกการจัดส่งหรือใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="92547-154"><strong>จัดส่งทันที</strong> – เลือกปริมาณทั้งหมดที่ป้อนในฟิลด์ <strong>จัดส่งทันที</strong></span><span class="sxs-lookup"><span data-stu-id="92547-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="92547-155">ใช้ตัวเลือกนี้เพื่อยืนยันหรือส่งใบสั่งเป็นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="92547-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="92547-156"><strong>เบิกสินค้าแล้ว</strong> – เลือกปริมาณทั้งหมดที่มีการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="92547-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="92547-157"><strong>ทั้งหมด</strong> – เลือกปริมาณทั้งหมดในใบสั่งขายที่ยังไม่ได้รับการปรับปรุงโดยชนิดเอกสารปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92547-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="92547-158"><strong>บันทึกการจัดส่ง</strong> – เลือกปริมาณทั้งหมดที่อัพเดตแล้วตามบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="92547-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="92547-159"><strong>ปริมาณที่เลือกและผลิตภัณฑ์ที่ไม่ได้สต็อค</strong> – เลือกปริมาณทั้งหมดที่ได้ถูกเลือกและปริมาณผลิตภัณฑ์ทั้งหมดที่ไม่ได้ถูกสต็อค</span><span class="sxs-lookup"><span data-stu-id="92547-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92547-160">การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="92547-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="92547-161">เลือกตัวเลือกนี้เพื่อบันทึกบัญชีใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="92547-162">ล้างตัวเลือกนี้เพื่อพิมพ์ใบสั่งขายชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="92547-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="92547-163"><strong>หมายเหตุ:</strong> ถ้าคุณทำข้อตกลงสำหรับกำหนดการชำระเงิน กำหนดการชำระเงินจะไม่ถูกแสดงบนใบสั่งขาย pro forma</span><span class="sxs-lookup"><span data-stu-id="92547-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="92547-164">กำหนดการชำระเงินจะแสดงบนใบสั่งขายจริงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92547-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92547-165">การเลือกหลังสุด</span><span class="sxs-lookup"><span data-stu-id="92547-165">Late selection</span></span></td>
<td><span data-ttu-id="92547-166">เลือกตัวเลือกนี้เพื่อใช้การสอบถามที่เลือกในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="92547-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="92547-167">ตัวเลือกนี้ใช้สำหรับชุดงาน</span><span class="sxs-lookup"><span data-stu-id="92547-167">This option is used for batch jobs.</span></span> <span data-ttu-id="92547-168">แบบสอบถามจะรันเมื่อชุดงานรัน</span><span class="sxs-lookup"><span data-stu-id="92547-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92547-169">ลดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="92547-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="92547-170">เลือกตัวเลือกนี้เพื่อลดปริมาณที่จัดส่งเมื่อเอกสารถูกลงรายการบัญชีอัตโนมัติ เพื่อให้ปริมาณที่ส่งเท่ากับสินค้าคงคลังที่มี</span><span class="sxs-lookup"><span data-stu-id="92547-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92547-171">พิมพ์</span><span class="sxs-lookup"><span data-stu-id="92547-171">Print</span></span></td>
<td><span data-ttu-id="92547-172">เลือกเวลาที่จะพิมพ์เอกสาร</span><span class="sxs-lookup"><span data-stu-id="92547-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="92547-173"><strong>ปัจจุบัน</strong> – พิมพ์เอกสารหลังจากแต่ละใบแจ้งหนี้มีการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="92547-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="92547-174"><strong>หลังจาก</strong> – พิมพ์เอกสารหลังจากกใบแจ้งหนี้ทั้งหมดมีการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="92547-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="92547-175">
<strong>หมายเหตุ:</strong> ฟิลด์ <strong>พิมพ์</strong> จะพร้อมใช้งานเมื่อคุณเลือกเท่านั้นการพิมพ์ <strong>พิมพ์ใบแจ้งหนี้</strong> <strong>พิมพ์การยืนยัน</strong> <strong>พิมพ์รายการเบิกสินค้า</strong> หรือตัวเลือก <strong>พิมพ์บันทึกการจัดส่ง</strong></span><span class="sxs-lookup"><span data-stu-id="92547-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="92547-176">ตัวอย่างเช่น ในหน้า <strong>การเรียงลำดับแบบฟอร์ม</strong> คุณตั้งค่าระบบให้เรียงลำดับข้อมูลตามบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="92547-177">คุณสามารถเลือก <strong>หลังจาก</strong> การพิมพ์เอกสารในชุดงานที่จะเรียงลำดับตามบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="92547-178">มิฉะนั้น เอกสารจะถูกพิมพ์ก่อนการประมวลผลเสร็จสิ้น และเอกสารจะไม่ถูกจัดเรียงตามลำดับที่ระบุในหน้า <strong>การจัดเรียงฟอร์ม</strong></span><span class="sxs-lookup"><span data-stu-id="92547-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92547-179">พิมพ์ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-179">Print invoice</span></span></td>
<td><span data-ttu-id="92547-180">เลือกตัวเลือกนี้เพื่อพิมพ์ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="92547-180">Select this option to print the invoice.</span></span> <span data-ttu-id="92547-181">ถ้าตัวเลือกนี้ปิดอยู่ คุณสามารถลงรายการใบแจ้งหนี้โดยไม่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="92547-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92547-182">ส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="92547-182">Send e-mail</span></span></td>
<td><span data-ttu-id="92547-183">เลือกตัวเลือกนี้เพื่อส่งใบแจ้งหนี้สำหรับใบสั่งขายไปยังลูกค้าตามอีเมลที่แนบหลังจากมีการลงรายการบัญชีใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="92547-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="92547-184">สิ่งที่แนบจะมีการส่งเป็นไฟล์ PDF และ XML</span><span class="sxs-lookup"><span data-stu-id="92547-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="92547-185">ตัวเลือกนี้จะพร้อมใช้งานเมื่อคุณเลือกเท่านั้นตัวเลือก <strong>เปิดใช้งาน CFD (ใบแจ้งหนี้อิเล็กทรอนิกส์)</strong> หน้า <strong>พารามิเตอร์ใบแจ้งหนี้อิเล็กทรอนิกส์ </strong></span><span class="sxs-lookup"><span data-stu-id="92547-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="92547-186"><strong>หมายเหตุ:</strong> (MEX) ตัวควบคุมนี้สามารถใช้ได้เฉพาะกับนิติบุคคลที่มีที่อยู่หลักอยู่ในเม็กซิโกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92547-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92547-187">ใช้ปลายทางการจัดการงานพิมพ์</span><span class="sxs-lookup"><span data-stu-id="92547-187">Use print management destination</span></span></td>
<td><span data-ttu-id="92547-188">เลือกตัวเลือกนี้เพื่อใช้การตั้งค่าการพิมพ์ที่ระบุไว้สำหรับธุรกรรม เอกสาร หรือโมดูลใน ในหน้า <strong>การตั้งค่าการจัดการพิมพ์</strong></span><span class="sxs-lookup"><span data-stu-id="92547-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92547-189">ตรวจสอบวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="92547-189">Check credit limit</span></span></td>
<td><span data-ttu-id="92547-190">เลือกข้อมูลที่ควรจะวิเคราะห์ เมื่อดำเนินการตรวจสอบวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="92547-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="92547-191"><strong>ไม่มี</strong> – ไม่มีข้อกำหนดสำหรับการตรวจสอบวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="92547-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="92547-192"><strong>ยอดดุล</strong> – มีการตรวจสอบวงเงินสินเชื่อเทียบกับยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="92547-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="92547-193"><strong>ยอดดุล + บันทึกการจัดส่งหรือใบรับสินค้า</strong>– มีการตรวจสอบวงเงินสินเชื่อเทียบกับยอดดุลลูกค้า การจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="92547-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="92547-194"><strong>ยอดดุล+ทั้งหมด</strong> – มีการตรวจสอบวงเงินสินเชื่อเทียบกับยอดดุลลูกค้า การจัดส่ง และใบสั่งที่เปิด</span><span class="sxs-lookup"><span data-stu-id="92547-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92547-195">การแก้ไขสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="92547-195">Credit correction</span></span></td>
<td><span data-ttu-id="92547-196">เลือกตัวเลือกนี้ เพื่อแสดงใบลดหนี้เป็นเดบิตในธุรกรรมใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="92547-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92547-197">ลงเครดิตปริมาณที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="92547-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="92547-198">ถ้าคุณกำลังลงรายการบัญชีใบลดหนี้ เลือกตัวเลือกนี้เพื่อรักษาปริมาณคงเหลือในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="92547-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="92547-199">ถ้าไม่ได้เลือกตัวเลือกนี้ ปริมาณคงเหลือจะตั้งเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="92547-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92547-200">อัพเดตบทสรุปสำหรับ</span><span class="sxs-lookup"><span data-stu-id="92547-200">Summary update for</span></span></td>
<td><span data-ttu-id="92547-201">เลือกวิธีใบสั่งขายหลายใบที่ควรสรุป</span><span class="sxs-lookup"><span data-stu-id="92547-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="92547-202"><strong>ไม่มี</strong> – ห้ามสรุปใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="92547-203">ตัวอย่างเช่น ใบแจ้งหนี้ที่แยกต่างหากจะถูกสร้างสำหรับแต่ละใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="92547-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="92547-204"><strong>บัญชีใบแจ้งหนี้</strong> – สรุปใบสั่งที่เลือกทั้งหมด ตามเงื่อนไขที่ตั้งค่าในหน้า <strong>พารามิเตอร์การอัพเดตบทสรุป</strong></span><span class="sxs-lookup"><span data-stu-id="92547-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="92547-205"><strong>ใบสั่ง</strong> – สรุปช่วงของใบสั่งที่เลือกเป็นใบสั่งเดียวที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="92547-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="92547-206">มีการสรุปใบสั่งตามเงื่อนไขที่ตั้งค่าในหน้า <strong>พารามิเตอร์การอัพเดตบทสรุป</strong></span><span class="sxs-lookup"><span data-stu-id="92547-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="92547-207">ถ้าคุณเลือกตัวเลือกนี้ คุณต้องเลือกค่าในฟิลด์ <strong>ใบสั่งขาย</strong></span><span class="sxs-lookup"><span data-stu-id="92547-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="92547-208"><strong>สรุปอัตโนมัติ</strong>– ถ้ามีการระบุการอัพเดตบทสรุปในหน้า <strong>การอัพเดตบทสรุป</strong> สรุปใบสั่งที่เลือกทั้งหมด ตามเงื่อนไขที่ตั้งค่าในหน้า <strong>พารามิเตอร์การอัพเดตบทสรุป</strong></span><span class="sxs-lookup"><span data-stu-id="92547-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="92547-209">ถ้าการปรับปรุงสรุปไม่ได้ถูกระบุ ลงรายการบัญชีใบสั่งแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="92547-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="92547-210"><strong>บันทึกการจัดส่ง</strong> – สรุปช่วงของใบสั่งที่เลือกเป็นใบแจ้งหนี้หนึ่งฉบับสำหรับบันทึกการจัดส่งแต่ละฉบับ</span><span class="sxs-lookup"><span data-stu-id="92547-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="92547-211">ตัวเลือกนี้จะพร้อมใช้งานเมื่อถ้า <strong>บันทึกการจัดส่ง</strong> มีการเลือกในฟิลด์ <strong>ปริมาณ</strong> เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92547-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





