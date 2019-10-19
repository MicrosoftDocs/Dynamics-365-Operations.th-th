---
title: จัดการการแม็ปแบบจำลอง ER ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก
description: ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์สามารถจัดการการแม็ปแบบจำลองการรายงานอิเล็กทรอนิกส์ (ER) ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcf322973ea5e4afd9c828c3cbd1ebbd9972a964
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182266"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="6ec4a-103">จัดการการแม็ปแบบจำลอง ER ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ec4a-104">ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์สามารถจัดการการแม็ปแบบจำลองการรายงานอิเล็กทรอนิกส์ (ER) ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="6ec4a-105">ในคู่มืองานนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำตามคู่มืองานเหล่านี้ในกระบวนงาน อันดับแรกคุณต้องทำขั้นตอนในคู่มืองาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของ ER" ให้เสร็จเรียบร้อยก่อน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="6ec4a-106">เนื่องจากการตั้งค่าคอนฟิก ER จะถูกใช้ร่วมกันระหว่างบริษัท คุณสามารถทำตามคู่มืองานนี้ให้เสร็จสมบูรณ์โดยใช้ชุดข้อมูลบริษัทที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="6ec4a-107">ฟังก์ชันสำหรับคู่มืองานนี้พร้อมใช้งาน ถ้าคุณได้ติดตั้งหนึ่งในโปรแกรมแก้ไขด่วนต่อไปนี้: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 สำหรับรุ่น Dynamics AX 7.0 หรือ https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 สำหรับรุ่น Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="6ec4a-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="6ec4a-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6ec4a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6ec4a-109">ตรวจสอบว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="6ec4a-110">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในคู่มืองาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="6ec4a-111">เพิ่มการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="6ec4a-112">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="6ec4a-113">เพิ่มการตั้งค่าคอนฟิกแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-113">Add a new model configuration.</span></span> <span data-ttu-id="6ec4a-114">ชื่อต้องไม่ซ้ำกันในแผนภูมิการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="6ec4a-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6ec4a-116">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="6ec4a-117">แบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-117">Sample data model</span></span>  
4. <span data-ttu-id="6ec4a-118">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-118">Click Create configuration.</span></span>
5. <span data-ttu-id="6ec4a-119">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-119">Click Designer.</span></span>
6. <span data-ttu-id="6ec4a-120">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6ec4a-121">ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="6ec4a-122">ราก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-122">Root</span></span>  
8. <span data-ttu-id="6ec4a-123">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6ec4a-123">Click Add.</span></span>
9. <span data-ttu-id="6ec4a-124">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="6ec4a-125">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6ec4a-126">บริษัท</span><span class="sxs-lookup"><span data-stu-id="6ec4a-126">Company</span></span>  
11. <span data-ttu-id="6ec4a-127">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6ec4a-127">Click Add.</span></span>
12. <span data-ttu-id="6ec4a-128">ในฟิลด์คำอธิบาย ป้อนข้อความ คำอธิบายของนิติบุคคลหรือบริษัทที่ผู้ใช้บันทึกขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="6ec4a-129">คำอธิบายเกี่ยวกับนิติบุคคลหรือบริษัทที่ผู้ใช้บันทึกขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="6ec4a-130">คลิก การอ้างอิงราก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-130">Click Root reference.</span></span>
14. <span data-ttu-id="6ec4a-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-131">Click OK.</span></span>
15. <span data-ttu-id="6ec4a-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-132">Click Save.</span></span>
16. <span data-ttu-id="6ec4a-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-133">Close the page.</span></span>
17. <span data-ttu-id="6ec4a-134">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-134">Click Change status.</span></span>
18. <span data-ttu-id="6ec4a-135">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6ec4a-135">Click Complete.</span></span>
19. <span data-ttu-id="6ec4a-136">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="6ec4a-137">เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="6ec4a-138">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6ec4a-139">ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองตามแบบจำลองข้อมูลตัวอย่างของแบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="6ec4a-140">ในฟิลด์ชื่อ พิมพ์ 'การแม็ปตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="6ec4a-141">การแม็ปตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-141">Sample mapping</span></span>  
4. <span data-ttu-id="6ec4a-142">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-142">Click Create configuration.</span></span>
5. <span data-ttu-id="6ec4a-143">ขยายหรือยุบส่วน ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6ec4a-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="6ec4a-144">หมายเหตุว่ากลุ่มข้อกำหนดเบื้องต้น การใช้งาน ได้ถูกเพิ่มโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="6ec4a-145">กลุ่มดังกล่าวประกอบด้วยส่วนประกอบข้อกำหนดเบื้องต้นที่อ้างอิงถึงการตั้งค่าคอนฟิกแบบจำลองข้อมูลหลัก และมีการทำเครื่องหมายเป็น การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="6ec4a-146">สิ่งนี้หมายความว่าการตั้งค่าคอนฟิกการแม็ปแบบจำลองการแม็ปตัวอย่างนี้จะถือเป็นการใช้งานของแบบจำลองข้อมูล แบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="6ec4a-147">ดังนั้น ส่วนประกอบนี้จะบังคับให้ ER ดาวน์โหลดการตั้งค่าคอนฟิกการแม็ปแบบจำลองการแม็ปตัวอย่างจากที่เก็บ ER เมื่อใดก็ตามที่มีการดาวน์โหลดการตั้งค่าคอนฟิกแบบจำลองแบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="6ec4a-148">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-148">Click Designer.</span></span>
    * <span data-ttu-id="6ec4a-149">หมายเหตุว่าการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่สร้างขึ้นประกอบด้วยการแม็ปที่ว่างเปล่าใหม่ที่มีชื่อเดียวกับการตั้งค่าคอนฟิกที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6ec4a-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="6ec4a-150">หมายเหตุว่าเมื่อการตั้งค่าคอนฟิกแบบจำลองหลักที่เลือกประกอบด้วยการแม็ปแบบจำลอง รายการเหล่านั้นจะถูกคัดลอกไปที่การตั้งค่าคอนฟิกการแม็ปแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="6ec4a-151">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-151">Click Designer.</span></span>
