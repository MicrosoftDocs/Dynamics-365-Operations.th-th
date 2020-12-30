---
title: ระบบอัตโนมัติของใบแจ้งหนี้สำหรับเอกสารที่สแกน
description: หัวข้อนี้อธิบายถึงลักษณะการทำงานที่พร้อมใช้งานสำหรับระบบอัตโนมัติตั้งแต่ต้นจนจบของใบแจ้งหนี้ของผู้จัดจำหน่าย แม้แต่ใบแจ้งหนี้ที่มีเอกสารแนบ
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d19d0e10f477e498e8f0fff1f431bc4bfdd9a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448353"
---
# <a name="invoice-automation-for-scanned-documents"></a><span data-ttu-id="826e2-103">ระบบอัตโนมัติของใบแจ้งหนี้สำหรับเอกสารที่สแกน</span><span class="sxs-lookup"><span data-stu-id="826e2-103">Invoice automation for scanned documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="826e2-104">หัวข้อนี้อธิบายถึงลักษณะการทำงานที่พร้อมใช้งานสำหรับระบบอัตโนมัติตั้งแต่ต้นจนจบของใบแจ้งหนี้ของผู้จัดจำหน่าย แม้แต่ใบแจ้งหนี้ที่มีเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="826e2-105">องค์กรที่ต้องการปรับปรุงกระบวนการของบัญชีเจ้าหนี้ (AP) มักจะระบุการประมวลผลใบแจ้งหนี้ให้เป็นหนึ่งในพื้นที่ของกระบวนการอันดับแรกที่ควรมีประสิทธิภาพมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="826e2-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="826e2-106">ในหลายกรณี องค์กรเหล่านี้จะงดการประมวลผลของใบแจ้งหนี้แบบกระดาษให้กับผู้ให้บริการการรู้จำอักขระเชิงแสงของบุคคลที่สาม (OCR)</span><span class="sxs-lookup"><span data-stu-id="826e2-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="826e2-107">พวกเขาจะได้รับข้อมูลเมตาของใบแจ้งหนี้ที่เครื่องสามารถอ่านได้ พร้อมด้วยรูปภาพสแกนของใบแจ้งหนี้แต่ละใบ</span><span class="sxs-lookup"><span data-stu-id="826e2-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="826e2-108">เพื่อช่วยในระบบอัตโนมัติ โซลูชัน "ไมล์ล่าสุด" จึงได้ถูกสร้างขึ้นเพื่อเปิดใช้งานปริมาณการใช้วัตถุเหล่านี้ในระบบออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="826e2-109">ขณะนี้ มีการเปิดใช้งานระบบอัตโนมัติ "ไมล์ล่าสุด" แบบสำเร็จรูป ผ่านโซลูชันระบบอัตโนมัติของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="826e2-110">บริบทของโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="826e2-110">Solution context</span></span>

<span data-ttu-id="826e2-111">โซลูชันระบบอัตโนมัติสำหรับใบแจ้งหนี้เปิดใช้งานอินเทอร์เฟสมาตรฐาน ที่สามารถยอมรับข้อมูลเมตาของใบแจ้งหนี้สำหรับส่วนหัวของใบแจ้งหนี้และรายการของใบแจ้งหนี้ และรวมถึงเอกสารแนบที่เกี่ยวข้องกับใบแจ้งหนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="826e2-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="826e2-112">ระบบภายนอกใดๆ ซึ่งสามารถสร้างอาร์ทิแฟกต์ที่สอดคล้องกับอินเทอร์เฟสนี้ จะสามารถส่งตัวดึงข้อมูลสำหรับการประมวลผลโดยอัตโนมัติของใบแจ้งหนี้และเอกสารแนบได้</span><span class="sxs-lookup"><span data-stu-id="826e2-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="826e2-113">ภาพประกอบต่อไปนี้แสดงสถานการณ์จำลองการรวมของตัวอย่างซึ่ง Contoso ได้ร่วมมือกับผู้ให้บริการ OCR สำหรับการประมวลผลใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="826e2-114">ผู้จัดจำหน่ายของ Contoso ส่งใบแจ้งหนี้ไปยังผู้ให้บริการทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="826e2-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="826e2-115">ผ่านการประมวลผล OCR ผู้ให้บริการสร้างข้อมูลเมตาของใบแจ้งหนี้ (ส่วนหัวและ/หรือรายการ) และรูปภาพสแกนของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="826e2-116">จากนั้นชั้นของการรวมจะแปลงอาร์ทิแฟกต์เหล่านี้ เพื่อให้สามารถนำไปใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="826e2-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![สถานการณ์จำลองการรวมของตัวอย่าง](media/vendor_invoice_automation_01.png)

