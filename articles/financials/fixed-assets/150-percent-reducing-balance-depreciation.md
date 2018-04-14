---
title: "ค่าเสื่อมราคายอดดุลที่ลดลง 150%"
description: "บทความนี้แสดงภาพรวมยอดดุลที่ลดลง 150% ของค่าเสื่อมราคา"
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
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 931c12278853d87e6fddbb166b56c6079d40b142
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="35589-103">ค่าเสื่อมราคายอดดุลที่ลดลง 150%</span><span class="sxs-lookup"><span data-stu-id="35589-103">150 percent reducing balance depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="35589-104">บทความนี้แสดงภาพรวมยอดดุลที่ลดลง 150% ของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="35589-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="35589-105">เมื่อคุณตั้งค่าโพรไฟล์ค่าเสื่อมราคาสินทรัพย์ถาวร และเลือก **ยอดดุลที่ลดลง 150%** ในฟิลด์ **วิธี** ในหน้า **โพรไฟล์ค่าเสื่อมราคา** สินทรัพย์ถาวรที่ถูกกำหนดโพรไฟล์ค่าเสื่อมราคาจะถูกคิดค่าเสื่อมราคาในเปอร์เซ็นต์เดียวกันในแต่ละรอบระยะเวลาค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="35589-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="35589-106">เปอร์เซ็นต์นี้จะถูกคำนวณโดยอาศัยอายุการบริการของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="35589-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="35589-107">ตัวอย่างเช่น ถ้าสินทรัพย์มีอายุการบริการห้าปี เปอร์เซ็นต์จะถูกคำนวณเป็น 30 เปอร์เซ็นต์ (150% ÷ 5)</span><span class="sxs-lookup"><span data-stu-id="35589-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="35589-108">เพื่อตั้งค่าค่าเสื่อมราคายอดดุลที่ลดลง 150% คุณต้องเลือกตัวเลือกในฟิลด์ **ปีค่าเสื่อมราคา** และฟิลด์ **ความถี่ของรอบระยะเวลา** บนหน้า **โพรไฟล์ค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="35589-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="35589-109">ตัวเลือกที่จะปรากฎในฟิลด์ **ความถี่ของรอบระยะเวลา** จะแตกต่างกันไป ขึ้นอยู่กับค่าที่ถูกเลือกในฟิลด์ **ปีค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="35589-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="35589-110">การเลือกปีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="35589-110">Selection of depreciation year</span></span>
<span data-ttu-id="35589-111">คุณสามารถเลือก **ปฏิทิน** หรือ **บัญชีการเงิน** ในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** ในหน้า**โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="35589-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="35589-112">ค่าเริ่มต้นคือ **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="35589-112">The default value is **Calendar**.</span></span> <span data-ttu-id="35589-113">การคัดเลือกของคุณกำหนดตัวเลือกที่พร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="35589-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="35589-114">ฟิลด์นี้จะกำหนดวันที่และจำนวนเงินของการลงรายการบัญชีการตั้งค่าเสื่อมราคาตลอดปีปฏิทินดังนี้:</span><span class="sxs-lookup"><span data-stu-id="35589-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="35589-115">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="35589-115">Calendar</span></span>

