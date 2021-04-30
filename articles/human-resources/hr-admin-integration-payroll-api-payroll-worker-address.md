---
title: ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882086"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="54224-103">ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="54224-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="54224-104">หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือนใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="54224-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="54224-105">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="54224-105">Properties</span></span>

| <span data-ttu-id="54224-106">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="54224-106">Property</span></span><br><span data-ttu-id="54224-107">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="54224-107">**Physical name**</span></span><br><span data-ttu-id="54224-108">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="54224-108">**_Type_**</span></span> | <span data-ttu-id="54224-109">ใช้</span><span class="sxs-lookup"><span data-stu-id="54224-109">Use</span></span> | <span data-ttu-id="54224-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="54224-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="54224-111">**เมือง**</span><span class="sxs-lookup"><span data-stu-id="54224-111">**City**</span></span><br><span data-ttu-id="54224-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="54224-112">mshr_city</span></span><br><span data-ttu-id="54224-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-113">*String*</span></span> | <span data-ttu-id="54224-114">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-114">Read-only</span></span><br><span data-ttu-id="54224-115">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-115">Required</span></span> | <span data-ttu-id="54224-116">เมืองที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="54224-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="54224-117">**หมายเลขบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="54224-117">**Personnel number**</span></span><br><span data-ttu-id="54224-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="54224-118">mshr_personnelnumber</span></span><br><span data-ttu-id="54224-119">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-119">*String*</span></span> | <span data-ttu-id="54224-120">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-120">Read-only</span></span><br><span data-ttu-id="54224-121">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-121">Required</span></span> | <span data-ttu-id="54224-122">หมายเลขด้านบุคลากรที่ไม่ซ้ำกันของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="54224-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="54224-123">**ภูมิภาคประเทศ**</span><span class="sxs-lookup"><span data-stu-id="54224-123">**Country region**</span></span><br><span data-ttu-id="54224-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="54224-124">mshr_countryregionid</span></span><br><span data-ttu-id="54224-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-125">*String*</span></span> | <span data-ttu-id="54224-126">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-126">Read-only</span></span><br><span data-ttu-id="54224-127">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-127">Required</span></span> | <span data-ttu-id="54224-128">ภูมิภาคประเทศที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="54224-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="54224-129">**มีผลใช้ตั้งแต่**</span><span class="sxs-lookup"><span data-stu-id="54224-129">**Valid from**</span></span><br><span data-ttu-id="54224-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="54224-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="54224-131">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="54224-131">*Date Time Offset*</span></span> | <span data-ttu-id="54224-132">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-132">Read-only</span></span> <br><span data-ttu-id="54224-133">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-133">Required</span></span> | <span data-ttu-id="54224-134">วันที่ที่ที่อยู่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="54224-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="54224-135">**ที่อยู่ที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="54224-135">**Worked in address**</span></span><br><span data-ttu-id="54224-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="54224-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="54224-137">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-137">Read-only</span></span><br><span data-ttu-id="54224-138">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-138">Required</span></span> | <span data-ttu-id="54224-139">แสดงถ้าที่อยู่เป็นที่อยู่ที่พนักงานทำงาน</span><span class="sxs-lookup"><span data-stu-id="54224-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="54224-140">**เขต**</span><span class="sxs-lookup"><span data-stu-id="54224-140">**County**</span></span><br><span data-ttu-id="54224-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="54224-141">mshr_county</span></span><br><span data-ttu-id="54224-142">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-142">*String*</span></span> | <span data-ttu-id="54224-143">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-143">Read-only</span></span><br><span data-ttu-id="54224-144">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-144">Required</span></span> | <span data-ttu-id="54224-145">ประเทศที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="54224-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="54224-146">**รหัสที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน**</span><span class="sxs-lookup"><span data-stu-id="54224-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="54224-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="54224-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="54224-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="54224-148">*GUID*</span></span> | <span data-ttu-id="54224-149">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-149">Required</span></span><br><span data-ttu-id="54224-150">ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="54224-150">System generated</span></span> | <span data-ttu-id="54224-151">ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงที่อยู่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="54224-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="54224-152">**ฟิลด์หลัก**</span><span class="sxs-lookup"><span data-stu-id="54224-152">**Primary field**</span></span><br><span data-ttu-id="54224-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="54224-153">mshr_primaryfield</span></span><br><span data-ttu-id="54224-154">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-154">*String*</span></span> | <span data-ttu-id="54224-155">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-155">Read-only</span></span><br><span data-ttu-id="54224-156">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-156">Required</span></span> |  |
| <span data-ttu-id="54224-157">**ถนน**</span><span class="sxs-lookup"><span data-stu-id="54224-157">**Street**</span></span><br><span data-ttu-id="54224-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="54224-158">mshr_street</span></span><br><span data-ttu-id="54224-159">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-159">*String*</span></span> | <span data-ttu-id="54224-160">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-160">Read-only</span></span><br><span data-ttu-id="54224-161">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-161">Required</span></span> | <span data-ttu-id="54224-162">ถนนที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="54224-162">The street defined for the address.</span></span> |
| <span data-ttu-id="54224-163">**มีผลใช้ถึง**</span><span class="sxs-lookup"><span data-stu-id="54224-163">**Valid to**</span></span><br><span data-ttu-id="54224-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="54224-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="54224-165">*ออฟเซ็ตเวลา วันที่*</span><span class="sxs-lookup"><span data-stu-id="54224-165">*Date Time Offset*</span></span> | <span data-ttu-id="54224-166">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-166">Read-only</span></span> <br><span data-ttu-id="54224-167">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-167">Required</span></span> | <span data-ttu-id="54224-168">วันที่ที่ที่อยู่มีผลบังคับใช้ถึง</span><span class="sxs-lookup"><span data-stu-id="54224-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="54224-169">**รหัสสถานที่**</span><span class="sxs-lookup"><span data-stu-id="54224-169">**Location ID**</span></span><br><span data-ttu-id="54224-170">mshr_locationidbr>*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="54224-171">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-171">Read-only</span></span> <br><span data-ttu-id="54224-172">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-172">Required</span></span> | <span data-ttu-id="54224-173">รหัสของที่อยู่</span><span class="sxs-lookup"><span data-stu-id="54224-173">The ID for the address.</span></span>  |
| <span data-ttu-id="54224-174">**รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="54224-174">**Postal code**</span></span><br><span data-ttu-id="54224-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="54224-175">mshr_zipcode</span></span><br><span data-ttu-id="54224-176">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-176">*String*</span></span> | <span data-ttu-id="54224-177">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-177">Read-only</span></span> <br><span data-ttu-id="54224-178">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-178">Required</span></span> |<span data-ttu-id="54224-179">หมายเลขรหัสที่กําหนดไว้ให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="54224-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="54224-180">**ที่อยู่อาศัย**</span><span class="sxs-lookup"><span data-stu-id="54224-180">**Lived in address**</span></span><br><span data-ttu-id="54224-181">mshr_islivedinaddressbr>*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="54224-182">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-182">Read-only</span></span><br><span data-ttu-id="54224-183">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-183">Required</span></span> | <span data-ttu-id="54224-184">แสดงถ้าที่อยู่เป็นที่อยู่ที่พนักงานอาศัย</span><span class="sxs-lookup"><span data-stu-id="54224-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="54224-185">**จังหวัด**</span><span class="sxs-lookup"><span data-stu-id="54224-185">**State**</span></span><br><span data-ttu-id="54224-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="54224-186">mshr_state</span></span><br><span data-ttu-id="54224-187">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="54224-187">*String*</span></span> | <span data-ttu-id="54224-188">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="54224-188">Read-only</span></span><br><span data-ttu-id="54224-189">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="54224-189">Required</span></span> | <span data-ttu-id="54224-190">รัฐที่ระบุสำหรับที่อยู่</span><span class="sxs-lookup"><span data-stu-id="54224-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="54224-191">ตัวอย่างการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54224-191">Example query</span></span>

<span data-ttu-id="54224-192">**คำขอ**</span><span class="sxs-lookup"><span data-stu-id="54224-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="54224-193">**การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="54224-193">**Response**</span></span>

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
