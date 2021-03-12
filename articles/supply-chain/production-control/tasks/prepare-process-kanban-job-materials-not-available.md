---
title: จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบไม่พร้อมใช้งานสำหรับเซลล์ทำงาน
description: 'ขั้นตอนนี้มุ่งเน้นการจัดเตรียมกระบวนการงานคัมบังเมื่อวัสดุและส่วนประกอบบางรายการไม่พร้อมใช้งานสำหรับเซลล์ทำงาน ดังนั้นจึงจำเป็นต้องเบิกวัสดุจากคลังสินค้า '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df0396a1d00e61ad82e52fc07779e239cd811ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994103"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="65637-103">จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบไม่พร้อมใช้งานสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="65637-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65637-104">ขั้นตอนนี้มุ่งเน้นการจัดเตรียมกระบวนการงานคัมบังเมื่อวัสดุและส่วนประกอบบางรายการไม่พร้อมใช้งานสำหรับเซลล์ทำงาน ดังนั้นจึงจำเป็นต้องเบิกวัสดุจากคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="65637-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="65637-105">ขั้นตอน "การจัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งาน" เป็นข้อกำหนดเบื้องต้นสำหรับการสร้างขั้นตอนนี้ </span><span class="sxs-lookup"><span data-stu-id="65637-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="65637-106">กระบวนงานนี้มีไว้สำหรับพนักงานควบคุมเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="65637-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="65637-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="65637-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="65637-108">ไปที่การควบคุมการผลิต > คัมบัง > บอร์ดคัมบังสำหรับงานกระบวนการ </span><span class="sxs-lookup"><span data-stu-id="65637-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="65637-109">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="65637-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="65637-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="65637-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="65637-111">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="65637-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="65637-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="65637-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="65637-113">เลือกคัมบัง 000356</span><span class="sxs-lookup"><span data-stu-id="65637-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="65637-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="65637-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="65637-115">ในรายการ ยกเลิกการเลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="65637-115">In the list, deselect row 4.</span></span> <span data-ttu-id="65637-116">หรือเลือกแถว 4 ถ้าคุณยังไม่เสร็จงาน "การเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="65637-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="65637-117">สลับการขยายของส่วนรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="65637-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="65637-118">ไอคอนไม่พบรายการอยู่ในสถานะการจัดหาวัสดุแสดงว่า ea 48 ของสินค้า P0002 ไม่มีสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="65637-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="65637-119">โอนย้ายวัสดุไปเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="65637-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="65637-120">สลับการขยายของส่วนงานการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="65637-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="65637-121">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์ หมายเลขสินค้าด้วยค่า 'P0002'</span><span class="sxs-lookup"><span data-stu-id="65637-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="65637-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="65637-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="65637-123">คลิก เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="65637-123">Click Start.</span></span>
    * <span data-ttu-id="65637-124">การโอนย้ายอยู่ระหว่างดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="65637-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="65637-125">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="65637-125">Click Complete.</span></span>
    * <span data-ttu-id="65637-126">สินค้า P0002 จะพร้อมใช้งานในรายการเบิกสินค้าสำหรับงานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="65637-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="65637-127">ซึ่งหมายความว่าเราสามารถจัดเตรียมคัมบังกับวัสดุที่จำเป็นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="65637-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="65637-128">คลิกจัดเตรียม </span><span class="sxs-lookup"><span data-stu-id="65637-128">Click Prepare.</span></span>
    * <span data-ttu-id="65637-129">โปรดสังเกตว่า ไอคอนในสถานะงานแสดงให้เห็นว่า ขณะนี้งานพร้อม</span><span class="sxs-lookup"><span data-stu-id="65637-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

