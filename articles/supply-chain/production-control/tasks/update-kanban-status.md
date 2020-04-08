---
title: การอัพเดตสถานะคัมบัง
description: 'เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48dd5c3a878efb7413f461e76fde086030015b60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146686"
---
# <a name="update-kanban-status"></a><span data-ttu-id="8fcb4-103">การอัพเดตสถานะคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8fcb4-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fcb4-104">เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง </span><span class="sxs-lookup"><span data-stu-id="8fcb4-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="8fcb4-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8fcb4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8fcb4-106">กระบวนงานนี้มีไว้สำหรับผู้ดูแลร้าน</span><span class="sxs-lookup"><span data-stu-id="8fcb4-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="8fcb4-107">ค้นหาคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8fcb4-107">Find the kanban.</span></span>
1. <span data-ttu-id="8fcb4-108">ไปที่การควบคุมการผลิต > คัมบัง > คัมบัง</span><span class="sxs-lookup"><span data-stu-id="8fcb4-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="8fcb4-109">เปิดตัวกรองคอลัมน์สถานะหน่วยจัดการวัสดุ</span><span class="sxs-lookup"><span data-stu-id="8fcb4-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="8fcb4-110">คลิกล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8fcb4-110">Click Clear.</span></span>
    * <span data-ttu-id="8fcb4-111">นี่จะรีเซ็ตตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8fcb4-111">This resets the filters.</span></span>  
4. <span data-ttu-id="8fcb4-112">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="8fcb4-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8fcb4-113">ตัวอย่างเช่น กรองข้อมูลในฟิลด์หมายเลขบัตรด้วยค่า '000149'</span><span class="sxs-lookup"><span data-stu-id="8fcb4-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="8fcb4-114">เปลี่ยนสถานะว่างเปล่า เป็นสถานะได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="8fcb4-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="8fcb4-115">คลิกกลับหน่วยจัดการวัสดุที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="8fcb4-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="8fcb4-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8fcb4-116">Click OK.</span></span>
    * <span data-ttu-id="8fcb4-117">สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="8fcb4-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="8fcb4-118">เปลี่ยนสถานะได้รับแล้ว เป็นสถานะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="8fcb4-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="8fcb4-119">คลิกคัมบังที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="8fcb4-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="8fcb4-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8fcb4-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8fcb4-121">สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ว่างแล้ว</span><span class="sxs-lookup"><span data-stu-id="8fcb4-121">Notice that the Handling unit status is Emptied.</span></span>  