<span data-ttu-id="826e2-118">การเปลี่ยนแปลงหลากหลายรูปแบบของสถานการณ์จำลองก่อนหน้านี้จะเป็นไปได้ ถ้าจำเป็นต้องมีการรวมใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="826e2-119">การย้ายข้อมูลเป็นกรณีการใช้อีกแบบหนึ่ง ที่ซึ่งสามารถใช้อินเทอร์เฟสนี้เพื่อสร้างใบแจ้งหนี้และเอกสารแนบได้</span><span class="sxs-lookup"><span data-stu-id="826e2-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="826e2-120">ส่วนประกอบของโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="826e2-120">Solution components</span></span>

<span data-ttu-id="826e2-121">รอยเท้าคาร์บอนของโซลูชันประกอบด้วยส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="826e2-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="826e2-122">เอนทิตีข้อมูลสำหรับส่วนหัวของใบแจ้งหนี้ รายการใบแจ้งหนี้ และเอกสารแนบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="826e2-123">ข้อยกเว้นในการประมวลผลสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="826e2-124">ตัวแสดงเอกสารแนบแบบเคียงข้างกันในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="826e2-125">ส่วนที่เหลือของหัวข้อนี้ให้คำอธิบายโดยละเอียดของส่วนประกอบของโซลูชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="826e2-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="826e2-126">เอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="826e2-126">Data entities</span></span>

