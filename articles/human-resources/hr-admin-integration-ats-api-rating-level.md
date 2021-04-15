---
title: ระดับการประเมิน
description: หัวข้อนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800344"
---
# <a name="rating-level"></a><span data-ttu-id="dce74-103">ระดับการประเมิน</span><span class="sxs-lookup"><span data-stu-id="dce74-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dce74-104">หัวข้อนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="dce74-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="dce74-105">ชื่อทางกายภาพ: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="dce74-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="dce74-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="dce74-106">Description</span></span>

<span data-ttu-id="dce74-107">เอนทิตี้นี้จะให้ระดับการจัดอันดับที่พร้อมใช้งานสำหรับทักษะต่างๆ</span><span class="sxs-lookup"><span data-stu-id="dce74-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="dce74-108">ระดับการจัดอันดับใช้ระหว่างนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dce74-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dce74-109">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="dce74-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="dce74-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="dce74-110">Properties</span></span>

| <span data-ttu-id="dce74-111">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="dce74-111">Property</span></span><br><span data-ttu-id="dce74-112">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="dce74-112">**Physical name**</span></span><br><span data-ttu-id="dce74-113">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="dce74-113">**_Type_**</span></span> | <span data-ttu-id="dce74-114">ใช้</span><span class="sxs-lookup"><span data-stu-id="dce74-114">Use</span></span> | <span data-ttu-id="dce74-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="dce74-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dce74-116">**รหัสเอนทิตี้ระดับการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="dce74-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="dce74-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="dce74-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="dce74-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="dce74-118">*GUID*</span></span> | <span data-ttu-id="dce74-119">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="dce74-119">Read-only</span></span><br><span data-ttu-id="dce74-120">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-120">Required</span></span><br><span data-ttu-id="dce74-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="dce74-121">System-generated</span></span> | <span data-ttu-id="dce74-122">ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="dce74-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="dce74-123">**รหัสระดับของการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="dce74-123">**Rating Level ID**</span></span><br><span data-ttu-id="dce74-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="dce74-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="dce74-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="dce74-125">*String*</span></span> | <span data-ttu-id="dce74-126">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="dce74-126">Read/write</span></span><br><span data-ttu-id="dce74-127">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-127">Required</span></span> | <span data-ttu-id="dce74-128">ตัวระบุเฉพาะที่ผู้ใช้สามารถอ่านได้สำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="dce74-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="dce74-129">**รหัสแบบจำลองการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="dce74-129">**Rating Model ID**</span></span><br><span data-ttu-id="dce74-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="dce74-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="dce74-131">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="dce74-131">*String*</span></span> | <span data-ttu-id="dce74-132">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="dce74-132">Read/write</span></span><br><span data-ttu-id="dce74-133">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-133">Required</span></span> | <span data-ttu-id="dce74-134">แบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="dce74-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="dce74-135">**รหัสเอนทิตี้แบบจำลองการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="dce74-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="dce74-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="dce74-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="dce74-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="dce74-137">*GUID*</span></span> | <span data-ttu-id="dce74-138">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="dce74-138">Read-only</span></span><br><span data-ttu-id="dce74-139">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-139">Required</span></span><br><span data-ttu-id="dce74-140">คีย์นอก: mshr_hcmratingmodelentityid ของ mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="dce74-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="dce74-141">ตัวระบุที่สร้างขึ้นสำหรับแบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="dce74-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="dce74-142">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="dce74-142">**Description**</span></span><br><span data-ttu-id="dce74-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="dce74-143">mshr_description</span></span><br><span data-ttu-id="dce74-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="dce74-144">*String*</span></span> | <span data-ttu-id="dce74-145">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="dce74-145">Read/write</span></span><br><span data-ttu-id="dce74-146">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-146">Required</span></span> | <span data-ttu-id="dce74-147">คำอธิบายของระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="dce74-147">The description of the rating level.</span></span> |
| <span data-ttu-id="dce74-148">**แฟคเตอร์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="dce74-148">**Factor**</span></span><br><span data-ttu-id="dce74-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="dce74-149">mshr_factor</span></span><br><span data-ttu-id="dce74-150">*เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="dce74-150">*Integer*</span></span> | <span data-ttu-id="dce74-151">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="dce74-151">Read/write</span></span><br><span data-ttu-id="dce74-152">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-152">Required</span></span> | <span data-ttu-id="dce74-153">ตัวคูณสำหรับระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="dce74-153">The factor for the rating level.</span></span> <span data-ttu-id="dce74-154">เมื่อคุณเปรียบเทียบรายการที่มีหมายเลขที่แตกต่างกันของระดับการจัดอันดับ ตัวคูณจะใช้เพื่อปรับคะแนนให้เป็นค่าปกติ</span><span class="sxs-lookup"><span data-stu-id="dce74-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="dce74-155">ค่าต้องเป็นเลขจํานวนเต็มระหว่าง 0 ถึง 9</span><span class="sxs-lookup"><span data-stu-id="dce74-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="dce74-156">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="dce74-156">**Note**</span></span><br><span data-ttu-id="dce74-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="dce74-157">mshr_note</span></span><br><span data-ttu-id="dce74-158">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="dce74-158">*String*</span></span> | <span data-ttu-id="dce74-159">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="dce74-159">Read/write</span></span><br><span data-ttu-id="dce74-160">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-160">Optional</span></span> | <span data-ttu-id="dce74-161">หมายเหตุใดๆที่สัมพันธ์กับระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="dce74-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="dce74-162">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="dce74-162">**Primary Field**</span></span><br><span data-ttu-id="dce74-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="dce74-163">mshr_primaryfield</span></span><br><span data-ttu-id="dce74-164">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="dce74-164">*String*</span></span> | <span data-ttu-id="dce74-165">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="dce74-165">Read-only</span></span><br><span data-ttu-id="dce74-166">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="dce74-166">Required</span></span> | <span data-ttu-id="dce74-167">ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="dce74-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="dce74-168">ชุดของรหัสระดับการจัดอันดับและรหัสแบบจำลองการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="dce74-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="dce74-169">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="dce74-169">See also</span></span>

[<span data-ttu-id="dce74-170">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="dce74-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="dce74-171">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="dce74-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]