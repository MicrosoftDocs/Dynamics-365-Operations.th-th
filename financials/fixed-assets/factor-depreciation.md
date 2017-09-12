---
title: "การคิดค่าเสื่อมราคาตามอัตรา"
description: "บทความนี้แสดงภาพรวมของวิธีคิดค่าเสื่อมราคาตามอัตรา"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: th-th
ms.lasthandoff: 06/29/2017


---

# <a name="factor-depreciation"></a><span data-ttu-id="bb23c-103">การคิดค่าเสื่อมราคาตามอัตรา</span><span class="sxs-lookup"><span data-stu-id="bb23c-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bb23c-104">บทความนี้แสดงภาพรวมของวิธีคิดค่าเสื่อมราคาตามอัตรา</span><span class="sxs-lookup"><span data-stu-id="bb23c-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="bb23c-105">ตัวคูณคือเปอร์เซ็นต์ที่ใช้ในการคิดค่าเสื่อมราคาสินทรัพย์ </span><span class="sxs-lookup"><span data-stu-id="bb23c-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="bb23c-106">เมื่อคุณตั้งค่าโพรไฟล์การคิดค่าเสื่อมราคาสินทรัพย์ถาวร และเลือก **ตัวคูณ** ในฟิลด์ **วิธีการ** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา** คุณสามารถตั้งค่าการคิดค่าเสื่อมราคาแบบก้าวหน้า แบบถดถอย หรือแบบเส้นตรง:</span><span class="sxs-lookup"><span data-stu-id="bb23c-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="bb23c-107">ในการคิดค่าเสื่อมราคาแบบก้าวหน้า ยอดค่าเสื่อมราคาจะเพิ่มขึ้นในแต่ละรอบระยะเวลาการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bb23c-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="bb23c-108">ในการคิดค่าเสื่อมราคาแบบถดถอย ยอดค่าเสื่อมราคาในแต่ละรอบระยะเวลาจะลดลงตามเวลา</span><span class="sxs-lookup"><span data-stu-id="bb23c-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="bb23c-109">ในค่าเสื่อมราคาแบบเส้นตรง ค่าเสื่อมราคาจะเท่ากันในแต่ละรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="bb23c-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="bb23c-110">กฎและตัวอย่างที่ระบุวิธีการที่คุณสามารถตั้งค่าตัวคูณต่อไปนี้ สำหรับการคิดค่าเสื่อมราคาแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="bb23c-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bb23c-111">หมายเหตุ: เมื่อคุณเลือก **ตัวคูณ** ในฟิลด์ **วิธีการ** ฟิลด์ **ตัวคูณ** และ ฟิลด์  **ช่วง** ถูกแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="bb23c-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="bb23c-112">การคิดค่าเสื่อมราคาแบบก้าวหน้า</span><span class="sxs-lookup"><span data-stu-id="bb23c-112">Progressive depreciation</span></span>
<span data-ttu-id="bb23c-113">ค่าในฟิลด์ **ตัวคูณ** มากกว่า **50**</span><span class="sxs-lookup"><span data-stu-id="bb23c-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="bb23c-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="bb23c-114">Example</span></span>

