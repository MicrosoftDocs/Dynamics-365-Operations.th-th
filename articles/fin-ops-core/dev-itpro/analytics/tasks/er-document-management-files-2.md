---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2 - ขยายแบบจำลองข้อมูล)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032f9c5707294ee33cc848ecc6990c1ef5bbfdbb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185048"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="d1edd-103">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2: ขยายแบบจำลองข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="d1edd-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1edd-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="d1edd-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d1edd-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="d1edd-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d1edd-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 1: เตรียมแบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="d1edd-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="d1edd-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="d1edd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="d1edd-108">ขยายแบบจำลองข้อมูลเพื่อแสดงไฟล์การจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d1edd-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="d1edd-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1edd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d1edd-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="d1edd-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d1edd-111">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="d1edd-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="d1edd-112">ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="d1edd-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="d1edd-113">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="d1edd-113">Click Designer.</span></span>
6. <span data-ttu-id="d1edd-114">ในแผนภูมิ ให้เลือก 'Customer invoice(InvoiceCustomer)'</span><span class="sxs-lookup"><span data-stu-id="d1edd-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="d1edd-115">เราจะขยายแบบจำลองข้อมูลนี้เพื่อแสดงข้อมูลในไฟล์ใดๆ ที่แนบมากับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d1edd-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="d1edd-116">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d1edd-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="d1edd-117">ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d1edd-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="d1edd-118">เอกสารแนบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d1edd-118">Invoice attachments</span></span>  
9. <span data-ttu-id="d1edd-119">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="d1edd-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="d1edd-120">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d1edd-120">Click Add.</span></span>
11. <span data-ttu-id="d1edd-121">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d1edd-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="d1edd-122">ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'</span><span class="sxs-lookup"><span data-stu-id="d1edd-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="d1edd-123">เนื้อหาไฟล์</span><span class="sxs-lookup"><span data-stu-id="d1edd-123">File content</span></span>  
13. <span data-ttu-id="d1edd-124">ในฟิลด์ประเภทสินค้า ให้เลือก 'คอนเทนเนอร์'</span><span class="sxs-lookup"><span data-stu-id="d1edd-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="d1edd-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d1edd-125">Click Add.</span></span>
15. <span data-ttu-id="d1edd-126">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d1edd-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="d1edd-127">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="d1edd-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="d1edd-128">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="d1edd-128">File name</span></span>  
17. <span data-ttu-id="d1edd-129">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="d1edd-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="d1edd-130">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d1edd-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="d1edd-131">แม็ปองค์ประกอบแบบจำลองข้อมูลใหม่ไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d1edd-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="d1edd-132">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d1edd-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="d1edd-133">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์คำนิยามด้วยค่า 'InvoiceCustomer'</span><span class="sxs-lookup"><span data-stu-id="d1edd-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="d1edd-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="d1edd-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="d1edd-135">เราจะแม็ปองค์ประกอบแบบจำลองใหม่ไปยังแหล่งข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d1edd-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="d1edd-136">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="d1edd-136">Click Designer.</span></span>
4. <span data-ttu-id="d1edd-137">ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d1edd-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="d1edd-138">ในแผนภูมิ ให้ขยาย 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d1edd-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="d1edd-139">ในแผนภูมิ ให้เลือก 'Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="d1edd-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="d1edd-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d1edd-140">Click Edit.</span></span>
8. <span data-ttu-id="d1edd-141">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''</span><span class="sxs-lookup"><span data-stu-id="d1edd-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="d1edd-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="d1edd-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="d1edd-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d1edd-143">Click Save.</span></span>
10. <span data-ttu-id="d1edd-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d1edd-144">Close the page.</span></span>
11. <span data-ttu-id="d1edd-145">ในแผนภูมิ ให้เลือก 'Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="d1edd-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="d1edd-146">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d1edd-146">Click Edit.</span></span>
13. <span data-ttu-id="d1edd-147">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''</span><span class="sxs-lookup"><span data-stu-id="d1edd-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="d1edd-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="d1edd-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="d1edd-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d1edd-149">Click Save.</span></span>
15. <span data-ttu-id="d1edd-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d1edd-150">Close the page.</span></span>
16. <span data-ttu-id="d1edd-151">ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d1edd-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="d1edd-152">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d1edd-152">Click Edit.</span></span>
18. <span data-ttu-id="d1edd-153">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''</span><span class="sxs-lookup"><span data-stu-id="d1edd-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="d1edd-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="d1edd-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="d1edd-155">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d1edd-155">Click Save.</span></span>
20. <span data-ttu-id="d1edd-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d1edd-156">Close the page.</span></span>
21. <span data-ttu-id="d1edd-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d1edd-157">Click Save.</span></span>
22. <span data-ttu-id="d1edd-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d1edd-158">Close the page.</span></span>
23. <span data-ttu-id="d1edd-159">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d1edd-159">Close the page.</span></span>
24. <span data-ttu-id="d1edd-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d1edd-160">Close the page.</span></span>
25. <span data-ttu-id="d1edd-161">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="d1edd-161">Click Change status.</span></span>
26. <span data-ttu-id="d1edd-162">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d1edd-162">Click Complete.</span></span>
27. <span data-ttu-id="d1edd-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d1edd-163">Click OK.</span></span>

