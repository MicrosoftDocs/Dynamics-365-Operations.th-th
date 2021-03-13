---
title: ระดับการประเมิน
description: หัวข้อนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125268"
---
# <a name="rating-level"></a><span data-ttu-id="3a2a1-103">ระดับการประเมิน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-103">Rating level</span></span>

<span data-ttu-id="3a2a1-104">หัวข้อนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="3a2a1-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3a2a1-105">ชื่อทางกายภาพ: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="3a2a1-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="3a2a1-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3a2a1-106">Description</span></span>

<span data-ttu-id="3a2a1-107">เอนทิตี้นี้จะให้ระดับการจัดอันดับที่พร้อมใช้งานสำหรับทักษะต่างๆ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="3a2a1-108">ระดับการจัดอันดับใช้ระหว่างนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3a2a1-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3a2a1-109">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="3a2a1-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="3a2a1-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-110">Properties</span></span>

| <span data-ttu-id="3a2a1-111">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-111">Property</span></span><br><span data-ttu-id="3a2a1-112">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-112">**Physical name**</span></span><br><span data-ttu-id="3a2a1-113">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-113">**_Type_**</span></span> | <span data-ttu-id="3a2a1-114">ใช้</span><span class="sxs-lookup"><span data-stu-id="3a2a1-114">Use</span></span> | <span data-ttu-id="3a2a1-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3a2a1-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3a2a1-116">**รหัสเอนทิตี้ระดับการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="3a2a1-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="3a2a1-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="3a2a1-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-118">*GUID*</span></span> | <span data-ttu-id="3a2a1-119">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="3a2a1-119">Read-only</span></span><br><span data-ttu-id="3a2a1-120">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-120">Required</span></span><br><span data-ttu-id="3a2a1-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3a2a1-121">System-generated</span></span> | <span data-ttu-id="3a2a1-122">ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="3a2a1-123">**รหัสระดับของการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-123">**Rating Level ID**</span></span><br><span data-ttu-id="3a2a1-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="3a2a1-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="3a2a1-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-125">*String*</span></span> | <span data-ttu-id="3a2a1-126">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-126">Read/write</span></span><br><span data-ttu-id="3a2a1-127">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-127">Required</span></span> | <span data-ttu-id="3a2a1-128">ตัวระบุเฉพาะที่ผู้ใช้สามารถอ่านได้สำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="3a2a1-129">**รหัสแบบจำลองการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-129">**Rating Model ID**</span></span><br><span data-ttu-id="3a2a1-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="3a2a1-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="3a2a1-131">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-131">*String*</span></span> | <span data-ttu-id="3a2a1-132">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-132">Read/write</span></span><br><span data-ttu-id="3a2a1-133">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-133">Required</span></span> | <span data-ttu-id="3a2a1-134">แบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="3a2a1-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3a2a1-135">**รหัสเอนทิตี้แบบจำลองการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="3a2a1-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="3a2a1-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="3a2a1-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-137">*GUID*</span></span> | <span data-ttu-id="3a2a1-138">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="3a2a1-138">Read-only</span></span><br><span data-ttu-id="3a2a1-139">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-139">Required</span></span><br><span data-ttu-id="3a2a1-140">คีย์นอก: mshr_hcmratingmodelentityid ของ mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="3a2a1-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="3a2a1-141">ตัวระบุที่สร้างขึ้นสำหรับแบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="3a2a1-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3a2a1-142">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-142">**Description**</span></span><br><span data-ttu-id="3a2a1-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3a2a1-143">mshr_description</span></span><br><span data-ttu-id="3a2a1-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-144">*String*</span></span> | <span data-ttu-id="3a2a1-145">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-145">Read/write</span></span><br><span data-ttu-id="3a2a1-146">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-146">Required</span></span> | <span data-ttu-id="3a2a1-147">คำอธิบายของระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-147">The description of the rating level.</span></span> |
| <span data-ttu-id="3a2a1-148">**แฟคเตอร์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-148">**Factor**</span></span><br><span data-ttu-id="3a2a1-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="3a2a1-149">mshr_factor</span></span><br><span data-ttu-id="3a2a1-150">*เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-150">*Integer*</span></span> | <span data-ttu-id="3a2a1-151">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-151">Read/write</span></span><br><span data-ttu-id="3a2a1-152">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-152">Required</span></span> | <span data-ttu-id="3a2a1-153">ตัวคูณสำหรับระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-153">The factor for the rating level.</span></span> <span data-ttu-id="3a2a1-154">เมื่อคุณเปรียบเทียบรายการที่มีหมายเลขที่แตกต่างกันของระดับการจัดอันดับ ตัวคูณจะใช้เพื่อปรับคะแนนให้เป็นค่าปกติ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="3a2a1-155">ค่าต้องเป็นเลขจํานวนเต็มระหว่าง 0 ถึง 9</span><span class="sxs-lookup"><span data-stu-id="3a2a1-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="3a2a1-156">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-156">**Note**</span></span><br><span data-ttu-id="3a2a1-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="3a2a1-157">mshr_note</span></span><br><span data-ttu-id="3a2a1-158">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-158">*String*</span></span> | <span data-ttu-id="3a2a1-159">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-159">Read/write</span></span><br><span data-ttu-id="3a2a1-160">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-160">Optional</span></span> | <span data-ttu-id="3a2a1-161">หมายเหตุใดๆที่สัมพันธ์กับระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="3a2a1-162">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="3a2a1-162">**Primary Field**</span></span><br><span data-ttu-id="3a2a1-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3a2a1-163">mshr_primaryfield</span></span><br><span data-ttu-id="3a2a1-164">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="3a2a1-164">*String*</span></span> | <span data-ttu-id="3a2a1-165">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="3a2a1-165">Read-only</span></span><br><span data-ttu-id="3a2a1-166">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-166">Required</span></span> | <span data-ttu-id="3a2a1-167">ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3a2a1-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="3a2a1-168">ชุดของรหัสระดับการจัดอันดับและรหัสแบบจำลองการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3a2a1-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3a2a1-169">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3a2a1-169">See also</span></span>

[<span data-ttu-id="3a2a1-170">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="3a2a1-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3a2a1-171">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="3a2a1-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

