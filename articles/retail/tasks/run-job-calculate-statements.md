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
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "365189"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="d1723-103">ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="d1723-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d1723-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อสร้างและคำนวณรายงานการเงินสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก </span><span class="sxs-lookup"><span data-stu-id="d1723-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="d1723-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="d1723-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d1723-106">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้าปลีก </span><span class="sxs-lookup"><span data-stu-id="d1723-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="d1723-107">คลิกคำนวณใบแจ้งยอด </span><span class="sxs-lookup"><span data-stu-id="d1723-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="d1723-108">เลือกร้านค้าหรือโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า </span><span class="sxs-lookup"><span data-stu-id="d1723-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d1723-109">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="d1723-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="d1723-110">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="d1723-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="d1723-111">ภายใต้การประมวลผลชุดงาน เลือก 'ใช่' </span><span class="sxs-lookup"><span data-stu-id="d1723-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="d1723-112">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1723-112">Click Recurrence.</span></span>
6. <span data-ttu-id="d1723-113">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="d1723-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="d1723-114">ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="d1723-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="d1723-115">เลือกตัวเลือก ไม่มีวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d1723-115">Select the No end date option.</span></span>
9. <span data-ttu-id="d1723-116">ในฟิลด์ PatternUnit ให้ป้อน 'วัน' </span><span class="sxs-lookup"><span data-stu-id="d1723-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="d1723-117">ในฟิลด์ Per ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d1723-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="d1723-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d1723-118">Click OK.</span></span>
12. <span data-ttu-id="d1723-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d1723-119">Click OK.</span></span>

