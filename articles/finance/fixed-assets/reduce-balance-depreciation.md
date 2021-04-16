---
title: การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง
description: บทความนี้แสดงภาพรวมยอดดุลที่ลดลงของค่าเสื่อมราคา
author: ShylaThompson
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25d34392819d9f687c306c1bf52153e0d074371a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826238"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="b5002-103">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="b5002-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5002-104">บทความนี้แสดงภาพรวมยอดดุลที่ลดลงของค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b5002-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="b5002-105">เมื่อคุณตั้งค่าโพรไฟล์การคิดค่าเสื่อมราคาสินทรัพย์ถาวร และเลือกยอดดุลที่ลดลงในฟิลด์วิธีบนหน้าโพรไฟล์การคิดค่าเสื่อมราคา สินทรัพย์ที่มีการกำหนดโพรไฟล์การคิดค่าเสื่อมราคาจะถูกคิดค่าเสื่อมราคาในเปอร์เซ็นต์เดียวกัน ในแต่ละรอบระยะเวลาการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b5002-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="b5002-106">ตั้งค่าการคิดค่าเสื่อมราคายอดดุลที่ลดลง คุณต้องทำการเลือกในฟิลด์สองฟิลด์บนแท็บด่วนทั่วไปของหน้าโพรไฟล์การคิดค่าเสื่อมราคาด้วย</span><span class="sxs-lookup"><span data-stu-id="b5002-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="b5002-107">อันดับแรก เลือกปีในฟิลด์ปีการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b5002-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="b5002-108">ขึ้นอยู่กับสิ่งที่เลือก ตัวเลือกต่าง ๆ ปรากฏขึ้นในฟิลด์ความถี่ของรอบระยะเวลา ตามที่อธิบายไว้ในส่วนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b5002-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="b5002-109">คุณต้องป้อนค่าในฟิลด์เปอร์เซ็นต์สำหรับโพรไฟล์การคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b5002-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="b5002-110">ถ้าคุณเลือกตัวเลือกการคิดค่าเสื่อมราคาเต็มจำนวน ข้อมูลพื้นฐานค่าเสื่อมราคาที่เหลือจะถูกนำมาใช้ในรอบระยะเวลาการคิดค่าเสื่อมราคาหลังสุด และอาจเป็นจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="b5002-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="b5002-111">บางประเทศ/ภูมิภาคไม่ใช้การคิดค่าเสื่อมราคาวิธีอื่นกับวิธีเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="b5002-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="b5002-112">การคิดค่าเสื่อมราคาวิธีอื่นเกิดขึ้นเมื่อยอดเงินการคิดค่าเสื่อมราคาสำรองมากกว่าหรือเท่ากับยอดเงินในโพรไฟล์ค่าเสื่อมราคาหลัก และยอดเงินค่าเสื่อมราคาที่ใช้เป็นยอดเงินในวิธีการสำรอง</span><span class="sxs-lookup"><span data-stu-id="b5002-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="b5002-113">เนื่องจากสินทรัพย์จะไม่ได้รับการคำนวณค่าเสื่อมราคาอย่างครบถ้วนตามการคำนวณเป็นเปอร์เซ็นต์ คุณต้องเลือกตัวเลือกค่าเสื่อมราคาแบบเต็มเพื่อคิดค่าเสื่อมราคาสินทรัพย์เต็มจำนวน</span><span class="sxs-lookup"><span data-stu-id="b5002-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b5002-114">เลือกปีการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b5002-114">Select a depreciation year</span></span>
<span data-ttu-id="b5002-115">คุณสามารถเลือกปีปฏิทินหรือปีบัญชีในฟิลด์ปีที่คิดค่าเสื่อมราคาในหน้าโพรไฟล์การคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b5002-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="b5002-116">การเลือกกำหนดตัวเลือกที่พร้อมใช้งานในฟิลด์ความถี่ของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b5002-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="b5002-117">ตัวเลือกเริ่มต้นคือ ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="b5002-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="b5002-118">ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="b5002-118">Calendar</span></span>

