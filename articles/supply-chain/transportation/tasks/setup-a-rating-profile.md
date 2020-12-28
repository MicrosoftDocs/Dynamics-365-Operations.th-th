---
title: โพรไฟล์การจัดอันดับ
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าข้อมูลสำหรับโพรไฟล์การจัดอันดับ
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c54e7457813774027debd301d9a0bf8ce1b6d47
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646439"
---
# <a name="rating-profiles"></a><span data-ttu-id="3606f-103">โพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-103">Rating profiles</span></span>

<span data-ttu-id="3606f-104">โพรไฟล์การจัดอันดับมีลักษณะสัญญาลอจิสติกส์ (แต่ไม่ใช่สัญญาทางกฎหมาย)</span><span class="sxs-lookup"><span data-stu-id="3606f-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="3606f-105">ซึ่งใช้ในการกำหนดภาษีการขนส่งสำหรับจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="3606f-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="3606f-106">แต่ละโพรไฟล์การกำหนดอัตรามีเอกลักษณ์เฉพาะสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="3606f-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="3606f-107">ในโพรไฟล์ คุณเชื่อมโยงผู้ขนส่งสินค้ากับต้นแบบอัตรา</span><span class="sxs-lookup"><span data-stu-id="3606f-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="3606f-108">ต้นแบบอัตราจะกำหนดการกำหนดฐานอัตราและฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="3606f-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="3606f-109">ฐานอัตราจะกำหนดอัตราของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="3606f-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="3606f-110">คุณสามารถตั้งค่าโพรไฟล์การกำหนดอัตราโดยใช้หน้าทั่วไปที่แสดงภาพรวมของโพรไฟล์การกำหนดอัตราที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3606f-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="3606f-111">หรือคุณสามารถตั้งค่าโพรไฟล์การจัดอันดับโดยตรงจากผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="3606f-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="3606f-112">ในทั้งสองกรณี ข้อมูลที่คุณตั้งค่าสำหรับโพรไฟล์การจัดอันดับจะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="3606f-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="3606f-113">การสร้างหรือแก้ไขโพรไฟล์การจัดอันดับบนหน้าโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="3606f-114">บนหน้า **โพรไฟล์การจัดอันดับ** คุณสามารถตรวจสอบโพรไฟล์การจัดอันดับที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3606f-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="3606f-115">คุณยังสามารถแก้ไขโพรไฟล์ที่มีอยู่และสร้างโพรไฟล์ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="3606f-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="3606f-116">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> การจัดอันดับ \> โพรไฟล์การจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="3606f-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="3606f-117">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มโพรไฟล์การจัดอันดับใหม่ให้กริด หรือเลือก **แก้ไข** เพื่อแก้ไขโพรไฟล์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3606f-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="3606f-118">ในแถวสำหรับโพรไฟล์การจัดอันดับใหม่หรือที่มีอยู่ ให้ตั้งค่าฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3606f-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="3606f-119">**โพรไฟล์การจัดอันดับ** – ป้อนรหัสเฉพาะ (รหัส) สำหรับโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="3606f-120">**ชื่อ** - ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="3606f-121">**ผู้ขนส่งสินค้า** – เลือกผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="3606f-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="3606f-122">โพรไฟล์การจัดอันดับที่คุณกำลังตั้งค่าจะแสดงอยู่บนหน้า **ผู้ขนส่ง** สำหรับผู้ขนส่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3606f-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="3606f-123">**ไซต์** และ **คลังสินค้า** – เลือกไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="3606f-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="3606f-124">**กลไกจัดการอัตรา** - เลือกกลไกจัดการอัตราสำหรับโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="3606f-125">**ต้นแบบอัตรา** - เลือกต้นแบบอัตราสำหรับโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="3606f-126">คุณสามารถใช้ต้นแบบอัตราเพื่อกำหนดชนิดฐานของอัตราและฐานอัตรา</span><span class="sxs-lookup"><span data-stu-id="3606f-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="3606f-127">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าต้นแบบอัตรา](set-up-rate-masters.md)</span><span class="sxs-lookup"><span data-stu-id="3606f-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="3606f-128">**กลไกจัดการเวลาในการส่งต่อ** – เลือกกลไกจัดการเวลาในการส่งต่อสำหรับโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="3606f-129">**ดัชนีเชื้อเพลิงของผู้ขนส่ง** – เลือกดัชนีเชื้อเพลิงของผู้ขนส่งสำหรับโพรไฟล์การกำหนดอัตรา</span><span class="sxs-lookup"><span data-stu-id="3606f-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="3606f-130">**วันที่และเวลาเริ่มต้นของผลบังคับใช้** และ **วันที่สิ้นสุดที่มีผลบังคับ** – กำหนดรอบระยะเวลาที่ควรใช้โพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="3606f-131">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3606f-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="3606f-132">การสร้างโพรไฟล์การจัดอันดับบนหน้าผู้ขนส่งโดยตรง</span><span class="sxs-lookup"><span data-stu-id="3606f-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="3606f-133">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3606f-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="3606f-134">เลือกผู้ขนส่งสินค้าในรายชื่อ</span><span class="sxs-lookup"><span data-stu-id="3606f-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="3606f-135">บนแท็บด่วน **โพรไฟล์การจัดอันดับ** เลือก **สร้าง** เพื่อสร้างโพรไฟล์การจัดอันดับ</span><span class="sxs-lookup"><span data-stu-id="3606f-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="3606f-136">ตั้งค่าฟิลด์สำหรับโพรไฟล์การจัดอันดับใหม่</span><span class="sxs-lookup"><span data-stu-id="3606f-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="3606f-137">ฟิลด์เหล่านี้จะสอดคล้องกับฟิลด์บนหน้า **โพรไฟล์การจัดอันดับ** ตามที่อธิบายไว้ในหัวข้อก่อนหน้านี้ของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="3606f-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="3606f-138">โพรไฟล์ที่สร้างขึ้นบนหน้า **ผู้ขนส่ง** จะแสดงอยู่บนหน้า **โพรไฟล์การจัดอันดับ**</span><span class="sxs-lookup"><span data-stu-id="3606f-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