8. <span data-ttu-id="6ec4a-152">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6ec4a-153">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-153">Click Add root.</span></span>
10. <span data-ttu-id="6ec4a-154">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6ec4a-155">บริษัท</span><span class="sxs-lookup"><span data-stu-id="6ec4a-155">Company</span></span>  
11. <span data-ttu-id="6ec4a-156">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6ec4a-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6ec4a-157">CompanyInfo</span></span>  
12. <span data-ttu-id="6ec4a-158">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-158">Click OK.</span></span>
13. <span data-ttu-id="6ec4a-159">ในแผนภูมิ ให้ขยาย 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="6ec4a-160">ในแผนภูมิ ขยาย 'Company\find()'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="6ec4a-161">ในแผนภูมิ ให้เลือก 'Company\find()\Name'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="6ec4a-162">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-162">Click Bind.</span></span>
17. <span data-ttu-id="6ec4a-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-163">Click Save.</span></span>
18. <span data-ttu-id="6ec4a-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-164">Close the page.</span></span>
19. <span data-ttu-id="6ec4a-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-165">Close the page.</span></span>
20. <span data-ttu-id="6ec4a-166">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="6ec4a-167">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6ec4a-167">Click User parameters.</span></span>
22. <span data-ttu-id="6ec4a-168">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="6ec4a-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-169">Click OK.</span></span>
24. <span data-ttu-id="6ec4a-170">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6ec4a-170">Click Edit.</span></span>
25. <span data-ttu-id="6ec4a-171">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="6ec4a-172">เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="6ec4a-173">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6ec4a-174">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6ec4a-175">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6ec4a-176">ในฟิลด์ชื่อ พิมพ์ 'รูปแบบตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="6ec4a-177">รูปแบบตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-177">Sample format</span></span>  
5. <span data-ttu-id="6ec4a-178">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-178">Click Create configuration.</span></span>
6. <span data-ttu-id="6ec4a-179">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-179">Click Designer.</span></span>
7. <span data-ttu-id="6ec4a-180">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="6ec4a-181">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="6ec4a-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-182">Click OK.</span></span>
10. <span data-ttu-id="6ec4a-183">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="6ec4a-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="6ec4a-184">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="6ec4a-185">ในแผนภูมิ ให้เลือก 'model\Company'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="6ec4a-186">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-186">Click Bind.</span></span>
14. <span data-ttu-id="6ec4a-187">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-187">Click Save.</span></span>
15. <span data-ttu-id="6ec4a-188">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-188">Close the page.</span></span>
    * <span data-ttu-id="6ec4a-189">เรียกใช้เวอร์ชันแบบร่างของรูปแบบที่สร้างขึ้นสำหรับวัตถุประสงค์ในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="6ec4a-190">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="6ec4a-190">Click Run.</span></span>
    * <span data-ttu-id="6ec4a-191">บนแท็บด่วนเวอร์ชัน คลิกรัน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="6ec4a-192">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-192">Click OK.</span></span>
    * <span data-ttu-id="6ec4a-193">ตรวจทานผลลัพธ์ที่ประกอบด้วยชื่อของบริษัทซึ่งผู้ใช้ที่กำลังรันการตั้งค่าคอนฟิกรูปแบบนี้จะเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="6ec4a-194">หมายเหตุว่าการตั้งค่าคอนฟิกการแม็ปแบบจำลองที่สร้างขึ้นจะถูกใช้โดยการตั้งค่าคอนฟิกรูปแบบนี้เนื่องจากมีเพียงการตั้งค่าคอนฟิกเดียวที่พร้อมใช้งานที่ประกอบด้วยการแม็ปแบบจำลองที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="6ec4a-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="6ec4a-195">เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER สำรอง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="6ec4a-196">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6ec4a-197">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6ec4a-198">ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองตามแบบจำลองข้อมูลตัวอย่างของแบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6ec4a-199">ในฟิลด์ชื่อ พิมพ์ 'การแม็บตัวอย่าง (สำรอง)'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="6ec4a-200">การแม็ปตัวอย่าง (สำรอง)</span><span class="sxs-lookup"><span data-stu-id="6ec4a-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="6ec4a-201">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-201">Click Create configuration.</span></span>
