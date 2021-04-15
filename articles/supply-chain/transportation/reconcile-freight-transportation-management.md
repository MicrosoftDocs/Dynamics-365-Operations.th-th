---
title: กระทบยอดการขนส่งในการจัดการการขนส่ง
description: หัวข้อนี้อธิบายถึงกระบวนการกระทบยอดค่าขนส่ง
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809097"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="a9050-103">กระทบยอดการขนส่งในการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a9050-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9050-104">หัวข้อนี้อธิบายถึงกระบวนการกระทบยอดค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a9050-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="a9050-105">การกระทบยอดการขนส่งสามารถทำได้ด้วยตนเอง หรือคุณสามารถตั้งค่าให้เกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9050-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="a9050-106">เมื่อต้องการใช้การกระทบยอดการขนส่งโดยอัตโนมัติ คุณจะต้องตั้งค่าต้นแบบการตรวจสอบซึ่งคุณสามารถกำหนดเงื่อนไขที่เป็นตัวกำหนดว่าจะจับคู่บิลการขนส่งใดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9050-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="a9050-107">กระบวนการกระทบยอดการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a9050-107">The freight reconciliation process</span></span>

<span data-ttu-id="a9050-108">อัตราค่าขนส่งจะถูกคำนวณโดยกลไกจัดการอัตราที่เชื่อมโยงกับผู้ขนส่งสินค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a9050-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="a9050-109">เมื่อโหลดได้รับการยืนยันแล้ว จะมีการสร้างบิลค่าขนส่ง และอัตราค่าขนส่งจะถูกโอนย้ายไป</span><span class="sxs-lookup"><span data-stu-id="a9050-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="a9050-110">อัตราค่าขนส่งจะถูกแบ่งเป็นค่าธรรมเนียมเบ็ดเตล็ดของเอกสารต้นทางที่เกี่ยวข้อง (ใบสั่งซื้อ ใบสั่งขาย และ/หรือใบสั่งโอนย้าย) ขึ้นอยู่กับการตั้งค่าที่ใช้สำหรับกระบวนการเรียกเก็บเงินทั่วไป</span><span class="sxs-lookup"><span data-stu-id="a9050-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="a9050-111">กระบวนการกระทบยอดการขนส่ง (ซึ่งเรียกว่ากระบวนการจับคู่) สามารถเริ่มต้นได้ทันทีที่ใบแจ้งหนี้ค่าขนส่งจากผู้ขนส่งสินค้ามาถึง</span><span class="sxs-lookup"><span data-stu-id="a9050-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="a9050-112">ใบแจ้งหนี้อาจได้รับทางอิเล็กทรอนิกส์หรือแบบกระดาษ</span><span class="sxs-lookup"><span data-stu-id="a9050-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="a9050-113">ถ้าได้รับใบแจ้งหนี้แบบกระดาษ คุณสามารถสร้างใบแจ้งหนี้ทางอิเล็กทรอนิกส์ได้โดยใช้บิลค่าขนส่งเป็นแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="a9050-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="a9050-114">[![กระบวนการกระทบยอดการขนส่ง](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="a9050-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="a9050-115">การกระทบยอดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a9050-115">Manual reconciliation</span></span>

<span data-ttu-id="a9050-116">ถ้าคุณกำลังกระทบยอดการขนส่งด้วยตนเอง คุณต้องจับคู่แต่ละบรรทัดในใบแจ้งหนี้กับบรรทัดในบิลค่าขนส่งของโหลดที่มีการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a9050-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="a9050-117">คุณทำการจับคู่นี้ได้ที่หน้า **การจับคู่บิลค่าขนส่งและใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="a9050-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="a9050-118">ถ้าจำนวนเงินในบรรทัดในใบแจ้งหนี้ไม่ตรงกับจำนวนเงินในบิลค่าขนส่ง คุณต้องเลือกเหตุผลการกระทบยอดของจำนวนเงินที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="a9050-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="a9050-119">ถ้ามีเหตุผลของการกระทบยอดหลายเหตุผล คุณสามารถแบ่งจำนวนเงินที่ไม่ตรงกันสำหรับแต่ละเหตุผลได้</span><span class="sxs-lookup"><span data-stu-id="a9050-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="a9050-120">เหตุผลของการกระทบยอดเป็นตัวกำหนดวิธีการลงรายการบัญชียอดผลต่างในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a9050-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="a9050-121">เมื่อมีการพิจารณาการกระทบยอดของจำนวนเงินทั้งหมดในใบแจ้งหนี้ จะถูกส่งเพื่อขอการอนุมัติ และจากนั้นจะมีการลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a9050-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="a9050-122">ภาพประกอบต่อไปนี้แสดงวิธีการสร้างใบแจ้งหนี้ค่าขนส่งและการทำการกระทบยอดค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a9050-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="a9050-123">[![งานการกระทบยอดค่าขนส่ง](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="a9050-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="a9050-124">การกระทบยอดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9050-124">Automatic reconciliation</span></span>