<span data-ttu-id="35589-116">คุณสามารถเลือกที่จะคงค่าเริ่มต้นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="35589-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="35589-117">ตัวเลือก **ปฏิทิน** อัพเดทค่าเสื่อมราคาโดยยึดวันที่ 1 มกราคมของทุกปีเป็นหลัก</span><span class="sxs-lookup"><span data-stu-id="35589-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="35589-118">โดยทั่วไป ฐานค่าเสื่อมราคาคือ มูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="35589-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="35589-119">ในตัวอย่างถัดไปของหัวข้อนี้ ฐานการคิดค่าเสื่อมราคาคือตัวเศษในนิพจน์แรกบนคอลัมน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="35589-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="35589-120">ถ้าคุณเลือก **ปฏิทิน** เป็นปีค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**:</span><span class="sxs-lookup"><span data-stu-id="35589-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="35589-121">**รายปี** ลงรายการบัญชียอดเงินในวันที่ 31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="35589-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="35589-122">**รายเดือน** ลงรายการบัญชีจำนวนเงินรายเดือนเมื่อสิ้นสุดเดือนปฏิทินแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="35589-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="35589-123">**รายไตรมาส** ลงรายการบัญชีจำนวนเงินรายไตรมาส เมื่อสิ้นสุดไตรมาสปฏิทินแต่ละไตรมาส (31 มีนาคม 30 มิถุนายน 30 กันยายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="35589-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="35589-124">**ทุกครึ่งปี** งรายการบัญชีจำนวนเงินรายครึ่งปี ณ ครึ่งปีปฏิทิน (30 มิถุนายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="35589-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="35589-125">ลงรายการบัญชี **รายวัน** ยอดเงินค่าเสื่อมราคาสำหรับวิธีคิดค่าเสื่อมราคารายวันโดยใช้ธุรกรรมหนึ่งรายการสำหรับแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="35589-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="35589-126">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="35589-126">Fiscal</span></span>

<span data-ttu-id="35589-127">ถ้าคุณเลือก **ทางการเงิน** ในฟิลด์ปี **การคิดค่าเสื่อมราคา** การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 150% จะถูกคำนวณตามปีบัญชีสำหรับปฏิทินทางการเงินที่ระบุไว้สำหรับสมุดบัญชี หรือสำหรับปฏิทินทางการเงินที่ถูกเลือกในหน้า **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="35589-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="35589-128">ปฏิทินทางการเงินถูกตั้งค่าบนหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="35589-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="35589-129">ตัวอย่างเช่น สำหรับปีบัญชีวันที่ 1 กรกฎาคมถึง 30 มิถุนายน การคำนวณค่าเสื่อมราคาเริ่มต้นในวันที่ 1 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="35589-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="35589-130">ปีบัญชีอาจจะยาวกว่าหรือสั้นกว่า 12 เดือนได้ </span><span class="sxs-lookup"><span data-stu-id="35589-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="35589-131">ค่าเสื่อมราคาถูกปรับสำหรับแต่ละรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="35589-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="35589-132">ความยาวปีบัญชีถัดไปถูกกำหนดด้วยการตั้งค่าของรอบระยะเวลาบนหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="35589-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="35589-133">ถ้าคุณเลือก **ทางการเงิน** ซึ่งเป็นปีการคิดค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="35589-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="35589-134">**รายปี** ลงรายการบัญชียอดรวมของค่าเสื่อมราคาที่คำนวณไว้สำหรับปีบัญชีในวันที่สุดท้ายของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="35589-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="35589-135">การลงรายการบัญชี **รอบระยะเวลาทางบัญชี** ยอดเงินของค่าเสื่อมราคาจะถูกคำนวณสำหรับปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="35589-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="35589-136">ยอดเงินนี้ถูกสะสมไว้ในรอบระยะเวลาทางบัญชีที่กำหนดไว้ในหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="35589-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="35589-137">ตัวอย่างค่าเสื่อมราคายอดดุลที่ลดลง 150%</span><span class="sxs-lookup"><span data-stu-id="35589-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="35589-138">ต้นทุนการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="35589-138">Acquisition cost</span></span>               | <span data-ttu-id="35589-139">11,000</span><span class="sxs-lookup"><span data-stu-id="35589-139">11,000</span></span> |
| <span data-ttu-id="35589-140">มูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="35589-140">Salvage value</span></span>                  | <span data-ttu-id="35589-141">1,000</span><span class="sxs-lookup"><span data-stu-id="35589-141">1,000</span></span>  |
| <span data-ttu-id="35589-142">ฐานการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="35589-142">Depreciation base</span></span>              | <span data-ttu-id="35589-143">10,000</span><span class="sxs-lookup"><span data-stu-id="35589-143">10,000</span></span> |
| <span data-ttu-id="35589-144">ปีสำหรับอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="35589-144">Service life years</span></span>             | <span data-ttu-id="35589-145">5</span><span class="sxs-lookup"><span data-stu-id="35589-145">5</span></span>      |
| <span data-ttu-id="35589-146">เปอร์เซ็นต์ค่าเสื่อมราคาต่อปี</span><span class="sxs-lookup"><span data-stu-id="35589-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="35589-147">30%</span><span class="sxs-lookup"><span data-stu-id="35589-147">30%</span></span>    |

<span data-ttu-id="35589-148">วิธีของยอดดุลที่ลดลง 150% แบ่ง 150 เปอร์เซ็นต์ด้วยปีของอายุการบริการ</span><span class="sxs-lookup"><span data-stu-id="35589-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="35589-149">เปอร์เซ็นต์ดังกล่าวจะถูกคูณด้วยมูลค่าตามบัญชีสุทธิของสินทรัพย์เพื่อกำหนดจำนวนเงินค่าเสื่อมราคาสำหรับปี</span><span class="sxs-lookup"><span data-stu-id="35589-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="35589-150">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="35589-150">Period</span></span> | <span data-ttu-id="35589-151">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="35589-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="35589-152">มูลค่าตามบัญชี</span><span class="sxs-lookup"><span data-stu-id="35589-152">Book value</span></span>             | <span data-ttu-id="35589-153">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="35589-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="35589-154">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="35589-154">Year 1</span></span> | <span data-ttu-id="35589-155">(11,000 – 1,000)×30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="35589-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="35589-156">11,000 – 3,000 = 8,000</span><span class="sxs-lookup"><span data-stu-id="35589-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="35589-157">11,000 – 1,000 – 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="35589-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="35589-158">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="35589-158">Year 2</span></span> | <span data-ttu-id="35589-159">7,000 × 30% = 2,100</span><span class="sxs-lookup"><span data-stu-id="35589-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="35589-160">8,000 – 2,100 = 5,900</span><span class="sxs-lookup"><span data-stu-id="35589-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="35589-161">7,000 – 2,100 = 4,900</span><span class="sxs-lookup"><span data-stu-id="35589-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="35589-162">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="35589-162">Year 3</span></span> | <span data-ttu-id="35589-163">4,900 × 30% = 1,470</span><span class="sxs-lookup"><span data-stu-id="35589-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="35589-164">5,900 – 1,470 = 4,430</span><span class="sxs-lookup"><span data-stu-id="35589-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="35589-165">4,900 – 1,470 = 3,430</span><span class="sxs-lookup"><span data-stu-id="35589-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="35589-166">โดยทั่วไป เมื่อยอดเงินถูกคำนวณโดยใช้วิธีค่าเสื่อมราคายอดดุลที่ลดลง 150% มีน้อยกว่ายอดเงินที่จะถูกคำนวณโดยใช้วิธีเส้นตรง จะมีการแปลงไปยังวิธีเส้นตรงสำหรับอายุที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="35589-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




