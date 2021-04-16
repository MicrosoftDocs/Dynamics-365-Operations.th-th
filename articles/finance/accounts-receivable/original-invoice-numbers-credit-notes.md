---
title: การอ้างอิงถึงใบแจ้งหนี้ต้นฉบับในใบลดหนี้
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและพิมพ์หมายเลขใบแจ้งหนี้ต้นฉบับในใบลดหนี้ที่เกี่ยวข้อง
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ce06a0ce4f2a308e1917ac2c7cbc66f0494a2ec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811521"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="b377b-103">การอ้างอิงถึงใบแจ้งหนี้ต้นฉบับในใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="b377b-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b377b-104">ในบางประเทศและภูมิภาค มีข้อกําหนดทางกฎหมายที่พิมพ์ใบลดหนี้ รวมถึงการอ้างอิงไปยังใบแจ้งหนี้ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="b377b-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="b377b-105">หัวข้อนี้อธิบายวิธีการตั้งค่าและพิมพ์หมายเลขใบแจ้งหนี้ต้นฉบับในใบลดหนี้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b377b-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b377b-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="b377b-106">Prerequisites</span></span>

- <span data-ttu-id="b377b-107">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เปิดคุณลักษณะ **โครงร่างการออกใบแจ้งหนี้เครดิตสำหรับการขายและรายงานใบแจ้งหนี้โครงการ**</span><span class="sxs-lookup"><span data-stu-id="b377b-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="b377b-108">สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](../../fin-and-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="b377b-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="b377b-109">ต้องตั้งค่าคอนฟิกรูปแบบที่สามารถพิมพ์ได้ของเอกสารที่กําหนดในการจัดการการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="b377b-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="b377b-110">ฟังก์ชันที่อธิบายไว้ในหัวข้อนี้จะใช้กับเอกสารต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b377b-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="b377b-111">**บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="b377b-111">**Accounts receivable**</span></span>

- <span data-ttu-id="b377b-112">ใบลดหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="b377b-112">Free text credit note</span></span>
- <span data-ttu-id="b377b-113">ใบลดหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b377b-113">Customer credit note</span></span>

<span data-ttu-id="b377b-114">**การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="b377b-114">**Project management and accounting**</span></span>

- <span data-ttu-id="b377b-115">ใบลดหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b377b-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="b377b-116">ตั้งค่าคอนฟิกพารามิเตอร์บัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="b377b-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="b377b-117">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าพารามิเตอร์ที่ควบคุมว่าจะพิมพ์การอ้างอิงถึงใบแจ้งหนี้ต้นฉบับในใบลดหนี้ที่เกี่ยวข้องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b377b-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="b377b-118">ไปที่ **บัญชีลูกหนี้** \> **การตั้งค่า** \> **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="b377b-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="b377b-119">บนแท็บ **อัปเดต** บนแท็บด่วน **ใบแจ้งหนี้** ให้ตั้งค่าตัวเลือก **ใช้โครงร่างการออกใบแจ้งหนี้เครดิตสำหรับการขายและรายงานใบแจ้งหนี้โครงการ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b377b-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![ตั้งค่าคอนฟิกพารามิเตอร์บัญชีลูกหนี้](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="b377b-121">กําหนดการอ้างอิงถึงใบแจ้งหนี้ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="b377b-121">Define references to original invoices</span></span>

<span data-ttu-id="b377b-122">ใช้ขั้นตอนต่อไปนี้เพื่อกําหนดการอ้างอิงถึงใบแจ้งหนี้ต้นฉบับตามชนิดเอกสาร</span><span class="sxs-lookup"><span data-stu-id="b377b-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="b377b-123">ใบลดหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="b377b-123">Free text credit note</span></span>

1. <span data-ttu-id="b377b-124">ไปที่ **บัญชีลูกหนี้** \> **ใบแจ้งหนี้** \> **ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b377b-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="b377b-125">สร้างใบลดหนี้ใหม่ หรือเลือกใบลดหนี้ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b377b-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="b377b-126">เปิดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b377b-126">Open the invoice.</span></span>
4. <span data-ttu-id="b377b-127">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ในกลุ่ม **ฟังก์ชัน** ให้เลือก **ออกใบแจ้งหนี้เครดิต**</span><span class="sxs-lookup"><span data-stu-id="b377b-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="b377b-128">ป้อนข้อมูลอ้างอิงถึงใบแจ้งหนี้ต้นฉบับ และเลือกเหตุผลของการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b377b-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![การนิยามการอ้างอิงของใบแจ้งหนี้ข้อความอิสระ](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="b377b-130">ใบลดหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b377b-130">Customer credit note</span></span>

1. <span data-ttu-id="b377b-131">ไปที่ **บัญชีลูกหนี้** \> **ใบสั่ง** \> **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b377b-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="b377b-132">เลือกและเปิดใบสั่งขายที่ออกใบแจ้งหนี้แล้วที่ต้องแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b377b-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="b377b-133">ในบานหน้าต่างการดำเนินการ บนแท็บ **ขาย** ในกลุ่ม **ใบลดหนี้** ให้เลือก **ใบลดหนี้**</span><span class="sxs-lookup"><span data-stu-id="b377b-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="b377b-134">ป้อนเหตุผลในการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b377b-134">Enter the reason for the correction.</span></span> <span data-ttu-id="b377b-135">การอ้างอิงถึงใบแจ้งหนี้ต้นฉบับจะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b377b-135">The reference to the original invoice is automatically established.</span></span>

![การนิยามข้อมูลอ้างอิงของใบสั่งขาย](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="b377b-137">ใบลดหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="b377b-137">Project credit note</span></span>

1. <span data-ttu-id="b377b-138">ไปที่ **การจัดการโครงการและการบัญชี** \> **ใบแจ้งหนี้โครงการ** \> **ข้อเสนอใบแจ้งหนี้โครงการ**</span><span class="sxs-lookup"><span data-stu-id="b377b-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="b377b-139">เลือกและเปิดใบแจ้งหนี้โครงการที่ต้องแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b377b-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="b377b-140">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้โครงการ** ในกลุ่ม **ฟังก์ชัน** ให้เลือก **เลือกสำหรับใบลดหนี้**</span><span class="sxs-lookup"><span data-stu-id="b377b-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="b377b-141">เลือก **การออกใบแจ้งหนี้เครดิต**</span><span class="sxs-lookup"><span data-stu-id="b377b-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="b377b-142">ป้อนเหตุผลในการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b377b-142">Enter the reason for the correction.</span></span> <span data-ttu-id="b377b-143">การอ้างอิงถึงใบแจ้งหนี้ต้นฉบับจะถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b377b-143">The reference to the original invoice is automatically established.</span></span>

![การนิยามการอ้างอิงของใบแจ้งหนี้โครงการ](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="b377b-145">การพิมพ์ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="b377b-145">Printing credit notes</span></span>

<span data-ttu-id="b377b-146">เมื่อคุณพิมพ์ข้อความอิสระ ลูกค้า และใบลดหนี้โครงการ ใบแจ้งหนี้จะรวมการอ้างอิงถึงใบแจ้งหนี้ต้นฉบับและเหตุผลของการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b377b-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![ใบลดหนี้ที่พิมพ์](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="b377b-148">ตรวจสอบให้แน่ใจว่าตั้งค่าคอนฟิกรูปแบบที่พิมพ์ได้ของเอกสารอย่างถูกต้อง โดยสมมติฐานว่าจะมีการพิมพ์การอ้างอิงไปยังต้นฉบับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b377b-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
