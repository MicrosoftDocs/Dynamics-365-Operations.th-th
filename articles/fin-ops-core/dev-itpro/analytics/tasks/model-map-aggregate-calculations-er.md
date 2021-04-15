---
title: ใช้การตั้งค่าคอนฟิกการแม็ปแบบจำลองสำหรับการคำนวณรวมที่ระดับฐานข้อมูล
description: หัวข้อนี้อธิบายวิธีออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลองของการรายงานทางอิเล็กทรอนิกส์ใหม่ และใช้ฟังก์ชัน ER ภายในสำหรับการคำนวณรวมที่มีประสิทธิภาพ
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f48596c30127976d915811ffa8412dcc9b2593
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745386"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="bcfd8-103">ใช้การตั้งค่าคอนฟิกการแม็ปแบบจำลองสำหรับการคำนวณรวมที่ระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bcfd8-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcfd8-104">กระบวนงานนี้แสดงข้อมูลเกี่ยวกับวิธีการออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง (ER) ของการรายงานทางอิเล็กทรอนิกส์ใหม่ และใช้ฟังก์ชัน ER ภายในสำหรับการคำนวณรวมที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="bcfd8-105">ในกระบวนงานนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="bcfd8-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="bcfd8-106">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="bcfd8-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="bcfd8-107">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="bcfd8-108">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ลำดับแรกคุณต้องทำขั้นตอนในกระบวนงาน " ER ช่วยเพิ่มประสิทธิภาพในการคำนวณการรวม ด้วยการดำเนินการเหล่านั้นที่ระดับฐานข้อมูล (ส่วนที่ 1: เตรียมการตั้งค่าคอนฟิก)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bcfd8-108">To complete these steps, you must first complete the steps in the procedure, "ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations)."</span></span>

1. <span data-ttu-id="bcfd8-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bcfd8-110">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="bcfd8-111">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต\การแม็ปตัวอย่างอินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="bcfd8-112">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-112">Click Designer.</span></span>
5. <span data-ttu-id="bcfd8-113">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-113">Click Designer.</span></span>
6. <span data-ttu-id="bcfd8-114">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\เรกคอร์ดตาราง'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="bcfd8-115">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-115">Click Add root.</span></span>
    * <span data-ttu-id="bcfd8-116">เพิ่มแหล่งข้อมูลใหม่ซึ่งแสดงเรกคอร์ดที่คุณต้องการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="bcfd8-117">ในฟิลด์ชื่อ พิมพ์ 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="bcfd8-118">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-118">Transactions</span></span>  
9. <span data-ttu-id="bcfd8-119">ในฟิลด์ตาราง พิมพ์ 'อินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="bcfd8-120">อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="bcfd8-120">Intrastat</span></span>  
10. <span data-ttu-id="bcfd8-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-121">Click OK.</span></span>
11. <span data-ttu-id="bcfd8-122">ในแผนภูมิ ให้เลือก 'ฟังก์ชัน\จัดกลุ่มโดย'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="bcfd8-123">ชนิดแหล่งข้อมูลนี้ใช้ในการแนะนำแหล่งข้อมูลใหม่ขณะทำงานกับเรกคอร์ดกลุ่ม และในการคำนวณการรวมที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bcfd8-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="bcfd8-124">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-124">Click Add root.</span></span>
13. <span data-ttu-id="bcfd8-125">ในฟิลด์ชื่อ พิมพ์ 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="bcfd8-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="bcfd8-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="bcfd8-127">คลิกแก้ไขกลุ่มโดย</span><span class="sxs-lookup"><span data-stu-id="bcfd8-127">Click Edit group by.</span></span>
15. <span data-ttu-id="bcfd8-128">ในแผนภูมิ เลือก 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="bcfd8-129">เลือกแหล่งข้อมูลเพิ่มเติมเกี่ยวกับชนิด 'รายการเรกคอร์ด' ที่แสดงถึงเรกคอร์ดที่คุณต้องการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-129">Select the added data source of the 'Record list' type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="bcfd8-130">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-130">Click Add field to.</span></span>
17. <span data-ttu-id="bcfd8-131">คลิกสิ่งที่จะจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-131">Click What to group.</span></span>
18. <span data-ttu-id="bcfd8-132">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="bcfd8-133">ในแผนภูมิ เลือก 'ธุรกรรม\ทิศทาง'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="bcfd8-134">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-134">Click Add field to.</span></span>
21. <span data-ttu-id="bcfd8-135">คลิกฟิลด์ที่ถูกจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="bcfd8-136">เลือกฟิลด์เพื่อระบุระดับการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="bcfd8-137">ตามการเลือกนี้ แหล่งข้อมูลจะส่งคืนเมื่อรันไทม์ที่จำนวนกลุ่มของธุรกรรมมากเท่ากับที่มีรหัสคำสั่งที่จะตรงตามความต้องการในตารางอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="bcfd8-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="bcfd8-138">ในแผนภูมิ เลือก ' ธุรกรรม\จำนวนเงินในใบแจ้งหนี้(AmountMST)'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="bcfd8-139">เลือกฟิลด์นี้เพื่อระบุแหล่งที่มาสำหรับการคำนวณการรวม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="bcfd8-140">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-140">Click Add field to.</span></span>
24. <span data-ttu-id="bcfd8-141">คลิกฟิลด์การรวม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="bcfd8-142">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="bcfd8-143">ในฟิลด์ วิธีการ ให้เลือก 'รวม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="bcfd8-144">เลือกชนิดการรวม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="bcfd8-145">ในฟิลด์ชื่อ พิมพ์ 'SumOfAmountMST'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="bcfd8-146">ระบุชื่อของการรวมนี้ในแหล่งข้อมูลที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="bcfd8-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-147">Click Save.</span></span>
    * <span data-ttu-id="bcfd8-148">หมายเหตุ ฟิลด์ 'ดำเนินการเมื่อ' บ่งชี้ว่า จะมีการดำเนินการจัดกลุ่มที่รันไทม์ในฐานข้อมูล SQL</span><span class="sxs-lookup"><span data-stu-id="bcfd8-148">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="bcfd8-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bcfd8-149">Close the page.</span></span>
