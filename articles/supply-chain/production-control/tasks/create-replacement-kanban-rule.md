---
title: สร้างกฎคัมบังการแทนที่
description: 'กระบวนงานนี้มุ่งเน้นการแทนที่กฎคัมบังที่มีอยู่ด้วยกฎคัมบังที่ใหม่ในวันที่เฉพาะ '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ded10b0972f07f4f86ee32cee596c5e30b15ebd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843780"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="92041-103">สร้างกฎคัมบังการแทนที่</span><span class="sxs-lookup"><span data-stu-id="92041-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92041-104">กระบวนงานนี้มุ่งเน้นการแทนที่กฎคัมบังที่มีอยู่ด้วยกฎคัมบังที่ใหม่ในวันที่เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="92041-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="92041-105">สิ่งนี้มีประโยชน์ เมื่อการเปลี่ยนแปลงในขั้นตอนการผลิตและกฎการเติมสินค้าต้องถูกทำให้สอดคล้องกันและต้องถูกจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="92041-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="92041-106">บริษัทข้อมูลสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="92041-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="92041-107">กระบวนงานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เมื่อพวกเขาเตรียมการผลิตสำหรับขั้นตอนการผลิตที่เปลี่ยนแปลงหรือกฎการเติมสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="92041-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="92041-108">งานนี้แทนที่กฎคัมบัง 000022 ด้วยกฎใหม่ และเพิ่มปริมาณสูงสุดจาก 48 เป็น 100 สำหรับกฎใหม่</span><span class="sxs-lookup"><span data-stu-id="92041-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="92041-109">เลือกกฎคัมบังเพื่อแทนที่</span><span class="sxs-lookup"><span data-stu-id="92041-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="92041-110">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="92041-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="92041-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="92041-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="92041-112">เลือกกฎคัมบัง 000022</span><span class="sxs-lookup"><span data-stu-id="92041-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="92041-113">สร้างกฎคัมบังการแทนที่</span><span class="sxs-lookup"><span data-stu-id="92041-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="92041-114">คลิกแทนที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="92041-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="92041-115">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="92041-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="92041-116">เลือกวันที่ในอนาคต เช่น หนึ่งสัปดาห์จากนี้ </span><span class="sxs-lookup"><span data-stu-id="92041-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="92041-117">นี่คือวันที่และเวลาเมื่อกฎคัมบังใหม่กลายเป็นใช้งานอยู่ และแทนที่กฎคัมบังเก่า</span><span class="sxs-lookup"><span data-stu-id="92041-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="92041-118">ถ้ากฎคัมบังเปลี่ยนแปลงพาธในขั้นตอนการผลิต กิจกรรมอื่นสามารถถูกเลือกได้ </span><span class="sxs-lookup"><span data-stu-id="92041-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="92041-119">ในกระบวนงานนี้ เราจะเก็บกิจกรรมไม่ได้ดำเนินการใดๆ</span><span class="sxs-lookup"><span data-stu-id="92041-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="92041-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="92041-120">Click OK.</span></span>
    * <span data-ttu-id="92041-121">หมายเหตุว่า กฎคัมบังใหม่ถูกสร้างเพื่อแทนที่กฎคัมบัง 000022</span><span class="sxs-lookup"><span data-stu-id="92041-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="92041-122">วันที่มีผลบังคับใช้ถูกตั้งค่าโดยขึ้นกับวันที่ที่เลื่อกเมื่อคุณแทนที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="92041-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="92041-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="92041-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="92041-124">เลือกกฎคัมบังที่ถูกแทนที่ 000022</span><span class="sxs-lookup"><span data-stu-id="92041-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="92041-125">หมายเหตุว่า กฎคัมบังที่ถูกแทนที่มีวันที่เดียวกับวันที่หมดอายุ เพราะนี่คือวันที่เมื่อจะหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="92041-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="92041-126">ในรายการ ให้เลือกแถว 1</span><span class="sxs-lookup"><span data-stu-id="92041-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="92041-127">เลือกกฎคัมบังใหม่ที่อยู่บนสุดของรายการ </span><span class="sxs-lookup"><span data-stu-id="92041-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="92041-128">นี่คือกฎคัมบังที่มีหมายเลขกฎคัมบังสูงสุด</span><span class="sxs-lookup"><span data-stu-id="92041-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="92041-129">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92041-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="92041-130">คลิกหมายเลขกฎคัมบัง เพื่อเปิดกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="92041-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="92041-131">แก้ไขขีดจำกัดสูงสุดสำหรับกฎคัมบังการแทนที่</span><span class="sxs-lookup"><span data-stu-id="92041-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="92041-132">ตั้งค่าปริมาณสูงสุดเป็น '100'</span><span class="sxs-lookup"><span data-stu-id="92041-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="92041-133">ขยาย FastTab ปริมาณ เพื่อดูฟิลด์ปริมาณสูงสุด </span><span class="sxs-lookup"><span data-stu-id="92041-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="92041-134">การเปลี่ยนปริมาณสูงสุดเป็น 100 จะอนุญาตให้สูงสุด 100 คัมบังถูกประมวลผลได้ </span><span class="sxs-lookup"><span data-stu-id="92041-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="92041-135">นี่คือขั้นตอนสุดท้ายในงานนี้</span><span class="sxs-lookup"><span data-stu-id="92041-135">This is the last step in this task.</span></span>  

