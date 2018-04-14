--- 
title: "สร้างการคาดการณ์พื้นฐาน"
description: "ผู้วางแผนการผลิตสามารถสร้างการคาดการณ์พื้นฐาน โดยใช้แบบจำลองการคาดการณ์อนุกรมเวลา หรือ โดยการคัดลอกประวัติความต้องการ "
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef11f3779fc94fa95f082893f6863dde8d8c921e
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="e967f-103">สร้างการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="e967f-103">Create a baseline forecast</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e967f-104">ผู้วางแผนการผลิตสามารถสร้างการคาดการณ์พื้นฐาน โดยใช้แบบจำลองการคาดการณ์อนุกรมเวลา หรือ โดยการคัดลอกประวัติความต้องการ </span><span class="sxs-lookup"><span data-stu-id="e967f-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="e967f-105">กระบวนงานนี้แสดงวิธีการคัดลอกความต้องการในอดีตเพื่อสร้างการคาดการณ์พื้นฐานสำหรับผลิตภัณฑ์ทั้งหมดโดยใช้คีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="e967f-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="e967f-106">การตั้งค่าคีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="e967f-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="e967f-107">ไปที่ การวางแผนหลัก > การตั้งค่า > กลุ่มการวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="e967f-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="e967f-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="e967f-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e967f-109">เช่น กรองข้อมูลในฟิลด์รายชื่อด้วยค่า 10</span><span class="sxs-lookup"><span data-stu-id="e967f-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="e967f-110">การคาดการณ์ความต้องการรันระหว่างนิติบุคคล </span><span class="sxs-lookup"><span data-stu-id="e967f-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="e967f-111">นั่นคือเหตุผลที่คุณต้องตั้งค่าบริษัททั้งหมดที่คุณต้องการสร้างการคาดการณ์ในระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="e967f-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="e967f-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e967f-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e967f-113">คลิก คีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="e967f-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="e967f-114">เลือกคีย์การปันส่วนสินค้าทั้งหมดที่คุณต้องการสร้างการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="e967f-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="e967f-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e967f-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e967f-116">เลือกคีย์การปันส่วนสินค้า D_Aloc </span><span class="sxs-lookup"><span data-stu-id="e967f-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="e967f-117">คลิก ></span><span class="sxs-lookup"><span data-stu-id="e967f-117">Click >.</span></span>
7. <span data-ttu-id="e967f-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e967f-118">Close the page.</span></span>
8. <span data-ttu-id="e967f-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e967f-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="e967f-120">ตั้งค่าพารามิเตอร์การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="e967f-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="e967f-121">ไปที่ การวางแผนหลัก >การตั้งค่า > การคาดการณ์ความต้องการ > พารามิเตอร์การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="e967f-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="e967f-122">ขยายส่วนพารามิเตอร์อัลกอริทึมการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="e967f-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="e967f-123">ในฟิลด์กลยุทธ์การสร้างการคาดการณ์ เลือก 'คัดลอกความต้องการในอดีต' </span><span class="sxs-lookup"><span data-stu-id="e967f-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="e967f-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e967f-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="e967f-125">สร้างการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="e967f-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="e967f-126">ไปที่ การวางแผนหลัก > การคาดการณ์ > การคาดการณ์ความต้องการ > การสร้างการคาดการณ์พื้นฐานทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="e967f-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="e967f-127">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e967f-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="e967f-128">ถ้าคุณมีใบสั่งขายที่เริ่มต้นจากวันที่ 1 มกราคม 2015 ให้ป้อนวันที่นี้ </span><span class="sxs-lookup"><span data-stu-id="e967f-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="e967f-129">ถ้าหากคุณไม่มี ให้ป้อนวันที่แรกสุดของใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="e967f-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="e967f-130">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e967f-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e967f-131">ป้อนวันที่ล่าสุดของใบสั่งขายของคุณ ตัวอย่างเช่น 31 มีนาคม 2015</span><span class="sxs-lookup"><span data-stu-id="e967f-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="e967f-132">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e967f-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="e967f-133">ป้อน 1 เมษายน 2015 </span><span class="sxs-lookup"><span data-stu-id="e967f-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="e967f-134">วันที่นี้จะสามารถคำนวณโดยอัตโนมัติเหมือนเป็นวันเริ่มต้นของกลุ่มการคาดการณ์กลุ่มถัดไป </span><span class="sxs-lookup"><span data-stu-id="e967f-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="e967f-135">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="e967f-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="e967f-136">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="e967f-136">Click Filter.</span></span>
7. <span data-ttu-id="e967f-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e967f-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e967f-138">ทำเครื่องหมายในฟิลด์แถว = กลุ่มการวางแผนระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="e967f-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="e967f-139">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="e967f-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e967f-140">พิมพ์กลุ่มการวางแผนระหว่างบริษัท ตัวอย่างเช่น 10 ที่คุณใช้ในงานแรก</span><span class="sxs-lookup"><span data-stu-id="e967f-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="e967f-141">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e967f-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e967f-142">เลือกฟิลด์แถว = คีย์การปันส่วนสินค้า </span><span class="sxs-lookup"><span data-stu-id="e967f-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="e967f-143">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="e967f-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="e967f-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e967f-144">Click OK.</span></span>
12. <span data-ttu-id="e967f-145">ขยายส่วนพารามิเตอร์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e967f-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="e967f-146">ในฟิลด์กลุ่มการคาดการณ์ เลือก 'เดือน'</span><span class="sxs-lookup"><span data-stu-id="e967f-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="e967f-147">ในฟิลด์ระดับการคาดการณ์ ให้ป้อน '3'</span><span class="sxs-lookup"><span data-stu-id="e967f-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="e967f-148">ในฟิลด์กรอบการหยุดเวลา ให้ป้อน '1'</span><span class="sxs-lookup"><span data-stu-id="e967f-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="e967f-149">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e967f-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="e967f-150">แสดงการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="e967f-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="e967f-151">ไปที่ การวางแผนหลัก > การคาดการณ์ > การคาดการณ์ความต้องการ > การคาดการณ์ความต้องการที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="e967f-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="e967f-152">ในตาราง มุมมองแบบรวม ให้เลือกเซลล์ในแถว 1 , คอลัมน์ 2</span><span class="sxs-lookup"><span data-stu-id="e967f-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="e967f-153">นี่คือเดือนที่สองที่คุณได้สร้างการคาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="e967f-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="e967f-154">ตั้งค่าเซลล์ปริมาณ เป็น '400'</span><span class="sxs-lookup"><span data-stu-id="e967f-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="e967f-155">ในเซลล์ ป้อนหมายเลขที่แตกต่างกันจากหมายเลขที่มีการคาดการณ์ ตัวอย่างเช่น 400</span><span class="sxs-lookup"><span data-stu-id="e967f-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="e967f-156">คุณได้ทำการปรับปรุงการคาดการณ์ด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="e967f-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="e967f-157">โปรดสังเกตการบ่งชี้ที่แสดงเป็นรูปภาพในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e967f-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="e967f-158">คลิก รายละเอียดรายการการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="e967f-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="e967f-159">ในหน้านี้ คุณสามารถดูค่าความถูกต้อง ความต้องการในอดีต และการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="e967f-159">On this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="e967f-160">คุณสามารถทำการเปลี่ยนแปลงการคาดการณ์ได้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="e967f-160">You can make changes to the forecast as well.</span></span>  


