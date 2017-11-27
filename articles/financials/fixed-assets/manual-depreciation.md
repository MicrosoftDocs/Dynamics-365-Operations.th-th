---
title: "การคิดค่าเสื่อมราคาด้วยตนเอง"
description: "บทความนี้แสดงภาพรวมของวิธีคิดค่าเสื่อมราคาด้วยตนเอง"
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
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d7a672b80a0da7ab05acf5b5efe041f0f89c0042
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="9f01a-103">การคิดค่าเสื่อมราคาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9f01a-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9f01a-104">บทความนี้แสดงภาพรวมของวิธีคิดค่าเสื่อมราคาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9f01a-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="9f01a-105">เมื่อคุณตั้งค่าการคิดค่าเสื่อมราคาสินทรัพย์ถาวรและเลือก **กำหนดเอง** ในฟิลด์ **วิธีการ** บนหน้า **โพรไฟล์การคิดค่าเสื่อมราคา** ค่าเสื่อมราคาของสินทรัพย์ถาวรที่มีการกำหนดให้กับโพรไฟล์การคิดค่าเสื่อมราคานี้ จะถูกกำหนดโดยเปอร์เซ็นต์ที่คุณป้อนสำหรับแต่ละช่วงเวลาในปีปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="9f01a-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="9f01a-106">ช่วงเวลาที่คุณตั้งค่าเปอร์เซ็นต์จะมีการลงรายการบัญชีตามค่าที่คุณเลือกไว้ในฟิลด์ **ความถี่ของรอบระยะเวลา** บนแท็บด่วน **ทั่วไป** ของหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="9f01a-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="9f01a-107">ต่อไปนี้เป็นค่าที่คุณสามารถเลือกได้:</span><span class="sxs-lookup"><span data-stu-id="9f01a-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="9f01a-108">ทุกปี</span><span class="sxs-lookup"><span data-stu-id="9f01a-108">Yearly</span></span>
-   <span data-ttu-id="9f01a-109">ทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="9f01a-109">Monthly</span></span>
-   <span data-ttu-id="9f01a-110">รายไตรมาส</span><span class="sxs-lookup"><span data-stu-id="9f01a-110">Quarterly</span></span>
-   <span data-ttu-id="9f01a-111">ทุกครึ่งปี</span><span class="sxs-lookup"><span data-stu-id="9f01a-111">Half-Yearly</span></span>
-   <span data-ttu-id="9f01a-112">รายวัน</span><span class="sxs-lookup"><span data-stu-id="9f01a-112">Daily</span></span>

<span data-ttu-id="9f01a-113">หลังจากคุณเลือกความถี่ของรอบระยะเวลา ให้คลิก **กำหนดการที่กำหนดเอง**และตั้งค่าเปอร์เซ็นต์สำหรับช่วงเวลาการลงรายการบัญชีแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="9f01a-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="9f01a-114">เมื่อรวมกันแล้ว กำหนดการที่กำหนดเองและช่วงเวลาของการลงรายการบัญชีจะเป็นตัวกำหนดยอดค่าเสื่อมราคา ดังที่แสดงในตัวอย่างในบทความหลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="9f01a-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="9f01a-115">การคิดค่าเสื่อมราคาด้วยตนเองจะถูกคำนวณเป็นเปอร์เซ็นต์ของราคาทุนของสินทรัพย์เสมอ</span><span class="sxs-lookup"><span data-stu-id="9f01a-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="9f01a-116">สำหรับการคิดค่าเสื่อมราคาด้วยตนเอง เปอร์เซ็นต์ที่คุณป้อนในช่วงของค่าเสื่อมราคาไม่ต้องรวมกันได้ 100%</span><span class="sxs-lookup"><span data-stu-id="9f01a-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="9f01a-117">การคิดค่าเสื่อมราคาด้วยตนเองเป็นวิธีการคิดค่าเสื่อมราคาที่ยืดหยุ่นซึ่งมักใช้เพื่อกำหนดโพรไฟล์ค่าเสื่อมราคาพิเศษบนหน้า **สมุดบัญชี** เช่นการคิดค่าเสื่อมราคาที่ไม่ใช่ประจำงวดสำหรับวัตถุประสงค์พิเศษ (ตัวอย่างเช่น ภาษี)</span><span class="sxs-lookup"><span data-stu-id="9f01a-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="9f01a-118">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="9f01a-118">Examples</span></span>
<span data-ttu-id="9f01a-119">ราคาทุนของสินทรัพย์: มูลค่าซากที่คาดไว้คือ 11,000.00: 1,000.00 ตารางต่อไปนี้แสดงช่วงเวลาและเปอร์เซ็นต์ที่คุณตั้งค่าบนหน้า **กำหนดการโพรไฟล์ค่าเสื่อมราคาสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9f01a-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="9f01a-120">หมายเลขช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="9f01a-120">Interval number</span></span> | <span data-ttu-id="9f01a-121">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="9f01a-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="9f01a-122">1</span><span class="sxs-lookup"><span data-stu-id="9f01a-122">1</span></span>               | <span data-ttu-id="9f01a-123">10.00</span><span class="sxs-lookup"><span data-stu-id="9f01a-123">10.00</span></span>      |
| <span data-ttu-id="9f01a-124">2</span><span class="sxs-lookup"><span data-stu-id="9f01a-124">2</span></span>               | <span data-ttu-id="9f01a-125">50.00</span><span class="sxs-lookup"><span data-stu-id="9f01a-125">50.00</span></span>      |
| <span data-ttu-id="9f01a-126">3</span><span class="sxs-lookup"><span data-stu-id="9f01a-126">3</span></span>               | <span data-ttu-id="9f01a-127">8.00</span><span class="sxs-lookup"><span data-stu-id="9f01a-127">8.00</span></span>       |

