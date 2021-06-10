---
title: ใบรับรองของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ใบรับรองของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055207"
---
# <a name="person-certificate"></a><span data-ttu-id="ae1fe-103">ใบรับรองของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ae1fe-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ae1fe-104">หัวข้อนี้อธิบายเอนทิตี้ใบรับรองของบุคคลสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="ae1fe-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ae1fe-105">ชื่อทางกายภาพ: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="ae1fe-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="ae1fe-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ae1fe-106">Description</span></span>

<span data-ttu-id="ae1fe-107">เอนทิตี้นี้จะอธิบายถึงใบรับรองวิชาชีพของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="ae1fe-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ae1fe-108">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="ae1fe-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ae1fe-109">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-109">Properties</span></span>

| <span data-ttu-id="ae1fe-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-110">Property</span></span><br><span data-ttu-id="ae1fe-111">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-111">**Physical name**</span></span><br><span data-ttu-id="ae1fe-112">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-112">**_Type_**</span></span> | <span data-ttu-id="ae1fe-113">ใช้</span><span class="sxs-lookup"><span data-stu-id="ae1fe-113">Use</span></span> | <span data-ttu-id="ae1fe-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ae1fe-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae1fe-115">**รหัสเอนทิตี้ใบรับรองของบุคคล**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="ae1fe-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="ae1fe-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="ae1fe-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-117">*GUID*</span></span> | <span data-ttu-id="ae1fe-118">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ae1fe-118">Read-only</span></span><br><span data-ttu-id="ae1fe-119">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-119">Required</span></span> | <span data-ttu-id="ae1fe-120">ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้ใบรับรองของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ae1fe-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="ae1fe-121">**หมายเลขฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-121">**Party Number**</span></span><br><span data-ttu-id="ae1fe-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="ae1fe-122">mshr_partynumber</span></span><br><span data-ttu-id="ae1fe-123">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-123">*String*</span></span> | <span data-ttu-id="ae1fe-124">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="ae1fe-124">Read/write</span></span><br><span data-ttu-id="ae1fe-125">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-125">Required</span></span> | <span data-ttu-id="ae1fe-126">รหัสฝ่าย (บุคคล) ของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="ae1fe-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="ae1fe-127">**ค่ารหัสบุคคล**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-127">**Person ID Value**</span></span><br><span data-ttu-id="ae1fe-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="ae1fe-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="ae1fe-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-129">*GUID*</span></span> | <span data-ttu-id="ae1fe-130">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ae1fe-130">Read-only</span></span><br><span data-ttu-id="ae1fe-131">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-131">Required</span></span><br><span data-ttu-id="ae1fe-132">คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="ae1fe-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="ae1fe-133">ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล)</span><span class="sxs-lookup"><span data-stu-id="ae1fe-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="ae1fe-134">**รหัสชนิดใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-134">**Certificate Type ID**</span></span><br><span data-ttu-id="ae1fe-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="ae1fe-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="ae1fe-136">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-136">*String*</span></span> | <span data-ttu-id="ae1fe-137">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="ae1fe-137">Read/write</span></span><br><span data-ttu-id="ae1fe-138">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-138">Required</span></span> |  <span data-ttu-id="ae1fe-139">ตัวระบุของชนิดใบรับรองที่กําหนดในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="ae1fe-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="ae1fe-140">**ค่ารหัสชนิดใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="ae1fe-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="ae1fe-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="ae1fe-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-142">*GUID*</span></span> | <span data-ttu-id="ae1fe-143">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ae1fe-143">Read-only</span></span><br><span data-ttu-id="ae1fe-144">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-144">Required</span></span><br><span data-ttu-id="ae1fe-145">คีย์นอก: mshr_hcmcertificatetypeentityid ของ mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="ae1fe-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="ae1fe-146">ตัวระบุเฉพาะที่ระบบสร้างขึ้นของชนิดใบรับรองในเอนทิตี้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ae1fe-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="ae1fe-147">**วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-147">**Start Date**</span></span><br><span data-ttu-id="ae1fe-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="ae1fe-148">mshr_startdate</span></span><br><span data-ttu-id="ae1fe-149">*วันเวลา*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-149">*Datetime*</span></span> | <span data-ttu-id="ae1fe-150">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="ae1fe-150">Read/write</span></span><br><span data-ttu-id="ae1fe-151">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-151">Required</span></span> | <span data-ttu-id="ae1fe-152">วันที่ที่ใบรับรองได้รับการออก</span><span class="sxs-lookup"><span data-stu-id="ae1fe-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="ae1fe-153">**วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-153">**End Date**</span></span><br><span data-ttu-id="ae1fe-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="ae1fe-154">mshr_enddate</span></span><br><span data-ttu-id="ae1fe-155">*วันเวลา*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-155">*Datetime*</span></span> | <span data-ttu-id="ae1fe-156">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="ae1fe-156">Read/write</span></span><br><span data-ttu-id="ae1fe-157">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-157">Optional</span></span> | <span data-ttu-id="ae1fe-158">วันที่ที่ใบรับรองจะหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="ae1fe-159">**บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-159">**Notes**</span></span><br><span data-ttu-id="ae1fe-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="ae1fe-160">mshr_notes</span></span><br><span data-ttu-id="ae1fe-161">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-161">*String*</span></span> | <span data-ttu-id="ae1fe-162">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="ae1fe-162">Read/write</span></span><br><span data-ttu-id="ae1fe-163">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-163">Optional</span></span> | <span data-ttu-id="ae1fe-164">หมายเหตุที่ใช้โดยผู้จัดการการจ้างงานหรือผู้จัดหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ae1fe-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="ae1fe-165">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="ae1fe-165">**Primary Field**</span></span><br><span data-ttu-id="ae1fe-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="ae1fe-166">mshr_primaryfield</span></span><br><span data-ttu-id="ae1fe-167">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="ae1fe-167">*String*</span></span> | <span data-ttu-id="ae1fe-168">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ae1fe-168">Read-only</span></span><br><span data-ttu-id="ae1fe-169">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="ae1fe-169">Required</span></span> |  <span data-ttu-id="ae1fe-170">ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ae1fe-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="ae1fe-171">ชุดของหมายเลขฝ่าย รหัสชนิดใบรับรองและวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ae1fe-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae1fe-172">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ae1fe-172">See also</span></span>

[<span data-ttu-id="ae1fe-173">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="ae1fe-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ae1fe-174">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="ae1fe-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]