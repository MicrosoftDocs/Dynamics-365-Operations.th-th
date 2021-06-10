---
title: สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051892"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="81b2c-103">สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="81b2c-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="81b2c-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรที่มีคำขอตำแหน่งสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="81b2c-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="81b2c-105">ชื่อทางกายภาพ: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="81b2c-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="81b2c-106">การแจงนับนี้จะมีตัวเลือกการตั้งค่าสถานะของแต่ละตําแหน่งเป็นคำขอการสรรหาบุคลากรในเอนทิตี RecruitingRequestPosition</span><span class="sxs-lookup"><span data-stu-id="81b2c-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="81b2c-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="81b2c-107">Value</span></span> | <span data-ttu-id="81b2c-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="81b2c-108">Label</span></span> | <span data-ttu-id="81b2c-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="81b2c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="81b2c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="81b2c-110">200000000</span></span> | <span data-ttu-id="81b2c-111">เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="81b2c-111">Open</span></span> | <span data-ttu-id="81b2c-112">ตําแหน่งในคำขอการสรรหาบุคลากรเปิดรับการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="81b2c-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="81b2c-113">การมอบหมายตําแหน่งงานนี้จะไม่ได้บ่งชี้ว่าไม่มีการมอบหมายตําแหน่งที่ใช้งานอยู่ในปัจจุบันให้กับตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="81b2c-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="81b2c-114">อาจมีพนักงานในตําแหน่งเมื่อสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="81b2c-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="81b2c-115">ตําแหน่งนี้บ่งชี้ว่าตําแหน่งนี้ว่างเฉพาะสำหรับการสรรหาบุคลากรในบริบทของคำขอการสรรหาบุคลากรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="81b2c-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="81b2c-116">200000001</span><span class="sxs-lookup"><span data-stu-id="81b2c-116">200000001</span></span> | <span data-ttu-id="81b2c-117">บรรจุแล้ว</span><span class="sxs-lookup"><span data-stu-id="81b2c-117">Filled</span></span> | <span data-ttu-id="81b2c-118">ผู้ปฏิบัติงานถูกเลือกเพื่อมอบหมายตําแหน่งงานให้กับตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="81b2c-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="81b2c-119">200000002</span><span class="sxs-lookup"><span data-stu-id="81b2c-119">200000002</span></span> | <span data-ttu-id="81b2c-120">ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="81b2c-120">Canceled</span></span> | <span data-ttu-id="81b2c-121">คำขอสรรหาบุคลากรให้กับตําแหน่งนี้ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="81b2c-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="81b2c-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="81b2c-122">See also</span></span>

[<span data-ttu-id="81b2c-123">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="81b2c-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="81b2c-124">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="81b2c-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]