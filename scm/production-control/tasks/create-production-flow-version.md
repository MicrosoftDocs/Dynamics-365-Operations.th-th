--- 
title: "สร้างเวอร์ชันขั้นตอนการผลิต"
description: "กระบวนงานนี้มุ่งเน้นสร้างเวอร์ชันใหม่ของขั้นตอนการผลิต "
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="0b238-103">สร้างเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="0b238-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b238-104">กระบวนงานนี้มุ่งเน้นสร้างเวอร์ชันใหม่ของขั้นตอนการผลิต </span><span class="sxs-lookup"><span data-stu-id="0b238-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="0b238-105">สำหรับกระบวนงานนี้ พารามิเตอร์การผลิตสำหรับ Lean Manufacturing และหน่วยวัดเวลาต้องถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="0b238-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="0b238-106">คุณต้องกำหนดสายธารคุณค่าและกลุ่มการผลิตอีกด้วย </span><span class="sxs-lookup"><span data-stu-id="0b238-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="0b238-107">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับขั้นตอนการผลิตและกิจกรรมในการผลิตแบบ lean ดูเอกสารในการผลิตแบบ Lean สำหรับ Microsoft Dynamics AX </span><span class="sxs-lookup"><span data-stu-id="0b238-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="0b238-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="0b238-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="0b238-109">สร้างขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="0b238-109">Create a production flow</span></span>
1. <span data-ttu-id="0b238-110">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="0b238-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="0b238-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0b238-111">Click New.</span></span>
3. <span data-ttu-id="0b238-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="0b238-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0b238-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0b238-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b238-114">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0b238-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0b238-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0b238-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b238-116">เลือกหน่วยปฏิบัติงานของสายธารคุณค่า </span><span class="sxs-lookup"><span data-stu-id="0b238-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="0b238-117">สายธารคุณค่าเป็นหน่วยปฏิบัติงานหน่วยหนึ่งที่ครอบคลุมกิจกรรมและขั้นตอนของสายธารคุณค่าทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="0b238-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="0b238-118">ในขั้นตอนนี้หน่วยปฏิบัติงานจะจำกัดเฉพาะนิติบุคคลและได้ไม่มีฟังก์ชันเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0b238-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="0b238-119">ในฟิลด์กลุ่มผลิตภัณฑ์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0b238-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0b238-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0b238-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b238-121">เลือกกลุ่มการผลิตสำหรับขั้นตอนการผลิต </span><span class="sxs-lookup"><span data-stu-id="0b238-121">Select a production group for the production flow.</span></span> <span data-ttu-id="0b238-122">กลุ่มการผลิตอนุญาตคำนิยามของวัสดุ แรงงาน และบัญชี WIP สำหรับกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="0b238-122">Production groups allow the definition of material, labour, and WIP accounts for a production process.</span></span> <span data-ttu-id="0b238-123">การเชื่อมโยงบริบทบัญชีกับขั้นตอนการผลิตต้องเลือกกลุ่มการผลิต</span><span class="sxs-lookup"><span data-stu-id="0b238-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="0b238-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0b238-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="0b238-125">สร้างเวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="0b238-125">Create a production flow version</span></span>
1. <span data-ttu-id="0b238-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="0b238-126">Click Add.</span></span>
2. <span data-ttu-id="0b238-127">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="0b238-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="0b238-128">กำหนดวันหมดอายุสำหรับเวอร์ชัน ถ้ากำหนด </span><span class="sxs-lookup"><span data-stu-id="0b238-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="0b238-129">คุณสามารถอัพเดตวันหมดอายุของเวอร์ชันตลอดเวลาที่ระบุ แม้กระทั่งสำหรับเวอร์ชันที่ใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="0b238-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="0b238-130">คุณสามารถใช้วันหมดอายุของเวอร์ชันในการวางแผนสำหรับการออกของเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="0b238-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="0b238-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0b238-131">Click OK.</span></span>
4. <span data-ttu-id="0b238-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0b238-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="0b238-133">ในฟิลด์หน่วย ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="0b238-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="0b238-134">ResolveChangesหน่วยเวลาที่ใช้ในการผลิตแบบสมดุล</span><span class="sxs-lookup"><span data-stu-id="0b238-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="0b238-135">ในฟิลด์เวลาเฉลี่ยที่ใช้ในการผลิตแบบสมดุล ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0b238-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="0b238-136">กำหนดเวลาเฉลี่ยที่ใช้ในการผลิตแบบสมดุล </span><span class="sxs-lookup"><span data-stu-id="0b238-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="0b238-137">สำหรับการควบคุมการผลิตแบบสมดุลของเวอร์ชันขั้นตอนการผลิต กำหนดเวลาการผลิตแบบสมดุลเฉลี่ยเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="0b238-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="0b238-138">เวลาที่ใช้ในการผลิตแบบสมดุลถูกกำหนดเป็นปริมาณต่อรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="0b238-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="0b238-139">ตัวอย่างเช่น เวลาที่ใช้ในการผลิตแบบสมดุลคือ 0.2 ชั่วโมงต่อ 10 ชิ้น </span><span class="sxs-lookup"><span data-stu-id="0b238-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="0b238-140">สำหรับเวลาการทำงาน 8 ชั่วโมง ซึ่งตรงกับกำลังการผลิตปริมาณที่สามารถประมวลผลได้ประจำวัน 400 ชิ้น</span><span class="sxs-lookup"><span data-stu-id="0b238-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="0b238-141">ในฟิลด์ปริมาณต่อวงจร ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0b238-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="0b238-142">กำหนดปริมาณต่อวงจรที่เกี่ยวข้องกับเวลาเฉลี่ยที่ใช้ในการผลิตแบบสมดุล</span><span class="sxs-lookup"><span data-stu-id="0b238-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="0b238-143">สลับการขยายของส่วนรายละเอียดเวอร์ชั่น</span><span class="sxs-lookup"><span data-stu-id="0b238-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="0b238-144">ในฟิลด์เวลาที่น้อยที่สุดในการผลิตแบบสมดุล ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0b238-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="0b238-145">กำหนดเวลาที่ใช้ในการผลิตแบบสมดุลที่ต่ำที่สุด </span><span class="sxs-lookup"><span data-stu-id="0b238-145">Define the minimum takt time.</span></span> <span data-ttu-id="0b238-146">เวลาที่ใช้ในการผลิตแบบสมดุลที่ต่ำที่สุดต้องน้อยกว่าหรือเท่ากับเวลาเฉลี่ยสมดุล</span><span class="sxs-lookup"><span data-stu-id="0b238-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="0b238-147">ในฟิลด์เวลาที่มากที่สุดในการผลิตแบบสมดุล ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0b238-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="0b238-148">เวลาที่ใช้ในการผลิตแบบสมดุลที่สูงที่สุดต้องสูงกว่าหรือเท่ากับเวลาเฉลี่ยสมดุล</span><span class="sxs-lookup"><span data-stu-id="0b238-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="0b238-149">ในฟิลด์รอบระยะเวลาสำหรับเวลาวงจรจริง (วัน) ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0b238-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="0b238-150">ป้อนตัวเลขจำนวนวันในรอบระยะเวลาสำหรับเวลาวงจรจริง </span><span class="sxs-lookup"><span data-stu-id="0b238-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="0b238-151">รอบระยะเวลาสำหรับเวลาวงจรจริงคือจำนวนวันที่งานจะรวมอยู่จากนาทีจริงย้อนหลังเพื่อคำนวณเวลาวงจรจริง </span><span class="sxs-lookup"><span data-stu-id="0b238-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="0b238-152">ค่าสามารถเปลี่ยนได้ตลอดเวลาและใช้สำหรับการคำนวณเวลาวงจรจริงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0b238-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="0b238-153">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0b238-153">Click Save.</span></span>


