---
title: สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลองในการรายงานทางอิเล็กทรอนิกส์ (ER)
description: ใช้กระบวนงานนี้เพื่อออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง (ER) ของการรายงานทางอิเล็กทรอนิกส์ใหม่ และใช้ฟังก์ชัน ER ภายในสำหรับการคำนวณรวมที่มีประสิทธิภาพ
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544967"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="6e5b1-103">สร้างการตั้งค่าคอนฟิกการแม็ปแบบจำลองในการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="6e5b1-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e5b1-104">ใช้กระบวนงานนี้เพื่อออกแบบการตั้งค่าคอนฟิกการแม็ปแบบจำลอง (ER) ของการรายงานทางอิเล็กทรอนิกส์ใหม่ และใช้ฟังก์ชัน ER ภายในสำหรับการคำนวณรวมที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="6e5b1-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="6e5b1-105">ในกระบวนงานนี้ คุณจะสร้างการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6e5b1-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="6e5b1-106">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทของผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ที่ได้รับมอบหมาย</span><span class="sxs-lookup"><span data-stu-id="6e5b1-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="6e5b1-107">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูลใดๆ</span><span class="sxs-lookup"><span data-stu-id="6e5b1-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="6e5b1-108">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์ "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="6e5b1-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="6e5b1-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6e5b1-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6e5b1-110">ตรวจสอบให้แน่ใจว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="6e5b1-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="6e5b1-111">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ จะต้องดำเนินขั้นตอนต่างๆ ในกระบวนงานให้เสร็จสมบูรณ์ “สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่”</span><span class="sxs-lookup"><span data-stu-id="6e5b1-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="6e5b1-112">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="6e5b1-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="6e5b1-113">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="6e5b1-113">Click Show filters.</span></span>
4. <span data-ttu-id="6e5b1-114">ในฟิลด์ "ชื่อ" ป้อนค่าตัวกรอง "อินทราสแทต" และใช้ตัวดำเนินการตัวกรอง "ขึ้นต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="6e5b1-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="6e5b1-115">ใช้ตัวกรองข้อมูลนี้เพื่อค้นหาการตั้งค่าคอนฟิกแบบจำลองข้อมูล 'อินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="6e5b1-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="6e5b1-116">แบบจำลองนี้อาจมีอยู่แล้วในแผนภูมิการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6e5b1-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="6e5b1-117">ถ้ามี ให้ข้ามงานย่อยถัดไป</span><span class="sxs-lookup"><span data-stu-id="6e5b1-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="6e5b1-118">เรียกการตั้งค่าคอนฟิกแบบจำลองอินทราสแทตที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="6e5b1-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="6e5b1-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e5b1-119">Close the page.</span></span>
2. <span data-ttu-id="6e5b1-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e5b1-120">Close the page.</span></span>
3. <span data-ttu-id="6e5b1-121">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6e5b1-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="6e5b1-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6e5b1-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6e5b1-123">เลือกไทล์ผู้ให้บริการของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="6e5b1-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="6e5b1-124">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="6e5b1-124">Click Repositories.</span></span>
    * <span data-ttu-id="6e5b1-125">คลิก ที่เก็บ ในไทล์ผู้ให้บริการ Microsoft</span><span class="sxs-lookup"><span data-stu-id="6e5b1-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="6e5b1-126">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="6e5b1-126">Click Show filters.</span></span>
7. <span data-ttu-id="6e5b1-127">ในฟิลด์ "พิมพ์ชื่อ" ป้อนค่าตัวกรอง "ทรัพยากร" และใช้ตัวดำเนินการตัวกรอง "ประกอบด้วย"</span><span class="sxs-lookup"><span data-stu-id="6e5b1-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="6e5b1-128">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="6e5b1-128">Click Open.</span></span>
9. <span data-ttu-id="6e5b1-129">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="6e5b1-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="6e5b1-130">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="6e5b1-130">Click Import.</span></span>
11. <span data-ttu-id="6e5b1-131">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="6e5b1-131">Click Yes.</span></span>
    * <span data-ttu-id="6e5b1-132">คุณนำเข้าการตั้งค่าคอนฟิกแบบจำลอง ER ที่ประกอบด้วยรูปแบบจำลองข้อมูลที่คุณจะใช้เพื่อสำรวจวิธีการใช้ฟังก์ชัน ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="6e5b1-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="6e5b1-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e5b1-133">Close the page.</span></span>
13. <span data-ttu-id="6e5b1-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e5b1-134">Close the page.</span></span>
14. <span data-ttu-id="6e5b1-135">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="6e5b1-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="6e5b1-136">เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลองของใหม่</span><span class="sxs-lookup"><span data-stu-id="6e5b1-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="6e5b1-137">ในแผนภูมิ เลือก 'แบบจำลองอินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="6e5b1-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="6e5b1-138">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6e5b1-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6e5b1-139">ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองข้อมูลตามอินทราสแทตแบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="6e5b1-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="6e5b1-140">ในฟิลด์ชื่อ พิมพ์ 'การแม็บตัวอย่างอินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="6e5b1-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="6e5b1-141">การแม็ปตัวอย่างอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="6e5b1-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="6e5b1-142">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6e5b1-142">Click Create configuration.</span></span>

