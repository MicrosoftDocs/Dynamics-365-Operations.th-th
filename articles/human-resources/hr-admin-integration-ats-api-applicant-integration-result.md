---
title: ผลการรวมผู้สมัคร
description: หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8bef974abff18d7c07ecd679b7e01b31ea1459c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053910"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="7a9b9-103">ผลการรวมผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="7a9b9-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7a9b9-104">หัวข้อนี้อธิบายชุดตัวเลือกผลลัพธ์การรวมผู้สมัครสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="7a9b9-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7a9b9-105">ชื่อทางกายภาพ: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="7a9b9-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="7a9b9-106">การแจงนับนี้จะระบุสถานะเกี่ยวกับเรกคอร์ดผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="7a9b9-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="7a9b9-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="7a9b9-107">Value</span></span> | <span data-ttu-id="7a9b9-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="7a9b9-108">Label</span></span> | <span data-ttu-id="7a9b9-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7a9b9-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7a9b9-110">200000000</span><span class="sxs-lookup"><span data-stu-id="7a9b9-110">200000000</span></span> | <span data-ttu-id="7a9b9-111">ไม่ได้ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="7a9b9-111">Not processed</span></span> | <span data-ttu-id="7a9b9-112">ผู้สมัครยังคงอยู่ภายใต้การพิจารณา</span><span class="sxs-lookup"><span data-stu-id="7a9b9-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="7a9b9-113">200000001</span><span class="sxs-lookup"><span data-stu-id="7a9b9-113">200000001</span></span> | <span data-ttu-id="7a9b9-114">จ้างงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="7a9b9-114">Hired</span></span> | <span data-ttu-id="7a9b9-115">ผู้สมัครได้รับการว่าจ้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="7a9b9-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="7a9b9-116">200000002</span><span class="sxs-lookup"><span data-stu-id="7a9b9-116">200000002</span></span> | <span data-ttu-id="7a9b9-117">ไม่จ้าง</span><span class="sxs-lookup"><span data-stu-id="7a9b9-117">Not hired</span></span> | <span data-ttu-id="7a9b9-118">ได้ตัดสินใจแล้วว่าไม่ว่าจ้างผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="7a9b9-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="7a9b9-119">200000003</span><span class="sxs-lookup"><span data-stu-id="7a9b9-119">200000003</span></span> | <span data-ttu-id="7a9b9-120">ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="7a9b9-120">Dismissed</span></span> | <span data-ttu-id="7a9b9-121">ผู้สมัครถูกยกเลิกจากการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="7a9b9-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7a9b9-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="7a9b9-122">See also</span></span>

[<span data-ttu-id="7a9b9-123">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="7a9b9-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7a9b9-124">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="7a9b9-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]