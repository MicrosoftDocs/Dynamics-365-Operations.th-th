---
title: การอัพเดตสถานะคัมบัง
description: 'เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252833"
---
# <a name="update-kanban-status"></a><span data-ttu-id="34afc-103">การอัพเดตสถานะคัมบัง</span><span class="sxs-lookup"><span data-stu-id="34afc-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34afc-104">เมื่อคัมบังถูกทำให้ว่างโดยไม่ได้ตั้งใจหรือคัมบังที่ได้รับต้องถูกทำให้ว่าง คุณต้องอัพเดตสถานะคัมบัง </span><span class="sxs-lookup"><span data-stu-id="34afc-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="34afc-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="34afc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="34afc-106">กระบวนงานนี้มีไว้สำหรับผู้ดูแลร้าน</span><span class="sxs-lookup"><span data-stu-id="34afc-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="34afc-107">ค้นหาคัมบัง</span><span class="sxs-lookup"><span data-stu-id="34afc-107">Find the kanban.</span></span>
1. <span data-ttu-id="34afc-108">ไปที่การควบคุมการผลิต > คัมบัง > คัมบัง</span><span class="sxs-lookup"><span data-stu-id="34afc-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="34afc-109">เปิดตัวกรองคอลัมน์สถานะหน่วยจัดการวัสดุ</span><span class="sxs-lookup"><span data-stu-id="34afc-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="34afc-110">คลิกล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="34afc-110">Click Clear.</span></span>
    * <span data-ttu-id="34afc-111">นี่จะรีเซ็ตตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="34afc-111">This resets the filters.</span></span>  
4. <span data-ttu-id="34afc-112">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="34afc-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="34afc-113">ตัวอย่างเช่น กรองข้อมูลในฟิลด์หมายเลขบัตรด้วยค่า '000149'</span><span class="sxs-lookup"><span data-stu-id="34afc-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="34afc-114">เปลี่ยนสถานะว่างเปล่า เป็นสถานะได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="34afc-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="34afc-115">คลิกกลับหน่วยจัดการวัสดุที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="34afc-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="34afc-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="34afc-116">Click OK.</span></span>
    * <span data-ttu-id="34afc-117">สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="34afc-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="34afc-118">เปลี่ยนสถานะได้รับแล้ว เป็นสถานะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="34afc-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="34afc-119">คลิกคัมบังที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="34afc-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="34afc-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="34afc-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="34afc-121">สังเกตว่าสถานะหน่วยจัดการวัสดุเป็น ว่างแล้ว</span><span class="sxs-lookup"><span data-stu-id="34afc-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]