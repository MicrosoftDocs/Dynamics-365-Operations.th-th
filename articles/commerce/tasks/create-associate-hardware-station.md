---
title: " สร้างและเชื่อมโยงสถานีฮาร์ดแวร์"
description: 'กระบวนการนี้นำไปสู่วิธีการสร้างสถานีฮาร์ดแวร์ใหม่ '
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0c02246a20ef28c0f4f28b73dfe5ff56f38a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247055"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="3fb86-103"> สร้างและเชื่อมโยงสถานีฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="3fb86-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fb86-104">กระบวนการนี้นำไปสู่วิธีการสร้างสถานีฮาร์ดแวร์ใหม่ </span><span class="sxs-lookup"><span data-stu-id="3fb86-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="3fb86-105">โพรไฟล์ฮาร์ดแวร์ใหม่จะถูกสร้างขึ้นและถูกใช้ในการเพิ่มสถานีฮาร์ดแวร์ใหม่ให้กับร้านค้าที่ถูกกำหนดไว้ล่วงหน้า (ช่องทาง) </span><span class="sxs-lookup"><span data-stu-id="3fb86-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="3fb86-106">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="3fb86-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3fb86-107">ไปที่ สิ่งจำเป็นสำหรับการค้า > ช่องทาง > ..</span><span class="sxs-lookup"><span data-stu-id="3fb86-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="3fb86-108">> ..</span><span class="sxs-lookup"><span data-stu-id="3fb86-108">> ..</span></span> <span data-ttu-id="3fb86-109">> ..</span><span class="sxs-lookup"><span data-stu-id="3fb86-109">> ..</span></span> <span data-ttu-id="3fb86-110">> โพรไฟล์สถานีฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="3fb86-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="3fb86-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3fb86-111">Click New.</span></span>
3. <span data-ttu-id="3fb86-112">ในฟิลด์รหัสสถานีฮาร์ดแวร์ ให้พิมพ์ 'TestHWProfile'</span><span class="sxs-lookup"><span data-stu-id="3fb86-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="3fb86-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3fb86-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3fb86-114">ในฟิลด์หมายเลขพอร์ต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3fb86-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="3fb86-115">ในฟิลด์โพรไฟล์ฮาร์ดแวร์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3fb86-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3fb86-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3fb86-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3fb86-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3fb86-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3fb86-118">ในฟิลด์ชื่อแพคเกจ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3fb86-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3fb86-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3fb86-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3fb86-120">นี่คือแพคเกจมาตรฐานที่มาพร้อมกับสภาพแวดล้อมใหม่ </span><span class="sxs-lookup"><span data-stu-id="3fb86-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="3fb86-121">หมายเลขเวอร์ชันอาจแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3fb86-121">The version number may vary.</span></span>  
11. <span data-ttu-id="3fb86-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3fb86-122">Click Save.</span></span>
12. <span data-ttu-id="3fb86-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3fb86-123">Close the page.</span></span>
13. <span data-ttu-id="3fb86-124">ไปยัง การขายปลีกและการค้า > ช่องทาง > ร้านค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3fb86-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="3fb86-125">ในรายการ ให้เลือกแถว 17</span><span class="sxs-lookup"><span data-stu-id="3fb86-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="3fb86-126">ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USRT นี่คือร้านค้าHouston</span><span class="sxs-lookup"><span data-stu-id="3fb86-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="3fb86-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3fb86-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="3fb86-128">สลับการขยายของส่วนสถานีฮาร์ดแวร์ </span><span class="sxs-lookup"><span data-stu-id="3fb86-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="3fb86-129">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3fb86-129">Click Add.</span></span>
18. <span data-ttu-id="3fb86-130">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3fb86-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="3fb86-131">ในฟิลด์รหัสโพรไฟล์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3fb86-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3fb86-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3fb86-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3fb86-133">นี่ต้องเป็นโพรไฟล์สถานีฮาร์ดแวร์แบบใหม่ที่ถูกสร้างขึ้นในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3fb86-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="3fb86-134">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3fb86-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="3fb86-135">ในฟิลด์ชื่อโฮสต์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3fb86-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="3fb86-136">ในฟิลด์รหัสเทอร์มินัลEFT ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3fb86-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="3fb86-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3fb86-137">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]