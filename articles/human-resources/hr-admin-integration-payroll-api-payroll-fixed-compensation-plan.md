---
title: แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021307"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="59275-103">แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="59275-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="59275-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีแผนค่าตอบแทนคงที่ในบัญชีเงินเดือนใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="59275-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="59275-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="59275-105">Properties</span></span>

| <span data-ttu-id="59275-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="59275-106">Property</span></span><br><span data-ttu-id="59275-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="59275-107">**Physical name**</span></span><br><span data-ttu-id="59275-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="59275-108">**_Type_**</span></span> | <span data-ttu-id="59275-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="59275-109">Use</span></span> | <span data-ttu-id="59275-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="59275-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="59275-111">**รหัสพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="59275-111">**Employee ID**</span></span><br><span data-ttu-id="59275-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="59275-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="59275-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="59275-113">*GUID*</span></span> | <span data-ttu-id="59275-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-114">Read-only</span></span><br><span data-ttu-id="59275-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-115">Required</span></span><br><span data-ttu-id="59275-116">คีย์นอก: เอนทิตี mshr_Employee_idของmshr_payrollemployeeentity</span><span class="sxs-lookup"><span data-stu-id="59275-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="59275-117">รหัสพนักงาน</span><span class="sxs-lookup"><span data-stu-id="59275-117">Employee ID</span></span> |
| <span data-ttu-id="59275-118">**อัตราการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="59275-118">**Pay rate**</span></span><br><span data-ttu-id="59275-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="59275-119">mshr_payrate</span></span><br><span data-ttu-id="59275-120">*ทศนิยม*</span><span class="sxs-lookup"><span data-stu-id="59275-120">*Decimal*</span></span> | <span data-ttu-id="59275-121">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-121">Read-only</span></span><br><span data-ttu-id="59275-122">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-122">Required</span></span> | <span data-ttu-id="59275-123">อัตราการค่าจ้างที่กําหนดในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="59275-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="59275-124">**รหัสแผน**</span><span class="sxs-lookup"><span data-stu-id="59275-124">**Plan ID**</span></span><br><span data-ttu-id="59275-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="59275-125">mshr_planid</span></span><br><span data-ttu-id="59275-126">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="59275-126">*String*</span></span> | <span data-ttu-id="59275-127">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-127">Read-only</span></span><br><span data-ttu-id="59275-128">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-128">Required</span></span> |<span data-ttu-id="59275-129">ระบุแผนค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="59275-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="59275-130">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="59275-130">**Valid from**</span></span><br><span data-ttu-id="59275-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="59275-131">mshr_validfrom</span></span><br><span data-ttu-id="59275-132">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="59275-132">*Date Time Offset*</span></span> |  <span data-ttu-id="59275-133">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-133">Read-only</span></span><br><span data-ttu-id="59275-134">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-134">Required</span></span> |<span data-ttu-id="59275-135">วันที่เริ่มต้นการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="59275-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="59275-136">**เอนทิตีแผนค่าตอบแทนคงที่ของบัญชีเงินเดือน**</span><span class="sxs-lookup"><span data-stu-id="59275-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="59275-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="59275-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="59275-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="59275-138">*GUID*</span></span> | <span data-ttu-id="59275-139">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-139">Required</span></span><br><span data-ttu-id="59275-140">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="59275-140">Sytem generated</span></span> | <span data-ttu-id="59275-141">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงตีแผนค่าตอบแทนโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="59275-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="59275-142">**ความถี่ในการชำระค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="59275-142">**Pay frequency**</span></span><br><span data-ttu-id="59275-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="59275-143">mshr_payfrequency</span></span><br><span data-ttu-id="59275-144">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="59275-144">*String*</span></span> | <span data-ttu-id="59275-145">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-145">Read-only</span></span><br><span data-ttu-id="59275-146">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-146">Required</span></span> |<span data-ttu-id="59275-147">ความถี่ในการชําระค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="59275-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="59275-148">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="59275-148">**Valid to**</span></span><br><span data-ttu-id="59275-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="59275-149">mshr_validto</span></span><br><span data-ttu-id="59275-150">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="59275-150">*Date Time Offset*</span></span> | <span data-ttu-id="59275-151">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-151">Read-only</span></span> <br><span data-ttu-id="59275-152">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-152">Required</span></span> | <span data-ttu-id="59275-153">วันที่สิ้นสุดการมีผลบังคับใช้ของค่าตอบแทนคงที่ของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="59275-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="59275-154">**รหัสตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="59275-154">**Position ID**</span></span><br><span data-ttu-id="59275-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="59275-155">mshr_positionid</span></span><br><span data-ttu-id="59275-156">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="59275-156">*String*</span></span> | <span data-ttu-id="59275-157">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-157">Read-only</span></span> <br><span data-ttu-id="59275-158">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-158">Required</span></span> | <span data-ttu-id="59275-159">รหัสไปรษณีย์ที่เชื่อมโยงกับพนักงานและการลงทะเบียนแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="59275-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="59275-160">**สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="59275-160">**Currency**</span></span><br><span data-ttu-id="59275-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="59275-161">mshr_currency</span></span><br><span data-ttu-id="59275-162">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="59275-162">*String*</span></span> | <span data-ttu-id="59275-163">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-163">Read-only</span></span> <br><span data-ttu-id="59275-164">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-164">Required</span></span> |<span data-ttu-id="59275-165">สกุลเงินที่กำหนดสำหรับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="59275-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="59275-166">**หมายเลขบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="59275-166">**Personnel number**</span></span><br><span data-ttu-id="59275-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="59275-167">mshr_personnelnumber</span></span><br><span data-ttu-id="59275-168">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="59275-168">*String*</span></span> | <span data-ttu-id="59275-169">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="59275-169">Read-only</span></span><br><span data-ttu-id="59275-170">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="59275-170">Required</span></span> |<span data-ttu-id="59275-171">หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="59275-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="59275-172">**การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="59275-172">**Query**</span></span>

<span data-ttu-id="59275-173">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="59275-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="59275-174">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="59275-174">**Response**</span></span>

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
