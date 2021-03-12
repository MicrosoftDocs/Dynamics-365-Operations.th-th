---
title: ตั้งค่าคำอธิบายเริ่มต้นสำหรับการลงรายการบัญชีโดยอัตโนมัติ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าข้อความเริ่มต้นที่ใช้เพื่ออธิบายรายการบัญชีที่ถูกลงรายการบัญชีโดยอัตโนมัติในบัญชีแยกประเภททั่วไป คุณสามารถตั้งค่าข้อความคำอธิบายเริ่มต้น โดยใช้ข้อความอิสระ หรือโดยการเลือกตัวแปรคงที่
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1b73b104ed8a8a015cb97dcf3055a648cfb083d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994751"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="49b41-104">ตั้งค่าคำอธิบายเริ่มต้นสำหรับการลงรายการบัญชีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="49b41-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49b41-105">หัวข้อนี้อธิบายวิธีการตั้งค่าข้อความเริ่มต้นที่ใช้เพื่ออธิบายรายการบัญชีที่ถูกลงรายการบัญชีโดยอัตโนมัติในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="49b41-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="49b41-106">คุณสามารถตั้งค่าข้อความคำอธิบายเริ่มต้น โดยใช้ข้อความอิสระ หรือโดยการเลือกตัวแปรคงที่</span><span class="sxs-lookup"><span data-stu-id="49b41-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="49b41-107">สำหรับชนิดธุรกรรมบางชนิดในบางประเทศหรือบางภูมิภาค คุณยังสามารถรวมข้อความจากฟิลด์ในฐานข้อมูล Microsoft Dynamics AX ที่เกี่ยวข้องกับชนิดของธุรกรรมดังกล่าวได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="49b41-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="49b41-108">สำหรับรายการของชนิดของธุรกรรมและประเทศและภูมิภาค ให้ดูที่ส่วน [ไม่จำเป็นต้องระบุ: เพิ่มข้อความอื่นๆ ไปยังกับคำอธิบายเริ่มต้น](#optional-add-other-text-to-default-descriptions) ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="49b41-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="49b41-109">ตั้งค่าคำอธิบายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49b41-109">Set up default descriptions</span></span>

1. <span data-ttu-id="49b41-110">ไปที่ **การจัดการองค์กร** \> **การตั้งค่า** \> **คำอธิบายเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="49b41-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="49b41-111">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="49b41-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="49b41-112">ในฟิลด์ **คำอธิบาย** เลือกชนิดของธุรกรรมเพื่อสร้างคำอธิบายเริ่มต้นให้</span><span class="sxs-lookup"><span data-stu-id="49b41-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="49b41-113">ในฟิลด์ **ภาษา** ให้เลือกภาษาที่นำคำอธิบายนี้ไปใช้</span><span class="sxs-lookup"><span data-stu-id="49b41-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="49b41-114">ในฟิลด์ **ข้อความ** ป้อนคำอธิบายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49b41-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="49b41-115">คุณสามารถพิมพ์ข้อความลงในฟิลด์ หรือคุณสามารถใช้ตัวแปรข้อความอิสระต่อไปนี้อย่างน้อยหนึ่งรายการ:</span><span class="sxs-lookup"><span data-stu-id="49b41-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="49b41-116">**%1** – เพิ่มวันที่ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="49b41-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="49b41-117">**%2** – เพิ่มตัวระบุที่สอดคล้องกับชนิดเอกสารที่มีการลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="49b41-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="49b41-118">ตัวอย่างเช่น สำหรับชนิดของธุรกรรมที่เกี่ยวข้องกับใบแจ้งหนี้ ตัวแปร **%2** จะเพิ่มหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="49b41-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="49b41-119">**%3** – เพิ่มตัวระบุที่เกี่ยวข้องกับชนิดเอกสารที่มีการลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="49b41-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="49b41-120">ตัวอย่างเช่น สำหรับชนิดของธุรกรรมที่เกี่ยวข้องกับใบแจ้งหนี้ ตัวแปร **%3** จะเพิ่มหมายเลขบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49b41-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="49b41-121">ไม่จำเป็น: เพิ่มข้อความอื่นที่คำอธิบายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49b41-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="49b41-122">สำหรับชนิดธุรกรรมบางชนิดในบางประเทศหรือบางภูมิภาค คำอธิบายเริ่มต้นสามารถรวมข้อความที่มาจากฟิลด์ในข้อมูลของคุณซึ่งเกี่ยวข้องกับชนิดของธุรกรรมดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="49b41-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="49b41-123">รายการต่อไปนี้แสดงชนิดของธุรกรรม และประเทศและภูมิภาค ที่ตัวเลือกนี้จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="49b41-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="49b41-124">**ชนิดธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="49b41-124">**Transaction types**</span></span>

<span data-ttu-id="49b41-125">คุณสามารถเพิ่มข้อความอื่นที่คำอธิบายเริ่มต้นสำหรับชนิดธุรกรรมที่เกี่ยวข้องกับชนิดเอกสารต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49b41-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="49b41-126">ใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49b41-126">Customer invoices</span></span>
- <span data-ttu-id="49b41-127">ใบลดหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49b41-127">Customer credit notes</span></span>
- <span data-ttu-id="49b41-128">การชำระเงินสดของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49b41-128">Customer cash payments</span></span>
- <span data-ttu-id="49b41-129">การชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="49b41-129">Vendor payments</span></span>
- <span data-ttu-id="49b41-130">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="49b41-130">Sales orders</span></span>
- <span data-ttu-id="49b41-131">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="49b41-131">Purchase orders</span></span>
- <span data-ttu-id="49b41-132">สมุดรายวันสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="49b41-132">Inventory journals</span></span>
- <span data-ttu-id="49b41-133">การวางแผนหลัก (MRP)</span><span class="sxs-lookup"><span data-stu-id="49b41-133">Master planning (MRP)</span></span>
- <span data-ttu-id="49b41-134">สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="49b41-134">Fixed assets</span></span>

<span data-ttu-id="49b41-135">**ประเทศและภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="49b41-135">**Countries and regions**</span></span>

<span data-ttu-id="49b41-136">ตัวเลือกนี้จะพร้อมใช้งานสำหรับประเทศและภูมิภาคดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49b41-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="49b41-137">บราซิล</span><span class="sxs-lookup"><span data-stu-id="49b41-137">Brazil</span></span>
- <span data-ttu-id="49b41-138">จีน</span><span class="sxs-lookup"><span data-stu-id="49b41-138">China</span></span>
- <span data-ttu-id="49b41-139">สาธารณรัฐเช็ก</span><span class="sxs-lookup"><span data-stu-id="49b41-139">Czech Republic</span></span>
- <span data-ttu-id="49b41-140">ยุโรปตะวันออก</span><span class="sxs-lookup"><span data-stu-id="49b41-140">Eastern Europe</span></span>
- <span data-ttu-id="49b41-141">ฮังการี</span><span class="sxs-lookup"><span data-stu-id="49b41-141">Hungary</span></span>
- <span data-ttu-id="49b41-142">อินเดีย</span><span class="sxs-lookup"><span data-stu-id="49b41-142">India</span></span>
- <span data-ttu-id="49b41-143">ญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="49b41-143">Japan</span></span>
- <span data-ttu-id="49b41-144">ลิทัวเนีย</span><span class="sxs-lookup"><span data-stu-id="49b41-144">Lithuania</span></span>
- <span data-ttu-id="49b41-145">ลัตเวีย</span><span class="sxs-lookup"><span data-stu-id="49b41-145">Latvia</span></span>
- <span data-ttu-id="49b41-146">โปแลนด์</span><span class="sxs-lookup"><span data-stu-id="49b41-146">Poland</span></span>
- <span data-ttu-id="49b41-147">รัสเซีย</span><span class="sxs-lookup"><span data-stu-id="49b41-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="49b41-148">เพิ่มข้อความคำอธิบายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49b41-148">Add text to default descriptions</span></span>

<span data-ttu-id="49b41-149">หลังจากที่คุณดำเนินการขั้นตอนในส่วน [ตั้งค่าคำอธิบายเริ่มต้น](#set-up-default-descriptions) เสร็จสมบูรณ์ก่อนหน้านี้ในหัวข้อนี้ ให้ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มข้อความอื่นในคำอธิบายเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49b41-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="49b41-150">บน FastTab **พารามิเตอร์** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="49b41-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="49b41-151">ในฟิลด์ **ตารางอ้างอิง** เลือกตารางฐานข้อมูลที่จะเพิ่มข้อมูลของพารามิเตอร์ไปยังคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="49b41-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="49b41-152">ในฟิลด์ **ฟิลด์อ้างอิง** เลือกฟิลด์ที่จะเพิ่มข้อมูลของพารามิเตอร์ไปยังคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="49b41-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="49b41-153">ทำซ้ำขั้นตอนที่ 1 ถึง 3 หากต้องการเพิ่มพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="49b41-153">Repeat steps 1 through 3 to add more parameters.</span></span>
