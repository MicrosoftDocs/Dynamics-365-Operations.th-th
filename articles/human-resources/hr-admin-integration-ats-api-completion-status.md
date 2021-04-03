---
title: สถานะการเสร็จสมบูรณ์
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468214"
---
# <a name="completion-status"></a><span data-ttu-id="638cd-103">สถานะการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="638cd-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="638cd-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="638cd-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="638cd-105">ชื่อทางกายภาพ: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="638cd-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="638cd-106">การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสถานะสำหรับการคัดเลือกผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="638cd-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="638cd-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="638cd-107">Value</span></span> | <span data-ttu-id="638cd-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="638cd-108">Label</span></span> | <span data-ttu-id="638cd-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="638cd-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="638cd-110">200000000</span><span class="sxs-lookup"><span data-stu-id="638cd-110">200000000</span></span> | <span data-ttu-id="638cd-111">ไม่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="638cd-111">Not Complete</span></span> | <span data-ttu-id="638cd-112">ผู้สมัครยังไม่เสร็จสิ้นการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="638cd-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="638cd-113">200000001</span><span class="sxs-lookup"><span data-stu-id="638cd-113">200000001</span></span> | <span data-ttu-id="638cd-114">ผ่าน</span><span class="sxs-lookup"><span data-stu-id="638cd-114">Pass</span></span> | <span data-ttu-id="638cd-115">ผู้สมัครได้ผ่านคัดเลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="638cd-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="638cd-116">200000002</span><span class="sxs-lookup"><span data-stu-id="638cd-116">200000002</span></span> | <span data-ttu-id="638cd-117">ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="638cd-117">Fail</span></span> | <span data-ttu-id="638cd-118">ผู้สมัครไม่ได้ผ่านคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="638cd-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="638cd-119">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="638cd-119">See also</span></span>

[<span data-ttu-id="638cd-120">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="638cd-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="638cd-121">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="638cd-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]