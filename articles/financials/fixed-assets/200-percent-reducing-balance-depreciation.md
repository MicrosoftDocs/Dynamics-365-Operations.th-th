---
title: "การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200%"
description: "บทความนี้แสดงภาพรวมยอดดุลที่ลดลง 200% ของค่าเสื่อมราคา"
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3db58ec2583036be93d70cdd044bcaddfc05ba7e
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="e6026-103">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200%</span><span class="sxs-lookup"><span data-stu-id="e6026-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6026-104">บทความนี้แสดงภาพรวมยอดดุลที่ลดลง 200% ของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="e6026-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="e6026-105">เมื่อคุณตั้งค่าโพรไฟล์การคิดค่าเสื่อมราคาสินทรัพย์ถาวร และเลือกค่า **ยอดดุลที่ลดลง 200%** ในฟิลด์ **วิธี** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา** สินทรัพย์ถาวรที่มีการกำหนดโพรไฟล์การคิดค่าเสื่อมราคาจะถูกคิดค่าเสื่อมราคาในอัตราเปอร์เซ็นต์เดียวกัน ในแต่ละรอบระยะเวลาการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="e6026-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="e6026-106">เปอร์เซ็นต์จะถูกคำนวณตามอายุการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e6026-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="e6026-107">ตัวอย่างเช่น ถ้าสินทรัพย์มีอายุการใช้งานห้าปี เปอร์เซ็นต์จะถูกคำนวณเป็น 40 เปอร์เซ็นต์ (200% ÷ 5)</span><span class="sxs-lookup"><span data-stu-id="e6026-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="e6026-108">วิธีนี้เรียกอีกอย่างว่ายอดดุลที่ลดลงสองเท่า</span><span class="sxs-lookup"><span data-stu-id="e6026-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="e6026-109">เพื่อตั้งค่าการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200% คุณยังต้องเลือกตัวเลือกอื่นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** ด้วย และฟิลด์ **ความถี่ของรอบระยะเวลา** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="e6026-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="e6026-110">ตัวเลือกที่พร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา** นั้นจะแตกต่างกันไป ขึ้นอยู่กับค่าที่ถูกเลือกในฟิลด์ **ปีที่คิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="e6026-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="e6026-111">เลือกปีการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="e6026-111">Select a depreciation year</span></span>
<span data-ttu-id="e6026-112">คุณสามารถเลือก **ปฏิทิน** หรือ **บัญชีการเงิน** ในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="e6026-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="e6026-113">ค่าเริ่มต้นคือ **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="e6026-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="e6026-114">การคัดเลือกของคุณกำหนดตัวเลือกที่พร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="e6026-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="e6026-115">ฟิลด์นี้จะกำหนดวันที่และจำนวนเงินของการลงรายการบัญชีการตั้งค่าเสื่อมราคาตลอดปีปฏิทินดังนี้:</span><span class="sxs-lookup"><span data-stu-id="e6026-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="e6026-116">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="e6026-116">Calendar</span></span>

