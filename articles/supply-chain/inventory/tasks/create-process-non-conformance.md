---
title: "สร้างและประมวลผลความสอดคล้องกัน"
description: "ใช้กระบวนงานนี้เพื่อดำเนินการจัดการไม่สอดคล้องกัน ขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่ "
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="ca86c-103">สร้างและประมวลผลความสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-103">Create and process a conformance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca86c-104">ใช้กระบวนงานนี้เพื่อดำเนินการจัดการไม่สอดคล้องกัน ขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="ca86c-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="ca86c-105">คุณสามารถรันการจัดทำเรกคอร์ดนี้ในบริษัทสาธิต USMF และสามารถใช้ค่าแนะนำ</span><span class="sxs-lookup"><span data-stu-id="ca86c-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="ca86c-106">โดยทั่วไป ทำกระบวนงานนี้ โดยเจ้าหน้าที่ในการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ca86c-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="ca86c-107">เป็นข้อกำหนดเบื้องต้น รันการบันทึกภารกิจ "ตรวจสอบคุณภาพของสินค้า"</span><span class="sxs-lookup"><span data-stu-id="ca86c-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="ca86c-108">เพื่อกระบวนการการอนุมัติของความไม่สอดคล้อง ผู้ใช้ที่รันบันทึกงานต้องมีค่า "ชื่อ" กำหนดบนหน้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ca86c-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="ca86c-109">การใช้บันทึกเอกสาร ผู้ใช้ต้องสามารถเรียกใช้ตัวเลือกผู้ใช้ในการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="ca86c-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="ca86c-110">เลือกใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ca86c-110">Select a quality order</span></span>
1. <span data-ttu-id="ca86c-111">ไปที่ใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="ca86c-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="ca86c-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ca86c-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ca86c-113">เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นจากการบันทึกงาน "ตรวจสอบคุณภาพของสินค้า"</span><span class="sxs-lookup"><span data-stu-id="ca86c-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="ca86c-114">สร้างความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-114">Create a nonconformance</span></span>
1. <span data-ttu-id="ca86c-115">คลิกการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="ca86c-115">Click Inquiries.</span></span>
2. <span data-ttu-id="ca86c-116">คลิกความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-116">Click Non conformances.</span></span>
3. <span data-ttu-id="ca86c-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ca86c-117">Click New.</span></span>
4. <span data-ttu-id="ca86c-118">ในฟิลด์ชนิดปัญหา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="ca86c-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ca86c-119">เลือกปัญหาที่พบในระหว่างกระบวนการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="ca86c-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="ca86c-120">ในฟิลด์ชนิดปัญหา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="ca86c-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ca86c-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ca86c-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ca86c-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ca86c-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ca86c-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ca86c-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="ca86c-124">อนุมัติหรือปฏิเสธเรกคอร์ดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="ca86c-125">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-125">Click Functions.</span></span>
2. <span data-ttu-id="ca86c-126">คลิกอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="ca86c-127">ตัวอย่างนี้ อนุมัติความไม่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="ca86c-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="ca86c-128">ความไม่สอดคล้องที่ได้รับอนุมัติสามารถเชื่อมโยงกับการดำเนินงานที่เกี่ยวข้องเพื่อบันทึกงานที่เสร็จสิ้นแล้วเป็นส่วนหนึ่ง ของการจัดการไม่สอดคล้องกัน และ เช่น ในงานนี้บันทึก การประมวลผลการแก้ไขการจัดการ</span><span class="sxs-lookup"><span data-stu-id="ca86c-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="ca86c-129">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="ca86c-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="ca86c-130">สร้างการดำเนินการของการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="ca86c-130">Create a correction action</span></span>
1. <span data-ttu-id="ca86c-131">คลิกการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="ca86c-131">Click Corrections.</span></span>
2. <span data-ttu-id="ca86c-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ca86c-132">Click New.</span></span>
3. <span data-ttu-id="ca86c-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ca86c-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ca86c-134">ในฟิลด์หมายเลขบุคลากร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="ca86c-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ca86c-135">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ca86c-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ca86c-136">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="ca86c-136">Click Select.</span></span>
7. <span data-ttu-id="ca86c-137">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="ca86c-137">Click Attach.</span></span>
    * <span data-ttu-id="ca86c-138">สร้างบันทึกย่อเกี่ยวกับการแก้ไข </span><span class="sxs-lookup"><span data-stu-id="ca86c-138">Create a note about the correction.</span></span> <span data-ttu-id="ca86c-139">ตัวอย่างนี้ การดำเนินการนั้นเพื่อ ติดต่อผู้จัดจำหน่ายเพื่ออธิบายกรณีไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="ca86c-140">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ca86c-140">Click New.</span></span>
9. <span data-ttu-id="ca86c-141">คลิกหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="ca86c-141">Click Note.</span></span>
    * <span data-ttu-id="ca86c-142">โปรดสังเกตว่า ขึ้นอยู่กับการตั้งค่ารายงาน ชนิดเอกสารต่าง ๆ สามารถพิมพ์บนรายงานที่เกี่ยวข้องกับการจัดการไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="ca86c-143">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ca86c-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="ca86c-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ca86c-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="ca86c-145">รักษาการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="ca86c-145">Maintain a correction</span></span>
1. <span data-ttu-id="ca86c-146">คลิกทำเครื่องหมายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ca86c-146">Click Mark complete.</span></span>
2. <span data-ttu-id="ca86c-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ca86c-147">Click OK.</span></span>
3. <span data-ttu-id="ca86c-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ca86c-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="ca86c-149">ปิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-149">Close a nonconformance</span></span>
1. <span data-ttu-id="ca86c-150">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-150">Click Functions.</span></span>
2. <span data-ttu-id="ca86c-151">คลิกปิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ca86c-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="ca86c-152">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="ca86c-152">Click Yes.</span></span>
4. <span data-ttu-id="ca86c-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ca86c-153">Close the page.</span></span>
5. <span data-ttu-id="ca86c-154">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ca86c-154">Close the page.</span></span>

