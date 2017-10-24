--- 
title: "จัดการหน่วยวัด"
description: "ขั้นตอนนี้แสดงวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง "
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="fc6c0-103">จัดการหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="fc6c0-103">Manage unit of measure</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc6c0-104">ขั้นตอนนี้แสดงวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง </span><span class="sxs-lookup"><span data-stu-id="fc6c0-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="fc6c0-105">คุณสามารถแนะนำขั้นตอนนี้โดยใช้ข้อมูลสาธิต หรือใช้ข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="fc6c0-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="fc6c0-106">ไปที่การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="fc6c0-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="fc6c0-107">คลิกหน่วย </span><span class="sxs-lookup"><span data-stu-id="fc6c0-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="fc6c0-108">สร้างหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="fc6c0-108">Create a unit of measure</span></span>
1. <span data-ttu-id="fc6c0-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fc6c0-109">Click New.</span></span>
2. <span data-ttu-id="fc6c0-110">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="fc6c0-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="fc6c0-111">ป้อนรหัสหรือสัญลักษณ์ที่จะใช้เมื่ออ้างอิงถึงหน่วยวัด </span><span class="sxs-lookup"><span data-stu-id="fc6c0-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="fc6c0-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fc6c0-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fc6c0-113">ป้อนชื่ออธิบายสำหรับหน่วยวัดในภาษาของระบบ</span><span class="sxs-lookup"><span data-stu-id="fc6c0-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="fc6c0-114">ในฟิลด์ประเภทของหน่วย ให้เลือกหนึ่งตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="fc6c0-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="fc6c0-115">ประเภทของหน่วยกำหนดตรรกะการจัดกลุ่ม เช่นพื้นที่ มวล หรือปริมาณ หน่วยวัดก็เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fc6c0-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="fc6c0-116">ในฟิลด์ความละเอียดทศนิยม ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="fc6c0-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="fc6c0-117">ระบุจำนวนของทศนิยมที่แปลงหน่วยวัดต้องปัดเศษเมื่อเสร็จสิ้นการคำนวณสำหรับหน่วยวัด </span><span class="sxs-lookup"><span data-stu-id="fc6c0-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="fc6c0-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fc6c0-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="fc6c0-119">กำหนดการแปลหน่วย</span><span class="sxs-lookup"><span data-stu-id="fc6c0-119">Define unit translations</span></span>
1. <span data-ttu-id="fc6c0-120">คลิกข้อความหน่วย</span><span class="sxs-lookup"><span data-stu-id="fc6c0-120">Click Unit texts.</span></span>
2. <span data-ttu-id="fc6c0-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fc6c0-121">Click New.</span></span>
    * <span data-ttu-id="fc6c0-122">ใช้ข้อความหน่วยเพื่อสร้างการแปล ID หรือสัญลักษณ์ที่แสดงถึงหน่วยวัดสำหรับใช้ในเอกสารภายนอกในภาษาเฉพาะของลูกค้า หรือผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="fc6c0-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="fc6c0-123">ในฟิลด์ภาษา ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="fc6c0-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="fc6c0-124">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="fc6c0-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="fc6c0-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fc6c0-125">Click Save.</span></span>
6. <span data-ttu-id="fc6c0-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc6c0-126">Close the page.</span></span>
7. <span data-ttu-id="fc6c0-127">คลิกคำอธิบายหน่วยที่แปล </span><span class="sxs-lookup"><span data-stu-id="fc6c0-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="fc6c0-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fc6c0-128">Click New.</span></span>
    * <span data-ttu-id="fc6c0-129">กำหนดคำอธิบายภาษาเฉพาะสำหรับหน่วยวัด </span><span class="sxs-lookup"><span data-stu-id="fc6c0-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="fc6c0-130">ในฟิลด์ภาษา ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="fc6c0-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="fc6c0-131">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fc6c0-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="fc6c0-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fc6c0-132">Click Save.</span></span>
12. <span data-ttu-id="fc6c0-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc6c0-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="fc6c0-134">กำหนดกฎการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="fc6c0-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="fc6c0-135">คลิกการแปลงหน่วย </span><span class="sxs-lookup"><span data-stu-id="fc6c0-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="fc6c0-136">กำหนดกฎสำหรับการแปลงหน่วยวัดไปยังหน่วยวัดอื่นและจากหน่วยวัดอื่นในประเภทของหน่วยที่เลือก </span><span class="sxs-lookup"><span data-stu-id="fc6c0-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="fc6c0-137">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="fc6c0-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="fc6c0-138">ในฟิลด์ปัจจัย ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="fc6c0-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="fc6c0-139">ตัวแปลงระหว่าง "หน่วยต้นทาง" และ "หน่วยปลายทาง" </span><span class="sxs-lookup"><span data-stu-id="fc6c0-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="fc6c0-140">ตัวอย่างเช่น ตัวแปลงจากเซนติเมตรเป็นเมตรคือ 100 เนื่องจาก 100 เซนติเมตรเป็น 1 เมตร</span><span class="sxs-lookup"><span data-stu-id="fc6c0-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="fc6c0-141">ในฟิลด์หน่วยปลายทาง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fc6c0-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="fc6c0-142">ในฟิลด์การปัดเศษ ให้เลือกหนึ่งตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="fc6c0-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="fc6c0-143">กำหนดวิธีการปัดเศษค่าที่แปลง </span><span class="sxs-lookup"><span data-stu-id="fc6c0-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="fc6c0-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fc6c0-144">Click OK.</span></span>
7. <span data-ttu-id="fc6c0-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc6c0-145">Close the page.</span></span>


