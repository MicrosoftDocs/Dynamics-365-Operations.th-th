---
title: ตรวจสอบคุณภาพของสินค้า
description: 'ขั้นตอนนี้แสดงให้คุณเห็นถึงวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ '
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "315440"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="78b6b-103">ตรวจสอบคุณภาพของสินค้า</span><span class="sxs-lookup"><span data-stu-id="78b6b-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78b6b-104">ขั้นตอนนี้แสดงให้คุณเห็นถึงวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ </span><span class="sxs-lookup"><span data-stu-id="78b6b-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="78b6b-105">คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="78b6b-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="78b6b-106">ก่อนที่คุณเริ่มกระบวนการตัวอย่างนี้ คุณจำเป็นต้องยืนยันใบสั่งซื้อ "000016" และลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="78b6b-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="78b6b-107">ซึ่งจะสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="78b6b-107">This will automatically create a quality order.</span></span> <span data-ttu-id="78b6b-108">ตรวจสอบคุณภาพจะโดยทั่วไปจะดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="78b6b-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="78b6b-109">เลือกใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="78b6b-109">Select a quality order</span></span>
1. <span data-ttu-id="78b6b-110">ไปที่การบริหารสินค้าคงคลัง > งานประจำงวด > การจัดการคุณภาพ > ใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="78b6b-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="78b6b-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78b6b-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="78b6b-112">เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นก่อนที่คุณเริ่มต้นขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="78b6b-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="78b6b-113">บันทึกผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="78b6b-113">Record test results</span></span>
1. <span data-ttu-id="78b6b-114">คลิก ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="78b6b-114">Click Results.</span></span>
2. <span data-ttu-id="78b6b-115">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="78b6b-115">Click Edit.</span></span>
3. <span data-ttu-id="78b6b-116">ในฟิลด์ปริมาณผลลัพธ์ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="78b6b-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="78b6b-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78b6b-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="78b6b-118">ในฟิลด์ผลที่ได้ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78b6b-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="78b6b-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="78b6b-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78b6b-120">ในตัวอย่างนี้ ผลลัพธ์จะขึ้นอยู่กับผลลัพธ์กำหนดไว้ </span><span class="sxs-lookup"><span data-stu-id="78b6b-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="78b6b-121">โดยปกติแล้วคุณจะบันทึกผลการทดสอบเฉพาะเจาะจงยิ่งขึ้น ตัวอย่างเช่นขนาดหรือมิติอื่น</span><span class="sxs-lookup"><span data-stu-id="78b6b-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="78b6b-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78b6b-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="78b6b-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="78b6b-123">Click Save.</span></span>
9. <span data-ttu-id="78b6b-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="78b6b-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="78b6b-125">ตรวจสอบความถูกต้องของใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="78b6b-125">Validate the quality order</span></span>
1. <span data-ttu-id="78b6b-126">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="78b6b-126">Click Validate.</span></span>
2. <span data-ttu-id="78b6b-127">ในฟิลด์ตรวจสอบความถูกต้อง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="78b6b-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="78b6b-128">เลือกผู้ดำเนินการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="78b6b-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="78b6b-129">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78b6b-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="78b6b-130">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="78b6b-130">Click Select.</span></span>
5. <span data-ttu-id="78b6b-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="78b6b-131">Click OK.</span></span>
6. <span data-ttu-id="78b6b-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="78b6b-132">Close the page.</span></span>

