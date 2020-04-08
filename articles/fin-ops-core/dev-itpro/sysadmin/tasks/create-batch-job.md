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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143684"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="adf04-103">การสร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="adf04-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="adf04-104">ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="adf04-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="adf04-105">ชุดงานจะรันโดยใช้ข้อมูลประจำตัวของผู้ใช้ที่สร้างงานนั้น </span><span class="sxs-lookup"><span data-stu-id="adf04-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="adf04-106">ใช้กระบวนงานต่อไปนี้ในการสร้างชุดงาน </span><span class="sxs-lookup"><span data-stu-id="adf04-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="adf04-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="adf04-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="adf04-108">สร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="adf04-108">Create the batch job</span></span>
1. <span data-ttu-id="adf04-109">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="adf04-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="adf04-110">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="adf04-110">Click **New**.</span></span>
3. <span data-ttu-id="adf04-111">ในฟิลด์ **คำอธิบายงาน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="adf04-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="adf04-112">ในฟิลด์ **วันที่/เวลาเริ่มต้นตามกำหนดการ** ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="adf04-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="adf04-113">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="adf04-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="adf04-114">สร้างการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="adf04-114">Create a recurrence</span></span>
1. <span data-ttu-id="adf04-115">ในบานหน้าต่างการดำเนินการ คลิก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="adf04-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="adf04-116">คลิก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="adf04-116">Click **Recurrence**.</span></span> <span data-ttu-id="adf04-117">ใช้ตัวเลือกเหล่านี้เพื่อป้อนช่วงและรูปแบบสำหรับการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="adf04-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="adf04-118">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="adf04-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="adf04-119">เพิ่มข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="adf04-119">Add alerts</span></span>
1. <span data-ttu-id="adf04-120">ในบานหน้าต่างการดำเนินการ คลิก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="adf04-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="adf04-121">คลิก **ข้อความแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="adf04-121">Click **Alerts**.</span></span> <span data-ttu-id="adf04-122">ระบุว่าคุณต้องการได้รับข้อความแจ้งเตือนเมื่อชุดงานสิ้นสุด มีข้อผิดพลาด หรือถูกยกเลิกหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="adf04-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="adf04-123">จากนั้นระบุว่าคุณต้องการให้แสดงข้อความแจ้งเตือนเป็นข้อความป็อปอัพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="adf04-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="adf04-124">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="adf04-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="adf04-125">ปรับเปลี่ยนสถานะของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="adf04-125">Adjust batch job status</span></span>
1. <span data-ttu-id="adf04-126">ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="adf04-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="adf04-127">เลือกชุดงานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="adf04-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="adf04-128">ในบานหน้าต่างการดำเนินการ คลิก **ชุดงาน > ฟังก์ชัน > เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="adf04-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="adf04-129">เลือกสถานะที่เหมาะสม:</span><span class="sxs-lookup"><span data-stu-id="adf04-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="adf04-130">**ระงับ**: ตั้งค่าชุดงานเป็น **ระงับ** เพื่อให้มีการหักจากตัวจัดกำหนดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="adf04-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="adf04-131">เทียบเท่ากับ *การหยุด*</span><span class="sxs-lookup"><span data-stu-id="adf04-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="adf04-132">**กำลังรอ**: ตั้งค่าชุดงานเป็น **กำลังรอ** ดังนั้นจึงรอให้มีการเบิกสินค้าโดยตัวจัดกำหนดการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="adf04-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="adf04-133">เทียบเท่ากับ *ไป*</span><span class="sxs-lookup"><span data-stu-id="adf04-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="adf04-134">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="adf04-134">Click **OK**.</span></span>
