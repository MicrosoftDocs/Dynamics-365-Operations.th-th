---
title: ชนิดการคัดเลือก
description: หัวข้อนี้อธิบายเอนทิตีชนิดการคัดเลือกสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465929"
---
# <a name="screening-types"></a><span data-ttu-id="918a5-103">ชนิดการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="918a5-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="918a5-104">หัวข้อนี้อธิบายเอนทิตีชนิดการคัดเลือกสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="918a5-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="918a5-105">ชื่อทางกายภาพ: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="918a5-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="918a5-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="918a5-106">Description</span></span>

<span data-ttu-id="918a5-107">เอนทิตีนี้อธิบายชนิดการคัดเลือกและตั้งค่าโดยบริษัทสำหรับกระบวนการคัดเลือกพนักงานก่อนการจ้างงานและปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="918a5-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="918a5-108">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="918a5-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="918a5-109">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="918a5-109">Properties</span></span>

| <span data-ttu-id="918a5-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="918a5-110">Property</span></span><br><span data-ttu-id="918a5-111">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="918a5-111">**Physical name**</span></span><br><span data-ttu-id="918a5-112">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="918a5-112">**_Type_**</span></span> | <span data-ttu-id="918a5-113">ใช้</span><span class="sxs-lookup"><span data-stu-id="918a5-113">Use</span></span> | <span data-ttu-id="918a5-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="918a5-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="918a5-115">**รหัสเอนทิตีชนิดการคัดเลือก**</span><span class="sxs-lookup"><span data-stu-id="918a5-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="918a5-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="918a5-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="918a5-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="918a5-117">*GUID*</span></span> | <span data-ttu-id="918a5-118">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="918a5-118">Read-only</span></span><br><span data-ttu-id="918a5-119">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="918a5-119">Required</span></span><br><span data-ttu-id="918a5-120">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="918a5-120">System-generated</span></span> | <span data-ttu-id="918a5-121">ตัวระบุหลักเฉพาะของเรกคอร์ดชนิดการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="918a5-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="918a5-122">**รหัสชนิดการคัดเลือก**</span><span class="sxs-lookup"><span data-stu-id="918a5-122">**Screening Type ID**</span></span><br><span data-ttu-id="918a5-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="918a5-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="918a5-124">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="918a5-124">*String*</span></span> | <span data-ttu-id="918a5-125">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="918a5-125">Read/write</span></span><br><span data-ttu-id="918a5-126">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="918a5-126">Required</span></span> | <span data-ttu-id="918a5-127">ตัวระบุเฉพาะที่กำหนดโดยผู้ใช้ของชนิดการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="918a5-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="918a5-128">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="918a5-128">**Description**</span></span><br><span data-ttu-id="918a5-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="918a5-129">mshr_description</span></span><br><span data-ttu-id="918a5-130">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="918a5-130">*String*</span></span> | <span data-ttu-id="918a5-131">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="918a5-131">Read/write</span></span><br><span data-ttu-id="918a5-132">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="918a5-132">Required</span></span> | <span data-ttu-id="918a5-133">คำอธิบายเกี่ยวกับชนิดการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="918a5-133">The description of the screening type.</span></span> |
| <span data-ttu-id="918a5-134">**หน่วยความถี่**</span><span class="sxs-lookup"><span data-stu-id="918a5-134">**Frequency Unit**</span></span><br><span data-ttu-id="918a5-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="918a5-135">mshr_frequencyunit</span></span><br><span data-ttu-id="918a5-136">*ชุดตัวเลือก mshr_hcmpersongender*</span><span class="sxs-lookup"><span data-stu-id="918a5-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="918a5-137">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="918a5-137">Read/write</span></span><br><span data-ttu-id="918a5-138">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="918a5-138">Required</span></span> | <span data-ttu-id="918a5-139">อธิบายความถี่ที่การคัดเลือกต้องเสร็จสมบูรณ์ของบุคคลที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="918a5-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="918a5-140">**สร้างจาก**</span><span class="sxs-lookup"><span data-stu-id="918a5-140">**Generate From**</span></span><br><span data-ttu-id="918a5-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="918a5-141">mshr_generatefrom</span></span><br><span data-ttu-id="918a5-142">*ชุดตัวเลือก mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="918a5-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="918a5-143">อ่าน-เขียน</span><span class="sxs-lookup"><span data-stu-id="918a5-143">Read-write</span></span><br><span data-ttu-id="918a5-144">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="918a5-144">Required</span></span> | <span data-ttu-id="918a5-145">ถ้าค่าความถี่เป็นค่าอื่นใดนอกเหนือจาก "ใช้เฉพาะครั้งเท่านั้น" ค่า GenerateFrom จะระบุวันที่เริ่มต้นคํานวณเหตุการณ์การคัดเลือกถัดไป</span><span class="sxs-lookup"><span data-stu-id="918a5-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="918a5-146">**ช่วงเวลาความถี่**</span><span class="sxs-lookup"><span data-stu-id="918a5-146">**Frequency Interval**</span></span><br><span data-ttu-id="918a5-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="918a5-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="918a5-148">*เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="918a5-148">*Integer*</span></span> | <span data-ttu-id="918a5-149">อ่าน-เขียน</span><span class="sxs-lookup"><span data-stu-id="918a5-149">Read-write</span></span><br><span data-ttu-id="918a5-150">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="918a5-150">Required</span></span> | <span data-ttu-id="918a5-151">ถ้าค่าความถี่เป็นค่าอื่นที่ไม่ใช่ "ใช้เฉพาะครั้งเท่านั้น" คุณต้องกําหนดช่วงเวลาให้กับหน่วยเวลาระหว่างเหตุการณ์ของการคัดเลือกแต่ละเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="918a5-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="918a5-152">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="918a5-152">See also</span></span>

[<span data-ttu-id="918a5-153">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="918a5-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="918a5-154">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="918a5-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]