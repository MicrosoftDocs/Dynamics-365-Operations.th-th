---
title: ลบงานคัมบังออกจากกำหนดการ
description: ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438178"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="6f5b5-103">ลบงานคัมบังออกจากกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="6f5b5-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f5b5-104">ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน</span><span class="sxs-lookup"><span data-stu-id="6f5b5-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="6f5b5-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="6f5b5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6f5b5-106">ขั้นตอนนี้มีไว้สำหรับหัวหน้างานผลิตหรือนักวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="6f5b5-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="6f5b5-107">ค้นหางานคัมบังที่วางแผนไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6f5b5-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="6f5b5-108">ไปที่การควบคุมการผลิต > คัมบัง > การกำหนดเวลางานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="6f5b5-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="6f5b5-109">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="6f5b5-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6f5b5-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6f5b5-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6f5b5-111">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="6f5b5-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="6f5b5-112">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="6f5b5-112">Click Select.</span></span>
5. <span data-ttu-id="6f5b5-113">ในฟิลด์แสดงสถานะงาน เลือก 'จัดกำหนดการแล้ว' </span><span class="sxs-lookup"><span data-stu-id="6f5b5-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="6f5b5-114">ลบงานคัมบังที่วางแผนไว้แล้วออกจากกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="6f5b5-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="6f5b5-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6f5b5-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f5b5-116">เลือกงานที่มีสถานะวางแผนไว้แล้ว ตัวอย่างเช่น งานจากวันที่ 19 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="6f5b5-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="6f5b5-117">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="6f5b5-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="6f5b5-118">คลิก แปลงกลับสถานะงาน </span><span class="sxs-lookup"><span data-stu-id="6f5b5-118">Click Revert job status.</span></span>
4. <span data-ttu-id="6f5b5-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6f5b5-119">Click OK.</span></span>
    * <span data-ttu-id="6f5b5-120">นี่จะแปลงกลับสถานะของงานปัจจุบันจาก 'วางแผนไว้แล้ว' เป็น 'ไม่ได้วางแผน' และลบออกจากบอร์ดกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="6f5b5-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

