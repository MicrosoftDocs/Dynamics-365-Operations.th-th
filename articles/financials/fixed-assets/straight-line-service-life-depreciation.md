---
title: "การคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรง"
description: "บทความนี้แสดงภาพรวมอายุบริการคงเหลือแบบเส้นตรงของค่าเสื่อมราคา"
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b8c078841ca2e4bd994bbfbbe2abb130a4cf6fa
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="55dab-103">การคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="55dab-103">Straight line service life depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="55dab-104">บทความนี้แสดงภาพรวมอายุบริการคงเหลือแบบเส้นตรงของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="55dab-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="55dab-105">เมื่อคุณตั้งค่าโพรไฟล์ค่าเสื่อมราคาสินทรัพย์ถาวร และเลือกค่าเสื่อมราคาบริการแบบเส้นตรงในฟิลด์วิธีการหน้าโพรไฟล์ค่าเสื่อมราคา สินทรัพย์ที่ถูกกำหนดโพรไฟล์ค่าเสื่อมราคานี้จะถูกคิดค่าเสื่อมราคาจากอายุบริการรวมของสินทรัพย์นั้น</span><span class="sxs-lookup"><span data-stu-id="55dab-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="55dab-106">โดยทั่วไปจะได้ยอดค่าเสื่อมราคาเดียวกันในแต่ละรอบระยะเวลาการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="55dab-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="55dab-107">ความแตกต่างเพียงในยอดค่าเสื่อมราคาที่คำนวณได้ระหว่างวิธีคิดค่าเสื่อมราคาตามอายุการใช้งานคงเหลือแบบเส้นตรงและวิธีคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรงคือเมื่อมีการปรับปรุงการลงรายการบัญชีที่สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="55dab-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="55dab-108">การตั้งค่าการคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรง คุณต้องเลือกตัวเลือกในฟิลด์ปีที่คิดค่าเสื่อมราคาและความถี่ของรอบระยะเวลาในหน้าโพรไฟล์การคิดค่าเสื่อมราคาด้วย</span><span class="sxs-lookup"><span data-stu-id="55dab-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="55dab-109">เลือกปีการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="55dab-109">Select a depreciation year</span></span>
<span data-ttu-id="55dab-110">คุณสามารถเลือกปีปฏิทินหรือปีบัญชีในฟิลด์ปีที่คิดค่าเสื่อมราคาในหน้าโพรไฟล์การคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="55dab-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="55dab-111">การเลือกกำหนดตัวเลือกที่พร้อมใช้งานในฟิลด์ความถี่ของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="55dab-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="55dab-112">ตัวเลือกเริ่มต้นคือ ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="55dab-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="55dab-113">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="55dab-113">Calendar</span></span>

