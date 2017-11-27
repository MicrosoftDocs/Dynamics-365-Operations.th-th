---
title: "การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125%"
description: "บทความนี้แสดงภาพรวมยอดดุลที่ลดลง 125% ของค่าเสื่อมราคา"
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="f82f8-103">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125%</span><span class="sxs-lookup"><span data-stu-id="f82f8-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f82f8-104">บทความนี้แสดงภาพรวมยอดดุลที่ลดลง 125% ของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="f82f8-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="f82f8-105">เมื่อคุณตั้งค่าโพรไฟล์การคิดค่าเสื่อมราคาสินทรัพย์ถาวร และเลือกค่า **ยอดดุลที่ลดลง 125%** ในฟิลด์ **วิธี** บนหน้า **โพรไฟล์การคิดค่าเสื่อมราคา** สินทรัพย์ถาวรที่มีการกำหนดโพรไฟล์การคิดค่าเสื่อมราคาจะถูกคิดค่าเสื่อมราคาในอัตราเปอร์เซ็นต์เดียวกัน ในแต่ละรอบระยะเวลาการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="f82f8-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="f82f8-106">เปอร์เซ็นต์นี้จะถูกคำนวณโดยอาศัยอายุการบริการของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f82f8-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="f82f8-107">ตัวอย่างเช่น ถ้าสินทรัพย์มีอายุการใช้งานห้าปี เปอร์เซ็นต์จะถูกคำนวณเป็น 25 เปอร์เซ็นต์ (125% ÷ 5)</span><span class="sxs-lookup"><span data-stu-id="f82f8-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="f82f8-108">เพื่อตั้งค่าการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125% คุณยังต้องเลือกตัวเลือกอื่นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** ด้วย และฟิลด์ **ความถี่ของรอบระยะเวลา** บนหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="f82f8-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f82f8-109">ตัวเลือกที่จะปรากฎบนฟิลด์ **ความถี่ของรอบระยะเวลา** นั้นจะแตกต่างกันไป ขึ้นอยู่กับค่าที่ถูกเลือกในฟิลด์ **ปีการคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="f82f8-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="f82f8-110">เลือกปีการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="f82f8-110">Select a depreciation year</span></span>
<span data-ttu-id="f82f8-111">คุณสามารถเลือก **ปฏิทิน** หรือ **บัญชีการเงิน** ในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="f82f8-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f82f8-112">ค่าเริ่มต้นคือ **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="f82f8-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="f82f8-113">การคัดเลือกของคุณกำหนดตัวเลือกที่พร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="f82f8-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="f82f8-114">ฟิลด์นี้จะกำหนดวันที่และจำนวนเงินของการลงรายการบัญชีการตั้งค่าเสื่อมราคาตลอดปีปฏิทินดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f82f8-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="f82f8-115">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="f82f8-115">Calendar</span></span>

