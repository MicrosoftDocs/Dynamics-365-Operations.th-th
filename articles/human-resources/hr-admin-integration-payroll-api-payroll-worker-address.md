---
title: ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052300"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="67f16-103">ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="67f16-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="67f16-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="67f16-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="67f16-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="67f16-105">Properties</span></span>

| <span data-ttu-id="67f16-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="67f16-106">Property</span></span><br><span data-ttu-id="67f16-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="67f16-107">**Physical name**</span></span><br><span data-ttu-id="67f16-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="67f16-108">**_Type_**</span></span> | <span data-ttu-id="67f16-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="67f16-109">Use</span></span> | <span data-ttu-id="67f16-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="67f16-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="67f16-111">**เมือง**</span><span class="sxs-lookup"><span data-stu-id="67f16-111">**City**</span></span><br><span data-ttu-id="67f16-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="67f16-112">mshr_city</span></span><br><span data-ttu-id="67f16-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-113">*String*</span></span> | <span data-ttu-id="67f16-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-114">Read-only</span></span><br><span data-ttu-id="67f16-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-115">Required</span></span> | <span data-ttu-id="67f16-116">เมืองที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="67f16-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="67f16-117">**หมายเลขบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="67f16-117">**Personnel number**</span></span><br><span data-ttu-id="67f16-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="67f16-118">mshr_personnelnumber</span></span><br><span data-ttu-id="67f16-119">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-119">*String*</span></span> | <span data-ttu-id="67f16-120">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-120">Read-only</span></span><br><span data-ttu-id="67f16-121">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-121">Required</span></span> | <span data-ttu-id="67f16-122">หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="67f16-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="67f16-123">**ภูมิภาคประเทศ**</span><span class="sxs-lookup"><span data-stu-id="67f16-123">**Country region**</span></span><br><span data-ttu-id="67f16-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="67f16-124">mshr_countryregionid</span></span><br><span data-ttu-id="67f16-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-125">*String*</span></span> | <span data-ttu-id="67f16-126">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-126">Read-only</span></span><br><span data-ttu-id="67f16-127">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-127">Required</span></span> | <span data-ttu-id="67f16-128">ภูมิภาคประเทศที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="67f16-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="67f16-129">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="67f16-129">**Valid from**</span></span><br><span data-ttu-id="67f16-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="67f16-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="67f16-131">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="67f16-131">*Date Time Offset*</span></span> | <span data-ttu-id="67f16-132">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-132">Read-only</span></span> <br><span data-ttu-id="67f16-133">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-133">Required</span></span> | <span data-ttu-id="67f16-134">วันที่ที่ที่อยู่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="67f16-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="67f16-135">**ที่อยู่ที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="67f16-135">**Worked in address**</span></span><br><span data-ttu-id="67f16-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="67f16-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="67f16-137">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-137">Read-only</span></span><br><span data-ttu-id="67f16-138">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-138">Required</span></span> | <span data-ttu-id="67f16-139">แสดงถ้าที่อยู่เป็นที่อยู่ที่พนักงานทำงาน</span><span class="sxs-lookup"><span data-stu-id="67f16-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="67f16-140">**เขต**</span><span class="sxs-lookup"><span data-stu-id="67f16-140">**County**</span></span><br><span data-ttu-id="67f16-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="67f16-141">mshr_county</span></span><br><span data-ttu-id="67f16-142">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-142">*String*</span></span> | <span data-ttu-id="67f16-143">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-143">Read-only</span></span><br><span data-ttu-id="67f16-144">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-144">Required</span></span> | <span data-ttu-id="67f16-145">ประเทศที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="67f16-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="67f16-146">**รหัสที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน**</span><span class="sxs-lookup"><span data-stu-id="67f16-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="67f16-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="67f16-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="67f16-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="67f16-148">*GUID*</span></span> | <span data-ttu-id="67f16-149">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-149">Required</span></span><br><span data-ttu-id="67f16-150">ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="67f16-150">System generated</span></span> | <span data-ttu-id="67f16-151">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงที่อยู่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="67f16-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="67f16-152">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="67f16-152">**Primary field**</span></span><br><span data-ttu-id="67f16-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="67f16-153">mshr_primaryfield</span></span><br><span data-ttu-id="67f16-154">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-154">*String*</span></span> | <span data-ttu-id="67f16-155">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-155">Read-only</span></span><br><span data-ttu-id="67f16-156">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-156">Required</span></span> |  |
| <span data-ttu-id="67f16-157">**ถนน**</span><span class="sxs-lookup"><span data-stu-id="67f16-157">**Street**</span></span><br><span data-ttu-id="67f16-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="67f16-158">mshr_street</span></span><br><span data-ttu-id="67f16-159">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-159">*String*</span></span> | <span data-ttu-id="67f16-160">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-160">Read-only</span></span><br><span data-ttu-id="67f16-161">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-161">Required</span></span> | <span data-ttu-id="67f16-162">ถนนที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="67f16-162">The street defined for the address.</span></span> |
| <span data-ttu-id="67f16-163">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="67f16-163">**Valid to**</span></span><br><span data-ttu-id="67f16-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="67f16-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="67f16-165">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="67f16-165">*Date Time Offset*</span></span> | <span data-ttu-id="67f16-166">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-166">Read-only</span></span> <br><span data-ttu-id="67f16-167">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-167">Required</span></span> | <span data-ttu-id="67f16-168">วันที่ที่ที่อยู่มีผลบังคับใช้ถึง</span><span class="sxs-lookup"><span data-stu-id="67f16-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="67f16-169">**รหัสสถานที่**</span><span class="sxs-lookup"><span data-stu-id="67f16-169">**Location ID**</span></span><br><span data-ttu-id="67f16-170">mshr_locationidbr>*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="67f16-171">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-171">Read-only</span></span> <br><span data-ttu-id="67f16-172">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-172">Required</span></span> | <span data-ttu-id="67f16-173">รหัสของที่อยู่</span><span class="sxs-lookup"><span data-stu-id="67f16-173">The ID for the address.</span></span>  |
| <span data-ttu-id="67f16-174">**รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="67f16-174">**Postal code**</span></span><br><span data-ttu-id="67f16-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="67f16-175">mshr_zipcode</span></span><br><span data-ttu-id="67f16-176">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-176">*String*</span></span> | <span data-ttu-id="67f16-177">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-177">Read-only</span></span> <br><span data-ttu-id="67f16-178">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-178">Required</span></span> |<span data-ttu-id="67f16-179">หมายเลขรหัสที่กําหนดไว้ให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="67f16-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="67f16-180">**ที่อยู่อาศัย**</span><span class="sxs-lookup"><span data-stu-id="67f16-180">**Lived in address**</span></span><br><span data-ttu-id="67f16-181">mshr_islivedinaddressbr>*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="67f16-182">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-182">Read-only</span></span><br><span data-ttu-id="67f16-183">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-183">Required</span></span> | <span data-ttu-id="67f16-184">แสดงถ้าที่อยู่เป็นที่อยู่ที่พนักงานอาศัย</span><span class="sxs-lookup"><span data-stu-id="67f16-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="67f16-185">**จังหวัด**</span><span class="sxs-lookup"><span data-stu-id="67f16-185">**State**</span></span><br><span data-ttu-id="67f16-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="67f16-186">mshr_state</span></span><br><span data-ttu-id="67f16-187">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="67f16-187">*String*</span></span> | <span data-ttu-id="67f16-188">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="67f16-188">Read-only</span></span><br><span data-ttu-id="67f16-189">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="67f16-189">Required</span></span> | <span data-ttu-id="67f16-190">รัฐที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="67f16-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="67f16-191">ตัวอย่างการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="67f16-191">Example query</span></span>

<span data-ttu-id="67f16-192">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="67f16-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="67f16-193">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="67f16-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
