---
title: การกำหนดหมายเลขเอกสารและใบสำคัญตามลำดับเวลา
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและการกำหนดหมายเลขตามลำดับเวลาสำหรับเอกสารที่ใช้ได้และใบสำคัญที่เกี่ยวข้อง
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4a27b6fdd1e244fb0cb8c5fcefc484494aeb88bd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254543"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="0febc-103">การกำหนดหมายเลขเอกสารและใบสำคัญตามลำดับเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0febc-104">ในบางประเทศ มีข้อกําหนดทางกฎหมายว่าต้องกําหนดหมายเลขเอกสารและใบสำคัญที่เกี่ยวข้องตามลำดับเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="0febc-105">ลำดับระยะเวลาต้องได้รับการสนับสนุนตามช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="0febc-106">ตัวเลขทั้งหมดที่เป็นของรอบระยะเวลาก่อนหน้านี้ต้องน้อยกว่าตัวเลขที่เป็นของรอบระยะเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="0febc-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="0febc-107">เพื่อตอบสนองความต้องการนี้ จึงมีการใช้ฟังก์ชันการกำหนดหมายเลขตามลำดับเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="0febc-108">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกและการใช้การกำหนดหมายเลขตามลำดับเวลาสำหรับเอกสารที่ใช้ได้และใบสำคัญที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0febc-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0febc-109">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0febc-109">Prerequisites</span></span>

<span data-ttu-id="0febc-110">ในพื้นที่ทำงานการจัดการคุณลักษณะ เปิดใช้งานคุณลักษณะ **การกำหนดหมายเลขตามลำดับเวลา**</span><span class="sxs-lookup"><span data-stu-id="0febc-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="0febc-111">สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0febc-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="0febc-112">ตั้งค่าคอนฟิกการกําหนดหมายเลขตามลำดับเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-112">Configure chronological numbering</span></span>

<span data-ttu-id="0febc-113">การกำหนดหมายเลขตามลำดับเวลาจะมีผลกระทบต่อเอกสารต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="0febc-114">**บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="0febc-114">**Accounts receivable**</span></span>
- <span data-ttu-id="0febc-115">ใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0febc-115">Customer invoice</span></span>
- <span data-ttu-id="0febc-116">ใบสำคัญใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0febc-116">Customer invoice voucher</span></span>
- <span data-ttu-id="0febc-117">ใบลดหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="0febc-117">Sales credit note</span></span>
- <span data-ttu-id="0febc-118">ใบสำคัญใบลดหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="0febc-118">Sales credit note voucher</span></span>
- <span data-ttu-id="0febc-119">ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0febc-119">Free text invoice</span></span>
- <span data-ttu-id="0febc-120">ใบสำคัญใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0febc-120">Free text invoice voucher</span></span>
- <span data-ttu-id="0febc-121">ใบลดหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0febc-121">Free text credit note</span></span>
- <span data-ttu-id="0febc-122">ใบสำคัญใบลดหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="0febc-122">Free text credit note voucher</span></span>
- <span data-ttu-id="0febc-123">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0febc-123">Packing slip</span></span>
- <span data-ttu-id="0febc-124">ใบสำคัญบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0febc-124">Packing slip voucher</span></span>
- <span data-ttu-id="0febc-125">ใบสำคัญการแก้ไขบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0febc-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="0febc-126">ใบสำคัญดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="0febc-126">Interest note voucher</span></span>
- <span data-ttu-id="0febc-127">ใบสำคัญจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0febc-127">Collection letter voucher</span></span>

<span data-ttu-id="0febc-128">**บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="0febc-128">**Accounts payable**</span></span>
- <span data-ttu-id="0febc-129">ใบสำคัญใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-129">Invoice voucher</span></span>
- <span data-ttu-id="0febc-130">ใบสำคัญใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-130">Credit note voucher</span></span>
- <span data-ttu-id="0febc-131">ใบสำคัญรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0febc-131">Product receipt voucher</span></span>

<span data-ttu-id="0febc-132">**การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="0febc-132">**Project management**</span></span>
- <span data-ttu-id="0febc-133">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-133">Invoice</span></span>
- <span data-ttu-id="0febc-134">ใบสำคัญใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-134">Invoice voucher</span></span>
- <span data-ttu-id="0febc-135">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-135">Credit note</span></span>
- <span data-ttu-id="0febc-136">ใบสำคัญใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0febc-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="0febc-137">กำหนดลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-137">Define number sequences</span></span>