<span data-ttu-id="55dab-114">ถ้าคุณเลือกปฏิทิน ปีของวันที่ 1 มกราคมถึง 31 ธันวาคมจะถูกกำหนด ถึงแม้ว่าคุณได้กำหนดปฏิทินทางบัญชีแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="55dab-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="55dab-115">ตัวเลือกปฏิทินอัพเดตฐานค่าเสื่อมราคา ซึ่งโดยปกติคือมูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก ในวันที่ 1 มกราคมของทุกปี</span><span class="sxs-lookup"><span data-stu-id="55dab-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="55dab-116">ในตัวอย่างถัดไปของหัวข้อนี้ ฐานการคิดค่าเสื่อมราคาคือตัวเศษในนิพจน์แรกบนคอลัมน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="55dab-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="55dab-117">ถ้าคุณเลือกปฏิทิน ตัวเลือกดังต่อไปนี้จะพร้อมใช้งานในฟิลด์ความถี่ของรอบระยะเวลา ซึ่งกำหนดวันที่และจำนวนเงินของการลงรายการบัญชีการรับรู้ค่าเสื่อมราคาตลอดปีปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="55dab-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="55dab-118">การลงรายการบัญชีรายปีด้วยยอดเงินในวันที่ 31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="55dab-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="55dab-119">ลงรายการบัญชีรายเดือนด้วยจำนวนเงินรายเดือนเมื่อสิ้นสุดเดือนปฏิทินแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="55dab-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="55dab-120">ลงรายการบัญชีรายไตรมาสด้วยจำนวนเงินรายไตรมาส เมื่อสิ้นสุดไตรมาสของปฏิทินแต่ละไตรมาส (31 มีนาคม 30 มิถุนายน 30 กันยายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="55dab-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="55dab-121">การลงรายการบัญชีครึ่งปีด้วยจำนวนเงินครึ่งปี ณ ครึ่งปีปฏิทิน (30 มิถุนายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="55dab-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="55dab-122">ลงรายการบัญชีรายวันยอดเงินค่าเสื่อมราคาสำหรับวิธีคิดค่าเสื่อมราคาต่อวัน โดยการใช้ธุรกรรมหนึ่งรายการสำหรับแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="55dab-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="55dab-123">ตัวอย่างเช่น ถ้าคุณเลือกรายปี ค่าเสื่อมราคารายปีจะถูกบันทึกบัญชีเพียงครั้งเดียว ในวันที่ 31 ธันวาคมของแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="55dab-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="55dab-124">ถ้าคุณเลือกรายเดือน ค่าเสื่อมราคารายเดือนจะถูกบันทึกลงในแต่ละเดือน เป็นหนึ่งในสิบสองเดือนของจำนวนค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="55dab-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="55dab-125">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="55dab-125">Fiscal</span></span>

<span data-ttu-id="55dab-126">ถ้าคุณเลือกปีบัญชีในฟิลด์ปีค่าเสื่อมราคา การคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรงจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="55dab-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="55dab-127">โดยจะคำนวณตามปีบัญชี ซึ่งกำหนดโดยปฏิทินทางบัญชีที่ระบุสำหรับสมุดบัญชี หรือปฏิทินทางบัญชีที่ถูกเลือกในหน้าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="55dab-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="55dab-128">ปฏิทินทางบัญชีถูกตั้งค่าในหน้าปฏิทินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="55dab-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="55dab-129">ตัวอย่างเช่น สำหรับปีบัญชีวันที่ 1 กรกฎาคมถึง 30 มิถุนายน การคำนวณค่าเสื่อมราคาเริ่มต้นในวันที่ 1 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="55dab-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="55dab-130">ปีบัญชีอาจจะยาวกว่าหรือสั้นกว่า 12 เดือนได้ </span><span class="sxs-lookup"><span data-stu-id="55dab-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="55dab-131">ค่าเสื่อมราคาที่จะปรับปรุงโดยอัตโนมัติสำหรับแต่ละรอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="55dab-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="55dab-132">ความยาวของปีบัญชีถัดไปจะขึ้นอยู่กับรอบระยะเวลาทางบัญชีที่คุณตั้งค่าเมื่อคุณสร้างปีบัญชีใหม่ในแบบฟอร์มปฏิทินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="55dab-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="55dab-133">ถ้าคุณเลือกปีบัญชี ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ความถี่ของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="55dab-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="55dab-134">การลงรายการบัญชีของยอดรวมของค่าเสื่อมราคารายปีที่คำนวณได้สำหรับปีบัญชีเป็นยอดเดียวในวันที่สุดท้ายของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="55dab-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="55dab-135">รอบระยะเวลาบัญชีจะคำนวณยอดรวมของค่าเสื่อมราคาสำหรับปีบัญชี ซึ่งจะคงค้างในรอบระยะเวลาที่กำหนดในแบบฟอร์มปฏิทินทางบัญชีสำหรับปฏิทินทางบัญชีนั้น</span><span class="sxs-lookup"><span data-stu-id="55dab-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="55dab-136">ตัวอย่าง: การคิดค่าเสื่อมราคาแบบเส้นตรงของสินทรัพย์ถาวรที่ไม่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="55dab-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="55dab-137">สมมติว่าสินทรัพย์ถาวรมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55dab-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="55dab-138">ต้นทุนการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="55dab-138">Acquisition cost</span></span>    | <span data-ttu-id="55dab-139">11,000</span><span class="sxs-lookup"><span data-stu-id="55dab-139">11,000</span></span> |
| <span data-ttu-id="55dab-140">มูลค่าซาก</span><span class="sxs-lookup"><span data-stu-id="55dab-140">Salvage value</span></span>       | <span data-ttu-id="55dab-141">1,000</span><span class="sxs-lookup"><span data-stu-id="55dab-141">1,000</span></span>  |
| <span data-ttu-id="55dab-142">ฐานการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="55dab-142">Depreciation base</span></span>   | <span data-ttu-id="55dab-143">10,000</span><span class="sxs-lookup"><span data-stu-id="55dab-143">10,000</span></span> |
| <span data-ttu-id="55dab-144">ปีสำหรับอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="55dab-144">Service life years</span></span>  | <span data-ttu-id="55dab-145">5</span><span class="sxs-lookup"><span data-stu-id="55dab-145">5</span></span>      |
| <span data-ttu-id="55dab-146">ค่าเสื่อมราคาต่อปี</span><span class="sxs-lookup"><span data-stu-id="55dab-146">Yearly depreciation</span></span> | <span data-ttu-id="55dab-147">2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-147">2,000</span></span>  |

<span data-ttu-id="55dab-148">คุณจะได้ยอดค่าเสื่อมราคาที่เท่ากันทุกปี</span><span class="sxs-lookup"><span data-stu-id="55dab-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="55dab-149">(ราคาต้นทุน - มูลค่าซาก) / จำนวนปีอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="55dab-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="55dab-150">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="55dab-150">Period</span></span> | <span data-ttu-id="55dab-151">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="55dab-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="55dab-152">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="55dab-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="55dab-153">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="55dab-153">Year 1</span></span> | <span data-ttu-id="55dab-154">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55dab-155">9,000</span><span class="sxs-lookup"><span data-stu-id="55dab-155">9,000</span></span>                                 |
| <span data-ttu-id="55dab-156">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="55dab-156">Year 2</span></span> | <span data-ttu-id="55dab-157">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55dab-158">7,000</span><span class="sxs-lookup"><span data-stu-id="55dab-158">7,000</span></span>                                 |
| <span data-ttu-id="55dab-159">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="55dab-159">Year 3</span></span> | <span data-ttu-id="55dab-160">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55dab-161">5,000</span><span class="sxs-lookup"><span data-stu-id="55dab-161">5,000</span></span>                                 |
| <span data-ttu-id="55dab-162">ปีที่ 4</span><span class="sxs-lookup"><span data-stu-id="55dab-162">Year 4</span></span> | <span data-ttu-id="55dab-163">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55dab-164">3,000</span><span class="sxs-lookup"><span data-stu-id="55dab-164">3,000</span></span>                                 |
| <span data-ttu-id="55dab-165">ปีที่ 5</span><span class="sxs-lookup"><span data-stu-id="55dab-165">Year 5</span></span> | <span data-ttu-id="55dab-166">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="55dab-167">1,000</span><span class="sxs-lookup"><span data-stu-id="55dab-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="55dab-168">ตัวอย่าง: การคิดค่าเสื่อมราคาแบบเส้นตรงของสินทรัพย์ถาวรที่มีการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="55dab-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="55dab-169">สมมติว่าคุณเพิ่มการปรับปรุงการซื้อสินทรัพย์ 4,000 ในปีที่ 2 ให้กับสินทรัพย์ถาวรเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="55dab-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="55dab-170">อายุการใช้งานของการปรับปรุงการซื้อสินทรัพย์จะเหมือนกับของสินทรัพย์ถาวรและเริ่มต้นเมื่อซื้อสินทรัพย์นั้น</span><span class="sxs-lookup"><span data-stu-id="55dab-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="55dab-171">มูลค่าตามบัญชีสุทธิยังคงเหลืออยู่ ณ สิ้นปีที่ 5 สอดคล้องกับมูลค่าตามบัญชีสุทธิของการปรับปรุงการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="55dab-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="55dab-172">การคำนวณค่าเสื่อราคาตามรอบระยะเวลาแสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55dab-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="55dab-173">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="55dab-173">Period</span></span> | <span data-ttu-id="55dab-174">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="55dab-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="55dab-175">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="55dab-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="55dab-176">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="55dab-176">Year 1</span></span> | <span data-ttu-id="55dab-177">10,000 / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="55dab-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="55dab-178">11,000 - 2,000 = 9,000</span><span class="sxs-lookup"><span data-stu-id="55dab-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="55dab-179">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="55dab-179">Year 2</span></span> | <span data-ttu-id="55dab-180">4,000 (การปรับปรุงการซื้อสินทรัพย์)</span><span class="sxs-lookup"><span data-stu-id="55dab-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="55dab-181">9,000 + 4,000 =13,000</span><span class="sxs-lookup"><span data-stu-id="55dab-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="55dab-182">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="55dab-182">Year 2</span></span> | <span data-ttu-id="55dab-183">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="55dab-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55dab-184">13,000 - 2,800 = 10,200</span><span class="sxs-lookup"><span data-stu-id="55dab-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="55dab-185">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="55dab-185">Year 3</span></span> | <span data-ttu-id="55dab-186">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="55dab-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55dab-187">10,200 - 2,800 = 7,400</span><span class="sxs-lookup"><span data-stu-id="55dab-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="55dab-188">ปีที่ 4</span><span class="sxs-lookup"><span data-stu-id="55dab-188">Year 4</span></span> | <span data-ttu-id="55dab-189">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="55dab-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55dab-190">7,400 - 2,800 = 4,600</span><span class="sxs-lookup"><span data-stu-id="55dab-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="55dab-191">ปีที่ 5</span><span class="sxs-lookup"><span data-stu-id="55dab-191">Year 5</span></span> | <span data-ttu-id="55dab-192">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="55dab-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="55dab-193">4,600 - 2,800 = 1,800</span><span class="sxs-lookup"><span data-stu-id="55dab-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="55dab-194">ปีที่ 6</span><span class="sxs-lookup"><span data-stu-id="55dab-194">Year 6</span></span> | <span data-ttu-id="55dab-195">คงเหลือ 800*\*</span><span class="sxs-lookup"><span data-stu-id="55dab-195">Remaining 800\*</span></span>                           | <span data-ttu-id="55dab-196">1,800 - 800 = 1,000</span><span class="sxs-lookup"><span data-stu-id="55dab-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="55dab-197">\*เนื่องจากยอดคงเหลือน้อยกว่ายอดค่าเสื่อมราคา จะใช้เฉพาะยอดคงเหลือหักด้วยมูลค่าซากเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="55dab-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