<span data-ttu-id="a9050-125">เมื่อต้องการใช้การกระทบยอดอัตโนมัติ คุณต้องระบุกำหนดการสำหรับการกระทบยอด และใบแจ้งหนี้และผู้ขนส่งสินค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="a9050-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="a9050-126">การจับคู่รายการใบแจ้งหนี้และบิลค่าขนส่งจะเสร็จสิ้นตามการตั้งค่าของชนิดต้นแบบการตรวจสอบและบิลค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a9050-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="a9050-127">หลังจากที่คุณรันการกระทบยอดอัตโนมัติ คุณต้องจัดการกับใบแจ้งหนี้ใดๆ ที่ระบบไม่สามารถจับคู่ได้</span><span class="sxs-lookup"><span data-stu-id="a9050-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="a9050-128">จากนั้นคุณต้องประมวลผลใบแจ้งหนี้เหล่านี้ด้วยตนเองก่อนที่คุณจะสามารถลงรายการบัญชีใบแจ้งหนี้ทั้งหมดสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a9050-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="a9050-129">จับคู่บิลการขนส่งกับใบแจ้งหนี้ค่าขนส่งโดยใช้การกระทบยอดอัตโนมัติหรือด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a9050-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="a9050-130">*การจับคู่* เป็นกระบวนการค้นหาบิลการขนส่งที่ตรงกับใบแจ้งหนี้ค่าขนส่งแต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="a9050-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="a9050-131">ซึ่งสามารถทำได้โดยการจับคู่บรรทัดใบแจ้งหนี้แบบทีละรายการ (การจับคู่ด้วยตนเอง) หรือจับคู่ใบแจ้งหนี้ที่พร้อมใช้งานทั้งหมดพร้อมกัน (การจับคู่อัตโนมัติ)</span><span class="sxs-lookup"><span data-stu-id="a9050-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="a9050-132">การจับคู่อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9050-132">Auto matching</span></span>

<span data-ttu-id="a9050-133">เมื่อจับคู่ใบแจ้งหนี้ค่าขนส่งหลายใบกับบิลการขนส่งเดียวกัน กระบวนการจับคู่อัตโนมัติจะทำงานได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="a9050-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="a9050-134">ใบแจ้งหนี้ค่าขนส่งทั้งหมดที่ไม่ได้จับคู่จะเรียงลำดับตามจํานวนเงินที่มีจํานวนสูงสุดก่อน</span><span class="sxs-lookup"><span data-stu-id="a9050-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="a9050-135">ใบแจ้งหนี้ค่าขนส่งจะตรงกันแบบทีละใบ จนกว่าบิลการขนส่งจะไม่มียอดเงินค่าบวกคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="a9050-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="a9050-136">ทั้งนี้ขึ้นอยู่กับการตั้งค่าต้นแบบการตรวจสอบและยอดเงินคงเหลือในใบแจ้งหนี้ค่าขนส่ง มีการตั้งค่ายอดคงเหลือในใบแจ้งหนี้ค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a9050-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="a9050-137">การจับคู่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a9050-137">Manual matching</span></span>

<span data-ttu-id="a9050-138">บิลการขนส่งทั้งหมดที่มียอดเงินค่าบวกจะพร้อมใช้งานในการจับคู่</span><span class="sxs-lookup"><span data-stu-id="a9050-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="a9050-139">คล้ายกับการจับคู่อัตโนมัติ ผู้ใช้จะสามารถจับคู่ใบแจ้งหนี้การขนส่งกับยอดเงินค่าลบกับบิลการขนส่งไม่ตรงกันอย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a9050-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="a9050-140">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a9050-140">Example</span></span>

<span data-ttu-id="a9050-141">สมมติว่าคุณมีบิลการขนส่ง (FB) เป็นจํานวนเงิน 1500 และคุณได้สร้างใบแจ้งหนี้ค่าขนส่งสามใบให้กับบิลการขนส่งที่มีรายการใบแจ้งหนี้หนึ่งรายการต่อหนึ่งใบที่มีการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a9050-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="a9050-142">บิลการขนส่งเดิม (FB): ยอดเงิน 1500</span><span class="sxs-lookup"><span data-stu-id="a9050-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="a9050-143">ใบแจ้งหนี้ 1 (Inv1): ยอดเงิน 1000</span><span class="sxs-lookup"><span data-stu-id="a9050-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="a9050-144">ใบแจ้งหนี้ 2 (Inv2): ยอดเงิน 600</span><span class="sxs-lookup"><span data-stu-id="a9050-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="a9050-145">ใบแจ้งหนี้ 3 (Inv3): ยอดเงิน -100</span><span class="sxs-lookup"><span data-stu-id="a9050-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="a9050-146">ผลลัพธ์การจับคู่อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9050-146">Automatic matching result</span></span>