<span data-ttu-id="0febc-138">เมื่อต้องการกําหนดลำดับหมายเลข ไปที่ **การจัดการองค์กร** > **ลำดับหมายเลข** > **ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="0febc-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="0febc-139">คุณสามารถกําหนดลำดับหมายเลขได้มากตามที่ต้องการ เพื่อครอบคลุมรอบระยะเวลาที่ได้รับผลกระทบต่อเอกสารที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="0febc-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="0febc-140">ระบุบริษัทสำหรับแต่ละลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="0febc-141">ต้องกําหนดเซกเมนต์ของลำดับหมายเลขเพื่อให้เรียงตามลำดับเวลาของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="0febc-142">ตัวอย่างเช่น ชื่อเซกเมนต์อาจประกอบด้วยคำนำหน้าพิเศษที่ระบุรอบระยะเวลาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0febc-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![การตั้งค่าลำดับหมายเลข](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="0febc-144">กำหนดค่ากลุ่มลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-144">Configure number sequence groups</span></span>

<span data-ttu-id="0febc-145">เมื่อต้องการตั้งค่าคอนฟิกกลุ่มลำดับหมายเลข ให้ไปที่ **บัญชีลูกหนี้** > **การตั้งค่า** > **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="0febc-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="0febc-146">บนแท็บ **ลำดับหมายเลข** ให้กําหนดกลุ่มลำดับหมายเลขได้มากเท่าที่ต้องการ เพื่อครอบคลุมรอบระยะเวลาที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="0febc-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="0febc-147">ในแต่ละกลุ่ม ในส่วน **การอ้างอิง** ให้เลือกหนึ่งในข้อมูลอ้างอิงเอกสารที่สนับสนุน และในฟิลด์ **รหัสลำดับหมายเลข** ให้อ้างอิงลำดับหมายเลขที่สร้างขึ้นก่อนหน้านี้ ให้กับรอบระยะเวลาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0febc-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![การตั้งค่ากลุ่มลำดับหมายเลข](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="0febc-149">ในทำนองเดียวกัน ให้ตั้งค่าคอนฟิกกลุ่มลำดับหมายเลขใน **บัญชีเจ้าหนี้** และโมดูล **การจัดการโครงการและการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="0febc-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="0febc-150">กำหนดค่ากลุ่มลำดับหมายเลขตามลำดับเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="0febc-151">เมื่อต้องการตั้งค่าคอนฟิกกลุ่มลำดับหมายเลขตามลำดับเวลา ให้ไปที่ **การจัดการองค์กร** > **ลำดับหมายเลข** > **กลุ่มลำดับหมายเลขตามลำดับเวลา**</span><span class="sxs-lookup"><span data-stu-id="0febc-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="0febc-152">กำหนดเงื่อนไขการบังคับใช้สำหรับกลุ่มลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-152">Define the applicability conditions for number sequence groups.</span></span>

![การตั้งค่าหมายเลขตามลำดับเวลา](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="0febc-154">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="0febc-154">Field</span></span>            | <span data-ttu-id="0febc-155">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="0febc-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0febc-156">มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="0febc-156">Effective</span></span>  | <span data-ttu-id="0febc-157">วันที่เริ่มต้นของการบังคับใช้กลุ่มลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="0febc-158">การหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="0febc-158">Expiration</span></span>      | <span data-ttu-id="0febc-159">วันที่สิ้นสุดของการบังคับใช้กลุ่มลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="0febc-160">หากไม่มีการใช้วันที่สิ้นสุดให้เลือก **ไม่เคย**</span><span class="sxs-lookup"><span data-stu-id="0febc-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="0febc-161">ชุดเลขที่เอกสาร</span><span class="sxs-lookup"><span data-stu-id="0febc-161">Number sequence group</span></span> | <span data-ttu-id="0febc-162">กลุ่มลำดับหมายเลขที่จะใช้ในการสร้างหมายเลขเอกสารในระหว่างรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="0febc-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="0febc-163">กลุ่มลำดับหมายเลขเดิม</span><span class="sxs-lookup"><span data-stu-id="0febc-163">Original number sequence group</span></span> | <span data-ttu-id="0febc-164">รหัสกลุ่มลำดับหมายเลขนี้ใช้สำหรับรายละเอียดเพิ่มเติมที่ใช้กับการกรองข้อมูลกรณีต่างๆ เมื่อมีการมอบหมายกลุ่มลำดับหมายเลข *ถาวร* เฉพาะไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="0febc-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="0febc-165">ค่าว่างเปล่าถือเป็นค่าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0febc-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="0febc-166">หากคุณต้องการละเว้นกลุ่มที่มอบหมายเบื้องต้น ให้ใช้ตัวเลือก **ค่าเริ่มต้น** ในการตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="0febc-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="0febc-167">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0febc-167">Default</span></span> | <span data-ttu-id="0febc-168">หากเปิดอยู่ ระบบจะไม่พิจารณากลุ่มลำดับหมายเลขเอกสารที่กำหนดเบื้องต้น และใช้เฉพาะวันที่เริ่มต้นและวันที่สิ้นสุดของรอบระยะเวลาเพื่อการวิเคราะห์การบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="0febc-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="0febc-169">หากปิดอยู่ ระบบจะใช้ค่าผสมทั้งหมด **มีผลบังคับใช้** + **หมดอายุที่มีผล** + **กลุ่มลำดับหมายเลขเดิม** ในการเลือก</span><span class="sxs-lookup"><span data-stu-id="0febc-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="0febc-170">การลงรายการบัญชีเอกสาร</span><span class="sxs-lookup"><span data-stu-id="0febc-170">Document posting</span></span>
<span data-ttu-id="0febc-171">เมื่อคุณลงรายการบัญชีเอกสาร จะมีการมอบหมายกลุ่มลำดับหมายเลขที่เหมาะสมไปยังเอกสาร ตามวันที่ลงรายการบัญชีของเอกสาร จากนั้นใช้เพื่อสร้างหมายเลขเอกสารตามลำดับหมายเลขที่ตรวจพบ</span><span class="sxs-lookup"><span data-stu-id="0febc-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="0febc-172">ระบบแสดงข้อความเกี่ยวกับการกำหนดกลุ่มลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0febc-172">The system provides a message regarding the number sequence group assignment.</span></span>

![หมายเลขเอกสาร](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="0febc-174">ในบางประเทศ จะมีตรรกะเฉพาะที่ใช้ป้อนหมายเลขเอกสารอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="0febc-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="0febc-175">ในกรณีนี้ ตรรกะเฉพาะประเทศจะแทนที่คุณลักษณะ **การกำหนดหมายเลขตามลำดับเวลา**</span><span class="sxs-lookup"><span data-stu-id="0febc-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]