--- 
title: "สร้างกฎคัมบังใหม่โดยทำซ้ำกฎคัมบังที่มีอยู่"
description: "ขั้นตอนนี้มุ่งเน้นการสร้างการทำซ้ำของกฎคัมบังที่มีอยู่ "
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d375e6c029e575269f7b9fce8a2eb9ac95717b5c
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="adb35-103">สร้างกฎคัมบังใหม่โดยทำซ้ำกฎคัมบังที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="adb35-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="adb35-104">ขั้นตอนนี้มุ่งเน้นการสร้างการทำซ้ำของกฎคัมบังที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="adb35-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="adb35-105">สิ่งนี้มีประโยชน์ถ้าคุณต้องการจะสร้างกฎคัมบังใหม่โดยอาศัยกฎคัมบังที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="adb35-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="adb35-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="adb35-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="adb35-107">ขั้นตอนนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสตรีมค่าตามที่พวกเขาจัดเตรียมการผลิตสำหรับผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="adb35-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="adb35-108">เลือกกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="adb35-108">Select a kanban rule</span></span>
1. <span data-ttu-id="adb35-109">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="adb35-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="adb35-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="adb35-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="adb35-111">เลือกเหตุการณ์กฎคัมบัง 000017 สำหรับ M0006</span><span class="sxs-lookup"><span data-stu-id="adb35-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="adb35-112">ทำซ้ำกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="adb35-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="adb35-113">คลิกทำซ้ำกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="adb35-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="adb35-114">เมื่อทำซ้ำกฎคัมบัง เป็นไปได้ที่จะเปลี่ยนชนิด วัน กิจกรรม และการเลือกผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="adb35-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="adb35-115">เปลี่ยนผลิตภัณฑ์สำหรับขั้นตอนนี้ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="adb35-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="adb35-116">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="adb35-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="adb35-117">เลือก M0007</span><span class="sxs-lookup"><span data-stu-id="adb35-117">Select M0007.</span></span>  
3. <span data-ttu-id="adb35-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="adb35-118">Click OK.</span></span>
    * <span data-ttu-id="adb35-119">โปรดทราบว่ามีการสร้างซ้ำของกฎคัมบัง 000017</span><span class="sxs-lookup"><span data-stu-id="adb35-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    


