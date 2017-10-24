--- 
title: "การตั้งค่าโพรไฟล์การลงบัญชีสินทรัพย์ถาวร"
description: "คำแนะนำของงานนี้จะตั้งค่าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร "
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="41efc-103">การตั้งค่าโพรไฟล์การลงบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="41efc-103">Set up fixed asset posting profiles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41efc-104">คำแนะนำของงานนี้จะตั้งค่าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="41efc-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="41efc-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="41efc-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="41efc-106">ตัวอย่างที่ให้ในคำแนะนำในงานนี้คือโพรไฟล์การลงรายการบัญชีพื้นฐาน อย่างไรก็ตาม ต้องมีการสร้างการลงโพรไฟล์สำหรับแผนภูมิบัญชีที่เฉพาะเจาะจงและข้อกำหนดการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="41efc-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="41efc-107">ไปที่สินทรัพย์ถาวร > การติดตั้ง > โพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="41efc-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="41efc-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="41efc-108">Click New.</span></span>
3. <span data-ttu-id="41efc-109">ในฟิลด์โพรไฟล์การลงรายการบัญชี ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="41efc-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="41efc-111">คุณจะต้องสร้างโพรไฟล์การลงรายการบัญชีสำหรับธุรกรรมสินทรัพย์ถาวรแต่ละชนิดที่คุณต้องใช้เมื่อทำงานกับสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="41efc-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="41efc-112">คู่มือของงานนี้จะเริ่มด้วยธุรกรรมการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="41efc-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="41efc-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-113">Click Add.</span></span>
6. <span data-ttu-id="41efc-114">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="41efc-115">ฟิลด์การจัดกลุ่มช่วยให้คุณสามารถกำหนดโพรไฟล์การลงรายการบัญชีไปยังตาราง (บัญชีหนึ่งบัญชีตั้งค่าสำหรับสินทรัพย์ถาวรแต่ละรายการ) หรือกลุ่ม (บัญชีหนึ่งบัญชีตั้งค่าสำหรับสินทรัพย์ถาวรแต่ละรายการ)</span><span class="sxs-lookup"><span data-stu-id="41efc-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="41efc-116">สำหรับคู่มืองานนี้ ฉันจะทิ้งชุดค่าเป็น "ทั้งหมด" เพื่อนำไปใช้กับสินทรัพย์ทั้งหมดที่มีสมุดบัญชีที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="41efc-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="41efc-117">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="41efc-118">สำหรับการซื้อสินทรัพย์ คุณสามารถป้อนบัญชีตรงข้าม หรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="41efc-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="41efc-119">ในฟิลด์ชนิดของธุรกรรม เลือก 'การปรับปรุงการซื้อสินทรัพย์'</span><span class="sxs-lookup"><span data-stu-id="41efc-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="41efc-120">สำหรับธุรกรรมการปรับปรุงการซื้อสินทรัพย์ เราจะใช้บัญชีเดียวกันกับที่ใช้สำหรับธุรกรรมการซื้อสิ้นทรัพย์</span><span class="sxs-lookup"><span data-stu-id="41efc-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="41efc-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-121">Click Add.</span></span>
10. <span data-ttu-id="41efc-122">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="41efc-123">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="41efc-124">สำหรับการปรับปรุงการซื้อสินทรัพย์ คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="41efc-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="41efc-125">ในฟิลด์ของชนิดธุรกรรม เลือก 'ค่าเสื่อมราคา'</span><span class="sxs-lookup"><span data-stu-id="41efc-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="41efc-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-126">Click Add.</span></span>
14. <span data-ttu-id="41efc-127">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="41efc-128">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="41efc-129">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="41efc-130">ในฟิลด์ของชนิดธุรกรรม เลือก 'การปรับปรุงค่าเสื่อมราคา'</span><span class="sxs-lookup"><span data-stu-id="41efc-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="41efc-131">สำหรับธุรกรรมการปรับปรุงค่าเสื่อมราคา เราจะใช้บัญชีเดียวกันกับที่ใช้สำหรับธุรกรรมค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="41efc-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="41efc-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-132">Click Add.</span></span>
19. <span data-ttu-id="41efc-133">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="41efc-134">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="41efc-135">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="41efc-136">ในฟิลด์ของชนิดธุรกรรม เลือก 'การตัดจำหน่าย - การขาย'</span><span class="sxs-lookup"><span data-stu-id="41efc-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="41efc-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-137">Click Add.</span></span>
24. <span data-ttu-id="41efc-138">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="41efc-139">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="41efc-140">สำหรับตัดจำหน่าย คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="41efc-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="41efc-141">ในฟิลด์ของชนิดธุรกรรม เลือก 'การตัดจำหน่าย - เศษซาก'</span><span class="sxs-lookup"><span data-stu-id="41efc-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="41efc-142">เราจะใช้บัญชีเดียวกันสำหรับการขายการตัดจำหน่ายและเศษการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41efc-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="41efc-143">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-143">Click Add.</span></span>
28. <span data-ttu-id="41efc-144">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="41efc-145">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="41efc-146">สำหรับตัดจำหน่าย คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="41efc-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="41efc-147">ขยายส่วนการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41efc-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="41efc-148">คุณต้องตั้งค่าโพรไฟล์การลงรายการบัญชีการตัดจำหน่าย สำหรับทั้งการขายและเศษซาก</span><span class="sxs-lookup"><span data-stu-id="41efc-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="41efc-149">เราจะเริ่มต้นด้วยธุรกรรมการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="41efc-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="41efc-150">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-150">Click Add.</span></span>
32. <span data-ttu-id="41efc-151">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="41efc-152">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าการซื้อสินทรัพย์'</span><span class="sxs-lookup"><span data-stu-id="41efc-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="41efc-153">มูลค่าการซื้อสินทรัพย์จะระบุค่าการซื้อสินทรัพย์และการปรับปรุงการซื้อสินทรัพย์สำหรับทั้งปี </span><span class="sxs-lookup"><span data-stu-id="41efc-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="41efc-154">นอกจากนี้คุณยังสามารถกำหนดบัญชีสำหรับชนิดธุรกรรมเหล่านี้แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="41efc-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="41efc-155">คุณสามารถตั้งค่ากระบวนการตัดจำหน่ายให้ใช้บัญชีที่แตกต่างกัน โดยขึ้นอยู่กับว่าผลการตัดจำหน่ายเป็นกำไรหรือขาดทุน </span><span class="sxs-lookup"><span data-stu-id="41efc-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="41efc-156">ฉันจะตั้งค่าชนิดมูลค่าการขายเป็น "ทั้งหมด" เพื่อใช้บัญชีเดียวกันสำหรับการตัดจำหน่ายทุกชนิด</span><span class="sxs-lookup"><span data-stu-id="41efc-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="41efc-157">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="41efc-158">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="41efc-159">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-159">Click Add.</span></span>
37. <span data-ttu-id="41efc-160">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="41efc-161">ในฟิลด์ค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="41efc-162">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="41efc-163">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="41efc-164">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-164">Click Add.</span></span>
41. <span data-ttu-id="41efc-165">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="41efc-166">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="41efc-167">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="41efc-168">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="41efc-169">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-169">Click Add.</span></span>
46. <span data-ttu-id="41efc-170">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="41efc-171">ในฟิลด์มูลค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="41efc-172">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="41efc-173">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="41efc-174">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-174">Click Add.</span></span>
51. <span data-ttu-id="41efc-175">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="41efc-176">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'การปรับปรุงค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="41efc-177">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="41efc-178">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="41efc-179">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-179">Click Add.</span></span>
56. <span data-ttu-id="41efc-180">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="41efc-181">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'มูลค่าตามบัญชีสุทธิ'</span><span class="sxs-lookup"><span data-stu-id="41efc-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="41efc-182">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="41efc-183">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="41efc-184">ในฟิลด์การขายหรือเศษซาก เลือก 'เศษซาก'</span><span class="sxs-lookup"><span data-stu-id="41efc-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="41efc-185">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-185">Click Add.</span></span>
62. <span data-ttu-id="41efc-186">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="41efc-187">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าการซื้อสินทรัพย์'</span><span class="sxs-lookup"><span data-stu-id="41efc-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="41efc-188">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="41efc-189">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="41efc-190">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-190">Click Add.</span></span>
67. <span data-ttu-id="41efc-191">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="41efc-192">ในฟิลด์ค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="41efc-193">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="41efc-194">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="41efc-195">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-195">Click Add.</span></span>
71. <span data-ttu-id="41efc-196">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="41efc-197">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="41efc-198">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="41efc-199">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="41efc-200">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-200">Click Add.</span></span>
76. <span data-ttu-id="41efc-201">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="41efc-202">ในฟิลด์มูลค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="41efc-203">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="41efc-204">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="41efc-205">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-205">Click Add.</span></span>
81. <span data-ttu-id="41efc-206">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="41efc-207">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'การปรับปรุงค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="41efc-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="41efc-208">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="41efc-209">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="41efc-210">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="41efc-210">Click Add.</span></span>
86. <span data-ttu-id="41efc-211">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="41efc-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="41efc-212">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'มูลค่าตามบัญชีสุทธิ'</span><span class="sxs-lookup"><span data-stu-id="41efc-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="41efc-213">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="41efc-214">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="41efc-214">In the Offset account field, specify the desired values.</span></span>


