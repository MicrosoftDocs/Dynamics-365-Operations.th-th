--- 
title: "รักษาข้อมูลการบาดเจ็บและการเจ็บป่วยของพนักงาน"
description: "ขั้นแรกควรจะมีการดำเนินการคุ่มืองาน 'การตั้งค่าเหตุการณ์การบาดเจ็บและการเจ็บป่วย' ให้เสร็จสมบูรณ์ก่อน เนื่องจากข้อมูลของการตั้งค่าบางส่วนถูกใช้ที่นี่ "
author: ShielaSogge
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: e46c49a136896fd166b92dd08c63993b0684536d
ms.contentlocale: th-th
ms.lasthandoff: 02/02/2018

---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="6b5ca-103">รักษาข้อมูลการบาดเจ็บและการเจ็บป่วยของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="6b5ca-103">Maintain employee injury and illness information</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b5ca-104">ขั้นแรกควรจะมีการดำเนินการคุ่มืองาน 'การตั้งค่าเหตุการณ์การบาดเจ็บและการเจ็บป่วย' ให้เสร็จสมบูรณ์ก่อน เนื่องจากข้อมูลของการตั้งค่าบางส่วนถูกใช้ที่นี่ </span><span class="sxs-lookup"><span data-stu-id="6b5ca-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="6b5ca-105">การบันทึกงานนี้ครอบคลุมขั้นตอนพื้นฐานในการสร้างกรณีการบาดเจ็บหรือการเจ็บป่วย </span><span class="sxs-lookup"><span data-stu-id="6b5ca-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="6b5ca-106">นอกจากการติดตามรายละเอียดของการบาดเจ็บหรือการเจ็บป่วย ยังมีสถานะกรณีที่มีต้องมีการติดตามข้อมูลด้วยเช่นกัน </span><span class="sxs-lookup"><span data-stu-id="6b5ca-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="6b5ca-107">กรณีมีค่าเริ่มต้นที่สถานะ 'เปิด' </span><span class="sxs-lookup"><span data-stu-id="6b5ca-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="6b5ca-108">สถานะต่างๆสามารถจัดการได้จากสินค้าเมนู 'สถานะกรณี' ในแถบแอพลิเคชันที่ด้านบนของแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="6b5ca-108">The statuses can be managed from the 'Case status' menu item in the application bar at the top of the form.</span></span>

