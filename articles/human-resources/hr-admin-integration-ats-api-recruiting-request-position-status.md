---
title: สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126061"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="01b75-103">สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="01b75-103">Recruiting request position status</span></span>

<span data-ttu-id="01b75-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="01b75-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="01b75-105">ชื่อทางกายภาพ: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="01b75-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="01b75-106">การแจงนับนี้จะมีตัวเลือกการตั้งค่าสถานะของแต่ละตําแหน่งเป็นคำขอการสรรหาบุคลากรในเอนทิตี RecruitingRequestPosition</span><span class="sxs-lookup"><span data-stu-id="01b75-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="01b75-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="01b75-107">Value</span></span> | <span data-ttu-id="01b75-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="01b75-108">Label</span></span> | <span data-ttu-id="01b75-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="01b75-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="01b75-110">200000000</span><span class="sxs-lookup"><span data-stu-id="01b75-110">200000000</span></span> | <span data-ttu-id="01b75-111">เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="01b75-111">Open</span></span> | <span data-ttu-id="01b75-112">ตําแหน่งในคำขอการสรรหาบุคลากรเปิดรับการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="01b75-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="01b75-113">การมอบหมายตําแหน่งงานนี้จะไม่ได้บ่งชี้ว่าไม่มีการมอบหมายตําแหน่งที่ใช้งานอยู่ในปัจจุบันให้กับตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="01b75-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="01b75-114">อาจมีพนักงานในตําแหน่งเมื่อสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="01b75-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="01b75-115">ตําแหน่งนี้บ่งชี้ว่าตําแหน่งนี้ว่างเฉพาะสำหรับการสรรหาบุคลากรในบริบทของคำขอการสรรหาบุคลากรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="01b75-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="01b75-116">200000001</span><span class="sxs-lookup"><span data-stu-id="01b75-116">200000001</span></span> | <span data-ttu-id="01b75-117">บรรจุแล้ว</span><span class="sxs-lookup"><span data-stu-id="01b75-117">Filled</span></span> | <span data-ttu-id="01b75-118">ผู้ปฏิบัติงานถูกเลือกเพื่อมอบหมายตําแหน่งงานให้กับตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="01b75-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="01b75-119">200000002</span><span class="sxs-lookup"><span data-stu-id="01b75-119">200000002</span></span> | <span data-ttu-id="01b75-120">ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="01b75-120">Canceled</span></span> | <span data-ttu-id="01b75-121">คำขอสรรหาบุคลากรให้กับตําแหน่งนี้ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="01b75-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="01b75-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="01b75-122">See also</span></span>

[<span data-ttu-id="01b75-123">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="01b75-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="01b75-124">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="01b75-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
