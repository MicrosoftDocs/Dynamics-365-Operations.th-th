---
title: รายละเอียดค่าจ้างสำหรับตำแหน่ง
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056791"
---
# <a name="payroll-position"></a><span data-ttu-id="597ba-103">ตําแหน่งในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="597ba-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="597ba-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="597ba-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="597ba-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="597ba-105">Properties</span></span>

| <span data-ttu-id="597ba-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="597ba-106">Property</span></span><br><span data-ttu-id="597ba-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="597ba-107">**Physical name**</span></span><br><span data-ttu-id="597ba-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="597ba-108">**_Type_**</span></span> | <span data-ttu-id="597ba-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="597ba-109">Use</span></span> | <span data-ttu-id="597ba-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="597ba-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="597ba-111">**ชั่วโมงปกติรายปี**</span><span class="sxs-lookup"><span data-stu-id="597ba-111">**Annual regular hours**</span></span><br><span data-ttu-id="597ba-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="597ba-112">annualregularhours</span></span><br><span data-ttu-id="597ba-113">*ทศนิยม*</span><span class="sxs-lookup"><span data-stu-id="597ba-113">*Decimal*</span></span> | <span data-ttu-id="597ba-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-114">Read-only</span></span><br><span data-ttu-id="597ba-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-115">Required</span></span> | <span data-ttu-id="597ba-116">ชั่วโมงปกติรายปีที่กําหนดไว้ในตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="597ba-117">**รหัสเอนทิตีรายละเอียดตำแหน่งค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="597ba-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="597ba-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="597ba-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="597ba-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="597ba-119">*Guid*</span></span> | <span data-ttu-id="597ba-120">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-120">Required</span></span><br><span data-ttu-id="597ba-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="597ba-121">System generated.</span></span> | <span data-ttu-id="597ba-122">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตำแหน่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="597ba-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="597ba-123">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="597ba-123">**Primary field**</span></span><br><span data-ttu-id="597ba-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="597ba-124">mshr_primaryfield</span></span><br><span data-ttu-id="597ba-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="597ba-125">*String*</span></span> | <span data-ttu-id="597ba-126">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-126">Required</span></span><br><span data-ttu-id="597ba-127">ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="597ba-127">System generated</span></span> |  |
| <span data-ttu-id="597ba-128">**ค่ารหัสตําแหน่งงาน**</span><span class="sxs-lookup"><span data-stu-id="597ba-128">**Position job ID value**</span></span><br><span data-ttu-id="597ba-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="597ba-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="597ba-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="597ba-130">*GUID*</span></span> | <span data-ttu-id="597ba-131">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-131">Read-only</span></span><br><span data-ttu-id="597ba-132">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-132">Required</span></span><br><span data-ttu-id="597ba-133">คีย์นอก:mshr_PayrollPositionJobEntity:mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="597ba-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="597ba-134">รหัสของงานที่เชื่อมโยงกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="597ba-135">**ค่ารหัสแผนค่าตอบแทนคงที่**</span><span class="sxs-lookup"><span data-stu-id="597ba-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="597ba-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="597ba-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="597ba-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="597ba-137">*GUID*</span></span> | <span data-ttu-id="597ba-138">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-138">Read-only</span></span><br><span data-ttu-id="597ba-139">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-139">Required</span></span><br><span data-ttu-id="597ba-140">คีย์นอก: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="597ba-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="597ba-141">รหัสของแผนค่าตอบแทนคงที่ที่เชื่อมโยงกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="597ba-142">**รหัสรอบการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="597ba-142">**Pay cycle ID**</span></span><br><span data-ttu-id="597ba-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="597ba-143">mshr_primaryfield</span></span><br><span data-ttu-id="597ba-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="597ba-144">*String*</span></span> | <span data-ttu-id="597ba-145">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-145">Read-only</span></span><br><span data-ttu-id="597ba-146">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-146">Required</span></span> | <span data-ttu-id="597ba-147">วงจรการค่าจ้างที่กําหนดไว้ในตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="597ba-148">**ชำระโดยนิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="597ba-148">**Paid by legal entity**</span></span><br><span data-ttu-id="597ba-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="597ba-149">paidbylegalentity</span></span><br><span data-ttu-id="597ba-150">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="597ba-150">*String*</span></span> | <span data-ttu-id="597ba-151">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-151">Read-only</span></span><br><span data-ttu-id="597ba-152">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-152">Required</span></span> | <span data-ttu-id="597ba-153">นิติบุคคลที่กําหนดตามตําแหน่งที่รับผิดชอบการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="597ba-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="597ba-154">**รหัสตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="597ba-154">**Position ID**</span></span><br><span data-ttu-id="597ba-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="597ba-155">mshr_positionid</span></span><br><span data-ttu-id="597ba-156">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="597ba-156">*String*</span></span> | <span data-ttu-id="597ba-157">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-157">Read-only</span></span><br><span data-ttu-id="597ba-158">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-158">Required</span></span> | <span data-ttu-id="597ba-159">รหัสของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-159">The ID of the position.</span></span> |
| <span data-ttu-id="597ba-160">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="597ba-160">**Valid to**</span></span><br><span data-ttu-id="597ba-161">validto</span><span class="sxs-lookup"><span data-stu-id="597ba-161">validto</span></span><br><span data-ttu-id="597ba-162">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="597ba-162">*Date Time Offset*</span></span> | <span data-ttu-id="597ba-163">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-163">Read-only</span></span><br><span data-ttu-id="597ba-164">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-164">Required</span></span> |<span data-ttu-id="597ba-165">วันที่เริ่มต้นการมีผลบังคับใช้ของรายละเอียดตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="597ba-166">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="597ba-166">**Valid from**</span></span><br><span data-ttu-id="597ba-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="597ba-167">validfrom</span></span><br><span data-ttu-id="597ba-168">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="597ba-168">*Date Time Offset*</span></span> | <span data-ttu-id="597ba-169">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="597ba-169">Read-only</span></span><br><span data-ttu-id="597ba-170">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="597ba-170">Required</span></span> |<span data-ttu-id="597ba-171">วันที่สิ้นสุดการมีผลบังคับใช้ของรายละเอียดตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="597ba-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="597ba-172">**การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="597ba-172">**Query**</span></span>

<span data-ttu-id="597ba-173">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="597ba-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="597ba-174">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="597ba-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
