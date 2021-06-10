---
title: แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059099"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="05a2d-103">แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="05a2d-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="05a2d-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="05a2d-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="05a2d-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="05a2d-105">Properties</span></span>

| <span data-ttu-id="05a2d-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="05a2d-106">Property</span></span><br><span data-ttu-id="05a2d-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="05a2d-107">**Physical name**</span></span><br><span data-ttu-id="05a2d-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="05a2d-108">**_Type_**</span></span> | <span data-ttu-id="05a2d-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="05a2d-109">Use</span></span> | <span data-ttu-id="05a2d-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="05a2d-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="05a2d-111">**รหัสพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="05a2d-111">**Employee ID**</span></span><br><span data-ttu-id="05a2d-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="05a2d-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="05a2d-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="05a2d-113">*GUID*</span></span> | <span data-ttu-id="05a2d-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-114">Read-only</span></span><br><span data-ttu-id="05a2d-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-115">Required</span></span><br><span data-ttu-id="05a2d-116">คีย์นอก: เอนทิตี mshr_Employee_idของmshr_payrollemployeeentity</span><span class="sxs-lookup"><span data-stu-id="05a2d-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="05a2d-117">รหัสพนักงาน</span><span class="sxs-lookup"><span data-stu-id="05a2d-117">Employee ID</span></span> |
| <span data-ttu-id="05a2d-118">**อัตราการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="05a2d-118">**Pay rate**</span></span><br><span data-ttu-id="05a2d-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="05a2d-119">mshr_payrate</span></span><br><span data-ttu-id="05a2d-120">*ทศนิยม*</span><span class="sxs-lookup"><span data-stu-id="05a2d-120">*Decimal*</span></span> | <span data-ttu-id="05a2d-121">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-121">Read-only</span></span><br><span data-ttu-id="05a2d-122">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-122">Required</span></span> | <span data-ttu-id="05a2d-123">อัตราการค่าจ้างที่กําหนดในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="05a2d-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="05a2d-124">**รหัสแผน**</span><span class="sxs-lookup"><span data-stu-id="05a2d-124">**Plan ID**</span></span><br><span data-ttu-id="05a2d-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="05a2d-125">mshr_planid</span></span><br><span data-ttu-id="05a2d-126">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="05a2d-126">*String*</span></span> | <span data-ttu-id="05a2d-127">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-127">Read-only</span></span><br><span data-ttu-id="05a2d-128">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-128">Required</span></span> |<span data-ttu-id="05a2d-129">ระบุแผนค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="05a2d-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="05a2d-130">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="05a2d-130">**Valid from**</span></span><br><span data-ttu-id="05a2d-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="05a2d-131">mshr_validfrom</span></span><br><span data-ttu-id="05a2d-132">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="05a2d-132">*Date Time Offset*</span></span> |  <span data-ttu-id="05a2d-133">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-133">Read-only</span></span><br><span data-ttu-id="05a2d-134">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-134">Required</span></span> |<span data-ttu-id="05a2d-135">วันที่เริ่มต้นการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="05a2d-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="05a2d-136">**เอนทิตีแผนค่าตอบแทนคงที่ของบัญชีเงินเดือน**</span><span class="sxs-lookup"><span data-stu-id="05a2d-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="05a2d-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="05a2d-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="05a2d-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="05a2d-138">*GUID*</span></span> | <span data-ttu-id="05a2d-139">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-139">Required</span></span><br><span data-ttu-id="05a2d-140">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="05a2d-140">Sytem generated</span></span> | <span data-ttu-id="05a2d-141">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตีแผนค่าตอบแทนโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="05a2d-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="05a2d-142">**ความถี่ในการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="05a2d-142">**Pay frequency**</span></span><br><span data-ttu-id="05a2d-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="05a2d-143">mshr_payfrequency</span></span><br><span data-ttu-id="05a2d-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="05a2d-144">*String*</span></span> | <span data-ttu-id="05a2d-145">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-145">Read-only</span></span><br><span data-ttu-id="05a2d-146">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-146">Required</span></span> |<span data-ttu-id="05a2d-147">ความถี่ในการชําระค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="05a2d-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="05a2d-148">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="05a2d-148">**Valid to**</span></span><br><span data-ttu-id="05a2d-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="05a2d-149">mshr_validto</span></span><br><span data-ttu-id="05a2d-150">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="05a2d-150">*Date Time Offset*</span></span> | <span data-ttu-id="05a2d-151">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-151">Read-only</span></span> <br><span data-ttu-id="05a2d-152">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-152">Required</span></span> | <span data-ttu-id="05a2d-153">วันที่สิ้นสุดการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="05a2d-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="05a2d-154">**รหัสตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="05a2d-154">**Position ID**</span></span><br><span data-ttu-id="05a2d-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="05a2d-155">mshr_positionid</span></span><br><span data-ttu-id="05a2d-156">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="05a2d-156">*String*</span></span> | <span data-ttu-id="05a2d-157">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-157">Read-only</span></span> <br><span data-ttu-id="05a2d-158">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-158">Required</span></span> | <span data-ttu-id="05a2d-159">รหัสไปรษณีย์ที่เชื่อมโยงกับพนักงานและการลงทะเบียนแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="05a2d-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="05a2d-160">**สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="05a2d-160">**Currency**</span></span><br><span data-ttu-id="05a2d-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="05a2d-161">mshr_currency</span></span><br><span data-ttu-id="05a2d-162">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="05a2d-162">*String*</span></span> | <span data-ttu-id="05a2d-163">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-163">Read-only</span></span> <br><span data-ttu-id="05a2d-164">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-164">Required</span></span> |<span data-ttu-id="05a2d-165">สกุลเงินที่กำหนดสำหรับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="05a2d-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="05a2d-166">**หมายเลขบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="05a2d-166">**Personnel number**</span></span><br><span data-ttu-id="05a2d-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="05a2d-167">mshr_personnelnumber</span></span><br><span data-ttu-id="05a2d-168">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="05a2d-168">*String*</span></span> | <span data-ttu-id="05a2d-169">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="05a2d-169">Read-only</span></span><br><span data-ttu-id="05a2d-170">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="05a2d-170">Required</span></span> |<span data-ttu-id="05a2d-171">หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="05a2d-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="05a2d-172">**การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="05a2d-172">**Query**</span></span>

<span data-ttu-id="05a2d-173">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="05a2d-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="05a2d-174">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="05a2d-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
