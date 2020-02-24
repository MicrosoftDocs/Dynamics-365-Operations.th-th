---
title: ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด
description: 'กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก '
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52798303ef5d96a44270f971703928d0c6c4c2c1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024176"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="e4d1c-103">ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="e4d1c-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e4d1c-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก </span><span class="sxs-lookup"><span data-stu-id="e4d1c-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="e4d1c-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="e4d1c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e4d1c-106">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="e4d1c-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="e4d1c-107">คลิกคำนวณใบแจ้งยอด </span><span class="sxs-lookup"><span data-stu-id="e4d1c-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="e4d1c-108">เลือกร้านค้าหรือโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า </span><span class="sxs-lookup"><span data-stu-id="e4d1c-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e4d1c-109">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="e4d1c-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="e4d1c-110">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="e4d1c-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="e4d1c-111">ภายใต้การประมวลผลชุดงาน เลือก 'ใช่' </span><span class="sxs-lookup"><span data-stu-id="e4d1c-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="e4d1c-112">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="e4d1c-112">Click Recurrence.</span></span>
6. <span data-ttu-id="e4d1c-113">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="e4d1c-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="e4d1c-114">ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="e4d1c-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="e4d1c-115">เลือกตัวเลือก ไม่มีวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="e4d1c-115">Select the No end date option.</span></span>
9. <span data-ttu-id="e4d1c-116">ในฟิลด์ PatternUnit ให้ป้อน 'วัน' </span><span class="sxs-lookup"><span data-stu-id="e4d1c-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="e4d1c-117">ในฟิลด์ Per ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="e4d1c-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="e4d1c-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e4d1c-118">Click OK.</span></span>
12. <span data-ttu-id="e4d1c-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e4d1c-119">Click OK.</span></span>

