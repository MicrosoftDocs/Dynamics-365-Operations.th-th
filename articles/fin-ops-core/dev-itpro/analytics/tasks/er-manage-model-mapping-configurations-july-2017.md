---
title: จัดการการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก
description: หัวข้อนี้อธิบายวิธีการจัดการการแม็ปแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f1013cfc9f421525fb0661cd5ace5eeaa157f9a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093809"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="f7f27-103">จัดการการแม็ปแบบจำลอง ER ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f7f27-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7f27-104">ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์สามารถจัดการการแม็ปแบบจำลองการรายงานอิเล็กทรอนิกส์ (ER) ในการตั้งค่าคอนฟิก ER ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f7f27-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="f7f27-105">ในคู่มืองานนี้ คุณจะสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นสำหรับบริษัทตัวอย่าง Litware, Inc. เพื่อทำให้คู่มืองานเหล่านี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำให้ขั้นตอนในคู่มืองานเสร็จสมบูรณ์ "ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก" และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f7f27-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="f7f27-106">เนื่องจากการตั้งค่าคอนฟิก ER จะถูกใช้ร่วมกันระหว่างบริษัท คุณสามารถทำตามคู่มืองานนี้ให้เสร็จสมบูรณ์โดยใช้ชุดข้อมูลบริษัทที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="f7f27-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="f7f27-107">ฟังก์ชันสำหรับคู่มืองานนี้พร้อมใช้งาน ถ้าคุณได้ติดตั้งหนึ่งในโปรแกรมแก้ไขด่วนต่อไปนี้: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 สำหรับรุ่น Dynamics AX 7.0 หรือ https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 สำหรับรุ่น Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="f7f27-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="f7f27-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f7f27-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f7f27-109">ตรวจสอบว่าผู้ให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, Inc. พร้อมใช้งาน และทำเครื่องหมายเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f7f27-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="f7f27-110">ถ้าคุณไม่เห็นผู้ให้บริการการตั้งค่าคอนฟิกนี้ ก่อนอื่นคุณต้องดำเนินขั้นตอนต่างๆ ให้สำเร็จในคู่มืองาน สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="f7f27-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="f7f27-111">เพิ่มการตั้งค่าคอนฟิกแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f27-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="f7f27-112">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="f7f27-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="f7f27-113">เพิ่มการตั้งค่าคอนฟิกแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f27-113">Add a new model configuration.</span></span> <span data-ttu-id="f7f27-114">ชื่อต้องไม่ซ้ำกันในแผนภูมิการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f7f27-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="f7f27-115">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f7f27-116">ในฟิลด์ชื่อ พิมพ์ 'แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="f7f27-117">แบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-117">Sample data model</span></span>  
4. <span data-ttu-id="f7f27-118">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f7f27-118">Click Create configuration.</span></span>
5. <span data-ttu-id="f7f27-119">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-119">Click Designer.</span></span>
6. <span data-ttu-id="f7f27-120">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="f7f27-121">ในฟิลด์ ชื่อ ให้พิมพ์ 'Root'</span><span class="sxs-lookup"><span data-stu-id="f7f27-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="f7f27-122">ราก</span><span class="sxs-lookup"><span data-stu-id="f7f27-122">Root</span></span>  
8. <span data-ttu-id="f7f27-123">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f7f27-123">Click Add.</span></span>
9. <span data-ttu-id="f7f27-124">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="f7f27-125">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f7f27-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="f7f27-126">บริษัท</span><span class="sxs-lookup"><span data-stu-id="f7f27-126">Company</span></span>  
11. <span data-ttu-id="f7f27-127">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f7f27-127">Click Add.</span></span>
12. <span data-ttu-id="f7f27-128">ในฟิลด์คำอธิบาย ป้อนข้อความ คำอธิบายของนิติบุคคลหรือบริษัทที่ผู้ใช้บันทึกขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7f27-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="f7f27-129">คำอธิบายเกี่ยวกับนิติบุคคลหรือบริษัทที่ผู้ใช้บันทึกขณะทำงาน</span><span class="sxs-lookup"><span data-stu-id="f7f27-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="f7f27-130">คลิก การอ้างอิงราก</span><span class="sxs-lookup"><span data-stu-id="f7f27-130">Click Root reference.</span></span>
14. <span data-ttu-id="f7f27-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f27-131">Click OK.</span></span>
15. <span data-ttu-id="f7f27-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f7f27-132">Click Save.</span></span>
16. <span data-ttu-id="f7f27-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-133">Close the page.</span></span>
17. <span data-ttu-id="f7f27-134">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="f7f27-134">Click Change status.</span></span>
18. <span data-ttu-id="f7f27-135">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f7f27-135">Click Complete.</span></span>
19. <span data-ttu-id="f7f27-136">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f7f27-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="f7f27-137">เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลองของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f27-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="f7f27-138">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f7f27-139">ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองตามแบบจำลองข้อมูลตัวอย่างของแบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="f7f27-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="f7f27-140">ในฟิลด์ชื่อ พิมพ์ 'การแม็ปตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="f7f27-141">การแม็ปตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-141">Sample mapping</span></span>  
4. <span data-ttu-id="f7f27-142">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f7f27-142">Click Create configuration.</span></span>
5. <span data-ttu-id="f7f27-143">ขยายหรือยุบส่วน ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="f7f27-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="f7f27-144">กลุ่มข้อกำหนดเบื้องต้น การใช้งาน ได้ถูกเพิ่มโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f7f27-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="f7f27-145">กลุ่มดังกล่าวประกอบด้วยส่วนประกอบข้อกำหนดเบื้องต้นที่อ้างอิงถึงการตั้งค่าคอนฟิกแบบจำลองข้อมูลหลัก และมีการทำเครื่องหมายเป็น การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f7f27-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="f7f27-146">สิ่งนี้หมายความว่าการตั้งค่าคอนฟิกการแม็ปแบบจำลองการแม็ปตัวอย่างนี้จะถือเป็นการใช้งานของแบบจำลองข้อมูล แบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="f7f27-147">ดังนั้น ส่วนประกอบนี้จะบังคับให้ ER ดาวน์โหลดการตั้งค่าคอนฟิกการแม็ปแบบจำลองการแม็ปตัวอย่างจากที่เก็บ ER เมื่อใดก็ตามที่มีการดาวน์โหลดการตั้งค่าคอนฟิกแบบจำลองแบบจำลองข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="f7f27-148">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-148">Click Designer.</span></span>
    * <span data-ttu-id="f7f27-149">การตั้งค่าคอนฟิกการแม็ปแบบจำลองที่สร้างขึ้นประกอบด้วยการแม็ปที่ว่างเปล่าใหม่ที่มีชื่อเดียวกับการตั้งค่าคอนฟิกที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7f27-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="f7f27-150">เมื่อการตั้งค่าคอนฟิกแบบจำลองหลักที่เลือกประกอบด้วยการแม็ปแบบจำลอง รายการเหล่านั้นจะถูกคัดลอกไปที่การตั้งค่าคอนฟิกการแม็ปแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f27-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="f7f27-151">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-151">Click Designer.</span></span>