<span data-ttu-id="bb23c-115">ราคาการซื้อสินทรัพย์คือ 100,000 ตัวคูณคือ 70 อายุการใช้งานคือ 10 ปี และการคิดค่าเสื่อมราคาเริ่มต้นในวันที่ 1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="bb23c-116">ยอดค่าเสื่อมราคาและยอดมูลค่าตามบัญชีสุทธิ แสดงไว้เฉพาะสำหรับอายุการใช้งานหกปีแรกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bb23c-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="bb23c-117">ปี</span><span class="sxs-lookup"><span data-stu-id="bb23c-117">Year</span></span> | <span data-ttu-id="bb23c-118">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="bb23c-118">Period</span></span>      | <span data-ttu-id="bb23c-119">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bb23c-119">Depreciation amount</span></span> | <span data-ttu-id="bb23c-120">ยอดมูลค่าตามบัญชีสุทธิ</span><span class="sxs-lookup"><span data-stu-id="bb23c-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="bb23c-121">1</span><span class="sxs-lookup"><span data-stu-id="bb23c-121">1</span></span>    | <span data-ttu-id="bb23c-122">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-122">December 31</span></span> | <span data-ttu-id="bb23c-123">307.69</span><span class="sxs-lookup"><span data-stu-id="bb23c-123">307.69</span></span>              | <span data-ttu-id="bb23c-124">99,692.31</span><span class="sxs-lookup"><span data-stu-id="bb23c-124">99,692.31</span></span>             |
| <span data-ttu-id="bb23c-125">2</span><span class="sxs-lookup"><span data-stu-id="bb23c-125">2</span></span>    | <span data-ttu-id="bb23c-126">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-126">December 31</span></span> | <span data-ttu-id="bb23c-127">1,447.21</span><span class="sxs-lookup"><span data-stu-id="bb23c-127">1,447.21</span></span>            | <span data-ttu-id="bb23c-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="bb23c-128">98,245.10</span></span>             |
| <span data-ttu-id="bb23c-129">3</span><span class="sxs-lookup"><span data-stu-id="bb23c-129">3</span></span>    | <span data-ttu-id="bb23c-130">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-130">December 31</span></span> | <span data-ttu-id="bb23c-131">3,104.50</span><span class="sxs-lookup"><span data-stu-id="bb23c-131">3,104.50</span></span>            | <span data-ttu-id="bb23c-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="bb23c-132">95,140.60</span></span>             |
| <span data-ttu-id="bb23c-133">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="bb23c-133">4</span></span>    | <span data-ttu-id="bb23c-134">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-134">December 31</span></span> | <span data-ttu-id="bb23c-135">5,150.21</span><span class="sxs-lookup"><span data-stu-id="bb23c-135">5,150.21</span></span>            | <span data-ttu-id="bb23c-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="bb23c-136">89,990.39</span></span>             |
| <span data-ttu-id="bb23c-137">5</span><span class="sxs-lookup"><span data-stu-id="bb23c-137">5</span></span>    | <span data-ttu-id="bb23c-138">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-138">December 31</span></span> | <span data-ttu-id="bb23c-139">7,522.95</span><span class="sxs-lookup"><span data-stu-id="bb23c-139">7,522.95</span></span>            | <span data-ttu-id="bb23c-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="bb23c-140">82,467.44</span></span>             |
| <span data-ttu-id="bb23c-141">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="bb23c-141">6</span></span>    | <span data-ttu-id="bb23c-142">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-142">December 31</span></span> | <span data-ttu-id="bb23c-143">10,184.06</span><span class="sxs-lookup"><span data-stu-id="bb23c-143">10,184.06</span></span>           | <span data-ttu-id="bb23c-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="bb23c-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="bb23c-145">ค่าเสื่อมราคาแบบถดถอย</span><span class="sxs-lookup"><span data-stu-id="bb23c-145">Digressive depreciation</span></span>
<span data-ttu-id="bb23c-146">ค่าในฟิลด์ **ตัวคูณ** น้อยกว่า **50**</span><span class="sxs-lookup"><span data-stu-id="bb23c-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="bb23c-147">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="bb23c-147">Example</span></span>

