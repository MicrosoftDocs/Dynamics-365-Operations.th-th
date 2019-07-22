---
title: การสร้างชุดงาน
description: 'ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ '
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d211dcd7cb47df135d395d2a993429746aa35a85
ms.sourcegitcommit: 6ba4006fb6a67ddd4b1e54e3d62b9d1239b5e5a3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700852"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="c136a-103">การสร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="c136a-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c136a-104">ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="c136a-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="c136a-105">ชุดงานจะรันโดยใช้ข้อมูลประจำตัวของผู้ใช้ที่สร้างงานนั้น </span><span class="sxs-lookup"><span data-stu-id="c136a-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="c136a-106">ใช้กระบวนงานต่อไปนี้ในการสร้างชุดงาน </span><span class="sxs-lookup"><span data-stu-id="c136a-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="c136a-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c136a-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="c136a-108">สร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="c136a-108">Create the batch job</span></span>
1. <span data-ttu-id="c136a-109">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="c136a-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c136a-110">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c136a-110">Click **New**.</span></span>
3. <span data-ttu-id="c136a-111">ในฟิลด์ **คำอธิบายงาน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c136a-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="c136a-112">ในฟิลด์ **วันที่/เวลาเริ่มต้นตามกำหนดการ** ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c136a-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="c136a-113">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c136a-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="c136a-114">สร้างการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="c136a-114">Create a recurrence</span></span>
1. <span data-ttu-id="c136a-115">ในบานหน้าต่างการดำเนินการ คลิก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="c136a-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c136a-116">คลิก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="c136a-116">Click **Recurrence**.</span></span> <span data-ttu-id="c136a-117">ใช้ตัวเลือกเหล่านี้เพื่อป้อนช่วงและรูปแบบสำหรับการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="c136a-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="c136a-118">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c136a-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="c136a-119">เพิ่มข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c136a-119">Add alerts</span></span>
1. <span data-ttu-id="c136a-120">ในบานหน้าต่างการดำเนินการ คลิก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="c136a-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c136a-121">คลิก **ข้อความแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="c136a-121">Click **Alerts**.</span></span> <span data-ttu-id="c136a-122">ระบุว่าคุณต้องการได้รับข้อความแจ้งเตือนเมื่อชุดงานสิ้นสุด มีข้อผิดพลาด หรือถูกยกเลิกหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="c136a-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="c136a-123">จากนั้นระบุว่าคุณต้องการให้แสดงข้อความแจ้งเตือนเป็นข้อความป็อปอัพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c136a-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="c136a-124">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c136a-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="c136a-125">ปรับเปลี่ยนสถานะของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="c136a-125">Adjust batch job status</span></span>
1. <span data-ttu-id="c136a-126">ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="c136a-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c136a-127">เลือกชุดงานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c136a-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="c136a-128">ในบานหน้าต่างการดำเนินการ คลิก **ชุดงาน > ฟังก์ชัน > เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="c136a-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="c136a-129">เลือกสถานะที่เหมาะสม:</span><span class="sxs-lookup"><span data-stu-id="c136a-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="c136a-130">**ระงับ**: ตั้งค่าชุดงานเป็น **ระงับ** เพื่อให้มีการหักจากตัวจัดกำหนดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="c136a-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="c136a-131">เทียบเท่ากับ *การหยุด*</span><span class="sxs-lookup"><span data-stu-id="c136a-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="c136a-132">**กำลังรอ**: ตั้งค่าชุดงานเป็น **กำลังรอ** ดังนั้นจึงรอให้มีการเบิกสินค้าโดยตัวจัดกำหนดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="c136a-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="c136a-133">เทียบเท่ากับ *ไป*</span><span class="sxs-lookup"><span data-stu-id="c136a-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="c136a-134">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c136a-134">Click **OK**.</span></span>
