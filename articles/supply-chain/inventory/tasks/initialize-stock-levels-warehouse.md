---
title: "เริ่มระดับสินค้าคงคลังในคลังสินค้า"
description: "ขั้นตอนนี้แสดงให้เห็นถึงการรับสินค้าคงคลังคงเหลือด้วยตนเอง โดยใช้สมุดรายวันการเคลื่อนย้ายสินค้าคงคลัง "
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 3b4685b034f7e6a3af0259fb921230e7b3397754
ms.contentlocale: th-th
ms.lasthandoff: 11/02/2017

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="dc7b1-103">เริ่มระดับสินค้าคงคลังในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="dc7b1-103">Initialize stock levels in the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc7b1-104">ขั้นตอนนี้แสดงให้เห็นถึงการรับสินค้าคงคลังคงเหลือด้วยตนเอง โดยใช้สมุดรายวันการเคลื่อนย้ายสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="dc7b1-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="dc7b1-105">(เป็นไปได้ที่มันสามารถอัพเดตสินค้าคงคลังคงเหลือเองด้วย โดยการนำเข้าธุรกรรมในเอนทิตี้ข้อมูล) คุณสามารถรันคำแนะนำนี้ในข้อมูลสาธิตของบริษัท USMF ซึ่งเป็นข้อกำหนดเบื้องต้นต่างๆ เช่น ชื่อสมุดรายวัน การตั้งค่าสินค้า โพรไฟล์การลงรายการบัญชี และบัญชีที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="dc7b1-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="dc7b1-106">คำแนะนำดังกล่าวได้แนะนำค่าเฉพาะสำหรับสินค้าและมิติที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="dc7b1-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="dc7b1-107">ถ้าคุณเลือกสินค้าอื่น คุณอาจต้องป้อนค่าสำหรับมิติที่ต่างออกไป</span><span class="sxs-lookup"><span data-stu-id="dc7b1-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="dc7b1-108">ไปที่ การจัดการสินค้าคงคลัง > รายการสมุดรายวัน > สินค้า > การเคลื่อนไหว</span><span class="sxs-lookup"><span data-stu-id="dc7b1-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="dc7b1-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dc7b1-109">Click New.</span></span>
3. <span data-ttu-id="dc7b1-110">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dc7b1-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dc7b1-111">เลือก IMov</span><span class="sxs-lookup"><span data-stu-id="dc7b1-111">Select IMov.</span></span>
    * <span data-ttu-id="dc7b1-112">นี่คือแนวทางปฏิบัติที่ดีในการใช้เท็มเพลตชื่อสมุดรายวันที่แตกต่างกันสำหรับวัตถุประสงค์ทางธุรกิจต่างๆ</span><span class="sxs-lookup"><span data-stu-id="dc7b1-112">It’s a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="dc7b1-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dc7b1-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="dc7b1-114">ในฟิลด์บัญชีตรงข้าม ระบุ ค่า '140200'</span><span class="sxs-lookup"><span data-stu-id="dc7b1-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="dc7b1-115">นี่คือบัญชีตรงข้ามที่จะเป็นบัญชีเริ่มต้นสำหรับรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="dc7b1-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="dc7b1-116">เป็นไปได้ที่จะแทนที่ค่าเริ่มต้นเพื่อจะมอบหมายบัญชีตรงข้ามที่แตกต่างกันต่อรายการ</span><span class="sxs-lookup"><span data-stu-id="dc7b1-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="dc7b1-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dc7b1-117">Click OK.</span></span>
8. <span data-ttu-id="dc7b1-118">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dc7b1-118">Click New.</span></span>
9. <span data-ttu-id="dc7b1-119">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dc7b1-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dc7b1-120">เลือก สินค้า A0001</span><span class="sxs-lookup"><span data-stu-id="dc7b1-120">Select item A0001.</span></span>
11. <span data-ttu-id="dc7b1-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dc7b1-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dc7b1-122">คลิก แท็บมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="dc7b1-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="dc7b1-123">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dc7b1-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dc7b1-124">เลือก ไซต์ 1</span><span class="sxs-lookup"><span data-stu-id="dc7b1-124">Select site 1.</span></span>
15. <span data-ttu-id="dc7b1-125">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dc7b1-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="dc7b1-126">เลือก คลังสินค้า 13</span><span class="sxs-lookup"><span data-stu-id="dc7b1-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="dc7b1-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dc7b1-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="dc7b1-128">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dc7b1-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="dc7b1-129">เลือก สถานที่เก็บ 13</span><span class="sxs-lookup"><span data-stu-id="dc7b1-129">Select location 13.</span></span>
20. <span data-ttu-id="dc7b1-130">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dc7b1-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="dc7b1-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dc7b1-131">Click Save.</span></span>
22. <span data-ttu-id="dc7b1-132">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="dc7b1-132">Click Post.</span></span>
23. <span data-ttu-id="dc7b1-133">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายโอนย้ายข้อผิดพลาดในการลงรายการบัญชีทั้งหมดไปยังสมุดรายวันใหม่</span><span class="sxs-lookup"><span data-stu-id="dc7b1-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="dc7b1-134">ถ้าคุณเปิดใช้งานตัวเลือกนี้ รายการใดๆ ที่มีการลงรายการบัญชีล้มเหลวจะถูกคัดลอกไปยังสมุดรายวันใหม่ </span><span class="sxs-lookup"><span data-stu-id="dc7b1-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="dc7b1-135">คุณสามารถใช้ข้อมูลในล็อกเพื่อแก้ไขปัญหา และลงรายการอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="dc7b1-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="dc7b1-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dc7b1-136">Click OK.</span></span>
25. <span data-ttu-id="dc7b1-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dc7b1-137">Close the page.</span></span>
26. <span data-ttu-id="dc7b1-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dc7b1-138">Close the page.</span></span>

