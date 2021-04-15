---
title: สถานะการเสร็จสมบูรณ์
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798380"
---
# <a name="completion-status"></a><span data-ttu-id="97651-103">สถานะการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="97651-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="97651-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะการเสร็จสมบูรณ์สำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="97651-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="97651-105">ชื่อทางกายภาพ: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="97651-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="97651-106">การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสถานะสำหรับการคัดเลือกผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="97651-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="97651-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="97651-107">Value</span></span> | <span data-ttu-id="97651-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="97651-108">Label</span></span> | <span data-ttu-id="97651-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="97651-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="97651-110">200000000</span><span class="sxs-lookup"><span data-stu-id="97651-110">200000000</span></span> | <span data-ttu-id="97651-111">ไม่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="97651-111">Not Complete</span></span> | <span data-ttu-id="97651-112">ผู้สมัครยังไม่เสร็จสิ้นการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="97651-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="97651-113">200000001</span><span class="sxs-lookup"><span data-stu-id="97651-113">200000001</span></span> | <span data-ttu-id="97651-114">ผ่าน</span><span class="sxs-lookup"><span data-stu-id="97651-114">Pass</span></span> | <span data-ttu-id="97651-115">ผู้สมัครได้ผ่านคัดเลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="97651-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="97651-116">200000002</span><span class="sxs-lookup"><span data-stu-id="97651-116">200000002</span></span> | <span data-ttu-id="97651-117">ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="97651-117">Fail</span></span> | <span data-ttu-id="97651-118">ผู้สมัครไม่ได้ผ่านคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="97651-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="97651-119">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="97651-119">See also</span></span>

[<span data-ttu-id="97651-120">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="97651-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="97651-121">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="97651-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]