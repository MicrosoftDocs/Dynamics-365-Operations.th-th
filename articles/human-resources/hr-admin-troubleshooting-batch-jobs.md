---
title: ปรับปรุงประสิทธิภาพโดยการจัดกำหนดการชุดงานหลังจากหลายชั่วโมง
description: หัวข้อนี้จะอธิบายถึงวิธีการแก้ไขปัญหาประสิทธิภาพการทำงานบางอย่างกับ Microsoft Dynamics 365 Human Resources โดยการจัดกำหนดการชุดงานที่รันเป็นเวลานานหลังจากหลายชั่วโมง
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 452a87cf5ba6c1ac73636584d75b2ec2ac555e02
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527776"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="4f005-103">ปรับปรุงประสิทธิภาพโดยการจัดกำหนดการชุดงานหลังจากหลายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4f005-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="4f005-104">ออก</span><span class="sxs-lookup"><span data-stu-id="4f005-104">Issue</span></span>

<span data-ttu-id="4f005-105">Microsoft Dynamics 365 Human Resources สามารถประสบปัญหาประสิทธิภาพการทำงานได้ ถ้ารันชุดงานที่รันเป็นเวลานานในระหว่างชั่วโมงการทำงานทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4f005-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="4f005-106">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="4f005-106">Resolution</span></span>

<span data-ttu-id="4f005-107">จัดกำหนดการชุดงานต่อไปนี้ในช่วงเวลาที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4f005-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="4f005-108">นอกจากนี้เราขอแนะนำให้ตรวจสอบความถี่ของชุดงานที่รันบ่อย</span><span class="sxs-lookup"><span data-stu-id="4f005-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="4f005-109">ถ้าเป็นไปได้ให้ลดการเกิดซ้ำของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4f005-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="4f005-110">ในหลายกรณีที่ความถี่เริ่มต้นไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="4f005-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="4f005-111">ชุดงานต่อไปนี้ควรรันในเวลากลางคืนหรือหลังจากหลายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="4f005-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="4f005-112">ตรวจสอบให้แน่ใจว่าได้ตรวจสอบโซนเวลาสำหรับชุดงานที่เกิดซ้ำเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4f005-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="4f005-113">ชุดงานบางชุดอาจใช้เวลามาตรฐานแปซิฟิก (PST)</span><span class="sxs-lookup"><span data-stu-id="4f005-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="4f005-114">ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4f005-114">Batch job</span></span> | <span data-ttu-id="4f005-115">การเกิดซ้ำเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4f005-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="4f005-116">การล้างประวัติชุดงาน</span><span class="sxs-lookup"><span data-stu-id="4f005-116">Batch job history cleanup</span></span> | <span data-ttu-id="4f005-117">1 ครั้งต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="4f005-117">1 time per month</span></span> |
| <span data-ttu-id="4f005-118">ส่งออกการล้างข้อมูลการแบ่งระยะ</span><span class="sxs-lookup"><span data-stu-id="4f005-118">Export staging cleanup</span></span> | <span data-ttu-id="4f005-119">1 ครั้งต่อวัน</span><span class="sxs-lookup"><span data-stu-id="4f005-119">1 time per day</span></span> |
| <span data-ttu-id="4f005-120">การซิงค์คำขอที่หายไปของการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f005-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="4f005-121">1 ครั้งต่อวัน</span><span class="sxs-lookup"><span data-stu-id="4f005-121">1 time per day</span></span> |
| <span data-ttu-id="4f005-122">งานระบบการบีบอัดฐานข้อมูลที่จำเป็นต้องรันเป็นประจำในช่วงเวลาที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4f005-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="4f005-123">1 ครั้งต่อวัน</span><span class="sxs-lookup"><span data-stu-id="4f005-123">1 time per day</span></span> |
| <span data-ttu-id="4f005-124">งานระบบการสร้างดัชนีฐานข้อมูลที่จำเป็นต้องรันเป็นประจำในช่วงเวลาที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4f005-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="4f005-125">1 ครั้งต่อวัน</span><span class="sxs-lookup"><span data-stu-id="4f005-125">1 time per day</span></span> |

1. <span data-ttu-id="4f005-126">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="4f005-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="4f005-127">ในแถบ **ค้นหา** ให้ค้นหาชุดงานด้านบนอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4f005-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="4f005-128">เลือก **รันในพื้นหลัง** แล้วจากนั้นเลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="4f005-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![ตั้งค่าการเกิดซ้ำ](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="4f005-130">ภายใต้ **กำหนดการเกิดซ้ำ** ให้กำหนด **วันที่เริ่มต้น** และ **เวลาเริ่มต้น** ที่จะเกิดขึ้นในระหว่างช่วงเวลาที่ไม่ทำงานหรือวันหยุดสุดสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="4f005-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="4f005-131">เลือก **ไม่มีวันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="4f005-131">Select **No end date**.</span></span> 

   ![กำหนดวันที่และเวลาเริ่มต้นของการเกิดซ้ำ](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="4f005-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f005-133">Select **OK**.</span></span>

6. <span data-ttu-id="4f005-134">หากจำเป็น ให้เปลี่ยนพารามิเตอร์อื่นๆ ภายใต้ **รันในพื้นหลัง** แล้วจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f005-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f005-135">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4f005-135">Additional resources</span></span>

[<span data-ttu-id="4f005-136">ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4f005-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