30. <span data-ttu-id="bcfd8-150">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-150">Click OK.</span></span>
31. <span data-ttu-id="bcfd8-151">ในแผนภูมิ ให้ขยาย 'รวม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="bcfd8-152">ในแผนภูมิ ขยาย 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="bcfd8-153">ในแผนภูมิ ขยาย 'TransactionsGroups\รวม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="bcfd8-154">ในแผนภูมิ เลือก 'TransactionsGroups\รวม\SumOfAmountMST'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="bcfd8-155">ในแผนภูมิ เลือก ' ยอดรวม\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="bcfd8-156">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-156">Click Bind.</span></span>
    * <span data-ttu-id="bcfd8-157">โดยขึ้นอยู่กับการตั้งค่านี้ แหล่งข้อมูลนี้จะคำนวณผลรวมของค่าฟิลด์ 'AmountMST' สำหรับแต่ละกลุ่มของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-157">Based on this setting, this data source will calculate the sum of values of the 'AmountMST' field for each groups of transactions.</span></span> <span data-ttu-id="bcfd8-158">การคำนวณการรวมนี้จะพร้อมใช้งานเป็นสินค้า TransactionsGroups.aggregated.TotalAmount</span><span class="sxs-lookup"><span data-stu-id="bcfd8-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="bcfd8-159">ในแผนภูมิ ขยาย 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="bcfd8-160">ในแผนภูมิ ให้เลือก 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="bcfd8-161">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="bcfd8-161">Click Edit.</span></span>
40. <span data-ttu-id="bcfd8-162">คลิกแก้ไขกลุ่มโดย</span><span class="sxs-lookup"><span data-stu-id="bcfd8-162">Click Edit group by.</span></span>
41. <span data-ttu-id="bcfd8-163">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="bcfd8-164">ในแผนภูมิ เลือก ' ธุรกรรม\จำนวนเงินในใบแจ้งหนี้(AmountMST)'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="bcfd8-165">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-165">Click Add field to.</span></span>
44. <span data-ttu-id="bcfd8-166">คลิกฟิลด์การรวม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="bcfd8-167">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="bcfd8-168">ในฟิลด์ วิธีการ ให้เลือก 'สูงสุด'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="bcfd8-169">ในฟิลด์ชื่อ พิมพ์ 'MaxOfAmountMST'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="bcfd8-170">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-170">Click Save.</span></span>
    * <span data-ttu-id="bcfd8-171">ในปัจจุบัน การดำเนินการของแหล่งข้อมูลของ GROUPBY สามารถแปลเป็นระดับฐานข้อมูล SQL พร้อมกับข้อจำกัดบางประการ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="bcfd8-172">สามารถทำการแปลสำหรับแหล่งข้อมูลอย่างใดอย่างหนึ่งของชนิด 'รายการเรกคอร์ด' หรือแหล่งข้อมูลที่แสดงเป็นนิพจน์โดยใช้ฟังก์ชันตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-172">Translation can be done for either data sources of the 'Record list' type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="bcfd8-173">นอกจากนี้ ยังสามารถทำได้เมื่อมีการตั้งค่าคอนฟิกการรวมเดียวเท่านั้นสำหรับฟิลด์เดียวของเรกคอร์ดที่จัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="bcfd8-174">โปรดทราบว่า ถึงแม้ว่าจะมีการตั้งค่าคอนฟิกการรวมมากกว่าหนึ่งรายการสำหรับฟิลด์ AmountMST ฟิลด์ 'ดำเนินการเมื่อ' ยังคงบ่งชี้ว่า จะมีดำเนินการจัดกลุ่มที่รันไทม์ในฐานข้อมูล SQL</span><span class="sxs-lookup"><span data-stu-id="bcfd8-174">Note that even though more than one aggregation was configured for the AmountMST field, the 'Execution at' field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="bcfd8-175">ทั้งนี้เนื่องจากมีการผูกการรวมหนึ่งรายการเท่านั้นกับสินค้าแบบจำลองข้อมูล และจะถูกใช้เมื่อรันไทม์เพื่อดึงข้อมูลจากแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="bcfd8-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="bcfd8-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bcfd8-176">Close the page.</span></span>
