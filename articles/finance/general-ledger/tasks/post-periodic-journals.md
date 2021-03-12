---
title: ลงรายการบัญชีสมุดรายวันประจำงวด
description: 'สมุดรายวันประจำงวดในบางครั้งจะเรียกว่าสมุดรายวันที่เกิดซ้ำ เนื่องจากยอดเงิน ข้อความ และข้อมูลอื่นๆได้ถูกทำซ้ำแต่ละครั้งที่มีการดึงข้อมูลสมุดรายวันประจำงวด '
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99d157e82f8451e2c8f0bc7946ba30ca48e99add
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968515"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="a5c59-103">ลงรายการบัญชีสมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="a5c59-103">Post periodic journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5c59-104">สมุดรายวันประจำงวดในบางครั้งจะเรียกว่าสมุดรายวันที่เกิดซ้ำ เนื่องจากยอดเงิน ข้อความ และข้อมูลอื่นๆได้ถูกทำซ้ำแต่ละครั้งที่มีการดึงข้อมูลสมุดรายวันประจำงวด </span><span class="sxs-lookup"><span data-stu-id="a5c59-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="a5c59-105">เมื่อคุณสร้างสมุดรายวันประจำงวด คุณระบุช่วงรอบระยะเวลาสำหรับการเกิดซ้ำ เช่น วันหรือเดือน </span><span class="sxs-lookup"><span data-stu-id="a5c59-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="a5c59-106">คำแนะนำของงานนี้จะสร้างสมุดรายวันประจำงวดที่มีการเกิดซ้ำรายเดือน</span><span class="sxs-lookup"><span data-stu-id="a5c59-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="a5c59-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > งานประจำงวด > การบันทึกบัญชีในสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="a5c59-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="a5c59-108">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a5c59-108">Click **New**.</span></span>
3. <span data-ttu-id="a5c59-109">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="a5c59-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="a5c59-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a5c59-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a5c59-111">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a5c59-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="a5c59-112">คำอธิบายจะเป็นชื่อของสมุดรายวันประจำงวดเมื่อดึงข้อมูลในภายหลัง เพื่อตรวจสอบให้แน่ใจว่าได้มีการตั้งชื่อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a5c59-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="a5c59-113">บน **บานหน้าต่างการดำเนินการ** คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="a5c59-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="a5c59-114">โดยทั่วไป สมุดรายวันประจำงวดจะรวมสมุดรายวันหลายรายการไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="a5c59-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="a5c59-115">อย่างไรก็ตาม คู่มืองานนี้จะเพิ่มเพียงแค่รายการเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a5c59-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="a5c59-116">ในฟิลด์ **วันที่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="a5c59-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="a5c59-117">ฟิลด์ **วันที่** ประกอบด้วยวันที่ลงรายการบัญชีสำหรับการโอนย้ายถัดไปในสมุดรายวันประจำวัน</span><span class="sxs-lookup"><span data-stu-id="a5c59-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="a5c59-118">สำหรับสมุดรายวันที่จะมีการดึงมาแต่ละเดือนนั้นควรจะใช้วันที่ในเดือนที่จะลงรายการบัญชี ซึ่งโดยปกติจะเป็นวันแรกหรือวันสุดท้ายในรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="a5c59-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="a5c59-119">คุณสามารถเว้นว่างฟิลด์วันที่และใส่วันที่ที่มีการดึงสมุดรายวันมาโดยใช้ฟิลด์วันที่ว่างเปล่า </span><span class="sxs-lookup"><span data-stu-id="a5c59-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="a5c59-120">ฟิลด์จะถูกอัพเดตโดยอัตโนมัติไปยังวันที่เกิดซ้ำถัดไปเมื่อมีการดึงธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="a5c59-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="a5c59-121">ในฟิลด์ **บัญชี** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a5c59-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="a5c59-122">ในฟิลด์ **รายละเอียด** เลือกค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a5c59-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="a5c59-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a5c59-123">Close the page.</span></span>
11. <span data-ttu-id="a5c59-124">ในฟิลด์ **เดบิต** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a5c59-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="a5c59-125">ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a5c59-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="a5c59-126">ในฟิลด์ **หน่วย** ให้เลือก 'เดือน'</span><span class="sxs-lookup"><span data-stu-id="a5c59-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="a5c59-127">ในฟิลด์ **จำนวนของหน่วย** ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="a5c59-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="a5c59-128">ในฟิลด์ **วันที่ล่าสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="a5c59-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="a5c59-129">การป้อนวันที่ล่าสุดในรอบระยะเวลาก่อนหน้านี้จะป้องกันไม่ให้มีการสร้างสมุดรายวันซ้ำโดยไม่ได้ตั้งใจในรอบระยะเวลาเริ่มต้นที่ไม่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="a5c59-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="a5c59-130">วันที่ล่าสุดจะถูกอัพเดตทุกครั้งในภายหลังที่มีการดึงข้อมูลสมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="a5c59-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="a5c59-131">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a5c59-131">Click **Save**.</span></span>
17. <span data-ttu-id="a5c59-132">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="a5c59-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="a5c59-133">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a5c59-133">Click **New**.</span></span>
19. <span data-ttu-id="a5c59-134">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="a5c59-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="a5c59-135">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a5c59-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="a5c59-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a5c59-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="a5c59-137">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a5c59-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="a5c59-138">บน **บานหน้าต่างการดำเนินการ** คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="a5c59-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="a5c59-139">บน **บานหน้าต่างการดำเนินการ** คลิก **สมุดรายวันเป็นครั้งคราว**</span><span class="sxs-lookup"><span data-stu-id="a5c59-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="a5c59-140">คลิก **ดึงข้อมูลสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="a5c59-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="a5c59-141">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="a5c59-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="a5c59-142">**วันที่สิ้นสุด** ทำหน้าที่เป็นวันตัดยอดสำหรับรายการใบสำคัญประจำงวด</span><span class="sxs-lookup"><span data-stu-id="a5c59-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="a5c59-143">โดยอ้างอิงตามการตั้งค่าการเกิดซ้ำ วันที่ล่าสุดและวันที่สิ้นสุดที่รายการเดียวกันอาจจะถูกนำรวมกันมากกว่าหนึ่งครั้งในสมุดรายวันผลลัพธ์ </span><span class="sxs-lookup"><span data-stu-id="a5c59-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="a5c59-144">วันที่สิ้นสุดจะถูกอัพเดตโดยอัตโนมัติตามวันที่รอบเวลาของรายการประจำงวดถูกโอนย้ายไปสมุดรายวันครั้งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="a5c59-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="a5c59-145">ในฟิลด์ **หมายเลขสมุดรายวันเป็นครั้งคราว** ให้ป้อนหรือเลือกค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a5c59-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="a5c59-146">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a5c59-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="a5c59-147">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a5c59-147">Click **OK**.</span></span> <span data-ttu-id="a5c59-148">สมุดรายวันรอบระยะเวลาในขณะนี้สามารถได้รับการตรวจทาน ได้รับการอนุมัติ หรือได้รับการลงรายการบัญชีขึ้นอยู่กับความต้องการและการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="a5c59-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   
