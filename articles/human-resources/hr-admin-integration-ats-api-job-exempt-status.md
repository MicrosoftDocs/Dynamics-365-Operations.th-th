---
title: สถานะยกเว้นงาน
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125580"
---
# <a name="job-exempt-status"></a><span data-ttu-id="18820-103">สถานะยกเว้นงาน</span><span class="sxs-lookup"><span data-stu-id="18820-103">Job exempt status</span></span>

<span data-ttu-id="18820-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะยกเว้นงานสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="18820-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="18820-105">ชื่อทางกายภาพ: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="18820-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="18820-106">การแจงนับนี้ระบุชุดตัวเลือกสำหรับค่าสถานะยกเว้นงานสำหรับ FLSA</span><span class="sxs-lookup"><span data-stu-id="18820-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="18820-107">มีอยู่ในชุดตัวเลือก cdm_jobexemptstatus ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="18820-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="18820-108">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="18820-108">Value</span></span> | <span data-ttu-id="18820-109">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="18820-109">Label</span></span> | <span data-ttu-id="18820-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="18820-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="18820-111">200000000</span><span class="sxs-lookup"><span data-stu-id="18820-111">200000000</span></span> | <span data-ttu-id="18820-112">ยกเว้น</span><span class="sxs-lookup"><span data-stu-id="18820-112">Exempt</span></span> | <span data-ttu-id="18820-113">งานมีสถานะยกเว้นตามแนวทาง FLSA</span><span class="sxs-lookup"><span data-stu-id="18820-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="18820-114">200000001</span><span class="sxs-lookup"><span data-stu-id="18820-114">200000001</span></span> | <span data-ttu-id="18820-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="18820-115">NonExempt</span></span> | <span data-ttu-id="18820-116">งานมีสถานะไม่ยกเว้นตามแนวทาง FLSA</span><span class="sxs-lookup"><span data-stu-id="18820-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="18820-117">200000002</span><span class="sxs-lookup"><span data-stu-id="18820-117">200000002</span></span> | <span data-ttu-id="18820-118">ไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="18820-118">Does Not Apply</span></span> | <span data-ttu-id="18820-119">แนวทางสถานะ FLSA ไม่ใช้กับงาน</span><span class="sxs-lookup"><span data-stu-id="18820-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="18820-120">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="18820-120">See also</span></span>

[<span data-ttu-id="18820-121">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="18820-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="18820-122">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="18820-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