<span data-ttu-id="826e2-127">แพคเกจข้อมูลคือหน่วยของงานที่ต้องถูกส่ง เพื่อให้สามารถสร้างส่วนหัวของใบแจ้งหนี้ รายการใบแจ้งหนี้ และเอกสารแนบใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="826e2-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="826e2-128">เอนทิตีข้อมูลต่อไปนี้จะถูกใช้สำหรับวัตถุที่สร้างแพคเกจข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="826e2-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="826e2-129">ส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-129">Vendor invoice header</span></span>
+ <span data-ttu-id="826e2-130">รายการใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-130">Vendor invoice line</span></span>
+ <span data-ttu-id="826e2-131">สิ่งที่แนบของเอกสารใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="826e2-132">การแนบเอกสารใบแจ้งหนี้ของผู้จัดจำหน่ายเป็นเอนทิตี้ข้อมูลใหม่ที่จะถูกนำมาใช้เป็นส่วนหนึ่งของคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="826e2-133">มีการปรับเปลี่ยนเอนทิตีส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายเพื่อให้สนับสนุนเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="826e2-134">เอนทิตี้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายยังไม่ได้ถูกแก้ไขสำหรับลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="826e2-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแพคเกจข้อมูล โปรดดู [ภาพรวมของการจัดการข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)</span><span class="sxs-lookup"><span data-stu-id="826e2-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="826e2-136">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างแพคเกจข้อมูลโดยใช้พื้นที่ทำงานการจัดการข้อมูล ให้ดูที่ [ประมวลผลและใช้บรรจุภัณฑ์ข้อมูลในโซลูชันแอป Dynamics 365 Finance and Operations](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md)</span><span class="sxs-lookup"><span data-stu-id="826e2-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="826e2-137">ในการสร้างข้อมูลการทดสอบที่มีใบแจ้งหนี้และเอกสารแนบอย่างรวดเร็ว ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="826e2-138">ลงชื่อเข้าใช้อินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="826e2-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="826e2-139">ไปที่ **บัญชีเจ้าหนี้** > **ใบแจ้งหนี้** > **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="826e2-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="826e2-140">สร้างใบแจ้งหนี้ที่มีรายการและเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="826e2-141">เอกสารแนบต้องเป็นส่วนหัวของเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-141">The attachments must be header attachments.</span></span> <span data-ttu-id="826e2-142">ในปัจจุบัน เอนทิตี้การแนบการเอกสารใบแจ้งหนี้ของผู้จัดจำหน่ายไม่สนับสนุนเอกสารแนบของรายการ</span><span class="sxs-lookup"><span data-stu-id="826e2-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="826e2-143">เปิดพื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="826e2-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="826e2-144">สร้างงานการส่งออกที่มีส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย รายการใบแจ้งหนี้ของผู้จัดจำหน่าย และเอนทิตี้การแนบเอกสารใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="826e2-145">ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="826e2-145">Export the data.</span></span>
1. <span data-ttu-id="826e2-146">ดาวน์โหลดข้อมูลที่ส่งออกเป็นแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="826e2-146">Download the exported data as a package.</span></span> <span data-ttu-id="826e2-147">ขณะนี้คุณสามารถใช้แพคเกจเพื่อนำเข้าข้อมูลไปยังอินสแตนซ์เป้าหมาย เพื่อวัตถุประสงค์ในการทดสอบได้</span><span class="sxs-lookup"><span data-stu-id="826e2-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="826e2-148">การกำหนดนิติบุคคลสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="826e2-149">ใบแจ้งหนี้ที่ถูกนำเข้าผ่านทางแพคเกจข้อมูลสามารถเชื่อมโยงกับนิติบุคคลที่เจ้าของได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="826e2-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="826e2-150">งานการนำเข้าที่ประมวลผลใบแจ้งหนี้จะนำเข้าไปในบริษัทเดียวกัน ที่ซึ่งมีการจัดตารางผลิตงานในพื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="826e2-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="826e2-151">กล่าวได้อีกอย่างหนึ่งว่า บริษัทของงานกำหนดบริษัทที่เป็นเจ้าของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="826e2-152">เมื่อแพคเกจข้อมูลที่ประกอบด้วยใบแจ้งหนี้ถูกส่งออกไปยัง Finance ผู้เรียก (นั่นคือ แอพลิเคชันการรวมที่ดำเนินการอยู่ภายนอก Finance) สามารถกล่าวถึงรหัสบริษัทในคำขอ HTTP ได้อย่างชัดแจ้ง</span><span class="sxs-lookup"><span data-stu-id="826e2-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="826e2-153">ในกรณีนี้ บริบทบริษัทซึ่งงานการประมวลผลรันใน Finance ถูกแทนที่ และใบแจ้งหนี้จะถูกนำเข้าไปยังบริษัทที่มีการส่งผ่านผ่านคำขอ HTTP</span><span class="sxs-lookup"><span data-stu-id="826e2-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="826e2-154">ลักษณะการทำงานนี้คือ ลักษณะการทำงานการจัดการข้อมูลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="826e2-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="826e2-155">จะมีการอธิบายไว้ที่นี่ ในบริบทของใบแจ้งหนี้ เพื่อความสมบูรณ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="826e2-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="826e2-156">การประมวลผลข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="826e2-156">Exception processing</span></span>

<span data-ttu-id="826e2-157">ในสถานการณ์จำลองที่ใบแจ้งหนี้ของผู้จัดจำหน่ายเข้ามาใน Finance and Operations ผ่านทางการรวม ต้องมีวิธีที่ง่ายสำหรับสมาชิกทีมบัญชีเจ้าหนี้เพื่อประมวลผลข้อยกเว้นหรือใบแจ้งหนี้ที่ล้มเหลว และเพื่อสร้างใบแจ้งหนี้ที่ค้างอยู่จากใบแจ้งหนี้ที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="826e2-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="826e2-158">ขณะนี้การประมวลผลข้อยกเว้นนี้สำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย เป็นส่วนหนึ่งของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="826e2-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="826e2-159">หน้ารายการข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="826e2-159">Exceptions list page</span></span>

