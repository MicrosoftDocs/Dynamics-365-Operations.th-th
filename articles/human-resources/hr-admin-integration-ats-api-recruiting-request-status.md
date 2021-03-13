---
title: สถานะคำขอการสรรหาบุคลากร
description: หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125965"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="68d7b-103">สถานะคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="68d7b-103">Recruiting request status</span></span>

<span data-ttu-id="68d7b-104">หัวข้อนี้อธิบายชุดตัวเลือกสถานะคำขอการสรรหาบุคลากรสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="68d7b-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="68d7b-105">ชื่อทางกายภาพ: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="68d7b-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="68d7b-106">การแจงหมายเลขนี้จะให้ชุดตัวเลือกของค่าสถานะสำหรับ RecruitingRequest</span><span class="sxs-lookup"><span data-stu-id="68d7b-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="68d7b-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="68d7b-107">Value</span></span> | <span data-ttu-id="68d7b-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="68d7b-108">Label</span></span> | <span data-ttu-id="68d7b-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="68d7b-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="68d7b-110">200000000</span><span class="sxs-lookup"><span data-stu-id="68d7b-110">200000000</span></span> | <span data-ttu-id="68d7b-111">ฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="68d7b-111">Draft</span></span> | <span data-ttu-id="68d7b-112">คำขออยู่ในแบบร่างและยังไม่พร้อมรับการสรรหาบุคลากรที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="68d7b-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="68d7b-113">200000001</span><span class="sxs-lookup"><span data-stu-id="68d7b-113">200000001</span></span> | <span data-ttu-id="68d7b-114">อยู่ระหว่างการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="68d7b-114">In Review</span></span> | <span data-ttu-id="68d7b-115">ส่งคำขอแล้วและถูกส่งเพื่ออนุมัติตามลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="68d7b-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="68d7b-116">พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="68d7b-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="68d7b-117">200000002</span><span class="sxs-lookup"><span data-stu-id="68d7b-117">200000002</span></span> | <span data-ttu-id="68d7b-118">รอดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="68d7b-118">Pending</span></span> | <span data-ttu-id="68d7b-119">คำขออยู่ระหว่างการดำเนินการของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="68d7b-119">The request is pending workflow action.</span></span> <span data-ttu-id="68d7b-120">พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="68d7b-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="68d7b-121">200000003</span><span class="sxs-lookup"><span data-stu-id="68d7b-121">200000003</span></span> | <span data-ttu-id="68d7b-122">ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="68d7b-122">Canceled</span></span> | <span data-ttu-id="68d7b-123">คำขอได้รับการยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="68d7b-123">The request has been canceled.</span></span> <span data-ttu-id="68d7b-124">พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="68d7b-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="68d7b-125">200000004</span><span class="sxs-lookup"><span data-stu-id="68d7b-125">200000004</span></span> | <span data-ttu-id="68d7b-126">ถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="68d7b-126">Denied</span></span> | <span data-ttu-id="68d7b-127">ปฏิเสธคำขอ</span><span class="sxs-lookup"><span data-stu-id="68d7b-127">The request has been denied.</span></span> <span data-ttu-id="68d7b-128">พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานลำดับงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="68d7b-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="68d7b-129">200000005</span><span class="sxs-lookup"><span data-stu-id="68d7b-129">200000005</span></span> | <span data-ttu-id="68d7b-130">ที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="68d7b-130">Active</span></span> | <span data-ttu-id="68d7b-131">ลำดับงานเสร็จสมบูรณ์และได้รับอนุมัติแล้ว และคำขอพร้อมแล้วที่จะสรรหาบุคลากรที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="68d7b-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="68d7b-132">200000006</span><span class="sxs-lookup"><span data-stu-id="68d7b-132">200000006</span></span> | <span data-ttu-id="68d7b-133">ปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="68d7b-133">Closed</span></span> | <span data-ttu-id="68d7b-134">ปิดคำขอสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="68d7b-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="68d7b-135">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="68d7b-135">See also</span></span>

[<span data-ttu-id="68d7b-136">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="68d7b-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="68d7b-137">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="68d7b-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
