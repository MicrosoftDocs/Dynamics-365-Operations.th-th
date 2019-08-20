---
title: การคิดค่าเสื่อมราคาด้วยตนเอง
description: บทความนี้แสดงภาพรวมของวิธีคิดค่าเสื่อมราคาด้วยตนเอง
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840324"
---
# <a name="manual-depreciation"></a><span data-ttu-id="36e0f-103">การคิดค่าเสื่อมราคาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="36e0f-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36e0f-104">บทความนี้แสดงภาพรวมของวิธีคิดค่าเสื่อมราคาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="36e0f-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="36e0f-105">เมื่อคุณตั้งค่าการคิดค่าเสื่อมราคาสินทรัพย์ถาวรและเลือก **กำหนดเอง** ในฟิลด์ **วิธีการ** บนหน้า **โพรไฟล์การคิดค่าเสื่อมราคา** ค่าเสื่อมราคาของสินทรัพย์ถาวรที่มีการกำหนดให้กับโพรไฟล์การคิดค่าเสื่อมราคานี้ จะถูกกำหนดโดยเปอร์เซ็นต์ที่คุณป้อนสำหรับแต่ละช่วงเวลาในปีปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="36e0f-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="36e0f-106">ช่วงเวลาที่คุณตั้งค่าเปอร์เซ็นต์จะมีการลงรายการบัญชีตามค่าที่คุณเลือกไว้ในฟิลด์ **ความถี่ของรอบระยะเวลา** บนแท็บด่วน **ทั่วไป** ของหน้า **โพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="36e0f-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="36e0f-107">ต่อไปนี้เป็นค่าที่คุณสามารถเลือกได้:</span><span class="sxs-lookup"><span data-stu-id="36e0f-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="36e0f-108">ทุกปี</span><span class="sxs-lookup"><span data-stu-id="36e0f-108">Yearly</span></span>
-   <span data-ttu-id="36e0f-109">ทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="36e0f-109">Monthly</span></span>
-   <span data-ttu-id="36e0f-110">รายไตรมาส</span><span class="sxs-lookup"><span data-stu-id="36e0f-110">Quarterly</span></span>
-   <span data-ttu-id="36e0f-111">ทุกครึ่งปี</span><span class="sxs-lookup"><span data-stu-id="36e0f-111">Half-Yearly</span></span>
-   <span data-ttu-id="36e0f-112">รายวัน</span><span class="sxs-lookup"><span data-stu-id="36e0f-112">Daily</span></span>

<span data-ttu-id="36e0f-113">หลังจากคุณเลือกความถี่ของรอบระยะเวลา ให้คลิก **กำหนดการที่กำหนดเอง**และตั้งค่าเปอร์เซ็นต์สำหรับช่วงเวลาการลงรายการบัญชีแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="36e0f-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="36e0f-114">เมื่อรวมกันแล้ว กำหนดการที่กำหนดเองและช่วงเวลาของการลงรายการบัญชีจะเป็นตัวกำหนดยอดค่าเสื่อมราคา ดังที่แสดงในตัวอย่างในบทความหลังจากนี้</span><span class="sxs-lookup"><span data-stu-id="36e0f-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="36e0f-115">การคิดค่าเสื่อมราคาด้วยตนเองจะถูกคำนวณเป็นเปอร์เซ็นต์ของราคาทุนของสินทรัพย์เสมอ</span><span class="sxs-lookup"><span data-stu-id="36e0f-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="36e0f-116">สำหรับการคิดค่าเสื่อมราคาด้วยตนเอง เปอร์เซ็นต์ที่คุณป้อนในช่วงของค่าเสื่อมราคาไม่ต้องรวมกันได้ 100%</span><span class="sxs-lookup"><span data-stu-id="36e0f-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="36e0f-117">การคิดค่าเสื่อมราคาด้วยตนเองเป็นวิธีการคิดค่าเสื่อมราคาที่ยืดหยุ่นซึ่งมักใช้เพื่อกำหนดโพรไฟล์ค่าเสื่อมราคาพิเศษบนหน้า **สมุดบัญชี** เช่นการคิดค่าเสื่อมราคาที่ไม่ใช่ประจำงวดสำหรับวัตถุประสงค์พิเศษ (ตัวอย่างเช่น ภาษี)</span><span class="sxs-lookup"><span data-stu-id="36e0f-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="36e0f-118">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="36e0f-118">Examples</span></span>
<span data-ttu-id="36e0f-119">ราคาทุนของสินทรัพย์: มูลค่าซากที่คาดไว้คือ 11,000.00: 1,000.00 ตารางต่อไปนี้แสดงช่วงเวลาและเปอร์เซ็นต์ที่คุณตั้งค่าบนหน้า **กำหนดการโพรไฟล์ค่าเสื่อมราคาสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="36e0f-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="36e0f-120">หมายเลขช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="36e0f-120">Interval number</span></span> | <span data-ttu-id="36e0f-121">เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="36e0f-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="36e0f-122">1</span><span class="sxs-lookup"><span data-stu-id="36e0f-122">1</span></span>               | <span data-ttu-id="36e0f-123">10.00</span><span class="sxs-lookup"><span data-stu-id="36e0f-123">10.00</span></span>      |
| <span data-ttu-id="36e0f-124">2</span><span class="sxs-lookup"><span data-stu-id="36e0f-124">2</span></span>               | <span data-ttu-id="36e0f-125">50.00</span><span class="sxs-lookup"><span data-stu-id="36e0f-125">50.00</span></span>      |
| <span data-ttu-id="36e0f-126">3</span><span class="sxs-lookup"><span data-stu-id="36e0f-126">3</span></span>               | <span data-ttu-id="36e0f-127">8.00</span><span class="sxs-lookup"><span data-stu-id="36e0f-127">8.00</span></span>       |

