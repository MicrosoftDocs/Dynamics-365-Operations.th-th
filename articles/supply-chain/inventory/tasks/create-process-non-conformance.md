---
title: สร้างและประมวลผลความสอดคล้องกัน
description: หัวข้อนี้อธิบายวิธีการดำเนินการจัดการความไม่สอดคล้อง โดยขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef9c3a06aed1d26e7f5648427178a5638027ec04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218692"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="cdec1-103">สร้างและประมวลผลความสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cdec1-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cdec1-104">หัวข้อนี้อธิบายวิธีการดำเนินการจัดการความไม่สอดคล้อง โดยขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="cdec1-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="cdec1-105">คุณสามารถรันการจัดทำเรกคอร์ดนี้ในบริษัทสาธิต USMF และสามารถใช้ค่าแนะนำ</span><span class="sxs-lookup"><span data-stu-id="cdec1-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="cdec1-106">โดยทั่วไป ทำกระบวนงานนี้ โดยเจ้าหน้าที่ในการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cdec1-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="cdec1-107">เป็นข้อกำหนดเบื้องต้น ดำเนินการคำแนะนำให้เสร็จสมบูรณ์ใน [ตรวจสอบคุณภาพของสินค้า](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)</span><span class="sxs-lookup"><span data-stu-id="cdec1-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="cdec1-108">เพื่อประมวลผลการอนุมัติของความไม่สอดคล้อง ผู้ใช้ที่รันการบันทึกงานต้องมีค่า "ชื่อ" ที่กำหนดบนหน้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cdec1-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="cdec1-109">การใช้บันทึกเอกสาร ผู้ใช้ต้องสามารถเรียกใช้ตัวเลือกผู้ใช้ในการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="cdec1-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="cdec1-110">เลือกใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cdec1-110">Select a quality order</span></span>
1. <span data-ttu-id="cdec1-111">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการสินค้าคงคลัง > งานประจำงวด > การจัดการคุณภาพ > ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="cdec1-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="cdec1-112">ในรายการ เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นใน [ตรวจสอบคุณภาพของสินค้า](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)</span><span class="sxs-lookup"><span data-stu-id="cdec1-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="cdec1-113">สร้างความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cdec1-113">Create a nonconformance</span></span>
1. <span data-ttu-id="cdec1-114">บนบานหน้าต่างการดำเนินการ เลือก **การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="cdec1-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="cdec1-115">เลือก **ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="cdec1-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="cdec1-116">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cdec1-116">Select **New**.</span></span>
4. <span data-ttu-id="cdec1-117">ในเมนูแบบหล่นลงของฟิลด์ **ชนิดปัญหา** ให้เลือกปัญหาที่พบในระหว่างกระบวนการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="cdec1-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="cdec1-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cdec1-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="cdec1-119">อนุมัติหรือปฏิเสธเรกคอร์ดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cdec1-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="cdec1-120">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="cdec1-120">Select **Functions**.</span></span>
2. <span data-ttu-id="cdec1-121">เลือก **อนุมัติความไม่สอดคล้อง**</span><span class="sxs-lookup"><span data-stu-id="cdec1-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="cdec1-122">ตัวอย่างนี้ อนุมัติความไม่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="cdec1-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="cdec1-123">ความไม่สอดคล้องที่ได้รับอนุมัติสามารถเชื่อมโยงกับการดำเนินงานที่เกี่ยวข้อง เพื่อบันทึกงานที่เสร็จสิ้นแล้วเป็นส่วนหนึ่งของการจัดการความไม่สอดคล้อง และ เช่นในหัวข้อนี้ การประมวลผลการจัดการการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="cdec1-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="cdec1-124">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cdec1-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="cdec1-125">สร้างการดำเนินการของการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="cdec1-125">Create a correction action</span></span>
1. <span data-ttu-id="cdec1-126">เลือก **การแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="cdec1-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="cdec1-127">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cdec1-127">Select **New**.</span></span>
3. <span data-ttu-id="cdec1-128">ในฟิลด์ **หมายเลขบุคลากร** ของแถวใหม่ ให้เลือกเรกคอร์ดที่ต้องการจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="cdec1-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="cdec1-129">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="cdec1-129">Click **Select**.</span></span>
5. <span data-ttu-id="cdec1-130">เลือก **แนบ**</span><span class="sxs-lookup"><span data-stu-id="cdec1-130">Select **Attach**.</span></span> <span data-ttu-id="cdec1-131">สร้างบันทึกย่อเกี่ยวกับการแก้ไข </span><span class="sxs-lookup"><span data-stu-id="cdec1-131">Create a note about the correction.</span></span> <span data-ttu-id="cdec1-132">ตัวอย่างนี้ การดำเนินการนั้นเพื่อ ติดต่อผู้จัดจำหน่ายเพื่ออธิบายกรณีไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cdec1-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="cdec1-133">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cdec1-133">Select **New**.</span></span>
7. <span data-ttu-id="cdec1-134">เลือก **หมายเหตุ**</span><span class="sxs-lookup"><span data-stu-id="cdec1-134">Select **Note**.</span></span> <span data-ttu-id="cdec1-135">โดยขึ้นอยู่กับการตั้งค่ารายงาน ชนิดเอกสารต่างๆ สามารถพิมพ์บนรายงานที่เกี่ยวข้องกับการจัดการความไม่สอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="cdec1-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="cdec1-136">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cdec1-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="cdec1-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdec1-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="cdec1-138">รักษาการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="cdec1-138">Maintain a correction</span></span>
1. <span data-ttu-id="cdec1-139">เลือก **ทำเครื่องหมายเป็นเสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="cdec1-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="cdec1-140">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cdec1-140">Select **OK**.</span></span>
3. <span data-ttu-id="cdec1-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdec1-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="cdec1-142">ปิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cdec1-142">Close a nonconformance</span></span>
1. <span data-ttu-id="cdec1-143">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="cdec1-143">Select **Functions**.</span></span>
2. <span data-ttu-id="cdec1-144">เลือก **ปิดความไม่สอดคล้อง**</span><span class="sxs-lookup"><span data-stu-id="cdec1-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="cdec1-145">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cdec1-145">Select **Yes**.</span></span>
4. <span data-ttu-id="cdec1-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cdec1-146">Close the pages.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]