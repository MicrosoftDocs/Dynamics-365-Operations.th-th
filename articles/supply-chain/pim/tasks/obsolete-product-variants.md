---
title: ค้นหาผลิตภัณฑ์ย่อยที่ล้าสมัย
description: กระบวนงานนี้แสดงวิธีการค้นหาผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยซึ่งล้าสมัย และวิธีการเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่ล้าสมัย
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5efd1d471559d320102cd81e4be1ba8c1858f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438337"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="7d363-103">ค้นหาผลิตภัณฑ์ย่อยที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="7d363-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d363-104">กระบวนงานนี้แสดงวิธีการค้นหาผลิตภัณฑ์ที่นำออกใช้หรือผลิตภัณฑ์ย่อยซึ่งล้าสมัย และวิธีการเชื่อมโยงสถานะรอบการขายของผลิตภัณฑ์กับผลิตภัณฑ์ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="7d363-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="7d363-105">ข้อกำหนดเบื้องต้น: คุณต้องกำหนดสถานะวงจรชีวิตผลิตภัณฑ์อย่างน้อยหนึ่งรายการที่ไม่ได้ใช้งานสำหรับการวางแผน ก่อนที่คุณจะสามารถเล่นคู่มืองานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="7d363-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="7d363-106">รันการจำลอง</span><span class="sxs-lookup"><span data-stu-id="7d363-106">Run a simulation</span></span>
1. <span data-ttu-id="7d363-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > งานประจำงวด > เปลี่ยนสถานะรอบการขายสำหรับผลิตภัณฑ์ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="7d363-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="7d363-108">ในฟิลด์สถานะรอบการขายของผลิตภัณฑ์ใหม่ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7d363-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="7d363-109">เลือก ใช่ ในฟิลด์ รันการจำลองโดยไม่อัพเดตข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7d363-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="7d363-110">ในฟิลด์ แยกผลิตภัณฑ์ที่สร้างภายในจำนวนวันนี้ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7d363-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="7d363-111">ในฟิลด์ แยกผลิตภัณฑ์ที่ใช้ในธุรกรรม (ในจำนวนวัน) ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7d363-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="7d363-112">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="7d363-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7d363-113">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="7d363-113">Click Filter.</span></span>
8. <span data-ttu-id="7d363-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d363-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7d363-115">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="7d363-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="7d363-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7d363-116">Click OK.</span></span>
11. <span data-ttu-id="7d363-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7d363-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="7d363-118">แนะนำให้รันการจำลองในชุดงาน ถ้าคุณคาดว่าจะค้นหาผลิตภัณฑ์จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="7d363-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="7d363-119">นอกจากนี้ ให้มั่นใจว่า จะไม่มีการรันการจำลองในระหว่างเวลาการทำงานที่ใช้งานมากที่สุดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="7d363-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="7d363-120">ตรวจสอบผลการจำลอง</span><span class="sxs-lookup"><span data-stu-id="7d363-120">Review the simulation results</span></span>
1. <span data-ttu-id="7d363-121">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > สอบถามและรายงาน > ประวัติการบำรุงรักษาสถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7d363-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="7d363-122">ในหน้านี้ คุณสามารถตรวจทานผลลัพธ์ของแบบจำลอง และทำการประเมินจำนวนผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่จะเชื่อมโยงกับสถานะรอบการขายของผลิตภัณฑ์ใหม่ เมื่อรันการปรับปรุงโดยไม่มีการจำลอง</span><span class="sxs-lookup"><span data-stu-id="7d363-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="7d363-123">รันการปรับปรุงของสถานะรอบการขายของผลิตภัณฑ์สำหรับผลิตภัณฑ์ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="7d363-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="7d363-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7d363-124">Close the page.</span></span>
2. <span data-ttu-id="7d363-125">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > งานประจำงวด > เปลี่ยนสถานะรอบการขายสำหรับผลิตภัณฑ์ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="7d363-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="7d363-126">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="7d363-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="7d363-127">โปรดทราบว่า มีการบันทึกการเลือกสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="7d363-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="7d363-128">เลือก ไม่ ในฟิลด์ รันการจำลองโดยไม่อัพเดตข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7d363-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="7d363-129">ขยายการดำเนินงานในส่วนเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="7d363-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="7d363-130">โดยขึ้นอยู่กับจำนวนของผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่ได้รับผลกระทบ ลองรันงานนี้ในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="7d363-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="7d363-131">ตรวจสอบให้แน่ใจว่า คุณไม่ได้รันงานการอัพเดตขนาดใหญ่ระหว่างชั่วโมงการทำงานที่ใช้งานมากที่สุดในบริษัท</span><span class="sxs-lookup"><span data-stu-id="7d363-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="7d363-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7d363-132">Click OK.</span></span>
7. <span data-ttu-id="7d363-133">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > สอบถามและรายงาน > ประวัติการบำรุงรักษาสถานะรอบการขายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7d363-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="7d363-134">ตรวจทานผลิตภัณฑ์และผลิตภัณฑ์ย่อยที่นำออกใช้ที่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="7d363-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="7d363-135">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7d363-135">In the list, find and select the desired record.</span></span>

