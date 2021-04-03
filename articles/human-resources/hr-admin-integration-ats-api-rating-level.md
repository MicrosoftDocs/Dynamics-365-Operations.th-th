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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464753"
---
# <a name="rating-level"></a><span data-ttu-id="75d00-103">ระดับการประเมิน</span><span class="sxs-lookup"><span data-stu-id="75d00-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="75d00-104">หัวข้อนี้อธิบายเอนทิตี้ระดับการจัดอันดับสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="75d00-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="75d00-105">ชื่อทางกายภาพ: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="75d00-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="75d00-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="75d00-106">Description</span></span>

<span data-ttu-id="75d00-107">เอนทิตี้นี้จะให้ระดับการจัดอันดับที่พร้อมใช้งานสำหรับทักษะต่างๆ</span><span class="sxs-lookup"><span data-stu-id="75d00-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="75d00-108">ระดับการจัดอันดับใช้ระหว่างนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="75d00-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="75d00-109">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="75d00-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="75d00-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="75d00-110">Properties</span></span>

| <span data-ttu-id="75d00-111">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="75d00-111">Property</span></span><br><span data-ttu-id="75d00-112">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="75d00-112">**Physical name**</span></span><br><span data-ttu-id="75d00-113">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="75d00-113">**_Type_**</span></span> | <span data-ttu-id="75d00-114">ใช้</span><span class="sxs-lookup"><span data-stu-id="75d00-114">Use</span></span> | <span data-ttu-id="75d00-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="75d00-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="75d00-116">**รหัสเอนทิตี้ระดับการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="75d00-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="75d00-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="75d00-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="75d00-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75d00-118">*GUID*</span></span> | <span data-ttu-id="75d00-119">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="75d00-119">Read-only</span></span><br><span data-ttu-id="75d00-120">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-120">Required</span></span><br><span data-ttu-id="75d00-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="75d00-121">System-generated</span></span> | <span data-ttu-id="75d00-122">ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="75d00-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="75d00-123">**รหัสระดับของการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="75d00-123">**Rating Level ID**</span></span><br><span data-ttu-id="75d00-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="75d00-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="75d00-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d00-125">*String*</span></span> | <span data-ttu-id="75d00-126">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="75d00-126">Read/write</span></span><br><span data-ttu-id="75d00-127">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-127">Required</span></span> | <span data-ttu-id="75d00-128">ตัวระบุเฉพาะที่ผู้ใช้สามารถอ่านได้สำหรับระดับ</span><span class="sxs-lookup"><span data-stu-id="75d00-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="75d00-129">**รหัสแบบจำลองการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="75d00-129">**Rating Model ID**</span></span><br><span data-ttu-id="75d00-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="75d00-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="75d00-131">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d00-131">*String*</span></span> | <span data-ttu-id="75d00-132">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="75d00-132">Read/write</span></span><br><span data-ttu-id="75d00-133">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-133">Required</span></span> | <span data-ttu-id="75d00-134">แบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="75d00-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="75d00-135">**รหัสเอนทิตี้แบบจำลองการจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="75d00-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="75d00-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="75d00-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="75d00-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75d00-137">*GUID*</span></span> | <span data-ttu-id="75d00-138">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="75d00-138">Read-only</span></span><br><span data-ttu-id="75d00-139">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-139">Required</span></span><br><span data-ttu-id="75d00-140">คีย์นอก: mshr_hcmratingmodelentityid ของ mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="75d00-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="75d00-141">ตัวระบุที่สร้างขึ้นสำหรับแบบจำลองการจัดอันดับซึ่งระดับการจัดอันดับเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="75d00-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="75d00-142">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="75d00-142">**Description**</span></span><br><span data-ttu-id="75d00-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="75d00-143">mshr_description</span></span><br><span data-ttu-id="75d00-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d00-144">*String*</span></span> | <span data-ttu-id="75d00-145">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="75d00-145">Read/write</span></span><br><span data-ttu-id="75d00-146">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-146">Required</span></span> | <span data-ttu-id="75d00-147">คำอธิบายของระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="75d00-147">The description of the rating level.</span></span> |
| <span data-ttu-id="75d00-148">**แฟคเตอร์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="75d00-148">**Factor**</span></span><br><span data-ttu-id="75d00-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="75d00-149">mshr_factor</span></span><br><span data-ttu-id="75d00-150">*เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="75d00-150">*Integer*</span></span> | <span data-ttu-id="75d00-151">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="75d00-151">Read/write</span></span><br><span data-ttu-id="75d00-152">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-152">Required</span></span> | <span data-ttu-id="75d00-153">ตัวคูณสำหรับระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="75d00-153">The factor for the rating level.</span></span> <span data-ttu-id="75d00-154">เมื่อคุณเปรียบเทียบรายการที่มีหมายเลขที่แตกต่างกันของระดับการจัดอันดับ ตัวคูณจะใช้เพื่อปรับคะแนนให้เป็นค่าปกติ</span><span class="sxs-lookup"><span data-stu-id="75d00-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="75d00-155">ค่าต้องเป็นเลขจํานวนเต็มระหว่าง 0 ถึง 9</span><span class="sxs-lookup"><span data-stu-id="75d00-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="75d00-156">**หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="75d00-156">**Note**</span></span><br><span data-ttu-id="75d00-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="75d00-157">mshr_note</span></span><br><span data-ttu-id="75d00-158">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d00-158">*String*</span></span> | <span data-ttu-id="75d00-159">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="75d00-159">Read/write</span></span><br><span data-ttu-id="75d00-160">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-160">Optional</span></span> | <span data-ttu-id="75d00-161">หมายเหตุใดๆที่สัมพันธ์กับระดับการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="75d00-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="75d00-162">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="75d00-162">**Primary Field**</span></span><br><span data-ttu-id="75d00-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="75d00-163">mshr_primaryfield</span></span><br><span data-ttu-id="75d00-164">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="75d00-164">*String*</span></span> | <span data-ttu-id="75d00-165">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="75d00-165">Read-only</span></span><br><span data-ttu-id="75d00-166">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="75d00-166">Required</span></span> | <span data-ttu-id="75d00-167">ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="75d00-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="75d00-168">ชุดของรหัสระดับการจัดอันดับและรหัสแบบจำลองการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="75d00-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="75d00-169">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="75d00-169">See also</span></span>

[<span data-ttu-id="75d00-170">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="75d00-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="75d00-171">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="75d00-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]