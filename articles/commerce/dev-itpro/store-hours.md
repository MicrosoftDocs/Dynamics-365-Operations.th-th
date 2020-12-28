---
title: สร้างและอัพเดตชั่วโมงทำการของร้านค้า
description: หัวข้อนี้อธิบายเกี่ยวกับวิธีการสร้างและอัพเดตชั่วโมงทำการของร้านค้าในศูนย์ควบคุมการค้า
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 4706432234437d2dc7943fb194cd01004ab7e6b7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687522"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="fa836-103">สร้างและอัพเดตชั่วโมงทำการของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fa836-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="fa836-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fa836-104">Overview</span></span>

<span data-ttu-id="fa836-105">จากสถานที่เดียว ร้านค้าปลีกสามารถสร้าง รักษา และจัดการชั่วโมงทำการของร้านค้าสำหรับร้านค้าต่างๆทั่วภูมิภาคทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="fa836-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="fa836-106">ชั่วโมงทำการของร้านค้าสามารถแสดงบนเทอร์มินัลขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="fa836-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="fa836-107">ด้วยวิธีนี้ พนักงานเก็บเงินสามารถแชร์ชั่วโมงทำการของร้านค้ากับลูกค้าและช่วยเหลือนักช้อปที่มีความสนใจในสินค้าคงคลังในร้านค้าอื่นๆได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="fa836-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="fa836-108">นอกจากนี้คุณยังสามารถพิมพ์ชั่วโมงทำการของร้านค้าบนใบเสร็จรับเงิน ในกรณีที่ลูกค้าต้องการส่งคืนไปยังร้านค้าในภายหลังได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="fa836-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="fa836-109">ชั่วโมงทำการของร้านค้าหลายชั่วโมงสามารถตั้งค่าคอนฟิกข้ามช่องทางต่างๆ</span><span class="sxs-lookup"><span data-stu-id="fa836-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="fa836-110">ช่องทางเหล่านี้รวมถึงร้านค้าจริง ศูนย์บริการ อุปกรณ์เคลื่อนที่ และไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="fa836-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="fa836-111">ถ้าลูกค้ามีใบสั่งซื้อสำหรับร้านค้าอื่น พนักงานเก็บเงินสามารถเลือกวันที่ที่สามารถรับสินค้าที่ร้านค้าดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="fa836-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="fa836-112">การค้นหาร้านค้าจะแสดงข้อมูลอ้างอิงถึงวันที่และเวลาทำการของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fa836-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="fa836-113">พนักงานเก็บเงินสามารถเลือกวันที่และสถานที่ และยังสามารถพิมพ์ใบเสร็จตามใบเบิกสินค้าซึ่งรวมถึงชั่วโมงทำการของร้านค้าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="fa836-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="fa836-114">ฟังก์ชันนี้มีอยู่ใน Microsoft Dynamics 365 Retail รุ่น 8.1.2 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="fa836-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="fa836-115">ตั้งค่าคอนฟิกชั่วโมงทำการของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fa836-115">Configure store hours</span></span>

