---
title: คำแนะนำการคำนวณปริมาณตามระบบคัมบัง
description: ขั้นตอนนี้มุ่งเน้นการเพิ่มประสิทธิภาพการคำนวณปริมาณตามระบบคัมบังสำหรับกฎคัมบังที่ระบุ โดยการใช้การคำนวณปริมาณตามระบบคัมบัง
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 409903740413994fead3f65b12afb414ca5c43ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255408"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="2d1c4-103">คำแนะนำการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-103">Calculate kanban quantity suggestions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d1c4-104">ขั้นตอนนี้มุ่งเน้นการเพิ่มประสิทธิภาพการคำนวณปริมาณตามระบบคัมบังสำหรับกฎคัมบังที่ระบุ โดยการใช้การคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="2d1c4-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="2d1c4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2d1c4-106">ขั้นตอนนี้มีไว้สำหรับผู้จัดการการสายธารคุณค่า </span><span class="sxs-lookup"><span data-stu-id="2d1c4-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="2d1c4-107">มันเป็นข้อกำหนดเบื้องต้นว่าคุณต้องเพิ่มนโยบายการคำนวณปริมาณตามระบบคัมบังใหม่ให้กับกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="2d1c4-108">สร้างการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="2d1c4-109">ไปที่การควบคุมการผลิต > งานประจำงวด > การคำนวณปริมาณตามระบบคัมบัง > คำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="2d1c4-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-110">Click New.</span></span>
3. <span data-ttu-id="2d1c4-111">ในฟิลด์ชื่อ ให้พิมพ์ 'Speaker2016'</span><span class="sxs-lookup"><span data-stu-id="2d1c4-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="2d1c4-112">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2d1c4-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2d1c4-113">เลือกนโยบายที่คุณสร้างขึ้นในขั้นตอนการเพิ่มนโยบายการคำนวณปริมาณตามระบบคัมบังใหม่ให้กับกฎคัมบัง </span><span class="sxs-lookup"><span data-stu-id="2d1c4-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="2d1c4-114">ตัวอย่างเช่น Speaker2016</span><span class="sxs-lookup"><span data-stu-id="2d1c4-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="2d1c4-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d1c4-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2d1c4-116">ในฟิลด์กฎของวันการใช้งาน ให้ตั้งค่าวันและเวลาเป็น ' 2012-12-17T08:00:00'</span><span class="sxs-lookup"><span data-stu-id="2d1c4-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="2d1c4-117">วันนี้เป็นวันที่ให้ข้อมูลพื้นฐานสำหรับการกำหนดว่า กฎคัมบังคงที่ใดรวมอยู่ในการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="2d1c4-118">ในฟิลด์วันที่สิ้นสุดรอบระยะเวลาความต้องการที่เติมเต็มแล้ว ให้ตั้งค่าวันและเวลาเป็น ' 2012-11-17T09:00:00'</span><span class="sxs-lookup"><span data-stu-id="2d1c4-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="2d1c4-119">วันที่เริ่มต้นเมื่อรวมธุรกรรมความต้องการในอดีตเพื่อคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="2d1c4-120">ในฟิลด์วันสิ้นสุดรอบระยะเวลาของความต้องการ ให้ตั้งวันและเวลาเป็น ' 2012-12-17T07:59:59'</span><span class="sxs-lookup"><span data-stu-id="2d1c4-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="2d1c4-121">วันที่สิ้นสุดเมื่อรวมธุรกรรมความต้องการในอดีตเพื่อคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="2d1c4-122">ในฟิลด์วันเริ่มต้นรอบระยะเวลาความต้องการ ให้ตั้งวันและเวลาเป็น ' 2012-12-17T08:00:00'</span><span class="sxs-lookup"><span data-stu-id="2d1c4-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="2d1c4-123">วันที่เริ่มต้นเมื่อรวมธุรกรรมความต้องการปัจจุบันเพื่อคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="2d1c4-124">ในฟิลด์รอบระยะเวลาของความต้องการ ให้ตั้งวันและเวลาเป็น ' 2013-01-16T07:59:59'</span><span class="sxs-lookup"><span data-stu-id="2d1c4-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="2d1c4-125">วันที่สิ้นสุดเมื่อรวมธุรกรรมความต้องการปัจจุบันเพื่อคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="2d1c4-126">สร้างข้อเสนอปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="2d1c4-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2d1c4-127">Click Save.</span></span>
2. <span data-ttu-id="2d1c4-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-128">Click Generate.</span></span>
    * <span data-ttu-id="2d1c4-129">ขั้นตอนนี้สร้างรายการข้อเสนอปริมาณตามระบบคัมบังสำหรับกฎคัมบัง 000020</span><span class="sxs-lookup"><span data-stu-id="2d1c4-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="2d1c4-130">รันการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="2d1c4-131">คลิก คำนวณ</span><span class="sxs-lookup"><span data-stu-id="2d1c4-131">Click Calculate.</span></span>
    * <span data-ttu-id="2d1c4-132">สิ่งนี้คำนวณข้อเสนอปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="2d1c4-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-133">Click OK.</span></span>
