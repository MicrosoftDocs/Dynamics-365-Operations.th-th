---
title: รายละเอียดค่าจ้างสำหรับตำแหน่ง
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources
author: jcart
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019333"
---
# <a name="payroll-position"></a><span data-ttu-id="0d620-103">ตําแหน่งในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="0d620-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d620-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีรายละเอียดค่าจ้างสำหรับตำแหน่งใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="0d620-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="0d620-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0d620-105">Properties</span></span>

| <span data-ttu-id="0d620-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="0d620-106">Property</span></span><br><span data-ttu-id="0d620-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="0d620-107">**Physical name**</span></span><br><span data-ttu-id="0d620-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="0d620-108">**_Type_**</span></span> | <span data-ttu-id="0d620-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="0d620-109">Use</span></span> | <span data-ttu-id="0d620-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="0d620-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0d620-111">**ชั่วโมงปกติรายปี**</span><span class="sxs-lookup"><span data-stu-id="0d620-111">**Annual regular hours**</span></span><br><span data-ttu-id="0d620-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="0d620-112">annualregularhours</span></span><br><span data-ttu-id="0d620-113">*ทศนิยม*</span><span class="sxs-lookup"><span data-stu-id="0d620-113">*Decimal*</span></span> | <span data-ttu-id="0d620-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-114">Read-only</span></span><br><span data-ttu-id="0d620-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-115">Required</span></span> | <span data-ttu-id="0d620-116">ชั่วโมงปกติรายปีที่กําหนดไว้ในตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="0d620-117">**รหัสเอนทิตีรายละเอียดตำแหน่งค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="0d620-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="0d620-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="0d620-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="0d620-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="0d620-119">*Guid*</span></span> | <span data-ttu-id="0d620-120">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-120">Required</span></span><br><span data-ttu-id="0d620-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0d620-121">System generated.</span></span> | <span data-ttu-id="0d620-122">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตำแหน่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="0d620-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="0d620-123">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="0d620-123">**Primary field**</span></span><br><span data-ttu-id="0d620-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0d620-124">mshr_primaryfield</span></span><br><span data-ttu-id="0d620-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d620-125">*String*</span></span> | <span data-ttu-id="0d620-126">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-126">Required</span></span><br><span data-ttu-id="0d620-127">ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0d620-127">System generated</span></span> |  |
| <span data-ttu-id="0d620-128">**ค่ารหัสตําแหน่งงาน**</span><span class="sxs-lookup"><span data-stu-id="0d620-128">**Position job ID value**</span></span><br><span data-ttu-id="0d620-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="0d620-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="0d620-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d620-130">*GUID*</span></span> | <span data-ttu-id="0d620-131">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-131">Read-only</span></span><br><span data-ttu-id="0d620-132">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-132">Required</span></span><br><span data-ttu-id="0d620-133">คีย์นอก:mshr_PayrollPositionJobEntity:mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="0d620-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="0d620-134">รหัสของงานที่เชื่อมโยงกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="0d620-135">**ค่ารหัสแผนค่าตอบแทนคงที่**</span><span class="sxs-lookup"><span data-stu-id="0d620-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="0d620-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="0d620-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="0d620-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d620-137">*GUID*</span></span> | <span data-ttu-id="0d620-138">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-138">Read-only</span></span><br><span data-ttu-id="0d620-139">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-139">Required</span></span><br><span data-ttu-id="0d620-140">คีย์นอก: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="0d620-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="0d620-141">รหัสของแผนค่าตอบแทนคงที่ที่เชื่อมโยงกับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="0d620-142">**รหัสรอบการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="0d620-142">**Pay cycle ID**</span></span><br><span data-ttu-id="0d620-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0d620-143">mshr_primaryfield</span></span><br><span data-ttu-id="0d620-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d620-144">*String*</span></span> | <span data-ttu-id="0d620-145">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-145">Read-only</span></span><br><span data-ttu-id="0d620-146">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-146">Required</span></span> | <span data-ttu-id="0d620-147">วงจรการค่าจ้างที่กําหนดไว้ในตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="0d620-148">**ชำระโดยนิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="0d620-148">**Paid by legal entity**</span></span><br><span data-ttu-id="0d620-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="0d620-149">paidbylegalentity</span></span><br><span data-ttu-id="0d620-150">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d620-150">*String*</span></span> | <span data-ttu-id="0d620-151">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-151">Read-only</span></span><br><span data-ttu-id="0d620-152">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-152">Required</span></span> | <span data-ttu-id="0d620-153">นิติบุคคลที่กําหนดตามตําแหน่งที่รับผิดชอบการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0d620-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="0d620-154">**รหัสตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="0d620-154">**Position ID**</span></span><br><span data-ttu-id="0d620-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="0d620-155">mshr_positionid</span></span><br><span data-ttu-id="0d620-156">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="0d620-156">*String*</span></span> | <span data-ttu-id="0d620-157">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-157">Read-only</span></span><br><span data-ttu-id="0d620-158">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-158">Required</span></span> | <span data-ttu-id="0d620-159">รหัสของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-159">The ID of the position.</span></span> |
| <span data-ttu-id="0d620-160">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="0d620-160">**Valid to**</span></span><br><span data-ttu-id="0d620-161">validto</span><span class="sxs-lookup"><span data-stu-id="0d620-161">validto</span></span><br><span data-ttu-id="0d620-162">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="0d620-162">*Date Time Offset*</span></span> | <span data-ttu-id="0d620-163">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-163">Read-only</span></span><br><span data-ttu-id="0d620-164">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-164">Required</span></span> |<span data-ttu-id="0d620-165">วันที่เริ่มต้นการมีผลบังคับใช้ของรายละเอียดตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="0d620-166">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="0d620-166">**Valid from**</span></span><br><span data-ttu-id="0d620-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="0d620-167">validfrom</span></span><br><span data-ttu-id="0d620-168">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="0d620-168">*Date Time Offset*</span></span> | <span data-ttu-id="0d620-169">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="0d620-169">Read-only</span></span><br><span data-ttu-id="0d620-170">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="0d620-170">Required</span></span> |<span data-ttu-id="0d620-171">วันที่สิ้นสุดการมีผลบังคับใช้ของรายละเอียดตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0d620-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="0d620-172">**การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="0d620-172">**Query**</span></span>

<span data-ttu-id="0d620-173">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="0d620-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="0d620-174">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="0d620-174">**Response**</span></span>

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
