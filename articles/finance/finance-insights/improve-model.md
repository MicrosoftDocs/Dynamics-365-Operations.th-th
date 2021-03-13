---
title: ปรับปรุงแบบจำลองการคาดคะเน (ตัวอย่าง)
description: หัวข้อนี้อธิบายถึงลักษณะการทำงานที่คุณสามารถใช้เพื่อปรับปรุงประสิทธิภาพการทำงานของแบบจำลองการคาดการณ์
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 2bcdea4a2a8f4386b274077cd1e95398fb6fac37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009384"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="0c9a0-103">ปรับปรุงแบบจำลองการคาดคะเน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0c9a0-104">หัวข้อนี้อธิบายถึงลักษณะการทำงานที่คุณสามารถใช้เพื่อปรับปรุงประสิทธิภาพการทำงานของแบบจำลองการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="0c9a0-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="0c9a0-105">คุณเริ่มต้นการปรับปรุงแบบจำลองของคุณในพื้นที่ทำงาน **การคาดการณ์การชำระเงินของลูกค้า** ใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="0c9a0-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="0c9a0-106">ดำเนินการขั้นตอนการปรับปรุงเสร็จสมบูรณ์แล้วใน AI Builder</span><span class="sxs-lookup"><span data-stu-id="0c9a0-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="0c9a0-107">เลือกผลลัพธ์ในอดีต</span><span class="sxs-lookup"><span data-stu-id="0c9a0-107">Select historical outcomes</span></span>

