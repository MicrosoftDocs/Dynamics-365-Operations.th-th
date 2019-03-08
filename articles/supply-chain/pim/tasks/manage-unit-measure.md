---
title: จัดการหน่วยวัด
description: 'ขั้นตอนนี้แสดงวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง '
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e208b7f1faab77f2b97ff7b440a228656684fca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "358933"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="3a16a-103">จัดการหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="3a16a-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a16a-104">ขั้นตอนนี้แสดงวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง </span><span class="sxs-lookup"><span data-stu-id="3a16a-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="3a16a-105">คุณสามารถแนะนำขั้นตอนนี้โดยใช้ข้อมูลสาธิต หรือใช้ข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="3a16a-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="3a16a-106">ไปที่การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="3a16a-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="3a16a-107">คลิกหน่วย </span><span class="sxs-lookup"><span data-stu-id="3a16a-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="3a16a-108">สร้างหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="3a16a-108">Create a unit of measure</span></span>
1. <span data-ttu-id="3a16a-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3a16a-109">Click New.</span></span>
2. <span data-ttu-id="3a16a-110">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="3a16a-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="3a16a-111">ป้อนรหัสหรือสัญลักษณ์ที่จะใช้เมื่ออ้างอิงถึงหน่วยวัด </span><span class="sxs-lookup"><span data-stu-id="3a16a-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="3a16a-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3a16a-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3a16a-113">ป้อนชื่ออธิบายสำหรับหน่วยวัดในภาษาของระบบ</span><span class="sxs-lookup"><span data-stu-id="3a16a-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="3a16a-114">ในฟิลด์ประเภทของหน่วย ให้เลือกหนึ่งตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="3a16a-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="3a16a-115">ประเภทของหน่วยกำหนดตรรกะการจัดกลุ่ม เช่นพื้นที่ มวล หรือปริมาณ หน่วยวัดก็เป็นส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3a16a-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="3a16a-116">ในฟิลด์ความละเอียดทศนิยม ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="3a16a-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="3a16a-117">ระบุจำนวนของทศนิยมที่แปลงหน่วยวัดต้องปัดเศษเมื่อเสร็จสิ้นการคำนวณสำหรับหน่วยวัด </span><span class="sxs-lookup"><span data-stu-id="3a16a-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="3a16a-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3a16a-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="3a16a-119">กำหนดการแปลหน่วย</span><span class="sxs-lookup"><span data-stu-id="3a16a-119">Define unit translations</span></span>
1. <span data-ttu-id="3a16a-120">คลิกข้อความหน่วย</span><span class="sxs-lookup"><span data-stu-id="3a16a-120">Click Unit texts.</span></span>
2. <span data-ttu-id="3a16a-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3a16a-121">Click New.</span></span>
    * <span data-ttu-id="3a16a-122">ใช้ข้อความหน่วยเพื่อสร้างการแปล ID หรือสัญลักษณ์ที่แสดงถึงหน่วยวัดสำหรับใช้ในเอกสารภายนอกในภาษาเฉพาะของลูกค้า หรือผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="3a16a-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="3a16a-123">ในฟิลด์ภาษา ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="3a16a-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="3a16a-124">ในฟิลด์ข้อความ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="3a16a-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="3a16a-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3a16a-125">Click Save.</span></span>
6. <span data-ttu-id="3a16a-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3a16a-126">Close the page.</span></span>
7. <span data-ttu-id="3a16a-127">คลิกคำอธิบายหน่วยที่แปล </span><span class="sxs-lookup"><span data-stu-id="3a16a-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="3a16a-128">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3a16a-128">Click New.</span></span>
    * <span data-ttu-id="3a16a-129">กำหนดคำอธิบายภาษาเฉพาะสำหรับหน่วยวัด </span><span class="sxs-lookup"><span data-stu-id="3a16a-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="3a16a-130">ในฟิลด์ภาษา ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="3a16a-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="3a16a-131">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3a16a-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3a16a-132">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3a16a-132">Click Save.</span></span>
12. <span data-ttu-id="3a16a-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3a16a-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="3a16a-134">กำหนดกฎการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="3a16a-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="3a16a-135">คลิกการแปลงหน่วย </span><span class="sxs-lookup"><span data-stu-id="3a16a-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="3a16a-136">กำหนดกฎสำหรับการแปลงหน่วยวัดไปยังหน่วยวัดอื่นและจากหน่วยวัดอื่นในประเภทของหน่วยที่เลือก </span><span class="sxs-lookup"><span data-stu-id="3a16a-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="3a16a-137">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="3a16a-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="3a16a-138">ในฟิลด์ปัจจัย ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="3a16a-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="3a16a-139">ตัวแปลงระหว่าง "หน่วยต้นทาง" และ "หน่วยปลายทาง" </span><span class="sxs-lookup"><span data-stu-id="3a16a-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="3a16a-140">ตัวอย่างเช่น ตัวแปลงจากเซนติเมตรเป็นเมตรคือ 100 เนื่องจาก 100 เซนติเมตรเป็น 1 เมตร</span><span class="sxs-lookup"><span data-stu-id="3a16a-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="3a16a-141">ในฟิลด์หน่วยปลายทาง ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3a16a-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="3a16a-142">ในฟิลด์การปัดเศษ ให้เลือกหนึ่งตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="3a16a-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="3a16a-143">กำหนดวิธีการปัดเศษค่าที่แปลง </span><span class="sxs-lookup"><span data-stu-id="3a16a-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="3a16a-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3a16a-144">Click OK.</span></span>
7. <span data-ttu-id="3a16a-145">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3a16a-145">Close the page.</span></span>

