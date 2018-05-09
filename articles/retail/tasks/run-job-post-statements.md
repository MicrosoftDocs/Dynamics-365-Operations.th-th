--- 
title: " ตั้งค่าคอนฟิกและดำเนินงานเพื่อลงรายการบัญชีใบแจ้งยอด"
description: "กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบแจ้งยอดสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก "
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0e8a92894ea8d7bdc0880ceb6517655b63988b6a
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="40107-103"> ตั้งค่าคอนฟิกและดำเนินงานเพื่อลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="40107-103">Configure and run a job to post statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="40107-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบแจ้งยอดสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก </span><span class="sxs-lookup"><span data-stu-id="40107-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="40107-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="40107-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="40107-106">ไปที่ พื้นที่ทำงานทั้งหมด > ..</span><span class="sxs-lookup"><span data-stu-id="40107-106">Go to All workspaces > ..</span></span> <span data-ttu-id="40107-107">> การเงินของร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="40107-107">> Retail store financials.</span></span>
2. <span data-ttu-id="40107-108">คลิกลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="40107-108">Click Post statements.</span></span>
    * <span data-ttu-id="40107-109">เลือกลำดับชั้นขององค์กร จากนั้นเลือกร้านค้าแต่ละรายหรือโหนดในแผนภูมิโหนดองค์กร เลือกโหนด </span><span class="sxs-lookup"><span data-stu-id="40107-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="40107-110">ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า</span><span class="sxs-lookup"><span data-stu-id="40107-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="40107-111">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="40107-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="40107-112">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="40107-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="40107-113">เลือกหรือไม่เลือกกล่องกาเครื่องหมายการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="40107-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="40107-114">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="40107-114">Click Recurrence.</span></span>
6. <span data-ttu-id="40107-115">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="40107-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="40107-116">ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา </span><span class="sxs-lookup"><span data-stu-id="40107-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="40107-117">เลือกว่าคุณต้องการหยุดการเกิดซ้ำหลังจากการรันได้จำนวนหนึ่ง, ณ วันหนึ่ง, หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="40107-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="40107-118">จากนั้นเลือกตัวเลือกต่างๆ เพื่อกำหนดความถี่ที่คุณต้องการรันงาน</span><span class="sxs-lookup"><span data-stu-id="40107-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="40107-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="40107-119">Click OK.</span></span>
9. <span data-ttu-id="40107-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="40107-120">Click OK.</span></span>


