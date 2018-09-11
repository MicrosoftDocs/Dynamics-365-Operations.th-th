--- 
title: "เพิ่มนโยบายการคำนวณปริมาณคัมบังให้กับกฎคัมบัง"
description: "ขั้นตอนนี้มุ่งเน้นการสร้างนโยบายการคำนวณปริมาณตามระบบคัมบังและการเพิ่มเติมให้กฎคัมบังเพื่อปรับประสิทธิภาพของขนาดและปริมาณระบบคัมบัง "
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 81a3bc9cf0f9853d9c5f795d835fc6cead2a47eb
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="15e72-103">เพิ่มนโยบายการคำนวณปริมาณคัมบังให้กับกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15e72-104">ขั้นตอนนี้มุ่งเน้นการสร้างนโยบายการคำนวณปริมาณตามระบบคัมบังและการเพิ่มเติมให้กฎคัมบังเพื่อปรับประสิทธิภาพของขนาดและปริมาณระบบคัมบัง </span><span class="sxs-lookup"><span data-stu-id="15e72-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="15e72-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="15e72-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="15e72-106">ขั้นตอนนี้มีไว้สำหรับผู้จัดการการสายธารคุณค่า </span><span class="sxs-lookup"><span data-stu-id="15e72-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="15e72-107">ขั้นตอนนี้เป็นข้อกำหนดเบื้องต้นสำหรับการสร้างกระบวนงานคำแนะนำที่ใช้ในการคำนวณปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="15e72-108">สร้างนโยบายการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="15e72-109">ไปที่การควบคุมผลิตภัณฑ์ > งานประจำงวด > การคำนวณปริมาณคัมบัง > นโยบายการคำนวณปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="15e72-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="15e72-110">Click New.</span></span>
3. <span data-ttu-id="15e72-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="15e72-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="15e72-112">ตัวอย่างเช่น พิมพ์ Speaker2016</span><span class="sxs-lookup"><span data-stu-id="15e72-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="15e72-113">ในฟิลด์แผนหลัก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="15e72-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="15e72-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="15e72-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15e72-115">เลือก StaticPlan เพื่อคำนวณความต้องการ</span><span class="sxs-lookup"><span data-stu-id="15e72-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="15e72-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="15e72-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="15e72-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="15e72-117">Click Save.</span></span>
8. <span data-ttu-id="15e72-118">ในฟิลด์ปริมาณคัมบังต่ำสุด ให้ป้อน '1' </span><span class="sxs-lookup"><span data-stu-id="15e72-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="15e72-119">นี่เป็นจำนวนเพิ่มเติมของคัมบังที่ถูกรวมอยู่ในการคำนวณปริมาณคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="15e72-120">ตั้งค่าความปลอดภัยเป็น '1' </span><span class="sxs-lookup"><span data-stu-id="15e72-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="15e72-121">นี่เป็นปัจจัยที่ถูกใช้เพื่อคำนวณปริมาณเพิ่มเติมของปริมาณสินค้าคงคลังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="15e72-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="15e72-122">ในฟิลด์จำนวนวันข้างหน้า ให้ป้อน '30' </span><span class="sxs-lookup"><span data-stu-id="15e72-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="15e72-123">นี่เป็นจำนวนวันล่วงหน้าวันที่ของการคำนวณปริมาณคัมบัง ที่ถูกรวมอยู่ในการคำนวณความต้องการ</span><span class="sxs-lookup"><span data-stu-id="15e72-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="15e72-124">ในฟิลด์จำนวนวันย้อนหลัง ให้ป้อน '30' </span><span class="sxs-lookup"><span data-stu-id="15e72-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="15e72-125">นี่คือจำนวนวันที่ได้หลังจากวันที่มีการคำนวณปริมาณตามระบบคัมบัง ซึ่งรวมถึงการคำนวณปริมาณความต้องการด้วย </span><span class="sxs-lookup"><span data-stu-id="15e72-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="15e72-126">โดยสูตรที่ใช้สำหรับการคำนวณนั้นจะถูกแสดงพร้อมกับมูลค่าที่แท้จริง </span><span class="sxs-lookup"><span data-stu-id="15e72-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="15e72-127">ตัวอย่างเช่น ปริมาณตามระบบคัมบัง = ((ความต้องการเฉลี่ยต่อวัน x ระยะเวลารอคอยสินค้า x 2.00) / ปริมาณผลิตภัณฑ์ต่อหน่วยจัดการวัสดุ) + 1</span><span class="sxs-lookup"><span data-stu-id="15e72-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="15e72-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="15e72-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="15e72-129">เพิ่มนโยบายการคำนวณปริมาณคัมบังให้กับกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="15e72-130">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="15e72-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="15e72-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15e72-132">เลือกกฏคัมบัง 000020 สำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="15e72-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="15e72-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="15e72-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="15e72-134">สลับการขยายในส่วนนโยบายการคำนวณระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="15e72-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="15e72-135">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="15e72-135">Click Add.</span></span>
    * <span data-ttu-id="15e72-136">เพิ่มนโยบายการคำนวณปริมาณตามระบบคัมบัง ซึ่งคุณเพิ่งสร้างในงานย่อยก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="15e72-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="15e72-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="15e72-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="15e72-138">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="15e72-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="15e72-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="15e72-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="15e72-140">เลือก Speaker2016 ของนโยบายที่คุณเพิ่งสร้างในงานย่อยก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="15e72-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  


