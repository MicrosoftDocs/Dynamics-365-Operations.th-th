---
title: เปลี่ยนกฎคัมบังสำหรับงานในกระบวนการ
description: 'กระบวนงานนี้มุ่งเน้นการเปลี่ยนแปลงกฎคัมบังที่ใช้แล้วสำหรับคัมบังที่กำหนด '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 485afff3747a87a6e36f0249b146a39361d81b23
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147146"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="f0f31-103">เปลี่ยนกฎคัมบังสำหรับงานในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="f0f31-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0f31-104">กระบวนงานนี้มุ่งเน้นการเปลี่ยนแปลงกฎคัมบังที่ใช้แล้วสำหรับคัมบังที่กำหนด </span><span class="sxs-lookup"><span data-stu-id="f0f31-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="f0f31-105">ซึ่งเป็นประโยชน์ในการตั้งระดับปริมาณระดับทรัพยากรหรือในกรณีของการแบ่ง </span><span class="sxs-lookup"><span data-stu-id="f0f31-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="f0f31-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f0f31-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f0f31-107">กระบวนงานนี้มีไว้สำหรับนักวางแผนซึ่งทำงานในบริษัทการผลิตแบบ Lean ที่มีความรับผิดชอบต่อสายธารคุณค่า</span><span class="sxs-lookup"><span data-stu-id="f0f31-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="f0f31-108">คัดลอกกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f0f31-108">Copy kanban rule</span></span>
1. <span data-ttu-id="f0f31-109">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f0f31-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="f0f31-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f0f31-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f0f31-111">เลือกเหตุการณ์กฎคัมบัง 000022 สำหรับ L0001</span><span class="sxs-lookup"><span data-stu-id="f0f31-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="f0f31-112">คลิกทำซ้ำกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f0f31-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="f0f31-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f0f31-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="f0f31-114">เปลี่ยนกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f0f31-114">Change kanban rule</span></span>
1. <span data-ttu-id="f0f31-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f0f31-115">Close the page.</span></span>
2. <span data-ttu-id="f0f31-116">ไปที่การกำหนดงานคัมบัง</span><span class="sxs-lookup"><span data-stu-id="f0f31-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="f0f31-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f0f31-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f0f31-118">เลือกรายการที่มีคัมบัง 000177</span><span class="sxs-lookup"><span data-stu-id="f0f31-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="f0f31-119">คลิกใช้กฎคัมบังสำรอง</span><span class="sxs-lookup"><span data-stu-id="f0f31-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="f0f31-120">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="f0f31-120">Click Next.</span></span>
6. <span data-ttu-id="f0f31-121">ในฟิลด์กฎคัมบัง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f0f31-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="f0f31-122">เลือกกฎคัมบังที่สร้างไว้ก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="f0f31-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="f0f31-123">นี่คือกฎคัมบังที่มีหมายเลขสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f0f31-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="f0f31-124">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="f0f31-124">Click Finish.</span></span>
    * <span data-ttu-id="f0f31-125">ขณะนี้งานคัมบังกำลังใช้กฎคัมบังอื่นอยู่ </span><span class="sxs-lookup"><span data-stu-id="f0f31-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="f0f31-126">ซึ่งสามารถใช้เพื่อตั้งระดับปริมาณเซลล์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f0f31-126">This can be useful to level load work cells.</span></span>  