<span data-ttu-id="fa836-116">ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิกชั่วโมงทำการของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fa836-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="fa836-117">ไปที่ **Retail และd Commerce** \> **การตั้งค่าช่องทาง** \> **ชั่วโมงทำการของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="fa836-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="fa836-118">เลือก **สร้าง** เพื่อสร้างเท็มเพลตชั่วโมงทำการของร้านค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="fa836-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="fa836-119">เมื่อต้องการใช้เท็มเพลตที่มีอยู่ ให้เลือกเท็มเพลตในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="fa836-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="fa836-120">ในกล่องโต้ตอบ **เพิ่มช่วง** ให้กำหนดช่วงวันที่ ชั่วโมงทำการของร้านค้า และวันหยุดใดๆที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="fa836-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="fa836-121">ถ้าชั่วโมงทำการของร้านค้าไม่มีการเปลี่ยนแปลง ให้เลือก **ไม่มีที่สิ้นสุด** ในฟิลด์ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="fa836-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="fa836-122">ถ้าชั่วโมงทำการของร้านค้าเป็นสำหรับเดือน สัปดาห์ หรือวันหนึ่งๆ ให้กำหนดวันที่ที่เหมาะสมในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="fa836-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa836-123">คุณสามารถสร้างเท็มเพลตได้หลายเท็มเพลตที่มีวันที่เริ่มต้นและสิ้นสุดที่ทับซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="fa836-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="fa836-124">อย่างไรก็ตาม คุณสามารถกำหนดชั่วโมงทำการของร้านค้าสำหรับร้านค้าในโซนเวลาที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="fa836-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="fa836-125">![กล่องโต้ตอบของการเพิ่มช่วง](../dev-itpro/media/Storehours1.png "กล่องโต้ตอบของการเพิ่มช่วง")</span><span class="sxs-lookup"><span data-stu-id="fa836-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="fa836-126">เชื่อมโยงเท็มเพลตชั่วโมงทำการของร้านค้ากับร้านค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="fa836-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="fa836-127">ในกล่องโต้ตอบ **เลือกโหนดองค์กร** เลือกร้านค้า ภูมิภาค และองค์กรที่ควรเชื่อมโยงกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fa836-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="fa836-128">เท็มเพลตชั่วโมงทำการของร้านค้าเพียงหนึ่งเท็มเพลตเท่านั้นสามารถถูกเชื่อมโยงกับแต่ละร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fa836-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="fa836-129">ใช้ปุ่มลูกศรเพื่อเลือกร้านค้า ภูมิภาค หรือองค์กร</span><span class="sxs-lookup"><span data-stu-id="fa836-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="fa836-130">ปฏิทินจะพร้อมใช้งานสำหรับร้านค้าหรือกลุ่มร้านค้า และจะมองเห็นได้ที่ POS สำหรับการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="fa836-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="fa836-131">![กล่องโต้ตอบเลือกโหนดองค์กร](../dev-itpro/media/Storehours2.png "กล่องโต้ตอบเลือกโหนดองค์กร")</span><span class="sxs-lookup"><span data-stu-id="fa836-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="fa836-132">บนหน้า **กำหนดการกระจาย** ให้รันงาน **1070** และ **1090** เพื่อทำให้ชั่วโมงทำการของร้านค้าพร้อมใช้งานสำหรับ POS</span><span class="sxs-lookup"><span data-stu-id="fa836-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="fa836-133">เพิ่มชั่วโมงทำการของร้านค้าในใบเสร็จรับเงินที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="fa836-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="fa836-134">ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มชั่วโมงทำการของร้านค้าลงในใบเสร็จรับเงิน POS ที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="fa836-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="fa836-135">เปิดตัวออกแบบใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="fa836-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="fa836-136">เลือก **ส่วนท้าย** ในมุมล่างซ้าย</span><span class="sxs-lookup"><span data-stu-id="fa836-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="fa836-137">ลากองค์ประกอบ **ชั่วโมงทำการของร้านค้า** จากบานหน้าต่างด้านซ้ายไปยังส่วนท้ายที่ด้านล่างของเท็มเพลตใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="fa836-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="fa836-138">คุณสามารถแก้ไขป้ายชื่อเริ่มต้นบนองค์ประกอบ **ชั่วโมงทำการของร้านค้า** ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="fa836-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="fa836-139">บันทึกใบเสร็จรับเงิน และปิดตัวออกแบบใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="fa836-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="fa836-140">บนหน้า **กำหนดการกระจาย** ให้รันงาน **1070** และ **1090**</span><span class="sxs-lookup"><span data-stu-id="fa836-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="fa836-141">ลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="fa836-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="fa836-142">ทำการขายให้เสร็จสมบูรณ์ และเลือกเพื่อพิมพ์ใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="fa836-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="fa836-143">ขณะนี้ใบเสร็จรับเงิน POS จะรวมชั่วโมงทำการของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="fa836-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="fa836-144">ถ้าวันหยุดใดๆรวมอยู่ในเท็มเพลต จะแสดงอยู่ในใบเสร็จรับเงิน</span><span class="sxs-lookup"><span data-stu-id="fa836-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="fa836-145">![ตัวอย่างใบเสร็จ](../dev-itpro/media/Storehours3.png "ตัวอย่างใบเสร็จ")</span><span class="sxs-lookup"><span data-stu-id="fa836-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