<span data-ttu-id="9f01a-128">ตารางต่อไปนี้แสดงวิธีคำนวณค่าเสื่อมราคาสำหรับแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="9f01a-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="9f01a-129">หมายเลขช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="9f01a-129">Interval number</span></span> | <span data-ttu-id="9f01a-130">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="9f01a-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="9f01a-131">มูลค่าตามบัญชีสุทธิเมื่อสิ้นสุดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="9f01a-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="9f01a-132">1</span><span class="sxs-lookup"><span data-stu-id="9f01a-132">1</span></span>                | <span data-ttu-id="9f01a-133">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="9f01a-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="9f01a-134">10,000 (11,000 – 1,000)</span><span class="sxs-lookup"><span data-stu-id="9f01a-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="9f01a-135">2</span><span class="sxs-lookup"><span data-stu-id="9f01a-135">2</span></span>                | <span data-ttu-id="9f01a-136">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="9f01a-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="9f01a-137">5,000 (10,000 – 5,000)</span><span class="sxs-lookup"><span data-stu-id="9f01a-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="9f01a-138">3</span><span class="sxs-lookup"><span data-stu-id="9f01a-138">3</span></span>                | <span data-ttu-id="9f01a-139">(11,000 – 1,000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="9f01a-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="9f01a-140">4,200 (5,000 – 800)</span><span class="sxs-lookup"><span data-stu-id="9f01a-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="9f01a-141">ถ้าคุณเลือก **ทุกเดือน** ในฟิลด์**ความถี่ของรอบระยะเวลา** คุณตั้งค่าช่วงเวลาของกำหนดการที่กำหนดเองเป็น 12 ช่วง</span><span class="sxs-lookup"><span data-stu-id="9f01a-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="9f01a-142">ตารางต่อไปนี้แสดงยอดค่าเสื่อมราคาสำหรับช่วงเวลาสองช่วงแรก</span><span class="sxs-lookup"><span data-stu-id="9f01a-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="9f01a-143">ช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="9f01a-143">Interval</span></span> | <span data-ttu-id="9f01a-144">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="9f01a-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="9f01a-145">มกราคม</span><span class="sxs-lookup"><span data-stu-id="9f01a-145">January</span></span>  | <span data-ttu-id="9f01a-146">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="9f01a-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="9f01a-147">กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="9f01a-147">February</span></span> | <span data-ttu-id="9f01a-148">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="9f01a-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="9f01a-149">ถ้าคุณเลือก **ทุกครึ่งปี** ในฟิลด์ ****ความถี่ของรอบระยะเวลา** คุณตั้งค่าช่วงเวลาของกำหนดการที่กำหนดเองเป็น 2 ช่วง</span><span class="sxs-lookup"><span data-stu-id="9f01a-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="9f01a-150">ตารางต่อไปนี้แสดงยอดค่าเสื่อมราคาสำหรับช่วงเวลาสองช่วงแรก</span><span class="sxs-lookup"><span data-stu-id="9f01a-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="9f01a-151">ช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="9f01a-151">Interval</span></span>    | <span data-ttu-id="9f01a-152">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="9f01a-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="9f01a-153">30 มิถุนายน</span><span class="sxs-lookup"><span data-stu-id="9f01a-153">June 30</span></span>     | <span data-ttu-id="9f01a-154">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="9f01a-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="9f01a-155">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="9f01a-155">December 31</span></span> | <span data-ttu-id="9f01a-156">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="9f01a-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="9f01a-157">ผลรวมของเปอร์เซ็นต์สำหรับช่วงเวลาทั้งหมดไม่จำเป็นต้องเป็น 100</span><span class="sxs-lookup"><span data-stu-id="9f01a-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="9f01a-158">อย่างไรก็ตาม คุณจะได้รับข้อความถ้าค่าในฟิลด์ **เปอร์เซ็นต์สะสม** ในหน้า **กำหนดการโพรไฟล์ค่าเสื่อมราคาสินทรัพย์ถาวร** ไม่เป็น **100**</span><span class="sxs-lookup"><span data-stu-id="9f01a-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




