---
title: สถานะการเสร็จสมบูรณ์
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055375"
---
# <a name="completion-status"></a><span data-ttu-id="cc3ea-103">สถานะการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cc3ea-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cc3ea-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="cc3ea-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cc3ea-105">ชื่อทางกายภาพ: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="cc3ea-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="cc3ea-106">การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสถานะสำหรับการคัดเลือกผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="cc3ea-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="cc3ea-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="cc3ea-107">Value</span></span> | <span data-ttu-id="cc3ea-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="cc3ea-108">Label</span></span> | <span data-ttu-id="cc3ea-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cc3ea-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cc3ea-110">200000000</span><span class="sxs-lookup"><span data-stu-id="cc3ea-110">200000000</span></span> | <span data-ttu-id="cc3ea-111">ไม่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cc3ea-111">Not Complete</span></span> | <span data-ttu-id="cc3ea-112">ผู้สมัครยังไม่เสร็จสิ้นการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="cc3ea-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="cc3ea-113">200000001</span><span class="sxs-lookup"><span data-stu-id="cc3ea-113">200000001</span></span> | <span data-ttu-id="cc3ea-114">ผ่าน</span><span class="sxs-lookup"><span data-stu-id="cc3ea-114">Pass</span></span> | <span data-ttu-id="cc3ea-115">ผู้สมัครได้ผ่านคัดเลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="cc3ea-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="cc3ea-116">200000002</span><span class="sxs-lookup"><span data-stu-id="cc3ea-116">200000002</span></span> | <span data-ttu-id="cc3ea-117">ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="cc3ea-117">Fail</span></span> | <span data-ttu-id="cc3ea-118">ผู้สมัครไม่ได้ผ่านคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="cc3ea-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cc3ea-119">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="cc3ea-119">See also</span></span>

[<span data-ttu-id="cc3ea-120">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="cc3ea-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cc3ea-121">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="cc3ea-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]