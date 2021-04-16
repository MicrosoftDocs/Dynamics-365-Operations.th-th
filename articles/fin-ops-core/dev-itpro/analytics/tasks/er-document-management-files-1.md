---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 1 - จัดเตรียมแบบจำลองข้อมูล)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER (ส่วนที่ 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b265c9af0635e6c9fb6295f7e8e4e353b2a5ba5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754949"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="f7fea-104">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 1 - จัดเตรียมแบบจำลองข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="f7fea-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7fea-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="f7fea-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f7fea-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="f7fea-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f7fea-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f7fea-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="f7fea-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="f7fea-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="f7fea-109">เข้าถึงรายการของการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="f7fea-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f7fea-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f7fea-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="f7fea-111">ตรวจสอบให้แน่ใจว่า 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="f7fea-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="f7fea-112">พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7fea-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="f7fea-113">เลือก 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="f7fea-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="f7fea-114">ผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="f7fea-114">provider.</span></span>
3. <span data-ttu-id="f7fea-115">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="f7fea-115">Click Repositories.</span></span>

    <span data-ttu-id="f7fea-116">ถ้ามีที่เก็บชนิด 'ทรัพยากรการดำเนินงาน' อยู่แล้ว ให้ข้ามขั้นตอนที่เหลือของงานย่อยปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f7fea-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="f7fea-117">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7fea-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="f7fea-118">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'</span><span class="sxs-lookup"><span data-stu-id="f7fea-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="f7fea-119">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f7fea-119">Click Create repository.</span></span>
7. <span data-ttu-id="f7fea-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7fea-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="f7fea-121">เรียกดูการตั้งคอนฟิกแบบจำลองใบแจ้งหนี้ของลูกค้าที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="f7fea-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f7fea-122">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="f7fea-122">Click Show filters.</span></span>
2. <span data-ttu-id="f7fea-123">ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรองของ "ทรัพยากรการดำเนินงาน" ในฟิลด์ "ชื่อ" โดยใช้ตัวดำเนินการกรอง "ขึ้นต้นด้วย" ป้อนค่าตัวกรองของ "" ในฟิลด์ "คำอธิบาย" โดยใช้ตัวดำเนินการตัวกรอง "ขึ้นต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="f7fea-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="f7fea-124">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="f7fea-124">Click Show filters.</span></span>
4. <span data-ttu-id="f7fea-125">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="f7fea-125">Click Open.</span></span>
5. <span data-ttu-id="f7fea-126">ในแผนภูมิ ให้เลือก 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="f7fea-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="f7fea-127">เลือกการตั้งค่าคอนฟิกแบบจำลอง 'แบบจำลองใบแจ้งหนี้ของลูกค้า' เพื่อนำเข้าข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="f7fea-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="f7fea-128">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="f7fea-128">Click Import.</span></span>

    <span data-ttu-id="f7fea-129">คลิก นำเข้าสำหรับรุ่น 1 ของการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7fea-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="f7fea-130">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f7fea-130">Click Yes.</span></span>
8. <span data-ttu-id="f7fea-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7fea-131">Close the page.</span></span>
9. <span data-ttu-id="f7fea-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7fea-132">Close the page.</span></span>
10. <span data-ttu-id="f7fea-133">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="f7fea-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="f7fea-134">ในแผนภูมิ ให้เลือก 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="f7fea-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="f7fea-135">สร้างแบบจำลองที่ได้รับมาเพื่อรองรับการเข้าถึงไฟล์การจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="f7fea-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="f7fea-136">คุณจะสร้างการตั้งค่าคอนฟิกของแบบจำลองใบแจ้งหนี้ของลูกค้าที่ได้รับมาจากการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft ของเราเอง </span><span class="sxs-lookup"><span data-stu-id="f7fea-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="f7fea-137">คุณจะใช้การตั้งค่าคอนฟิกนี้เพื่อใช้การเข้าถึงไฟล์การจัดการเอกสาร และทำให้พร้อมใช้งานสำหรับเอกสารอิเล็กทรอนิกส์ที่คุณจะสร้างตามแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="f7fea-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="f7fea-138">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7fea-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f7fea-139">ในฟิลด์ใหม่ ป้อน 'ได้รับมาจากชื่อ: แบบจำลองใบแจ้งหนี้ของลูกค้า, Microsoft'</span><span class="sxs-lookup"><span data-stu-id="f7fea-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="f7fea-140">ในฟิลด์ชื่อ ให้พิมพ์ 'แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)'</span><span class="sxs-lookup"><span data-stu-id="f7fea-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f7fea-141">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f7fea-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]