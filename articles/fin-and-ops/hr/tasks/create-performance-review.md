--- 
title: "สร้างการตรวจสอบประสิทธิภาพ"
description: "กระบวนงานนี้แสดงวิธีการสร้างการตรวจสอบประสิทธิภาพและอธิบายวัตถุประสงค์สำหรับแต่ละส่วนของการตรวจทาน "
author: kherr75
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8568dd98635e463f48f3ecfb2cead57b9896b126
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-performance-review"></a><span data-ttu-id="974fc-103">สร้างการตรวจสอบประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="974fc-103">Create a performance review</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="974fc-104">กระบวนงานนี้แสดงวิธีการสร้างการตรวจสอบประสิทธิภาพและอธิบายวัตถุประสงค์สำหรับแต่ละส่วนของการตรวจทาน </span><span class="sxs-lookup"><span data-stu-id="974fc-104">This procedure shows how to create a performance review and describes the purpose for each section of the review.</span></span> <span data-ttu-id="974fc-105">กระบวนงานนี้สร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="974fc-105">This procedure was created using the USMF demo data company.</span></span> <span data-ttu-id="974fc-106">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="974fc-106">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="974fc-107">คลิก การบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="974fc-107">Click Employee self service.</span></span>
2. <span data-ttu-id="974fc-108">คลิก การตรวจทานใหม่ เพื่อสร้างการตรวจทานใหม่</span><span class="sxs-lookup"><span data-stu-id="974fc-108">Click New review to create a new review.</span></span>
3. <span data-ttu-id="974fc-109">ในฟิลด์ชนิดการตรวจทาน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="974fc-109">In the Review type field, enter or select a value.</span></span>
4. <span data-ttu-id="974fc-110">ในฟิลด์รอบระยะเวลาประสิทธิภาพ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="974fc-110">In the Performance period field, enter or select a value.</span></span>
5. <span data-ttu-id="974fc-111">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="974fc-111">In the End date field, enter a date.</span></span>
6. <span data-ttu-id="974fc-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="974fc-112">Click OK.</span></span>
    * <span data-ttu-id="974fc-113">คุณยังสามารถสร้างการตรวจทานจากเท็มเพลต </span><span class="sxs-lookup"><span data-stu-id="974fc-113">You can also create a review from a template.</span></span> <span data-ttu-id="974fc-114">นี่คือวิธีที่ดีที่สุดในการสร้างการตรวจทานเนื่องจากแต่ละส่วนจะประกอบด้วยข้อมูลที่คุณต้องการในการเริ่มต้นการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="974fc-114">This is the best way to create a review because each section will contain the information that you need to start a review.</span></span>  
7. <span data-ttu-id="974fc-115">คลิก แสดงส่วน เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="974fc-115">Click Show sections to open the drop dialog.</span></span>
8. <span data-ttu-id="974fc-116">เลือก ไม่ ในฟิลด์แสดงเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="974fc-116">Select No in the Show attachments field.</span></span>
9. <span data-ttu-id="974fc-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="974fc-117">Click Save.</span></span>
    * <span data-ttu-id="974fc-118">โปรดสังเกตว่าแท็บเอกสารแนบถูกซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="974fc-118">Notice that the attachments tab is now hidden.</span></span>  