<span data-ttu-id="e6026-117">คุณสามารถเลือกที่จะคงค่าเริ่มต้นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="e6026-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="e6026-118">ตัวเลือก **ปฏิทิน** อัพเดทค่าเสื่อมราคาโดยยึดวันที่ 1 มกราคมของทุกปีเป็นหลัก</span><span class="sxs-lookup"><span data-stu-id="e6026-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="e6026-119">โดยทั่วไป ค่าเสื่อมราคาคือมูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="e6026-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="e6026-120">ในตัวอย่างถัดไปของหัวข้อนี้ ฐานการคิดค่าเสื่อมราคาคือตัวเศษในนิพจน์แรกบนคอลัมน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e6026-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="e6026-121">ถ้าคุณเลือก **ปฏิทิน** เป็นปีค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**:</span><span class="sxs-lookup"><span data-stu-id="e6026-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="e6026-122">**รายปี** ลงรายการบัญชียอดเงินในวันที่ 31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="e6026-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="e6026-123">**รายเดือน** ลงรายการบัญชีจำนวนเงินรายเดือนเมื่อสิ้นสุดเดือนปฏิทินแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="e6026-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="e6026-124">**รายไตรมาส** ลงรายการบัญชีจำนวนเงินรายไตรมาส เมื่อสิ้นสุดไตรมาสปฏิทินแต่ละไตรมาส (31 มีนาคม 30 มิถุนายน 30 กันยายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="e6026-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="e6026-125">**ทุกครึ่งปี** งรายการบัญชีจำนวนเงินรายครึ่งปี ณ ครึ่งปีปฏิทิน (30 มิถุนายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="e6026-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="e6026-126">ลงรายการบัญชี **รายวัน** ยอดเงินค่าเสื่อมราคาสำหรับวิธีคิดค่าเสื่อมราคารายวันโดยใช้ธุรกรรมหนึ่งรายการสำหรับแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="e6026-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="e6026-127">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e6026-127">Fiscal</span></span>

<span data-ttu-id="e6026-128">ถ้าคุณเลือก **ทางการเงิน** ในฟิลด์ปี **การคิดค่าเสื่อมราคา** การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200% จะถูกคำนวณตามปีบัญชีสำหรับปฏิทินทางการเงินที่ระบุไว้สำหรับสมุดบัญชี หรือสำหรับปฏิทินทางการเงินที่ถูกเลือกในหน้า **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="e6026-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="e6026-129">ปฏิทินทางการเงินถูกตั้งค่าบนหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="e6026-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="e6026-130">ตัวอย่างเช่น สำหรับปีบัญชีวันที่ 1 กรกฎาคมถึง 30 มิถุนายน การคำนวณค่าเสื่อมราคาเริ่มต้นในวันที่ 1 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="e6026-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="e6026-131">ปีบัญชีอาจจะยาวกว่าหรือสั้นกว่า 12 เดือนได้ </span><span class="sxs-lookup"><span data-stu-id="e6026-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="e6026-132">ค่าเสื่อมราคาถูกปรับสำหรับแต่ละรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="e6026-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="e6026-133">ความยาวปีบัญชีถัดไปถูกกำหนดด้วยการตั้งค่าของรอบระยะเวลาบนหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="e6026-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="e6026-134">เมื่อมีการเลือก **ทางการเงิน** เป็นปีที่คิดค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**:</span><span class="sxs-lookup"><span data-stu-id="e6026-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="e6026-135">**รายปี** จะลงรายการบัญชีของยอดรวมของค่าเสื่อมราคาที่คำนวณได้สำหรับปีบัญชีให้เป็นยอดเดียวในวันที่สุดท้ายของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="e6026-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="e6026-136">การลงรายการบัญชี **รอบระยะเวลาทางบัญชี** ยอดเงินของค่าเสื่อมราคาจะถูกคำนวณสำหรับปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="e6026-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="e6026-137">ยอดเงินนี้ถูกสะสมไว้ในรอบระยะเวลาทางบัญชีที่กำหนดไว้ในหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="e6026-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="e6026-138">ตัวอย่างของการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200%</span><span class="sxs-lookup"><span data-stu-id="e6026-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="e6026-139">ต้นทุนการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e6026-139">Acquisition cost</span></span>               | <span data-ttu-id="e6026-140">11,000</span><span class="sxs-lookup"><span data-stu-id="e6026-140">11,000</span></span> |
| <span data-ttu-id="e6026-141">มูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="e6026-141">Salvage value</span></span>                  | <span data-ttu-id="e6026-142">1, 000</span><span class="sxs-lookup"><span data-stu-id="e6026-142">1, 000</span></span> |
| <span data-ttu-id="e6026-143">ฐานการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="e6026-143">Depreciation base</span></span>              | <span data-ttu-id="e6026-144">10,000</span><span class="sxs-lookup"><span data-stu-id="e6026-144">10,000</span></span> |
| <span data-ttu-id="e6026-145">ปีสำหรับอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e6026-145">Service life years</span></span>             | <span data-ttu-id="e6026-146">5</span><span class="sxs-lookup"><span data-stu-id="e6026-146">5</span></span>      |
| <span data-ttu-id="e6026-147">เปอร์เซ็นต์ค่าเสื่อมราคาต่อปี</span><span class="sxs-lookup"><span data-stu-id="e6026-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="e6026-148">40%</span><span class="sxs-lookup"><span data-stu-id="e6026-148">40%</span></span>    |

<span data-ttu-id="e6026-149">วิธียอดดุลที่ลดลง 200% แบ่ง 200 เปอร์เซ็นต์ด้วยปีของอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e6026-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="e6026-150">เปอร์เซ็นต์ดังกล่าวจะถูกคูณด้วยมูลค่าตามบัญชีสุทธิของสินทรัพย์เพื่อกำหนดจำนวนเงินค่าเสื่อมราคาสำหรับปี</span><span class="sxs-lookup"><span data-stu-id="e6026-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="e6026-151">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="e6026-151">Period</span></span> | <span data-ttu-id="e6026-152">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="e6026-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="e6026-153">มูลค่าตามบัญชี</span><span class="sxs-lookup"><span data-stu-id="e6026-153">Book value</span></span>             | <span data-ttu-id="e6026-154">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="e6026-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="e6026-155">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="e6026-155">Year 1</span></span> | <span data-ttu-id="e6026-156">(11,000 – 1,000) × 40% = 4,000</span><span class="sxs-lookup"><span data-stu-id="e6026-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="e6026-157">11,000 - 4,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="e6026-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="e6026-158">11,000 – 1,000 – 4,000 = 6,000</span><span class="sxs-lookup"><span data-stu-id="e6026-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="e6026-159">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="e6026-159">Year 2</span></span> | <span data-ttu-id="e6026-160">6,000 × 40% = 2,400</span><span class="sxs-lookup"><span data-stu-id="e6026-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="e6026-161">7,000 - 2,400 = 4,600</span><span class="sxs-lookup"><span data-stu-id="e6026-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="e6026-162">6,000 - 2,400 = 3,600</span><span class="sxs-lookup"><span data-stu-id="e6026-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="e6026-163">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="e6026-163">Year 3</span></span> | <span data-ttu-id="e6026-164">3,600 × 40% = 1,440</span><span class="sxs-lookup"><span data-stu-id="e6026-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="e6026-165">4,600 – 1,440 = 3,160</span><span class="sxs-lookup"><span data-stu-id="e6026-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="e6026-166">3,600 – 1,440 = 2,160</span><span class="sxs-lookup"><span data-stu-id="e6026-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="e6026-167">โดยทั่วไป เมื่อยอดเงินถูกคำนวณโดยใช้วิธีค่าเสื่อมราคายอดดุลที่ลดลง 200% มีน้อยกว่ายอดเงินที่จะถูกคำนวณโดยใช้วิธีเส้นตรง จะมีการแปลงไปยังวิธีเส้นตรงสำหรับอายุที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="e6026-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




