---
title: ความถี่ในการคัดกรอง
description: หัวข้อนี้อธิบายชุดตัวเลือกความถี่ของคัดกรองสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: b98f25cb0129c2723a5a9e86839db0b0958bbb11
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054079"
---
# <a name="screening-frequency"></a><span data-ttu-id="27ea7-103">ความถี่ในการคัดกรอง</span><span class="sxs-lookup"><span data-stu-id="27ea7-103">Screening frequency</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="27ea7-104">หัวข้อนี้อธิบายชุดตัวเลือกความถี่ของคัดกรองสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="27ea7-104">This topic describes the Screening frequency option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="27ea7-105">ชื่อทางกายภาพ: mshr_hcmfrequencyunit</span><span class="sxs-lookup"><span data-stu-id="27ea7-105">Physical name: mshr_hcmfrequencyunit</span></span>

<span data-ttu-id="27ea7-106">การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสำหรับความถี่ในการคัดกรอง</span><span class="sxs-lookup"><span data-stu-id="27ea7-106">This enumeration provides the option set of values for the screening frequency.</span></span> 

| <span data-ttu-id="27ea7-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="27ea7-107">Value</span></span> | <span data-ttu-id="27ea7-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="27ea7-108">Label</span></span> | <span data-ttu-id="27ea7-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="27ea7-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="27ea7-110">200000000 ครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="27ea7-110">200000000 One-time only</span></span> | <span data-ttu-id="27ea7-111">ต้องมีคัดกรองเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="27ea7-111">The screening is required only once.</span></span> |
| <span data-ttu-id="27ea7-112">200000001 รายวัน</span><span class="sxs-lookup"><span data-stu-id="27ea7-112">200000001 Daily</span></span> | <span data-ttu-id="27ea7-113">ความถี่ของคัดกรองจะคํานวณเป็นวัน</span><span class="sxs-lookup"><span data-stu-id="27ea7-113">The screening frequency is calculated in days.</span></span> |
| <span data-ttu-id="27ea7-114">200000002 รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="27ea7-114">200000002 Weekly</span></span> | <span data-ttu-id="27ea7-115">ความถี่ของคัดกรองจะคํานวณเป็นสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="27ea7-115">The screening frequency is calculated in weeks.</span></span> |
| <span data-ttu-id="27ea7-116">200000003 รายเดือน</span><span class="sxs-lookup"><span data-stu-id="27ea7-116">200000003 Monthly</span></span> | <span data-ttu-id="27ea7-117">ความถี่ของคัดกรองจะคํานวณเป็นเดือน</span><span class="sxs-lookup"><span data-stu-id="27ea7-117">The screening frequency is calculated in months.</span></span> |
| <span data-ttu-id="27ea7-118">200000004 รายปี</span><span class="sxs-lookup"><span data-stu-id="27ea7-118">200000004 Yearly</span></span> | <span data-ttu-id="27ea7-119">ความถี่ของคัดกรองจะคํานวณเป็นปี</span><span class="sxs-lookup"><span data-stu-id="27ea7-119">The screening frequency is calculated in years.</span></span> |

## <a name="see-also"></a><span data-ttu-id="27ea7-120">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="27ea7-120">See also</span></span>

[<span data-ttu-id="27ea7-121">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="27ea7-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="27ea7-122">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="27ea7-122">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]