10. <span data-ttu-id="974fc-119">คลิก แสดงส่วน เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="974fc-119">Click Show sections to open the drop dialog.</span></span>
11. <span data-ttu-id="974fc-120">เลือก ใช่ ในฟิลด์แสดงเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="974fc-120">Select Yes in the Show attachments field.</span></span>
12. <span data-ttu-id="974fc-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="974fc-121">Click Save.</span></span>
13. <span data-ttu-id="974fc-122">คลิก เพิ่มเป้าหมายไปยังการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="974fc-122">Click Add goal to review.</span></span>
14. <span data-ttu-id="974fc-123">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="974fc-123">Click Cancel.</span></span>
15. <span data-ttu-id="974fc-124">คลิกเพิ่มความสามารถเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="974fc-124">Click Add competency to open the drop dialog.</span></span>
16. <span data-ttu-id="974fc-125">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="974fc-125">In the Title field, type a value.</span></span>
17. <span data-ttu-id="974fc-126">ในฟิลด์คำอธิบาย ให้ป้อน 'เพิ่มทักษะของลูกค้าด้วยการทำงานร่วมกับทีมสนับสนุน'</span><span class="sxs-lookup"><span data-stu-id="974fc-126">In the Description field, enter 'Increase customer skills by working with the support team'.</span></span>
18. <span data-ttu-id="974fc-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="974fc-127">Click OK.</span></span>
19. <span data-ttu-id="974fc-128">คลิก ยุบทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="974fc-128">Click Collapse all.</span></span>
20. <span data-ttu-id="974fc-129">คลิก ขยายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="974fc-129">Click Expand all.</span></span>
21. <span data-ttu-id="974fc-130">คลิก เพิ่มข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="974fc-130">Click Add comment.</span></span>
22. <span data-ttu-id="974fc-131">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="974fc-131">Click Post.</span></span>
23. <span data-ttu-id="974fc-132">คลิกแท็บการวัด</span><span class="sxs-lookup"><span data-stu-id="974fc-132">Click the Measurements tab.</span></span>
24. <span data-ttu-id="974fc-133">คลิกเพิ่มการวัดเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="974fc-133">Click Add measurement to open the drop dialog.</span></span>
25. <span data-ttu-id="974fc-134">ในฟิลด์การวัด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="974fc-134">In the Measurement field, enter or select a value.</span></span>
26. <span data-ttu-id="974fc-135">ในฟิลด์ยอดเงินเป้าหมาย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="974fc-135">In the Target amount field, enter a number.</span></span>
27. <span data-ttu-id="974fc-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="974fc-136">Click OK.</span></span>
28. <span data-ttu-id="974fc-137">คลิกแท็บกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="974fc-137">Click the Activities tab.</span></span>
29. <span data-ttu-id="974fc-138">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="974fc-138">Click Add.</span></span>
30. <span data-ttu-id="974fc-139">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="974fc-139">In the Title field, type a value.</span></span>
31. <span data-ttu-id="974fc-140">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="974fc-140">In the Description field, type a value.</span></span>
32. <span data-ttu-id="974fc-141">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="974fc-141">In the Start date field, enter a date.</span></span>
33. <span data-ttu-id="974fc-142">ในฟิลด์วันที่เสร็จสมบูรณ์ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="974fc-142">In the Date completed field, enter a date.</span></span>
34. <span data-ttu-id="974fc-143">เลือก ใช่ ในฟิลด์แผนการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="974fc-143">Select Yes in the Development plan field.</span></span>
35. <span data-ttu-id="974fc-144">ในฟิลด์คำสำคัญ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="974fc-144">In the Keywords field, type a value.</span></span>
36. <span data-ttu-id="974fc-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="974fc-145">Click Save.</span></span>
37. <span data-ttu-id="974fc-146">คลิกแท็บการจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="974fc-146">Click the Ratings tab.</span></span>
    * <span data-ttu-id="974fc-147">รายละเอียดการจัดอันดับ แท็บด่วน ช่วยให้พนักงานสามารถจัดอันดับตนเองและผู้จัดการสามารถจัดอันดับพนักงานได้ </span><span class="sxs-lookup"><span data-stu-id="974fc-147">The rating details FastTab allows employees to rate themselves and the manager to rate the employee.</span></span> <span data-ttu-id="974fc-148">ถ้ามีการใช้น้ำหนัก ค่าน้ำหนักของคะแนนจะถูกคำนวณโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="974fc-148">If weights are used, the weight value of the scores will be calculated automatically.</span></span>    <span data-ttu-id="974fc-149">เมื่อต้องการดูส่วนนี้ ให้เปิดใช้งานการตั้งค่าพารามิเตอร์สำหรับการแสดงการจัดอันดับของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="974fc-149">To see this section, enable the parameter settings for showing employee ratings.</span></span>  
38. <span data-ttu-id="974fc-150">คลิกแท็บการลงชื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="974fc-150">Click the Sign offs tab.</span></span>
    * <span data-ttu-id="974fc-151">ถ้าการตรวจทานใช้ลำดับงาน การลงชื่ออนุมัติจะปรากฏเมื่อลำดับงานเสร็จสมบูรณ์แล้วเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="974fc-151">If the review uses workflow, then the signoffs will appear only after the workflow is complete.</span></span> <span data-ttu-id="974fc-152">ถ้าไม่มีการใช้ลำดับงาน จะแสดงทั้งผู้ปฏิบัติงานและผู้จัดการที่นี่ </span><span class="sxs-lookup"><span data-stu-id="974fc-152">If no workflow is used, then both the worker and the manager are listed here.</span></span> <span data-ttu-id="974fc-153">กล่องกาเครื่องหมายที่บังคับจะถูกเลือกตามการตั้งค่าของชนิดการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="974fc-153">The required check box is selected based on the settings of the review type.</span></span>  
