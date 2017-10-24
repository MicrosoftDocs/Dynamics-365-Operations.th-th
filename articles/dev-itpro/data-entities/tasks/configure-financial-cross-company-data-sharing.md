--- 
title: "ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท "
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 779722bd3acd10a85b089a4d30757b62293ea4e4
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="3504c-103">ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท</span><span class="sxs-lookup"><span data-stu-id="3504c-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3504c-104">กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="3504c-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="3504c-105">ใช้บริษัท USMF และข้อมูลทางการเงินซึ่งใช้เท็มเพลตร่วมกัน </span><span class="sxs-lookup"><span data-stu-id="3504c-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="3504c-106">คู่มืองานนี้ต้องการ Dynamics AX แพลตฟอร์ม 7.1 เป็นต้นไป</span><span class="sxs-lookup"><span data-stu-id="3504c-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="3504c-107">ไปที่การดูแลระบบ > พื้นที่ทำงาน > การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3504c-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="3504c-108">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="3504c-108">Click Import.</span></span>
3. <span data-ttu-id="3504c-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="3504c-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3504c-110">ในฟิลด์รูปแบบข้อมูลต้นทาง ให้เลือกชนิดแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="3504c-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="3504c-111">คลิก อัพโหลด</span><span class="sxs-lookup"><span data-stu-id="3504c-111">Click Upload.</span></span> <span data-ttu-id="3504c-112">นำทางไปยังสถานที่ของข้อมูลทางการเงินที่ใช้ไฟล์แพคเกจเท็มเพลตร่วมกัน และเลือกไฟล์นั้น</span><span class="sxs-lookup"><span data-stu-id="3504c-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="3504c-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3504c-113">Click Save.</span></span>
6. <span data-ttu-id="3504c-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3504c-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3504c-115">เลือกข้อมูลที่ใช้นโยบายร่วมกัน ที่เพิ่งถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3504c-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="3504c-116">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="3504c-116">Click Import.</span></span>
8. <span data-ttu-id="3504c-117">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="3504c-117">Click Close.</span></span>
9. <span data-ttu-id="3504c-118">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="3504c-118">Refresh the page.</span></span>
10. <span data-ttu-id="3504c-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3504c-119">Close the page.</span></span>
11. <span data-ttu-id="3504c-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3504c-120">Close the page.</span></span>
12. <span data-ttu-id="3504c-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3504c-121">Close the page.</span></span>
13. <span data-ttu-id="3504c-122">ไปที่การจัดการระบบ > การตั้งค่า > ตั้งค่าคอนฟิกลิขสิทธิ์การใช้ข้อมูลร่วมกันข้ามบริษัท</span><span class="sxs-lookup"><span data-stu-id="3504c-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="3504c-123">ในรายการนี้ ให้ค้นหาและเลือกจำนวนวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3504c-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="3504c-124">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3504c-124">Click Add.</span></span>
16. <span data-ttu-id="3504c-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3504c-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="3504c-126">ในฟิลด์บริษัท ให้พิมพ์ 'USSI'</span><span class="sxs-lookup"><span data-stu-id="3504c-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="3504c-127">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3504c-127">Click Add.</span></span>
19. <span data-ttu-id="3504c-128">ในฟิลด์บริษัท ให้พิมพ์ 'USMF'</span><span class="sxs-lookup"><span data-stu-id="3504c-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="3504c-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3504c-129">Click Save.</span></span>
21. <span data-ttu-id="3504c-130">คลิกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3504c-130">Click Enable.</span></span>
22. <span data-ttu-id="3504c-131">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="3504c-131">Click Yes.</span></span>
23. <span data-ttu-id="3504c-132">คลิกค้นหาปัญหาที่มีร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="3504c-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="3504c-133">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="3504c-133">Click Yes.</span></span>
25. <span data-ttu-id="3504c-134">คลิกอัพเดตค่าฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3504c-134">Click Update field value.</span></span>
26. <span data-ttu-id="3504c-135">คลิกใช้ค่าจากบริษัท 1</span><span class="sxs-lookup"><span data-stu-id="3504c-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="3504c-136">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="3504c-136">Refresh the page.</span></span>
28. <span data-ttu-id="3504c-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3504c-137">Close the page.</span></span>


