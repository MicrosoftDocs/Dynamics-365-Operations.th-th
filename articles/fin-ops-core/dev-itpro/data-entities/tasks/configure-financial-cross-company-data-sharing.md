---
title: ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท '
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35ec8fc809841c0830224646fb57b0e4e4d40ef4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752303"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="b2784-103">ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท</span><span class="sxs-lookup"><span data-stu-id="b2784-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2784-104">กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="b2784-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="b2784-105">ใช้บริษัท USMF และข้อมูลทางการเงินซึ่งใช้เท็มเพลตร่วมกัน </span><span class="sxs-lookup"><span data-stu-id="b2784-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="b2784-106">คำแนะนำงานนี้ต้องการแพลตฟอร์ม Dynamics AX 7.1 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="b2784-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="b2784-107">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > พื้นที่ทำงาน > การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="b2784-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="b2784-108">คลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="b2784-108">Click **Import**.</span></span>
3. <span data-ttu-id="b2784-109">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b2784-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b2784-110">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** ให้เลือกชนิด 'แพคเกจ'</span><span class="sxs-lookup"><span data-stu-id="b2784-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="b2784-111">คลิก **อัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="b2784-111">Click **Upload**.</span></span> <span data-ttu-id="b2784-112">นำทางไปยังสถานที่ของข้อมูลทางการเงินที่ใช้ไฟล์แพคเกจเท็มเพลตร่วมกัน และเลือกไฟล์นั้น</span><span class="sxs-lookup"><span data-stu-id="b2784-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="b2784-113">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b2784-113">Click **Save**.</span></span>
6. <span data-ttu-id="b2784-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2784-114">In the list, mark the selected row.</span></span> <span data-ttu-id="b2784-115">เลือกข้อมูลที่ใช้นโยบายร่วมกัน ที่เพิ่งถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b2784-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="b2784-116">คลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="b2784-116">Click **Import**.</span></span>
8. <span data-ttu-id="b2784-117">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="b2784-117">Click **Close**.</span></span>
9. <span data-ttu-id="b2784-118">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="b2784-118">Refresh the page.</span></span>
10. <span data-ttu-id="b2784-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b2784-119">Close the page.</span></span>
11. <span data-ttu-id="b2784-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b2784-120">Close the page.</span></span>
12. <span data-ttu-id="b2784-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b2784-121">Close the page.</span></span>
13. <span data-ttu-id="b2784-122">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการระบบ > ตั้งค่า > ตั้งค่าคอนฟิกการใช้ข้อมูลร่วมกันข้ามบริษัท**</span><span class="sxs-lookup"><span data-stu-id="b2784-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="b2784-123">ในรายการนี้ ให้ค้นหาและเลือก **จำนวนวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="b2784-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="b2784-124">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="b2784-124">Click **Add**.</span></span>
16. <span data-ttu-id="b2784-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2784-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="b2784-126">ในฟิลด์ **บริษัท** ให้ป้อน 'USSI'</span><span class="sxs-lookup"><span data-stu-id="b2784-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="b2784-127">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="b2784-127">Click **Add**.</span></span>
19. <span data-ttu-id="b2784-128">ในฟิลด์ **บริษัท** ให้ป้อน 'USMF'</span><span class="sxs-lookup"><span data-stu-id="b2784-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="b2784-129">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b2784-129">Click **Save**.</span></span>
21. <span data-ttu-id="b2784-130">คลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="b2784-130">Click **Enable**.</span></span>
22. <span data-ttu-id="b2784-131">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="b2784-131">Click **Yes**.</span></span>
23. <span data-ttu-id="b2784-132">คลิก **ค้นหาปัญหาที่มีร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="b2784-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="b2784-133">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="b2784-133">Click **Yes**.</span></span>
25. <span data-ttu-id="b2784-134">คลิก **อัพเดตค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="b2784-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="b2784-135">คลิก **ใช้ค่าจากบริษัท 1**</span><span class="sxs-lookup"><span data-stu-id="b2784-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="b2784-136">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="b2784-136">Refresh the page.</span></span>
28. <span data-ttu-id="b2784-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b2784-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]