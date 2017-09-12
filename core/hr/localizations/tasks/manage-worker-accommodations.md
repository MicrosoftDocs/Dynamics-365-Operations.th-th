--- 
title: "จัดการที่พักของผู้ปฏิบัติงาน"
description: "ขั้นตอนนี้เป็นขั้นตอนที่นำไปสู่การตั้งค่าชนิดของสภาพแวดล้อมของที่พัก เช่นเก้าอี้ ergonomic หรือช่วงการพักที่เป็นเวลา "
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="9bee5-103">จัดการที่พักของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9bee5-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="9bee5-104">ขั้นตอนนี้เป็นขั้นตอนที่นำไปสู่การตั้งค่าชนิดของสภาพแวดล้อมของที่พัก เช่นเก้าอี้ ergonomic หรือช่วงการพักที่เป็นเวลา </span><span class="sxs-lookup"><span data-stu-id="9bee5-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="9bee5-105">และยังแสดงวิธีการกำหนดชนิดของที่พักเหล่านี้กับผู้ปฏิบัติงาน และมีทั้งขั้นตอนอนุมัติหรือปฏิเสธชนิดของที่พัก </span><span class="sxs-lookup"><span data-stu-id="9bee5-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="9bee5-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="9bee5-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="9bee5-107">ตั้งค่าที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-107">Setup accommodations</span></span>
1. <span data-ttu-id="9bee5-108">ไปที่ทรัพยากรบุคคล > การตั้งค่า > ชนิดของที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="9bee5-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9bee5-109">Click New.</span></span>
3. <span data-ttu-id="9bee5-110">ในฟิลด์ประเภทที่พัก ให้ป้อนชื่อสำหรับที่พัก </span><span class="sxs-lookup"><span data-stu-id="9bee5-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="9bee5-111">ตัวอย่าง: แป้นพิมพ์</span><span class="sxs-lookup"><span data-stu-id="9bee5-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="9bee5-112">ในฟิลด์คำอธิบาย ป้อนคำอธิบายสำหรับที่พัก </span><span class="sxs-lookup"><span data-stu-id="9bee5-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="9bee5-113">ตัวอย่าง: Ergonomic Keyboard</span><span class="sxs-lookup"><span data-stu-id="9bee5-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="9bee5-114">ในฟิลด์หมายเหตุ ป้อนข้อมูลใดๆ ที่ช่วยในการอธิบายที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="9bee5-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9bee5-115">Click Save.</span></span>
7. <span data-ttu-id="9bee5-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9bee5-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="9bee5-117">กำหนดที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-117">Assign accommodations</span></span>
1. <span data-ttu-id="9bee5-118">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="9bee5-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="9bee5-119">จากรายการ ให้เลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="9bee5-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="9bee5-120">คลิกชื่อของพนักงานเพื่อดูรายละเอียดเกี่ยวกับพนักงานที่ร้องขอที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="9bee5-121">ขยายแท็บด่วนข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="9bee5-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="9bee5-122">คลิกที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-122">Click Accommodations.</span></span>
6. <span data-ttu-id="9bee5-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9bee5-123">Click New.</span></span>
7. <span data-ttu-id="9bee5-124">ในฟิลด์ประเภทที่พัก ให้เลือกชื่อสำหรับที่พักที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="9bee5-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="9bee5-125">ตัวอย่าง: แป้นพิมพ์</span><span class="sxs-lookup"><span data-stu-id="9bee5-125">Example: Keyboard</span></span>
8. <span data-ttu-id="9bee5-126">ในฟิลด์ภารกิจงาน เลือกภารกิจเกี่ยวกับงานที่มีการร้องขอที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="9bee5-127">ในฟิลด์สถานะ ป้อนสถานะที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="9bee5-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="9bee5-128">ตัวอย่าง: สมเหตุสมผล</span><span class="sxs-lookup"><span data-stu-id="9bee5-128">Example: Reasonable</span></span>
    * <span data-ttu-id="9bee5-129">สถานะต่อไปนี้จะพร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="9bee5-129">The following statuses are available.</span></span> <span data-ttu-id="9bee5-130">จะมีการสร้างการบ่งชี้ที่พัก แต่ยังไม่ได้รับการตรวจทาน </span><span class="sxs-lookup"><span data-stu-id="9bee5-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="9bee5-131">จะมีการบ่งชี้ว่าเป็นที่พักที่เหมาะสม และจะได้รับ </span><span class="sxs-lookup"><span data-stu-id="9bee5-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="9bee5-132">การบ่งชี้อย่างหนักแน่นว่าที่พักที่ค่าโสหุ้ยไม่สมเหตุสมผลจากนายจ้างจะถูกปฏิเสธ </span><span class="sxs-lookup"><span data-stu-id="9bee5-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="9bee5-133">ในตัวอย่างนี้ คำขอจะถูกอนุมัติทันทีเนื่องจากการร้องขอที่พักเป็นระดับต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="9bee5-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="9bee5-134">ในฟิลด์ที่ยอมรับ ให้เลือกบุคคลที่ได้รับการยอมรับการร้องขอที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="9bee5-135">คลิก เลือก</span><span class="sxs-lookup"><span data-stu-id="9bee5-135">Click Select.</span></span>
12. <span data-ttu-id="9bee5-136">ในฟิลด์วันที่ได้รับการยอมรับ ป้อนวันที่และเวลาเมื่อมีการยอมรับคำขอที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="9bee5-137">ขยายส่วนของหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="9bee5-137">Expand the Note section.</span></span>
14. <span data-ttu-id="9bee5-138">ในฟิลด์การเงิน ป้อนข้อมูลใดๆ หรือต้นทุนทรัพยากรที่ช่วยในการอธิบายผลกระทบของที่พัก</span><span class="sxs-lookup"><span data-stu-id="9bee5-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="9bee5-139">ถ้ามีการปฏิเสธที่พัก สามารถใช้ฟิลด์การตอบเพื่อบ่งชี้ว่าเพราะเหตุใดการร้องขอจึงถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="9bee5-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="9bee5-140">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9bee5-140">Click Save.</span></span>


