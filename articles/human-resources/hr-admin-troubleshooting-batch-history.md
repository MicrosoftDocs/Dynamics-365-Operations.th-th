---
title: ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ
description: บืความนี้จะอธิบายถึงวิธีการแก้ไขปัญหาประสิทธิภาพการทำงานบางอย่างกับ Microsoft Dynamics 365 Human Resources โดยการล้างข้อมูลประวัติชุดงาน
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420710"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="216c8-103">ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="216c8-103">Optimize performance with auto cleanup tasks</span></span>

<span data-ttu-id="216c8-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="216c8-104">**Issue**</span></span>

<span data-ttu-id="216c8-105">Microsoft Dynamics 365 Human Resources สามารถประสบปัญหาประสิทธิภาพการทำงานได้ ถ้าประวัติชุดงานขยายใหญ่เกินไป</span><span class="sxs-lookup"><span data-stu-id="216c8-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="216c8-106">**สาเหตุ**</span><span class="sxs-lookup"><span data-stu-id="216c8-106">**Cause**</span></span>

<span data-ttu-id="216c8-107">ชุดงานที่รันบ่อยสามารถนำไปสู่การเจริญเติบโตที่ไม่ยั่งยืนของประวัติชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="216c8-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="216c8-108">นี่อาจทำให้เกิดปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="216c8-108">This can cause performance issues.</span></span> 

<span data-ttu-id="216c8-109">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="216c8-109">**Resolution**</span></span>

<span data-ttu-id="216c8-110">จัดกำหนดการงานแบบอัตโนมัติเพื่อล้างข้อมูลประวัติชุดงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="216c8-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="216c8-111">เราขอแนะนำให้ตั้งค่างานสำหรับการรันรายสัปดาห์ แต่คุณอาจต้องรันการล้างข้อมูลบ่อยขึ้นหรือน้อยลง ทั้งนี้ขึ้นอยู่กับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="216c8-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="216c8-112">กระบวนงานต่อไปนี้มีการตั้งค่าที่แนะนำของเรา แต่คุณสามารถเปลี่ยนแปลงข้อมูลเหล่านี้ตามความต้องการของคุณได้</span><span class="sxs-lookup"><span data-stu-id="216c8-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="216c8-113">ในทรัพยากรบุคคล เลือก **การจัดการระบบ**</span><span class="sxs-lookup"><span data-stu-id="216c8-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="216c8-114">ในแถบ **ค้นหา** ให้ป้อน **การล้างข้อมูลประวัติชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="216c8-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![ค้นหาการล้างข้อมูลประวัติชุดงาน](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="216c8-116">ใน **ขีดจำกัดเวลาการเก็บประวัติ (วัน)** ให้ป้อน **30**</span><span class="sxs-lookup"><span data-stu-id="216c8-116">In **History limit (days)**, enter **30**.</span></span>

   ![ตั้งค่าขีดจำกัดเวลาการเก็บประวัติเป็น 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="216c8-118">เลือก **รันในพื้นหลัง** แล้วจากนั้น เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="216c8-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![ตั้งค่าการเกิดซ้ำ](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="216c8-120">ภายใต้ **กำหนดการเกิดซ้ำ** ให้กำหนด **วันที่เริ่มต้น** และ **เวลาเริ่มต้น** ที่จะเกิดขึ้นในระหว่างช่วงเวลาที่ไม่ทำงานหรือวันหยุดสุดสัปดาห์ และจากนั้น เลือก **ไม่มีวันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="216c8-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![กำหนดวันที่และเวลาเริ่มต้นของการเกิดซ้ำ](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="216c8-122">ภายใต้ **รูปแบบการเกิดซ้ำ** เลือก **วัน** และตั้งค่า **ทำซ้ำหลังจากช่วงเวลาที่ระบุ** เป็น **7**</span><span class="sxs-lookup"><span data-stu-id="216c8-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![ตั้งค่าการล้างข้อมูลให้ทำซ้ำรายสัปดาห์](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="216c8-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="216c8-124">Select **OK**.</span></span>

8. <span data-ttu-id="216c8-125">เปลี่ยนพารามิเตอร์อื่นๆ ภายใต้ **รันในพื้นหลัง** ตามที่จำเป็น แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="216c8-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

