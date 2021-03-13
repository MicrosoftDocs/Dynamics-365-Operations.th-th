---
title: ความถี่ในการคัดกรองที่สร้างจาก
description: หัวข้อนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources
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
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126157"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="45242-103">ความถี่ในการคัดกรองที่สร้างจาก</span><span class="sxs-lookup"><span data-stu-id="45242-103">Screening frequency generate from</span></span>

<span data-ttu-id="45242-104">หัวข้อนี้อธิบายความถี่ของคัดกรองที่สร้างจากชุดตัวเลือกสำหรับ Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="45242-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="45242-105">ชื่อทางกายภาพ: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="45242-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="45242-106">การกําหนดตัวเลขนี้จะให้ชุดตัวเลือกของค่าในการกําหนดวันที่เริ่มต้นของการคํานวณเพื่อคัดกรองที่ต้องการครั้งต่อไป</span><span class="sxs-lookup"><span data-stu-id="45242-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="45242-107">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="45242-107">Value</span></span> | <span data-ttu-id="45242-108">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="45242-108">Label</span></span> | <span data-ttu-id="45242-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="45242-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="45242-110">200000000 ไม่ได้เลือก</span><span class="sxs-lookup"><span data-stu-id="45242-110">200000000 Not selected</span></span> | <span data-ttu-id="45242-111">ไม่ได้เลือกค่า</span><span class="sxs-lookup"><span data-stu-id="45242-111">No value has been selected.</span></span> |
| <span data-ttu-id="45242-112">200000001 วันที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="45242-112">200000001 Date completed</span></span> | <span data-ttu-id="45242-113">การคํานวณจะเสร็จสิ้นจากวันที่ที่คัดกรองครั้งล่าสุดเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="45242-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="45242-114">200000002 ต้องระบุวันที่</span><span class="sxs-lookup"><span data-stu-id="45242-114">200000002 Date required</span></span> | <span data-ttu-id="45242-115">การคํานวณจะเสร็จสิ้นจากวันที่ที่คัดกรองครั้งล่าสุดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="45242-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="45242-116">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="45242-116">See also</span></span>

[<span data-ttu-id="45242-117">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="45242-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="45242-118">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="45242-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
