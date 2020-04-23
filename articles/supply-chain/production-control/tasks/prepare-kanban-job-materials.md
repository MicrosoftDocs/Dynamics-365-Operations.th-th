---
title: จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งานสำหรับเซลล์ทำงาน
description: 'งานนี้มุ่งเน้นการเตรียมกระบวนการงานคัมบังเมื่อวัสดุทั้งหมดจะพร้อมใช้งานสำหรับเซลล์ทำงาน '
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd6d5add4d11c917a705e88d10b589e2c43fab89
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206944"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="0a6a6-103">จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งานสำหรับเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="0a6a6-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a6a6-104">งานนี้มุ่งเน้นการเตรียมกระบวนการงานคัมบังเมื่อวัสดุทั้งหมดจะพร้อมใช้งานสำหรับเซลล์ทำงาน </span><span class="sxs-lookup"><span data-stu-id="0a6a6-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="0a6a6-105">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="0a6a6-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="0a6a6-106">งานนี้มีไว้สำหรับผู้ปฏิบัติงานเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="0a6a6-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="0a6a6-107">ไปที่บอร์ดคัมบังสำหรับงานกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="0a6a6-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="0a6a6-108">ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="0a6a6-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0a6a6-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0a6a6-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0a6a6-110">เลือกเซลล์ทำงาน 1250 และคลิกตกลง </span><span class="sxs-lookup"><span data-stu-id="0a6a6-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="0a6a6-111">ในรายการ ให้เลือกแถว 4</span><span class="sxs-lookup"><span data-stu-id="0a6a6-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="0a6a6-112">ในบริษัทสาธิตสะอาด คัมบัง 000329 ในแถว 4 คืองานแรกที่ยังไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0a6a6-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="0a6a6-113">สลับการขยายของส่วนรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0a6a6-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="0a6a6-114">ตรวจสอบว่าสถานะการจัดหาวัสดุพร้อมใช้งานสำหรับสินค้าทั้งหมดในรายการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="0a6a6-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="0a6a6-115">ถ้ามีงานหลายงานให้เลือก รายการเบิกสินค้าจะแสดงผลรวมของรายการทั้งหมดที่จำเป็นสำหรับงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0a6a6-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="0a6a6-116">คลิกจัดเตรียม </span><span class="sxs-lookup"><span data-stu-id="0a6a6-116">Click Prepare.</span></span>
    * <span data-ttu-id="0a6a6-117">กระบวนการจัดเตรียมตอนนี้เสร็จสมบูรณ์แล้ว </span><span class="sxs-lookup"><span data-stu-id="0a6a6-117">The preparation process is now completed.</span></span> <span data-ttu-id="0a6a6-118">กล่องกาเครื่องหมายที่เลือกสำหรับแถวทั้งหมดในรายการเบิกสินค้าบ่งชี้ว่า มีการเบิกตามสถานะการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="0a6a6-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

