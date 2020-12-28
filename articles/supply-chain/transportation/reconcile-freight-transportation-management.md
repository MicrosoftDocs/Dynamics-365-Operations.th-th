---
title: กระทบยอดการขนส่งในการจัดการการขนส่ง
description: หัวข้อนี้อธิบายถึงกระบวนการกระทบยอดค่าขนส่ง
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable,TMSFBDetailReconcile,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13fecd5256c7bfc3a27d15482e0fa6200cfd72df
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438951"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="2e0c9-103">กระทบยอดการขนส่งในการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e0c9-104">หัวข้อนี้อธิบายถึงกระบวนการกระทบยอดค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="2e0c9-105">การกระทบยอดการขนส่งสามารถทำได้ด้วยตนเอง หรือคุณสามารถตั้งค่าให้เกิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2e0c9-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="2e0c9-106">เมื่อต้องการใช้การกระทบยอดการขนส่งโดยอัตโนมัติ คุณจะต้องตั้งค่าต้นแบบการตรวจสอบซึ่งคุณสามารถกำหนดเงื่อนไขที่เป็นตัวกำหนดว่าจะจับคู่บิลการขนส่งใดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2e0c9-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="2e0c9-107">กระบวนการกระทบยอดการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-107">The freight reconciliation process</span></span>
<span data-ttu-id="2e0c9-108">อัตราค่าขนส่งจะถูกคำนวณโดยกลไกจัดการอัตราที่เชื่อมโยงกับผู้ขนส่งสินค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="2e0c9-109">เมื่อโหลดได้รับการยืนยันแล้ว จะมีการสร้างบิลค่าขนส่ง และอัตราค่าขนส่งจะถูกโอนย้ายไป</span><span class="sxs-lookup"><span data-stu-id="2e0c9-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="2e0c9-110">อัตราค่าขนส่งจะถูกแบ่งเป็นค่าธรรมเนียมเบ็ดเตล็ดของเอกสารต้นทางที่เกี่ยวข้อง (ใบสั่งซื้อ ใบสั่งขาย และ/หรือใบสั่งโอนย้าย) ขึ้นอยู่กับการตั้งค่าที่ใช้สำหรับกระบวนการเรียกเก็บเงินทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2e0c9-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="2e0c9-111">กระบวนการกระทบยอดการขนส่ง (ซึ่งเรียกว่ากระบวนการจับคู่) สามารถเริ่มต้นได้ทันทีที่ใบแจ้งหนี้ค่าขนส่งจากผู้ขนส่งสินค้ามาถึง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="2e0c9-112">ใบแจ้งหนี้อาจได้รับทางอิเล็กทรอนิกส์หรือแบบกระดาษ</span><span class="sxs-lookup"><span data-stu-id="2e0c9-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="2e0c9-113">ถ้าได้รับใบแจ้งหนี้แบบกระดาษ คุณสามารถสร้างใบแจ้งหนี้ทางอิเล็กทรอนิกส์ได้โดยใช้บิลค่าขนส่งเป็นแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="2e0c9-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="2e0c9-114">[![กระบวนการกระทบยอดการขนส่ง](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="2e0c9-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="2e0c9-115">การกระทบยอดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-115">Manual reconciliation</span></span>
<span data-ttu-id="2e0c9-116">ถ้าคุณกำลังกระทบยอดการขนส่งด้วยตนเอง คุณต้องจับคู่แต่ละบรรทัดในใบแจ้งหนี้กับบรรทัดในบิลค่าขนส่งของโหลดที่มีการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2e0c9-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="2e0c9-117">คุณทำการจับคู่นี้ได้ที่หน้า **การจับคู่บิลค่าขนส่งและใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="2e0c9-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="2e0c9-118">ถ้าจำนวนเงินในบรรทัดในใบแจ้งหนี้ไม่ตรงกับจำนวนเงินในบิลค่าขนส่ง คุณต้องเลือกเหตุผลการกระทบยอดของจำนวนเงินที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="2e0c9-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="2e0c9-119">ถ้ามีเหตุผลของการกระทบยอดหลายเหตุผล คุณสามารถแบ่งจำนวนเงินที่ไม่ตรงกันสำหรับแต่ละเหตุผลได้</span><span class="sxs-lookup"><span data-stu-id="2e0c9-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="2e0c9-120">เหตุผลของการกระทบยอดเป็นตัวกำหนดวิธีการลงรายการบัญชียอดผลต่างในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="2e0c9-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="2e0c9-121">เมื่อมีการพิจารณาการกระทบยอดของจำนวนเงินทั้งหมดในใบแจ้งหนี้ จะถูกส่งเพื่อขอการอนุมัติ และจากนั้นจะมีการลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="2e0c9-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="2e0c9-122">ภาพประกอบต่อไปนี้แสดงวิธีการสร้างใบแจ้งหนี้ค่าขนส่งและการทำการกระทบยอดค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="2e0c9-123">[![งานการกระทบยอดค่าขนส่ง](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="2e0c9-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="2e0c9-124">การกระทบยอดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2e0c9-124">Automatic reconciliation</span></span>
<span data-ttu-id="2e0c9-125">เมื่อต้องการใช้การกระทบยอดอัตโนมัติ คุณต้องระบุกำหนดการสำหรับการกระทบยอด และใบแจ้งหนี้และผู้ขนส่งสินค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="2e0c9-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="2e0c9-126">การจับคู่รายการใบแจ้งหนี้และบิลค่าขนส่งจะเสร็จสิ้นตามการตั้งค่าของชนิดต้นแบบการตรวจสอบและบิลค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2e0c9-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="2e0c9-127">หลังจากที่คุณรันการกระทบยอดอัตโนมัติ คุณต้องจัดการกับใบแจ้งหนี้ใดๆ ที่ระบบไม่สามารถจับคู่ได้</span><span class="sxs-lookup"><span data-stu-id="2e0c9-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="2e0c9-128">จากนั้นคุณต้องประมวลผลใบแจ้งหนี้เหล่านี้ด้วยตนเองก่อนที่คุณจะสามารถลงรายการบัญชีใบแจ้งหนี้ทั้งหมดสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2e0c9-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