1. <span data-ttu-id="6b5ca-109">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > การบาดเจ็บและการเจ็บป่วย > เหตุการณ์การบาดเจ็บหรือการเจ็บป่วย</span><span class="sxs-lookup"><span data-stu-id="6b5ca-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="6b5ca-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-110">Click New.</span></span>
3. <span data-ttu-id="6b5ca-111">ในฟิลด์คำอธิบายกรณี ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-112">ตัวอย่างเช่น การบาดเจ็บข้อมือ</span><span class="sxs-lookup"><span data-stu-id="6b5ca-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="6b5ca-113">ในฟิลด์ผู้ปฏิบัติงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-114">ตัวอย่าง Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="6b5ca-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="6b5ca-115">ในฟิลด์วันที่และเวลาของเหตุการณ์ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="6b5ca-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="6b5ca-116">ตัวอย่าง 1/20/2016 10:00 น.</span><span class="sxs-lookup"><span data-stu-id="6b5ca-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="6b5ca-117">ในฟิลด์ชนิดการบาดเจ็บหรือการเจ็บป่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-118">ตัวอย่าง: การแตกร้าว</span><span class="sxs-lookup"><span data-stu-id="6b5ca-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="6b5ca-119">ในฟิลด์อวัยวะ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-120">ตัวอย่าง: ข้อมือ</span><span class="sxs-lookup"><span data-stu-id="6b5ca-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="6b5ca-121">ในฟิลด์ชนิดของผลลัพธ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-122">ตัวอย่าง: การบำบัด</span><span class="sxs-lookup"><span data-stu-id="6b5ca-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="6b5ca-123">ในฟิลด์วันที่และเวลาที่รายงาน ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="6b5ca-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="6b5ca-124">วันที่และเวลาที่รายงานต้องเป็นวันหลังจากวันที่และวันเกิดเหตุ</span><span class="sxs-lookup"><span data-stu-id="6b5ca-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="6b5ca-125">ในฟิลด์บุคคลที่รายงานกรณี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-126">นี่อาจเป็นพนักงานหรือพยานอื่นในเหตุการณ์ </span><span class="sxs-lookup"><span data-stu-id="6b5ca-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="6b5ca-127">ตัวอย่าง Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="6b5ca-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="6b5ca-128">ขยายส่วนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="6b5ca-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="6b5ca-129">ในฟิลด์สถานที่เกิดเหตุ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-130">ตัวอย่าง คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="6b5ca-131">เลือก ใช่ ในฟิลด์ในบริเวณสถานที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6b5ca-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="6b5ca-132">ถ้าเหตุการณ์เกิดขึ้นในบริเวณสถานที่ทำงาน ให้เลือก ใช่</span><span class="sxs-lookup"><span data-stu-id="6b5ca-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="6b5ca-133">ในฟิลด์วันที่และเวลาที่เริ่มการทำงาน ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="6b5ca-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="6b5ca-134">ป้อนวันที่และเวลาที่ส่งผลกระทบต่อการเริ่มทำงานแต่ละครั้ง ก่อนที่จะเกิดเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="6b5ca-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="6b5ca-135">ในฟิลด์งานหรืองานของพนักงาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-136">ป้อนงานหรืองานที่ผู้ปฏิบัติงานกำลังดำเนินการอยู่เมื่อเกิดเหตุการณ์ </span><span class="sxs-lookup"><span data-stu-id="6b5ca-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="6b5ca-137">ตัวอย่าง:  การโหลดกล่อง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="6b5ca-138">ในฟิลด์สาเหตุของเหตุการณ์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-139">ป้อนสาเหตุของเหตุการณ์ </span><span class="sxs-lookup"><span data-stu-id="6b5ca-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="6b5ca-140">ตัวอย่าง:  ลื่นบนพื้นเปียก</span><span class="sxs-lookup"><span data-stu-id="6b5ca-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="6b5ca-141">ในฟิลด์ระดับความรุนแรง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="6b5ca-142">ในฟิลด์การดำเนินการที่จะใช้ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-143">ตัวอย่าง ล้างสิ่งที่หกโดยทันที</span><span class="sxs-lookup"><span data-stu-id="6b5ca-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="6b5ca-144">ในฟิลด์จำนวนวันหยุดงานที่คาดไว้ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6b5ca-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="6b5ca-145">ป้อนจำนวนวันที่คาดว่าบุคคลจะหยุดงาน </span><span class="sxs-lookup"><span data-stu-id="6b5ca-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="6b5ca-146">หลังจากที่แต่ละบุคคลกลับมาทำงาน ให้อัพเดตฟิลด์ 'จำนวนวันหยุดงาน' ด้วยจำนวนวันที่หยุดจริง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="6b5ca-147">ขยายส่วนต้นทุนการบาดเจ็บหรือการเจ็บป่วย</span><span class="sxs-lookup"><span data-stu-id="6b5ca-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="6b5ca-148">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6b5ca-148">Click Add.</span></span>
22. <span data-ttu-id="6b5ca-149">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6b5ca-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="6b5ca-150">ในฟิลด์ชนิดต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-151">ตัวอย่าง:  การบำบัด    คุณยังสามารถป้อนยอดเงินและแนบเอกสารประกอบการสนับสนุนใดๆ เช่น ใบแจ้งหนี้ หรือบันทึกย่อของแพทย์ ไปยังต้นทุน</span><span class="sxs-lookup"><span data-stu-id="6b5ca-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="6b5ca-152">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6b5ca-152">Click Add.</span></span>
25. <span data-ttu-id="6b5ca-153">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6b5ca-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="6b5ca-154">ในฟิลด์ชนิดต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-155">ตัวอย่าง แพทย์</span><span class="sxs-lookup"><span data-stu-id="6b5ca-155">Example: Doctor</span></span>  
27. <span data-ttu-id="6b5ca-156">ขยายส่วนการรักษาการบาดเจ็บหรือการเจ็บป่วย</span><span class="sxs-lookup"><span data-stu-id="6b5ca-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="6b5ca-157">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6b5ca-157">Click Add.</span></span>
29. <span data-ttu-id="6b5ca-158">ในฟิลด์วันที่การรักษา ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="6b5ca-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="6b5ca-159">ในฟิลด์ชนิดการรักษา ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="6b5ca-160">ตัวอย่าง เข้าเฝือก</span><span class="sxs-lookup"><span data-stu-id="6b5ca-160">Example:  Splint</span></span>  
31. <span data-ttu-id="6b5ca-161">ไม่จำเป็นต้องตั้งให้การเข้ารับบริการที่ห้องฉุกเฉินของโรงพยาบาลเป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="6b5ca-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="6b5ca-162">ในฟิลด์ข้อคิดเห็นเกี่ยวกับการรักษา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-163">ตัวอย่าง เข้าเฝือกเป็นเวลา 2 สัปดาห์</span><span class="sxs-lookup"><span data-stu-id="6b5ca-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="6b5ca-164">ในฟิลด์ชื่อแพทย์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-165">ตัวอย่าง นายแพทย์แอนเดอร์สัน</span><span class="sxs-lookup"><span data-stu-id="6b5ca-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="6b5ca-166">ในฟิลด์สถานประกอบการรักษาพยาบาลและที่ตั้ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-167">ตัวอย่าง Elm St. ฉุกเฉิน</span><span class="sxs-lookup"><span data-stu-id="6b5ca-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="6b5ca-168">ในฟิลด์รายละเอียดการรักษา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6b5ca-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="6b5ca-169">ตัวอย่าง Xray ยืนยันการแตกร้าว เข้าเฝือก</span><span class="sxs-lookup"><span data-stu-id="6b5ca-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="6b5ca-170">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6b5ca-170">Click Save.</span></span>
    * <span data-ttu-id="6b5ca-171">สถานะกรณีสามารถอัพเดตได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="6b5ca-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="6b5ca-172">ตั้งค่ากรณีเป็น อยู่ระหว่างดำเนินการ หากระหว่างการประมวลผลการบาดเจ็บหรือการเจ็บป่วยอยู่ระหว่างการดำเนินการ </span><span class="sxs-lookup"><span data-stu-id="6b5ca-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="6b5ca-173">เมื่อคุณปิดเหตุการณ์ คุณสามารถเพิ่มเท่านั้นหรือลบต้นทุน การรักษาพยาบาลหรือการยื่นเอกสารแจ้งที่เกี่ยวข้องกับเหตุการณ์ได้เท่านั้น </span><span class="sxs-lookup"><span data-stu-id="6b5ca-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="6b5ca-174">เพื่อปรับเปลี่ยนข้อมูลอื่น ให้เปิดกรณีอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6b5ca-174">To modify other information, reopen the case.</span></span>  