<span data-ttu-id="826e2-160">หน้ารายการใหม่สำหรับข้อยกเว้นของใบแจ้งหนี้จะพร้อมใช้งานเมื่อ **บัญชีเจ้าหนี้** > **ใบแจ้งหนี้** > **การนำเข้าล้มเหลว** > **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ล้มเหลวในการนำเข้า**</span><span class="sxs-lookup"><span data-stu-id="826e2-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="826e2-161">หน้านี้แสดงเรกคอร์ดส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมด จากตารางการจัดเตรียมของเอนทิตีข้อมูลส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="826e2-162">หมายเหตุว่า คุณสามารถดูเรกคอร์ดที่เหมือนกันจากพื้นที่ทำงาน **การจัดการข้อมูล** ได้ ซึ่งคุณยังสามารถทำการดำเนินการเดียวกันกับที่มีการกำหนดไว้ในลักษณะการจัดการข้อยกเว้นได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="826e2-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="826e2-163">อย่างไรก็ตาม UI ที่คุณลักษณะการจัดการข้อยกเว้นมีให้ ได้รับการปรับให้เหมาะสมสำหรับผู้ใช้งานตามหน้าที่</span><span class="sxs-lookup"><span data-stu-id="826e2-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![หน้ารายการข้อยกเว้น](media/vendor_invoice_automation_02.png)

<span data-ttu-id="826e2-165">หน้ารายการนี้ประกอบด้วยฟิลด์ต่อไปนี้ที่เข้ามาผ่านทางตัวดึงข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="826e2-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="826e2-166">**บริษัท** – บริษัทที่เป็นเจ้าของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="826e2-167">**ข้อความแสดงข้อผิดพลาด**– ข้อความแสดงข้อผิดพลาดที่กรอบงานการจัดการข้อมูลออกมาเพื่ออธิบายว่า เพราะเหตุใดจึงไม่สามารถสร้างใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="826e2-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="826e2-168">**หมายเลข** – หมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="826e2-169">**บัญชีใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="826e2-169">**Invoice account**</span></span>
+ <span data-ttu-id="826e2-170">**ชื่อ** – ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="826e2-171">**บัญชีผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="826e2-171">**Vendor account**</span></span>
+ <span data-ttu-id="826e2-172">**ใบสั่งซื้อ** – หมายเลขใบสั่งซื้อ (PO) สำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="826e2-173">**วันที่ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="826e2-173">**Posting date**</span></span>
+ <span data-ttu-id="826e2-174">**วันที่ในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="826e2-174">**Invoice date**</span></span>
+ <span data-ttu-id="826e2-175">**คำอธิบายใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="826e2-175">**Invoice description**</span></span>
+ <span data-ttu-id="826e2-176">**สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="826e2-176">**Currency**</span></span>
+ <span data-ttu-id="826e2-177">**ล็อก**</span><span class="sxs-lookup"><span data-stu-id="826e2-177">**Log**</span></span>
+ <span data-ttu-id="826e2-178">**การอ้างอิงรายการ**– ตัวระบุที่มาจากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="826e2-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="826e2-179">การอ้างอิงรายการไม่ใช่รหัสใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="826e2-180">หน้ารายการนี้ยังมีบานหน้าต่างแสดงตัวอย่างที่คุณสามารถใช้ในลักษณะต่อไปนี้ได้อีกด้วย:</span><span class="sxs-lookup"><span data-stu-id="826e2-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="826e2-181">ดูข้อความแสดงข้อผิดพลาดทั้งหมด เพื่อให้คุณไม่จำเป็นต้องขยายคอลัมน์ **ข้อความแสดงข้อผิดพลาด** ในกริด</span><span class="sxs-lookup"><span data-stu-id="826e2-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="826e2-182">ดูรายการทั้งหมดของเอกสารแนบสำหรับใบแจ้งหนี้ ถ้ามีเอกสารแนบใด ๆ มาพร้อมกับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="826e2-183">หน้ารายการสนับสนุนการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="826e2-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="826e2-184">**แก้ไข** – เปิดเรกคอร์ดข้อยกเว้นในโหมดแก้ไข เพื่อให้คุณสามารถแก้ไขปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="826e2-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="826e2-185">**ตัวเลือก** – เข้าถึงตัวเลือกมาตรฐานที่มีอยู่ในหน้ารายการ</span><span class="sxs-lookup"><span data-stu-id="826e2-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="826e2-186">คุณสามารถใช้ตัวเลือก **เพิ่มไปยังพื้นที่ทำงาน** เพื่อตรึงหน้ารายการข้อยกเว้นไปยังพื้นที่ทำงานของคุณให้เป็นไทล์หรือรายการ</span><span class="sxs-lookup"><span data-stu-id="826e2-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="826e2-187">หน้ารายละเอียดข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="826e2-187">Exception details page</span></span>

