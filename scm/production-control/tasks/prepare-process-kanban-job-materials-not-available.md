--- 
title: "จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบไม่พร้อมใช้งานสำหรับเซลล์ทำงาน"
description: "ขั้นตอนนี้มุ่งเน้นการจัดเตรียมกระบวนการงานคัมบังเมื่อวัสดุและส่วนประกอบบางรายการไม่พร้อมใช้งานสำหรับเซลล์ทำงาน ดังนั้นจึงจำเป็นต้องเบิกวัสดุจากคลังสินค้า "
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="7ce70-103">จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบไม่พร้อมใช้งานสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="7ce70-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ce70-104">ขั้นตอนนี้มุ่งเน้นการจัดเตรียมกระบวนการงานคัมบังเมื่อวัสดุและส่วนประกอบบางรายการไม่พร้อมใช้งานสำหรับเซลล์ทำงาน ดังนั้นจึงจำเป็นต้องเบิกวัสดุจากคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="7ce70-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="7ce70-105">ขั้นตอน "การจัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งาน" เป็นข้อกำหนดเบื้องต้นสำหรับการสร้างขั้นตอนนี้ </span><span class="sxs-lookup"><span data-stu-id="7ce70-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="7ce70-106">กระบวนงานนี้มีไว้สำหรับพนักงานควบคุมเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="7ce70-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="7ce70-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="7ce70-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7ce70-108">ไปที่การควบคุมการผลิต > คัมบัง > บอร์ดคัมบังสำหรับงานกระบวนการ </span><span class="sxs-lookup"><span data-stu-id="7ce70-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="7ce70-109">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="7ce70-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7ce70-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7ce70-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7ce70-111">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="7ce70-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="7ce70-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7ce70-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ce70-113">เลือกคัมบัง 000356</span><span class="sxs-lookup"><span data-stu-id="7ce70-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="7ce70-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7ce70-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ce70-115">ในรายการ ยกเลิกการเลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="7ce70-115">In the list, deselect row 4.</span></span> <span data-ttu-id="7ce70-116">หรือเลือกแถว 4 ถ้าคุณยังไม่เสร็จงาน "การเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="7ce70-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="7ce70-117">สลับการขยายของส่วนรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7ce70-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="7ce70-118">ไอคอนไม่พบรายการอยู่ในสถานะการจัดหาวัสดุแสดงว่า ea 48 ของสินค้า P0002 ไม่มีสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="7ce70-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="7ce70-119">โอนย้ายวัสดุไปเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="7ce70-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="7ce70-120">สลับการขยายของส่วนงานการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="7ce70-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="7ce70-121">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์ หมายเลขสินค้าด้วยค่า 'P0002'</span><span class="sxs-lookup"><span data-stu-id="7ce70-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="7ce70-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7ce70-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7ce70-123">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7ce70-123">Click Start.</span></span>
    * <span data-ttu-id="7ce70-124">การโอนย้ายอยู่ระหว่างดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7ce70-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="7ce70-125">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7ce70-125">Click Complete.</span></span>
    * <span data-ttu-id="7ce70-126">สินค้า P0002 จะพร้อมใช้งานในรายการเบิกสินค้าสำหรับงานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="7ce70-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="7ce70-127">ซึ่งหมายความว่าเราสามารถจัดเตรียมคัมบังกับวัสดุที่จำเป็นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7ce70-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="7ce70-128">คลิกจัดเตรียม </span><span class="sxs-lookup"><span data-stu-id="7ce70-128">Click Prepare.</span></span>
    * <span data-ttu-id="7ce70-129">โปรดสังเกตว่า ไอคอนในสถานะงานแสดงให้เห็นว่า ขณะนี้งานพร้อม</span><span class="sxs-lookup"><span data-stu-id="7ce70-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


