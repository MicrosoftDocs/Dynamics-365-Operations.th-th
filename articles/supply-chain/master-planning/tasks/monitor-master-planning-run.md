--- 
title: "ตรวจสอบการรันการวางแผนหลัก"
description: "ผู้วางแผนการผลิตต้องการดูว่า การรันการวางแผนหลักอยู่ระหว่างดำเนินการหรือไม่ "
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 550e2de01187d889ef968a4ff6828f93bb44a8a1
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="8116c-103">ตรวจสอบการรันการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="8116c-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8116c-104">ผู้วางแผนการผลิตต้องการดูว่า การรันการวางแผนหลักอยู่ระหว่างดำเนินการหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="8116c-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="8116c-105">ใช้บริษัทข้อมูลสาธิต USMF เพื่อทำให้กระบวนงานนี้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="8116c-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="8116c-106">ดำเนินการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="8116c-106">Run master planning</span></span>
1. <span data-ttu-id="8116c-107">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="8116c-107">Click Master planning.</span></span>
    * <span data-ttu-id="8116c-108">คุณจะพบสิ่งนี้บนแดชบอร์ดเริมต้น</span><span class="sxs-lookup"><span data-stu-id="8116c-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="8116c-109">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8116c-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8116c-110">ตัวอย่างเช่น StaticPlan</span><span class="sxs-lookup"><span data-stu-id="8116c-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="8116c-111">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="8116c-111">Click Run.</span></span>
4. <span data-ttu-id="8116c-112">เลือก ใช่ ในฟิลด์เวลาของการประมวลผลการติดตาม</span><span class="sxs-lookup"><span data-stu-id="8116c-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="8116c-113">ถ้าฟิลด์ถูกเลือกแล้ว ให้ข้ามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="8116c-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="8116c-114">ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="8116c-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="8116c-115">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="8116c-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="8116c-116">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="8116c-116">Click Filter.</span></span>
8. <span data-ttu-id="8116c-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8116c-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8116c-118">ทำเครื่องหมายแถว ที่ซึ่งฟิลด์ = หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="8116c-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="8116c-119">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8116c-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="8116c-120">ตัวอย่าง : T0001</span><span class="sxs-lookup"><span data-stu-id="8116c-120">Example: T0001</span></span>  
10. <span data-ttu-id="8116c-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8116c-121">Click OK.</span></span>
11. <span data-ttu-id="8116c-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8116c-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="8116c-123">ตรวจสอบการรันการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="8116c-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="8116c-124">คลิกประวัติ</span><span class="sxs-lookup"><span data-stu-id="8116c-124">Click History.</span></span>
2. <span data-ttu-id="8116c-125">คลิกการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8116c-125">Click Inquiries.</span></span>
3. <span data-ttu-id="8116c-126">คลิกระยะเวลาของงานกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="8116c-126">Click Process task duration.</span></span>
4. <span data-ttu-id="8116c-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8116c-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8116c-128">สำหรับสินค้าแต่ละรายการ คุณสามารถได้รับภาพรวมของระยะเวลาในการดำเนินขั้นตอนการวางแผนแต่ละขั้นให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8116c-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