<span data-ttu-id="826e2-188">เมื่อคุณเริ่มต้นโหมดแก้ไข หน้ารายละเอียดข้อยกเว้นสำหรับใบแจ้งหนี้ที่มีปัญหาจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="826e2-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="826e2-189">ถ้ามีเอกสารแนบใด ๆ ใบแจ้งหนี้และเอกสารแนบเริ่มต้นปรากฏขึ้นเคียงข้างหน้ารายละเอียดข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="826e2-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![หน้ารายละเอียดข้อยกเว้น](media/vendor_invoice_automation_03.png)

<span data-ttu-id="826e2-191">ในภาพอธิบายก่อนหน้านี้ ไม่มีรายการใด ๆ สำหรับส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายที่เข้ามา</span><span class="sxs-lookup"><span data-stu-id="826e2-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="826e2-192">ดังนั้น ส่วนรายการจะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="826e2-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="826e2-193">หน้ารายละเอียดข้อยกเว้นสนับสนุนการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="826e2-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="826e2-194">**สร้างใบแจ้งหนี้ที่ค้างอยู่**– หลังจากที่คุณได้แก้ไขปัญหาในใบแจ้งหนี้ในฐานะที่เป็นส่วนหนึ่งของการประมวลผลข้อยกเว้น คุณสามารถคลิกปุ่มนี้เพื่อสร้างใบแจ้งหนี้ที่ค้างอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="826e2-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="826e2-195">การสร้างใบแจ้งหนี้ที่ค้างอยู่เกิดขึ้นเบื้องหลัง (เป็นการดำเนินการแบบอะซิงโครนัส)</span><span class="sxs-lookup"><span data-stu-id="826e2-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="826e2-196">บริการที่ใช้ร่วมกันเปรียบเทียบกับการประมวลผลข้อยกเว้นตามองค์กร</span><span class="sxs-lookup"><span data-stu-id="826e2-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="826e2-197">หน้ารายการข้อยกเว้นสนับสนุนโครงสร้างความปลอดภัยมาตรฐานที่พื้นที่ทำงาน **การจัดการข้อมูล** สนับสนุนเพื่อการประมวลผลเรกคอร์ดการแบ่งระยะ</span><span class="sxs-lookup"><span data-stu-id="826e2-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="826e2-198">งานการนำเข้าใบแจ้งหนี้จะถูกรักษาไว้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="826e2-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="826e2-199">โดยบทบาทผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="826e2-199">By user role</span></span>
+ <span data-ttu-id="826e2-200">ตามผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="826e2-200">By user</span></span>
+ <span data-ttu-id="826e2-201">โดยนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="826e2-201">By legal entity</span></span>

![นำเข้างานที่มีการรักษาความปลอดภัยโดยบทบาทผู้ใช้และนิติบุคคล](media/vendor_invoice_automation_04.png)

