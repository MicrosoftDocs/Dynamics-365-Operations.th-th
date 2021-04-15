---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2 - ขยายแบบจำลองข้อมูล)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER (ส่วนที่ 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754925"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="2c76b-104">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 2 - ขยายแบบจำลองข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="2c76b-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c76b-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="2c76b-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="2c76b-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="2c76b-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="2c76b-107">เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 1: เตรียมแบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="2c76b-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="2c76b-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="2c76b-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="2c76b-109">ขยายแบบจำลองข้อมูลเพื่อแสดงไฟล์การจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="2c76b-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="2c76b-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="2c76b-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2c76b-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="2c76b-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2c76b-112">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="2c76b-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="2c76b-113">ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="2c76b-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="2c76b-114">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="2c76b-114">Click Designer.</span></span>
6. <span data-ttu-id="2c76b-115">ในแผนภูมิ ให้เลือก 'Customer invoice(InvoiceCustomer)'</span><span class="sxs-lookup"><span data-stu-id="2c76b-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="2c76b-116">เราจะขยายแบบจำลองข้อมูลนี้เพื่อแสดงข้อมูลในไฟล์ใดๆ ที่แนบมากับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="2c76b-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="2c76b-117">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2c76b-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="2c76b-118">ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="2c76b-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="2c76b-119">เอกสารแนบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="2c76b-119">Invoice attachments</span></span>  
9. <span data-ttu-id="2c76b-120">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="2c76b-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="2c76b-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2c76b-121">Click Add.</span></span>
11. <span data-ttu-id="2c76b-122">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2c76b-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="2c76b-123">ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'</span><span class="sxs-lookup"><span data-stu-id="2c76b-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="2c76b-124">เนื้อหาไฟล์</span><span class="sxs-lookup"><span data-stu-id="2c76b-124">File content</span></span>  
13. <span data-ttu-id="2c76b-125">ในฟิลด์ประเภทสินค้า ให้เลือก 'คอนเทนเนอร์'</span><span class="sxs-lookup"><span data-stu-id="2c76b-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="2c76b-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2c76b-126">Click Add.</span></span>
15. <span data-ttu-id="2c76b-127">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="2c76b-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="2c76b-128">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="2c76b-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="2c76b-129">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="2c76b-129">File name</span></span>  
17. <span data-ttu-id="2c76b-130">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="2c76b-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="2c76b-131">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2c76b-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="2c76b-132">แม็ปองค์ประกอบแบบจำลองข้อมูลใหม่ไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c76b-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="2c76b-133">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c76b-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="2c76b-134">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์คำนิยามด้วยค่า 'InvoiceCustomer'</span><span class="sxs-lookup"><span data-stu-id="2c76b-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="2c76b-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="2c76b-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="2c76b-136">เราจะแม็ปองค์ประกอบแบบจำลองใหม่ไปยังแหล่งข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="2c76b-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="2c76b-137">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="2c76b-137">Click Designer.</span></span>
4. <span data-ttu-id="2c76b-138">ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="2c76b-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="2c76b-139">ในแผนภูมิ ให้ขยาย 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="2c76b-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="2c76b-140">ในแผนภูมิ ให้เลือก 'Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="2c76b-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="2c76b-141">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="2c76b-141">Click Edit.</span></span>
8. <span data-ttu-id="2c76b-142">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''</span><span class="sxs-lookup"><span data-stu-id="2c76b-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="2c76b-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="2c76b-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="2c76b-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2c76b-144">Click Save.</span></span>
10. <span data-ttu-id="2c76b-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c76b-145">Close the page.</span></span>
11. <span data-ttu-id="2c76b-146">ในแผนภูมิ ให้เลือก 'Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="2c76b-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="2c76b-147">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="2c76b-147">Click Edit.</span></span>
13. <span data-ttu-id="2c76b-148">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''</span><span class="sxs-lookup"><span data-stu-id="2c76b-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="2c76b-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="2c76b-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="2c76b-150">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2c76b-150">Click Save.</span></span>
15. <span data-ttu-id="2c76b-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c76b-151">Close the page.</span></span>
16. <span data-ttu-id="2c76b-152">ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="2c76b-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="2c76b-153">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="2c76b-153">Click Edit.</span></span>
18. <span data-ttu-id="2c76b-154">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''</span><span class="sxs-lookup"><span data-stu-id="2c76b-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="2c76b-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="2c76b-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="2c76b-156">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2c76b-156">Click Save.</span></span>
20. <span data-ttu-id="2c76b-157">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c76b-157">Close the page.</span></span>
21. <span data-ttu-id="2c76b-158">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="2c76b-158">Click Save.</span></span>
22. <span data-ttu-id="2c76b-159">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c76b-159">Close the page.</span></span>
23. <span data-ttu-id="2c76b-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c76b-160">Close the page.</span></span>
24. <span data-ttu-id="2c76b-161">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2c76b-161">Close the page.</span></span>
25. <span data-ttu-id="2c76b-162">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="2c76b-162">Click Change status.</span></span>
26. <span data-ttu-id="2c76b-163">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2c76b-163">Click Complete.</span></span>
27. <span data-ttu-id="2c76b-164">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2c76b-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]