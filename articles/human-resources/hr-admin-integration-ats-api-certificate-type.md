---
title: ชนิดของประกาศนียบัตร
description: หัวข้อนี้อธิบายเอนทิตี้ชนิดของใบรับรองสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125724"
---
# <a name="certificate-type"></a><span data-ttu-id="b7f77-103">ชนิดของประกาศนียบัตร</span><span class="sxs-lookup"><span data-stu-id="b7f77-103">Certificate type</span></span>

<span data-ttu-id="b7f77-104">หัวข้อนี้อธิบายเอนทิตี้ชนิดของใบรับรองสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="b7f77-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b7f77-105">ชื่อทางกายภาพ: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="b7f77-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="b7f77-106">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b7f77-106">Description</span></span>

<span data-ttu-id="b7f77-107">เอนทิตี้นี้จะกําหนดรายการของชนิดใบรับรองวิชาชีพที่ตั้งค่าในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b7f77-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="b7f77-108">เอนทิตี้ไม่ได้ระบุเฉพาะกับนิติบุคคล (บริษัท)</span><span class="sxs-lookup"><span data-stu-id="b7f77-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="b7f77-109">การแสดง JSON</span><span class="sxs-lookup"><span data-stu-id="b7f77-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="b7f77-110">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b7f77-110">Properties</span></span>

| <span data-ttu-id="b7f77-111">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b7f77-111">Property</span></span><br><span data-ttu-id="b7f77-112">**ชื่อทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="b7f77-112">**Physical name**</span></span><br><span data-ttu-id="b7f77-113">**_ชนิด_**</span><span class="sxs-lookup"><span data-stu-id="b7f77-113">**_Type_**</span></span> | <span data-ttu-id="b7f77-114">ใช้</span><span class="sxs-lookup"><span data-stu-id="b7f77-114">Use</span></span> | <span data-ttu-id="b7f77-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b7f77-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b7f77-116">**รหัสเอนทิตี้ชนิดใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="b7f77-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="b7f77-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="b7f77-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="b7f77-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b7f77-118">*GUID*</span></span> | <span data-ttu-id="b7f77-119">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="b7f77-119">Read-only</span></span><br><span data-ttu-id="b7f77-120">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="b7f77-120">Required</span></span> 
<span data-ttu-id="b7f77-121">ระบบถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b7f77-121">System-generated</span></span> | <span data-ttu-id="b7f77-122">ตัวระบุหลักที่ไม่ซ้ำกันสำหรับชนิดใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="b7f77-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="b7f77-123">**ชนิดใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="b7f77-123">**Certificate Type**</span></span><br><span data-ttu-id="b7f77-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="b7f77-124">mshr_certificatetype</span></span><br><span data-ttu-id="b7f77-125">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="b7f77-125">*String*</span></span> | <span data-ttu-id="b7f77-126">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="b7f77-126">Read/write</span></span><br><span data-ttu-id="b7f77-127">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="b7f77-127">Required</span></span> | <span data-ttu-id="b7f77-128">ตัวระบุของผู้ใช้สามารถอ่านได้ที่ไม่ซ้ำกันสำหรับชนิดใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="b7f77-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="b7f77-129">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="b7f77-129">**Description**</span></span><br><span data-ttu-id="b7f77-130">msdyn_description</span><span class="sxs-lookup"><span data-stu-id="b7f77-130">mshr_description</span></span><br><span data-ttu-id="b7f77-131">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="b7f77-131">*String*</span></span> | <span data-ttu-id="b7f77-132">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="b7f77-132">Read/write</span></span><br><span data-ttu-id="b7f77-133">จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="b7f77-133">Required</span></span> | <span data-ttu-id="b7f77-134">คำอธิบายของชนิดใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="b7f77-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="b7f77-135">**ต้องการการต่ออายุ**</span><span class="sxs-lookup"><span data-stu-id="b7f77-135">**Require Renewal**</span></span><br><span data-ttu-id="b7f77-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="b7f77-136">mshr_requirerenewal</span></span><br><span data-ttu-id="b7f77-137">*mshr_noyes ตัวเลือกที่ตั้งค่า*</span><span class="sxs-lookup"><span data-stu-id="b7f77-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="b7f77-138">อ่าน/เขียน</span><span class="sxs-lookup"><span data-stu-id="b7f77-138">Read/write</span></span><br><span data-ttu-id="b7f77-139">ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="b7f77-139">Optional</span></span> | <span data-ttu-id="b7f77-140">ระบุว่าการต่ออายุจำเป็นสำหรับใบรับรองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b7f77-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b7f77-141">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b7f77-141">See also</span></span>

[<span data-ttu-id="b7f77-142">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b7f77-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b7f77-143">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="b7f77-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

