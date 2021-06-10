---
title: การคัดเลือกบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้การสรรหาบุคลากรของบุคคลสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059291"
---
# <a name="person-screening"></a><span data-ttu-id="0de2e-103">การคัดเลือกบุคคล</span><span class="sxs-lookup"><span data-stu-id="0de2e-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0de2e-104">หัวข้อนี้อธิบายเอนทิตี้การสรรหาบุคลากรของบุคคลสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="0de2e-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0de2e-105">ชื่อทางกายภาพ: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="0de2e-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="0de2e-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="0de2e-106">Description</span></span>

<span data-ttu-id="0de2e-107">เอนทิตี้นี้จะอธิบายถึงการสรรหาผู้สมัครที่ผ่านหรือต้องผ่านสำหรับการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="0de2e-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0de2e-108">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="0de2e-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="0de2e-109">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0de2e-109">Properties</span></span>

| <span data-ttu-id="0de2e-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0de2e-110">Property</span></span><br><span data-ttu-id="0de2e-111">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="0de2e-111">**Physical name**</span></span><br><span data-ttu-id="0de2e-112">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="0de2e-112">**_Type_**</span></span> | <span data-ttu-id="0de2e-113">ใช้</span><span class="sxs-lookup"><span data-stu-id="0de2e-113">Use</span></span> | <span data-ttu-id="0de2e-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="0de2e-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0de2e-115">**รหัสเอนทิตี้การสรรหาของบุคคล**</span><span class="sxs-lookup"><span data-stu-id="0de2e-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="0de2e-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="0de2e-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="0de2e-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0de2e-117">*GUID*</span></span> | <span data-ttu-id="0de2e-118">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0de2e-118">Read-only</span></span><br><span data-ttu-id="0de2e-119">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-119">Required</span></span><br><span data-ttu-id="0de2e-120">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0de2e-120">System-generated</span></span> | <span data-ttu-id="0de2e-121">ตัวระบุหลักเฉพาะของเรกคอร์ดการสรรหาของบุคคล</span><span class="sxs-lookup"><span data-stu-id="0de2e-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="0de2e-122">**หมายเลขฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="0de2e-122">**Party Number**</span></span><br><span data-ttu-id="0de2e-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="0de2e-123">mshr_partynumber</span></span><br><span data-ttu-id="0de2e-124">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0de2e-124">*String*</span></span> | <span data-ttu-id="0de2e-125">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="0de2e-125">Read/write</span></span><br><span data-ttu-id="0de2e-126">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-126">Required</span></span> | <span data-ttu-id="0de2e-127">หมายเลขฝ่าย (บุคคล) ที่เชื่อมโยงกับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="0de2e-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="0de2e-128">**ค่ารหัสบุคคล**</span><span class="sxs-lookup"><span data-stu-id="0de2e-128">**Person ID Value**</span></span><br><span data-ttu-id="0de2e-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="0de2e-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="0de2e-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0de2e-130">*GUID*</span></span> | <span data-ttu-id="0de2e-131">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0de2e-131">Read-only</span></span><br><span data-ttu-id="0de2e-132">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-132">Required</span></span><br><span data-ttu-id="0de2e-133">คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="0de2e-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="0de2e-134">ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล)</span><span class="sxs-lookup"><span data-stu-id="0de2e-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="0de2e-135">**รหัสชนิดการคัดเลือก**</span><span class="sxs-lookup"><span data-stu-id="0de2e-135">**Screening Type ID**</span></span><br><span data-ttu-id="0de2e-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="0de2e-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="0de2e-137">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0de2e-137">*String*</span></span> | <span data-ttu-id="0de2e-138">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="0de2e-138">Read/write</span></span><br><span data-ttu-id="0de2e-139">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-139">Required</span></span><br><span data-ttu-id="0de2e-140">คีย์นอก: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="0de2e-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="0de2e-141">ตัวระบุของชนิดการคัดเลือกที่กําหนดในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="0de2e-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="0de2e-142">**ค่ารหัสชนิดการคัดเลือก**</span><span class="sxs-lookup"><span data-stu-id="0de2e-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="0de2e-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="0de2e-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="0de2e-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0de2e-144">*GUID*</span></span> | <span data-ttu-id="0de2e-145">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0de2e-145">Read-only</span></span><br><span data-ttu-id="0de2e-146">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-146">Required</span></span><br><span data-ttu-id="0de2e-147">คีย์นอก: mshr_hcmscreeningtypeentityid ของ mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="0de2e-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="0de2e-148">ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับชนิดการคัดเลือกในเอนทิตี้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0de2e-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="0de2e-149">**ต้องการภายใน**</span><span class="sxs-lookup"><span data-stu-id="0de2e-149">**Required By**</span></span><br><span data-ttu-id="0de2e-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="0de2e-150">mshr_requiredby</span></span><br><span data-ttu-id="0de2e-151">*วันเวลา*</span><span class="sxs-lookup"><span data-stu-id="0de2e-151">*Datetime*</span></span> | <span data-ttu-id="0de2e-152">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="0de2e-152">Read/write</span></span><br><span data-ttu-id="0de2e-153">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-153">Optional</span></span> | <span data-ttu-id="0de2e-154">วันที่ที่การคัดเลือกจำเป็นที่จะทำให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="0de2e-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="0de2e-155">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="0de2e-155">**Status**</span></span><br><span data-ttu-id="0de2e-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="0de2e-156">mshr_status</span></span><br><span data-ttu-id="0de2e-157">*การกำหนดตัวเลือก mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="0de2e-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="0de2e-158">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="0de2e-158">Read/write</span></span><br><span data-ttu-id="0de2e-159">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-159">Required</span></span> | <span data-ttu-id="0de2e-160">แสดงสถานะของผู้สมัครสำหรับการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="0de2e-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="0de2e-161">**วันที่เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="0de2e-161">**Completed Date**</span></span><br><span data-ttu-id="0de2e-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="0de2e-162">mshr_completeddate</span></span><br><span data-ttu-id="0de2e-163">*วันเวลา*</span><span class="sxs-lookup"><span data-stu-id="0de2e-163">*Datetime*</span></span> | <span data-ttu-id="0de2e-164">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="0de2e-164">Read/write</span></span><br><span data-ttu-id="0de2e-165">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-165">Optional</span></span> | <span data-ttu-id="0de2e-166">วันที่ที่การคัดเลือกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0de2e-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="0de2e-167">**บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="0de2e-167">**Notes**</span></span><br><span data-ttu-id="0de2e-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="0de2e-168">mshr_note</span></span><br><span data-ttu-id="0de2e-169">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0de2e-169">*String*</span></span> | <span data-ttu-id="0de2e-170">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="0de2e-170">Read/write</span></span><br><span data-ttu-id="0de2e-171">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0de2e-171">Optional</span></span> | <span data-ttu-id="0de2e-172">หมายเหตุที่ใช้โดยผู้จัดการการจ้างงานหรือผู้จัดหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="0de2e-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0de2e-173">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="0de2e-173">See also</span></span>

[<span data-ttu-id="0de2e-174">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="0de2e-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0de2e-175">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="0de2e-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]