<span data-ttu-id="a9050-147">การจับคู่อัตโนมัติจะปฏิบัติการตามลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a9050-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="a9050-148">เรียงลำดับใบแจ้งหนี้ค่าขนส่งทั้งหมดจากมากไปน้อยตามยอดเงิน: Inv1 -> Inv2 -> Inv3</span><span class="sxs-lookup"><span data-stu-id="a9050-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="a9050-149">จับคู่ Inv1 กับ FB</span><span class="sxs-lookup"><span data-stu-id="a9050-149">Match Inv1 with FB.</span></span> <span data-ttu-id="a9050-150">Inv1 มีการจับคู่ 1000 รายการและ FB มียอดคงเหลือ 500 รายการ ดังนั้นสถานะถูกตั้งค่าเป็น *ตรงกันบางส่วน*</span><span class="sxs-lookup"><span data-stu-id="a9050-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="a9050-151">จับคู่ Inv2 กับ FB</span><span class="sxs-lookup"><span data-stu-id="a9050-151">Match Inv2 with FB.</span></span> <span data-ttu-id="a9050-152">Inv2 มีการจับคู่ 500 รายการและ FB มียอดคงเหลือ 0 รายการ ดังนั้นสถานะถูกตั้งค่าเป็น *ตรงกันทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="a9050-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="a9050-153">เนื่องจากขณะนี้ FB ตรงกันอย่างสมบูรณ์ แล้ว Inv3 จะไม่มีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="a9050-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="a9050-154">ผลลัพธ์การจับคู่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="a9050-154">Manual matching result</span></span>

<span data-ttu-id="a9050-155">สำหรับการจับคู่ด้วยตนเอง ผลลัพธ์จะแตกต่างกันไปโดยขึ้นอยู่กับลำดับของการจับคู่ ดังที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a9050-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="a9050-156">กรณีการจับคู่ด้วยตนเอง 1</span><span class="sxs-lookup"><span data-stu-id="a9050-156">Manual matching case 1</span></span>

<span data-ttu-id="a9050-157">วิธีการหนึ่งในการจับคู่ด้วยตนเองจากตัวอย่างนี้จะดําเนินการต่อไปดังนี้</span><span class="sxs-lookup"><span data-stu-id="a9050-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="a9050-158">จับคู่ FB กับ Inv1</span><span class="sxs-lookup"><span data-stu-id="a9050-158">Match FB with Inv1.</span></span> <span data-ttu-id="a9050-159">FB มียอดคงเหลือ 500 รายการ ดังนั้นสถานะถูกตั้งค่าเป็น *ตรงกันบางส่วน*</span><span class="sxs-lookup"><span data-stu-id="a9050-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="a9050-160">จับคู่ Inv2 กับ FB</span><span class="sxs-lookup"><span data-stu-id="a9050-160">Match Inv2 with FB.</span></span> <span data-ttu-id="a9050-161">Inv2 มีการจับคู่ 500 รายการและ FB มียอดคงเหลือ 0 รายการ ดังนั้นสถานะถูกตั้งค่าเป็น *ตรงกันทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="a9050-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="a9050-162">เมื่อจับคู่ Inv3 ด้วยตนเอง คุณจะไม่พบบิลการขนส่งที่ไม่ตรงกันใดๆ</span><span class="sxs-lookup"><span data-stu-id="a9050-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="a9050-163">กรณีนี้ต้องเหมือนกับการจับคู่อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a9050-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="a9050-164">กรณีการจับคู่ด้วยตนเอง 2</span><span class="sxs-lookup"><span data-stu-id="a9050-164">Manual matching case 2</span></span>

<span data-ttu-id="a9050-165">อีกวิธีการหนึ่งในการจับคู่ด้วยตนเองจากตัวอย่างนี้จะดําเนินการต่อไปดังนี้</span><span class="sxs-lookup"><span data-stu-id="a9050-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="a9050-166">จับคู่ Inv3 กับ FB.</span><span class="sxs-lookup"><span data-stu-id="a9050-166">Match Inv3 with FB.</span></span> <span data-ttu-id="a9050-167">ขณะนี้ FB มียอดเงินคงเหลือ 1600 ซึ่งเหมือนกับหักลบค่าลบ 100 จาก 1500</span><span class="sxs-lookup"><span data-stu-id="a9050-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="a9050-168">ทั้ง FB และ Inv3 มีปริมาณที่จับคู่เท่ากับ -100</span><span class="sxs-lookup"><span data-stu-id="a9050-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="a9050-169">จับคู่ Inv1 และ Inv 2 กับ FB ทีละรายการ</span><span class="sxs-lookup"><span data-stu-id="a9050-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="a9050-170">FB ตรงกันอย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a9050-170">FB is fully matched.</span></span>

<span data-ttu-id="a9050-171">ตามตัวอย่างนี้แสดง ควรจับคู่ใบแจ้งหนี้ค่าขนส่งกับยอดเงินค่าลบด้วยตนเองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a9050-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="a9050-172">การสิ่งนี้จะตรวจสอบให้แน่ใจว่าสามารถจับคู่ใบแจ้งหนี้ค่าขนส่งกับยอดเงินค่าลบกับบิลการขนส่งที่ไม่ตรงกันอย่างสมบูรณ์ เนื่องจากช่วยให้คุณสามารถควบคุมลำดับการจับคู่ได้</span><span class="sxs-lookup"><span data-stu-id="a9050-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]