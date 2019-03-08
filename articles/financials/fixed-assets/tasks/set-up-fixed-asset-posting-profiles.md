---
title: การตั้งค่าโพรไฟล์การลงบัญชีสินทรัพย์ถาวร
description: 'คำแนะนำของงานนี้จะตั้งค่าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร '
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "351113"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="1eb66-103">การตั้งค่าโพรไฟล์การลงบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="1eb66-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1eb66-104">คำแนะนำของงานนี้จะตั้งค่าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="1eb66-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="1eb66-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="1eb66-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="1eb66-106">ตัวอย่างที่ให้ในคำแนะนำในงานนี้คือโพรไฟล์การลงรายการบัญชีพื้นฐาน อย่างไรก็ตาม ต้องมีการสร้างการลงโพรไฟล์สำหรับแผนภูมิบัญชีที่เฉพาะเจาะจงและข้อกำหนดการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="1eb66-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="1eb66-107">ไปที่สินทรัพย์ถาวร > การติดตั้ง > โพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="1eb66-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="1eb66-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1eb66-108">Click New.</span></span>
3. <span data-ttu-id="1eb66-109">ในฟิลด์โพรไฟล์การลงรายการบัญชี ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="1eb66-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1eb66-111">คุณจะต้องสร้างโพรไฟล์การลงรายการบัญชีสำหรับธุรกรรมสินทรัพย์ถาวรแต่ละชนิดที่คุณต้องใช้เมื่อทำงานกับสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="1eb66-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="1eb66-112">คู่มือของงานนี้จะเริ่มด้วยธุรกรรมการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1eb66-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="1eb66-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-113">Click Add.</span></span>
6. <span data-ttu-id="1eb66-114">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="1eb66-115">ฟิลด์การจัดกลุ่มช่วยให้คุณสามารถกำหนดโพรไฟล์การลงรายการบัญชีไปยังตาราง (บัญชีหนึ่งบัญชีตั้งค่าสำหรับสินทรัพย์ถาวรแต่ละรายการ) หรือกลุ่ม (บัญชีหนึ่งบัญชีตั้งค่าสำหรับสินทรัพย์ถาวรแต่ละรายการ)</span><span class="sxs-lookup"><span data-stu-id="1eb66-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="1eb66-116">สำหรับคู่มืองานนี้ ฉันจะทิ้งชุดค่าเป็น "ทั้งหมด" เพื่อนำไปใช้กับสินทรัพย์ทั้งหมดที่มีสมุดบัญชีที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1eb66-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="1eb66-117">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1eb66-118">สำหรับการซื้อสินทรัพย์ คุณสามารถป้อนบัญชีตรงข้าม หรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="1eb66-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="1eb66-119">ในฟิลด์ชนิดของธุรกรรม เลือก 'การปรับปรุงการซื้อสินทรัพย์'</span><span class="sxs-lookup"><span data-stu-id="1eb66-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="1eb66-120">สำหรับธุรกรรมการปรับปรุงการซื้อสินทรัพย์ เราจะใช้บัญชีเดียวกันกับที่ใช้สำหรับธุรกรรมการซื้อสิ้นทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1eb66-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="1eb66-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-121">Click Add.</span></span>
10. <span data-ttu-id="1eb66-122">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="1eb66-123">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1eb66-124">สำหรับการปรับปรุงการซื้อสินทรัพย์ คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="1eb66-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="1eb66-125">ในฟิลด์ของชนิดธุรกรรม เลือก 'ค่าเสื่อมราคา'</span><span class="sxs-lookup"><span data-stu-id="1eb66-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="1eb66-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-126">Click Add.</span></span>
14. <span data-ttu-id="1eb66-127">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="1eb66-128">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="1eb66-129">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="1eb66-130">ในฟิลด์ของชนิดธุรกรรม เลือก 'การปรับปรุงค่าเสื่อมราคา'</span><span class="sxs-lookup"><span data-stu-id="1eb66-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="1eb66-131">สำหรับธุรกรรมการปรับปรุงค่าเสื่อมราคา เราจะใช้บัญชีเดียวกันกับที่ใช้สำหรับธุรกรรมค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1eb66-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="1eb66-132">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-132">Click Add.</span></span>
19. <span data-ttu-id="1eb66-133">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="1eb66-134">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="1eb66-135">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="1eb66-136">ในฟิลด์ของชนิดธุรกรรม เลือก 'การตัดจำหน่าย - การขาย'</span><span class="sxs-lookup"><span data-stu-id="1eb66-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="1eb66-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-137">Click Add.</span></span>
24. <span data-ttu-id="1eb66-138">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="1eb66-139">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1eb66-140">สำหรับตัดจำหน่าย คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="1eb66-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="1eb66-141">ในฟิลด์ของชนิดธุรกรรม เลือก 'การตัดจำหน่าย - เศษซาก'</span><span class="sxs-lookup"><span data-stu-id="1eb66-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="1eb66-142">เราจะใช้บัญชีเดียวกันสำหรับการขายการตัดจำหน่ายและเศษการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="1eb66-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="1eb66-143">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-143">Click Add.</span></span>
28. <span data-ttu-id="1eb66-144">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="1eb66-145">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1eb66-146">สำหรับตัดจำหน่าย คุณสามารถป้อนบัญชีตรงข้ามหรือปล่อยว่างต้องได้รับการกรอกข้อมูลสำหรับธุรกรรมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="1eb66-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="1eb66-147">ขยายส่วนการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="1eb66-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="1eb66-148">คุณต้องตั้งค่าโพรไฟล์การลงรายการบัญชีการตัดจำหน่าย สำหรับทั้งการขายและเศษซาก</span><span class="sxs-lookup"><span data-stu-id="1eb66-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="1eb66-149">เราจะเริ่มต้นด้วยธุรกรรมการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="1eb66-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="1eb66-150">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-150">Click Add.</span></span>
32. <span data-ttu-id="1eb66-151">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="1eb66-152">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าการซื้อสินทรัพย์'</span><span class="sxs-lookup"><span data-stu-id="1eb66-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="1eb66-153">มูลค่าการซื้อสินทรัพย์จะระบุค่าการซื้อสินทรัพย์และการปรับปรุงการซื้อสินทรัพย์สำหรับทั้งปี </span><span class="sxs-lookup"><span data-stu-id="1eb66-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="1eb66-154">นอกจากนี้คุณยังสามารถกำหนดบัญชีสำหรับชนิดธุรกรรมเหล่านี้แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="1eb66-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="1eb66-155">คุณสามารถตั้งค่ากระบวนการตัดจำหน่ายให้ใช้บัญชีที่แตกต่างกัน โดยขึ้นอยู่กับว่าผลการตัดจำหน่ายเป็นกำไรหรือขาดทุน </span><span class="sxs-lookup"><span data-stu-id="1eb66-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="1eb66-156">ฉันจะตั้งค่าชนิดมูลค่าการขายเป็น "ทั้งหมด" เพื่อใช้บัญชีเดียวกันสำหรับการตัดจำหน่ายทุกชนิด</span><span class="sxs-lookup"><span data-stu-id="1eb66-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="1eb66-157">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="1eb66-158">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="1eb66-159">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-159">Click Add.</span></span>
37. <span data-ttu-id="1eb66-160">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="1eb66-161">ในฟิลด์ค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="1eb66-162">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="1eb66-163">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="1eb66-164">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-164">Click Add.</span></span>
41. <span data-ttu-id="1eb66-165">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="1eb66-166">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="1eb66-167">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="1eb66-168">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="1eb66-169">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-169">Click Add.</span></span>
46. <span data-ttu-id="1eb66-170">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="1eb66-171">ในฟิลด์มูลค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="1eb66-172">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="1eb66-173">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="1eb66-174">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-174">Click Add.</span></span>
51. <span data-ttu-id="1eb66-175">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="1eb66-176">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'การปรับปรุงค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="1eb66-177">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="1eb66-178">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="1eb66-179">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-179">Click Add.</span></span>
56. <span data-ttu-id="1eb66-180">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="1eb66-181">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'มูลค่าตามบัญชีสุทธิ'</span><span class="sxs-lookup"><span data-stu-id="1eb66-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="1eb66-182">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="1eb66-183">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="1eb66-184">ในฟิลด์การขายหรือเศษซาก เลือก 'เศษซาก'</span><span class="sxs-lookup"><span data-stu-id="1eb66-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="1eb66-185">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-185">Click Add.</span></span>
62. <span data-ttu-id="1eb66-186">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="1eb66-187">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าการซื้อสินทรัพย์'</span><span class="sxs-lookup"><span data-stu-id="1eb66-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="1eb66-188">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="1eb66-189">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="1eb66-190">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-190">Click Add.</span></span>
67. <span data-ttu-id="1eb66-191">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="1eb66-192">ในฟิลด์ค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="1eb66-193">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="1eb66-194">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="1eb66-195">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-195">Click Add.</span></span>
71. <span data-ttu-id="1eb66-196">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="1eb66-197">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'ค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="1eb66-198">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="1eb66-199">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="1eb66-200">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-200">Click Add.</span></span>
76. <span data-ttu-id="1eb66-201">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="1eb66-202">ในฟิลด์มูลค่าการลงรายการบัญชี เลือก 'ค่าเสื่อมราคา (ปีก่อนหน้านี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="1eb66-203">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="1eb66-204">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="1eb66-205">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-205">Click Add.</span></span>
81. <span data-ttu-id="1eb66-206">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="1eb66-207">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'การปรับปรุงค่าเสื่อมราคา (ในปีนี้)'</span><span class="sxs-lookup"><span data-stu-id="1eb66-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="1eb66-208">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="1eb66-209">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="1eb66-210">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1eb66-210">Click Add.</span></span>
86. <span data-ttu-id="1eb66-211">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="1eb66-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="1eb66-212">ในฟิลด์มูลค่าการลงรายบัญชี เลือก 'มูลค่าตามบัญชีสุทธิ'</span><span class="sxs-lookup"><span data-stu-id="1eb66-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="1eb66-213">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="1eb66-214">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1eb66-214">In the Offset account field, specify the desired values.</span></span>