<span data-ttu-id="0c9a0-108">คุณเลือกหนึ่งในผลลัพธ์ที่เป็นไปได้ที่เป็นไปได้สำหรับใบแจ้งหนี้อย่างน้อยหนึ่งรายการ: **ตรงเวลา** **ล่าช้า** และ **ล่าช้ามาก**</span><span class="sxs-lookup"><span data-stu-id="0c9a0-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="0c9a0-109">ควรเลือกผลลัพธ์ทั้งสามประการ</span><span class="sxs-lookup"><span data-stu-id="0c9a0-109">All three outcomes should be selected.</span></span> <span data-ttu-id="0c9a0-110">ถ้าคุณยกเลิกการเลือกผลลัพธ์ใด ๆ ใบแจ้งหนี้จะถูกกรองออกจากกระบวนการฝึกอบรมและความถูกต้องของการคาดการณ์จะถูกลดลง</span><span class="sxs-lookup"><span data-stu-id="0c9a0-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="0c9a0-111">[![การยืนยันผลลัพธ์](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="0c9a0-112">ถ้าองค์กรของคุณต้องการผลลัพธ์เพียงสองประการ ให้เปลี่ยนขีดจำกัด **ล่าช้า** และ **ล่าช้ามาก** เป็น 0 (ศูนย์) วัน</span><span class="sxs-lookup"><span data-stu-id="0c9a0-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="0c9a0-113">ด้วยวิธีนี้ คุณจะยุบการคาดการณ์ไปยังสถานะไบนารีของ **ตรงเวลา** หรือ **ล่าช้า** ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="0c9a0-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="0c9a0-114">เลือกฟิลด์</span><span class="sxs-lookup"><span data-stu-id="0c9a0-114">Select fields</span></span>

<span data-ttu-id="0c9a0-115">เมื่อคุณกำลังเลือกฟิลด์ที่จะรวมไว้ในแบบจำลอง ให้ทราบว่ารายชื่อมีฟิลด์ที่พร้อมใช้งานทั้งหมดในตาราง Microsoft Dataverse ที่ถูกแม็ปกับข้อมูลในที่จัดเก็บข้อมูลดิบ Azure</span><span class="sxs-lookup"><span data-stu-id="0c9a0-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="0c9a0-116">บางฟิลด์เหล่านี้ **ไม่** ควรเลือก</span><span class="sxs-lookup"><span data-stu-id="0c9a0-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="0c9a0-117">ฟิลด์ที่ไม่ควรมีการเลือกอยู่เป็นหนึ่งในสามประเภทดังนี้</span><span class="sxs-lookup"><span data-stu-id="0c9a0-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="0c9a0-118">ฟิลด์นี้จำเป็นสำหรับตาราง Dataverse แต่ไม่มีข้อมูลที่สำรองไว้ในที่จัดเก็บข้อมูลดิบ</span><span class="sxs-lookup"><span data-stu-id="0c9a0-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="0c9a0-119">ฟิลด์เป็นรหัส และดังนั้นจึงไม่ได้ทำให้รู้สึกสำหรับลักษณะการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="0c9a0-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="0c9a0-120">ฟิลด์นี้แสดงข้อมูลที่จะไม่พร้อมใช้งานในระหว่างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="0c9a0-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="0c9a0-121">ส่วนต่อไปนี้จะแสดงฟิลด์ที่พร้อมใช้งานสำหรับใบแจ้งหนี้และเอนทิตีของลูกค้า และแสดงรายการฟิลด์ที่ **ไม่** ควรเลือกสำหรับการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="0c9a0-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="0c9a0-122">ประเภทที่ระบุไว้สำหรับแต่ละฟิลด์เหล่านั้นอ้างอิงถึงประเภทในรายการข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="0c9a0-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="0c9a0-123">ตาราง Dataverse ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0c9a0-123">Invoice Dataverse table</span></span>

<span data-ttu-id="0c9a0-124">ภาพประกอบต่อไปนี้แสดงฟิลด์ที่ทีให้ใช้สำหรับตารางใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="0c9a0-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="0c9a0-125">[![ฟิลด์ที่พร้อมใช้งานสำหรับตารางใบแจ้งหนี้](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="0c9a0-126">ไม่ควรเลือกฟิลด์ต่อไปนี้สำหรับการฝึกอบรม:</span><span class="sxs-lookup"><span data-stu-id="0c9a0-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="0c9a0-127">**บัญชีใบแจ้งหนี้** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="0c9a0-128">**ปิด** (ประเภท 3) – ฟิลด์นี้จะใช้ในการกรองข้อมูลใบแจ้งหนี้สำหรับการฝึกอบรม (ปิด) และการคาดการณ์ (ไม่ได้ปิด)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="0c9a0-129">**ชื่อ** (ประเภท 1)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-129">**Name** (category 1)</span></span>
- <span data-ttu-id="0c9a0-130">**รหัสที่มา** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="0c9a0-131">**เรกคอร์ดที่มา** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="0c9a0-132">**ตารางที่มา** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="0c9a0-133">ตาราง Dataverse ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0c9a0-133">Customer Dataverse table</span></span>

<span data-ttu-id="0c9a0-134">ภาพประกอบต่อไปนี้แสดงฟิลด์ที่ทีให้ใช้สำหรับตารางลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0c9a0-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="0c9a0-135">[![ฟิลด์ที่พร้อมใช้งานสำหรับตารางลูกค้า](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="0c9a0-136">ไม่ควรเลือกฟิลด์ต่อไปนี้สำหรับการฝึกอบรม:</span><span class="sxs-lookup"><span data-stu-id="0c9a0-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="0c9a0-137">**คีย์ที่ไม่ซ้ำกันของแถว** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="0c9a0-138">ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0c9a0-138">Filters</span></span>

<span data-ttu-id="0c9a0-139">ตัวกรองข้อมูลไม่สนับสนุนสถานการณ์จำลองการคาดการณ์การชำระเงินของลูกค้าในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="0c9a0-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="0c9a0-140">ดังนั้น ให้เลือก **ข้ามขั้นตอนนี้** และดำเนินการต่อไปยังหน้าสรุป</span><span class="sxs-lookup"><span data-stu-id="0c9a0-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="0c9a0-141">[![แบบจำลองโฟกัสที่มีตัวกรอง](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="0c9a0-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="0c9a0-142">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="0c9a0-142">Privacy notice</span></span>
<span data-ttu-id="0c9a0-143">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="0c9a0-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
