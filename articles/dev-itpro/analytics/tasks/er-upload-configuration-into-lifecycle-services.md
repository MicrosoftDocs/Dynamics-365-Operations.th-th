---
title: ER อัพโหลดการตั้งค่าคอนฟิกลงใน Lifecycle Services
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) และอัพโหลดลงใน Microsoft Lifecycle Services (LCS) '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551124"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="cae94-103">ER อัพโหลดการตั้งค่าคอนฟิกลงใน Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="cae94-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cae94-104">ขั้นตอนต่อไปนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ใหม่ (ER) และอัพโหลดลงใน Microsoft Lifecycle Services (LCS) </span><span class="sxs-lookup"><span data-stu-id="cae94-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="cae94-105">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกและอัพโหลดไปยัง LCS สำหรับบริษัทตัวอย่างซึ่งคือ Litware, inc ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="cae94-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="cae94-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="cae94-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="cae94-107">การเข้าถึง LCS ยังต้องการสำหรับการเสร็จสมบูรณ์ของขั้นตอนเหล่านี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cae94-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="cae94-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="cae94-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cae94-109">เลือก ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="cae94-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="cae94-110">และกำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="cae94-110">and set it as active.</span></span>
3. <span data-ttu-id="cae94-111">คลิกการตั้งค่าคอนฟลิก</span><span class="sxs-lookup"><span data-stu-id="cae94-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="cae94-112">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="cae94-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="cae94-113">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cae94-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="cae94-114">คุณจะสร้างการตั้งค่าคอนฟิกที่ประกอบด้วย แบบจำลองข้อมูลตัวอย่างสำหรับเอกสารทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="cae94-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="cae94-115">การตั้งค่าคอนฟิกแบบจำลองข้อมูลนี้จะถูกอัพโหลดลงใน LCS ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="cae94-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="cae94-116">ในฟิลด์ชื่อ พิมพ์ 'การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="cae94-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="cae94-117">การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cae94-117">Sample model configuration</span></span>  
3. <span data-ttu-id="cae94-118">ในฟิลด์คำอธิบาย พิมพ์ 'การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="cae94-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="cae94-119">การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cae94-119">Sample model configuration</span></span>  
4. <span data-ttu-id="cae94-120">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="cae94-120">Click Create configuration.</span></span>
5. <span data-ttu-id="cae94-121">คลิก ตัวออกแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="cae94-121">Click Model designer.</span></span>
6. <span data-ttu-id="cae94-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="cae94-122">Click New.</span></span>
7. <span data-ttu-id="cae94-123">ในฟิลด์ชื่อ ให้พิมพ์ 'จุดเข้าใช้งาน'</span><span class="sxs-lookup"><span data-stu-id="cae94-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="cae94-124">จุดเข้าใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cae94-124">Entry point</span></span>  
8. <span data-ttu-id="cae94-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cae94-125">Click Add.</span></span>
9. <span data-ttu-id="cae94-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="cae94-126">Click Save.</span></span>
10. <span data-ttu-id="cae94-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cae94-127">Close the page.</span></span>
11. <span data-ttu-id="cae94-128">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="cae94-128">Click Change status.</span></span>
12. <span data-ttu-id="cae94-129">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cae94-129">Click Complete.</span></span>
13. <span data-ttu-id="cae94-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cae94-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="cae94-131">ลงทะเบียนที่จัดเก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="cae94-131">Register a new  repository</span></span>
1. <span data-ttu-id="cae94-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cae94-132">Close the page.</span></span>
2. <span data-ttu-id="cae94-133">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="cae94-133">Click Repositories.</span></span>
    * <span data-ttu-id="cae94-134">การดำเนินการนี้ทำให้คุณสามารถเปิดรายการในรายการของที่เก็บ สำหรับผู้ให้บริการการตั้งค่าคอนฟิก Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="cae94-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="cae94-135">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cae94-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="cae94-136">การดำเนินการนี้อนุญาตให้คุณเพิ่มที่เก็บใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="cae94-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="cae94-137">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก เลือก LCS</span><span class="sxs-lookup"><span data-stu-id="cae94-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="cae94-138">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="cae94-138">Click Create repository.</span></span>
