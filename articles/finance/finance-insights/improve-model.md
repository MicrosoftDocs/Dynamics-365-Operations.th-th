---
title: ปรับปรุงแบบจำลองการคาดคะเน (ตัวอย่าง)
description: หัวข้อนี้อธิบายถึงลักษณะการทำงานที่คุณสามารถใช้เพื่อปรับปรุงประสิทธิภาพการทำงานของแบบจำลองการคาดการณ์
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186653"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="d0c14-103">ปรับปรุงแบบจำลองการคาดคะเน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="d0c14-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d0c14-104">หัวข้อนี้อธิบายถึงลักษณะการทำงานที่คุณสามารถใช้เพื่อปรับปรุงประสิทธิภาพการทำงานของแบบจำลองการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d0c14-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="d0c14-105">คุณเริ่มต้นการปรับปรุงแบบจำลองของคุณในพื้นที่ทำงาน **การคาดการณ์การชำระเงินของลูกค้า** ใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d0c14-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="d0c14-106">ดำเนินการขั้นตอนการปรับปรุงเสร็จสมบูรณ์แล้วใน AI Builder</span><span class="sxs-lookup"><span data-stu-id="d0c14-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="d0c14-107">เลือกผลลัพธ์ในอดีต</span><span class="sxs-lookup"><span data-stu-id="d0c14-107">Select historical outcomes</span></span>