8. <span data-ttu-id="f7f27-152">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="f7f27-153">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="f7f27-153">Click Add root.</span></span>
10. <span data-ttu-id="f7f27-154">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f7f27-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="f7f27-155">บริษัท</span><span class="sxs-lookup"><span data-stu-id="f7f27-155">Company</span></span>  
11. <span data-ttu-id="f7f27-156">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="f7f27-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="f7f27-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="f7f27-157">CompanyInfo</span></span>  
12. <span data-ttu-id="f7f27-158">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f27-158">Click OK.</span></span>
13. <span data-ttu-id="f7f27-159">ในแผนภูมิ ให้ขยาย 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f7f27-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="f7f27-160">ในแผนภูมิ ขยาย 'Company\find()'</span><span class="sxs-lookup"><span data-stu-id="f7f27-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="f7f27-161">ในแผนภูมิ ให้เลือก 'Company\find()\Name'</span><span class="sxs-lookup"><span data-stu-id="f7f27-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="f7f27-162">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f7f27-162">Click Bind.</span></span>
17. <span data-ttu-id="f7f27-163">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f7f27-163">Click Save.</span></span>
18. <span data-ttu-id="f7f27-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-164">Close the page.</span></span>
19. <span data-ttu-id="f7f27-165">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-165">Close the page.</span></span>
20. <span data-ttu-id="f7f27-166">ในบานหน้าต่างการดำเนินการ คลิก การจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="f7f27-167">คลิก พารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f7f27-167">Click User parameters.</span></span>
22. <span data-ttu-id="f7f27-168">เลือก ใช่ ในฟิลด์ รันการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f7f27-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="f7f27-169">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f27-169">Click OK.</span></span>
24. <span data-ttu-id="f7f27-170">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f7f27-170">Click Edit.</span></span>
25. <span data-ttu-id="f7f27-171">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="f7f27-172">เพิ่มการตั้งค่าคอนฟิกรูปแบบของ ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="f7f27-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="f7f27-173">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="f7f27-174">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f7f27-175">ในฟิลด์ใหม่ ป้อน 'จัดรูปแบบตามแบบจำลองข้อมูล แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="f7f27-176">ในฟิลด์ชื่อ พิมพ์ 'รูปแบบตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="f7f27-177">รูปแบบตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-177">Sample format</span></span>  
5. <span data-ttu-id="f7f27-178">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f7f27-178">Click Create configuration.</span></span>
6. <span data-ttu-id="f7f27-179">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-179">Click Designer.</span></span>
7. <span data-ttu-id="f7f27-180">คลิกเพิ่มรากเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="f7f27-181">ในแผนภูมิ ให้เลือก 'ข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="f7f27-182">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f27-182">Click OK.</span></span>
10. <span data-ttu-id="f7f27-183">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="f7f27-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="f7f27-184">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="f7f27-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="f7f27-185">ในแผนภูมิ ให้เลือก 'model\Company'</span><span class="sxs-lookup"><span data-stu-id="f7f27-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="f7f27-186">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="f7f27-186">Click Bind.</span></span>
14. <span data-ttu-id="f7f27-187">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f7f27-187">Click Save.</span></span>
15. <span data-ttu-id="f7f27-188">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-188">Close the page.</span></span>
    * <span data-ttu-id="f7f27-189">เรียกใช้เวอร์ชันแบบร่างของรูปแบบที่สร้างขึ้นสำหรับวัตถุประสงค์ในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="f7f27-190">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="f7f27-190">Click Run.</span></span>
    * <span data-ttu-id="f7f27-191">บนแท็บด่วนเวอร์ชัน คลิกรัน</span><span class="sxs-lookup"><span data-stu-id="f7f27-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="f7f27-192">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f27-192">Click OK.</span></span>
    * <span data-ttu-id="f7f27-193">ตรวจทานผลลัพธ์ที่ประกอบด้วยชื่อของบริษัทซึ่งผู้ใช้ที่กำลังรันการตั้งค่าคอนฟิกรูปแบบนี้จะเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="f7f27-194">การตั้งค่าคอนฟิกการแม็ปแบบจำลองที่สร้างขึ้นจะถูกใช้โดยการตั้งค่าคอนฟิกรูปแบบนี้เนื่องจากมีเพียงการตั้งค่าคอนฟิกเดียวที่พร้อมใช้งานที่ประกอบด้วยการแม็ปแบบจำลองที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f7f27-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="f7f27-195">เพิ่มการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER สำรอง</span><span class="sxs-lookup"><span data-stu-id="f7f27-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="f7f27-196">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="f7f27-197">คลิก สร้างการตั้งค่าคอนฟิก เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="f7f27-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f7f27-198">ในฟิลด์ใหม่ ป้อน 'การแม็ปแบบจำลองตามแบบจำลองข้อมูลตัวอย่างของแบบจำลองข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="f7f27-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="f7f27-199">ในฟิลด์ชื่อ พิมพ์ 'การแม็บตัวอย่าง (สำรอง)'</span><span class="sxs-lookup"><span data-stu-id="f7f27-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="f7f27-200">การแม็ปตัวอย่าง (สำรอง)</span><span class="sxs-lookup"><span data-stu-id="f7f27-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="f7f27-201">คลิก สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f7f27-201">Click Create configuration.</span></span>
