---
title: สถานะยกเว้นงาน
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053862"
---
# <a name="job-exempt-status"></a><span data-ttu-id="f46b0-103">สถานะยกเว้นงาน</span><span class="sxs-lookup"><span data-stu-id="f46b0-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f46b0-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f46b0-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f46b0-105">ชื่อทางกายภาพ: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="f46b0-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="f46b0-106">การแจงนับนี้ระบุชุดตัวเลือกสำหรับค่าสถานะยกเว้นงานสำหรับ FLSA</span><span class="sxs-lookup"><span data-stu-id="f46b0-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="f46b0-107">มีอยู่ในชุดตัวเลือก cdm_jobexemptstatus ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f46b0-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="f46b0-108">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f46b0-108">Value</span></span> | <span data-ttu-id="f46b0-109">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="f46b0-109">Label</span></span> | <span data-ttu-id="f46b0-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f46b0-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f46b0-111">200000000</span><span class="sxs-lookup"><span data-stu-id="f46b0-111">200000000</span></span> | <span data-ttu-id="f46b0-112">ยกเว้น</span><span class="sxs-lookup"><span data-stu-id="f46b0-112">Exempt</span></span> | <span data-ttu-id="f46b0-113">งานมีสถานะยกเว้นตามแนวทาง FLSA</span><span class="sxs-lookup"><span data-stu-id="f46b0-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="f46b0-114">200000001</span><span class="sxs-lookup"><span data-stu-id="f46b0-114">200000001</span></span> | <span data-ttu-id="f46b0-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="f46b0-115">NonExempt</span></span> | <span data-ttu-id="f46b0-116">งานมีสถานะไม่ยกเว้นตามแนวทาง FLSA</span><span class="sxs-lookup"><span data-stu-id="f46b0-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="f46b0-117">200000002</span><span class="sxs-lookup"><span data-stu-id="f46b0-117">200000002</span></span> | <span data-ttu-id="f46b0-118">ไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="f46b0-118">Does Not Apply</span></span> | <span data-ttu-id="f46b0-119">แนวทางสถานะ FLSA ไม่ใช้กับงาน</span><span class="sxs-lookup"><span data-stu-id="f46b0-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f46b0-120">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="f46b0-120">See also</span></span>

[<span data-ttu-id="f46b0-121">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="f46b0-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f46b0-122">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="f46b0-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]