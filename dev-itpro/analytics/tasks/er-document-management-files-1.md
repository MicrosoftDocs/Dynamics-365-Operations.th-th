--- 
title: "จัดเตรียมแบบจำลองข้อมูลเพื่อใช้ไฟล์การจัดการเอกสารในรูปแบบผลลัพธ์สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER "
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96195003c209c56c7ea4cbfec2f3543eb68453ff
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="ea481-103">จัดเตรียมแบบจำลองข้อมูลเพื่อใช้ไฟล์การจัดการเอกสารในรูปแบบผลลัพธ์สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="ea481-103">Prepare data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea481-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="ea481-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ea481-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="ea481-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ea481-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="ea481-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="ea481-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="ea481-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="ea481-108">เข้าถึงรายการของการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea481-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="ea481-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ea481-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ea481-110">ตรวจสอบให้แน่ใจว่า 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="ea481-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="ea481-111">พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ea481-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="ea481-112">เลือก 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="ea481-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="ea481-113">ผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea481-113">provider.</span></span>
3. <span data-ttu-id="ea481-114">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="ea481-114">Click Repositories.</span></span>
    * <span data-ttu-id="ea481-115">ถ้ามีที่เก็บชนิด 'ทรัพยากรการดำเนินงาน' อยู่แล้ว ให้ข้ามขั้นตอนที่เหลือของงานย่อยปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ea481-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="ea481-116">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ea481-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="ea481-117">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'</span><span class="sxs-lookup"><span data-stu-id="ea481-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="ea481-118">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="ea481-118">Click Create repository.</span></span>
7. <span data-ttu-id="ea481-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ea481-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="ea481-120">เรียกดูการตั้งคอนฟิกแบบจำลองใบแจ้งหนี้ของลูกค้าที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea481-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="ea481-121">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="ea481-121">Click Show filters.</span></span>
2. <span data-ttu-id="ea481-122">ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรองของ "ทรัพยากรการดำเนินงาน" ในฟิลด์ "ชื่อ" โดยใช้ตัวดำเนินการกรอง "ขึ้นต้นด้วย" ป้อนค่าตัวกรองของ "" ในฟิลด์ "คำอธิบาย" โดยใช้ตัวดำเนินการตัวกรอง "ขึ้นต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="ea481-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="ea481-123">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="ea481-123">Click Show filters.</span></span>
4. <span data-ttu-id="ea481-124">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="ea481-124">Click Open.</span></span>
5. <span data-ttu-id="ea481-125">ในแผนภูมิ ให้เลือก 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="ea481-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="ea481-126">เลือกการตั้งค่าคอนฟิกแบบจำลอง 'แบบจำลองใบแจ้งหนี้ของลูกค้า' เพื่อนำเข้าข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="ea481-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="ea481-127">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="ea481-127">Click Import.</span></span>
    * <span data-ttu-id="ea481-128">คลิก นำเข้าสำหรับรุ่น 1 ของการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ea481-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="ea481-129">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="ea481-129">Click Yes.</span></span>
8. <span data-ttu-id="ea481-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea481-130">Close the page.</span></span>
9. <span data-ttu-id="ea481-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea481-131">Close the page.</span></span>
10. <span data-ttu-id="ea481-132">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ea481-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="ea481-133">ในแผนภูมิ ให้เลือก 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="ea481-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="ea481-134">สร้างแบบจำลองที่ได้รับมาเพื่อรองรับการเข้าถึงไฟล์การจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ea481-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="ea481-135">คุณจะสร้างการตั้งค่าคอนฟิกของแบบจำลองใบแจ้งหนี้ของลูกค้าที่ได้รับมาจากการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft ของเราเอง </span><span class="sxs-lookup"><span data-stu-id="ea481-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="ea481-136">คุณจะใช้การตั้งค่าคอนฟิกนี้เพื่อใช้การเข้าถึงไฟล์การจัดการเอกสาร และทำให้พร้อมใช้งานสำหรับเอกสารอิเล็กทรอนิกส์ที่คุณจะสร้างตามแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="ea481-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="ea481-137">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="ea481-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="ea481-138">ในฟิลด์ใหม่ ป้อน 'ได้รับมาจากชื่อ: แบบจำลองใบแจ้งหนี้ของลูกค้า, Microsoft'</span><span class="sxs-lookup"><span data-stu-id="ea481-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="ea481-139">ในฟิลด์ชื่อ ให้พิมพ์ 'แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)'</span><span class="sxs-lookup"><span data-stu-id="ea481-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="ea481-140">แบบจำลองใบแจ้งหนี้ของลูกค้า (กำหนดเอง)</span><span class="sxs-lookup"><span data-stu-id="ea481-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="ea481-141">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ea481-141">Click Create configuration.</span></span>