<span data-ttu-id="826e2-203">ถ้ามีการตั้งค่าคอนฟิกความปลอดภัยสำหรับงานการนำเข้าใบแจ้งหนี้ หน้ารายการข้อยกเว้นจะพิจารณาการตั้งค่าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="826e2-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="826e2-204">ผู้ใช้จะสามารถดูเฉพาะเรกคอร์ดข้อยกเว้นของใบแจ้งหนี้ที่การตั้งค่านี้อนุญาตให้มองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="826e2-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="826e2-205">ตัวอย่างเช่น Contoso ได้ตัดสินใจให้ประมวลผลข้อยกเว้นของใบแจ้งหนี้โดยนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="826e2-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="826e2-206">ดังนั้น ความปลอดภัยจะถูกตั้งค่าคอนฟิกในงานการนำเข้าใบแจ้งหนี้ ในลักษณะที่ผู้ใช้ในนิติบุคคล A สามารถเห็นเฉพาะข้อยกเว้นใบแจ้งหนี้ในนิติบุคคล A ในขณะที่ผู้ใช้ในนิติบุคคล B สามารถเห็นเฉพาะข้อยกเว้นใบแจ้งหนี้ในนิติบุคคล B การตั้งค่านี้ช่วยให้สามารถแบ่งแยกหน้าที่สำหรับการจัดการข้อยกเว้นของใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="826e2-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="826e2-207">Contoso อาจตัดสินใจได้ด้วยว่าไม่ต้องการบังคับใช้ความปลอดภัยใด ๆ เพื่อให้ผู้ใช้เดียวกันสามารถประมวลผลข้อยกเว้นของใบแจ้งหนี้สำหรับนิติบุคคลทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="826e2-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="826e2-208">การตั้งค่านี้เปิดใช้งานในสถานการณ์จำลองของบริการที่ใช้ร่วมกันสำหรับการจัดการข้อยกเว้นของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="826e2-209">ตัวแสดงเอกสารแนบแบบเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="826e2-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="826e2-210">เพื่อช่วยให้คุณสามารถดูเอกสารแนบสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายได้ง่าย ขณะนี้หน้าต่อไปนี้ที่ถูกใช้ในกระบวนการออกใบแจ้งหนี้ได้ให้มีตัวแสดงเอกสารแนบ:</span><span class="sxs-lookup"><span data-stu-id="826e2-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="826e2-211">**การจัดการข้อยกเว้น**</span><span class="sxs-lookup"><span data-stu-id="826e2-211">**Exception handling**</span></span>
+ <span data-ttu-id="826e2-212">หน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** (ยังพร้อมใช้งานในกระบวนการตรวจทานใบแจ้งหนี้ด้วย)</span><span class="sxs-lookup"><span data-stu-id="826e2-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="826e2-213">หน้าการสอบถาม **สมุดรายวันใบแจ้งหนี้** (สำหรับใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว)</span><span class="sxs-lookup"><span data-stu-id="826e2-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="826e2-214">นี่เป็นฟังก์ชันการทำงานหลักที่ตัวแสดงเอกสารแนบมีให้:</span><span class="sxs-lookup"><span data-stu-id="826e2-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="826e2-215">ดูชนิดของเอกสารแนบทั้งหมดที่การจัดการเอกสารสนับสนุน (แฟ้ม รูปภาพ Url และบันทึกย่อ)</span><span class="sxs-lookup"><span data-stu-id="826e2-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="826e2-216">ดูไฟล์ TIFF แบบหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="826e2-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="826e2-217">ดำเนินการต่อไปนี้ในไฟล์รูปภาพ:</span><span class="sxs-lookup"><span data-stu-id="826e2-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="826e2-218">เน้นส่วนของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="826e2-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="826e2-219">บล็อคส่วนของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="826e2-219">Block parts of the image.</span></span>
  + <span data-ttu-id="826e2-220">เพิ่มคำอธิบายไปยังรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="826e2-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="826e2-221">ย่อ/ขยายรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="826e2-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="826e2-222">เลื่อนรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="826e2-222">Pan the image.</span></span>
  + <span data-ttu-id="826e2-223">ยกเลิกและทำซ้ำการกระทำ</span><span class="sxs-lookup"><span data-stu-id="826e2-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="826e2-224">ทำให้รูปภาพพอดีกับขนาด</span><span class="sxs-lookup"><span data-stu-id="826e2-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="826e2-225">การดำเนินการเหล่านี้จะพร้อมใช้งานเฉพาะสำหรับไฟล์รูปภาพ (JPEG, TIFF, PNG และอื่น ๆ)</span><span class="sxs-lookup"><span data-stu-id="826e2-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="826e2-226">การเปลี่ยนแปลงใด ๆ ที่คุณทำกับรูปภาพโดยใช้การดำเนินการเหล่านี้ จะถูกบันทึกเป็นไฟล์รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="826e2-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="826e2-227">ในปัจจุบัน ตัวแสดงเอกสารแนบไม่รวมความสามารถในการตรวจสอบหรือการกำหนดเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="826e2-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="826e2-228">เอกสารแนบเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="826e2-228">Default attachment</span></span>

