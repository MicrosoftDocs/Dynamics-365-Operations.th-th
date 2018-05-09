--- 
title: "เรียกใช้รูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER "
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.openlocfilehash: 2807307b6bddb253d699c99996f527279385137d
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="run-format-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="f4764-103">เรียกใช้รูปแบบเพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="f4764-103">Run format to use Document Management files in format outputs</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4764-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="f4764-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f4764-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="f4764-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f4764-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 3: สร้างรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="f4764-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="f4764-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="f4764-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="f4764-108">เพิ่มสิ่งที่แนบที่จำเป็นสำหรับใบสั่งขายของใบแจ้งหนี้ใบเดียว</span><span class="sxs-lookup"><span data-stu-id="f4764-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="f4764-109">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > เปิดใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="f4764-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="f4764-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="f4764-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f4764-111">เช่น กรองข้อมูลในฟิลด์ใบแจ้งหนี้ ด้วยค่า 'CIV-000148'</span><span class="sxs-lookup"><span data-stu-id="f4764-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="f4764-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="f4764-112">CIV-000148</span></span>  
3. <span data-ttu-id="f4764-113">คลิกเพื่อติดตามการเชื่อมโยงของใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f4764-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="f4764-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="f4764-114">CIV-000148</span></span>  
4. <span data-ttu-id="f4764-115">คลิกเพื่อติดตามลิงค์ในฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f4764-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="f4764-116">000148</span><span class="sxs-lookup"><span data-stu-id="f4764-116">000148</span></span>  
5. <span data-ttu-id="f4764-117">ในฟิลด์รายการหรือหัวข้อ ให้เลือกตัวเลือกของหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="f4764-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="f4764-118">เลือกหัวข้อเพื่อบ่งชี้ว่านี่จะเป็นเป้าหมายสำหรับการเพิ่มสิ่งที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="f4764-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="f4764-119">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="f4764-119">Click Attach.</span></span>
    * <span data-ttu-id="f4764-120">เพิ่มไฟล์บางรายการเป็นเอกสารแนบสำหรับใบสั่งขายนี้ </span><span class="sxs-lookup"><span data-stu-id="f4764-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="f4764-121">ใช้ไฟล์ชนิดเอกสารที่รองรับโดยการจัดการเอกสาร (ที่มีนามสกุลไฟล์ DOCX, DPF, XML, JPG ฯลฯ) </span><span class="sxs-lookup"><span data-stu-id="f4764-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="f4764-122">เลือกดูและเลือกไฟล์ที่จะแนบและประมวลผลเพิ่มเติมกับใบแจ้งหนี้ที่เกี่ยวข้องในข้อความอิเล็กทรอนิกส์ ER</span><span class="sxs-lookup"><span data-stu-id="f4764-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="f4764-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f4764-123">Click New.</span></span>
8. <span data-ttu-id="f4764-124">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="f4764-124">Click File.</span></span>
9. <span data-ttu-id="f4764-125">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f4764-125">Click New.</span></span>
10. <span data-ttu-id="f4764-126">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="f4764-126">Click File.</span></span>
11. <span data-ttu-id="f4764-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f4764-127">Close the page.</span></span>
12. <span data-ttu-id="f4764-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f4764-128">Close the page.</span></span>
13. <span data-ttu-id="f4764-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f4764-129">Close the page.</span></span>
14. <span data-ttu-id="f4764-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f4764-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="f4764-131">รันรายงานที่ออกแบบไว้สำหรับใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f4764-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="f4764-132">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f4764-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f4764-133">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="f4764-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="f4764-134">ในแผนภูมิ ขยาย 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="f4764-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f4764-135">ในแผนภูมิ เลือกตัวอย่างข้อความใบแจ้งหนี้ 'Customer invoice model\Customer invoice model (custom)\Electronic'</span><span class="sxs-lookup"><span data-stu-id="f4764-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="f4764-136">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="f4764-136">Click Run.</span></span>
6. <span data-ttu-id="f4764-137">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน ()</span><span class="sxs-lookup"><span data-stu-id="f4764-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="f4764-138">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="f4764-138">Click Filter.</span></span>
8. <span data-ttu-id="f4764-139">เลือกแถวของสมุดรายวันใบแจ้งหนี้ของลูกค้าและฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f4764-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="f4764-140">ในฟิลด์เกณฑ์ ให้พิมพ์ '000148'</span><span class="sxs-lookup"><span data-stu-id="f4764-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="f4764-141">ในฟิลด์ "ใบสั่งขาย" เกณฑ์ ให้พิมพ์หมายเลขใบสั่ง 000148</span><span class="sxs-lookup"><span data-stu-id="f4764-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="f4764-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f4764-142">Click OK.</span></span>
11. <span data-ttu-id="f4764-143">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f4764-143">Click OK.</span></span>
    * <span data-ttu-id="f4764-144">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="f4764-144">Review the generated output.</span></span> <span data-ttu-id="f4764-145">โปรดทราบว่าสำหรับแต่ละเอกสารแนบจะมีการสร้างโหนด XML เดียว </span><span class="sxs-lookup"><span data-stu-id="f4764-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="f4764-146">ระบบจะเติมเนื้อหาของเอกสารแนบกับผลลัพธ์ XML ในรูปแบบข้อความ MIME (base64)</span><span class="sxs-lookup"><span data-stu-id="f4764-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  


