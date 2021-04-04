---
title: ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 4 - รันรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อใช้ไฟล์การจัดการเอกสารในผลลัพธ์ ER (ส่วนที่ 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede71118f64eec27b150a4c575aead97d3174509
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559736"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="fcbd5-104">ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 4 - รันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="fcbd5-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcbd5-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ให้ใช้ไฟล์การจัดการเอกสาร (เอกสารแนบ) ในผลลัพธ์ ER </span><span class="sxs-lookup"><span data-stu-id="fcbd5-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="fcbd5-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="fcbd5-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="fcbd5-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "ER ใช้ไฟล์การจัดการเอกสารในผลลัพธ์รูปแบบ (ส่วนที่ 3: สร้างรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="fcbd5-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="fcbd5-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="fcbd5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="fcbd5-109">เพิ่มสิ่งที่แนบที่จำเป็นสำหรับใบสั่งขายของใบแจ้งหนี้ใบเดียว</span><span class="sxs-lookup"><span data-stu-id="fcbd5-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="fcbd5-110">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > เปิดใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fcbd5-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="fcbd5-111">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="fcbd5-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fcbd5-112">เช่น กรองข้อมูลในฟิลด์ใบแจ้งหนี้ ด้วยค่า 'CIV-000148'</span><span class="sxs-lookup"><span data-stu-id="fcbd5-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="fcbd5-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="fcbd5-113">CIV-000148</span></span>  
3. <span data-ttu-id="fcbd5-114">คลิกเพื่อติดตามการเชื่อมโยงของใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fcbd5-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="fcbd5-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="fcbd5-115">CIV-000148</span></span>  
4. <span data-ttu-id="fcbd5-116">คลิกเพื่อติดตามลิงค์ในฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fcbd5-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="fcbd5-117">000148</span><span class="sxs-lookup"><span data-stu-id="fcbd5-117">000148</span></span>  
5. <span data-ttu-id="fcbd5-118">ในฟิลด์รายการหรือหัวข้อ ให้เลือกตัวเลือกของหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="fcbd5-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="fcbd5-119">เลือกหัวข้อเพื่อบ่งชี้ว่านี่จะเป็นเป้าหมายสำหรับการเพิ่มสิ่งที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="fcbd5-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="fcbd5-120">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="fcbd5-120">Click Attach.</span></span>
    * <span data-ttu-id="fcbd5-121">เพิ่มไฟล์บางรายการเป็นเอกสารแนบสำหรับใบสั่งขายนี้ </span><span class="sxs-lookup"><span data-stu-id="fcbd5-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="fcbd5-122">ใช้ไฟล์ชนิดเอกสารที่รองรับโดยการจัดการเอกสาร (ที่มีนามสกุลไฟล์ DOCX, DPF, XML, JPG ฯลฯ) </span><span class="sxs-lookup"><span data-stu-id="fcbd5-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="fcbd5-123">เลือกดูและเลือกไฟล์ที่จะแนบและประมวลผลเพิ่มเติมกับใบแจ้งหนี้ที่เกี่ยวข้องในข้อความอิเล็กทรอนิกส์ ER</span><span class="sxs-lookup"><span data-stu-id="fcbd5-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="fcbd5-124">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fcbd5-124">Click New.</span></span>
8. <span data-ttu-id="fcbd5-125">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="fcbd5-125">Click File.</span></span>
9. <span data-ttu-id="fcbd5-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fcbd5-126">Click New.</span></span>
10. <span data-ttu-id="fcbd5-127">คลิกไฟล์</span><span class="sxs-lookup"><span data-stu-id="fcbd5-127">Click File.</span></span>
11. <span data-ttu-id="fcbd5-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fcbd5-128">Close the page.</span></span>
12. <span data-ttu-id="fcbd5-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fcbd5-129">Close the page.</span></span>
13. <span data-ttu-id="fcbd5-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fcbd5-130">Close the page.</span></span>
14. <span data-ttu-id="fcbd5-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fcbd5-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="fcbd5-132">รันรายงานที่ออกแบบไว้สำหรับใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fcbd5-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="fcbd5-133">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fcbd5-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fcbd5-134">ในแผนภูมิ ให้ขยาย 'แบบจำลองใบแจ้งหนี้ของลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="fcbd5-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="fcbd5-135">ในแผนภูมิ ขยาย 'Customer invoice model\Customer invoice model (custom)'</span><span class="sxs-lookup"><span data-stu-id="fcbd5-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="fcbd5-136">ในแผนภูมิ เลือกตัวอย่างข้อความใบแจ้งหนี้ 'Customer invoice model\Customer invoice model (custom)\Electronic'</span><span class="sxs-lookup"><span data-stu-id="fcbd5-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="fcbd5-137">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="fcbd5-137">Click Run.</span></span>
6. <span data-ttu-id="fcbd5-138">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน ()</span><span class="sxs-lookup"><span data-stu-id="fcbd5-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="fcbd5-139">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="fcbd5-139">Click Filter.</span></span>
8. <span data-ttu-id="fcbd5-140">เลือกแถวของสมุดรายวันใบแจ้งหนี้ของลูกค้าและฟิลด์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fcbd5-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="fcbd5-141">ในฟิลด์เกณฑ์ ให้พิมพ์ '000148'</span><span class="sxs-lookup"><span data-stu-id="fcbd5-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="fcbd5-142">ในฟิลด์เกณฑ์ "ใบสั่งขาย" ให้พิมพ์หมายเลขใบสั่ง 000148</span><span class="sxs-lookup"><span data-stu-id="fcbd5-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="fcbd5-143">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="fcbd5-143">Click OK.</span></span>
11. <span data-ttu-id="fcbd5-144">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="fcbd5-144">Click OK.</span></span>
    * <span data-ttu-id="fcbd5-145">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="fcbd5-145">Review the generated output.</span></span> <span data-ttu-id="fcbd5-146">โปรดทราบว่าสำหรับแต่ละเอกสารแนบจะมีการสร้างโหนด XML เดียว </span><span class="sxs-lookup"><span data-stu-id="fcbd5-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="fcbd5-147">ระบบจะเติมเนื้อหาของเอกสารแนบกับผลลัพธ์ XML ในรูปแบบข้อความ MIME (base64)</span><span class="sxs-lookup"><span data-stu-id="fcbd5-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]