39. <span data-ttu-id="974fc-154">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="974fc-154">Click the General tab.</span></span>
    * <span data-ttu-id="974fc-155">รอบระยะเวลาประสิทธิภาพจะสร้างวันที่เริ่มต้นและวันที่สิ้นสุดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="974fc-155">The performance period creates the default start and end dates.</span></span> <span data-ttu-id="974fc-156">โดยวันที่ดังกล่าวจะสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="974fc-156">Those dates are editable.</span></span>  
    * <span data-ttu-id="974fc-157">สถานะต่างๆ ควบคุมการเข้าถึงเพื่อตรวจทาน </span><span class="sxs-lookup"><span data-stu-id="974fc-157">The statuses control the access to the review.</span></span> <span data-ttu-id="974fc-158">สถานะ ยังไม่เริ่มต้น อนุญาตให้ทุกคนสามารถแก้ไขการตรวจทานได้ </span><span class="sxs-lookup"><span data-stu-id="974fc-158">The Not started status allows everyone to edit the review.</span></span> <span data-ttu-id="974fc-159">สถานะ อยู่ระหว่างดำเนินการ อนุญาตให้เฉพาะพนักงานดูและแก้ไขการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="974fc-159">The In progress status allows only the employee to view and edit the review.</span></span> <span data-ttu-id="974fc-160"> สถานะ พร้อมสำหรับการทบทวน อนุญาตให้เฉพาะผู้จัดการดูและแก้ไขการตรวจทาน </span><span class="sxs-lookup"><span data-stu-id="974fc-160">Ready for review allows only the manager to view and edit the review.</span></span> <span data-ttu-id="974fc-161">สถานะ การทบทวนขั้นสุดท้าย อนุญาตให้ทั้งพนักงานและผู้จัดการสามารถดูการตรวจทาน และแก้ไขได้ถ้าตั้งค่าไว้ในฟิลด์ชนิดการตรวจทาน </span><span class="sxs-lookup"><span data-stu-id="974fc-161">Final review status allows both the employee and manager to view the review and also edit it if set up in the review type.</span></span> <span data-ttu-id="974fc-162">สถานะ เสร็จสมบูรณ์ ถูกปฏิเสธ และยกเลิกแล้ว การตรวจทานจะเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="974fc-162">The Completed, Rejected, and Canceled statuses make the review read-only.</span></span>  
40. <span data-ttu-id="974fc-163">ในฟิลด์ภาพรวม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="974fc-163">In the Overview field, type a value.</span></span>
41. <span data-ttu-id="974fc-164">คลิกแท็บการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="974fc-164">Click the Review tab.</span></span>
    * <span data-ttu-id="974fc-165">เมื่อการตรวจทานเปลี่ยนเป็นสถานะต่างๆ พนักงานและผู้จัดการสามารถเพิ่มข้อคิดเห็นสำหรับแต่ละเป้าหมายหรือความสามารถได้</span><span class="sxs-lookup"><span data-stu-id="974fc-165">As the review moves through the statuses, the employee and manager can add comments for each goal or competency.</span></span>  
42. <span data-ttu-id="974fc-166">คลิกแท็บการลงชื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="974fc-166">Click the Sign offs tab.</span></span>
    * <span data-ttu-id="974fc-167">ผู้ปฏิบัติงานและผู้จัดการสามารถลงชื่ออนุมัติการตรวจทาน </span><span class="sxs-lookup"><span data-stu-id="974fc-167">The worker and manager can sign off on the review.</span></span> <span data-ttu-id="974fc-168">เมื่อการลงชื่ออนุมัติที่จำเป็นทั้งหมดเสร็จสมบูรณ์ สถานะจะเปลี่ยนเป็นเสร็จสมบูรณ์ และจะไม่สามารถเปลี่ยนแปลงเพิ่มเติมได้อีก</span><span class="sxs-lookup"><span data-stu-id="974fc-168">When all required signoffs are complete, the status is changed to Completed and no more changes can be made.</span></span>  