<span data-ttu-id="b5002-119">ตัวเลือกปฏิทินอัพเดตฐานค่าเสื่อมราคา ซึ่งโดยปกติคือมูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก ในวันที่ 1 มกราคมของทุกปี</span><span class="sxs-lookup"><span data-stu-id="b5002-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="b5002-120">ในตัวอย่างการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลงในหัวข้อนี้ ฐานการคิดค่าเสื่อมราคาคือตัวเศษในนิพจน์แรกบนคอลัมน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b5002-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b5002-121">ถ้าคุณเลือกปฏิทิน ตัวเลือกดังต่อไปนี้จะพร้อมใช้งานในฟิลด์ความถี่ของรอบระยะเวลา ซึ่งกำหนดวันที่และจำนวนเงินของการลงรายการบัญชีการรับรู้ค่าเสื่อมราคาตลอดปีปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="b5002-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="b5002-122">ลงรายการบัญชีรายปี ณ วันที่ 31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="b5002-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="b5002-123">ลงรายการบัญชีรายเดือนด้วยจำนวนเงินรายเดือนเมื่อสิ้นสุดเดือนปฏิทินแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="b5002-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b5002-124">ลงรายการบัญชีรายไตรมาสด้วยจำนวนเงินรายไตรมาส เมื่อสิ้นสุดไตรมาสของปฏิทินแต่ละไตรมาส (31 มีนาคม 30 มิถุนายน 30 กันยายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="b5002-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b5002-125">การลงรายการบัญชีครึ่งปีด้วยจำนวนเงินครึ่งปี ณ ครึ่งปีปฏิทิน (30 มิถุนายน และ 31 ธันวาคม)</span><span class="sxs-lookup"><span data-stu-id="b5002-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b5002-126">ลงรายการบัญชีรายวันยอดเงินค่าเสื่อมราคาสำหรับวิธีคิดค่าเสื่อมราคาต่อวัน โดยการใช้ธุรกรรมหนึ่งรายการสำหรับแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="b5002-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="b5002-127">ตัวอย่างเช่น ถ้าคุณเลือกรายปี ค่าเสื่อมราคารายปีจะถูกบันทึกบัญชีเพียงครั้งเดียว ในวันที่ 31 ธันวาคมของแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="b5002-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="b5002-128">ถ้าคุณเลือกรายเดือน ค่าเสื่อมราคารายเดือนจะถูกบันทึกลงในแต่ละเดือน เป็นหนึ่งในสิบสองเดือนของจำนวนค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="b5002-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b5002-129">ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="b5002-129">Fiscal</span></span>

<span data-ttu-id="b5002-130">ถ้าคุณเลือกปีบัญชีในฟิลด์ปีค่าเสื่อมราคา วิธีการคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรงจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="b5002-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="b5002-131">ซึ่งจะคำนวณตามปีบัญชี ซึ่งตั้งค่าไว้ในหน้าปฏิทินทางการเงินสำหรับปฏิทินทางการเงินที่เลือกในหน้าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="b5002-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="b5002-132">ตัวอย่างเช่น สำหรับปีบัญชีวันที่ 1 กรกฎาคมถึง 30 มิถุนายน การคำนวณค่าเสื่อมราคาเริ่มต้นในวันที่ 1 กรกฎาคม</span><span class="sxs-lookup"><span data-stu-id="b5002-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b5002-133">ปีบัญชีอาจจะยาวกว่าหรือสั้นกว่า 12 เดือนได้ </span><span class="sxs-lookup"><span data-stu-id="b5002-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b5002-134">ค่าเสื่อมราคาจะถูกปรับปรุงสำหรับแต่ละรอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="b5002-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="b5002-135">ความยาวของปีบัญชีถัดไปจะขึ้นอยู่กับรอบระยะเวลาทางบัญชีที่คุณตั้งค่าเมื่อคุณสร้างปีบัญชีใหม่ในหน้าปฏิทินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="b5002-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="b5002-136">ถ้าคุณเลือกปีบัญชี ตัวเลือกต่อไปนี้จะพร้อมใช้งานในฟิลด์ความถี่ของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b5002-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="b5002-137">ลงรายการบัญชีรายปีด้วยยอดรวมของค่าเสื่อมราคาที่คำนวณได้สำหรับปีบัญชีเป็นยอดเดียวในวันสุดท้ายของปีบัญชี</span><span class="sxs-lookup"><span data-stu-id="b5002-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b5002-138">รอบระยะเวลาทางบัญชีลงรายการบัญชียอดรวมของค่าเสื่อมราคาที่คำนวณได้สำหรับปีบัญชี ซึ่งถูกสะสมไว้ในรอบระยะเวลาทางบัญชีที่ถูกกำหนด สำหรับปฏิทินทางการเงินที่ถูกเลือกในหน้าบัญชีแยกประเภท หรือสำหรับปฏิทินทางการเงินที่ถูกเลือกสำหรับสมุดบัญชีสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b5002-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="b5002-139">ตัวอย่างของการคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="b5002-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="b5002-140">สมมติว่าราคาทุนของสินทรัพย์ถาวรคือ 11,000 มูลค่าซากคือ 1,000 และสัดส่วนเปอร์เซ็นต์การคิดค่าเสื่อมราคาคือ 30</span><span class="sxs-lookup"><span data-stu-id="b5002-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="b5002-141">เมื่อใช้วิธีการยอดดุลที่ลดลง จะมีการคำนวณ 30 เปอร์เซ็นต์ของฐานการคิดค่าเสื่อมราคา (มูลค่าตามบัญชีสุทธิลบด้วยมูลค่าซาก) เมื่อสิ้นสุดรอบระยะเวลาการคิดค่าเสื่อมราคาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b5002-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="b5002-142">การคิดค่าเสื่อมราคาสำหรับสามปีแรกแสดงไว้ที่ตารางด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="b5002-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="b5002-143">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b5002-143">Period</span></span> | <span data-ttu-id="b5002-144">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="b5002-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="b5002-145">มูลค่าตามบัญชีสุทธิ ณ สิ้นปี</span><span class="sxs-lookup"><span data-stu-id="b5002-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="b5002-146">ปีที่ 1</span><span class="sxs-lookup"><span data-stu-id="b5002-146">Year 1</span></span> | <span data-ttu-id="b5002-147">(11,000 - 1,000) \* 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="b5002-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="b5002-148">(11,000 - 1,000) - 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="b5002-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="b5002-149">ปีที่ 2</span><span class="sxs-lookup"><span data-stu-id="b5002-149">Year 2</span></span> | <span data-ttu-id="b5002-150">(7,000 - 1,000) \* 30% = 1,800</span><span class="sxs-lookup"><span data-stu-id="b5002-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="b5002-151">(7,000 -1,800) = 5,200</span><span class="sxs-lookup"><span data-stu-id="b5002-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="b5002-152">ปีที่ 3</span><span class="sxs-lookup"><span data-stu-id="b5002-152">Year 3</span></span> | <span data-ttu-id="b5002-153">(5,200 - 1,000) \* 30% = 1,260</span><span class="sxs-lookup"><span data-stu-id="b5002-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="b5002-154">(5,200 - 1,260) = 3,940</span><span class="sxs-lookup"><span data-stu-id="b5002-154">(5,200 - 1,260) = 3,940</span></span>               |


-







[!INCLUDE[footer-include](../../includes/footer-banner.md)]