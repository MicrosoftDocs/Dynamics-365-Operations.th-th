--- 
title: "การอัพเดตสถานะคัมบัง"
description: "เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง "
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 413f53a9ecc58439d4094d141bab4b510725b76e
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="update-kanban-status"></a><span data-ttu-id="dfb76-103">การอัพเดตสถานะคัมบัง</span><span class="sxs-lookup"><span data-stu-id="dfb76-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfb76-104">เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง </span><span class="sxs-lookup"><span data-stu-id="dfb76-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="dfb76-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="dfb76-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dfb76-106">กระบวนงานนี้มีไว้สำหรับผู้ดูแลร้าน</span><span class="sxs-lookup"><span data-stu-id="dfb76-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="dfb76-107">ค้นหาคัมบัง</span><span class="sxs-lookup"><span data-stu-id="dfb76-107">Find the kanban.</span></span>
1. <span data-ttu-id="dfb76-108">ไปที่การควบคุมการผลิต > คัมบัง > คัมบัง</span><span class="sxs-lookup"><span data-stu-id="dfb76-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="dfb76-109">เปิดตัวกรองคอลัมน์สถานะหน่วยจัดการวัสดุ</span><span class="sxs-lookup"><span data-stu-id="dfb76-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="dfb76-110">คลิกล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dfb76-110">Click Clear.</span></span>
    * <span data-ttu-id="dfb76-111">นี่จะรีเซ็ตตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="dfb76-111">This resets the filters.</span></span>  
4. <span data-ttu-id="dfb76-112">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="dfb76-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dfb76-113">ตัวอย่างเช่น กรองข้อมูลในฟิลด์หมายเลขบัตรด้วยค่า '000149'</span><span class="sxs-lookup"><span data-stu-id="dfb76-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="dfb76-114">เปลี่ยนสถานะว่างเปล่า เป็นสถานะได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="dfb76-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="dfb76-115">คลิกกลับหน่วยจัดการวัสดุที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="dfb76-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="dfb76-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dfb76-116">Click OK.</span></span>
    * <span data-ttu-id="dfb76-117">สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="dfb76-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="dfb76-118">เปลี่ยนสถานะได้รับแล้ว เป็นสถานะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="dfb76-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="dfb76-119">คลิกคัมบังที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="dfb76-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="dfb76-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dfb76-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dfb76-121">สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ว่างแล้ว</span><span class="sxs-lookup"><span data-stu-id="dfb76-121">Notice that the Handling unit status is Emptied.</span></span>  


