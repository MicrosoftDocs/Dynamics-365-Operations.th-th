---
title: ลบงานคัมบังออกจากกำหนดการ
description: ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "352079"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="2cdc9-103">ลบงานคัมบังออกจากกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="2cdc9-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cdc9-104">ขั้นตอนนี้มุ่งเน้นไปที่การลบกระบวนงานคัมบังที่วางแผนไว้แล้วจากตารางกำหนดการโดยการแปลงกลับสถานะของงานไปเป็นไม่ได้วางแผน</span><span class="sxs-lookup"><span data-stu-id="2cdc9-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="2cdc9-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="2cdc9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2cdc9-106">ขั้นตอนนี้มีไว้สำหรับหัวหน้างานผลิตหรือนักวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="2cdc9-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="2cdc9-107">ค้นหางานคัมบังที่วางแผนไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="2cdc9-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="2cdc9-108">ไปที่การควบคุมการผลิต > คัมบัง > การกำหนดเวลางานคัมบัง </span><span class="sxs-lookup"><span data-stu-id="2cdc9-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="2cdc9-109">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="2cdc9-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2cdc9-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2cdc9-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2cdc9-111">เลือกเซลล์ทำงาน 1250</span><span class="sxs-lookup"><span data-stu-id="2cdc9-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="2cdc9-112">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="2cdc9-112">Click Select.</span></span>
5. <span data-ttu-id="2cdc9-113">ในฟิลด์แสดงสถานะงาน เลือก 'จัดกำหนดการแล้ว' </span><span class="sxs-lookup"><span data-stu-id="2cdc9-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="2cdc9-114">ลบงานคัมบังที่วางแผนไว้แล้วออกจากกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="2cdc9-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="2cdc9-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2cdc9-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2cdc9-116">เลือกงานที่มีสถานะวางแผนไว้แล้ว ตัวอย่างเช่น งานจากวันที่ 19 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="2cdc9-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="2cdc9-117">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="2cdc9-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="2cdc9-118">คลิก แปลงกลับสถานะงาน </span><span class="sxs-lookup"><span data-stu-id="2cdc9-118">Click Revert job status.</span></span>
4. <span data-ttu-id="2cdc9-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2cdc9-119">Click OK.</span></span>
    * <span data-ttu-id="2cdc9-120">นี่จะแปลงกลับสถานะของงานปัจจุบันจาก 'วางแผนไว้แล้ว' เป็น 'ไม่ได้วางแผน' และลบออกจากบอร์ดกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="2cdc9-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

