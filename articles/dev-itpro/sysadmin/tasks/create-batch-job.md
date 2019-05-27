---
title: การสร้างชุดงาน
description: 'ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ '
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562892"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="38cd3-103">การสร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="38cd3-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38cd3-104">ชุดงานคือกลุ่มของงานที่ส่งไปยังอินสแตนซ์เซิร์ฟเวอร์แอพลิเคชันออบเจ็กต์ (AOS) สำหรับการประมวลผลโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="38cd3-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="38cd3-105">ชุดงานจะรันโดยใช้ข้อมูลประจำตัวของผู้ใช้ที่สร้างงานนั้น </span><span class="sxs-lookup"><span data-stu-id="38cd3-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="38cd3-106">ใช้กระบวนงานต่อไปนี้ในการสร้างชุดงาน </span><span class="sxs-lookup"><span data-stu-id="38cd3-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="38cd3-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="38cd3-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="38cd3-108">สร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="38cd3-108">Create the batch job</span></span>
1. <span data-ttu-id="38cd3-109">ไปที่ การดูแลระบบ > การสอบถาม > ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="38cd3-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="38cd3-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="38cd3-110">Click New.</span></span>
3. <span data-ttu-id="38cd3-111">ในฟิลด์คำอธิบายงาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="38cd3-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="38cd3-112">ในฟิลด์วันที่/เวลาเริ่มต้นตามกำหนดการ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="38cd3-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="38cd3-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="38cd3-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="38cd3-114">สร้างการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="38cd3-114">Create a recurrence</span></span>
1. <span data-ttu-id="38cd3-115">ในบานหน้าต่างการดำเนินการ คลิกชุดงาน</span><span class="sxs-lookup"><span data-stu-id="38cd3-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="38cd3-116">การเกิดซ้ำ </span><span class="sxs-lookup"><span data-stu-id="38cd3-116">Click Recurrence.</span></span>
    * <span data-ttu-id="38cd3-117">ใช้ตัวเลือกเหล่านี้เพื่อป้อนช่วงและรูปแบบสำหรับการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="38cd3-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="38cd3-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="38cd3-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="38cd3-119">เพิ่มข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="38cd3-119">Add alerts</span></span>
1. <span data-ttu-id="38cd3-120">ในบานหน้าต่างการดำเนินการ คลิกชุดงาน</span><span class="sxs-lookup"><span data-stu-id="38cd3-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="38cd3-121">คลิกที่ข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="38cd3-121">Click Alerts.</span></span>
    * <span data-ttu-id="38cd3-122">ระบุว่าคุณต้องการได้รับข้อความแจ้งเตือนเมื่อชุดงานสิ้นสุด มีข้อผิดพลาด หรือถูกยกเลิกหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="38cd3-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="38cd3-123">จากนั้นระบุว่าคุณต้องการให้แสดงข้อความแจ้งเตือนเป็นข้อความป็อปอัพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="38cd3-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="38cd3-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="38cd3-124">Click OK.</span></span>