<span data-ttu-id="bb23c-148">ราคาการซื้อสินทรัพย์คือ 100,000 ตัวคูณคือ 20 อายุการใช้งานคือ 10 ปี และการคิดค่าเสื่อมราคาเริ่มต้นในวันที่ 1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="bb23c-149">ยอดค่าเสื่อมราคาและยอดมูลค่าตามบัญชีสุทธิ แสดงไว้เฉพาะสำหรับอายุการใช้งานหกปีแรกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bb23c-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="bb23c-150">ปี</span><span class="sxs-lookup"><span data-stu-id="bb23c-150">Year</span></span> | <span data-ttu-id="bb23c-151">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="bb23c-151">Period</span></span>      | <span data-ttu-id="bb23c-152">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bb23c-152">Depreciation amount</span></span> | <span data-ttu-id="bb23c-153">ยอดมูลค่าตามบัญชีสุทธิ</span><span class="sxs-lookup"><span data-stu-id="bb23c-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="bb23c-154">1</span><span class="sxs-lookup"><span data-stu-id="bb23c-154">1</span></span>    | <span data-ttu-id="bb23c-155">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-155">December 31</span></span> | <span data-ttu-id="bb23c-156">56,080.43</span><span class="sxs-lookup"><span data-stu-id="bb23c-156">56,080.43</span></span>           | <span data-ttu-id="bb23c-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="bb23c-157">43,919.57</span></span>             |
| <span data-ttu-id="bb23c-158">2</span><span class="sxs-lookup"><span data-stu-id="bb23c-158">2</span></span>    | <span data-ttu-id="bb23c-159">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-159">December 31</span></span> | <span data-ttu-id="bb23c-160">10,665.70</span><span class="sxs-lookup"><span data-stu-id="bb23c-160">10,665.70</span></span>           | <span data-ttu-id="bb23c-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="bb23c-161">33,253.87</span></span>             |
| <span data-ttu-id="bb23c-162">3</span><span class="sxs-lookup"><span data-stu-id="bb23c-162">3</span></span>    | <span data-ttu-id="bb23c-163">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-163">December 31</span></span> | <span data-ttu-id="bb23c-164">7,156.22</span><span class="sxs-lookup"><span data-stu-id="bb23c-164">7,156.22</span></span>            | <span data-ttu-id="bb23c-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="bb23c-165">26,097.65</span></span>             |
| <span data-ttu-id="bb23c-166">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="bb23c-166">4</span></span>    | <span data-ttu-id="bb23c-167">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-167">December 31</span></span> | <span data-ttu-id="bb23c-168">5,538.06</span><span class="sxs-lookup"><span data-stu-id="bb23c-168">5,538.06</span></span>            | <span data-ttu-id="bb23c-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="bb23c-169">20,559.59</span></span>             |
| <span data-ttu-id="bb23c-170">5</span><span class="sxs-lookup"><span data-stu-id="bb23c-170">5</span></span>    | <span data-ttu-id="bb23c-171">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-171">December 31</span></span> | <span data-ttu-id="bb23c-172">4,579.89</span><span class="sxs-lookup"><span data-stu-id="bb23c-172">4,579.89</span></span>            | <span data-ttu-id="bb23c-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="bb23c-173">15,979.70</span></span>             |
| <span data-ttu-id="bb23c-174">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="bb23c-174">6</span></span>    | <span data-ttu-id="bb23c-175">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="bb23c-175">December 31</span></span> | <span data-ttu-id="bb23c-176">3,937.36</span><span class="sxs-lookup"><span data-stu-id="bb23c-176">3,937.36</span></span>            | <span data-ttu-id="bb23c-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="bb23c-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="bb23c-178">การคิดค่าเสื่อมราคาแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="bb23c-178">Straight line depreciation</span></span>
<span data-ttu-id="bb23c-179">ค่าในฟิลด์ **ตัวคูณ** เท่ากับ **50**</span><span class="sxs-lookup"><span data-stu-id="bb23c-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="bb23c-180">ในกรณีนี้ ค่าเสื่อมราคาจะเท่ากันในแต่ละรอบระยะเวลา และคุณควรพิจารณาผลกระทบของค่าที่คุณระบุในฟิลด์อื่นๆ ตามที่อธิบายไว้ใน [การคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรง](straight-line-service-life-depreciation.md)</span><span class="sxs-lookup"><span data-stu-id="bb23c-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