6. <span data-ttu-id="f7f27-202">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-202">Click Designer.</span></span>
7. <span data-ttu-id="f7f27-203">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="f7f27-203">Click Designer.</span></span>
8. <span data-ttu-id="f7f27-204">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="f7f27-205">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="f7f27-205">Click Add root.</span></span>
10. <span data-ttu-id="f7f27-206">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f7f27-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="f7f27-207">บริษัท</span><span class="sxs-lookup"><span data-stu-id="f7f27-207">Company</span></span>  
11. <span data-ttu-id="f7f27-208">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="f7f27-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="f7f27-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="f7f27-209">CompanyInfo</span></span>  
12. <span data-ttu-id="f7f27-210">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f27-210">Click OK.</span></span>
13. <span data-ttu-id="f7f27-211">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f7f27-211">Click Edit.</span></span>
14. <span data-ttu-id="f7f27-212">ในแผนภูมิ เลือก 'สตริง\เชื่อมเข้าด้วยกัน'</span><span class="sxs-lookup"><span data-stu-id="f7f27-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="f7f27-213">คลิก เพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="f7f27-213">Click Add function.</span></span>
16. <span data-ttu-id="f7f27-214">ในแผนภูมิ ให้ขยาย 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="f7f27-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="f7f27-215">ในแผนภูมิ ขยาย 'Company\find()'</span><span class="sxs-lookup"><span data-stu-id="f7f27-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="f7f27-216">ในแผนภูมิ ให้เลือก 'Company\find()\Name'</span><span class="sxs-lookup"><span data-stu-id="f7f27-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="f7f27-217">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f7f27-217">Click Add data source.</span></span>
20. <span data-ttu-id="f7f27-218">ในฟิลด์สูตร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f7f27-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="f7f27-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="f7f27-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="f7f27-220">ในแผนภูมิ ให้เลือก 'Company\find()\Company(DataArea)'</span><span class="sxs-lookup"><span data-stu-id="f7f27-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="f7f27-221">คลิก เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f7f27-221">Click Add data source.</span></span>
23. <span data-ttu-id="f7f27-222">ในฟิลด์สูตร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f7f27-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="f7f27-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="f7f27-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="f7f27-224">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f7f27-224">Click Save.</span></span>
25. <span data-ttu-id="f7f27-225">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-225">Close the page.</span></span>
26. <span data-ttu-id="f7f27-226">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f7f27-226">Click Save.</span></span>
27. <span data-ttu-id="f7f27-227">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-227">Close the page.</span></span>
28. <span data-ttu-id="f7f27-228">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f7f27-228">Close the page.</span></span>
29. <span data-ttu-id="f7f27-229">เลือก ใช่ ในฟิลด์ รันฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="f7f27-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="f7f27-230">ใช้การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f7f27-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="f7f27-231">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง\รูปแบบตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="f7f27-232">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f7f27-232">Click Run.</span></span>
    * <span data-ttu-id="f7f27-233">โปรดทราบว่าจะไม่สามารถดำเนินการรุ่นแบบร่างที่เลือกของการตั้งค่าคอนฟิกรูปแบบ ER ได้ เนื่องจากมีการตั้งค่าคอนฟิกการแม็ปแบบจำลองมากกว่าหนึ่งรายการที่พร้อมใช้งานสำหรับแบบจำลองข้อมูลที่ไม่ได้กำหนดไว้ซึ่งได้ถูกเลือกเป็นแหล่งข้อมูลของรูปแบบ ER ที่กำลังรันอยู่</span><span class="sxs-lookup"><span data-stu-id="f7f27-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="f7f27-234">ถัดไป คุณจะกำหนดการตั้งค่าคอนฟิกการแม็ปแบบจำลองสำรองเป็นการตั้งค่าคอนฟิกที่การแม็ปแบบจำลองจะใช้เป็นแหล่งข้อมูลสำหรับการรันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="f7f27-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="f7f27-235">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง\การแม็ปตัวอย่าง (สำรอง)'</span><span class="sxs-lookup"><span data-stu-id="f7f27-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="f7f27-236">เลือก ใช่ ในฟิลด์ ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="f7f27-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="f7f27-237">ในแผนภูมิ เลือก 'แบบจำลองข้อมูลตัวอย่าง\รูปแบบตัวอย่าง'</span><span class="sxs-lookup"><span data-stu-id="f7f27-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="f7f27-238">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f7f27-238">Click Run.</span></span>
7. <span data-ttu-id="f7f27-239">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="f7f27-239">Click OK.</span></span>
    * <span data-ttu-id="f7f27-240">การตั้งค่าคอนฟิกการแม็ปแบบจำลองเริ่มต้นจะถูกใช้โดยการตั้งค่าคอนฟิกรูปแบบนี้สำหรับการสร้างเอกสารอิเล็กทรอนิกส์ (ผลลัพธ์ที่สร้างขึ้นประกอบด้วยรหัสบริษัท)</span><span class="sxs-lookup"><span data-stu-id="f7f27-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

