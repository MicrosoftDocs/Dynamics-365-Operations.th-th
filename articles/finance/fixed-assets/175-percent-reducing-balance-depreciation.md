---
title: ค่าเสื่อมราคายอดดุลที่ลดลง 175%
description: หัวข้อนี้แสดงภาพรวมวิธีการที่ยอดดุลลดลง 175% ของค่าเสื่อมราคา
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a21c315aa9a7193c20e4184da20d4d6d38386c4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180143"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="1997f-103">ค่าเสื่อมราคายอดดุลที่ลดลง 175%</span><span class="sxs-lookup"><span data-stu-id="1997f-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1997f-104">หัวข้อนี้แสดงภาพรวมวิธีการที่ยอดดุลลดลง 175% ของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1997f-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="1997f-105">เมื่อคุณตั้งค่าโพรไฟล์การคิดค่าเสื่อมราคาสินทรัพย์ถาวร และเลือกค่า **ยอดดุลที่ลดลง 175%** ในฟิลด์ **วิธี** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา** สินทรัพย์ถาวรที่มีการกำหนดโพรไฟล์การคิดค่าเสื่อมราคาจะถูกคิดค่าเสื่อมราคาในอัตราเปอร์เซ็นต์เดียวกัน ในแต่ละรอบระยะเวลาการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1997f-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="1997f-106">เพื่อตั้งค่าการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 175% คุณยังต้องเลือกตัวเลือกอื่นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** และฟิลด์ **ความถี่ของรอบระยะเวลา** บนหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="1997f-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1997f-107">ตัวเลือกที่จะปรากฎบนฟิลด์ **ความถี่ของรอบระยะเวลา** นั้นจะแตกต่างกันไป ขึ้นอยู่กับค่าที่ถูกเลือกในฟิลด์ **ปีการคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="1997f-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="1997f-108">เลือกปีการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1997f-108">Select a depreciation year</span></span>
<span data-ttu-id="1997f-109">คุณสามารถเลือก **ปฏิทิน** หรือ **บัญชีการเงิน** ในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** ในหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="1997f-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1997f-110">ค่าเริ่มต้นคือ **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="1997f-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="1997f-111">การคัดเลือกของคุณกำหนดตัวเลือกที่พร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="1997f-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="1997f-112">ฟิลด์นี้จะกำหนดวันที่และจำนวนเงินของการลงรายการบัญชีการตั้งค่าเสื่อมราคาตลอดปีปฏิทินดังนี้:</span><span class="sxs-lookup"><span data-stu-id="1997f-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="1997f-113">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="1997f-113">Calendar</span></span>

