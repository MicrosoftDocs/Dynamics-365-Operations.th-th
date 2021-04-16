---
title: ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด
description: 'กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบแจ้งยอดสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก '
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52baa707c36f3468263782dc8ec735e44af88e38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804244"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="99a7c-103">ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="99a7c-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99a7c-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบแจ้งยอดสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก </span><span class="sxs-lookup"><span data-stu-id="99a7c-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="99a7c-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="99a7c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="99a7c-106">ไปที่ พื้นที่ทำงานทั้งหมด > ..</span><span class="sxs-lookup"><span data-stu-id="99a7c-106">Go to All workspaces > ..</span></span> <span data-ttu-id="99a7c-107">> การเงินของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="99a7c-107">> Store financials.</span></span>
2. <span data-ttu-id="99a7c-108">คลิกลงรายการบัญชีใบแจ้งยอดในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="99a7c-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="99a7c-109">เลือกลำดับชั้นขององค์กร จากนั้นเลือกร้านค้าแต่ละรายหรือโหนดในแผนภูมิโหนดองค์กร เลือกโหนด </span><span class="sxs-lookup"><span data-stu-id="99a7c-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="99a7c-110">ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า</span><span class="sxs-lookup"><span data-stu-id="99a7c-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="99a7c-111">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="99a7c-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="99a7c-112">คลิกที่แท็บดำเนินการในเบื้องหลัง ![ดำเนินการในเบื้องหลังรันในเบื้องหลัง](../dev-itpro/media/runbackground.png "รันในแบบเบื้องหลัง")</span><span class="sxs-lookup"><span data-stu-id="99a7c-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="99a7c-113">เลือกหรือไม่เลือกกล่องกาเครื่องหมายการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="99a7c-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="99a7c-114">![การประมวลผลชุดงาน](../dev-itpro/media/batchprocessing.png "ชุดงานการประมวณผล & การเกิดซ้ำ ")</span><span class="sxs-lookup"><span data-stu-id="99a7c-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="99a7c-115">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="99a7c-115">Click Recurrence.</span></span>
6. <span data-ttu-id="99a7c-116">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="99a7c-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="99a7c-117">ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="99a7c-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="99a7c-118">เลือกว่าคุณต้องการหยุดการเกิดซ้ำหลังจากการรันได้จำนวนหนึ่ง, ณ วันหนึ่ง, หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="99a7c-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="99a7c-119">จากนั้นเลือกตัวเลือกต่างๆ เพื่อกำหนดความถี่ที่คุณต้องการรันงาน</span><span class="sxs-lookup"><span data-stu-id="99a7c-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="99a7c-120">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="99a7c-120">Click OK.</span></span>
9. <span data-ttu-id="99a7c-121">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="99a7c-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]