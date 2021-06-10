---
title: ความถี่ในการคัดกรองที่สร้างจาก
description: หัวข้อนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054103"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="1c3f5-103">ความถี่ในการคัดกรองที่สร้างจาก</span><span class="sxs-lookup"><span data-stu-id="1c3f5-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1c3f5-104">หัวข้อนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="1c3f5-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1c3f5-105">ชื่อทางกายภาพ: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="1c3f5-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="1c3f5-106">การกําหนดตัวเลขนี้จะให้ชุดตัวเลือกของค่าในการกําหนดวันที่เริ่มต้นของการคํานวณเพื่อคัดกรองที่ต้องการครั้งต่อไป</span><span class="sxs-lookup"><span data-stu-id="1c3f5-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="1c3f5-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="1c3f5-107">Value</span></span> | <span data-ttu-id="1c3f5-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="1c3f5-108">Label</span></span> | <span data-ttu-id="1c3f5-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c3f5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1c3f5-110">200000000 ไม่ได้เลือก</span><span class="sxs-lookup"><span data-stu-id="1c3f5-110">200000000 Not selected</span></span> | <span data-ttu-id="1c3f5-111">ไม่ได้เลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1c3f5-111">No value has been selected.</span></span> |
| <span data-ttu-id="1c3f5-112">200000001 วันที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1c3f5-112">200000001 Date completed</span></span> | <span data-ttu-id="1c3f5-113">การคํานวณจะเสร็จสิ้นจากวันที่ที่คัดกรองครั้งล่าสุดเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1c3f5-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="1c3f5-114">200000002 ต้องระบุวันที่</span><span class="sxs-lookup"><span data-stu-id="1c3f5-114">200000002 Date required</span></span> | <span data-ttu-id="1c3f5-115">การคํานวณจะเสร็จสิ้นจากวันที่ที่คัดกรองครั้งล่าสุดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c3f5-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1c3f5-116">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="1c3f5-116">See also</span></span>

[<span data-ttu-id="1c3f5-117">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="1c3f5-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="1c3f5-118">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c3f5-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]