--- 
title: "นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) รุ่นใหม่จาก Microsoft Lifecycle Services (LCS)"
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="49d69-103">นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services สำหรับการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="49d69-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49d69-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) รุ่นใหม่จาก Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="49d69-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="49d69-105">ในตัวอย่างนี้ คุณจะสร้างเลือกเวอร์ชันที่ต้องการของการตั้งค่าคอนฟิก ER และนำเข้าสำหรับบริษัทตัวอย่าง ซึ่งคือ Litware, inc ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="49d69-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="49d69-106">เมื่อต้องการดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ลำดับแรกคุณต้องดำเนินงานขั้นตอนในกระบวนงาน "อัพโหลดการตั้งค่าคอนฟิก ER ลงใน Lifecycle Services" </span><span class="sxs-lookup"><span data-stu-id="49d69-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="49d69-107">การเข้าถึง LCS ยังต้องการสำหรับการเสร็จสมบูรณ์ของขั้นตอนเหล่านี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="49d69-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="49d69-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="49d69-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="49d69-109">คลิกการตั้งค่าคอนฟลิก</span><span class="sxs-lookup"><span data-stu-id="49d69-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="49d69-110">ลบเวอร์ชันที่ใช้ร่วมกันของการตั้งค่าคอนฟิกแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49d69-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="49d69-111">ในแผนภูมิ เลือก 'การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="49d69-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="49d69-112">เวอร์ชันแรกของการตั้งค่าคอนฟิกแบบจำลองข้อมูลตัวอย่างได้ถูกสร้างขึ้น และถูกเผยแพร่ไปยัง LCS ในระหว่างกระบวนงาน 'อัพโหลดการตั้งค่าคอนฟิก ER ลงใน Lifecycle Services' </span><span class="sxs-lookup"><span data-stu-id="49d69-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="49d69-113">ในกระบวนงานนี้ คุณจะลบเวอร์ชันนี้ของการตั้งค่าคอนฟิก ER </span><span class="sxs-lookup"><span data-stu-id="49d69-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="49d69-114">การตั้งค่าคอนฟิกแบบจำลองข้อมูลตัวอย่างรุ่นนี้จะถูกนำเข้าในภายหลังจาก LCS</span><span class="sxs-lookup"><span data-stu-id="49d69-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="49d69-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="49d69-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49d69-116">เลือกเวอร์ชันของการตั้งค่าคอนฟิกนี้ ซึ่งอยู่ในสถานะ 'ใช้ร่วมกัน' </span><span class="sxs-lookup"><span data-stu-id="49d69-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="49d69-117">สถานะนี้ระบุว่าการตั้งค่าคอนฟิกได้ถูกเผยแพร่ไปยัง LCS แล้ว</span><span class="sxs-lookup"><span data-stu-id="49d69-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="49d69-118">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="49d69-118">Click Change status.</span></span>
4. <span data-ttu-id="49d69-119">คลิกยกเลิกการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="49d69-119">Click Discontinue.</span></span>
    * <span data-ttu-id="49d69-120">เปลี่ยนสถานะของเวอร์ชันที่เลือกจาก 'ใช้ร่วมกัน' เป็น 'ถูกยกเลิก' เพื่อทำให้พร้อมใช้งานสำหรับการลบ</span><span class="sxs-lookup"><span data-stu-id="49d69-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="49d69-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="49d69-121">Click OK.</span></span>
6. <span data-ttu-id="49d69-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="49d69-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49d69-123">เลือกเวอร์ชันของการตั้งค่าคอนฟิกนี้ ซึ่งมีสถานะเป็น 'ถูกยกเลิก'</span><span class="sxs-lookup"><span data-stu-id="49d69-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="49d69-124">คลิก ลบ</span><span class="sxs-lookup"><span data-stu-id="49d69-124">Click Delete.</span></span>
8. <span data-ttu-id="49d69-125">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="49d69-125">Click Yes.</span></span>
    * <span data-ttu-id="49d69-126">หมายเหตุว่า เฉพาะแบบร่างเวอร์ชัน 2 ของการตั้งค่าคอนฟิกแบบจำลองข้อมูลพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="49d69-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="49d69-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="49d69-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="49d69-128">นำเข้าเวอร์ชันที่ใช้ร่วมกันของการตั้งค่าคอนฟิกแบบจำลองข้อมูลจาก LCS</span><span class="sxs-lookup"><span data-stu-id="49d69-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="49d69-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="49d69-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="49d69-130">เปิดรายการของที่เก็บสำหรับผู้ให้บริการการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="49d69-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="49d69-131">’Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="49d69-131">configuration provider.</span></span>  
2. <span data-ttu-id="49d69-132">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="49d69-132">Click Repositories.</span></span>
3. <span data-ttu-id="49d69-133">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="49d69-133">Click Open.</span></span>
    * <span data-ttu-id="49d69-134">เลือกที่เก็บ LCS และเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="49d69-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="49d69-135">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="49d69-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="49d69-136">เลือกเวอร์ชันแรกของ 'การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง' ในรายการเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="49d69-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="49d69-137">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="49d69-137">Click Import.</span></span>
6. <span data-ttu-id="49d69-138">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="49d69-138">Click Yes.</span></span>
    * <span data-ttu-id="49d69-139">ยืนยันการนำเข้าของเวอร์ชันที่เลือกจาก LCS</span><span class="sxs-lookup"><span data-stu-id="49d69-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="49d69-140">หมายเหตุว่า ข้อความข้อมูล (เหนือแบบฟอร์ม) ยืนยันความสำเร็จของการนำเข้าเวอร์ชันที่เลือก</span><span class="sxs-lookup"><span data-stu-id="49d69-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="49d69-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="49d69-141">Close the page.</span></span>
8. <span data-ttu-id="49d69-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="49d69-142">Close the page.</span></span>
9. <span data-ttu-id="49d69-143">คลิกการตั้งค่าคอนฟลิก</span><span class="sxs-lookup"><span data-stu-id="49d69-143">Click Configurations.</span></span>
10. <span data-ttu-id="49d69-144">ในแผนภูมิ เลือก 'การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="49d69-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="49d69-145">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="49d69-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49d69-146">เลือกเวอร์ชันของการตั้งค่าคอนฟิกนี้ ซึ่งมีสถานะเป็น 'ใช้ร่วมกัน'</span><span class="sxs-lookup"><span data-stu-id="49d69-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="49d69-147">หมายเหตุว่า เวอร์ชันที่ใช้ร่วมกัน 1 ของการตั้งค่าคอนฟิกแบบจำลองข้อมูลที่เลือก พร้อมใช้งานด้วย ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="49d69-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