3. <span data-ttu-id="2d1c4-134">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d1c4-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2d1c4-135">ข้อความแจ้งเตือนแนะนำปริมาณตามระบบคัมบังคือ 2</span><span class="sxs-lookup"><span data-stu-id="2d1c4-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="2d1c4-136">เปลี่ยนแปลงปริมาณสินค้า และคำนวณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="2d1c4-137">ตั้งค่าปริมาณผลิตภัณฑ์เป็น 5</span><span class="sxs-lookup"><span data-stu-id="2d1c4-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="2d1c4-138">คลิก คำนวณ</span><span class="sxs-lookup"><span data-stu-id="2d1c4-138">Click Calculate.</span></span>
3. <span data-ttu-id="2d1c4-139">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-139">Click OK.</span></span>
    * <span data-ttu-id="2d1c4-140">โปรดสังเกตว่า ตรงที่มีปริมาณตามระบบคัมบังเท่ากับ 5 คำแนะนำถูกเปลี่ยนให้เป็นปริมาณตามระบบคัมบังเท่ากับ 4</span><span class="sxs-lookup"><span data-stu-id="2d1c4-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="2d1c4-141">ซึ่งมีสาเหตุจากข้อเท็จจริงที่ว่า มีปริมาณผลิตภัณฑ์ต่ำ เราต้องการคัมบังเพิ่มเติมเพื่อตอบสนองความต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d1c4-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="2d1c4-142">อัพเดตกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-142">Update kanban rule</span></span>
1. <span data-ttu-id="2d1c4-143">ในฟิลด์ของกฎของวันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="2d1c4-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="2d1c4-144">ตั้ง 'กฎใช้งาน ณ วันนี้' เป็นวันในอนาคต </span><span class="sxs-lookup"><span data-stu-id="2d1c4-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="2d1c4-145">ตัวอย่างเช่น วันนี้ + หนึ่งปี</span><span class="sxs-lookup"><span data-stu-id="2d1c4-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="2d1c4-146">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="2d1c4-146">Click Update.</span></span>
3. <span data-ttu-id="2d1c4-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-147">Click OK.</span></span>
4. <span data-ttu-id="2d1c4-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2d1c4-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="2d1c4-149">ตรวจสอบความถูกต้องของการเปลี่ยนแปลงในกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="2d1c4-150">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > การผลิตแบบ Lean > กฏคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="2d1c4-151">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d1c4-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d1c4-152">เลือกกฎคัมบังที่สร้างขึ้นโดยงานย่อยก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="2d1c4-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="2d1c4-153">สิ่งควรเป็นกฎคัมบังแรกในการเรียงลำดับตามหมายเลขรายการ</span><span class="sxs-lookup"><span data-stu-id="2d1c4-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="2d1c4-154">สลับการขยายส่วนของรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="2d1c4-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="2d1c4-155">โปรดสังเกตวันทีผลมีการบังคับใช้ ซึ่งหมายความว่า กฎนี้จะไม่ถูกใช้งานจนกว่าถึงวันที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="2d1c4-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="2d1c4-156">สลับการขยายส่วนของปริมาณ </span><span class="sxs-lookup"><span data-stu-id="2d1c4-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="2d1c4-157">โปรดสังเกตว่า นี่คือปริมาณเริ่มต้นที่คุณป้อนไว้ในการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="2d1c4-158">โปรดสังเกตว่า นี่คือปริมาณคัมบังแบบคงที่ที่เท่ากับ 4 จากการคำนวณปริมาณตามระบบคัมบัง</span><span class="sxs-lookup"><span data-stu-id="2d1c4-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="2d1c4-159">คลิก ListPanelแท็บ</span><span class="sxs-lookup"><span data-stu-id="2d1c4-159">Click the ListPanel tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]