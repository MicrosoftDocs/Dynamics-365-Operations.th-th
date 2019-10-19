---
title: ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท '
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184381"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="df5e6-103">ตั้งค่าคอนฟิกการใช้ข้อมูลทางการเงินร่วมกันข้ามบริษัท</span><span class="sxs-lookup"><span data-stu-id="df5e6-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df5e6-104">กระบวนงานนี้แสดงวิธีการตั้งค่าคอนฟิก เปิดใช้งาน ตรวจสอบความถูกต้อง และแก้ไขความขัดแย้ง เมื่อมีการใช้ข้อมูลร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="df5e6-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="df5e6-105">ใช้บริษัท USMF และข้อมูลทางการเงินซึ่งใช้เท็มเพลตร่วมกัน </span><span class="sxs-lookup"><span data-stu-id="df5e6-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="df5e6-106">คำแนะนำงานนี้ต้องการแพลตฟอร์ม Dynamics AX 7.1 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="df5e6-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="df5e6-107">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > พื้นที่ทำงาน > การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="df5e6-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="df5e6-108">คลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="df5e6-108">Click **Import**.</span></span>
3. <span data-ttu-id="df5e6-109">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="df5e6-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="df5e6-110">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** ให้เลือกชนิด 'แพคเกจ'</span><span class="sxs-lookup"><span data-stu-id="df5e6-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="df5e6-111">คลิก **อัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="df5e6-111">Click **Upload**.</span></span> <span data-ttu-id="df5e6-112">นำทางไปยังสถานที่ของข้อมูลทางการเงินที่ใช้ไฟล์แพคเกจเท็มเพลตร่วมกัน และเลือกไฟล์นั้น</span><span class="sxs-lookup"><span data-stu-id="df5e6-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="df5e6-113">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="df5e6-113">Click **Save**.</span></span>
6. <span data-ttu-id="df5e6-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="df5e6-114">In the list, mark the selected row.</span></span> <span data-ttu-id="df5e6-115">เลือกข้อมูลที่ใช้นโยบายร่วมกัน ที่เพิ่งถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="df5e6-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="df5e6-116">คลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="df5e6-116">Click **Import**.</span></span>
8. <span data-ttu-id="df5e6-117">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="df5e6-117">Click **Close**.</span></span>
9. <span data-ttu-id="df5e6-118">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="df5e6-118">Refresh the page.</span></span>
10. <span data-ttu-id="df5e6-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="df5e6-119">Close the page.</span></span>
11. <span data-ttu-id="df5e6-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="df5e6-120">Close the page.</span></span>
12. <span data-ttu-id="df5e6-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="df5e6-121">Close the page.</span></span>
13. <span data-ttu-id="df5e6-122">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการระบบ > ตั้งค่า > ตั้งค่าคอนฟิกการใช้ข้อมูลร่วมกันข้ามบริษัท**</span><span class="sxs-lookup"><span data-stu-id="df5e6-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="df5e6-123">ในรายการนี้ ให้ค้นหาและเลือก **จำนวนวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="df5e6-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="df5e6-124">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="df5e6-124">Click **Add**.</span></span>
16. <span data-ttu-id="df5e6-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="df5e6-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="df5e6-126">ในฟิลด์ **บริษัท** ให้ป้อน 'USSI'</span><span class="sxs-lookup"><span data-stu-id="df5e6-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="df5e6-127">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="df5e6-127">Click **Add**.</span></span>
19. <span data-ttu-id="df5e6-128">ในฟิลด์ **บริษัท** ให้ป้อน 'USMF'</span><span class="sxs-lookup"><span data-stu-id="df5e6-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="df5e6-129">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="df5e6-129">Click **Save**.</span></span>
21. <span data-ttu-id="df5e6-130">คลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="df5e6-130">Click **Enable**.</span></span>
22. <span data-ttu-id="df5e6-131">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="df5e6-131">Click **Yes**.</span></span>
23. <span data-ttu-id="df5e6-132">คลิก **ค้นหาปัญหาที่มีร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="df5e6-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="df5e6-133">คลิก **ใช่** </span><span class="sxs-lookup"><span data-stu-id="df5e6-133">Click **Yes**.</span></span>
25. <span data-ttu-id="df5e6-134">คลิก **อัพเดตค่าฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="df5e6-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="df5e6-135">คลิก **ใช้ค่าจากบริษัท 1**</span><span class="sxs-lookup"><span data-stu-id="df5e6-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="df5e6-136">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="df5e6-136">Refresh the page.</span></span>
28. <span data-ttu-id="df5e6-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="df5e6-137">Close the page.</span></span>

