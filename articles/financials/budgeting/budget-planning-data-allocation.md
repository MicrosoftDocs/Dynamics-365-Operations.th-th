---
title: "การปันส่วนข้อมูลของการวางแผนงบประมาณ"
description: "บทความนี้อธิบายถึงวิธีการปันส่วนต่างๆ ที่มีอยู่ใน Microsoft Dynamics 365 for Finance and Operations และวิธีการใช้"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 430040f7b3706aa1ad913d70c0dbcab9249ea222
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="f976d-103">การปันส่วนข้อมูลของการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f976d-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f976d-104">บทความนี้อธิบายถึงวิธีการปันส่วนต่างๆ ที่มีอยู่ใน Microsoft Dynamics 365 for Finance and Operations และวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="f976d-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations and how they can be used.</span></span>  

<span data-ttu-id="f976d-105">คุณสามารถกระจายข้อมูลในแผนงบประมาณได้หลายวิธี เพื่อที่จะแสดงยอดเงินที่นำเสนอไว้ได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f976d-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="f976d-106">วิธีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f976d-106">Allocation methods</span></span>
<span data-ttu-id="f976d-107">วิธีการปันส่วนสามวิธี (ปันส่วนข้ามรอบระยะเวลา การปันส่วนไปยังมิติ และใช้กฎการปันส่วนบัญชีแยกประเภท) สามารถสร้างรายการแผนงบประมาณที่ขึ้นอยู่กับรายการในแผนงบประมาณเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f976d-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="f976d-108">วิธีอื่นอีกสามวิธี (รวม กระจาย และคัดลอกจากแผนงบประมาณ) สามารถสร้างรายการแผนงบประมาณในแผนงบประมาณอื่นได้</span><span class="sxs-lookup"><span data-stu-id="f976d-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="f976d-109">สำหรับวิธีการปันส่วนทั้งหกวิธี ให้คุณระบุสถานการณ์จำลองปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f976d-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="f976d-110">สถานการณ์จำลองปลายทางอาจเหมือนกับสถานการณ์จำลองต้นทาง หรือแตกต่างจากสถานการณ์จำลองต้นทาง อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f976d-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="f976d-111">นอกจากนี้ คุณสามารถระบุว่ารายการใหม่จะถูกผนวกเข้ากับแผนงบประมาณ หรือแทนที่รายการปัจจุบันในแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f976d-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="f976d-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**ปันส่วนข้ามรอบระยะเวลา** – ประเภทการปันส่วนตามระยะเวลา ถูกใช้เพื่อปันส่วนรายการแผนงบประมาณ จากสถานการณ์จำลองแผนงบประมาณต้นทางข้ามรอบระยะเวลาในสถานการณ์จำลองปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f976d-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="f976d-113">ยอดเงินต้นทางจะถูกกำหนดให้กับรายการหลายรายการในสถานการณ์จำลองปลายทาง ขึ้นกับเปอร์เซ็นต์และวันที่ที่ถูกกำหนดในประเภทการปันส่วนรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="f976d-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="f976d-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**ปันส่วนให้กับมิติ**– รายการแผนงบประมาณถูกปันส่วนจากสถานการณ์จำลองต้นทาง ไปยังสถานการณ์จำลองปลายทางหนึ่งรายการหรือมากกว่า ตามเปอร์เซ็นต์ของการวางแผนและมิติทางการเงินที่กำหนดไว้ในเงื่อนไขการปันส่วนงบประมาณที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f976d-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="f976d-115">![AggregateChart](./media/aggregatechart-300x230.png)
**รวม** – รายการแผนงบประมาณจะถูกรวม จากสถานการณ์จำลองแผนงบประมาณต้นทางในแผนงบประมาณ (ข้อมูลรอง) ที่เกี่ยวข้อง ไปยังสถานการณ์จำลองปลายทางในแผนงบประมาณหลัก</span><span class="sxs-lookup"><span data-stu-id="f976d-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="f976d-116">วิธีการนี้ทำให้ยอดเงินงบประมาณที่จัดเตรียมไว้ในระดับที่ต่ำกว่าในองค์กร มีการรวมบัญชีในระดับสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="f976d-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="f976d-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**กระจาย**– มีการกระจายรายการแผนงบประมาณ จากสถานการณ์จำลองการวางแผนงบประมาณต้นทางในแผนงบประมาณหลัก ไปยังในสถานการณ์จำลองปลายทางในแผนงบประมาณที่เชื่อมโยง (ข้อมูลรอง) ขึ้นอยู่กับมิติทางการเงินของหน่วยงานขององค์กรของแผนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f976d-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="f976d-118">วิธีการนี้ทำให้ยอดเงินงบประมาณที่จัดเตรียมไว้ในระดับที่ต่ำกว่าในองค์กร มีการครอบคลุมการตรวจทานแบบเฉพาะส่วนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="f976d-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="f976d-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**ใช้กฎการปันส่วนบัญชีแยกประเภท** – มีการกระจายรายการแผนงบประมาณจากสถานการณ์จำลองแผนงบประมาณต้นทาง ไปยังกฎการปันส่วนบัญชีแยกประเภท ขึ้นกับกฎการปันส่วนบัญชีแยกประเภทที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="f976d-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="f976d-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**สำเนาจากแผนงบประมาณ**– ดังเช่นในวิธีกระจายการปันส่วน รายการแผนงบประมาณถูกสร้างขึ้นในปลายทาง ขึ้นอยู่กับรายการในแผนงบประมาณที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f976d-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="f976d-121">อย่างไรก็ตาม สำหรับวิธีการนี้ แผนงบประมาณต้นทางไม่จำเป็นต้องเป็นแผนหลัก แต่สามารถเป็นที่ระดับสูงกว่าใดๆในลำดับชั้นของแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f976d-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="f976d-122">วิธีการปันส่วนนี้มีประโยชน์ ถ้ายอดเงินรวมถูกตั้งงบประมาณแบบดั้งเดิมไว้ที่ระดับสูงมากกว่ามากๆ และต้องถูกโอนย้ายไปยังระดับที่ต่ำกว่าขององค์กรสำหรับการตรวจทานที่มีรายละเอียด และการปรับปรุงก่อนที่จะสามารถได้รับการอนุมัติในระดับที่สูงกว่าได้</span><span class="sxs-lookup"><span data-stu-id="f976d-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="f976d-123">การใช้วิธีการปันส่วนในแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f976d-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="f976d-124">เมื่อต้องการดำเนินการปันส่วนในหน้าแผนงบประมาณ ให้เลือกรายการเพื่อปันส่วน แล้วคลิก **ปันส่วนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="f976d-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="f976d-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="f976d-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="f976d-126">ถัดไป ให้เลือกวิธีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f976d-126">Next, select an allocation method.</span></span> <span data-ttu-id="f976d-127">จากนั้น ฟิลด์ที่เหลืออยู่จะถูกตั้งค่า ขึ้นอยู่กับวิธีการที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="f976d-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="f976d-128">ฟิลด์เหล่านี้ประกอบด้วย ต้นทางและปลายทางของข้อมูลแผนงบประมาณ และตัวเลือกที่ทำให้คุณสามารถใช้คูณแหล่งที่มาด้วยตัวคูณที่ระบุ เมื่อมีการสร้างยอดเงินปลายทาง เพื่อทำให้การปรับปรุงจำนวนมากง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="f976d-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="f976d-129">คุณยังสามารถตั้งค่าตัวเลือก **ผนวกเข้ากับแผน** ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="f976d-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="f976d-130">เลือก **ไม่ใช่** เพื่อแทนที่รายการแผนงบประมาณที่มีอยู่ หรือเลือก **ใช่** เพื่อเก็บรายการแผนงบประมาณที่มีอยู่ และเพิ่มรายการใหม่สำหรับยอดเงินที่ปันส่วน</span><span class="sxs-lookup"><span data-stu-id="f976d-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="f976d-131">การปันส่วนอัตโนมัติในระหว่างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f976d-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="f976d-132">ลักษณะการทำงานที่มีประสิทธิภาพหนึ่งลักษณะ ช่วยให้การปันส่วนสามารถถูกกระทำได้โดยอัตโนมัติเป็นส่วนหนึ่งของลำดับงานการวางแผนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f976d-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="f976d-133">เนื่องจากแผนงบประมาณเคลื่อนที่ผ่านลำดับงาน งานอัตโนมัติสามารถเรียกใช้การปันส่วนที่ระยะการวางแผนงบประมาณที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="f976d-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="f976d-134">เพื่อตั้งค่าการปันส่วนโดยอัตโนมัติ ลำดับแรกคุณต้องสร้างกำหนดการปันส่วนในหน้า **การตั้งค่าคอนฟิกการวางแผนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="f976d-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="f976d-135">กำหนดการปันส่วนกำหนดวิธีการปันส่วนที่จะถูกใช้เมื่อดำเนินการปันส่วนโดยอัตโนมัติ และค่าของตัวเลือกการปันส่วนต่างๆ (ดูที่ส่วนก่อนหน้านี้สำหรับคำอธิบาย)</span><span class="sxs-lookup"><span data-stu-id="f976d-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="f976d-136">ถัดไป คุณสร้างการปันส่วนระยะในหน้า **การตั้งค่าคอนฟิกการวางแผนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="f976d-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="f976d-137">การปันส่วนระยะมอบหมาย กำหนดการปันส่วนให้กับลำดับงานการวางแผนงบประมาณและระยะ</span><span class="sxs-lookup"><span data-stu-id="f976d-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="f976d-138">ในตอนท้าย เพิ่มงานอัตโนมัติสำหรับการปันส่วนระยะการวางแผนงบประมาณ ที่ระยะของลำดับงานที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f976d-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="f976d-139">ในตัวอย่างต่อไปนี้ การปันส่วนระยะการวางแผนงบประมาณสองแบบ (ถูกล้อมรอบด้วยสีแดง) ได้ถูกแทรกลงในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f976d-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="f976d-140">[![การปันส่วนขั้นการวางแผนงบประมาณ](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="f976d-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