<span data-ttu-id="f82f8-116">คุณสามารถเลือกที่จะคงค่าเริ่มต้นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="f82f8-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="f82f8-117">ตัวเลือก **ปฏิทิน** อัพเดทค่าเสื่อมราคาโดยยึดวันที่ 1 มกราคมของทุกปีเป็นหลัก</span><span class="sxs-lookup"><span data-stu-id="f82f8-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="f82f8-118">โดยทั่วไป ฐานค่าเสื่อมราคาคือ มูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="f82f8-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="f82f8-119">ในตัวอย่างถัดไปของหัวข้อนี้ ฐานการคิดค่าเสื่อมราคาคือตัวเศษในนิพจน์แรกบนคอลัมน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f82f8-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="f82f8-120">ถ้าคุณเลือก **ปฏิทิน** เป็นปีค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**:</span><span class="sxs-lookup"><span data-stu-id="f82f8-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f82f8-121">**รายปี** ลงรายการบัญชียอดเงินในวันที่ 31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="f82f8-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="f82f8-122">**รายเดือน** ลงรายการบัญชีจำนวนเงินรายเดือนเมื่อสิ้นสุดเดือนปฏิทินแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="f82f8-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="f82f8-123">**รายไตรมาส** ลงรายการบัญชีจำนวนเงินรายไตรมาส เมื่อสิ้นสุดไตรมาสปฏิทินแต่ละไตรมาส (31 มีนาคม 30 มิถุนายน 30 กันยายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="f82f8-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="f82f8-124">**ทุกครึ่งปี** งรายการบัญชีจำนวนเงินรายครึ่งปี ณ ครึ่งปีปฏิทิน (30 มิถุนายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="f82f8-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="f82f8-125">ลงรายการบัญชี **รายวัน** ยอดเงินค่าเสื่อมราคาสำหรับวิธีคิดค่าเสื่อมราคารายวันโดยใช้ธุรกรรมหนึ่งรายการสำหรับแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="f82f8-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="f82f8-126">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f82f8-126">Fiscal</span></span>

<span data-ttu-id="f82f8-127">ถ้าคุณเลือก **ทางการเงิน** ในฟิลด์ **ปีการคิดค่าเสื่อมราคา** การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125% จะถูกคำนวณตามปีบัญชีสำหรับปฏิทินทางการเงินที่ระบุไว้สำหรับสมุดบัญชี หรือสำหรับปฏิทินทางการเงินที่ถูกเลือกในหน้า **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="f82f8-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="f82f8-128">ปฏิทินทางการเงินถูกตั้งค่าบนหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="f82f8-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="f82f8-129">ตัวอย่างเช่น สำหรับปีบัญชีวันที่ 1 กรกฎาคมถึง 30 มิถุนายน การคำนวณค่าเสื่อมราคาเริ่มต้นในวันที่ 1 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="f82f8-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="f82f8-130">ปีบัญชีอาจจะยาวกว่าหรือสั้นกว่า 12 เดือนได้ </span><span class="sxs-lookup"><span data-stu-id="f82f8-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="f82f8-131">ค่าเสื่อมราคาจะถูกปรับปรุงโดยอัตโนมัติในแต่ละรอบระยะเวลา และความยาวของปีบัญชีถัดไปจะถูกกำหนดโดยการตั้งค่ารอบระยะเวลาในหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="f82f8-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="f82f8-132">ถ้าคุณเลือก **ทางการเงิน** ซึ่งเป็นปีการคิดค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="f82f8-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f82f8-133">**รายปี** จะลงรายการบัญชีของยอดรวมของค่าเสื่อมราคาที่คำนวณได้สำหรับปีบัญชีให้เป็นยอดเดียวในวันที่สุดท้ายของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="f82f8-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="f82f8-134">การลงรายการบัญชี **รอบระยะเวลาทางบัญชี** ยอดเงินของค่าเสื่อมราคาจะถูกคำนวณสำหรับปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="f82f8-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="f82f8-135">ยอดเงินนี้ถูกสะสมไว้ในรอบระยะเวลาทางบัญชีที่กำหนดไว้ในหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="f82f8-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="f82f8-136">ตัวอย่างช่น การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125%</span><span class="sxs-lookup"><span data-stu-id="f82f8-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="f82f8-137">ต้นทุนการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f82f8-137">Acquisition cost</span></span>               | <span data-ttu-id="f82f8-138">11,000</span><span class="sxs-lookup"><span data-stu-id="f82f8-138">11,000</span></span> |
| <span data-ttu-id="f82f8-139">มูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="f82f8-139">Salvage value</span></span>                  | <span data-ttu-id="f82f8-140">1,000</span><span class="sxs-lookup"><span data-stu-id="f82f8-140">1,000</span></span>  |
| <span data-ttu-id="f82f8-141">ฐานการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="f82f8-141">Depreciation base</span></span>              | <span data-ttu-id="f82f8-142">10,000</span><span class="sxs-lookup"><span data-stu-id="f82f8-142">10,000</span></span> |
| <span data-ttu-id="f82f8-143">ปีสำหรับอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f82f8-143">Service life years</span></span>             | <span data-ttu-id="f82f8-144">5</span><span class="sxs-lookup"><span data-stu-id="f82f8-144">5</span></span>      |
| <span data-ttu-id="f82f8-145">เปอร์เซ็นต์ค่าเสื่อมราคาต่อปี</span><span class="sxs-lookup"><span data-stu-id="f82f8-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="f82f8-146">25%</span><span class="sxs-lookup"><span data-stu-id="f82f8-146">25%</span></span>    |

<span data-ttu-id="f82f8-147">วิธียอดดุลที่ลดลง 125% แบ่งเป็น 125 เปอร์เซ็นต์ด้วยปีของอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f82f8-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="f82f8-148">เปอร์เซ็นต์ดังกล่าวจะถูกคูณด้วยมูลค่าตามบัญชีสุทธิของสินทรัพย์เพื่อกำหนดจำนวนเงินค่าเสื่อมราคาสำหรับปี</span><span class="sxs-lookup"><span data-stu-id="f82f8-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="f82f8-149">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="f82f8-149">Period</span></span> | <span data-ttu-id="f82f8-150">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="f82f8-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="f82f8-151">มูลค่าตามบัญชี</span><span class="sxs-lookup"><span data-stu-id="f82f8-151">Book value</span></span>                    | <span data-ttu-id="f82f8-152">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="f82f8-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="f82f8-153">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="f82f8-153">Year 1</span></span> | <span data-ttu-id="f82f8-154">(11,000 – 1,000) × 25% = 2,500</span><span class="sxs-lookup"><span data-stu-id="f82f8-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="f82f8-155">(11,000 – 2,500) = 8,500</span><span class="sxs-lookup"><span data-stu-id="f82f8-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="f82f8-156">(11,000 – 1,000 – 2,500) = 7,500</span><span class="sxs-lookup"><span data-stu-id="f82f8-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="f82f8-157">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="f82f8-157">Year 2</span></span> | <span data-ttu-id="f82f8-158">7,500 × 25% = 1,875</span><span class="sxs-lookup"><span data-stu-id="f82f8-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="f82f8-159">(8,500 – 1,875) = 6,625</span><span class="sxs-lookup"><span data-stu-id="f82f8-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="f82f8-160">(7,500 – 1,875) = 5,625</span><span class="sxs-lookup"><span data-stu-id="f82f8-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="f82f8-161">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="f82f8-161">Year 3</span></span> | <span data-ttu-id="f82f8-162">5,625 × 25% = 1,406.25</span><span class="sxs-lookup"><span data-stu-id="f82f8-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="f82f8-163">(6,625 – 1,406.25) = 5,218.75</span><span class="sxs-lookup"><span data-stu-id="f82f8-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="f82f8-164">(5,625 – 1,406.25) = 4,218.75</span><span class="sxs-lookup"><span data-stu-id="f82f8-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="f82f8-165">โดยทั่วไป เมื่อยอดเงินถูกคำนวณโดยใช้วิธีค่าเสื่อมราคายอดดุลที่ลดลง 125% มีน้อยกว่ายอดเงินที่จะถูกคำนวณโดยใช้วิธีเส้นตรง จะมีการแปลงไปยังวิธีเส้นตรงสำหรับอายุที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f82f8-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