50. <span data-ttu-id="bcfd8-177">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-177">Click OK.</span></span>
51. <span data-ttu-id="bcfd8-178">ในแผนภูมิ ขยาย 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="bcfd8-179">ในแผนภูมิ ขยาย 'TransactionsGroups\รวม'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="bcfd8-180">ในแผนภูมิ เลือก 'TransactionsGroups\รวม\MaxOfAmountMST'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="bcfd8-181">ในแผนภูมิ เลือก 'ยอดรวม\มูลค่าทางสถิติรวม(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="bcfd8-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-182">Click Bind.</span></span>
56. <span data-ttu-id="bcfd8-183">ในแผนภูมิ ขยาย 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="bcfd8-184">ในแผนภูมิ ให้เลือก 'TransactionsGroups'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="bcfd8-185">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="bcfd8-185">Click Edit.</span></span>
59. <span data-ttu-id="bcfd8-186">คลิกแก้ไขกลุ่มโดย</span><span class="sxs-lookup"><span data-stu-id="bcfd8-186">Click Edit group by.</span></span>
    * <span data-ttu-id="bcfd8-187">หมายเหตุว่า ฟิลด์ 'ดำเนินการเมื่อ' บ่งชี้ว่า การจัดกลุ่มนี้จะสามารถทำได้ในรันไทม์ในหน่วยความจำได้ เนื่องจากการรวมทั้งสองของฟิลด์เดียวกันจะผูกอยู่กับข้อมูลแบบจำลองสินค้า</span><span class="sxs-lookup"><span data-stu-id="bcfd8-187">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="bcfd8-188">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="bcfd8-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="bcfd8-189">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-189">Click Delete.</span></span>
62. <span data-ttu-id="bcfd8-190">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="bcfd8-190">Click Yes.</span></span>
63. <span data-ttu-id="bcfd8-191">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="bcfd8-191">Click Delete.</span></span>
64. <span data-ttu-id="bcfd8-192">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="bcfd8-192">Click Yes.</span></span>
65. <span data-ttu-id="bcfd8-193">คลิกเพิ่มฟิลด์ไปยัง</span><span class="sxs-lookup"><span data-stu-id="bcfd8-193">Click Add field to.</span></span>
66. <span data-ttu-id="bcfd8-194">คลิกสิ่งที่จะจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bcfd8-194">Click What to group.</span></span>
67. <span data-ttu-id="bcfd8-195">ในแผนภูมิ ขยาย 'เรกคอร์ดสินค้าที่ซื้อขายกัน(Iอินทราสแทต)'</span><span class="sxs-lookup"><span data-stu-id="bcfd8-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="bcfd8-196">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bcfd8-196">Click Save.</span></span>
    * <span data-ttu-id="bcfd8-197">หมายเหตุว่า ฟิลด์ 'ดำเนินการเมื่อ' บ่งชี้ว่า การจัดกลุ่มนี้จะสามารถทำได้ในขณะทำงานในหน่วยความจำ แม้ว่าจะไม่มีการรวมที่กำหนดและแหล่งข้อมูลที่เลือกของชนิด 'เรกคอร์ดตาราง' อ้างอิงถึงตาราง 'อินทราสแทต' เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="bcfd8-197">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of 'Table records' type refers to the same 'Intrastat' table.</span></span> <span data-ttu-id="bcfd8-198">ทั้งนี้เนื่องจากแหล่งข้อมูลประกอบด้วยฟิลด์ที่คำนวณบางฟิลด์ ซึ่งไม่สามารถแปลเป็นระดับฐานข้อมูล SQL ได้</span><span class="sxs-lookup"><span data-stu-id="bcfd8-198">This is because the data source contains some calculated fields which can't yet be translated to the SQL database level.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]