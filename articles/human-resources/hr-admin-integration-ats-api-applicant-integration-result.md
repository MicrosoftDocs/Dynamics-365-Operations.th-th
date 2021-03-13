---
title: ผลการรวมผู้สมัคร
description: หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 157864cd0eee879013724615ce31306c99c5aa68
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125820"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="698c7-103">ผลการรวมผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="698c7-103">Applicant integration result</span></span>

<span data-ttu-id="698c7-104">หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="698c7-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="698c7-105">ชื่อทางกายภาพ: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="698c7-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="698c7-106">การแจงนับนี้จะระบุสถานะเกี่ยวกับเรกคอร์ดผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="698c7-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="698c7-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="698c7-107">Value</span></span> | <span data-ttu-id="698c7-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="698c7-108">Label</span></span> | <span data-ttu-id="698c7-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="698c7-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="698c7-110">200000000</span><span class="sxs-lookup"><span data-stu-id="698c7-110">200000000</span></span> | <span data-ttu-id="698c7-111">ไม่ได้ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="698c7-111">Not processed</span></span> | <span data-ttu-id="698c7-112">ผู้สมัครยังคงอยู่ภายใต้การพิจารณา</span><span class="sxs-lookup"><span data-stu-id="698c7-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="698c7-113">200000001</span><span class="sxs-lookup"><span data-stu-id="698c7-113">200000001</span></span> | <span data-ttu-id="698c7-114">จ้างงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="698c7-114">Hired</span></span> | <span data-ttu-id="698c7-115">ผู้สมัครได้รับการว่าจ้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="698c7-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="698c7-116">200000002</span><span class="sxs-lookup"><span data-stu-id="698c7-116">200000002</span></span> | <span data-ttu-id="698c7-117">ไม่จ้าง</span><span class="sxs-lookup"><span data-stu-id="698c7-117">Not hired</span></span> | <span data-ttu-id="698c7-118">ได้ตัดสินใจแล้วว่าไม่ว่าจ้างผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="698c7-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="698c7-119">200000003</span><span class="sxs-lookup"><span data-stu-id="698c7-119">200000003</span></span> | <span data-ttu-id="698c7-120">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="698c7-120">Dismissed</span></span> | <span data-ttu-id="698c7-121">ผู้สมัครถูกยกเลิกจากการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="698c7-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="698c7-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="698c7-122">See also</span></span>

[<span data-ttu-id="698c7-123">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="698c7-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="698c7-124">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="698c7-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
