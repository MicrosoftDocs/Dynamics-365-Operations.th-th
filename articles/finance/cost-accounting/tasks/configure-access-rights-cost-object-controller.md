---
title: ตั้งค่าคอนฟิกสิทธิ์การเข้าถึงสำหรับตัวควบคุมออบเจ็กต์ต้นทุน
description: ใช้กระบวนงานนี้เพื่อตั้งค่าคอนฟิกสิทธิการเข้าถึงสำหรับผู้ควบคุมออบเจ็กต์ต้นทุน
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4b50782c7a1b69b6953c65d6df155f003028333
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448560"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="0d573-103">ตั้งค่าคอนฟิกสิทธิ์การเข้าถึงสำหรับตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d573-104">ใช้กระบวนงานนี้เพื่อตั้งค่าคอนฟิกสิทธิการเข้าถึงสำหรับผู้ควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="0d573-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="0d573-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="0d573-106">กำหนดบทบาทตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="0d573-107">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0d573-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="0d573-108">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="0d573-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0d573-109">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ชื่อผู้ใช้ ด้วยค่า 'Alicia'</span><span class="sxs-lookup"><span data-stu-id="0d573-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="0d573-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0d573-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0d573-111">คลิกการกำหนดบทบาท</span><span class="sxs-lookup"><span data-stu-id="0d573-111">Click Assign roles.</span></span>
5. <span data-ttu-id="0d573-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0d573-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="0d573-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0d573-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="0d573-114">เปิดใช้งานความปลอดภัยรายการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="0d573-114">Enable access list security</span></span>
1. <span data-ttu-id="0d573-115">ไปที่ การบัญชีต้นทุน > มิติ > ลำดับชั้นของมิติ</span><span class="sxs-lookup"><span data-stu-id="0d573-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="0d573-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0d573-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0d573-117">เลือกองค์กร</span><span class="sxs-lookup"><span data-stu-id="0d573-117">Select Organization.</span></span>  
3. <span data-ttu-id="0d573-118">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="0d573-118">Click Edit.</span></span>
4. <span data-ttu-id="0d573-119">เลือก ใช่ ในฟิลด์ ลำดับชั้นรายการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="0d573-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="0d573-120">คลิกดูลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="0d573-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="0d573-121">กำหนดสิทธิ์การเข้าถึงให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="0d573-121">Assign access rights to user</span></span>
1. <span data-ttu-id="0d573-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d573-122">Click New.</span></span>
2. <span data-ttu-id="0d573-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0d573-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0d573-124">ในฟิลด์รหัสผู้ใช้ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0d573-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="0d573-125">เลือกผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="0d573-125">Select Admin.</span></span>  
4. <span data-ttu-id="0d573-126">ในแผนภูมิ ให้เลือก 'Organization\CEO\CFO\FIM'</span><span class="sxs-lookup"><span data-stu-id="0d573-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="0d573-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0d573-127">Click New.</span></span>
6. <span data-ttu-id="0d573-128">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0d573-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0d573-129">ในฟิลด์รหัสผู้ใช้ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0d573-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="0d573-130">เลือก Alicia</span><span class="sxs-lookup"><span data-stu-id="0d573-130">Select Alicia.</span></span>  
8. <span data-ttu-id="0d573-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d573-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="0d573-132">เปิดใช้งานสิทธิ์การเข้าถึงในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="0d573-133">ไปที่ การบัญชีต้นทุน > การตั้งค่า > พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="0d573-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="0d573-134">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="0d573-134">Click the General tab.</span></span>
3. <span data-ttu-id="0d573-135">เลือก ใช่ ในฟิลด์ เปิดใช้งานดูการเข้าถึงสำหรับสมาชิกมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="0d573-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d573-136">Click Save.</span></span>
5. <span data-ttu-id="0d573-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0d573-137">Close the page.</span></span>
6. <span data-ttu-id="0d573-138">ไปที่ บัญชีต้นทุน > การตั้งค่า > การตั้งค่าคอนฟิกพื้นที่ทำงานของการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="0d573-139">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="0d573-139">Click Edit.</span></span>
8. <span data-ttu-id="0d573-140">เลือก ใช่ ในฟิลด์ เผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="0d573-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="0d573-141">ถ้าคุณเลือก ใช่ ผู้ใช้ที่ได้รับการกำหนดบทบาทหนึ่งบทบาทใดในสี่รายการต่อไปนี้จะสามารถดูรายงานในพื้นที่ทำงานการควบคุมต้นทุน: ผู้จัดการการบัญชีต้นทุน นักบัญชีต้นทุน เสมียนบัญชีต้นทุน และตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="0d573-142">ถ้าคุณเลือก ไม่ใช่ เฉพาะผู้ใช้ที่ได้รับการกำหนดบทบาทหนึ่งบทบาทใดในรายการต่อไปนี้จะสามารถดูรายงาน: ผู้จัดการการบัญชีต้นทุน นักบัญชีต้นทุน และเสมียนบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0d573-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="0d573-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0d573-143">Click Save.</span></span>

