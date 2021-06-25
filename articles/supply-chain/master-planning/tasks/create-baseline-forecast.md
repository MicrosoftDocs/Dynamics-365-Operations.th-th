---
title: 'คู่มือ: สร้างการคาดการณ์พื้นฐาน'
description: 'ผู้วางแผนการผลิตสามารถสร้างการคาดการณ์พื้นฐาน โดยใช้แบบจำลองการคาดการณ์อนุกรมเวลา หรือ โดยการคัดลอกประวัติความต้องการ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223973"
---
# <a name="guide-create-a-baseline-forecast"></a><span data-ttu-id="5cc15-103">คู่มือ: สร้างการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="5cc15-103">Guide: Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5cc15-104">ผู้วางแผนการผลิตสามารถสร้างการคาดการณ์พื้นฐาน โดยใช้แบบจำลองการคาดการณ์อนุกรมเวลา หรือ โดยการคัดลอกประวัติความต้องการ </span><span class="sxs-lookup"><span data-stu-id="5cc15-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="5cc15-105">กระบวนงานนี้แสดงวิธีการคัดลอกความต้องการในอดีตเพื่อสร้างการคาดการณ์พื้นฐานสำหรับผลิตภัณฑ์ทั้งหมดโดยใช้คีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="5cc15-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span>

## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="5cc15-106">การตั้งค่าคีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="5cc15-106">Set up an item allocation key</span></span>

1. <span data-ttu-id="5cc15-107">ไปที่ **การวางแผนหลัก > การตั้งค่า > กลุ่มการวางแผนระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="5cc15-107">Go to **Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="5cc15-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="5cc15-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5cc15-109">ตัวอย่างเช่น กรองในฟิลด์ *ชื่อ* ด้วยค่า *10*</span><span class="sxs-lookup"><span data-stu-id="5cc15-109">For example, filter on the *Name* field with a value of *10*.</span></span>
    * <span data-ttu-id="5cc15-110">การคาดการณ์ความต้องการรันระหว่างนิติบุคคล </span><span class="sxs-lookup"><span data-stu-id="5cc15-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="5cc15-111">นั่นคือเหตุผลที่คุณต้องตั้งค่าบริษัททั้งหมดที่คุณต้องการสร้างการคาดการณ์ในระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="5cc15-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="5cc15-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5cc15-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5cc15-113">เลือก **คีย์การปันส่วนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="5cc15-113">Select **Item allocation keys**.</span></span>
    * <span data-ttu-id="5cc15-114">เลือกคีย์การปันส่วนสินค้าทั้งหมดที่คุณต้องการสร้างการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="5cc15-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="5cc15-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5cc15-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5cc15-116">เลือกคีย์การปันส่วนสินค้า D_Aloc </span><span class="sxs-lookup"><span data-stu-id="5cc15-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="5cc15-117">เลือก **>**</span><span class="sxs-lookup"><span data-stu-id="5cc15-117">Select **>**.</span></span>
7. <span data-ttu-id="5cc15-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5cc15-118">Close the page.</span></span>
8. <span data-ttu-id="5cc15-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5cc15-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="5cc15-120">ตั้งค่าพารามิเตอร์การคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="5cc15-120">Set up the demand forecasting parameters</span></span>

1. <span data-ttu-id="5cc15-121">ไปที่ **การวางแผนหลัก >การตั้งค่า > การคาดการณ์ความต้องการ > พารามิเตอร์การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="5cc15-121">Go to **Master planning > Setup > Demand forecasting > Demand forecasting parameters**.</span></span>
2. <span data-ttu-id="5cc15-122">ขยายส่วน **พารามิเตอร์อัลกอริทึมการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="5cc15-122">Expand the **Forecast algorithm parameters** section.</span></span>
3. <span data-ttu-id="5cc15-123">ในฟิลด์ **กลยุทธ์การสร้างการคาดการณ์** เลือก **คัดลอกความต้องการในอดีต**</span><span class="sxs-lookup"><span data-stu-id="5cc15-123">In the **Forecast generation strategy** field, select **Copy over historical demand**.</span></span>
4. <span data-ttu-id="5cc15-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5cc15-124">Select **Save**.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="5cc15-125">สร้างการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="5cc15-125">Create a baseline forecast</span></span>

