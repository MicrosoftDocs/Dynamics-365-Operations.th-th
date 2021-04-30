---
title: รายละเอียดค่าจ้างสำหรับตำแหน่ง
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882084"
---
# <a name="payroll-position"></a><span data-ttu-id="269dd-103">ตําแหน่งในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="269dd-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="269dd-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="269dd-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="269dd-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="269dd-105">Properties</span></span>

| <span data-ttu-id="269dd-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="269dd-106">Property</span></span><br><span data-ttu-id="269dd-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="269dd-107">**Physical name**</span></span><br><span data-ttu-id="269dd-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="269dd-108">**_Type_**</span></span> | <span data-ttu-id="269dd-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="269dd-109">Use</span></span> | <span data-ttu-id="269dd-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="269dd-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="269dd-111">**ชั่วโมงปกติรายปี**</span><span class="sxs-lookup"><span data-stu-id="269dd-111">**Annual regular hours**</span></span><br><span data-ttu-id="269dd-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="269dd-112">annualregularhours</span></span><br><span data-ttu-id="269dd-113">*ทศนิยม*</span><span class="sxs-lookup"><span data-stu-id="269dd-113">*Decimal*</span></span> | <span data-ttu-id="269dd-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-114">Read-only</span></span><br><span data-ttu-id="269dd-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-115">Required</span></span> | <span data-ttu-id="269dd-116">ชั่วโมงปกติรายปีที่กําหนดไว้ในตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="269dd-117">**รหัสเอนทิตีรายละเอียดตำแหน่งค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="269dd-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="269dd-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="269dd-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="269dd-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="269dd-119">*Guid*</span></span> | <span data-ttu-id="269dd-120">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-120">Required</span></span><br><span data-ttu-id="269dd-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="269dd-121">System generated.</span></span> | <span data-ttu-id="269dd-122">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตำแหน่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="269dd-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="269dd-123">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="269dd-123">**Primary field**</span></span><br><span data-ttu-id="269dd-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="269dd-124">mshr_primaryfield</span></span><br><span data-ttu-id="269dd-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="269dd-125">*String*</span></span> | <span data-ttu-id="269dd-126">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-126">Required</span></span><br><span data-ttu-id="269dd-127">ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="269dd-127">System generated</span></span> |  |
| <span data-ttu-id="269dd-128">**ค่ารหัสตําแหน่งงาน**</span><span class="sxs-lookup"><span data-stu-id="269dd-128">**Position job ID value**</span></span><br><span data-ttu-id="269dd-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="269dd-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="269dd-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="269dd-130">*GUID*</span></span> | <span data-ttu-id="269dd-131">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-131">Read-only</span></span><br><span data-ttu-id="269dd-132">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-132">Required</span></span><br><span data-ttu-id="269dd-133">คีย์นอก:mshr_PayrollPositionJobEntity:mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="269dd-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="269dd-134">รหัสของงานที่เชื่อมโยงกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="269dd-135">**ค่ารหัสแผนค่าตอบแทนคงที่**</span><span class="sxs-lookup"><span data-stu-id="269dd-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="269dd-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="269dd-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="269dd-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="269dd-137">*GUID*</span></span> | <span data-ttu-id="269dd-138">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-138">Read-only</span></span><br><span data-ttu-id="269dd-139">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-139">Required</span></span><br><span data-ttu-id="269dd-140">คีย์นอก: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="269dd-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="269dd-141">รหัสของแผนค่าตอบแทนคงที่ที่เชื่อมโยงกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="269dd-142">**รหัสรอบการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="269dd-142">**Pay cycle ID**</span></span><br><span data-ttu-id="269dd-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="269dd-143">mshr_primaryfield</span></span><br><span data-ttu-id="269dd-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="269dd-144">*String*</span></span> | <span data-ttu-id="269dd-145">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-145">Read-only</span></span><br><span data-ttu-id="269dd-146">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-146">Required</span></span> | <span data-ttu-id="269dd-147">วงจรการค่าจ้างที่กําหนดไว้ในตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="269dd-148">**ชำระโดยนิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="269dd-148">**Paid by legal entity**</span></span><br><span data-ttu-id="269dd-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="269dd-149">paidbylegalentity</span></span><br><span data-ttu-id="269dd-150">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="269dd-150">*String*</span></span> | <span data-ttu-id="269dd-151">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-151">Read-only</span></span><br><span data-ttu-id="269dd-152">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-152">Required</span></span> | <span data-ttu-id="269dd-153">นิติบุคคลที่กําหนดตามตําแหน่งที่รับผิดชอบการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="269dd-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="269dd-154">**รหัสตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="269dd-154">**Position ID**</span></span><br><span data-ttu-id="269dd-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="269dd-155">mshr_positionid</span></span><br><span data-ttu-id="269dd-156">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="269dd-156">*String*</span></span> | <span data-ttu-id="269dd-157">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-157">Read-only</span></span><br><span data-ttu-id="269dd-158">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-158">Required</span></span> | <span data-ttu-id="269dd-159">รหัสของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-159">The ID of the position.</span></span> |
| <span data-ttu-id="269dd-160">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="269dd-160">**Valid to**</span></span><br><span data-ttu-id="269dd-161">validto</span><span class="sxs-lookup"><span data-stu-id="269dd-161">validto</span></span><br><span data-ttu-id="269dd-162">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="269dd-162">*Date Time Offset*</span></span> | <span data-ttu-id="269dd-163">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-163">Read-only</span></span><br><span data-ttu-id="269dd-164">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-164">Required</span></span> |<span data-ttu-id="269dd-165">วันที่เริ่มต้นการมีผลบังคับใช้ของรายละเอียดตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="269dd-166">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="269dd-166">**Valid from**</span></span><br><span data-ttu-id="269dd-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="269dd-167">validfrom</span></span><br><span data-ttu-id="269dd-168">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="269dd-168">*Date Time Offset*</span></span> | <span data-ttu-id="269dd-169">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="269dd-169">Read-only</span></span><br><span data-ttu-id="269dd-170">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="269dd-170">Required</span></span> |<span data-ttu-id="269dd-171">วันที่สิ้นสุดการมีผลบังคับใช้ของรายละเอียดตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="269dd-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="269dd-172">**การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="269dd-172">**Query**</span></span>

<span data-ttu-id="269dd-173">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="269dd-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="269dd-174">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="269dd-174">**Response**</span></span>

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