<span data-ttu-id="826e2-229">ถ้าใบแจ้งหนี้ของผู้จัดจำหน่ายมีเอกสารแนบมากกว่าหนึ่งรายการ คุณสามารถตั้งค่าหนึ่งในเอกสารให้เป็นเอกสารแนบเริ่มต้นในหน้า **เอกสารแนบ** ได้</span><span class="sxs-lookup"><span data-stu-id="826e2-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="826e2-230">ตัวเลือก **เป็นเอกสารแนบเริ่มต้น** เป็นตัวเลือกใหม่ที่ถูกเพิ่มให้เป็นส่วนหนึ่งของคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="826e2-231">ตัวเลือกนี้ยังถูกแสดงในเอนทิตี้ข้อมูลเอกสารแนบของใบแจ้งหนี้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="826e2-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="826e2-232">ดังนั้น เอกสารแนบเริ่มต้นสามารถถูกตั้งค่าได้ผ่านการรวม</span><span class="sxs-lookup"><span data-stu-id="826e2-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="826e2-233">เอกสารเดียวเท่านั้นที่สามารถถูกตั้งค่าเป็นเอกสารแนบเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="826e2-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="826e2-234">หลังจากที่คุณตั้งค่าเอกสารเป็นเอกสารแนบเริ่มต้น นั้นจะถูกแสดงในตัวแสดงเอกสารแนบโดยอัตโนมัติ เมื่อมีการเปิดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="826e2-235">ถ้าคุณไม่ตั้งค่าเอกสารใด ๆ เป็นเอกสารแนบเริ่มต้น ตัวแสดงจะไม่แสดงเอกสารแนบใด ๆ โดยอัตโนมัติ เมื่อมีการเปิดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="826e2-236">แสดง/ซ่อนเอกสารแนบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="826e2-237">ปุ่มใหม่ที่พร้อมใช้งานในหน้าการสอบถาม **การประมวลผลข้อยกเว้น** **ใบแจ้งหนี้ที่ค้างอยู่** และ **สมุดรายวันใบแจ้งหนี้** ช่วยให้คุณสามารถแสดงหรือซ่อนตัวแสดงเอกสารแนบได้</span><span class="sxs-lookup"><span data-stu-id="826e2-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="826e2-238">ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="826e2-238">Security</span></span>

<span data-ttu-id="826e2-239">การดำเนินการต่อไปนี้ในตัวแสดงเอกสารแนบจะถูกควบคุมผ่านทางความปลอดภัยตามบทบาท:</span><span class="sxs-lookup"><span data-stu-id="826e2-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="826e2-240">การเน้น</span><span class="sxs-lookup"><span data-stu-id="826e2-240">Highlighting</span></span>
+ <span data-ttu-id="826e2-241">บล็อค</span><span class="sxs-lookup"><span data-stu-id="826e2-241">Block</span></span>
+ <span data-ttu-id="826e2-242">คำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="826e2-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="826e2-243">หน้าใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="826e2-243">Pending vendor invoices page</span></span>

<span data-ttu-id="826e2-244">สิทธิ์ต่อไปนี้ให้การเข้าถึงแบบอ่านอย่างเดียว หรือการเข้าถึงแบบอ่าน/เขียนไปยังตัวแสดงเอกสารแนบสำหรับการดำเนินการเน้น การบล็อค และคำอธิบายประกอบ:</span><span class="sxs-lookup"><span data-stu-id="826e2-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="826e2-245">**รักษารูปภาพของใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์นี้ให้การเข้าถึงแบบอ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="826e2-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="826e2-246">**ดูรูปภาพของใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์นี้ให้การเข้าถึงแบบอ่านเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="826e2-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="826e2-247">หน้าที่ต่อไปนี้ให้การเข้าถึงแบบอ่านอย่างเดียว หรือการเข้าถึงแบบอ่าน/เขียนไปยังตัวแสดงเอกสารแนบสำหรับการดำเนินการดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="826e2-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="826e2-248">**รักษาใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์ในการรักษารูปภาพของใบแจ้งหนี้ของผู้จัดจำหน่ายถูกกำหนดให้กับหน้าที่นี้</span><span class="sxs-lookup"><span data-stu-id="826e2-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="826e2-249">**สอบถามสถานะใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์ในการดูรูปภาพของใบแจ้งหนี้ของผู้จัดจำหน่ายถูกกำหนดให้กับหน้าที่นี้</span><span class="sxs-lookup"><span data-stu-id="826e2-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="826e2-250">บทบาทต่อไปนี้ให้การเข้าถึงแบบอ่านอย่างเดียว หรือการเข้าถึงแบบอ่าน/เขียนไปยังตัวแสดงเอกสารแนบสำหรับการดำเนินการดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="826e2-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="826e2-251">**เจ้าหน้าที่บัญชีเจ้าหนี้** และ **ผู้จัดการฝ่ายเจ้าหนี้บัญชี** – หน้าที่ในการรักษาภาษีใบแจ้งหนี้ของผู้จัดจำหน่ายถูกกำหนดให้กับบทบาทเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="826e2-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="826e2-252">**เจ้าหน้าที่บัญชีเจ้าหนี้** **ผู้จัดการฝ่ายเจ้าหนี้บัญชี** **เจ้าหน้าที่ฝ่ายชำระเงินส่วนกลางของบัญชีเจ้าหนี้** และ **เจ้าหน้าที่ฝ่ายชำระเงินของบัญชีเจ้าหนี้** – การสอบถามหน้าที่ของสถานะใบแจ้งหนี้ของผู้จัดจำหน่ายถูกกำหนดให้กับบทบาทเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="826e2-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="826e2-253">หน้ารายละเอียดข้อยกเว้นของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="826e2-253">Invoice exception details page</span></span>

