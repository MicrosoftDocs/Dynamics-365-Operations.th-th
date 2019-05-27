---
title: สร้างและประมวลผลความสอดคล้องกัน
description: 'ใช้กระบวนงานนี้เพื่อดำเนินการจัดการไม่สอดคล้องกัน ขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่ '
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572822"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="f3c73-103">สร้างและประมวลผลความสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3c73-104">ใช้กระบวนงานนี้เพื่อดำเนินการจัดการไม่สอดคล้องกัน ขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="f3c73-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="f3c73-105">คุณสามารถรันการจัดทำเรกคอร์ดนี้ในบริษัทสาธิต USMF และสามารถใช้ค่าแนะนำ</span><span class="sxs-lookup"><span data-stu-id="f3c73-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="f3c73-106">โดยทั่วไป ทำกระบวนงานนี้ โดยเจ้าหน้าที่ในการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f3c73-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="f3c73-107">เป็นข้อกำหนดเบื้องต้น รันการบันทึกภารกิจ "ตรวจสอบคุณภาพของสินค้า"</span><span class="sxs-lookup"><span data-stu-id="f3c73-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="f3c73-108">เพื่อกระบวนการการอนุมัติของความไม่สอดคล้อง ผู้ใช้ที่รันบันทึกงานต้องมีค่า "ชื่อ" กำหนดบนหน้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f3c73-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="f3c73-109">การใช้บันทึกเอกสาร ผู้ใช้ต้องสามารถเรียกใช้ตัวเลือกผู้ใช้ในการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="f3c73-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f3c73-110">เลือกใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f3c73-110">Select a quality order</span></span>
1. <span data-ttu-id="f3c73-111">ไปที่ใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f3c73-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="f3c73-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f3c73-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f3c73-113">เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นจากการบันทึกงาน "ตรวจสอบคุณภาพของสินค้า"</span><span class="sxs-lookup"><span data-stu-id="f3c73-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="f3c73-114">สร้างความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-114">Create a nonconformance</span></span>
1. <span data-ttu-id="f3c73-115">คลิกการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="f3c73-115">Click Inquiries.</span></span>
2. <span data-ttu-id="f3c73-116">คลิกความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-116">Click Non conformances.</span></span>
3. <span data-ttu-id="f3c73-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f3c73-117">Click New.</span></span>
4. <span data-ttu-id="f3c73-118">ในฟิลด์ชนิดปัญหา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f3c73-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f3c73-119">เลือกปัญหาที่พบในระหว่างกระบวนการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f3c73-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="f3c73-120">ในฟิลด์ชนิดปัญหา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f3c73-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f3c73-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f3c73-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f3c73-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f3c73-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f3c73-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f3c73-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="f3c73-124">อนุมัติหรือปฏิเสธเรกคอร์ดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="f3c73-125">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-125">Click Functions.</span></span>
2. <span data-ttu-id="f3c73-126">คลิกอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="f3c73-127">ตัวอย่างนี้ อนุมัติความไม่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="f3c73-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="f3c73-128">ความไม่สอดคล้องที่ได้รับอนุมัติสามารถเชื่อมโยงกับการดำเนินงานที่เกี่ยวข้องเพื่อบันทึกงานที่เสร็จสิ้นแล้วเป็นส่วนหนึ่ง ของการจัดการไม่สอดคล้องกัน และ เช่น ในงานนี้บันทึก การประมวลผลการแก้ไขการจัดการ</span><span class="sxs-lookup"><span data-stu-id="f3c73-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="f3c73-129">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f3c73-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="f3c73-130">สร้างการดำเนินการของการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="f3c73-130">Create a correction action</span></span>
1. <span data-ttu-id="f3c73-131">คลิกการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="f3c73-131">Click Corrections.</span></span>
2. <span data-ttu-id="f3c73-132">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f3c73-132">Click New.</span></span>
3. <span data-ttu-id="f3c73-133">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f3c73-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f3c73-134">ในฟิลด์หมายเลขบุคลากร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f3c73-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f3c73-135">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f3c73-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f3c73-136">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="f3c73-136">Click Select.</span></span>
7. <span data-ttu-id="f3c73-137">คลิกแนบ</span><span class="sxs-lookup"><span data-stu-id="f3c73-137">Click Attach.</span></span>
    * <span data-ttu-id="f3c73-138">สร้างบันทึกย่อเกี่ยวกับการแก้ไข </span><span class="sxs-lookup"><span data-stu-id="f3c73-138">Create a note about the correction.</span></span> <span data-ttu-id="f3c73-139">ตัวอย่างนี้ การดำเนินการนั้นเพื่อ ติดต่อผู้จัดจำหน่ายเพื่ออธิบายกรณีไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="f3c73-140">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f3c73-140">Click New.</span></span>
9. <span data-ttu-id="f3c73-141">คลิกหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="f3c73-141">Click Note.</span></span>
    * <span data-ttu-id="f3c73-142">โปรดสังเกตว่า ขึ้นอยู่กับการตั้งค่ารายงาน ชนิดเอกสารต่าง ๆ สามารถพิมพ์บนรายงานที่เกี่ยวข้องกับการจัดการไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="f3c73-143">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f3c73-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f3c73-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f3c73-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="f3c73-145">รักษาการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="f3c73-145">Maintain a correction</span></span>
1. <span data-ttu-id="f3c73-146">คลิกทำเครื่องหมายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f3c73-146">Click Mark complete.</span></span>
2. <span data-ttu-id="f3c73-147">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f3c73-147">Click OK.</span></span>
3. <span data-ttu-id="f3c73-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f3c73-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="f3c73-149">ปิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-149">Close a nonconformance</span></span>
1. <span data-ttu-id="f3c73-150">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-150">Click Functions.</span></span>
2. <span data-ttu-id="f3c73-151">คลิกปิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="f3c73-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="f3c73-152">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="f3c73-152">Click Yes.</span></span>
4. <span data-ttu-id="f3c73-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f3c73-153">Close the page.</span></span>
5. <span data-ttu-id="f3c73-154">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f3c73-154">Close the page.</span></span>