1. <span data-ttu-id="5cc15-126">ไปที่ **การวางแผนหลัก > การคาดการณ์ > การคาดการณ์ความต้องการ > การสร้างการคาดการณ์พื้นฐานทางสถิติ**</span><span class="sxs-lookup"><span data-stu-id="5cc15-126">Go to **Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast**.</span></span>
2. <span data-ttu-id="5cc15-127">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5cc15-127">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5cc15-128">ถ้าคุณมีใบสั่งขายที่เริ่มต้นจากวันที่ 1 มกราคม 2015 ให้ป้อนวันที่นี้ </span><span class="sxs-lookup"><span data-stu-id="5cc15-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="5cc15-129">ถ้าหากคุณไม่มี ให้ป้อนวันที่แรกสุดของใบสั่งขายของคุณ</span><span class="sxs-lookup"><span data-stu-id="5cc15-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="5cc15-130">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5cc15-130">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="5cc15-131">ป้อนวันที่ล่าสุดของใบสั่งขายของคุณ ตัวอย่างเช่น *2015-03-31*</span><span class="sxs-lookup"><span data-stu-id="5cc15-131">Enter the last date of your sales orders, for example *2015-03-31*.</span></span>  
4. <span data-ttu-id="5cc15-132">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5cc15-132">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5cc15-133">ป้อน *2015-04-01*</span><span class="sxs-lookup"><span data-stu-id="5cc15-133">Enter *2015-04-01*.</span></span> <span data-ttu-id="5cc15-134">วันที่นี้จะสามารถคำนวณโดยอัตโนมัติเหมือนเป็นวันเริ่มต้นของกลุ่มการคาดการณ์กลุ่มถัดไป </span><span class="sxs-lookup"><span data-stu-id="5cc15-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="5cc15-135">ขยายส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="5cc15-135">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="5cc15-136">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="5cc15-136">Select **Filter**.</span></span>
7. <span data-ttu-id="5cc15-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5cc15-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5cc15-138">ทำเครื่องหมายในแถวที่ **ฟิลด์** = *กลุ่มการวางแผนระหว่างบริษัท*</span><span class="sxs-lookup"><span data-stu-id="5cc15-138">Mark the row where **Field** = *Intercompany planning group*.</span></span>  
8. <span data-ttu-id="5cc15-139">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5cc15-139">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="5cc15-140">พิมพ์กลุ่มการวางแผนระหว่างบริษัท (ตัวอย่างเช่น *10*) ที่คุณใช้ในงานแรก</span><span class="sxs-lookup"><span data-stu-id="5cc15-140">Type the intercompany planning group (for example, *10*) that you used in the first task.</span></span>  
9. <span data-ttu-id="5cc15-141">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5cc15-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5cc15-142">เลือกแถวที่ **ฟิลด์** = *คีย์การปันส่วนสินค้า*</span><span class="sxs-lookup"><span data-stu-id="5cc15-142">Select the row where **Field** = *Item allocation key*.</span></span>  
10. <span data-ttu-id="5cc15-143">ในฟิลด์ **เงื่อนไข** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5cc15-143">In the **Criteria** field, type a value.</span></span>
11. <span data-ttu-id="5cc15-144">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5cc15-144">Select **OK**.</span></span>
12. <span data-ttu-id="5cc15-145">ขยายส่วน **พารามิเตอร์ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="5cc15-145">Expand the **Advanced parameters** section.</span></span>
13. <span data-ttu-id="5cc15-146">ในฟิลด์ **กลุ่มการคาดการณ์** เลือก *เดือน*</span><span class="sxs-lookup"><span data-stu-id="5cc15-146">In the **Forecast bucket** field, select *Month*.</span></span>
14. <span data-ttu-id="5cc15-147">ในฟิลด์ **ระดับการคาดการณ์** ให้ป้อน *3*</span><span class="sxs-lookup"><span data-stu-id="5cc15-147">In the **Forecast horizon** field, enter *3*.</span></span>
15. <span data-ttu-id="5cc15-148">ในฟิลด์ **กรอบการหยุดเวลา** ให้ป้อน *1*</span><span class="sxs-lookup"><span data-stu-id="5cc15-148">In the **Freeze time fence** field, enter *1*.</span></span>
16. <span data-ttu-id="5cc15-149">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5cc15-149">Select **OK**.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="5cc15-150">แสดงการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="5cc15-150">Visualize the demand forecast</span></span>

1. <span data-ttu-id="5cc15-151">ไปที่ **การวางแผนหลัก > การคาดการณ์ > การคาดการณ์ความต้องการ > การคาดการณ์ความต้องการที่ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="5cc15-151">Go to **Master planning > Forecasting > Demand forecasting > Adjusted demand forecast**.</span></span>
2. <span data-ttu-id="5cc15-152">ในตาราง มุมมองแบบรวม ให้เลือกเซลล์ในแถว 1 , คอลัมน์ 2</span><span class="sxs-lookup"><span data-stu-id="5cc15-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="5cc15-153">นี่คือเดือนที่สองที่คุณได้สร้างการคาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="5cc15-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="5cc15-154">ตั้งค่า **เซลล์ปริมาณ** เป็น *400*</span><span class="sxs-lookup"><span data-stu-id="5cc15-154">Set **QtyCell** to *400*.</span></span>
    * <span data-ttu-id="5cc15-155">ในเซลล์ ป้อนหมายเลขที่แตกต่างกันจากหมายเลขที่มีการคาดการณ์ ตัวอย่างเช่น 400</span><span class="sxs-lookup"><span data-stu-id="5cc15-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="5cc15-156">คุณได้ทำการปรับปรุงการคาดการณ์ด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="5cc15-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="5cc15-157">โปรดสังเกตการบ่งชี้ที่แสดงเป็นรูปภาพในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5cc15-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="5cc15-158">เลือก **รายละเอียดรายการการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="5cc15-158">Select **Forecast line details**.</span></span>
    * <span data-ttu-id="5cc15-159">ในหน้านี้ คุณสามารถดูค่าความถูกต้อง ความต้องการในอดีต และการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="5cc15-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="5cc15-160">คุณสามารถทำการเปลี่ยนแปลงการคาดการณ์ได้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="5cc15-160">You can make changes to the forecast as well.</span></span>  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]