6. <span data-ttu-id="cae94-139">ในฟิลด์โครงการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cae94-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="cae94-140">เลือกโครงการ LCS ที่ต้องการ </span><span class="sxs-lookup"><span data-stu-id="cae94-140">Select the desired LCS project.</span></span> <span data-ttu-id="cae94-141">คุณต้องมีการเข้าถึงโครงการ</span><span class="sxs-lookup"><span data-stu-id="cae94-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="cae94-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cae94-142">Click OK.</span></span>
    * <span data-ttu-id="cae94-143">ดำเนินการรายการที่เก็บใหม่ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cae94-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="cae94-144">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cae94-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cae94-145">เลือกเรกคอร์ดที่เก็บ LCS</span><span class="sxs-lookup"><span data-stu-id="cae94-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="cae94-146">หมายเหตุว่า ที่เก็บที่ลงทะเบียนแล้วถูกทำเครื่องหมายโดยผู้ให้บริการปัจจุบัน ซึ่งหมายถึงว่า เฉพาะการตั้งค่าคอนฟิกที่เป็นเจ้าของโดยผู้ให้บริการสามารถถูกวางในที่เก็บนี้ได้ และถูกอัพโหลดลงในโครงการ LCS ที่เลือกได้ ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="cae94-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="cae94-147">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="cae94-147">Click Open.</span></span>
    * <span data-ttu-id="cae94-148">เปิดที่เก็บเพื่อดูรายการของการตั้งค่าคอนฟิก ER </span><span class="sxs-lookup"><span data-stu-id="cae94-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="cae94-149">ซึ่งจะว่างเปล่าถ้าโครงการนี้ยังไม่ได้ถูกใช้สำหรับการใช้การตั้งค่าคอนฟิก ER ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="cae94-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="cae94-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cae94-150">Close the page.</span></span>
11. <span data-ttu-id="cae94-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cae94-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="cae94-152">อัพโหลดการตั้งค่าคอนฟิกลงใน LCS</span><span class="sxs-lookup"><span data-stu-id="cae94-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="cae94-153">คลิกการตั้งค่าคอนฟลิก</span><span class="sxs-lookup"><span data-stu-id="cae94-153">Click Configurations.</span></span>
2. <span data-ttu-id="cae94-154">ในแผนภูมิ เลือก 'การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="cae94-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="cae94-155">เลือกการตั้งค่าคอนฟิกที่สร้างขึ้น ซึ่งได้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="cae94-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="cae94-156">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cae94-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cae94-157">เลือกเวอร์ชันของการตั้งค่าคอนฟิกที่เลือก ที่มีสถานะเป็น 'เสร็จสมบูรณ์แล้ว'</span><span class="sxs-lookup"><span data-stu-id="cae94-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="cae94-158">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="cae94-158">Click Change status.</span></span>
5. <span data-ttu-id="cae94-159">คลิกใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="cae94-159">Click Share.</span></span>
    * <span data-ttu-id="cae94-160">สถานะการตั้งค่าคอนฟิกจะเปลี่ยนจาก 'เสร็จสมบูรณ์แล้ว' เป็น 'ใช้ร่วมกัน' เมื่อมีการเผยแพร่ใน LCS</span><span class="sxs-lookup"><span data-stu-id="cae94-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="cae94-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="cae94-161">Click OK.</span></span>
7. <span data-ttu-id="cae94-162">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cae94-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cae94-163">เลือกเวอร์ชันของการตั้งค่าคอนฟิกที่มีสถานะเป็น 'ใช้ร่วมกัน'</span><span class="sxs-lookup"><span data-stu-id="cae94-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="cae94-164">หมายเหตุว่า สถานะของเวอร์ชันที่เลือกได้เปลี่ยนจาก 'เสร็จสมบูรณ์แล้ว' เป็น 'ใช้ร่วมกัน'</span><span class="sxs-lookup"><span data-stu-id="cae94-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="cae94-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cae94-165">Close the page.</span></span>
9. <span data-ttu-id="cae94-166">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="cae94-166">Click Repositories.</span></span>
    * <span data-ttu-id="cae94-167">การดำเนินการนี้ทำให้คุณสามารถเปิดรายการในรายการของที่เก็บ สำหรับผู้ให้บริการการตั้งค่าคอนฟิก Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="cae94-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="cae94-168">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="cae94-168">Click Open.</span></span>
    * <span data-ttu-id="cae94-169">เลือกที่เก็บ LCS และเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="cae94-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="cae94-170">หมายเหตุว่า การตั้งค่าคอนฟิกที่เลือกถูกแสดงเป็นสินทรัพย์ของโครงการ LCS ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cae94-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="cae94-171">เปิดใช้ LCS โดยใช้ https://lcs.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="cae94-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="cae94-172">เปิดโครงการที่ถูกใช้ก่อนหน้าสำหรับการลงทะเบียนที่เก็บ เปิด 'ไลบรารีแอสเซท' ของโครงการนี้และขยายเนื้อหาของชนิดสินทรัพย์ 'การตั้งค่าคอนฟิก GER' – การตั้งค่าคอนฟิก ER ที่อัพโหลดแล้วจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cae94-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="cae94-173">โปรดทราบว่า การตั้งค่าคอนฟิก LCS ที่อัปโหลดสามารถถูกนำเข้าไปยังอินสแตนซ์ Microsoft Dynamics 365 for Finance and Operations Enterprise edition อีกรายการหนึ่งได้ หากผู้ให้บริการมีการเข้าถึงไปยังโครงการ LCS นี้</span><span class="sxs-lookup"><span data-stu-id="cae94-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  