<span data-ttu-id="36e0f-128">ตารางต่อไปนี้แสดงวิธีคำนวณค่าเสื่อมราคาสำหรับแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="36e0f-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="36e0f-129">หมายเลขช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="36e0f-129">Interval number</span></span> | <span data-ttu-id="36e0f-130">การคำนวณยอดค่าเสื่อมราคารายปี</span><span class="sxs-lookup"><span data-stu-id="36e0f-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="36e0f-131">มูลค่าตามบัญชีสุทธิเมื่อสิ้นสุดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="36e0f-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="36e0f-132">1</span><span class="sxs-lookup"><span data-stu-id="36e0f-132">1</span></span>                | <span data-ttu-id="36e0f-133">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="36e0f-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="36e0f-134">10,000 (11,000 – 1,000)</span><span class="sxs-lookup"><span data-stu-id="36e0f-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="36e0f-135">2</span><span class="sxs-lookup"><span data-stu-id="36e0f-135">2</span></span>                | <span data-ttu-id="36e0f-136">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="36e0f-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="36e0f-137">5,000 (10,000 – 5,000)</span><span class="sxs-lookup"><span data-stu-id="36e0f-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="36e0f-138">3</span><span class="sxs-lookup"><span data-stu-id="36e0f-138">3</span></span>                | <span data-ttu-id="36e0f-139">(11,000 – 1,000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="36e0f-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="36e0f-140">4,200 (5,000 – 800)</span><span class="sxs-lookup"><span data-stu-id="36e0f-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="36e0f-141">ถ้าคุณเลือก **ทุกเดือน** ในฟิลด์**ความถี่ของรอบระยะเวลา** คุณตั้งค่าช่วงเวลาของกำหนดการที่กำหนดเองเป็น 12 ช่วง</span><span class="sxs-lookup"><span data-stu-id="36e0f-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="36e0f-142">ตารางต่อไปนี้แสดงยอดค่าเสื่อมราคาสำหรับช่วงเวลาสองช่วงแรก</span><span class="sxs-lookup"><span data-stu-id="36e0f-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="36e0f-143">ช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="36e0f-143">Interval</span></span> | <span data-ttu-id="36e0f-144">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="36e0f-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="36e0f-145">มกราคม</span><span class="sxs-lookup"><span data-stu-id="36e0f-145">January</span></span>  | <span data-ttu-id="36e0f-146">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="36e0f-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="36e0f-147">กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="36e0f-147">February</span></span> | <span data-ttu-id="36e0f-148">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="36e0f-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="36e0f-149">ถ้าคุณเลือก <strong>ทุกครึ่งปี</strong> ในฟิลด์ *<strong><em>ความถี่ของรอบระยะเวลา</em>* </strong> คุณตั้งค่าช่วงเวลาของกำหนดการที่กำหนดเองเป็น 2 ช่วง</span><span class="sxs-lookup"><span data-stu-id="36e0f-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="36e0f-150">ตารางต่อไปนี้แสดงยอดค่าเสื่อมราคาสำหรับช่วงเวลาสองช่วงแรก</span><span class="sxs-lookup"><span data-stu-id="36e0f-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="36e0f-151">ช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="36e0f-151">Interval</span></span>    | <span data-ttu-id="36e0f-152">ยอดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="36e0f-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="36e0f-153">30 มิถุนายน</span><span class="sxs-lookup"><span data-stu-id="36e0f-153">June 30</span></span>     | <span data-ttu-id="36e0f-154">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="36e0f-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="36e0f-155">31 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="36e0f-155">December 31</span></span> | <span data-ttu-id="36e0f-156">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="36e0f-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="36e0f-157">ผลรวมของเปอร์เซ็นต์สำหรับช่วงเวลาทั้งหมดไม่จำเป็นต้องเป็น 100</span><span class="sxs-lookup"><span data-stu-id="36e0f-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="36e0f-158">อย่างไรก็ตาม คุณจะได้รับข้อความถ้าค่าในฟิลด์ **เปอร์เซ็นต์สะสม** ในหน้า **กำหนดการโพรไฟล์ค่าเสื่อมราคาสินทรัพย์ถาวร** ไม่เป็น **100**</span><span class="sxs-lookup"><span data-stu-id="36e0f-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