<span data-ttu-id="826e2-254">สิทธิ์ต่อไปนี้ให้การเข้าถึงแบบอ่านอย่างเดียว หรือการเข้าถึงแบบอ่าน/เขียนไปยังตัวแสดงเอกสารแนบสำหรับการดำเนินการเน้น การบล็อค และคำอธิบายประกอบ</span><span class="sxs-lookup"><span data-stu-id="826e2-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="826e2-255">แบบนอกกรอบ บทบาทที่ถูกระบุไว้ในส่วนนี้ให้การเข้าถึงแบบอ่านอย่างเดียวไปยังรูปของใบแจ้งหนี้ในตัวแสดงเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="826e2-256">ถ้าบทบาทต้องมีสิทธิ์ในการเขียนไปยังรูปภาพด้วย คุณสามารถให้สิทธิในการเขียนให้กับบทบาทนั้น โดยใช้สิทธิ์และหน้าที่ที่ได้อธิบายไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="826e2-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="826e2-257">**รักษารูปภาพเอนทิตี้ส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์นี้ให้การเข้าถึงแบบอ่าน/เขียนไปยังรูปใบแจ้งหนี้ในตัวแสดงเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="826e2-258">**ดูรูปภาพเอนทิตี้ส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์นี้ให้การดูแบบอ่านอย่างเดียวไปยังรูปใบแจ้งหนี้ในตัวแสดงเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="826e2-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="826e2-259">หน้าที่ต่อไปนี้ให้การเข้าถึงแบบอ่านอย่างเดียวไปยังตัวแสดงเอกสารแนบสำหรับการดำเนินการดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="826e2-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="826e2-260">**รักษาใบแจ้งหนี้ของผู้จัดจำหน่าย** – สิทธิ์ในการรักษารูปภาพเอนทิตี้ส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายถูกกำหนดให้กับหน้าที่นี้</span><span class="sxs-lookup"><span data-stu-id="826e2-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="826e2-261">บทบาทต่อไปนี้ให้การเข้าถึงแบบอ่านอย่างเดียวไปยังตัวแสดงเอกสารแนบสำหรับการดำเนินการดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="826e2-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="826e2-262">**เจ้าหน้าที่บัญชีเจ้าหนี้** และ **ผู้จัดการฝ่ายเจ้าหนี้บัญชี** – หน้าที่ในการรักษาภาษีใบแจ้งหนี้ของผู้จัดจำหน่ายถูกกำหนดให้กับบทบาทเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="826e2-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="826e2-263">โดยค่าเริ่มต้น ถ้าบทบาทผู้ใช้ให้สิทธิ์ในการแก้ไขในหน้าใด ๆ ผู้ใช้จะมีสิทธิ์ในการแก้ไขบนตัวแสดงสิ่งที่แนบสำหรับการดำเนินการที่เน้น การบล็อค และคำอธิบายด้วย</span><span class="sxs-lookup"><span data-stu-id="826e2-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="826e2-264">อย่างไรก็ตาม ถ้ามีสถานการณ์จำลองที่บทบาทเฉพาะควรมีสิทธิ์ในการแก้ไขในนหน้า แต่ไม่ได้อยู่ในตัวแสดงเอกสารแนบ สิทธิ์ที่เหมาะสมจากรายการก่อนหน้านี้สามารถถูกใช้เพื่อให้ตอบสนองกรณีการใช้</span><span class="sxs-lookup"><span data-stu-id="826e2-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
