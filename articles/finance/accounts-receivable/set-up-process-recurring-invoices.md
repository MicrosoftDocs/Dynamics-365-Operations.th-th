---
title: ตั้งค่า และประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ
description: บทความนี้อธิบายวิธีการตั้งค่าและประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ คุณสามารถใช้ใบแจ้งหนี้ที่เกิดซ้ำถ้าคุณต้องออกใบแจ้งหนี้ยอดเงินเดียวกันเป็นประจำให้ลูกค้า
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834dc64ce531fb614bc7836e0def16f27ecf5e18
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188649"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="ecdfc-104">ตั้งค่า และประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecdfc-105">บทความนี้อธิบายวิธีการตั้งค่าและประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="ecdfc-106">คุณสามารถใช้ใบแจ้งหนี้ที่เกิดซ้ำถ้าคุณต้องออกใบแจ้งหนี้ยอดเงินเดียวกันเป็นประจำให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ecdfc-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

## <a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="ecdfc-107">สร้างเท็มเพลตสำหรับใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-107">Create a recurring free text invoice template</span></span>

<span data-ttu-id="ecdfc-108">เมื่อมีการออกอินวอยซ์ลูกค้าสำหรับบริการเดียวกันเป็นประจำ คุณต้องกำหนดแม่แบบใบแจ้งหนี้ข้อความอิสระที่สามารถนำมาใช้ใหม่เพื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="ecdfc-109">เท็มเพลต #DEF ประกอบด้วยข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-109">This template contains the following information:</span></span>

-   <span data-ttu-id="ecdfc-110">ข้อมูลหัวข้อ เช่นกลุ่มภาษี เงื่อนไขการชำระเงิน และวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ecdfc-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="ecdfc-111">ข้อมูลรายการ เช่นคำอธิบายการบริการ บัญชีรายได้ ราคาต่อหน่วย และยอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="ecdfc-112">ค่าธรรมเนียมสำหรับการจัดส่งหรือการจัดการ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="ecdfc-113">การกระจายการลงบัญชีพร้อมกับรายละเอียดมิติทางการเงิน เช่นศูนย์ต้นทุนและหน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="ecdfc-114">มีผลบังคับ คุณกำลังสร้างใบแจ้งหนี้ทั้งฉบับ และจะบันทึกเป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ecdfc-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="ecdfc-115">คุณสามารถตั้งค่าเท็มเพลตด้วยการใช้หน้า **ใบแจ้งหนี้ที่เกิดซ้ำ** ได้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="ecdfc-116">กำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระให้กับลูกค้าและป้อนรายละเอียดการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="ecdfc-117">หลังจากที่สร้างเท็มเพลต คุณต้องกำหนดเท็มเพลตให้แก่ลูกค้าที่คุณต้องการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="ecdfc-118">นอกจากนี้ คุณต้องระบุ เมื่อใด และบ่อยเพียงใด เพื่อที่จะใช้ใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="ecdfc-119">คุณสามารถกำหนดเท็มเพลตที่แท็บ **ใบแจ้งหนี้** ที่หน้าของ **ลูกค้า** ได้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="ecdfc-120">เพิ่มเท็มเพลตในรายการ และอัพเดตข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ecdfc-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="ecdfc-121">วันที่เริ่มต้นและ อีกทางหนึ่งคือ วันที่สิ้นสุดสำหรับการเรียกเก็บเงินที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="ecdfc-122">ความถี่ของการเรียกเก็บเงินที่เกิดซ้ำ (ตัวอย่างเช่น ทุกวัน หรือ เดือนละครั้ง)</span><span class="sxs-lookup"><span data-stu-id="ecdfc-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="ecdfc-123">ยอดเงินการเรียกเก็บเงินสูงสุด (ถ้าจำเป็นต้องมีข้อมูลนี้)</span><span class="sxs-lookup"><span data-stu-id="ecdfc-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="ecdfc-124">ลูกค้าสามารถมีเท็มเพลตหลายเท็มเพลต ที่มีความถี่ที่แตกต่าง</span><span class="sxs-lookup"><span data-stu-id="ecdfc-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="ecdfc-125">สร้างใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-125">Generate the recurring invoices</span></span>
<span data-ttu-id="ecdfc-126">ในหน้า **ใบแจ้งหนี้ที่เกิดซ้ำ**, จะมีงานที่ประมวลผลเท็มเพลใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="ecdfc-127">ให้คุณระบุวันที่ในใบแจ้งหนี้และเท็มเพลตในการสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="ecdfc-128">ใบแจ้งหนี้จะถูกสร้างขึ้น และกำหนดหมายเลขรหัสการเกิดซ้ำเดียวสำหรับใบแจ้งหนี้แต่ละกลุ่มที่ถูกประมวลผล</span><span class="sxs-lookup"><span data-stu-id="ecdfc-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

## <a name="post-recurring-free-text-invoices"></a><span data-ttu-id="ecdfc-129">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-129">Post recurring free text invoices</span></span>

<span data-ttu-id="ecdfc-130">หลังจากที่สร้างใบแจ้งหนี้ที่เกิดซ้ำ ใบแจ้งหนี้รหัสการเกิดซ้ำปรากฏในงานการลงรายการบัญชีในหน้า **ใบแจ้งหนี้ที่เกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="ecdfc-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="ecdfc-131">คุณสามารถดูใบแจ้งหนี้ทั้งหมดสำหรับรหัสการเกิดซ้ำ โดยการคลิกลิงค์</span><span class="sxs-lookup"><span data-stu-id="ecdfc-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="ecdfc-132">ในระหว่างการตรวจทานใบแจ้งหนี้สำหรับรหัสการเกิดซ้ำ คุณสามารถลบใบแจ้งหนี้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="ecdfc-133">การตั้งค่าการเกิดซ้ำของลูกค้าจะตั้งค่าสำหรับเท็มเพลตนั้นใหม่ เพื่อที่จะสามารถสร้างใหม่ได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="ecdfc-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="ecdfc-134">คุณสามารถลงรายการบัญชีเดียว มาก หรือทั้งหมดของใบแจ้งหนี้สำหรับรหัสการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="ecdfc-135">ถ้าเปิดใช้งานลำดับงาน คุณต้องคลิก **ส่ง** ก่อนที่คุณสามารถลงรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ecdfc-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

## <a name="print-recurring-free-text-invoices"></a><span data-ttu-id="ecdfc-136">พิมพ์ใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-136">Print recurring free text invoices</span></span>

<span data-ttu-id="ecdfc-137">หลังจากที่ลงรายการบัญชีใบแจ้งหนี้ที่เกิดซ้ำ คุณสามารถพิมพ์ใบแจ้งหนี้จากหน้ารายการใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="ecdfc-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="ecdfc-138">คุณสามารถพิมพ์ใบแจ้งหนี้ที่เลือก หรือคุณสามารถเลือกช่วงของใบแจ้งหนี้ที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="ecdfc-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]