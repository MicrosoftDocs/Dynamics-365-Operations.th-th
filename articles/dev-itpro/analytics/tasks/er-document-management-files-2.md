--- 
title: "ขยายแบบจำลองข้อมูลเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69bd2e589f86a6885e6b2a7b2fe82cfe8d55f278
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="d4fbf-103">ขยายแบบจำลองข้อมูลเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d4fbf-103">Extend data model to use Document Management files in format outputs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4fbf-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="d4fbf-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d4fbf-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="d4fbf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d4fbf-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในคู่มืองาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 1: เตรียมแบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="d4fbf-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="d4fbf-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="d4fbf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="d4fbf-108">ขยายแบบจำลองข้อมูลเพื่อแสดงไฟล์การจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d4fbf-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="d4fbf-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d4fbf-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d4fbf-110">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="d4fbf-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d4fbf-111">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="d4fbf-112">ในแผนภูมิ เลือก 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="d4fbf-113">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="d4fbf-113">Click Designer.</span></span>
6. <span data-ttu-id="d4fbf-114">ในแผนภูมิ ให้เลือก 'Customer invoice(InvoiceCustomer)'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="d4fbf-115">เราจะขยายแบบจำลองข้อมูลนี้เพื่อแสดงข้อมูลในไฟล์ใดๆ ที่แนบมากับใบสั่งขายที่เกี่ยวข้องกับใบแจ้งหนี้ที่ประมวลผลทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d4fbf-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="d4fbf-116">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d4fbf-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="d4fbf-117">ในฟิลด์ชื่อ ให้พิมพ์ 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="d4fbf-118">เอกสารแนบใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d4fbf-118">Invoice attachments</span></span>  
9. <span data-ttu-id="d4fbf-119">ในฟิลด์ประเภทสินค้า ให้เลือก 'รายการบันทึก'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="d4fbf-120">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d4fbf-120">Click Add.</span></span>
11. <span data-ttu-id="d4fbf-121">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d4fbf-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="d4fbf-122">ในฟิลด์ชื่อ ให้พิมพ์ 'เนื้อหาไฟล์'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="d4fbf-123">เนื้อหาไฟล์</span><span class="sxs-lookup"><span data-stu-id="d4fbf-123">File content</span></span>  
13. <span data-ttu-id="d4fbf-124">ในฟิลด์ประเภทสินค้า ให้เลือก 'คอนเทนเนอร์'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="d4fbf-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d4fbf-125">Click Add.</span></span>
15. <span data-ttu-id="d4fbf-126">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d4fbf-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="d4fbf-127">ในฟิลด์ชื่อ ให้พิมพ์ 'ชื่อไฟล์'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="d4fbf-128">ชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="d4fbf-128">File name</span></span>  
17. <span data-ttu-id="d4fbf-129">ในฟิลด์ประเภทสินค้า ให้เลือก 'สตริง'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="d4fbf-130">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d4fbf-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="d4fbf-131">แม็ปองค์ประกอบแบบจำลองข้อมูลใหม่ไปยังแหล่งข้อมูล Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d4fbf-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="d4fbf-132">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4fbf-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="d4fbf-133">ใช้ตัวกรองด่วนเพื่อกรองข้อมูลในฟิลด์คำนิยามด้วยค่า 'InvoiceCustomer'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="d4fbf-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="d4fbf-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="d4fbf-135">เราจะแม็ปองค์ประกอบแบบจำลองใหม่ไปยังแหล่งข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d4fbf-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="d4fbf-136">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="d4fbf-136">Click Designer.</span></span>
4. <span data-ttu-id="d4fbf-137">ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="d4fbf-138">ในแผนภูมิ ให้ขยาย 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="d4fbf-139">ในแผนภูมิ ให้เลือก 'Invoice attachments\File name'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="d4fbf-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d4fbf-140">Click Edit.</span></span>
8. <span data-ttu-id="d4fbf-141">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''</span><span class="sxs-lookup"><span data-stu-id="d4fbf-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="d4fbf-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="d4fbf-143">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d4fbf-143">Click Save.</span></span>
10. <span data-ttu-id="d4fbf-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d4fbf-144">Close the page.</span></span>
11. <span data-ttu-id="d4fbf-145">ในแผนภูมิ ให้เลือก 'Invoice attachments\File content'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="d4fbf-146">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d4fbf-146">Click Edit.</span></span>
13. <span data-ttu-id="d4fbf-147">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''</span><span class="sxs-lookup"><span data-stu-id="d4fbf-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="d4fbf-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="d4fbf-149">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d4fbf-149">Click Save.</span></span>
15. <span data-ttu-id="d4fbf-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d4fbf-150">Close the page.</span></span>
16. <span data-ttu-id="d4fbf-151">ในแผนภูมิ ให้เลือก 'เอกสารแนบใบแจ้งหนี้'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="d4fbf-152">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d4fbf-152">Click Edit.</span></span>
18. <span data-ttu-id="d4fbf-153">ในฟิลด์สูตร ให้ป้อน 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''</span><span class="sxs-lookup"><span data-stu-id="d4fbf-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="d4fbf-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="d4fbf-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="d4fbf-155">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d4fbf-155">Click Save.</span></span>
20. <span data-ttu-id="d4fbf-156">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d4fbf-156">Close the page.</span></span>
21. <span data-ttu-id="d4fbf-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d4fbf-157">Click Save.</span></span>
22. <span data-ttu-id="d4fbf-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d4fbf-158">Close the page.</span></span>
23. <span data-ttu-id="d4fbf-159">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d4fbf-159">Close the page.</span></span>
24. <span data-ttu-id="d4fbf-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d4fbf-160">Close the page.</span></span>
25. <span data-ttu-id="d4fbf-161">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="d4fbf-161">Click Change status.</span></span>
26. <span data-ttu-id="d4fbf-162">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d4fbf-162">Click Complete.</span></span>
27. <span data-ttu-id="d4fbf-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d4fbf-163">Click OK.</span></span>


