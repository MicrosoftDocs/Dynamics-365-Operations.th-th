--- 
title: " ตั้งค่าคอนฟิกและดำเนินงานเพื่อการคำนวณใบแจ้งยอด"
description: "กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก "
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6d98adc919d50957b92a879b69517e0a826ea45f
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="6de01-103"> ตั้งค่าคอนฟิกและดำเนินงานเพื่อการคำนวณใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="6de01-103">Configure and run a job to calculate statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6de01-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก </span><span class="sxs-lookup"><span data-stu-id="6de01-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="6de01-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="6de01-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6de01-106">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้าปลีก </span><span class="sxs-lookup"><span data-stu-id="6de01-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="6de01-107">คลิกคำนวณใบแจ้งยอด </span><span class="sxs-lookup"><span data-stu-id="6de01-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="6de01-108">เลือกร้านค้าหรือโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า </span><span class="sxs-lookup"><span data-stu-id="6de01-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="6de01-109">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="6de01-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="6de01-110">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="6de01-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="6de01-111">ภายใต้การประมวลผลชุดงาน เลือก 'ใช่' </span><span class="sxs-lookup"><span data-stu-id="6de01-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="6de01-112">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="6de01-112">Click Recurrence.</span></span>
6. <span data-ttu-id="6de01-113">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="6de01-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="6de01-114">ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="6de01-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="6de01-115">เลือกตัวเลือก ไม่มีวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="6de01-115">Select the No end date option.</span></span>
9. <span data-ttu-id="6de01-116">ในฟิลด์ PatternUnit ให้ป้อน 'วัน' </span><span class="sxs-lookup"><span data-stu-id="6de01-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="6de01-117">ในฟิลด์ Per ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6de01-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="6de01-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6de01-118">Click OK.</span></span>
12. <span data-ttu-id="6de01-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6de01-119">Click OK.</span></span>


