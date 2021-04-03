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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467564"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="74f06-103">ผลการรวมผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="74f06-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="74f06-104">หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="74f06-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="74f06-105">ชื่อทางกายภาพ: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="74f06-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="74f06-106">การแจงนับนี้จะระบุสถานะเกี่ยวกับเรกคอร์ดผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="74f06-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="74f06-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="74f06-107">Value</span></span> | <span data-ttu-id="74f06-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="74f06-108">Label</span></span> | <span data-ttu-id="74f06-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="74f06-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="74f06-110">200000000</span><span class="sxs-lookup"><span data-stu-id="74f06-110">200000000</span></span> | <span data-ttu-id="74f06-111">ไม่ได้ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="74f06-111">Not processed</span></span> | <span data-ttu-id="74f06-112">ผู้สมัครยังคงอยู่ภายใต้การพิจารณา</span><span class="sxs-lookup"><span data-stu-id="74f06-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="74f06-113">200000001</span><span class="sxs-lookup"><span data-stu-id="74f06-113">200000001</span></span> | <span data-ttu-id="74f06-114">จ้างงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="74f06-114">Hired</span></span> | <span data-ttu-id="74f06-115">ผู้สมัครได้รับการว่าจ้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="74f06-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="74f06-116">200000002</span><span class="sxs-lookup"><span data-stu-id="74f06-116">200000002</span></span> | <span data-ttu-id="74f06-117">ไม่จ้าง</span><span class="sxs-lookup"><span data-stu-id="74f06-117">Not hired</span></span> | <span data-ttu-id="74f06-118">ได้ตัดสินใจแล้วว่าไม่ว่าจ้างผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="74f06-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="74f06-119">200000003</span><span class="sxs-lookup"><span data-stu-id="74f06-119">200000003</span></span> | <span data-ttu-id="74f06-120">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="74f06-120">Dismissed</span></span> | <span data-ttu-id="74f06-121">ผู้สมัครถูกยกเลิกจากการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="74f06-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="74f06-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="74f06-122">See also</span></span>

[<span data-ttu-id="74f06-123">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="74f06-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="74f06-124">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="74f06-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]