---
title: ตรวจสอบความถูกต้องของขั้นตอนการผลิตและรุ่น
description: 'ขั้นตอนนี้แสดงวิธีการสร้างขั้นตอนการผลิตใหม่และเวอร์ชันแรกสำหรับการผลิตแบบ lean '
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c30947d01cfb85ea3dbf1aa3e4ea8e092efd18cb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210260"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="be1be-103">ตรวจสอบความถูกต้องของขั้นตอนการผลิตและรุ่น</span><span class="sxs-lookup"><span data-stu-id="be1be-103">Validate a production flow and version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be1be-104">ขั้นตอนนี้แสดงวิธีการสร้างขั้นตอนการผลิตใหม่และเวอร์ชันแรกสำหรับการผลิตแบบ lean </span><span class="sxs-lookup"><span data-stu-id="be1be-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="be1be-105">ข้อกำหนดเบื้องต้น: ต้องกำหนดพารามิเตอร์การผลิตสำหรับการผลิตแบบ Lean และหน่วยวัดสำหรับเวลาคลาส</span><span class="sxs-lookup"><span data-stu-id="be1be-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="be1be-106">คุณต้องกำหนดสตรีมค่าและกลุ่มการผลิต </span><span class="sxs-lookup"><span data-stu-id="be1be-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="be1be-107">อ้างอิงถึงเอกสารใน Lean Manufacturing เพื่อทำความคุ้นเคยตัวคุณเองกับแนวคิดของขั้นตอนการผลิตและกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="be1be-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="be1be-108">ขั้นตอนนี้แสดงถึงนิติบุคคล USMF ในข้อมูลสาธิต </span><span class="sxs-lookup"><span data-stu-id="be1be-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="be1be-109">อย่างไรก็ตาม สมมติว่ามีการกำหนดค่านิติบุคคลสำหรับการผลิตแบบ Lean นิติบุคคลอื่น ๆ สามารถใช้</span><span class="sxs-lookup"><span data-stu-id="be1be-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="be1be-110">สร้างขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="be1be-110">Create a production flow</span></span>
1. <span data-ttu-id="be1be-111">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="be1be-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="be1be-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="be1be-112">Click New.</span></span>
3. <span data-ttu-id="be1be-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="be1be-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="be1be-114">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="be1be-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="be1be-115">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be1be-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="be1be-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be1be-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be1be-117">สตรีมค่าเป็นหน่วยปฏิบัติงานที่ครอบคลุมผ่านกิจกรรมทั้งหมดและขั้นตอนของสตรีมค่า </span><span class="sxs-lookup"><span data-stu-id="be1be-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="be1be-118">ในขั้นตอนนี้หน่วยปฏิบัติงานจะจำกัดเฉพาะนิติบุคคลและได้ไม่มีฟังก์ชันเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="be1be-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="be1be-119">ในฟิลด์กลุ่มผลิตภัณฑ์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be1be-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="be1be-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be1be-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be1be-121">กลุ่มการผลิตอนุญาตคำนิยามของวัสดุ แรงงาน และบัญชี WIP สำหรับกระบวนการผลิต </span><span class="sxs-lookup"><span data-stu-id="be1be-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="be1be-122">การเชื่อมโยงบริบทบัญชีกับขั้นตอนการผลิตต้องเลือกกลุ่มการผลิต</span><span class="sxs-lookup"><span data-stu-id="be1be-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="be1be-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="be1be-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="be1be-124">สร้างเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="be1be-124">Create a production flow version</span></span>
1. <span data-ttu-id="be1be-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="be1be-125">Click Add.</span></span>
2. <span data-ttu-id="be1be-126">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="be1be-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="be1be-127">คุณสามารถอัพเดตวันหมดอายุของเวอร์ชันตลอดเวลาที่ระบุ แม้กระทั่งสำหรับเวอร์ชันที่ใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="be1be-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="be1be-128">ใช้วันหมดอายุของเวอร์ชันในการวางแผนสำหรับการออกของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="be1be-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="be1be-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="be1be-129">Click OK.</span></span>
4. <span data-ttu-id="be1be-130">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be1be-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="be1be-131">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="be1be-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="be1be-132">เลือกหน่วยเวลาที่ใช้ในการผลิตแบบสมดุล</span><span class="sxs-lookup"><span data-stu-id="be1be-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="be1be-133">ในฟิลด์เวลาเฉลี่ยที่ใช้ในการผลิตแบบสมดุล ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="be1be-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="be1be-134">สำหรับการควบคุมการผลิตแบบสมดุลของเวอร์ชันขั้นตอนการผลิต กำหนดเวลาการผลิตแบบสมดุลเฉลี่ยเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="be1be-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="be1be-135">การผลิตแบบสมดุลถูกกำหนดเป็นปริมาณต่อรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="be1be-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="be1be-136">ในตัวอย่างที่กำหนด เวลาในการผลิตแบบสมดุลคือ 0.2 ชั่วโมงต่อ 10 ชิ้น </span><span class="sxs-lookup"><span data-stu-id="be1be-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="be1be-137">สำหรับเวลาการทำงาน 8 ชั่วโมง ซึ่งตรงกับกำลังการผลิตปริมาณที่สามารถประมวลผลได้ประจำวัน 400 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="be1be-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="be1be-138">ในฟิลด์ปริมาณต่อวงจร ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="be1be-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="be1be-139">ขยายหรือยุบส่วนรายละเอียดเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="be1be-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="be1be-140">ในฟิลด์เวลาที่น้อยที่สุดในการผลิตแบบสมดุล ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="be1be-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="be1be-141">เวลาที่ใช้ในการผลิตแบบสมดุลที่ต่ำที่สุดต้องน้อยกว่าหรือเท่ากับเวลาเฉลี่ยสมดุล</span><span class="sxs-lookup"><span data-stu-id="be1be-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="be1be-142">ในฟิลด์เวลาที่มากที่สุดในการผลิตแบบสมดุล ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="be1be-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="be1be-143">เวลาที่ใช้ในการผลิตแบบสมดุลที่สูงที่สุดต้องสูงกว่าหรือเท่ากับเวลาเฉลี่ยสมดุล</span><span class="sxs-lookup"><span data-stu-id="be1be-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="be1be-144">ป้อนจำนวนวันในรอบระยะเวลาสำหรับเวลาวงจรจริง</span><span class="sxs-lookup"><span data-stu-id="be1be-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="be1be-145">รอบระยะเวลาสำหรับเวลาวงจรจริงคือจำนวนวันที่งานจะรวมอยู่จากนาทีจริงย้อนหลังเพื่อคำนวณเวลาวงจรจริง </span><span class="sxs-lookup"><span data-stu-id="be1be-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="be1be-146">ค่าสามารถเปลี่ยนได้ตลอดเวลาและใช้สำหรับการคำนวณเวลาวงจรจริงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="be1be-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="be1be-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="be1be-147">Click Save.</span></span>