<span data-ttu-id="d0c14-108">คุณเลือกหนึ่งในผลลัพธ์ที่เป็นไปได้ที่เป็นไปได้สำหรับใบแจ้งหนี้อย่างน้อยหนึ่งรายการ: **ตรงเวลา** **ล่าช้า** และ **ล่าช้ามาก**</span><span class="sxs-lookup"><span data-stu-id="d0c14-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="d0c14-109">ควรเลือกผลลัพธ์ทั้งสามประการ</span><span class="sxs-lookup"><span data-stu-id="d0c14-109">All three outcomes should be selected.</span></span> <span data-ttu-id="d0c14-110">ถ้าคุณยกเลิกการเลือกผลลัพธ์ใด ๆ ใบแจ้งหนี้จะถูกกรองออกจากกระบวนการฝึกอบรมและความถูกต้องของการคาดการณ์จะถูกลดลง</span><span class="sxs-lookup"><span data-stu-id="d0c14-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="d0c14-111">[![การยืนยันผลลัพธ์](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="d0c14-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="d0c14-112">ถ้าองค์กรของคุณต้องการผลลัพธ์เพียงสองประการ ให้เปลี่ยนขีดจำกัด **ล่าช้า** และ **ล่าช้ามาก** เป็น 0 (ศูนย์) วัน</span><span class="sxs-lookup"><span data-stu-id="d0c14-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="d0c14-113">ด้วยวิธีนี้ คุณจะยุบการคาดการณ์ไปยังสถานะไบนารีของ **ตรงเวลา** หรือ **ล่าช้า** ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="d0c14-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="d0c14-114">เลือกฟิลด์</span><span class="sxs-lookup"><span data-stu-id="d0c14-114">Select fields</span></span>

<span data-ttu-id="d0c14-115">เมื่อคุณกำลังเลือกฟิลด์ที่จะรวมไว้ในแบบจำลอง ให้ทราบว่ารายชื่อมีฟิลด์ที่พร้อมใช้งานทั้งหมดในตาราง Microsoft Dataverse ที่ถูกแม็ปกับข้อมูลในที่จัดเก็บข้อมูลดิบ Azure</span><span class="sxs-lookup"><span data-stu-id="d0c14-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="d0c14-116">บางฟิลด์เหล่านี้ **ไม่** ควรเลือก</span><span class="sxs-lookup"><span data-stu-id="d0c14-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="d0c14-117">ฟิลด์ที่ไม่ควรมีการเลือกอยู่เป็นหนึ่งในสามประเภทดังนี้</span><span class="sxs-lookup"><span data-stu-id="d0c14-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="d0c14-118">ฟิลด์นี้จำเป็นสำหรับตาราง Dataverse แต่ไม่มีข้อมูลที่สำรองไว้ในที่จัดเก็บข้อมูลดิบ</span><span class="sxs-lookup"><span data-stu-id="d0c14-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="d0c14-119">ฟิลด์เป็นรหัส และดังนั้นจึงไม่ได้ทำให้รู้สึกสำหรับลักษณะการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="d0c14-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="d0c14-120">ฟิลด์นี้แสดงข้อมูลที่จะไม่พร้อมใช้งานในระหว่างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d0c14-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="d0c14-121">ส่วนต่อไปนี้จะแสดงฟิลด์ที่พร้อมใช้งานสำหรับใบแจ้งหนี้และเอนทิตีของลูกค้า และแสดงรายการฟิลด์ที่ **ไม่** ควรเลือกสำหรับการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="d0c14-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="d0c14-122">ประเภทที่ระบุไว้สำหรับแต่ละฟิลด์เหล่านั้นอ้างอิงถึงประเภทในรายการข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="d0c14-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="d0c14-123">ตาราง Dataverse ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d0c14-123">Invoice Dataverse table</span></span>

<span data-ttu-id="d0c14-124">ภาพประกอบต่อไปนี้แสดงฟิลด์ที่ทีให้ใช้สำหรับตารางใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d0c14-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="d0c14-125">[![ฟิลด์ที่พร้อมใช้งานสำหรับตารางใบแจ้งหนี้](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="d0c14-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="d0c14-126">ไม่ควรเลือกฟิลด์ต่อไปนี้สำหรับการฝึกอบรม:</span><span class="sxs-lookup"><span data-stu-id="d0c14-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="d0c14-127">**บัญชีใบแจ้งหนี้** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="d0c14-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="d0c14-128">**ปิด** (ประเภท 3) – ฟิลด์นี้จะใช้ในการกรองข้อมูลใบแจ้งหนี้สำหรับการฝึกอบรม (ปิด) และการคาดการณ์ (ไม่ได้ปิด)</span><span class="sxs-lookup"><span data-stu-id="d0c14-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="d0c14-129">**ชื่อ** (ประเภท 1)</span><span class="sxs-lookup"><span data-stu-id="d0c14-129">**Name** (category 1)</span></span>
- <span data-ttu-id="d0c14-130">**รหัสที่มา** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="d0c14-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="d0c14-131">**เรกคอร์ดที่มา** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="d0c14-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="d0c14-132">**ตารางที่มา** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="d0c14-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="d0c14-133">ตาราง Dataverse ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d0c14-133">Customer Dataverse table</span></span>

<span data-ttu-id="d0c14-134">ภาพประกอบต่อไปนี้แสดงฟิลด์ที่ทีให้ใช้สำหรับตารางลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d0c14-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="d0c14-135">[![ฟิลด์ที่พร้อมใช้งานสำหรับตารางลูกค้า](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="d0c14-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="d0c14-136">ไม่ควรเลือกฟิลด์ต่อไปนี้สำหรับการฝึกอบรม:</span><span class="sxs-lookup"><span data-stu-id="d0c14-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="d0c14-137">**คีย์ที่ไม่ซ้ำกันของแถว** (ประเภท 2)</span><span class="sxs-lookup"><span data-stu-id="d0c14-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="d0c14-138">ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d0c14-138">Filters</span></span>

<span data-ttu-id="d0c14-139">ตัวกรองข้อมูลไม่สนับสนุนสถานการณ์จำลองการคาดการณ์การชำระเงินของลูกค้าในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d0c14-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="d0c14-140">ดังนั้น ให้เลือก **ข้ามขั้นตอนนี้** และดำเนินการต่อไปยังหน้าสรุป</span><span class="sxs-lookup"><span data-stu-id="d0c14-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="d0c14-141">[![แบบจำลองโฟกัสที่มีตัวกรอง](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="d0c14-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
