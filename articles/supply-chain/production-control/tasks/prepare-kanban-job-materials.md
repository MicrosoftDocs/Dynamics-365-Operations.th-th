--- 
title: "จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งานสำหรับเซลล์ทำงาน"
description: "งานนี้มุ่งเน้นการเตรียมกระบวนการงานคัมบังเมื่อวัสดุทั้งหมดจะพร้อมใช้งานสำหรับเซลล์ทำงาน "
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62f3f71cc5e47f0fb027211a911e61673ca2e375
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="43dbd-103">จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งานสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="43dbd-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43dbd-104">งานนี้มุ่งเน้นการเตรียมกระบวนการงานคัมบังเมื่อวัสดุทั้งหมดจะพร้อมใช้งานสำหรับเซลล์ทำงาน </span><span class="sxs-lookup"><span data-stu-id="43dbd-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="43dbd-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="43dbd-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="43dbd-106">งานนี้มีไว้สำหรับผู้ปฏิบัติงานเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="43dbd-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="43dbd-107">ไปที่บอร์ดคัมบังสำหรับงานกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="43dbd-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="43dbd-108">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="43dbd-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="43dbd-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="43dbd-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="43dbd-110">เลือกเซลล์ทำงาน 1250 และคลิกตกลง </span><span class="sxs-lookup"><span data-stu-id="43dbd-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="43dbd-111">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="43dbd-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="43dbd-112">ในบริษัทสาธิตสะอาด คัมบัง 000329 ในแถว 4 คืองานแรกที่ยังไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="43dbd-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="43dbd-113">สลับการขยายของส่วนรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="43dbd-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="43dbd-114">ตรวจสอบว่าสถานะการจัดหาวัสดุพร้อมใช้งานสำหรับสินค้าทั้งหมดในรายการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="43dbd-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="43dbd-115">ถ้ามีงานหลายงานให้เลือก รายการเบิกสินค้าจะแสดงผลรวมของรายการทั้งหมดที่จำเป็นสำหรับงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="43dbd-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="43dbd-116">คลิกจัดเตรียม </span><span class="sxs-lookup"><span data-stu-id="43dbd-116">Click Prepare.</span></span>
    * <span data-ttu-id="43dbd-117">กระบวนการจัดเตรียมตอนนี้เสร็จสมบูรณ์แล้ว </span><span class="sxs-lookup"><span data-stu-id="43dbd-117">The preparation process is now completed.</span></span> <span data-ttu-id="43dbd-118">กล่องกาเครื่องหมายที่เลือกสำหรับแถวทั้งหมดในรายการเบิกสินค้าบ่งชี้ว่า มีการเบิกตามสถานะการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="43dbd-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  


