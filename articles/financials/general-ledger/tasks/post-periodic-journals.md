--- 
title: "ลงรายการบัญชีสมุดรายวันประจำงวด"
description: "สมุดรายวันประจำงวดในบางครั้งจะเรียกว่าสมุดรายวันที่เกิดซ้ำ เนื่องจากยอดเงิน ข้อความ และข้อมูลอื่นๆได้ถูกทำซ้ำแต่ละครั้งที่มีการดึงข้อมูลสมุดรายวันประจำงวด "
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 57b73c43be6ef4dda82cb919d4eb83eeae9c3633
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="0a743-103">ลงรายการบัญชีสมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="0a743-103">Post periodic journals</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a743-104">สมุดรายวันประจำงวดในบางครั้งจะเรียกว่าสมุดรายวันที่เกิดซ้ำ เนื่องจากยอดเงิน ข้อความ และข้อมูลอื่นๆได้ถูกทำซ้ำแต่ละครั้งที่มีการดึงข้อมูลสมุดรายวันประจำงวด </span><span class="sxs-lookup"><span data-stu-id="0a743-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="0a743-105">เมื่อคุณสร้างสมุดรายวันประจำงวด คุณระบุช่วงรอบระยะเวลาสำหรับการเกิดซ้ำ เช่น วันหรือเดือน </span><span class="sxs-lookup"><span data-stu-id="0a743-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="0a743-106">คำแนะนำของงานนี้จะสร้างสมุดรายวันประจำงวดที่มีการเกิดซ้ำรายเดือน</span><span class="sxs-lookup"><span data-stu-id="0a743-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="0a743-107">ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > สมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="0a743-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="0a743-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0a743-108">Click New.</span></span>
3. <span data-ttu-id="0a743-109">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0a743-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="0a743-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0a743-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0a743-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0a743-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0a743-112">คำอธิบายจะเป็นชื่อของสมุดรายวันประจำงวดเมื่อดึงข้อมูลในภายหลัง เพื่อตรวจสอบให้แน่ใจว่าได้มีการตั้งชื่อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0a743-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="0a743-113">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="0a743-113">Click Lines.</span></span>
    * <span data-ttu-id="0a743-114">โดยทั่วไป สมุดรายวันประจำงวดจะรวมสมุดรายวันหลายรายการไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="0a743-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="0a743-115">อย่างไรก็ตาม คู่มืองานนี้จะเพิ่มเพียงแค่รายการเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0a743-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="0a743-116">ในฟิลด์วันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0a743-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="0a743-117">ฟิลด์วันที่ประกอบด้วย วันที่ลงรายการบัญชีสำหรับการโอนย้ายถัดไปในสมุดรายวันประจำวัน </span><span class="sxs-lookup"><span data-stu-id="0a743-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="0a743-118">สำหรับสมุดรายวันที่จะมีการดึงมาแต่ละเดือนนั้นควรจะใช้วันที่ในเดือนที่จะลงรายการบัญชี ซึ่งโดยปกติจะเป็นวันแรกหรือวันสุดท้ายในรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="0a743-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="0a743-119">คุณสามารถเว้นว่างฟิลด์วันที่และใส่วันที่ที่มีการดึงสมุดรายวันมาโดยใช้ฟิลด์วันที่ว่างเปล่า </span><span class="sxs-lookup"><span data-stu-id="0a743-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="0a743-120">ฟิลด์จะถูกอัพเดตโดยอัตโนมัติไปยังวันที่เกิดซ้ำถัดไปเมื่อมีการดึงธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0a743-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="0a743-121">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0a743-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="0a743-122">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0a743-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="0a743-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0a743-123">Close the page.</span></span>
11. <span data-ttu-id="0a743-124">ในฟิลด์เดบิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0a743-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="0a743-125">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0a743-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="0a743-126">ในฟิลด์หน่วย ให้เลือกเดือน</span><span class="sxs-lookup"><span data-stu-id="0a743-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="0a743-127">ในหมายเลขของฟิลด์หน่วย ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="0a743-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="0a743-128">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0a743-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="0a743-129">การป้อนวันที่ล่าสุดในรอบระยะเวลาก่อนหน้านี้จะป้องกันไม่ให้มีการสร้างสมุดรายวันซ้ำโดยไม่ได้ตั้งใจในรอบระยะเวลาเริ่มต้นที่ไม่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="0a743-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="0a743-130">วันที่ล่าสุดจะถูกอัพเดตทุกครั้งในภายหลังที่มีการดึงข้อมูลสมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="0a743-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="0a743-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0a743-131">Click Save.</span></span>
17. <span data-ttu-id="0a743-132">ไปที่แดชบอร์ดเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="0a743-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="0a743-133">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0a743-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="0a743-134">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0a743-134">Click New.</span></span>
20. <span data-ttu-id="0a743-135">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0a743-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="0a743-136">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0a743-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="0a743-137">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0a743-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="0a743-138">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0a743-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="0a743-139">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="0a743-139">Click Lines.</span></span>
25. <span data-ttu-id="0a743-140">คลิกที่สมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="0a743-140">Click Period journal.</span></span>
26. <span data-ttu-id="0a743-141">คลิกที่ดึงข้อมูลสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="0a743-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="0a743-142">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0a743-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0a743-143">วันที่สิ้นสุดทำหน้าที่เป็นวันตัดยอดสำหรับรายการใบสำคัญประจำงวด </span><span class="sxs-lookup"><span data-stu-id="0a743-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="0a743-144">โดยอ้างอิงตามการตั้งค่าการเกิดซ้ำ วันที่ล่าสุดและวันที่สิ้นสุดที่รายการเดียวกันอาจจะถูกนำรวมกันมากกว่าหนึ่งครั้งในสมุดรายวันผลลัพธ์ </span><span class="sxs-lookup"><span data-stu-id="0a743-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="0a743-145">วันที่สิ้นสุดจะถูกอัพเดตโดยอัตโนมัติตามวันที่รอบเวลาของรายการประจำงวดถูกโอนย้ายไปสมุดรายวันครั้งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="0a743-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="0a743-146">ในฟิลด์หมายเลขสมุดรายวันประจำงวด ให้ป้อนหรือเลือกค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0a743-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="0a743-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0a743-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="0a743-148">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0a743-148">Click OK.</span></span>
    * <span data-ttu-id="0a743-149">สมุดรายวันรอบระยะเวลาในขณะนี้สามารถได้รับการตรวจทาน ได้รับการอนุมัติ หรือได้รับการลงรายการบัญชีขึ้นอยู่กับความต้องการและการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="0a743-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