<span data-ttu-id="1997f-114">คุณสามารถเลือกที่จะคงค่าเริ่มต้นในฟิลด์ **ปีที่คิดค่าเสื่อมราคา** **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="1997f-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="1997f-115">ตัวเลือก **ปฏิทิน** อัพเดทค่าเสื่อมราคาโดยยึดวันที่ 1 มกราคมของทุกปีเป็นหลัก</span><span class="sxs-lookup"><span data-stu-id="1997f-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="1997f-116">โดยทั่วไป ฐานค่าเสื่อมราคาคือ มูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="1997f-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="1997f-117">ในตัวอย่างถัดไปของหัวข้อนี้ ฐานการคิดค่าเสื่อมราคาคือตัวเศษในนิพจน์แรกบนคอลัมน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1997f-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="1997f-118">ถ้าคุณเลือก **ปฏิทิน** เป็นปีค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**:</span><span class="sxs-lookup"><span data-stu-id="1997f-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="1997f-119">**รายปี** ลงรายการบัญชียอดเงินในวันที่ 31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="1997f-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="1997f-120">**รายเดือน** ลงรายการบัญชีจำนวนเงินรายเดือนเมื่อสิ้นสุดเดือนปฏิทินแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="1997f-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="1997f-121">**รายไตรมาส** ลงรายการบัญชีจำนวนเงินรายไตรมาส เมื่อสิ้นสุดไตรมาสปฏิทินแต่ละไตรมาส (31 มีนาคม 30 มิถุนายน 30 กันยายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="1997f-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="1997f-122">**ทุกครึ่งปี** งรายการบัญชีจำนวนเงินรายครึ่งปี ณ ครึ่งปีปฏิทิน (30 มิถุนายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="1997f-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="1997f-123">ลงรายการบัญชี **รายวัน** ยอดเงินค่าเสื่อมราคาสำหรับวิธีคิดค่าเสื่อมราคารายวันโดยใช้ธุรกรรมหนึ่งรายการสำหรับแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="1997f-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="1997f-124">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="1997f-124">Fiscal</span></span>

<span data-ttu-id="1997f-125">ถ้าคุณเลือก **ทางการเงิน** ในฟิลด์ **ปีการคิดค่าเสื่อมราคา** การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 175% จะถูกคำนวณตามปีบัญชีสำหรับปฏิทินทางการเงินที่ระบุไว้สำหรับสมุดบัญชี หรือสำหรับปฏิทินทางการเงินที่ถูกเลือกในหน้า **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="1997f-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="1997f-126">ปฏิทินทางการเงินถูกตั้งค่าบนหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="1997f-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="1997f-127">สำหรับข้อมูลเพิ่มเติม ดู [ปฏิทินทางการเงิน ปีบัญชี และรอบระยะเวลา](../budgeting/fiscal-calendars-fiscal-years-periods.md)</span><span class="sxs-lookup"><span data-stu-id="1997f-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="1997f-128">ตัวอย่างเช่น สำหรับปีบัญชีวันที่ 1 กรกฎาคมถึง 30 มิถุนายน การคำนวณค่าเสื่อมราคาเริ่มต้นในวันที่ 1 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="1997f-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="1997f-129">ปีบัญชีอาจจะยาวกว่าหรือสั้นกว่า 12 เดือนได้ </span><span class="sxs-lookup"><span data-stu-id="1997f-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="1997f-130">ค่าเสื่อมราคาจะถูกปรับปรุงโดยอัตโนมัติในแต่ละรอบระยะเวลา และความยาวของปีบัญชีถัดไปจะถูกกำหนดโดยการตั้งค่ารอบระยะเวลาในหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="1997f-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="1997f-131">ถ้าคุณเลือก **ทางการเงิน** ซึ่งเป็นปีการคิดค่าเสื่อมราคา ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ **ความถี่ของรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="1997f-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="1997f-132">**รายปี** ลงรายการบัญชียอดรวมของค่าเสื่อมราคาที่คำนวณไว้สำหรับปีบัญชีในวันที่สุดท้ายของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="1997f-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="1997f-133">**รอบระยะเวลาทางบัญชี** คำนวณยอดรวมของค่าเสื่อมราคาสำหรับปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="1997f-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="1997f-134">ยอดเงินนี้ถูกสะสมไว้ในรอบระยะเวลาทางบัญชีที่กำหนดไว้ในหน้า **ปฏิทินทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="1997f-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="1997f-135">ตัวอย่างเช่น การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 175%</span><span class="sxs-lookup"><span data-stu-id="1997f-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="1997f-136">ต้นทุนการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1997f-136">Acquisition cost</span></span>               | <span data-ttu-id="1997f-137">11,000</span><span class="sxs-lookup"><span data-stu-id="1997f-137">11,000</span></span> |
| <span data-ttu-id="1997f-138">มูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="1997f-138">Salvage value</span></span>                  | <span data-ttu-id="1997f-139">1,000</span><span class="sxs-lookup"><span data-stu-id="1997f-139">1,000</span></span>  |
| <span data-ttu-id="1997f-140">ฐานการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1997f-140">Depreciation base</span></span>              | <span data-ttu-id="1997f-141">10,000</span><span class="sxs-lookup"><span data-stu-id="1997f-141">10,000</span></span> |
| <span data-ttu-id="1997f-142">ปีสำหรับอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1997f-142">Service life years</span></span>             | <span data-ttu-id="1997f-143">5</span><span class="sxs-lookup"><span data-stu-id="1997f-143">5</span></span>      |
| <span data-ttu-id="1997f-144">เปอร์เซ็นต์ค่าเสื่อมราคาต่อปี</span><span class="sxs-lookup"><span data-stu-id="1997f-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="1997f-145">35%</span><span class="sxs-lookup"><span data-stu-id="1997f-145">35%</span></span>    |

<span data-ttu-id="1997f-146">วิธีการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 175% จะหาร 175 ด้วยจำนวนปีของอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1997f-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="1997f-147">เปอร์เซ็นต์ดังกล่าวจะถูกคูณด้วยมูลค่าตามบัญชีสุทธิของสินทรัพย์เพื่อกำหนดจำนวนเงินค่าเสื่อมราคาสำหรับปี</span><span class="sxs-lookup"><span data-stu-id="1997f-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="1997f-148">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="1997f-148">Period</span></span> | <span data-ttu-id="1997f-149">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="1997f-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="1997f-150">มูลค่าตามบัญชี</span><span class="sxs-lookup"><span data-stu-id="1997f-150">Book value</span></span>                  | <span data-ttu-id="1997f-151">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="1997f-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="1997f-152">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="1997f-152">Year 1</span></span> | <span data-ttu-id="1997f-153">(11,000 – 1,000) × 35% = 3,500</span><span class="sxs-lookup"><span data-stu-id="1997f-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="1997f-154">11,000 – 3,500 = 7,500</span><span class="sxs-lookup"><span data-stu-id="1997f-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="1997f-155">11,000 – 1,000 – 3,500 = 6,500</span><span class="sxs-lookup"><span data-stu-id="1997f-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="1997f-156">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="1997f-156">Year 2</span></span> | <span data-ttu-id="1997f-157">6,500 × 35% = 2,275</span><span class="sxs-lookup"><span data-stu-id="1997f-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="1997f-158">7,500 – 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="1997f-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="1997f-159">6,500 – 2,275 = 4,225</span><span class="sxs-lookup"><span data-stu-id="1997f-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="1997f-160">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="1997f-160">Year 3</span></span> | <span data-ttu-id="1997f-161">4,225 × 35% = 1,478.75</span><span class="sxs-lookup"><span data-stu-id="1997f-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="1997f-162">5,225 – 1,478.75 = 3,746.25</span><span class="sxs-lookup"><span data-stu-id="1997f-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="1997f-163">4,225 – 1,478.75 = 2,746.25</span><span class="sxs-lookup"><span data-stu-id="1997f-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="1997f-164">โดยทั่วไป เมื่อยอดเงินถูกคำนวณโดยใช้วิธีค่าเสื่อมราคายอดดุลที่ลดลง 175% มีน้อยกว่ายอดเงินที่จะถูกคำนวณโดยใช้วิธีเส้นตรง จะมีการแปลงไปยังวิธีเส้นตรงสำหรับอายุที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="1997f-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