6. <span data-ttu-id="6ec4a-202">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-202">Click Designer.</span></span>
7. <span data-ttu-id="6ec4a-203">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ec4a-203">Click Designer.</span></span>
8. <span data-ttu-id="6ec4a-204">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6ec4a-205">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-205">Click Add root.</span></span>
10. <span data-ttu-id="6ec4a-206">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6ec4a-207">บริษัท</span><span class="sxs-lookup"><span data-stu-id="6ec4a-207">Company</span></span>  
11. <span data-ttu-id="6ec4a-208">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6ec4a-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6ec4a-209">CompanyInfo</span></span>  
12. <span data-ttu-id="6ec4a-210">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-210">Click OK.</span></span>
13. <span data-ttu-id="6ec4a-211">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6ec4a-211">Click Edit.</span></span>
14. <span data-ttu-id="6ec4a-212">ในแผนภูมิ เลือก 'สตริง\เชื่อมเข้าด้วยกัน'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="6ec4a-213">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="6ec4a-213">Click Add function.</span></span>
16. <span data-ttu-id="6ec4a-214">ในแผนภูมิ ให้ขยาย 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="6ec4a-215">ในแผนภูมิ ขยาย 'Company\find()'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="6ec4a-216">ในแผนภูมิ ให้เลือก 'Company\find()\Name'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="6ec4a-217">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ec4a-217">Click Add data source.</span></span>
20. <span data-ttu-id="6ec4a-218">ในฟิลด์สูตร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6ec4a-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="6ec4a-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="6ec4a-220">ในแผนภูมิ ให้เลือก 'Company\find()\Company(DataArea)'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="6ec4a-221">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ec4a-221">Click Add data source.</span></span>
23. <span data-ttu-id="6ec4a-222">ในฟิลด์สูตร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6ec4a-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="6ec4a-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="6ec4a-224">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-224">Click Save.</span></span>
25. <span data-ttu-id="6ec4a-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-225">Close the page.</span></span>
26. <span data-ttu-id="6ec4a-226">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ec4a-226">Click Save.</span></span>
27. <span data-ttu-id="6ec4a-227">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-227">Close the page.</span></span>
28. <span data-ttu-id="6ec4a-228">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6ec4a-228">Close the page.</span></span>
29. <span data-ttu-id="6ec4a-229">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="6ec4a-230">ใช้การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="6ec4a-231">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง\รูปแบบตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="6ec4a-232">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="6ec4a-232">Click Run.</span></span>
    * <span data-ttu-id="6ec4a-233">หมายเหตุว่าจะไม่สามารถดำเนินการเวอร์ชันแบบร่างที่เลือกของการตั้งค่าคอนฟิกรูปแบบ ER ได้เนื่องจากมีการตั้งค่าคอนฟิกการแม็ปแบบจำลองมากกว่าหนึ่งรายการที่พร้อมใช้งานสำหรับแบบจำลองข้อมูลที่ไม่ได้กำหนดที่เลือกไว้เป็นแหล่งข้อมูลของรูปแบบ ER ที่กำลังรันอยู่</span><span class="sxs-lookup"><span data-stu-id="6ec4a-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="6ec4a-234">ถัดไป คุณจะกำหนดการตั้งค่าคอนฟิกการแม็ปแบบจำลองสำรองเป็นการตั้งค่าคอนฟิกที่การแม็ปแบบจำลองจะใช้เป็นแหล่งข้อมูลสำหรับการรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="6ec4a-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="6ec4a-235">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง\การแม็ปตัวอย่าง (สำรอง)'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="6ec4a-236">เลือก ใช่ ในฟิลด์ ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="6ec4a-237">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง\รูปแบบตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="6ec4a-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="6ec4a-238">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="6ec4a-238">Click Run.</span></span>
7. <span data-ttu-id="6ec4a-239">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6ec4a-239">Click OK.</span></span>
    * <span data-ttu-id="6ec4a-240">หมายเหตุว่าการตั้งค่าคอนฟิกการแม็ปแบบจำลองเริ่มต้นจะถูกใช้โดยการตั้งค่าคอนฟิกรูปแบบนี้สำหรับการสร้างเอกสารอิเล็กทรอนิกส์ (ผลลัพธ์ที่สร้างขึ้นประกอบด้วยรหัสบริษัท)</span><span class="sxs-lookup"><span data-stu-id="6ec4a-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

