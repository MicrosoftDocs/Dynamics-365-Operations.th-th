---
title: ใบรับรองของบุคคล
description: หัวข้อนี้อธิบายเอนทิตี้ใบรับรองของบุคคลสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125364"
---
# <a name="person-certificate"></a><span data-ttu-id="5a102-103">ใบรับรองของบุคคล</span><span class="sxs-lookup"><span data-stu-id="5a102-103">Person certificate</span></span>

<span data-ttu-id="5a102-104">หัวข้อนี้อธิบายเอนทิตี้ใบรับรองของบุคคลสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="5a102-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5a102-105">ชื่อทางกายภาพ: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="5a102-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="5a102-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5a102-106">Description</span></span>

<span data-ttu-id="5a102-107">เอนทิตี้นี้จะอธิบายถึงใบรับรองวิชาชีพของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="5a102-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5a102-108">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="5a102-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="5a102-109">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="5a102-109">Properties</span></span>

| <span data-ttu-id="5a102-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="5a102-110">Property</span></span><br><span data-ttu-id="5a102-111">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="5a102-111">**Physical name**</span></span><br><span data-ttu-id="5a102-112">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="5a102-112">**_Type_**</span></span> | <span data-ttu-id="5a102-113">ใช้</span><span class="sxs-lookup"><span data-stu-id="5a102-113">Use</span></span> | <span data-ttu-id="5a102-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5a102-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5a102-115">**รหัสเอนทิตี้ใบรับรองของบุคคล**</span><span class="sxs-lookup"><span data-stu-id="5a102-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="5a102-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="5a102-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="5a102-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5a102-117">*GUID*</span></span> | <span data-ttu-id="5a102-118">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="5a102-118">Read-only</span></span><br><span data-ttu-id="5a102-119">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-119">Required</span></span> | <span data-ttu-id="5a102-120">ตัวระบุเฉพาะที่ระบบสร้างขึ้นสำหรับเรกคอร์ดเอนทิตี้ใบรับรองของบุคคล</span><span class="sxs-lookup"><span data-stu-id="5a102-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="5a102-121">**หมายเลขฝ่าย**</span><span class="sxs-lookup"><span data-stu-id="5a102-121">**Party Number**</span></span><br><span data-ttu-id="5a102-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="5a102-122">mshr_partynumber</span></span><br><span data-ttu-id="5a102-123">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="5a102-123">*String*</span></span> | <span data-ttu-id="5a102-124">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="5a102-124">Read/write</span></span><br><span data-ttu-id="5a102-125">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-125">Required</span></span> | <span data-ttu-id="5a102-126">รหัสฝ่าย (บุคคล) ของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="5a102-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="5a102-127">**ค่ารหัสบุคคล**</span><span class="sxs-lookup"><span data-stu-id="5a102-127">**Person ID Value**</span></span><br><span data-ttu-id="5a102-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="5a102-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="5a102-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5a102-129">*GUID*</span></span> | <span data-ttu-id="5a102-130">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="5a102-130">Read-only</span></span><br><span data-ttu-id="5a102-131">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-131">Required</span></span><br><span data-ttu-id="5a102-132">คีย์นอก: mshr_dirpersonentityid ของ mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="5a102-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="5a102-133">ตัวระบุเฉพาะที่ระบบสร้างขึ้นของเรกคอร์ดเอนทิตี้ฝ่าย (บุคคล)</span><span class="sxs-lookup"><span data-stu-id="5a102-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="5a102-134">**รหัสชนิดใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="5a102-134">**Certificate Type ID**</span></span><br><span data-ttu-id="5a102-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="5a102-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="5a102-136">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="5a102-136">*String*</span></span> | <span data-ttu-id="5a102-137">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="5a102-137">Read/write</span></span><br><span data-ttu-id="5a102-138">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-138">Required</span></span> |  <span data-ttu-id="5a102-139">ตัวระบุของชนิดใบรับรองที่กําหนดในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5a102-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="5a102-140">**ค่ารหัสชนิดใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="5a102-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="5a102-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="5a102-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="5a102-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5a102-142">*GUID*</span></span> | <span data-ttu-id="5a102-143">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="5a102-143">Read-only</span></span><br><span data-ttu-id="5a102-144">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-144">Required</span></span><br><span data-ttu-id="5a102-145">คีย์นอก: mshr_hcmcertificatetypeentityid ของ mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="5a102-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="5a102-146">ตัวระบุเฉพาะที่ระบบสร้างขึ้นของชนิดใบรับรองในเอนทิตี้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5a102-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="5a102-147">**วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5a102-147">**Start Date**</span></span><br><span data-ttu-id="5a102-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="5a102-148">mshr_startdate</span></span><br><span data-ttu-id="5a102-149">*วันเวลา*</span><span class="sxs-lookup"><span data-stu-id="5a102-149">*Datetime*</span></span> | <span data-ttu-id="5a102-150">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="5a102-150">Read/write</span></span><br><span data-ttu-id="5a102-151">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-151">Required</span></span> | <span data-ttu-id="5a102-152">วันที่ที่ใบรับรองได้รับการออก</span><span class="sxs-lookup"><span data-stu-id="5a102-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="5a102-153">**วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="5a102-153">**End Date**</span></span><br><span data-ttu-id="5a102-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="5a102-154">mshr_enddate</span></span><br><span data-ttu-id="5a102-155">*วันเวลา*</span><span class="sxs-lookup"><span data-stu-id="5a102-155">*Datetime*</span></span> | <span data-ttu-id="5a102-156">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="5a102-156">Read/write</span></span><br><span data-ttu-id="5a102-157">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-157">Optional</span></span> | <span data-ttu-id="5a102-158">วันที่ที่ใบรับรองจะหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="5a102-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="5a102-159">**บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="5a102-159">**Notes**</span></span><br><span data-ttu-id="5a102-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="5a102-160">mshr_notes</span></span><br><span data-ttu-id="5a102-161">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="5a102-161">*String*</span></span> | <span data-ttu-id="5a102-162">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="5a102-162">Read/write</span></span><br><span data-ttu-id="5a102-163">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-163">Optional</span></span> | <span data-ttu-id="5a102-164">หมายเหตุที่ใช้โดยผู้จัดการการจ้างงานหรือผู้จัดหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="5a102-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="5a102-165">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="5a102-165">**Primary Field**</span></span><br><span data-ttu-id="5a102-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="5a102-166">mshr_primaryfield</span></span><br><span data-ttu-id="5a102-167">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="5a102-167">*String*</span></span> | <span data-ttu-id="5a102-168">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="5a102-168">Read-only</span></span><br><span data-ttu-id="5a102-169">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="5a102-169">Required</span></span> |  <span data-ttu-id="5a102-170">ฟิลด์ที่จะใช้เป็นตัวระบุของเรกคอร์ดเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="5a102-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="5a102-171">ชุดของหมายเลขฝ่าย รหัสชนิดใบรับรองและวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5a102-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5a102-172">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="5a102-172">See also</span></span>

[<span data-ttu-id="5a102-173">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="5a102-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5a102-174">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5a102-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

