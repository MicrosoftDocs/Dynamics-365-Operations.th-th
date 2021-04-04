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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464729"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="9bbd4-103">สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="9bbd4-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9bbd4-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="9bbd4-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9bbd4-105">ชื่อทางกายภาพ: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="9bbd4-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="9bbd4-106">การแจงนับนี้จะมีตัวเลือกการตั้งค่าสถานะของแต่ละตําแหน่งเป็นคำขอการสรรหาบุคลากรในเอนทิตี RecruitingRequestPosition</span><span class="sxs-lookup"><span data-stu-id="9bbd4-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="9bbd4-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="9bbd4-107">Value</span></span> | <span data-ttu-id="9bbd4-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="9bbd4-108">Label</span></span> | <span data-ttu-id="9bbd4-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9bbd4-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9bbd4-110">200000000</span><span class="sxs-lookup"><span data-stu-id="9bbd4-110">200000000</span></span> | <span data-ttu-id="9bbd4-111">เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="9bbd4-111">Open</span></span> | <span data-ttu-id="9bbd4-112">ตําแหน่งในคำขอการสรรหาบุคลากรเปิดรับการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="9bbd4-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="9bbd4-113">การมอบหมายตําแหน่งงานนี้จะไม่ได้บ่งชี้ว่าไม่มีการมอบหมายตําแหน่งที่ใช้งานอยู่ในปัจจุบันให้กับตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="9bbd4-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="9bbd4-114">อาจมีพนักงานในตําแหน่งเมื่อสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="9bbd4-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="9bbd4-115">ตําแหน่งนี้บ่งชี้ว่าตําแหน่งนี้ว่างเฉพาะสำหรับการสรรหาบุคลากรในบริบทของคำขอการสรรหาบุคลากรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9bbd4-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="9bbd4-116">200000001</span><span class="sxs-lookup"><span data-stu-id="9bbd4-116">200000001</span></span> | <span data-ttu-id="9bbd4-117">บรรจุแล้ว</span><span class="sxs-lookup"><span data-stu-id="9bbd4-117">Filled</span></span> | <span data-ttu-id="9bbd4-118">ผู้ปฏิบัติงานถูกเลือกเพื่อมอบหมายตําแหน่งงานให้กับตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="9bbd4-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="9bbd4-119">200000002</span><span class="sxs-lookup"><span data-stu-id="9bbd4-119">200000002</span></span> | <span data-ttu-id="9bbd4-120">ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="9bbd4-120">Canceled</span></span> | <span data-ttu-id="9bbd4-121">คำขอสรรหาบุคลากรให้กับตําแหน่งนี้ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="9bbd4-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9bbd4-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="9bbd4-122">See also</span></span>

[<span data-ttu-id="9bbd4-123">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="9bbd4-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9bbd4-124">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="9bbd4-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]